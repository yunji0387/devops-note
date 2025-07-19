# Serverless Overview

# Table of Contents
1. [Introduction to Serverless Computing](#serverless_overview)
2. [Serverless Pros and Cons](#serverless_pros_cons)
3. [Introduction to Faas Model](#faas_model)
4. [The Serverless Framework](#serverless_framework)
5. [Serverless Reference architecture and Use Cases](#serverless_architecture)
6. [Popular Serverless Platforms](#serverless_platform)
7. [AWS Lambda](#aws_lambda)

---

<a id="serverless_overview"></a>
# Introduction to Serverless Computing
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

# Introduction to Serverless Computing

## Overview
The video provides an introduction to **Serverless Computing**, explaining its concepts, evolution, characteristics, and benefits.

## Definition of Serverless Computing
- Defined by the **Cloud Native Computing Foundation (CNCF)** as building and running applications without server management.
- Applications are bundled as functions, executed, scaled, and billed based on demand.
- Combines **Function-as-a-Service (FaaS)** and **Backend-as-a-Service (BaaS)** services.

## Evolution of IT Computing
- Evolutionary trend from traditional computing to serverless computing:
  - **Traditional Computing**: Physical machines, long deployment times, years of lifespan.
  - **Virtualization**: Use of VMs and containers, faster provisioning, days or weeks of lifespan.
  - **Serverless Computing**: Milliseconds to deploy, lifespan of seconds.

## Characteristics of Serverless Computing
- **Hostless**: No server management required.
- **Elastic**: Immediate autoscaling.
- **Automated Load Balancing**: Distributes incoming traffic efficiently.
- **Stateless**: Faster performance and higher scalability.
- **Event-Driven**: Functions triggered by events.
- **High Availability**: Ensured without extra effort.
- **Usage-Based Billing**: Charged only for actual usage, not idle time.

## How Serverless Functions Work
- Developers write functions in languages supported by the cloud provider (e.g., Python, Java, Node.js, C#, Go).
- Functions are uploaded to the cloud and triggered by defined events.
- Cloud providers manage infrastructure, security, scalability, etc.

## Benefits of Serverless Computing
- Developers focus on application code and business logic.
- Facilitates creation of high-quality and optimized applications.
- Functions can be built using popular programming languages.
- Enables better testing and improved user experience.

## Cloud Providers' Responsibilities
- Manage infrastructure tasks including compute, memory, networking, and server management.
- Ensure autoscaling, high availability, security, performance, and monitoring.

## Comparison of Cloud Service Models
- **Traditional**: Entire stack managed by you.
- **IaaS (Infrastructure as a Service)**: You manage from OS upwards.
- **PaaS (Platform as a Service)**: You manage Application and Data layers.
- **Serverless**: You manage only the Application layer.
- **SaaS (Software as a Service)**: Entire stack managed by the cloud provider.

## Conclusion
- **Serverless Computing** allows building applications without worrying about server management.
- Enables developers to focus on coding and applications.
- Users are billed only for usage, not for idle time.

<!-- /MarkdownTOC -->
</details>

---

<a id="serverless_pros_cons"></a>
# Serverless Pros and Cons
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

# Serverless Pros and Cons

## **Benefits of Serverless Computing**
- **No Infrastructure Management**: Developers focus on code; cloud providers manage infrastructure setup and maintenance.
- **Cost-Effective**: Pay-per-request billing avoids charges for idle resources.
- **High Availability and Fault Tolerance**: Ensured by cloud providers.
- **Resource Optimization**: Functions run only when needed, saving resources.
- **Rapid Development and Deployment**: Functions deploy in milliseconds, and many cloud providers include an Integrated Development Environment (IDE).
- **Language Flexibility**: Support for multiple popular programming languages.
- **Faster Time to Market**: Focus on development leads to quicker product releases.
- **Innovation**: Serverless allows more experimentation.
- **Green Computing**: Reduced resource usage contributes to environmentally friendly practices.

## **Constraints of Serverless Computing**
- **Cost for Continuous Workloads**: May not be cost-effective for long-running processes.
- **Vendor Lock-in**: Dependencies on specific cloud providers' technologies.
- **Cold Starts**: Delays in function execution after idle periods.
- **Latency**: Can be too high for time-critical applications (e.g., banking, healthcare).
- **Security Concerns**: Changes in attack surfaces and limitations in provider’s security.
- **Monitoring and Debugging Challenges**: Difficult to test and debug in distributed systems.
- **Limited Language Support**: Dependent on cloud provider offerings.
- **No State Persistence**: Previous run state not available in subsequent invocations.
- **No Control Over Servers**: Cannot optimize for utilization or performance.

## **Serverless vs. Containers**
- **Pros of Serverless/Cons of Containers**:
  - Serverless is cost-effective, scalable, and has quicker deployments.
- **Pros of Containers/Cons of Serverless**:
  - Containers allow easier testing, porting, and support any language.
  - Suitable for long-running and time-critical workloads.

**Advice**: Build serverless first, and if needed, move to containers.

## **Serverless vs. Traditional Computing**
- **Pros of Serverless/Cons of Traditional**:
  - Serverless allows developers to focus on code, is cost-effective, and scalable.
- **Pros of Traditional/Cons of Serverless**:
  - Traditional computing allows full control over data, straightforward networking, and minimal vendor lock-in.

## **Conclusion**
- Both serverless computing and traditional computing have their own benefits and constraints.
- Serverless and containers can complement each other in a hybrid solution.

<!-- /MarkdownTOC -->
</details>

---

<a id="faas_model"></a>
# Introduction to Faas Model
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

# Introduction to the FaaS Model

## **What is FaaS (Function-as-a-Service)?**
- **Definition**: FaaS allows executing code in response to events without managing complex infrastructure.
- **Characteristics**:
  - Subset of serverless computing.
  - Applications are created as multiple functions written in any programming language.
  - Can be deployed on hybrid clouds and on-premises.
  - Stateless but can maintain state using external caches.
  - Functions execute in milliseconds, processing requests in parallel.
  - Billed based on function run time, not server instance sizes.

## **Benefits of FaaS**
- **Cost-Effective**: Pay only when an action occurs, no idle costs.
- **Scalability**: Functions scale automatically and independently.
- **Focus on Code**: Developers can focus on application code, reducing time-to-market.
- **High Availability**: Spread across regions and availability zones without incremental costs.

## **Components of a Serverless Stack**
1. **FaaS**: Functions-as-a-service.
2. **BaaS**: Backend-as-a-service.
3. **API Gateway**: Directs event requests to respective functions.

## **How FaaS Works**
- Event requests from various channels (HTTP, webhooks, scheduled jobs) go through the API Gateway.
- Functions process these requests, possibly interacting with backend services for further processing or storage.
- Response is sent back to the client via FaaS and API Gateway.

## **Real-world Example**
- Uploading a profile picture triggers a FaaS function that creates and stores a thumbnail image.

## **Principles and Best Practices**
- Functions should be designed for a single task.
- Code should be limited, efficient, and lightweight.
- Avoid overusing functions and third-party libraries to control costs and maintain scalability.

## **Managed and Self-managed FaaS Providers**
- **Managed Providers**: AWS Lambda, Google Cloud Functions, Azure Functions, IBM Cloud Functions, OpenShift Cloud Functions, Netlify, Oracle, Twilio, etc.
- **Self-managed Choices**: Fission, Fn Project, Knative, OpenFaaS.

## **Conclusion**
- FaaS provides a simplified, cost-effective, and scalable approach to execute code in response to events, without dealing with infrastructure complexities.

<!-- /MarkdownTOC -->
</details>

---

<a id="serverless_framework"></a>
# The Serverless Framework
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

# The Serverless Framework

## **Overview of Serverless Framework**
- **Definition**: A free and open-source web framework built using Node.js.
- **Purpose**: Initially designed to quickly and safely provision AWS Lambda Functions, Events, and infrastructure Resources.
- **Supported Providers**: AWS, Microsoft Azure, Google Cloud Platform, Apache OpenWhisk.
- **Functionality**: Provides a CLI for structure, automation, and best practices for building serverless architectures.

## **Components of Serverless Architecture**
- **Function**: Independent unit of code, deployed in the cloud, performing a single task.
- **Event**: Triggers the functions, e.g., an HTTP request on an API Gateway URL or a new file in an S3 bucket.
- **Resource**: Infrastructure components used by functions, e.g., a database or an S3 bucket.
- **Service**: The Framework's unit of organization, configured via a `serverless.yml` file.

## **Creating a Basic Serverless Function**
1. **Install Serverless CLI**: Install using npm globally.
2. **Create a Service**: Use the `serverless` command to create an AWS HTTP API using Python.
3. **Configuration**: Define functions, events, and resources in `serverless.yml` file.
4. **Deploy**: Everything in the configuration file is deployed at once.

## **Demo: Hello World Application**
- **Steps**:
  1. Setup AWS credentials.
  2. Install the serverless CLI.
  3. Create and deploy a Hello World function.
  4. Test the function by accessing the provided URL.

## **Conclusion**
- The Serverless Framework simplifies the creation, deployment, and testing of serverless functions across various cloud providers.

<!-- /MarkdownTOC -->
</details>

---

<a id="serverless_architecture"></a>
# Serverless Reference architecture and Use Cases
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

# Serverless Reference Architecture and Use Cases

## **Web Application Reference Architecture**
### **To Do App Example**
- **Overview**: A simple To Do app allowing registered users to create, read, update, and delete items.
- **Architecture**:
  ### **Front-End**:
    - **Components**: Static content generated using Create React App (HTML, CSS, JavaScript, images).
    - **Hosting**: Hosted on AWS Amplify Console.
    - **Operation**: Resources are downloaded to the user's browser and interact with the back end via REST API calls.
  ### **Back-End**:
    - **Components**: Business logic implemented using AWS Lambda and accessed via Amazon API Gateway.
    - **Data Storage**: Amazon DynamoDB.
    - **User Management**: Amazon Cognito for user registration and authentication.
  ### **User Registration and Authentication**:
    - **Components**: Uses Cognito User Pools for user registration and authentication.

## **Serverless Framework Use Cases**
### **1. Event Streaming**:
  - **Description**: Applications can be written and deployed without upfront infrastructure setup and can trigger from topics or event logs.
  - **Benefits**: Elastic, scalable event pipelines without maintenance overhead.
### **2. Post-Processing**:
  - **Examples**:
    - **Image and Video Manipulation**: Dynamically resize images or change video transcoding for different target devices.
    - **AI Applications**: Image recognition or detecting shadows in passport photos.
### **3. Multi-Language Support**:
  - **Description**: Serverless applications can support multiple languages, preventing language lock-in.

## **Conclusion**
- The Serverless Framework enables event-driven applications using various AWS services.
- Use cases include event streaming, post-processing, and multi-language support.

<!-- /MarkdownTOC -->
</details>

---

<a id="serverless_platform"></a>
# Popular Serverless Platforms
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

# Popular Serverless Platforms

## **1. Amazon Web Services (AWS) Lambda**
   - **Description**: Serverless, event-driven computing service.
   - **Key Features**:
     - **Auto-scaling**: Responds to execution requests at any scale.
     - **Pay-as-you-go**: Charged only for running a function and data transfer.
     - **Use Cases**: File processing, web applications, IoT, mobile back-ends.

## **2. Google Cloud Functions**
   - **Description**: Focuses on simplicity and an intuitive developer experience.
   - **Key Features**:
     - **Auto-scaling**: Scales up and down to zero based on traffic.
     - **Firebase Integration**: Alerts developers on data updates.
     - **Use Cases**: Asynchronous workloads, lightweight ETL functions.

## **3. Microsoft Azure Functions**
   - **Description**: Serverless solution focusing on less code and infrastructure.
   - **Key Features**:
     - **Language Support**: C#, Java, JavaScript, PowerShell, Python, etc.
     - **DevOps**: Easy setup for continuous integration and delivery.
     - **Use Cases**: File processing in blob storage, IoT data collection, timed code execution.

## **4. IBM Cloud Functions**
   - **Description**: Integrates easily with other services and is cost-effective.
   - **Key Features**:
     - **High Availability**: Available in multiple regions with auto-synchronization.
     - **IBM Watson Integration**: Cognitive services for image or video analysis.
     - **Monitoring and Logging**: Provides Log Analysis with LogDNA and Cloud Monitoring.
     - **Use Cases**: Object detection in images, event-driven computing.

## **5. Knative**
   - **Description**: Open-source platform based on containers running via Kubernetes.
   - **Key Features**:
     - **Vendor Agnostic**: Avoids vendor lock-in and is platform-agnostic.
     - **Rollout Strategy**: Allows gradual traffic shifting to new serverless components.
     - **Use Cases**: Deployable on any cloud supporting Kubernetes.

## **Conclusion**
- **AWS Lambda**: Provides event-driven and pay-as-you-go serverless platform.
- **Google Cloud Functions**: Offers simplified developer experience and real-time data sync with Firebase.
- **Microsoft Azure**: Promotes cloud and edge computing with DevOps capabilities.
- **IBM Cloud Functions**: Ensures high availability and cost-effective computing with powerful integrations.
- **Knative**: Container-based platform avoiding vendor lock-in and offering flexibility in deployment.

<!-- /MarkdownTOC -->
</details>

---

<a id="aws_lambda"></a>
# AWS Lambda
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

# AWS Lambda Serverless Application

## Overview
Build a serverless application using AWS Lambda to capitalize and reverse text input from an HTML front-end.

## Components
- **AWS CodeCommit**: Fully managed source control that hosts private Git repositories.
- **AWS Amplify**: Solution for building, shipping, and hosting full-stack apps.
- **AWS Lambda**: Event-driven compute service without the need for server management.
- **AWS Step Function**: Visual workflow for building distributed apps, orchestrating microservices, and more.
- **AWS API Gateway**: Managed service for creating, publishing, and maintaining APIs.

## Process
1. **Initialize CodeCommit Repository**:
    - Create and clone a blank repository.
    - Develop a simple HTML page.
    - Commit and push changes to AWS CodeCommit.

2. **Set Up AWS Amplify**:
    - Host static HTML content.
    - Link master branch with Amplify for continuous delivery.

3. **Lambda Function Development**:
    - **Capitalize Function**:
        ```python
        import json
        def lambda_handler(event, context):
            input_text = str(event['inputText'])
            capitalised_input_text = input_text.upper()
            return {"inputText": capitalised_input_text}
        ```

    - **Reverse Function**:
        ```python
        import json
        def lambda_handler(event, context):
            input_text = str(event['inputText'])
            reversed_input_text = input_text [::-1]
            return {"inputText": reversed_input_text}
        ```

4. **Chain Functions with StepFunctions**:
    - Design a workflow using StepFunctions for the Lambda functions.

5. **Integrate with API Gateway**:
    - Define the stage and generate the SDK.
    - Deploy the API and integrate with the web app.

6. **Finalize Web App**:
    - Commit and push changes to the CodeCommit repository.
    - Wait for deployment via Amplify.
    - Test the app using the provided URL.

## Conclusion
AWS services, particularly Lambda, enable the creation of sophisticated apps with integrated front-end and back-end components in a serverless architecture.


<!-- /MarkdownTOC -->
</details>

---
