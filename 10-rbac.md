# Creating the IAM

Using Root user permission the network and Iam permission were set up and segmented by role, and protected by guardrails. Three user groups were created with least privilege policies to enforce hc-permnissionboundary. This enabled users to operate only on resources integral to their role. Some configurations included; Region and security controls include a region lock (hc-region-lock) that denies actions outside the team-east-1 and an MFA policy (hc-region-mfa) that requires multi-factor authentication for sensitive operations. 

Red and Blue Team Members were able to build, configure and manage core infrastructure such as EC2, VPC, S3, and EventBridge as well as manage SNS resources with a constrained topic prefix for alerting. 

Each group’s policies were scoped through managed and custom IAM rules. Permission boundaries were enforced to prevent privilege escalation, with policies requiring MFA and password reset upon login. Together, these permissions ensured that every user, service, and automated function operated within tightly scoped boundaries that balanced the needs of infrastructure deployment, adversarial simulation, and defensive monitoring, while maintaining security and cost-control across the environment.
