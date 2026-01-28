# Business Scenario
Primary Region: Africa **(Cape Town) af-south-1** 
- Closest AWS region to African customers
- Supports core AWS services

**E-Commerce APP Summary** 
This solution is a secure, highly available, and cost-effective AWS architecture designed to support a low-latency e-commerce platform serving customers across Africa. The application is hosted in a single AWS Region (Africa – Cape Town) and deployed across 2 Availability Zones to eliminate single points of failure and ensure business continuity.

User traffic is routed through Amazon Route 53 and delivered via Amazon CloudFront, which provides fast content delivery and reduced latency. AWS WAF is integrated at the edge to protect the application from common web threats. An Application Load Balancer, deployed across two public subnets, distributes incoming requests to application servers running on Amazon EC2 in private subnets, ensuring the backend is not directly exposed to the internet.

User authentication and access management are handled by Amazon Cognito, providing secure sign-up, sign-in, and token-based authentication without increasing operational overhead. Relational customer and transaction data is stored in Amazon RDS with Multi-AZ support for high availability, while Amazon S3 is used for durable and cost-efficient storage of product images, delivered securely via CloudFront.

The architecture enforces strong security controls, including encryption of data at rest and in transit, least-privilege IAM access, network isolation using VPC subnets, and centralized monitoring and logging through Amazon CloudWatch and AWS CloudTrail. This design balances performance, security, availability, and cost, while remaining scalable to support future business growth.

## E-Commerce AWS Architectural Design

![E-Commerce Application](https://github.com/Irene890/Images/blob/main/E-Commerce%20App.drawio.png)

