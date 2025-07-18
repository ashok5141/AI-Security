# 🛡️ AI Security Learning Plan: Generative Models (LLMs)

**Duration**: 📅 6 Weeks  
**Time Commitment**: 1–2 hours/day  
**Goal**: Progress from beginner to expert in securing generative AI systems (e.g., ChatGPT, Copilot) by understanding fundamentals, OWASP Top 10 for LLMs, common vulnerabilities, threat modeling, mitigation, governance, and advanced techniques.

---

## Week 1: Foundations of Generative AI & Security Basics

| Day | Topic                                              | Resources                                                                                     |
|-----|----------------------------------------------------|----------------------------------------------------------------------------------------------|
| 1   | What is Generative AI?                             | https://www.paloaltonetworks.com/cyberpedia/what-is-generative-ai-security                    |
| 2   | How LLMs work (architecture & training)            | https://www.youtube.com/watch?v=ScaH1Y1DoFI                                                   |
| 3   | AI security threat landscape                       | https://aws.amazon.com/blogs/security/securing-generative-ai-an-introduction-to-the-generative-ai-security-scoping-matrix/ |
| 4   | Key attack surfaces in LLMs                        | https://www.nist.gov/itl/ai-risk-management-framework                                         |
| 5   | Prompt injection fundamentals                      | https://promptingguide.ai/risks/prompt-injection                                             |
| 6   | Data leakage & privacy concerns                    | https://arxiv.org/abs/2304.09751                                                              |
| 7   | Weekly recap & hands-on lab                        | Query an open LLM and test simple prompt injections                                           |

---

## Week 2: OWASP Top 10 for LLMs – Part I

| Day | Risk ID | Focus Area                       | Resources                                                                                  |
|-----|---------|----------------------------------|-------------------------------------------------------------------------------------------|
| 8   | A01     | Prompt Injection                 | https://owasp.org/www-project-top-10-for-large-language-model-applications/#a01           |
| 9   | A02     | Sensitive Information Disclosure | https://arxiv.org/abs/2304.09751                                                          |
| 10  | A03     | Supply Chain Vulnerabilities     | https://www.n-ix.com/generative-ai-security-risks/                                        |
| 11  | A04     | Model & Data Poisoning           | https://arxiv.org/abs/2004.00338                                                          |
| 12  | A05     | Improper Output Handling         | https://owasp.org/www-project-top-10-for-large-language-model-applications/#a05           |
| 13  | A06–A07 | Excessive Agency & Prompt Leakage| https://owasp.org/www-project-top-10-for-large-language-model-applications/#a06            |
| 14  | Review  | Recap OWASP A01–A07              | Build simple demos to trigger each risk                                                   |

---

## Week 3: OWASP Top 10 for LLMs – Part II

| Day | Risk ID | Focus Area                      | Resources                                                                                   |
|-----|---------|---------------------------------|--------------------------------------------------------------------------------------------|
| 15  | A08     | Embedding & Vector Weaknesses   | https://strobes.co/blog/owasp-top-10-risk-mitigations-for-llms-and-gen-ai-apps-2025/          |
| 16  | A09     | Misinformation & Hallucinations | https://incidentdatabase.ai/                                                               |
| 17  | A10     | Unbounded Resource Consumption  | https://www.nist.gov/itl/ai-risk-management-framework                                        |
| 18  | Deep Dive | Case Studies: real-world breaches | https://incidentdatabase.ai/                                                               |
| 19  | Lab       | Exploit A08–A10 on a sandbox LLM | Use a local LLaMA or Mistral instance                                                      |
| 20  | Recap     | OWASP Top 10 summary             | Write a short cheat sheet                                                                  |
| 21  | Review    | Blog post: “Mitigations & Best Practices” | https://www.ibm.com/products/tutorials/ibm-framework-for-securing-generative-ai              |

---

## Week 4: Threat Modeling & Adversarial Testing

