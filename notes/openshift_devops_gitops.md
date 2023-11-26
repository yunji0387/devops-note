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

# CI/CD with OpenShift Pipelines

## Overview
- **Objective**: Understanding OpenShift Pipelines and how they enhance CI/CD practices using Tekton.
- **Definition**: OpenShift Pipelines is a cloud-native CI/CD solution built on Kubernetes, using Tekton as its foundation.

## Understanding OpenShift Pipelines
1. **Functionality**: Automates building, testing, and deploying applications in Kubernetes.
2. **Integration**: Works seamlessly with Kubernetes, leveraging its scalability and flexibility.

## Benefits of OpenShift Pipelines
- **Kubernetes Tool Integration**: Integrates tools like Kubecontrol, Helm, and operators.
- **Scalability & Reusability**: Handles larger workloads and allows reusing pipeline templates.
- **Platform Compatibility**: Supports deployment across various platforms (on-premise, cloud, hybrid).

## Core Concepts Shared with Tekton
- **Events, Triggers, Pipelines, Tasks, Steps**: Fundamental building blocks for CI/CD workflows.

## OpenShift-Specific Features
1. **Resources**: Handles inputs/outputs like repositories, images, and configurations.
2. **Conditions**: Sets criteria for task execution within pipelines.
3. **Pipeline Run & Task Run**: Represents execution instances of pipelines and tasks.
4. **Additional Components**:
   - **Web Console**: Simplifies pipeline management and monitoring.
   - **Event-Based Triggers**: Automates pipeline triggering.
   - **Security**: Leverages OpenShift's authentication and authorization.
   - **Built-In Services**: Integrates services like image registries and storage.
   - **Pipeline Templates**: Facilitates reusability of pipeline patterns.

## Using OpenShift Pipelines
1. **Verification**: Confirm installation via the OpenShift Web Console.
2. **Pipeline Builder**: Graphical tool for creating and managing pipelines.
3. **Task Catalog**: Repository of predefined and community-contributed tasks.
4. **Pipeline Creation & Execution**:
   - Create and name a new pipeline.
   - Add tasks from the task catalog.
   - Configure task parameters.
   - Visually connect tasks and define execution order.
   - Save and execute the pipeline.
5. **Monitoring**: View pipeline execution and task logs for insights.

## Conclusion
- **Key Learnings**:
   - OpenShift Pipelines builds upon Tekton, adding an abstraction layer for ease of use.
   - Integrates deeply with Kubernetes and OpenShift ecosystem.
   - Enhances the CI/CD workflow with a user-friendly interface and robust features.

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
