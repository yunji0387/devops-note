# OWASP Application SSecurity Risks

## Table of Content
1. [Intro to OWASP (Top 10) Sec Vulnerabilities](#intro)
2. [OWASP Top 1-3](#owasp1_3)
3. [OWASP Top 4-6](#owasp4_6)
4. [OWASP Top 7-10](#owasp7_10)
5. [Discover Code Vulnerabilities with Snyk (SAST) Free Tool](#discover_synk_tool)
6. [SQL Injections](#sql_injections)
7. [Other Types of SQL Injection Atack](#other_sql_injections)
8. [Example of an SQL Injection](#sql_injection_example)
9. [Cross Site Scripting](#cross_site_scripting)
10. [Storing Secrets Securely](#storing_secrets)

---

<a id="intro"></a>
# Introduction to Security Testing and Mitigation Strategies
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

## What is OWASP?
- **OWASP**: Open Web Application Security Project, formed in 2003, focuses on improving software security.
- **Purpose**: Provides the security industry with the OWASP Top 10, a consensus-based report on current software security vulnerabilities.
- **Usage**: Globally recognized as a standard for checking web application security.

## Current OWASP Top 10 (2021)
1. **Broken Access Control**: Risks information disclosure and data integrity.
2. **Cryptographic Failures**: Concerns data exposure.
3. **Injection**: Involves hostile data use and unsafe queries.
4. **Insecure Design**: Relates to flaws in control designs.
5. **Security Misconfiguration**: Involves incorrectly enabled features or configuration issues.
6. **Vulnerable and Outdated Components**: Issues with version control and compatibility.
7. **Identification and Authentication Failures**: Covers password issues and automated attacks like credential stuffing.
8. **Software and Data Integrity Failures**: Concerns integrity violations from untrusted sources.
9. **Security Logging and Monitoring Failures**: Involves the detection and response to breaches.
10. **Server-Side Request Forgery**: Leads to URL validation failures.

## Developing the OWASP Top 10
- **Step 1**: Plan a schedule and publish a call for data.
- **Step 2**: Determine survey content and request industry participation.
- **Step 3**: Collect, normalize, and analyze the data.
- **Step 4**: Determine categories from data and survey, and release a draft for public review.
- **Step 5**: Reach a consensus and release the updated list.

## Key Takeaways
- **Understanding OWASP**: It's essential for software security and is supported by a broad consensus within the security community.
- **Using the OWASP Top 10**: It helps identify risks, improve processes, and secure code in any organization.
- **Development Process**: Involves extensive data collection and community involvement to ensure the list remains relevant and accurate.

<!-- /MarkdownTOC -->
</details>

---

<a id="owasp1_3"></a>
# OWASP Top 1-3
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

## 1. Broken Access Control
### Description
- **What it is**: A failure where attackers gain unauthorized access to perform actions outside of an application's intended permissions.
- **Implications**: Can lead to data modification, deletion, and unauthorized actions, potentially resulting in security breaches and financial losses.

### Prevention Strategies
- **Assign Limited Privileges**: Restrict users to necessary permissions to prevent unauthorized actions.
- **Regular Access Control Audits**: Conduct frequent checks to ensure appropriate access levels are maintained.
- **Minimize Public Information**: Limit the exposure of application details to prevent exploitation.
- **Disable Directory Listings**: Prevent exposure of file paths in URLs to secure web server directories.
- **Monitor and Respond to Access Control Failures**: Ensure system administrators are alerted to and address any access control failures in server logs.

## 2. Cryptographic Failures
### Description
- **What it is**: Inadequate encryption that leads to the exposure of sensitive data.
- **Implications**: Attackers can decrypt or access sensitive information, leading to data breaches.

### Prevention Strategies
- **Use Authenticated Encryption**: Encrypt all sensitive data in the database and during transmission using robust methods.
- **Implement HTTPS**: Secure data in transit by using HTTPS over HTTP to prevent interceptions.
- **Avoid Outdated Protocols**: Replace protocols like SMTP and FTP with more secure alternatives to mitigate man-in-the-middle attacks.
- **Secure Encryption Keys**: Manage keys carefully, avoid hardcoding them, ensure they are backed up, and store them securely.

## 3. Injection
### Description
- **What it is**: Execution of unintended commands due to untrusted data being sent to an interpreter.
- **Implications**: Allows hackers unauthorized access to data, potentially leading to data theft and system compromise.

### Prevention Strategies
- **Use Secure APIs**: Opt for APIs that either avoid using the interpreter or provide a parameterized interface.
- **Sanitize Inputs**: Block special characters and keywords using an escape list and regularly update this list.
- **Regularly Update Keyword Filters**: Ensure filters are current to prevent newly discovered vulnerabilities from being exploited.
- **Sanitize SQL Statements**: Verify and clean data used in SQL statements to prevent SQL injection.

## Key Takeaways
- **Common Vulnerabilities**: The top threats include broken access control, cryptographic failures, and injection attacks.
- **Strategic Prevention**: Implementing rigorous access control, using robust encryption, and sanitizing inputs are crucial.
- **Impact of Vulnerabilities**: These vulnerabilities can severely affect an application's security, potentially leading to significant financial and reputational damage.

<!-- /MarkdownTOC -->
</details>

---

<a id="owasp4_6"></a>
# OWASP Top 4-6
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->


<!-- /MarkdownTOC -->
</details>

---

<a id="owasp7_10"></a>
# OWASP Top 7-10
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->


<!-- /MarkdownTOC -->
</details>

---

<a id="discover_synk_tool"></a>
# Discover Code Vulnerabilities with Snyk (SAST) Free Tool
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->


<!-- /MarkdownTOC -->
</details>

---

<a id="sql_injections"></a>
# SQL Injections
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->


<!-- /MarkdownTOC -->
</details>

---

<a id="other_sql_injections"></a>
# Other Types of SQL Injection Atack
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->


<!-- /MarkdownTOC -->
</details>

---

<a id="sql_injection_example"></a>
# Example of an SQL Injection
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->


<!-- /MarkdownTOC -->
</details>

---

<a id="cross_site_scripting"></a>
# Cross Site Scripting
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->


<!-- /MarkdownTOC -->
</details>

---

<a id="storing_secrets"></a>
# Storing Secrets Securely
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->


<!-- /MarkdownTOC -->
</details>

---

<a id="storing_secrets"></a>
# Storing Secrets Securely
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->


<!-- /MarkdownTOC -->
</details>

---
