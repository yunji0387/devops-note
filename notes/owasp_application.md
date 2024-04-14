# OWASP Application Security Risks

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

## 1. Insecure Design
### Description
- **What it is**: Flaws in the design phase of application development that fail to include necessary security controls.
- **Consequences**: Makes applications susceptible to various cyber threats, such as brute force and OTP bypass attacks.

### Prevention Strategies
- **Security from the Start**: Integrate firewalls and other security measures during the design phase to combat specific threats.
- **Risk-Based Security**: Address potential architectural flaws early and ensure robust security by design to mitigate risks effectively.

## 2. Security Misconfiguration
### Description
- **What it is**: Incorrect or incomplete configurations that leave applications vulnerable to attacks.
- **Consequences**: Can lead to unauthorized access and data breaches, affecting application integrity and organizational reputation.

### Prevention Strategies
- **Principle of Least Privilege (PoLP)**: Ensure users have only the minimum necessary permissions.
- **Disable Unsafe Features**: Remove developer features like debug mode before deployment and ensure no unnecessary features are active.
- **Regular Configuration Audits**: Check for default usernames and passwords, clear text configuration files, and other vulnerabilities during the design phase and ongoing operations.
- **Involve System Administrators**: Combine the expertise of developers and system administrators to maintain secure configurations across all application layers.

## 3. Vulnerable and Outdated Components
### Description
- **What it is**: Use of outdated or unpatched software components that compromise security.
- **Consequences**: Leaves the application open to exploits, potentially delaying necessary patches and exposing the system to attack.

### Prevention Strategies
- **Regular Updates and Patch Management**: Stay informed about the latest patches and updates for all components.
- **Inventory Management**: Maintain a detailed list of all installed components, including versions and dependencies.
- **Eliminate Unused Dependencies**: Remove unnecessary features and dependencies to minimize attack surfaces.
- **Stay Informed**: Keep abreast of new security risks and vulnerabilities as reported by organizations like OWASP and CISA.

## Key Takeaways
- **Insecure Design**: Emphasize security controls during the initial design phase to avoid vulnerabilities that cannot be remedied later.
- **Security Misconfiguration**: Actively manage configurations and disable unnecessary features to prevent unauthorized access.
- **Vulnerable and Outdated Components**: Regularly update and patch all components to protect against known vulnerabilities and ensure functionality with evolving technologies.

<!-- /MarkdownTOC -->
</details>

---

<a id="owasp7_10"></a>
# OWASP Top 7-10
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

## 1. Identification and Authentication Failures
### Description
- **What it is**: Vulnerabilities that occur when authentication mechanisms are subverted through methods like credential stuffing and brute force attacks.
- **Consequences**: May lead to unauthorized access and impersonation, significantly compromising user data and system integrity.

### Prevention Strategies
- **Multifactor Authentication**: Use it to add an additional layer of security beyond just passwords.
- **Secure Session Management**: Implement server-side session management with secure, randomly generated session IDs that aren't exposed in URLs.
- **Software Supply Chain Security**: Utilize tools to scan and secure application components throughout the development lifecycle.

## 2. Software and Data Integrity Failures
### Description
- **What it is**: Failures that occur when software updates or data are tampered with due to inadequate verification processes.
- **Consequences**: Can lead to malicious code execution, data breaches, and compromised systems.

### Prevention Strategies
- **Segregated CI/CD Pipelines**: Ensure that the build and deployment environments are secure and access-controlled.
- **Digital Signatures and Integrity Checks**: Use these to verify the legitimacy and integrity of data and updates.
- **Regular Vulnerability Scanning**: Employ tools to scan for vulnerabilities in application components.

## 3. Security Logging and Monitoring Failures
### Description
- **What it is**: Inadequate logging of important system events and insufficient monitoring of these logs.
- **Consequences**: Delays in detecting and responding to security incidents, potentially allowing attackers to persist within systems undetected.

### Prevention Strategies
- **Comprehensive Logging**: Ensure all critical events are logged with sufficient detail.
- **Centralized Log Management**: Use tools like Logstash and Elasticsearch for log aggregation and analysis.
- **Effective Monitoring Systems**: Implement systems with real-time alerts to detect and respond to suspicious activities.

## 4. Server-Side Request Forgeries (SSRF)
### Description
- **What it is**: Attacks that exploit server functionality to induce a server to make requests that benefit the attacker.
- **Consequences**: Can lead to internal network enumeration, remote code execution, and data breaches.

### Prevention Strategies
- **Input Sanitization**: Validate all user-supplied input to ensure it does not contain malicious links or commands.
- **Use of Whitelists**: Enforce strict rules on permissible URLs, ports, and protocols.
- **Restrict HTTP Redirects and Response Handling**: Limit the server's ability to follow redirects or interact with unauthorized services.

