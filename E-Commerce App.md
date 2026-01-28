* Scenario
Users across Africa resolve the application domain via Route 53, which routes traffic to CloudFront, cloudfront is protected by WAF.
CloudFront serves cached static content from edge locations and forwards dynamic requests to an Application Load Balancer deployed across two public subnets in separate Availability Zones.
The ALB routes traffic to EC2 instances running in public subnets across the same AZs. 
The application stores relational data in an Amazon RDS Multi-AZ deployment and caches frequently accessed data using ElastiCache. 
Product images are stored securely in Amazon S3, accessed by CloudFront for reads and by EC2 using IAM roles for uploads. 
The application uses Cloudwatch for centralized dashboard for performance metrics and alarms as well as Cloud trail for logging API calls for security auditing.

** Design
