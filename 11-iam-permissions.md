# IAM Permissions and Team Access

IAM was used to enforce least privilege access while supporting the Blue Team (defenders) and Red Team (attackers). Each member was assigned access based on their function:

- **blue_user_1** – Console access with full logging and infrastructure visibility  
- **red_user_1** – Console access restricted only to the honeypot EC2 instance  
- **blue-team group** – Responsible for monitoring infrastructure and defensive visibility  
- **red-team group** – Simulated external attackers with no lateral movement privileges  

This structure ensured that the Blue Team could detect, investigate, and remediate incidents while the Red Team was constrained to attacker-like privileges, preventing unfair access to infrastructure data.