## Key Takeaways
- **Identification and Authentication**: Strengthen authentication mechanisms and manage sessions securely.
- **Software and Data Integrity**: Guard against tampering and unauthorized changes in the software supply chain.
- **Logging and Monitoring**: Maintain robust logs and monitoring systems to quickly detect and mitigate threats.
- **SSRF Prevention**: Control how servers interact with external systems and data to prevent exploitation.

<!-- /MarkdownTOC -->
</details>

---

<a id="discover_synk_tool"></a>
# Discover Code Vulnerabilities with Snyk (SAST) Free Tool
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

## Objectives
After completing this reading, you will be able to:
- Describe the importance of Snyk.
- Explain various features and applications of Snyk.
- Describe the evolution and historical background of Snyk.
- Recognize various types of intended users of Snyk.

## Introduction to Snyk
Snyk is designed to aid developers by providing tools and strategies to manage open-source dependencies, identify vulnerabilities, and secure their codebases. Its key features include:
- **Dependability Scrutiny**: Scans codebases for vulnerabilities in open-source dependencies, offering insights and actionable steps for resolution.
- **Container Vigilance**: Scans container images to ensure they are protected from known security threats.
- **Persistent Surveillance**: Continuously monitors dependencies and containers, alerting users to new vulnerabilities.
- **Resolution and Correction**: Guides the remediation process by suggesting patches, updates, or safer package versions.
- **Harmonized Tool Integration**: Integrates seamlessly with development tools like code repositories, CI/CD pipelines, and issue tracking systems.
- **Security Frameworks**: Allows organizations to set and enforce security protocols defining acceptable risk levels.
- **Developer-Centric Approach**: Provides clear, actionable insights tailored for developers, embedding security naturally into the development process.
- **Broad Compatibility**: Supports a wide range of programming languages and package managers.

## Intended Users of Snyk
Snyk is intended for various roles within software development and management, including:
- **Developers**: Helps detect and fix security issues during code development.
- **DevOps Teams**: Ensures applications are secure throughout deployment.
- **Security Experts**: Assists in identifying vulnerabilities and collaborating on solutions.
- **Product Managers**: Ensures the product is secure and meets user requirements.
- **Open-Source Contributors**: Checks shared code for vulnerabilities.
- **App Managers**: Maintains application security and compliance.
- **Top Security Officials**: Oversees overall application and data security.
- **Compliance Teams**: Ensures software complies with relevant standards.
- **Cloud Native Teams**: Secures modern technologies like containers.

## Purpose of Snyk
Snyk's primary goal is to support software creators by identifying and fixing security vulnerabilities in code, dependencies, and infrastructure components. Key functionalities include:
- **Vulnerability Detection**: Identifies weak spots in software components.
- **Early Fixes**: Provides solutions to prevent minor issues from becoming major threats.
- **Guiding Solutions**: Offers advice on improving security postures.
- **Continuous Monitoring**: Stays vigilant for new vulnerabilities, ensuring timely responses.

## History of Snyk
Founded in 2015 by Guy Podjarny, Danny Grander, and Assaf Hefetz, Snyk aimed to enhance security in open-source software. Key milestones include:
- **2015**: Launch of Snyk to address open-source vulnerabilities.
- **2017**: Introduction of product offerings for vulnerability scanning.
- **2018**: Expansion into container security.
- **2019-2022**: Continued growth, feature enhancements, and integration with popular development tools.

## Similar Products to Snyk
Alternatives to Snyk include WhiteSource, SonarQube, Nexus Lifecycle, Veracode, Checkmarx, Black Duck, GitLab Security, GitHub Security, Aqua Security Trivy, and JFrog Xray. Each offers unique features that may suit different organizational needs.

## Conclusion
Snyk plays a crucial role in modern software development by integrating security directly into the development process, thereby helping developers, teams, and organizations build safer software efficiently.

<!-- /MarkdownTOC -->
</details>

---

<a id="sql_injections"></a>
# SQL Injections
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

## Objectives
After watching this video, you will be able to:
- Describe SQL injections and how they exploit databases.
- Identify four main types of SQL injection attacks.
- Explain the common SQL clauses and operators used in SQL injection attacks.

## What is an SQL Injection?
SQL injection is a type of security attack that allows attackers to interfere with the queries that an application makes to its database. It is typically done by inserting or "injecting" a malicious SQL query via input data from the client to the application.

## Types of SQL Injection Attacks
1. **SQL Manipulation**: This involves altering SQL commands to change their intended function. Examples include:
   - Modifying a `WHERE` clause to always return `TRUE`.
   - Using a `UNION` statement to retrieve data from other tables.
   
2. **Code Injection**: Injecting raw SQL code into a vulnerable SQL query to execute unintended commands.

3. **Function Call Injection**: Injecting SQL functions into queries to execute functions for data manipulation or other purposes.

4. **Buffer Overflow**: Overloading a database buffer with more data than it can handle, often leading to unexpected behavior or system crashes.

