# Microservices Overview

# Table of Contents
1. [Twelve-Factor App Methodology](#twelve_factor)
2. [What are Microservices](#what_are_microservices)
3. [Comparison of Monolith vs SOA vs Microservices](#comparison)
4. [Microservicess Patterns](#microservices_patterns)
5. [Microservices Anti-Patterns](#microservices_anti_patterns)

---

<a id="twelve_factor"></a>
# Twelve-Factor App Methodology
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

# Twelve-Factor App Methodology Summary

## Overview
- Modern software is often delivered as **Software-as-a-Service (SaaS)**, accessed via the internet.
- The **Twelve-Factor App methodology** is suited for such applications and can work with microservices.
- The twelve factors map to **code**, **deploy**, and **operate** phases of the software delivery lifecycle.

## Code Phase

### Factor 1: Codebase
- One-to-one relationship between a codebase and an app.
- Track codebase in a **version control system** (e.g., Git).
- Multiple deploys may have different versions of the same codebase.

### Factor 5: Build, Release, Run
- **Build**: Compile code and gather dependencies.
- **Release**: Combine build with deployment configuration.
- **Run**: Execute the application.
- Stages should be strictly separated.

### Factor 10: Dev/Prod Parity
- Minimize differences between development and production environments.
- Ensures continuous delivery and early identification of failures.

### Factor 2: Dependencies
- Declare all dependencies explicitly.
- Avoid assumptions about the existence of packages on a machine.

## Deploy Phase

### Factor 3: Config
- Configuration differs between deployments (e.g., database credentials).
- Store config within **environment variables**.

### Factor 4: Backend Services
- Treat local and third-party services uniformly.
- Services should be swappable via URLs or locators without code changes.

### Factor 6: Processes
- Processes should be **stateless** and share nothing.
- Store persistent data in a backend service.

### Factor 7: Port Binding
- Export HTTP by binding to a port.
- Allow the web app to become a backend service for others.

## Operate Phase

### Factor 8: Concurrency
- Applications should run concurrent processes for scalability.
- Stateless processes ensure no interdependencies.

### Factor 9: Disposability
- Processes should start quickly and end gracefully.
- Allows for quick deployment and scaling.

### Factor 11: Logs
- Treat logs as event streams written to standard output.
- Execution environment handles log capture and routing.

### Factor 12: Admin Processes
- One-off processes (e.g., database migration) should run against a release.
- Include admin processes in the application code for synchronization.

## Conclusion
- Twelve-factor methodology aids in creating efficient SaaS applications by mapping to the software delivery lifecycle.

<!-- /MarkdownTOC -->
</details>

---

<a id="what_are_microservices"></a>
# What are Microservices
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

# What are Microservices?

## Overview
- **Microservices** is an architectural approach where an application is divided into many loosely coupled and independently deployable smaller services.
- These services often have their own technology stack, including databases and data management models.

## Key Characteristics

### 1. Independent Components
- Each service in a microservices architecture is its own component and communicates via **API** endpoints.
- Different programming languages can be chosen for different components.

### 2. Communication Methods
- Components communicate over **REST APIs**, **event streaming**, and **message brokers**.
- Services are segregated by business functionality, referred to as a **bounded context**.

### 3. Ease of Updates
- No interdependency allows for easy updates to add new features without modifying the entire application.

### 4. Technology Stack Freedom
- Teams can choose their own technology stack that best suits their needs and expertise.

## Benefits of Microservices

### 1. Scalability
- Components can be scaled independently, reducing waste and cost.
- Horizontal scaling, or "scaling out", is often used, where more instances of resources are added.
- Precise scaling of only the necessary components is possible.

### 2. Risk Mitigation
- Independent iteration of components lessens risks associated with changes.
- Failures in one service do not necessarily impact other services.

### 3. Efficient Communication
- Event streaming helps broadcast state changes, assisting in scaling microservices.

## Conclusion
- Microservices make each application component its own service, allowing for different technology stacks, individual scaling, and independent iteration, thereby reducing risks and enhancing efficiency.

<!-- /MarkdownTOC -->
</details>

---

<a id="comparison"></a>
# Comparison of Monolith vs SOA vs Microservices
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

# Comparison of Monolith vs. SOA vs. Microservices

## Monolith Implementation

### Definition
- A **Monolithic Application** has most or all of its functionalities within a single process, managed through internal layers or libraries.

### Characteristics
- Layers (e.g., security, UI, data access) are **tightly connected** and dependent on each other.
- Example: A Windows Forms Application where UI, business logic, and data access are in one codebase.

### Pros and Cons
- **Pros**: Simplicity and less cross-cutting of features as everything is in the same codebase.
- **Cons**: Difficulty in modification and adapting to new technologies as the application grows.

## Service Oriented Architecture (SOA)

### Definition
- **SOA** is designed with a service provider and consumer approach, where services work as discrete units of functionality.

### Components
- **Interface**: How a service provider will execute requests.
- **Contract**: Defines interaction between service provider and consumer.
- **Implementation**: The service code.

### Pros and Cons
- **Pros**: Increased reliability and support for parallel development.
- **Cons**: Complexity, slow development pace, and high investment cost.
- **Example**: A banking system with interfaces corresponding to different business functions.

## Microservices

### Definition
- **Microservices** consist of loosely coupled, reusable, and specialized components working independently.

### Characteristics
- Each service is independent and can have its own technology stack.
- Data is not shared among services, allowing for independent scaling.

### Pros and Cons
- **Pros**: Ease of development, flexibility to add new technology, and targeted scalability.
- **Cons**: Challenges in security and debugging due to independence of services.
- **Example**: An e-commerce application with separate microservices for order processing, security, and analytics.

## Conclusion
- **Monolithic Design**: Interconnected and interdependent, simple but can become complex over time.
- **SOA Design**: Provides seamless integration and reusability but can be complex and expensive.
- **Microservices**: Offers targeted scalability and flexibility but may have security and debugging challenges.

<!-- /MarkdownTOC -->
</details>

---

<a id="microservices_patterns"></a>
# Microservicess Patterns
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

# Microservices Patterns

## Overview
After watching this video, you will understand various **patterns** used in **microservices** and their applications.

## Patterns Discussed

### Single-Page Application (SPA) Pattern

#### Description
- **SPAs** incorporate all functionalities into one interface using HTML, CSS, and JavaScript.
- Dynamic service calls to backend REST-based services update parts of the screen.

#### Pros and Cons
- **Pros**: Simplifies the front-end experience.
- **Cons**: Puts more responsibility on backend services.

### Backend for Frontend (BFF) Pattern

#### Description
- Inserts a layer between user experience and resources.
- Different backends are developed for different channels (e.g., mobile, web) to optimize user experience.

#### Example
- A mobile app may display a limited subset of data compared to a web application.

### Strangler Pattern

#### Description
- Facilitates gradual refactoring of a monolithic application by splitting into multiple functional domains.
- The new microservices-based implementation replaces the original application over time.

#### Steps
1. **Transform**: Create a parallel new site.
2. **Coexist**: Leave the existing site functional and incrementally redirect to the new site for new functionalities.
3. **Eliminate**: Remove outdated functionalities.

### Service Discovery Pattern

#### Description
- Helps applications and services discover each other dynamically in a microservices architecture.
- Used by load balancers for health checks and traffic rebalancing.

### Other Patterns

#### Entity and Aggregate Pattern
- Used in e-commerce sites where an order is an aggregate of products.

#### Adapter Pattern
- Helps translate relationships between incompatible objects, such as integrating with a third-party API.

## Conclusion
- **SPAs** provide dynamic updates to the page.
- **BFF Pattern** facilitates customized user experiences.
- **Strangler Pattern** aids in breaking up monolithic apps.
- **Service Discovery Pattern** ensures dynamic discovery of services.

<!-- /MarkdownTOC -->
</details>

---

<a id="microservices_anti_patterns"></a>
# Microservices Anti-Patterns
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

# Microservices Anti-Patterns

## Overview
Understanding **anti-patterns** in microservices is crucial to avoid pitfalls during development.

## Anti-Patterns

### 1. Don't Start with Microservices

#### Description
- Avoid starting with microservices from scratch.
- Only consider microservices when a monolithic application becomes too complex to manage.

#### Guideline
- Refactor into smaller services when the application becomes cumbersome to update and maintain.

### 2. Not Taking Automation Seriously

#### Description
- Microservices involve multiple applications each with different deploy cycles.
- Lack of automation can lead to unnecessary trouble.

#### Guideline
- Ensure proper **deployment** and **monitoring automation**.
- Utilize **DevOps** or **cloud services** for managing the infrastructure.

### 3. Don't Build Nanoservices

#### Description
- Building services that are too small (nanoservices) can increase complexity.

#### Guideline
- Start with larger services.
- Only create smaller services when there are issues with deployment, data model complexity, or scaling requirements.

### 4. Don't Turn into SOA

#### Description
- Microservices and SOA both build reusable components but have differences in granularity and data storage.

#### Guideline
- Ensure that a microservices project doesn't morph into an SOA project.

### 5. Don't Build a Gateway for Each Service

#### Description
- Implementing functionalities like authentication and routing in each service can lead to re-engineering efforts.

#### Guideline
- Use an **API Gateway** for managing non-functional concerns centrally.

## Conclusion
- Microservices aim to **enhance customer experience**, **provide flexibility**, and **reduce costs**.
- Avoiding these anti-patterns ensures that microservices remain beneficial and don't become a hindrance to development and management.

<!-- /MarkdownTOC -->
</details>

---
