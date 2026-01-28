# Business Scenario
Primary Region: Africa **(Cape Town) af-south-1** 
- Closest AWS region to African customers
- Supports core AWS services

**E-Commerce APP Scenario** User requests are first resolved through Route 53 and accelerated via CloudFront edge locations to ensure a responsive experience for the African user base. This perimeter is secured by AWS WAF and end-to-end SSL/TLS certificates provided by ACM. Once traffic reaches the regional ALB, it is balanced across EC2 instances residing in separate Availability Zones for maximum fault tolerance. The backend architecture separates concerns by storing product media in S3 (secured via SSE-KMS) and relational records in a Multi-AZ RDS instance. Frequently accessed datasets are offloaded to ElastiCache to reduce database load. For governance and performance tracking, the entire lifecycle is monitored by CloudWatch and audited through CloudTrail.

## E-Commerce AWS Architectural Design

![E-Commerce Application](https://github.com/Irene890/Images/blob/main/E-commerce%20APP.jpg)