## How SQL Injections Work
- **Example of SQL Manipulation**:
  - Original SQL command: `SELECT * FROM users WHERE username = 'alice' AND password = 'mypassword';`
  - After manipulation: `SELECT * FROM users WHERE username = 'alice' AND password = 'mypassword' OR 'a' = 'a';`
  - This change forces the query to always return true, bypassing authentication.

- **Code Snippet Explanation**:
  - Code uses string concatenation to construct SQL queries based on user input.
  - Vulnerable input example: Username - `" OR 1=1` and Password - `" OR 1=1`.
  - Resulting malicious query: `SELECT * FROM Users WHERE Name = "" OR 1=1 AND Password = "" OR 1=1;`
  - This query will return all users because `1=1` is always true, bypassing all user authentication.

## Key SQL Clauses and Operators Used in Attacks
- **WHERE Clause**: Often manipulated to alter the logic of SQL queries.
- **UNION Operator**: Used to combine results from multiple SELECT statements into a single result.
- **Logical Operators** (`AND`, `OR`): Used to add conditions that always evaluate to true, compromising query integrity.

## Conclusion
You learned the dangers of SQL injections and how they are executed using simple modifications to SQL queries. You also saw the importance of sanitizing and validating all user inputs to prevent such attacks. SQL injections remain a critical threat to database security, and understanding them is key to safeguarding your applications.

<!-- /MarkdownTOC -->
</details>

---

<a id="other_sql_injections"></a>
# Other Types of SQL Injection Atack
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

## Key Points

### Types of SQL Injection Attacks

1. **Code Injection:**
   - Attackers insert new SQL statements into an existing SQL command.
   - Example: Adding `DELETE FROM users WHERE username = 'admin';` after a procedural command.
   - Risks: Can delete tables or entire databases.

2. **Function Call Injection:**
   - Custom functions are inserted into vulnerable SQL statements.
   - Example: Using `myappadmin.adduser('admin', 'newpass')` in a `TRANSLATE` function.
   - Purpose: Attackers execute unauthorized changes or transactions.

3. **Buffer Overflow:**
   - Occurs when data exceeds storage capacity of buffers in SQL functions.
   - Example: Exploiting functions like `tz_offset` and `to_timestamp_tz`.
   - Effect: Can cause system crashes or execute malicious code.

### Prevention Strategies

- **Use Query Parameters:**
  - Implement placeholders in SQL statements to prevent execution of injected code.
  - Example: `SELECT * FROM Users WHERE userid = ?;`

- **Server-Side Validation:**
  - Identify and sanitize untrusted data inputs.

- **Restrict User Privileges:**
  - Limit user permissions to minimize potential damage from attacks.

- **Regular Security Testing:**
  - Employ dynamic application security testing (DAST) to detect vulnerabilities.

## Key Takeaways

Understanding and mitigating different types of SQL injection attacks, such as code injection, function call injection, and buffer overflow, are crucial for protecting databases. Implementing preventative measures like using query parameters and conducting regular security tests are effective ways to secure applications against these attacks.

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

## Overview

Cross-site scripting (XSS) is a security vulnerability in which attackers execute malicious scripts in a user's browser through an application that sends untrusted data without proper validation or escaping. XSS is often abbreviated as "XSS" and can have various harmful effects on users and web applications.

## Types of Cross-Site Scripting Attacks

1. **Stored (Persistent) XSS:**
   - Malicious scripts are stored on a server or database.
   - Scripts execute whenever a user accesses the stored data.

2. **Blind XSS:**
   - Scripts execute in the background, unknown to users or administrators.
   - Often targets backend systems to compromise the application or server.

3. **Reflected XSS:**
   - Non-persistent and occurs when a script is reflected off a web server.
   - Typically delivered through phishing emails with malicious links.

## Preventative Measures

1. **Monitor HTTP Requests:**
   - Detect and block suspicious requests that may contain XSS code.
   - Example: Filtering out banned HTML tags and escape sequences.

2. **Data Sanitization:**
   - Escape special characters and block potentially harmful inputs.
   - Refactor code to eliminate unsafe functions and variables, like `innerHTML`.

3. **Disable HTTP TRACE:**
   - Turn off HTTP TRACE support on servers to prevent attackers from hijacking session cookies.

4. **Avoid Unsafe Sinks:**
   - Use safer alternatives like `textContent` for DOM manipulation.

## Example of an XSS Attack

- **Scenario:**
  - An attacker injects JavaScript into a web page using an input field meant for a credit card number.
  - Code Example: `page += "<input name='credit card' type='text' value='" + request.getParameter("CC") + "'>";`
  - The attacker modifies the "CC" parameter to include a script tag, redirecting the session ID to a malicious site.

## Key Takeaways

- XSS allows attackers to hijack sessions, deface websites, or redirect users to malicious sites.
- Understanding and defending against stored, blind, and reflected XSS is crucial for web application security.
- Implementing stringent input validation, proper escaping, and disabling unsafe features are effective strategies against XSS.

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
