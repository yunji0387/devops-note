# Create and Deploy Microservices

# Table of Contents
1. [IBM Cloud Code Engine](#ibm_cloud_code_engine)
2. [Project, Application, Build, and Jobs](#project_application_build_job)
3. [Building Container Images for Microserrvices](#building_container_for_microservices)
4. [Deploying and Running Application](#deploying_and_running_application)
5. [Updating Deployed Application](#update_deployed_application)

---

<a id="ibm_cloud_code_engine"></a>
# IBM Cloud Code Engine
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

# IBM Cloud Code Engine Overview

## Challenges of Self-hosting Microservices
- **Configuration and Building**:
  - Making microservices production-ready involves configuring library dependencies, resources, credentials, etc.
  - Microservices need to be compiled and built into an executable binary.
- **Infrastructure Selection**:
  - Choices involve web servers, operating systems, networks, databases, etc.
- **Scaling**:
  - Microservices must scale dynamically based on traffic, e.g., peak traffic during holidays.
- **Communication**:
  - Communication among microservices should be reliable and secure.
- **Monitoring**:
  - Logging, monitoring, and dashboard activities are required for stability.

### Example: Python-based Microservice Deployment
- **Web Server Interfaces**:
  - **WSGI** (Web Server Gateway Interface): Synchronous service calls.
    - Popular servers: Green Unicorn, uWSGI.
  - **ASGI** (Asynchronous Server Gateway Interface): Supports asynchronous calls.
    - Popular servers: Daphne, Hypercorn.
- **Infrastructure**: Can range from a laptop to a sophisticated cluster.

## IBM Cloud Code Engine Solution

### Overview
- **Purpose**: Eases the deployment burden, allowing developers to focus on code.
- **Type**: Fully managed, serverless platform.
- **Features**: Combines PaaS, CaaS, and serverless deployment models.

### Use Cases
1. **Deploy Built Applications**:
   - Deploy microservices, web apps, or console apps directly.
2. **Push Source Code Directly**:
   - Code Engine builds and deploys applications from source code (GitHub or local).
3. **Run Batch Jobs**:
   - Deploy data processing or analytics tasks on the same platform.

### Benefits
- **Cluster Management**: Handles provisioning, configuring, scaling, and server management.
- **Focus on Code**: Developers can concentrate on code development.
- **Quick Deployment**: Builds and deploys apps in seconds.
- **Auto-scaling**: Automatically scales workloads up and down.
- **Security and Isolation**: Ensures secure connections and isolates workloads.
- **Integration**: Fully integrates with the IBM Cloud services catalog.

## Conclusion
- Self-hosted microservices deployment can be complex.
- IBM Cloud Code Engine simplifies the deployment process, allowing developers to focus on coding.
- The platform supports application deployment, direct source code deployment, and batch job execution.

<!-- /MarkdownTOC -->
</details>

---

<a id="project_application_build_job"></a>
# Project, Application, Build, and Jobs
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->


<!-- /MarkdownTOC -->
</details>

---

<a id="building_container_for_microservices"></a>
# Building Container Images for Microserrvices
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->


<!-- /MarkdownTOC -->
</details>

---

<a id="deploying_and_running_application"></a>
# Deploying and Running Application
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->


<!-- /MarkdownTOC -->
</details>

---

<a id="update_deployed_application"></a>
# Updating Deployed Application
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->


<!-- /MarkdownTOC -->
</details>

---
