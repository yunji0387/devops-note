# Introduction to CI/CD

# Table of Contents
1. [What is CI/CD?](#what_is_cicd)
2. [Platform and Tools](#platform_and_tools)
3. [Infrastructure as Code (IaC)](#iac)

---

<a id="what_is_cicd"></a>
# What Is CI/CD?
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

## Key Objectives
- Understand Continuous Integration (CI) and Continuous Delivery (CD).
- Differentiate between CI and CD.
- Recognize the benefits of CI/CD.

## CI/CD Overview
- **CI/CD**: Two distinct processes, often mentioned together but not a single process.
- **Continuous Integration (CI)**: Integrating code back into the main branch regularly. Aims to prevent divergence and ensure compatibility.
- **Continuous Delivery (CD)**: Taking integrated code and deploying it, not necessarily to production.

## Definitions
- **Continuous Integration (CI)**: An automation process for integrating work into a repository. Facilitates team collaboration and quick bug detection.
- **Continuous Delivery (CD)**: Prepares code for release and automates deployment processes.

## Phases
- **CI Phases**: Plan, Code, Build, and Test.
- **CD Phases**: Release, Deploy, and Operate.

## Continuous Deployment
- Different from Continuous Delivery. Focuses on deploying to production environments.
- **Continuous Delivery**: Deployment to non-production environments.
- **Continuous Deployment**: Automatic deployment to production.

## CI/CD in DevOps
- Located in the Build and Test phases of the DevOps pipeline.

## Benefits of CI/CD
- Faster reaction to code changes.
- Reduced integration risk.
- Higher code quality.
- Main or master branch always deployable.
- Quicker and more reliable deployments.

## Summary Points
- CI and CD are sequential, distinct processes.
- CI involves code integration back into the main branch.
- CD prepares and deploys integrated code to various environments.
- Continuous Deployment focuses on production deployment.
- CI/CD offers significant benefits in software development processes.

<!-- /MarkdownTOC -->
</details>

---

<a id="platform_and_tools"></a>
# Platform and Tools
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

# ‘Platform and Tools’ Summary

## Objectives
- Recognize the viability of using diverse CI/CD tools.
- Identify common CI/CD tools.

## Key Insights
- **Tool Diversity**: Different teams within the same organization often use various tools for their CI/CD pipelines.
- **Tool Examples**: Jenkins, Travis CI, Circle CI, GitHub Actions, etc.
- **Flexibility**: The specific tool used is less important than the automation of processes.

## Common CI/CD Tools
- **Jenkins**: An older and complex CI/CD software installed on a server for central builds.
- **Circle CI**: Implements DevOps practices, performs Continuous Delivery, uses `circle.yaml` for workflows.
- **Travis CI**: A hosted CI service for GitHub and Bitbucket projects, supports open-source projects, uses `.travis.yaml` for workflows.
- **GitHub Actions**: Automates build, test, and deploy workflows, exclusively for GitHub.

## Conclusion
- Different tools for CI/CD are acceptable and often seen in diverse business lines.
- The focus should be on automation rather than manual processes.
- There is a wide array of CI/CD tools available, allowing teams to choose the one that best fits their needs.

<!-- /MarkdownTOC -->
</details>

---

<a id="iac"></a>
# Infrastructure as Code (IaC)
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

# Infrastructure as Code (IaC) Summary

## Overview
- **Infrastructure as Code (IaC)**: Method to manage and provision infrastructure through machine-readable definition files.
- **Key Concept**: Infrastructure setup and management using code, not manual processes.

## Benefits of IaC
- **Consistency and Repeatable Setups**: Ensures identical environments are created every time.
- **Error Reduction**: Minimizes manual errors in system configurations.
- **Rapid Provisioning**: Quick and efficient setup of development, test, and production environments.
- **Knowledge Preservation**: Codifies infrastructure setup, reducing dependency on individual expertise.
- **Cloud Computing Optimization**: Maximizes cloud benefits, such as scalability and cost-efficiency.

## Types of IaC Tools
- **Declarative (Specify 'What')**: Terraform, Puppet, SaltStack, CloudFormation, Ansible (partially).
- **Imperative (Specify 'How')**: Chef, Ansible (partially).

## Common IaC Tools
- **Terraform**: Open source, declarative, pre-execution checks.
- **Ansible**: Open source, simple setup, uses YAML, ideal for memory-constrained environments.
- **Chef**: Imperative, uses Ruby for "Cookbooks."
- **Puppet**: Declarative, platform-independent.
- **SaltStack**: Focuses on parallel execution and direct command issuance.

## Conclusion
- IaC has evolved from Configuration Management Systems (CMSs).
- Offers speed, efficiency, and reliability in infrastructure provisioning.
- Various tools available, each with unique features and approaches.

<!-- /MarkdownTOC -->
</details>

---
