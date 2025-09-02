# Network Environment

The project infrastructure was built within a dedicated VPC. A subnet was configured to support the honeypot EC2 instance, with routing directed to both local resources and the Internet Gateway for controlled inbound/outbound connectivity.

- VPC CIDR: 10.0.0.0/16
- Subnet CIDR: 10.0.32.0/20
- Route Table: Configured with routes to local VPC resources and the Internet Gateway
- Network ACLs & Security Groups: Restricted traffic according to Red/Blue team IAM
