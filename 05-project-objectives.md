# Project Objectives

## Red Team Objectives (Atack & Exploit)
- Perform reconnaissance on the Voyage & Virtue website and supporting infrastructure.
- Attempt to gain initial access through login portals and other exposed entry points.
- Explore privilege escalation paths and lateral movement opportunities.
- Conduct simulated data exfiltration using tokened assets from guest and employee portals.
- Emulate attacker behavior to validate defensive coverage.

## Blue Team Objectives (Detect & Respond)
- Deploy GuardDuty, CloudWatch, and EventBridge for real-time monitoring of AWS resources.
- Detect unauthorized access attempts and privilege escalation activities.
- Trigger Canary tokens embedded in static web assets to identify adversary interaction.
- Correlate alerts across multiple sources to improve fidelity of detection.
- Execute response actions including IAM lockouts, VPC flow log analysis, and alert escalation.
- Capture findings to refine Purple Team playbooks and inform lessons learned.