| Day | Topic                                  | Resources                                                                                          |
|-----|----------------------------------------|---------------------------------------------------------------------------------------------------|
| 22  | STRIDE threat modeling for LLMs        | https://learn.microsoft.com/security/compass/stride-threat-modeling                                |
| 23  | Adversarial attacks & MITRE ATLAS      | https://atlas.mitre.org/                                                                          |
| 24  | Jailbreaking & prompt bypass           | https://llm-attacks.org/                                                                          |
| 25  | Secure prompt engineering techniques   | https://github.com/dair-ai/Prompt-Engineering-Guide                                                |
| 26  | Red teaming with PromptInject          | https://github.com/promptinject/promptinject                                                       |
| 27  | Tool exploration: LangChain Guardrails | https://docs.langchain.com/docs/security                                                            |
| 28  | Weekly recap & hands-on challenge      | Simulate a red-team exercise against a hosted LLM                                                  |

---

## Week 5: Mitigation Strategies & Secure Deployment

| Day | Topic                                     | Resources                                                                                         |
|-----|-------------------------------------------|--------------------------------------------------------------------------------------------------|
| 29  | Defense-in-depth for LLM APIs             | https://cloud.google.com/architecture/secure-ai                                                   |
| 30  | Rate limiting, input/output filtering     | https://docs.microsoft.com/azure/ai-services/                                                      |
| 31  | Model watermarking & fingerprinting       | https://arxiv.org/abs/2004.04410                                                                  |
| 32  | Differential privacy & secure training    | https://www.ibm.com/blog/privacy-in-gen-ai                                                        |
| 33  | Monitoring, logging & anomaly detection   | https://learn.microsoft.com/azure/security-center/azure-defender-for-iot-security-overview        |
| 34  | CI/CD pipeline security for LLMs          | https://owasp.org/www-project-secure-coding-practices/                                             |
| 35  | Weekly recap & secure deployment lab      | Deploy a minimal LLM service with logging and filters                                             |

---

## Week 6: Governance, Compliance & Advanced Topics

| Day | Topic                                       | Resources                                                                                          |
|-----|---------------------------------------------|---------------------------------------------------------------------------------------------------|
| 36  | AI governance frameworks (AI TRiSM)         | https://www.ibm.com/products/tutorials/ibm-framework-for-securing-generative-ai                    |
| 37  | Regulatory compliance (GDPR, ISO/IEC 42001) | https://www.iso.org/standard/81230.html                                                            |
| 38  | Ethical AI & bias mitigation                | https://www.partnershiponai.org/ai-ethics                                                         |
| 39  | Secure multi-model orchestration             | https://www.aivillage.org/                                                                        |
| 40  | Advanced red teaming & purple teaming       | https://mlsecops.com/                                                                             |
| 41  | Capstone project planning                   | Design end-to-end LLM security architecture                                                       |
| 42  | Final review & knowledge consolidation      | Prepare a presentation or write a blog summarizing your journey                                    |

---

## 🧰 Bonus Tools to Explore

