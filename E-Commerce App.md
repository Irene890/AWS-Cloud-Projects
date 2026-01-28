# Business Scenario
Primary Region: Africa **(Cape Town) af-south-1** 
- Closest AWS region to African customers
- Supports core AWS services

**E-Commerce APP Scenario** User access the application via Route 53 and Cloudfront, where WAF provides edge protection. CloudFront forwards traffic to a single Application Load Balancer deployed across two public subnets in separate Availability Zones. Once traffic reaches the regional ALB, it is balanced across EC2 instances residing in separate Availability Zones for maximum fault tolerance. The backend architecture separates concerns by storing product media in S3 (secured via SSE-KMS) and relational records in a Multi-AZ RDS instance. Frequently accessed datasets are offloaded to ElastiCache to reduce database load. For governance and performance tracking, the entire lifecycle is monitored by CloudWatch and audited through CloudTrail.

Users access the application via Route 53 and CloudFront, where AWS WAF provides edge protection. CloudFront forwards traffic to a single Application Load Balancer deployed across two public subnets in separate Availability Zones. The ALB routes requests to EC2 instances in two private subnets. Amazon Cognito is used separately for authentication, and the application stores relational data in a Multi-AZ RDS database while serving images from Amazon S3 via CloudFront.


## E-Commerce AWS Architectural Design

![E-Commerce Application](https://github.com/Irene890/Images/blob/main/E-Commerce%20App%20design.jpg)

