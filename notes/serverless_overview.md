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



<!-- /MarkdownTOC -->
</details>

---

<a id="serverless_framework"></a>
# The Serverless Framework
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->



<!-- /MarkdownTOC -->
</details>

---

<a id="serverless_architecture"></a>
# Serverless Reference architecture and Use Cases
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->



<!-- /MarkdownTOC -->
</details>

---

<a id="serverless_platform"></a>
# Popular Serverless Platforms
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->



<!-- /MarkdownTOC -->
</details>

---

<a id="aws_lambda"></a>
# AWS Lambda
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->



<!-- /MarkdownTOC -->
</details>

---
