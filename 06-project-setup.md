# Project Setup

The project was designed and implemented in AWS, where the team agreed to operate under a single AWS account. This approach ensured consistent resource management and simplified billing, while still allowing the team to assign individual IAM roles and permissions for security and accountability.


## Choice of Cloud Tools: GuardDuty, VPC, S3, and CloudWatch

To maintain an enterprise-aligned approach, the project team prioritized automation and security-focused AWS services for building and managing resources. GuardDuty was implemented to provide continuous monitoring for malicious or unauthorized activity, ensuring early detection of potential threats. A Virtual Private Cloud (VPC) was configured with subnet segmentation and routing controls to simulate enterprise-grade network architecture. Amazon S3 was used for hosting and storing project data, while CloudWatch enabled logging, monitoring, and alerting to track system performance and suspicious activity. 

By integrating these services into the project workflow, the project ensured that the environment remained secure, reproducible, and aligned with best practices for cloud operations and monitoring.
