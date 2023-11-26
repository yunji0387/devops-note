# DevOps and GitOps with OpenShift
Explore DevOps Pipeline

# Table of Contents
1. [Components of DevOps Pipeline](#devops_pipeline)
2. [CI/CD with OpenShift Pipelines](#cicd_with_openshift)
3. [Introduction to GitOps](#intro_to_gitops)

---


<a id="devops_pipeline"></a>
# Components of DevOps Pipeline
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

# Components of DevOps Pipeline

## Overview
- **Objective**: Understanding the structure and function of a DevOps pipeline, including its key components for CI/CD and compliance.
- **Definition**: A DevOps pipeline is an automated workflow that facilitates software delivery.

## Continuous Integration (CI) Pipeline
1. **Purpose**: Validates, packages, and builds components, creating deployable artifacts.
2. **Components**:
   - **Pull Requests**: Trigger PR pipeline for code validation.
   - **Issue Tracker**: Integrates with CI pipeline for issue resolution.
   - **Application Repository**: Stores source code for build and testing.
   - **Code Risk Analyzer**: Analyzes code for risks and vulnerabilities.
   - **Slack Integration**: Enables communication with development team.
   - **DevOps Insights**: Generates reports for performance improvement.
   - **SonarCube**: Manages code quality.
   - **Secrets Manager**: Secures sensitive information.
   - **Evidence & Inventory**: Stores artifacts and tracks deployments.

## Continuous Delivery (CD) Pipeline
1. **Purpose**: Deploys artifacts into target environments.
2. **Components**:
   - **Change Request Tool**: Manages and tracks system changes.
   - **Key Protect**: Stores cryptographic keys and sensitive information.
   - **Security & Compliance Center**: Enforces security and compliance policies.
   - **DevOps Insights & Secrets Manager**: Similar role as in CI pipeline.
   - **CD Workflow**: Automates deployment, security, and documentation processes.

## Continuous Compliance Pipeline
1. **Objective**: Maintains security and compliance standards throughout the development lifecycle.
2. **Workflow**:
   - **Static Code Analysis**: Validates application code against security and compliance rules.
   - **Compliance Checks**: Verifies industry-specific or regulatory compliance.
   - **Key Protect & Security Center**: Secures and evaluates compliance.
   - **DevOps Insights & Secrets Manager**: Collects data and manages sensitive information.
   - **Slack Notifications**: Informs team about pipeline status.
   - **Evidence Collection**: Demonstrates compliance through logs and artifacts.

## Conclusion
- **Utility of Pipelines**: Automates software delivery, ensuring quality, security, and compliance.
- **CI Pipeline**: Focuses on code validation, testing, and artifact creation.
- **CD Pipeline**: Responsible for artifact deployment and environment configuration.
- **Compliance Pipeline**: Ensures continuous alignment with security and regulatory standards.

<!-- /MarkdownTOC -->
</details>

---

<a id="cicd_with_openshift"></a>
# CI/CD with OpenShift Pipelines
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->



<!-- /MarkdownTOC -->
</details>

---

<a id="intro_to_gitops"></a>
# Introduction to GitOps
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->



<!-- /MarkdownTOC -->
</details>

---
