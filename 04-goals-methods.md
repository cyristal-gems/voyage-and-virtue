# Key Goals of the Project

The key goals of the project included deploying a secure VPC with subnet segmentation, IAM role-based access, and routing controls to simulate enterprise cloud architecture. Instead of relying on Infrastructure as Code (IaC) tools, the team utilized AWS-native services such as GuardDuty, CloudWatch, and S3 to establish monitoring, alerting, and data management within the environment.

 To test the resilience of the system, the Red Team conducted realistic attack simulations against the art website, focusing on the effectiveness of embedded honeypots and canary tokens as detection mechanisms. On the defensive side, logging and monitoring pipelines were integrated to identify malicious activity, contain intrusions, and enable corrective responses in real time. To maintain safety and efficiency, automation guardrails such as deny policies and self-destruct triggers on compromised resources were applied, ensuring the project remained secure and cost-effective. 

Finally, Purple-Team collaboration was emphasized through the development of concise playbooks that mapped MITRE ATT&CK techniques to detection and remediation steps, strengthening reporting accuracy and knowledge transfer between offensive and defensive roles.
