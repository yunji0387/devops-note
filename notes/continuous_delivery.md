# Continuous Delivery (CD)

# Table of Contents
1. [What is Continuous Delivery (CD)](#what_is_cd)
2. [Continuous Delivery Key Principles](#cd_principles)
3. [Continuous Delivery Practices](#cd_practices)
4. [Tools of Continuous delivery (CD)](#tools_of_cd)
5. [Introduction to Tekton and Pipelines](#intro_to_tekton_and_pipelines)
6. [Building a Tekton Pipeline](#building_tekton_pipelines)
7. [Creating Tekton Triggers](#creating_tekton_triggers)
8. [Leveraging the Tekton Catalog](#leveraging_tekton_catalog)
9. [Creating Tasks for Quality Checks and Testing](#creating_tasks_for_quality_checks_and_testings)
10. [Building an Image](#building_image)
11. [Deploy to Kubernetes](#deploy_to_kubernetes)

---

<a id="what_is_cd"></a>
# What is Continuous Delivery (CD)
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

# What is Continuous Delivery?

## Overview
- **Objective**: Understand Continuous Delivery and its differentiation from Continuous Integration.

## Continuous Integration vs Continuous Delivery
- **Continuous Integration (CI)**: Involves integrating code into a main/master/trunk branch regularly to ensure compatibility and functionality.
- **Continuous Delivery (CD)**: Takes the integrated code and deploys it, possibly in various environments, but not necessarily each time CI occurs.

## Definition and Practice of Continuous Delivery
- **Definition**: Practices ensuring that code can be rapidly and safely deployed to production or production-like environments.
- **Key Aspects**:
  - Automated deployment to development, test, or staging environments.
  - Continuous Deployment refers specifically to automatic deployments to production.

## Goals of Continuous Delivery
- **Main Goal**: Enable software release to production at any time.
- **Requirements**:
  - Main/master branch must always be deployable.
  - Implement checks to prevent bad code from entering the main branch.
  - Utilize CI for testing during pull requests.
- **Benefits**:
  - Automates software transport through various stages of the SDLC.
  - Reduces deployment time and costs, including manual failures.
  - Increases deployment confidence and scalability.
  - Improves Quality Assurance across development, testing, and staging stages, leading to reliable production deployments.

## Key Takeaways
- CI/CD are distinct processes in software development.
- Continuous Delivery focuses on building software ready for release at any time.
- It involves deploying code automatically through various stages before production.
- Pull requests and feature branches ensure code reliability before merging.
- The process aims for bug-free, purpose-fit software in production.

<!-- /MarkdownTOC -->
</details>

---

<a id="cd_principles"></a>
# Continuous Delivery Key Principles
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

# Continuous Delivery Key Principles

## Overview
- **Objective**: Understand and describe the five key principles of Continuous Delivery.

## Five Key Principles

### 1. Build in Quality
- **Concept**: Ensure quality at every step of the development process.
- **Implementation**:
  - Plan for quality.
  - Utilize code reviews and quality checks in every pull request.

### 2. Work in Small Batches
- **Advantages**:
  - Reduces risk.
  - Easier to manage and integrate.
- **Approach**:
  - Keep user stories small.
  - Continuously integrate small changes with the base code.

### 3. Automate Repetitive Tasks
- **Issue**: People are inefficient at repetitive tasks.
- **Solution**:
  - Use automation for tasks like testing.
  - Examples: GitHub Actions for automated testing and integration.

### 4. Relentless Continuous Improvement
- **Philosophy**: Frequent practice leads to proficiency and reduced failure rates.
- **Process**:
  - Deliver changes to a known, working environment.
  - Constantly evaluate and improve processes.

### 5. Collective Responsibility
- **Culture**:
  - Avoid blame culture; focus on system improvement.
- **Responsibility**:
  - Everyone is accountable for their contribution.
  - Emphasize solving systemic issues over individual blame.

## Conclusion
- Continuous Delivery is about integrating quality, working in manageable increments, automating routine tasks, constantly improving processes, and fostering a culture of collective responsibility.
- The focus is on system efficiency and effectiveness, rather than individual performance.

<!-- /MarkdownTOC -->
</details>

---

<a id="cd_practices"></a>
# Continuous Delivery Practices
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->



<!-- /MarkdownTOC -->
</details>

---

<a id="tools_of_cd"></a>
# Tools of Continuous delivery (CD)
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->



<!-- /MarkdownTOC -->
</details>

---

<a id="intro_to_tekton_and_pipelines"></a>
# Introduction to Tekton and Pipelines
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->



<!-- /MarkdownTOC -->
</details>

---

<a id="building_tekton_pipelines"></a>
# Building a Tekton Pipeline
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->



<!-- /MarkdownTOC -->
</details>

---

<a id="creating_tekton_triggers"></a>
# Creating Tekton Triggers
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->



<!-- /MarkdownTOC -->
</details>

---

<a id="leveraging_tekton_catalog"></a>
# Leveraging the Tekton Catalog
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->



<!-- /MarkdownTOC -->
</details>

---

<a id="creating_tasks_for_quality_checks_and_testings"></a>
# Creating Tasks for Quality Checks and Testing
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->



<!-- /MarkdownTOC -->
</details>

---

<a id="building_image"></a>
# Building an Image
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->



<!-- /MarkdownTOC -->
</details>

---

<a id="deploy_to_kubernetes"></a>
# Deploy to Kubernetes
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->



<!-- /MarkdownTOC -->
</details>

---
