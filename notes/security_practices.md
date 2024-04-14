# Security Best Practices, Final Project, and Assessment

## Table of Content
1. [Code Practices](#code_practices)
2. [Dependencies](#dependencies)
3. [CodeQL Analysis](#codeql_analysis)
4. [Secure Development Environment](#secure_dev_env)
5. [Security Best Practices](#security_best_practices)


---

<a id="code_practices"></a>
# Code Practices
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

## Overview

Code practices are essential to the software development process, focusing on security within the DevOps community. By implementing robust code practices early, developers can prevent costly fixes later and reduce vulnerabilities in the application layer.

## General Code Practices

1. **Secure Software Development Lifecycle:**
   - Integrating security from the start of development ensures the application is secure throughout its lifecycle.

2. **Secure Coding Standards:**
   - Establish and follow a set of secure coding guidelines to cultivate good coding habits.

3. **Use of Tested Libraries and Code:**
   - Utilize tested and approved managed code and reusable object libraries to enhance efficiency and security.

4. **Secure Updating:**
   - Focus updates on exposed threats or security-critical components of the source code.

5. **Security Training:**
   - Participate in training courses focused on secure software development to increase security awareness and improve coding skills.

## Input Validation and Scrubbing

### Validation

- **Purpose:** Ensures the input matches the expected type, range, length, and characters.
- **Techniques:**
  - Check input against a whitelist of allowed characters.
  - Reject any input that doesn't meet predefined criteria.
  - Validate data from untrusted sources rigorously.

### Scrubbing

- **Purpose:** Removes or sanitizes any malicious characters entered as input.
- **Examples of Malicious Characters:** `<`, `>`, `"`, `'`, `%`, `()`, `&`, `+`, `\`, etc.
- **Control Measures:** If malicious characters are necessary inputs, apply additional controls like output encoding and use of secure APIs.

## Output Sanitization

- **Encoding:** Convert input code into safe output code for interpreters.
- **Sanitization:** Cleanse all output from untrusted sources to prevent injection attacks in SQL, XML, LDAP, or local OS commands.

## Error Handling and Security

- **Goal:** Provide useful error messages for users and diagnostic information for developers without aiding potential attackers.
- **Practices:**
  - Use custom error pages and generic error messages.
  - Release memory upon error conditions to prevent corruption.
  - Restrict access to logs and log tampering events or failures.

## Conclusion

Effective code practices are crucial for developing secure software. These practices not only enhance security but also reduce the overall risk and potential costs associated with later fixes. Input validation, scrubbing, and proper error handling are key components in mitigating security risks in software development.

<!-- /MarkdownTOC -->
</details>

---

<a id="dependencies"></a>
# Dependencies
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->


<!-- /MarkdownTOC -->
</details>

---

<a id="codeql_analysis"></a>
# CodeQL Analysis
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->


<!-- /MarkdownTOC -->
</details>

---

<a id="secure_dev_env"></a>
# Secure Development Environment
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->


<!-- /MarkdownTOC -->
</details>

---

<a id="security_best_practices"></a>
# Security Best Practices
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->


<!-- /MarkdownTOC -->
</details>

---
