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

# Continuous Delivery Practices

## Overview
- **Objective**: Learn Continuous Delivery best practices, CI/CD pipeline requirements, and distinguish between Continuous Deployment and Continuous Delivery.

## Best Practices for Continuous Delivery

### 1. Make Every Change Releasable
- **Includes**: User documentation, operations runbooks.
- **Purpose**: Ensures each change is functional and well-documented.

### 2. Build on Continuous Integration
- **Approach**: Use short-lived feature branches, avoid long-lived branches.
- **Method**: Trunk-based development, where changes are continuously integrated into the main codebase.

### 3. Construct Automated Delivery Pipelines
- **Goal**: Consistent and predictable code releases.
- **Focus**: Automate processes across the software development lifecycle.

### 4. Aim for No Downtime
- **Strategy**: Validate new functions before deploying to public instances.

### 5. Release at the Granularity of Test
- **Rule**: If parts are tested together, they should be released together.
- **Tools**: Use release automation tools for coordinated delivery.

## CI/CD Pipeline Requirements

1. **Code Repository**: Hosts and manages all source code.
2. **Build Server**: Manages application building, ensures clean builds.
3. **Integration Server**: Handles build automation and testing.
4. **Artifact Repository**: Stores binaries and artifacts for deployment.

## Continuous Deployment vs Continuous Delivery

- **Continuous Delivery**:
  - Automated movement of code through the development lifecycle.
  - Depends on passing automation tests.

- **Continuous Deployment**:
  - Part of Continuous Delivery.
  - Involves deploying delivered code to production.

## Business Implementation
- **Determination**: Based on business needs.
- **Benefit of Continuous Deployment**: Facilitates repeated, reliable, and quick software releases to production.

## Conclusion
- Continuous Delivery involves several best practices focusing on automation, testing, and deployment.
- A CI/CD pipeline encompasses various servers and repositories for streamlined development.
- Understanding the distinction between Continuous Deployment and Continuous Delivery is crucial for aligning with business objectives.

<!-- /MarkdownTOC -->
</details>

---

<a id="tools_of_cd"></a>
# Tools of Continuous delivery (CD)
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

# Tools of Continuous Delivery

## Overview
- **Objective**: Understand and describe various Continuous Delivery (CD) tools and key considerations when choosing a CD tool.

## Key Continuous Delivery Tools

### Jenkins
- **Type**: Older CI/CD tool.
- **Pros**: Large community, many plugins.
- **Cons**: Lacks visibility in pipeline, requires extensive setup and maintenance.

### Spinnaker
- **Origin**: Developed by Netflix.
- **Features**: Cloud-agnostic, manages CD pipelines, simplifies release rollbacks, supports load balancers and scaling clusters.

### Concourse CI
- **Focus**: Built with containers, scalable, flexible with Docker image builds.

### GitLab
- **Capabilities**: Implements both CI and CD, integrates with source code management, supports major cloud platforms.

### Travis CI
- **Characteristics**: CI tool with CD capabilities, minimal maintenance, less feature-rich.

### Tekton
- **Strengths**: Open source, vendor-neutral for Kubernetes, modular, supports multiple environments.

### Go CD
- **Advantages**: Easy pipeline setup, native Docker/Kubernetes support, Value Stream Map tool, YAML/JSON pipeline configuration.

### Argo CD
- **Development**: By Intuit, for GitOps workflow.
- **Utility**: Easy to use UI, integrates with various CI tools, focuses on Kubernetes controller for application state management.

## Choosing a CD Tool: Key Considerations

1. **Features**: Look for audit trails, integrated secrets, and role-based access control.
2. **Compatibility**: Ensure compatibility with existing CI pipelines.
3. **Ease of Use**: Consider setup and maintenance requirements.
4. **Scanning and Deployment**: Tools should handle application security scanning and automate deployments.

## Pipeline Tasks

1. **Security Scanning**: Includes vulnerability and secret scanning, SAST, and DAST.
2. **Code Deployment**: Emphasize automation for consistency across environments.

## Spotlight on Argo CD and Tekton

- **Argo CD**: 
  - Focuses on GitOps pattern.
  - Automates and audits CD processes.
  - Monitors and ensures parity between current and desired application states.

- **Tekton**: 
  - Offers standardized CI/CD tooling.
  - Compatible with tools like Jenkins, Skaffold, Knative.
  - Provides fully portable pipelines for reuse.

## Conclusion
- A variety of CD tools are available, each with unique features and strengths.
- Argo CD and Tekton stand out for their specific functionalities in Kubernetes and pipeline portability.
- When selecting a CD tool, consider features, compatibility, ease of use, and the ability to handle key pipeline tasks.

<!-- /MarkdownTOC -->
</details>

---

<a id="intro_to_tekton_and_pipelines"></a>
# Introduction to Tekton and Pipelines
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

# Introduction to Tekton and Pipelines

