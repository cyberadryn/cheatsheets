# 🌐 OWASP Top 10 - Cheat Sheet (2023 Edition)

Stay secure by mastering the top 10 most critical web application security risks.

---

## 🥇 A01:2021 – Broken Access Control

**❗ Description:**  
Improper restriction of authenticated users to access resources or actions outside their privileges.

**🛡️ Prevention:**  
- Enforce server-side access controls  
- Deny by default  
- Use role-based access control (RBAC)  
- Avoid exposing object references in URLs  

---

## 🔐 A02:2021 – Cryptographic Failures *(Formerly Sensitive Data Exposure)*

**❗ Description:**  
Sensitive data (e.g. passwords, credit cards) is not protected during transit or at rest.

**🛡️ Prevention:**  
- Use HTTPS (TLS 1.2 or 1.3 only)  
- Don’t store sensitive data unnecessarily  
- Use strong, modern cryptographic algorithms (AES-256, SHA-256)  
- Use proper key management practices  

---

## 💥 A03:2021 – Injection

**❗ Description:**  
Unsanitized input allows attackers to execute malicious commands (e.g., SQL, OS, LDAP).

**🛡️ Prevention:**  
- Use parameterized queries (e.g., `PreparedStatement`)  
- Validate and sanitize all user inputs  
- Use ORM libraries  
- Employ allow-lists  

---

## 🧑‍💻 A04:2021 – Insecure Design

**❗ Description:**  
Flawed architectural or design patterns that expose systems to risk.

**🛡️ Prevention:**  
- Threat model your app  
- Apply secure design principles (e.g., least privilege, fail-safe defaults)  
- Define security stories and abuse cases  
- Conduct design reviews  

---

## 🛠️ A05:2021 – Security Misconfiguration

**❗ Description:**  
Default settings, open S3 buckets, unnecessary features enabled, or verbose error messages.

**🛡️ Prevention:**  
- Harden all environments  
- Disable unnecessary features  
- Automate secure configuration management  
- Use security headers (e.g., CSP, X-Frame-Options)  

---

## 🪪 A06:2021 – Vulnerable and Outdated Components

**❗ Description:**  
Use of outdated or vulnerable libraries, plugins, and frameworks.

**🛡️ Prevention:**  
- Inventory components and their versions  
- Subscribe to security advisories  
- Use tools like Dependabot, OWASP Dependency-Check  
- Apply patches regularly  

---

## 🧪 A07:2021 – Identification and Authentication Failures

**❗ Description:**  
Weak or misconfigured authentication allows unauthorized access.

**🛡️ Prevention:**  
- Use multi-factor authentication (MFA)  
- Enforce strong password policies  
- Implement secure session management  
- Use standard authentication libraries (e.g., OAuth2, OpenID Connect)  

---

## 🧯 A08:2021 – Software and Data Integrity Failures

**❗ Description:**  
Code or data is modified without verification, leading to potential compromise (e.g., CI/CD attacks).

**🛡️ Prevention:**  
- Use signed packages  
- Verify code integrity in pipelines  
- Enforce code reviews  
- Protect CI/CD pipelines with secrets management  

---

## 🕵️ A09:2021 – Security Logging and Monitoring Failures

**❗ Description:**  
Missing or ineffective logging and alerting, making it hard to detect or respond to breaches.

**🛡️ Prevention:**  
- Log all critical events (login, access control changes, etc.)  
- Use centralized logging (e.g., ELK, SIEM)  
- Alert on suspicious activities  
- Retain logs securely  

---

## 🔄 A10:2021 – Server-Side Request Forgery (SSRF)

**❗ Description:**  
A vulnerable server can be tricked into sending requests to unintended destinations, such as internal resources.

**🛡️ Prevention:**  
- Validate and sanitize URLs  
- Block internal IP address ranges  
- Disable unnecessary URL fetch capabilities  
- Use network segmentation  

---

> 🔒 **Pro Tip:** Combine secure coding practices, regular testing, and developer training to stay ahead of threats.


