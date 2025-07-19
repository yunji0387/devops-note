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

# Overview of Project, Application, Build, and Jobs in IBM Cloud Code Engine

## **Project**
- **Definition**: A group in Code Engine that manages resources and entities (e.g., build, app, job, TLS certificates).
- **Functions**:
  - **Namespace**: Provides isolation for entities. Entity names must be unique within a namespace but can be duplicated across namespaces.
  - **Access Control**: Manages resources and provides control over who can access what.
  - **Monitoring**: Allows monitoring of resource allocation (CPU, memory) for the entire project.
- **Example**: A project named `my-project` may have 11 applications and 2 jobs.

## **Application**
- **Definition**: Code that runs to serve HTTP requests or provide REST APIs.
- **Features**:
  - Supports **WebSockets** for long-running, session-based communication.
  - **Auto-scaling**: Dynamically scales up or down based on workload and configuration settings.
- **Example**: An application named `my-application` under the project `my-project`.

## **Build**
- **Definition**: Process of creating a container image from source code.
- **Methods**:
  - **Dockerfile**: A set of instructions to create a Docker container image.
  - **Cloud Native Buildpack**: Automates tasks like inspecting code and creating a build plan to produce an image.
- **Usage**: After building the container image, it can be deployed to Code Engine to create an application.

## **Job**
- **Definition**: A one-time execution of code.
- **Characteristics**:
  - Unlike applications, jobs are designed to run once and exit.
  - Can specify workload configurations before running.
- **Examples of Jobs**:
  - **Data Processing**: Query and transform data in batches.
  - **Machine Learning**: Model training jobs.
  - **Reporting**: Generate reports based on a schedule.
  - **Billing**: Create and send bills.

## **Conclusion**
- **Project**: Groups and manages Code Engine entities.
- **Application**: Serves HTTP requests or WebSocket sessions.
- **Build**: Creates a container image from source code.
- **Job**: Executes code once or in multiple instances.

<!-- /MarkdownTOC -->
</details>

---

<a id="building_container_for_microservices"></a>
# Building Container Images for Microserrvices
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

# Building Container Images for Microservices

## **Container**
- **Definition**: A standalone, executable unit of software that packages an application's source code, libraries, dependencies, and runtimes.
- **Characteristics**:
  - **Portable**: Can run on any device or in the cloud.
  - **Efficient**: Does not require a guest OS, leveraging the host OS instead.
  - **Ideal for Microservices**: Matches the lightweight and isolated nature of microservices.

## **Docker**
- **Definition**: A software platform for building and running applications as containers.
- **Popularity**: Led to an explosive usage of containerization and fostered a large ecosystem.
- **Usage in IBM Cloud Engine**: Docker is the main container technology used.

## **Building a Docker Container Image**
- **Steps**:
  1. **Dockerfile Creation**:
     - Acts as a blueprint outlining instructions to build the container.
  2. **Building Container Image**:
     - The image includes all application assets and is immutable.
     - Consider an image like a class template in OOP.
  3. **Running Container**:
     - Instantiating an image creates a running container.

- **Dockerfile Example**:
  - `FROM`: Specifies base image (e.g., Python, uwsgi-nginx-flask).
  - `COPY`: Copies files to `/app` folder in the image.
  - `ENV`: Sets environment variables (e.g., `LISTEN_PORT` to 8080).
  - `EXPOSE`: Indicates the port on which the container listens.
  - `RUN`: Executes commands (e.g., `pip install` for dependencies).
  - `CMD`: Provides a default executable for the container (only one `CMD` allowed).

## **Container Registry**
- **Definition**: A repository to manage container images.
- **Examples**: Docker Hub, IBM Cloud Container Registry.
- **Image Name**: Consists of hostname (e.g., `icr.io` for IBM), repository (group of related images), and tag (version info).
- **Usage**: After building, an image can be pushed to a registry and then pulled using its unique name.

## **Conclusion**
- **Container**: A standalone, portable unit containing all software dependencies.
- **Docker**: A platform to build and run containers.
- **Dockerfile**: Used to instruct Docker to build a container image.
- **Container Registry**: Manages container images and allows them to be pulled by name.

