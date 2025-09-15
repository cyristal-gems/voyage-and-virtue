# Voyage & Virtue: Honeypot-Canary AWS Environment Simulation
This repository provides a detailed account of the phase 2 cybersecurity capstone project, designed to replicate real-world offensive and defensive engagements in a controlled cloud environment. The honeypot-canary was built on Amazon Web Services (AWS), chosen for its scalability, security features, and ability to model enterprise-grade infrastructure within an academic setting. The exercise followed the Red Team vs. Blue Team methodology, which is widely used in cybersecurity training and operations. The Red Team functioned as the offensive group, attempting to compromise a simulated target environment by exploiting vulnerabilities, extracting sensitive information, and evading detection. In contrast, the Blue Team assumed a defensive role, responsible for architecting a secure environment, deploying monitoring tools, and responding to adversarial actions. To bridge these two perspectives, Purple Team practices were incorporated, emphasizing collaboration between attackers and defenders to improve overall organizational security posture.

---

## Executive Summary
Voyage & Virtue demonstrates deception-based cloud security in AWS by combining static S3 website hosting, Canary tokens, IAM role-based access, and GuardDuty monitoring. The project used a Red Team vs. Blue Team model with Purple Team facilitation, resulting in insights into adversary emulation, detection engineering, and defensive operations.

---

## MITRE ATT&CK Mapping
The project’s defensive measures were aligned with the MITRE ATT&CK framework to ensure that common adversary behaviors could be identified and countered.  
The table below summarizes the tactics, techniques, and detection strategies incorporated into the Voyage & Virtue environment.

| Tactic         | Technique ID | Technique Name                  | Detection/Defensive Action              |
|----------------|--------------|---------------------------------|-----------------------------------------|
| Initial Access | T1078        | Valid Accounts                  | IAM restrictions, GuardDuty alerts      |
| Discovery      | T1083        | File and Directory Discovery    | Canary tokens in deceptive directories  |
| Persistence    | T1136        | Create Account                  | IAM deny policies, automated teardown   |
| Exfiltration   | T1048        | Exfiltration Over Alt. Protocol | Canary tokens, CloudWatch monitoring    |
| Execution      | T1059        | Command and Scripting Interpreter | Honeypot logging and alerts           |

---

## Project Architecture

<img width="2600" height="1800" alt="voyageandvirturetopology" src="https://github.com/user-attachments/assets/1a9b9c84-d9e5-4c9f-b599-c1e6dc2757cc" />

---

## Table of Contents

- [Introduction](01-introduction.md)
- [Team Roles and Dynamics](02-team-roles.md)
- [Project Concept](03-project-concept.md)
- [Key Goals of the Project](04-goals-methods.md)
- [Project Objectives](05-project-objectives.md)
- [Project Setup](06-project-setup.md)
- [Planned Features](07-planned-features.md)
- [Network Architecture](08-network-architecture.md)
- [Network Environment](09-network-environment.md)
- [RBAC](10-rbac.md)
- [IAM Permissions and Team Access](11-iam-permissions.md)
- [Voyage & Virtue Website Setup](12-website-showcase.md)
- [Red Team Recon](13-redteam-recon.md)
- [Summary](14-summary.md)
- [Static Site Files](15-static-site/)