## Overview
- **Purpose**: This video introduces Tekton, explaining its functionality and workings in the context of CI/CD pipelines.
- **Key Point**: Tekton is an open-source framework for creating flexible CI/CD pipelines.

## What is Tekton?
- **Definition**: Tekton is an open-source framework used for building CI/CD pipelines.
- **Flexibility**: Offers a range of building blocks for creating simple to complex pipelines.
- **Applications**: Automates the processes of building, testing, and deploying applications.
- **Execution Control**: Enables running steps either in series or parallel.
- **Compatibility**: Functions across cloud providers and on-premises systems.

## Benefits of Using Tekton
1. **Standardization**: Being vendor-neutral, Tekton standardizes CI/CD tooling across various environments.
2. **Built-In Best Practices**: Offers a logical layout for creating scalable, serverless, and cloud-native CI/CD systems.
3. **Flexibility and Customization**: Provides options to design and customize pipelines based on team requirements.
4. **Cloud Native**: Runs natively on Kubernetes clusters, removing the need for separate CI/CD solutions.

## Tekton's Conceptual Building Blocks
1. **Events**: External triggers like pull requests or Git pushes.
2. **Triggers**: Initiates pipeline runs based on events.
3. **Pipelines**: Collections of tasks executed in response to triggers.
4. **Tasks**: Units of work comprising one or more steps.
5. **Steps**: Actual command executions within tasks.

## Tekton's Physical Building Blocks (Kubernetes CRDs)
1. **EventListener**: Listens for external events like Git activities.
2. **TriggerBinding**: Captures parameters from events for pipeline runs.
3. **TriggerTemplate**: Associates parameters with PipelineRuns.
4. **PipelineRun**: Instantiates a pipeline, managing task executions.
5. **TaskRun**: Creates a Kubernetes pod for each task.
6. **PersistentVolumeClaim**: Facilitates sharing of artifacts across tasks.

## Conclusion
- **Tekton's Role**: A comprehensive framework for CI/CD pipeline creation and management within Kubernetes environments.
- **Learnings**: Understanding of Tekton's flexibility, benefits, conceptual and physical components.

<!-- /MarkdownTOC -->
</details>

---

<a id="building_tekton_pipelines"></a>
# Building a Tekton Pipeline
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

# Building a Tekton Pipeline

## Overview
- **Objective**: This video demonstrates how to create Tekton tasks, pass parameters to them, and organize these tasks into a Tekton pipeline.
- **Focus**: The process starts from defining steps and tasks, moving towards building a complete pipeline.

## Creating Tekton Tasks
1. **Starting Point**: Define the necessary steps for a Continuous Delivery pipeline, such as code checkout, quality checks, unit tests, artifact building, and deployment.
2. **Task Definition**: Tasks in Tekton, which represent these steps, are defined in YAML files (Kubernetes manifests).
3. **Example - Checkout Task**:
   - **API Version**: Define the API version, e.g., `tekton.dev/v1beta1`.
   - **Resource Type**: Specify the resource type as `task`.
   - **Task Name**: Set a name in the metadata section, e.g., `checkout`.
   - **Steps**: Define steps within the task, including the image used (e.g., `bitnami/git:latest`) and the command to execute (e.g., `git clone`).

## Passing Parameters to Tasks
1. **Defining Parameters**: Parameters are defined using the `params` keyword.
2. **Example Parameter**: Name a parameter `repo-url` with a description and type (string).
3. **Referencing Parameters**: Use `$(params.repo-url)` to reference the parameter in the task's arguments.

## Organizing Tasks into a Pipeline
1. **Pipeline Definition**: Similar to tasks, pipelines are defined in a Kubernetes manifest.
2. **Setting Up**:
   - **API Version**: Specify the API version for the pipeline.
   - **Resource Type**: Declare the resource type as `pipeline`.
   - **Pipeline Name**: Name the pipeline in the metadata section, e.g., `pipeline`.
3. **Adding Tasks**: Add tasks to the pipeline, referencing previously defined tasks and passing necessary parameters.
4. **Pipeline Example**:
   - Define a parameter `repo-url` for the pipeline.
   - Add the `checkout` task, referencing it with `taskRef` and passing the `repo-url` parameter.

## Executing the Pipeline
1. **Applying Definitions**:
   - Use `kubectl` to apply the task and pipeline definitions (`tasks.yaml` and `pipeline.yaml`).
   - Verify creation with `kubectl get pipelines`.
2. **Running the Pipeline**:
   - Utilize the Tekton CLI (`tkn`) to start the pipeline with `tkn pipeline start`.
   - Pass necessary parameters using the `-p` flag.
   - Observe the execution and logs, ensuring the successful run of the pipeline.

## Conclusion
- **Learnings**: Understanding of how to write Tekton tasks, pass parameters, and build a pipeline.
- **Next Steps**: Continue expanding the pipeline by creating more tasks and integrating them into the pipeline definition.

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