- [PromptInject](https://github.com/promptinject/promptinject)
- [Guardrails AI](https://github.com/shreyashankar/gpt-guardrails)
- [AI Security Risks](https://www.n-ix.com/generative-ai-security-risks/)
- [LangChain Security](https://docs.langchain.com/docs/security)
- [LLM Attacks](https://llm-attacks.org/)
- [AI Incident Database](https://incidentdatabase.ai/)


## ✅ Tips for Success

- Take notes in Obsidian, Notion, or GitHub.
- Try hands-on testing with open-source LLMs (e.g., LLaMA, Mistral).
- Join communities like [AI Village](https://www.aivillage.org/) or [MLSecOps](https://mlsecops.com/).
- Stay updated with newsletters like [Import AI](https://www.importai.com/).
 


























## Resume
```bash
Ashok R
Email: ashokrmsec@gmail.com | Phone: +1 (337) 255-4378  
LinkedIn: linkedin.com/in/ashokreddyz | Portfolio: ashok5141.github.io  

SUMMARY  
Security Engineer with 6+ years in application and cloud security, specializing in secure SDLC, threat modeling, and DevSecOps automation. Proven ability to reduce vulnerabilities pre-production, secure cloud-native applications, and build scalable pipelines across AWS environments. OSCP candidate passionate about security tooling, leadership, and delivering measurable risk reduction.

SKILLS  
• Secure Code Review: Java, Python, JavaScript, OWASP Top 10, SAST/DAST, IAST  
• Cloud Security: AWS (IAM, KMS, Lambda, S3, EC2), Terraform, Prowler, Pacu  
• DevSecOps: GitHub Actions, Jenkins, SonarQube, Snyk, ZAP, TruffleHog  
• AppSec: Threat modeling (STRIDE), secure design reviews, CI/CD integration  
• Scripting: Python, Bash, PowerShell – security automation and payload development  
• Standards & Frameworks: NIST 800-53, SOC 2, MITRE ATT&CK, CIS Benchmarks  
• Tools: Burp Suite Pro, OWASP ZAP, Nmap, Scout Suite, Veracode, Wireshark  
• Other: Secret scanning, phishing simulations, internal AppSec training

EXPERIENCE

**Security Engineer**  
*ProBPM Inc* | Sep 2024 – Present  
• Conducted 25+ threat models across microservices, reducing high-risk issues by 35%  
• Remediated 150+ vulnerabilities via secure code reviews (Java, Python, JS) pre-production  
• Built CI-integrated SAST/DAST pipelines in GitHub Actions, reducing post-deployment issues by 40%  
• Automated security triage and secret scanning via Python, saving 20+ hours/week  
• Trained 80+ developers on secure coding, improving adoption by 50%  

**Research Assistant – AppSec & Cloud Security**  
*University of Louisiana at Lafayette* | Feb 2023 – May 2024  
• Designed threat models for IoT malware and Zigbee-based devices, reducing threats by 40%  
• Hardened AWS infra with Terraform, implemented logging standards and detection alerts  
• Developed Python-based anomaly detection in ELK, increasing incident response visibility  
• Conducted secure software design reviews aligned with NIST 800-53

**Application Security Engineer**  
*Network Intelligence* | Sep 2019 – Feb 2023  
• Performed manual and automated security testing on 80+ web/mobile/cloud applications  
• Integrated SAST/DAST/SCA tools (SonarQube, ZAP, Snyk) into Jenkins pipelines  
• Led secure architecture reviews and threat modeling sessions across business units  
• Automated secret scanning using TruffleHog, reducing leakage risk by 50%  
• Built dashboards for tracking vulnerability KPIs and remediation metrics  

**Senior Software Developer**  
*Maktron Global IT Solutions* | Jun 2017 – Sep 2019  
• Led secure dev of 8+ ASP.NET MVC apps with RBAC and OWASP ASVS compliance  
• Migrated databases to AWS RDS with encryption and IAM-based access controls  
• Authored threat-resilient design docs aligned with HIPAA and NIST guidance  

PROJECTS

**DevSecOps Pipeline with AWS**  
• Automated SAST/DAST with role-based CI triggers, reducing security bugs by 40%  
• Integrated Okta MFA in CI/CD, hardened Terraform deployments, enforced K8s RBAC  
• Built real-time dashboards for IAM drift, misconfig alerts, and security posture  

**AWS Cloud Penetration Testing**  
• Simulated privilege escalation with Pacu and mitigated STS abuse via SCP policies  
• Created custom Splunk detections for EC2 log abuse, brute-force, and beaconing  
• Auto-rotated 50+ leaked secrets using TruffleHog and AWS Secrets Manager  

EDUCATION  
**M.S. in Computer Science**, University of Louisiana at Lafayette, USA  
Relevant Coursework: Secure DevOps, Cryptography, AppSec, Cloud Security, AI Security  

**B.E. in Electronics & Communication**, Sri Mittapalli College of Engineering, India  
Final Project: Software Vulnerability Detection via CVE matching  

CERTIFICATIONS  
• CEH – Certified Ethical Hacker  
• OSCP – Offensive Security Certified Professional (In Progress)  
• Medal of Excellence – Cyber Excellence Academy  

ACHIEVEMENTS  
• Top 5% on HackTheBox CTFs – 200+ cloud/app/network challenges solved  
• Reduced prod vulnerabilities by 40% via AppSec automation  
• Awarded for driving org-wide secure coding training and AppSec adoption  

```