<!-- /MarkdownTOC -->
</details>

---

<a id="deploying_and_running_application"></a>
# Deploying and Running Application
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

# Deploying and Running Applications

## **Deployment Modes**
- **Container Image Deployment**:
  1. **Manual Image Push**:
     - Build and push container image to a private/public container registry.
     - Cloud Code Engine pulls and deploys using the unique image name.
  2. **Automatic Image Build**:
     - Specify a Dockerfile or buildpack with source code.
     - Cloud Engine builds and deploys the application automatically.
- **Difference**: Who is responsible for building and pushing the container image.

## **IBM Cloud Console**
- **Definition**: A web portal for managing IBM cloud services, including Code Engine.
- **Steps to Create and Deploy Application**:
  1. Specify application's name.
  2. Choose deployment from Container image or Source code (default: Container image).
  3. Provide image reference and optionally, registry access.
  4. Additional advanced settings can be configured as required.

## **IBM Cloud CLI**
- **Alternative to Console**: For more precise deployment.
- **Commands**:
  1. **Create and Deploy**:
     ```bash
     ibmcloud ce app create --name <app-name> --image <image-reference> --registry-access <registry-access>
     ```
     - Example: Deploy `helloworldapp` from `us.icr.io` with registry access `myregistry`.
  2. **Test Application**:
     ```bash
     ibmcloud ce app get --name <app-name> --output <output-format>
     ```
     - Example: Get the URL of the deployed `helloworldapp`.

## **Endpoint URL**
- Once deployed, the Code Engine provides an endpoint URL leading to the application's main page or microservice entry point.

## **Conclusion**
- Applications can be deployed on Cloud Engine from a container image or source code.
- Deployment can be done using either IBM Cloud Console or IBM Cloud CLI.

<!-- /MarkdownTOC -->
</details>

---

<a id="update_deployed_application"></a>
# Updating Deployed Application
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

# Updating Deployed Applications

## **Common Scenarios for Updating Applications**
1. **Update Environment Variables**: Modify database location, secret keys, etc.
2. **Update Application Visibility**: Change URL visibility from public to private or project-only.
3. **Update Image Reference or GitHub Repo**: Switch to a new container image or source code repository.
4. **Update Runtime Resources**: Adjust computational resources (CPU, memory) allocated to the application.

## **IBM Cloud Console**
- **Easy Updates**: Suitable for simpler updates like adding environment variables.
- **Update Steps**:
  - **Environment Variables**: Add/update via "Add environment variable" button.
  - **Visibility**: Update via the "Domain mappings" tab (options: cluster-local, private, public).
  - **Image Reference**: Update via the "Code" tab.
  - **Runtime Resources**: Adjust CPU, memory, and ephemeral storage via the "Runtime" tab.

## **IBM Cloud CLI**
- **Precise Updates**: Suitable for more complex application updates.
- **Commands**:
  - **Update Environment Variable**:
    ```bash
    ibmcloud ce app update --name <app-name> --env <var-name=var-value>
    ```
  - **Update Visibility**:
    ```bash
    ibmcloud ce app update --name <app-name> --visibility <visibility-option>
    ```
  - **Update Image Reference**:
    ```bash
    ibmcloud ce app update --name <app-name> --image <image-reference> --registry-secret <registry-secret>
    ```
  - **Update Runtime Resources**:
    ```bash
    ibmcloud ce app update --name <app-name> --cpu <cpu-amount> --memory <memory-amount>
    ```

## **Revision Management**
- Code engine manages application revisions, allowing updates without needing to deploy a new application.

## **Examples**
- Migrating data from SQL DB to NoSQL DB and updating the Pets DB service.
- Changing `pet_db_service` environment variable `DB_HOST` to `localhost`.
- Updating `pet_db_service` visibility to `private`.
- Updating `pet_db_service` image reference to `us.icr.io/petshop/no_sql_pet_db_service`.
- Increasing `pet_db_service` runtime resources to 2 CPUs and 16 GB memory.

## **Conclusion**
- Applications can be updated either through IBM Cloud Console UI or IBM Cloud CLI as per preference.

<!-- /MarkdownTOC -->
</details>

---
