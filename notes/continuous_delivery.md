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

Welcome to ‘Continuous Delivery Practices.’ After watching this video, you will be able to describe Continuous Delivery best practices, explain the requirements of a CI/CD pipeline, and describe the differences between Continuous Deployment and Continuous Delivery. There are many best practices to follow when implementing Continuous Delivery. It’s important to make every change releasable. This means you should always include user documentation, operations runbooks, and information about what your change does. This ensures that every change will work and be documented well enough to be delivered to customers as well as serve any audit that may occur. You also need to keep in mind that Continuous Delivery is built upon Continuous Integration. As a best practice, you should avoid delaying any integration caused by long-lived branches. You want to use short-lived feature branches that are continuously integrated into the main codebase. This is also called trunk-based development because you always come back to the trunk, otherwise known as the master or main branch. Every change is built, tested, and deployed together for the fastest feedback. A well-constructed, automated delivery pipeline is integral to a successful Continuous Delivery implementation. This ensures that all code releases move into the test and production environments in a consistent, predictable way. Automate as many processes as possible. In Continuous Delivery, you must automate as many processes as possible in your software development lifecycle to create a good, reliable delivery pipeline. This pipeline is not only for code builds and deployments, but for the creation of new development environments as well. You want to aim for no downtime. To ensure application availability while you make frequent Continuous Delivery updates, when you push a new function to production, you must first validate it before deploying it to public-running application instances. You also want to release at the granularity of test. If two parts of the system must be tested together, they should be released together so that you know that the parts of your system are compatible. Release automation tools are good at coordinating this kind of delivery. Alternatively, you can fully decouple. A CI/CD pipeline requires several elements to be in place: You need a code repository to host and manage all source code. Your source code management system is the single version of the truth. Everything you need to build and release your code must be checked into version control. That code needs a build server to manage the building of the application. You want that environment to perform clean builds, starting from the same state every time. You need an integration server or orchestrator that handles the build automation and runs tests against your code. There should be no manual steps. Everything should be automated. And finally, you need a repository to store all the binaries and artifacts of the application so that once built and tested, they can be deployed easily. So, what’s the difference between Continuous Deployment and Continuous Delivery? Continuous Deployment can be part of a Continuous Delivery pipeline. Specifically, Continuous Delivery is the automated movement of code through the development lifecycle (or delivery lifecycle) once it passes the required automation tests. Continuous Deployment is taking that delivered code and deploying it to production. Whether and how Continuous Delivery is implemented all depends on your business needs. If your business needs the delivery team to release new or updated software to production repeatedly, reliably, and quickly, then Continuous Deployment will be of great benefit. In this video, you learned that there are several best practices to follow when implementing Continuous Delivery, a CI/CD pipeline requires a code repository, build server, integration server, and a storage repository, Continuous Delivery is the practice of automating the movement of code through the development lifecycle, and Continuous Deployment is the practice of taking the delivered code and deploying it into the production environment.

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
