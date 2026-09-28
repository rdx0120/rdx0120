# Rohan Anand Dalvi

**Security engineering · Detection & response · Security automation**

Hi, I'm Rohan. I work in healthcare IT and security, where I spend much of my time on endpoint monitoring, Wazuh detections, and vulnerability remediation.

The projects here build on that work and give me room to explore areas like AWS, security automation, and application security. I include testing and debugging notes so you can see how things work, what went wrong, and what still needs work.

I'm looking for a dedicated security engineering role where I can keep building tools and improving detections. I'm also working toward a longer-term focus on application security.

## Selected projects

### [Secure CI/CD Pipeline](https://github.com/rdx0120/secure-pipeline)
**Python · GitHub Actions · Semgrep · Terraform · OPA**

I built this pipeline to check what security scanners actually examined before trusting their results. It blocks runs when scan coverage can't be established. In my AWS lab, I also applied a Terraform plan after it passed OPA checks, inspected the deployed IAM permissions, and tested GitHub Actions access through OIDC.

[Code and setup](https://github.com/rdx0120/secure-pipeline#readme) · [Design and debugging lessons](https://github.com/rdx0120/secure-pipeline/blob/main/LESSONS.md) · [AI-use disclosure](https://github.com/rdx0120/secure-pipeline/blob/main/AI-USE.md)

### [Sigma Detection Pack](https://github.com/rdx0120/sigma-detection-pack)
**Sigma · Wazuh · Sysmon · MITRE ATT&CK**

A collection of Windows and Google Workspace detections, with test fixtures and notes on investigating alerts. I validated two endpoint detections against live Wazuh telemetry. The deployment notes cover the troubleshooting along the way, including rules that loaded successfully but never fired.

[Rules and setup](https://github.com/rdx0120/sigma-detection-pack#readme) · [Wazuh deployment notes](https://github.com/rdx0120/sigma-detection-pack/blob/main/runbooks/wazuh-deployment-notes.md)

### [KEV / EPSS Vulnerability Prioritizer](https://github.com/rdx0120/kev-epss-prioritizer)
**Python · Greenbone · Nessus · CISA KEV · FIRST EPSS**

This Python CLI helps decide which vulnerability findings to address first. It combines CISA KEV, EPSS scores, and asset context into a remediation queue with reasons and target dates. One detail I worked through was making sure a failed EPSS request could be retried instead of being saved as a missing score.

[Code, usage, and methodology](https://github.com/rdx0120/kev-epss-prioritizer#readme)

### [AWS Detection Lab](https://github.com/rdx0120/aws-detection-lab)
**CloudTrail · GuardDuty · Prowler · Sigma · Stratus Red Team**

I used an isolated AWS account to fix configuration findings and test detections against six emulated attack techniques. My custom rules matched the captured CloudTrail events for all six. I documented the results, the delay before logs became searchable, and the gaps I observed during testing.

[Lab walkthrough](https://github.com/rdx0120/aws-detection-lab#readme) · [Detection coverage and latency](https://github.com/rdx0120/aws-detection-lab/blob/main/docs/detection-latency-and-coverage.md) · [Remediation notes](https://github.com/rdx0120/aws-detection-lab/blob/main/docs/prowler-hipaa-remediation.md)

## Other projects

- **[YARAdec](https://github.com/rdx0120/YARAdec):** My rebuild of the original [YARA decompiler](https://github.com/jbgalet/yaradec) for YARA 4.x. This involved binary parsing, reconstructing rule logic, and comparing scan results before and after decompilation.
- **[Threat Model Casebook](https://github.com/rdx0120/threat-model-casebook):** Practice threat models for payment systems and a multi-tenant API, covering what could go wrong, which mitigations matter most, and what risks remain.
- **[Security Program Blueprint](https://github.com/rdx0120/one-person-security-program):** A plan for running a small security program, informed by my healthcare work. It distinguishes controls I've operated from improvements I've proposed.

## A note on the write-ups

I use AI tools during development and document that assistance alongside my own decisions, testing, and changes. The repositories also credit upstream projects and explain the limits of the results.

Outside these projects, I'm continuing to practice web application testing and secure code review.
