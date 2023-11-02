# Web API Essentials: REST API and GraphQL

# Table of Contents
1. [What is REST?](#rest_overview)
2. [Introductin to API Gateway](#api_gateway)
3. [Creating REST APIs](#creating_rest_api)
4. [Making API Request using cURL and Postman](#api_request)
5. [Documenting and Testing REST API with Swagger](#swagger)

---

<a id="rest_overview"></a>
# What is REST?
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

# What is REST?

## Overview
This video explains **RESTful APIs**, their **key characteristics**, and **benefits**.

## Understanding REST

### Definition
- **REST** stands for **Representational State Transfer**.
- It is an architectural style for integrating applications and is common in microservices architectures.

### Characteristics of RESTful APIs
1. **HTTP Requests**: All requests are managed through HTTP.
2. **Stateless Communication**:
   - Each request contains all information required for processing.
   - No stored context on the server; session state is on the client.
3. **Uniform Interface**: Ensures consistency between components regardless of the request origin.

### CRUD Operations
- REST APIs use HTTP requests for CRUD operations:
  - **POST**: Create a record
  - **GET**: Retrieve a record
  - **PUT**: Update a record
  - **DELETE**: Delete a record

## Benefits of REST APIs

### Scalability
- The stateless nature of REST APIs ensures scalability.

### Uniformity
- The interface is consistent, regardless of where the request originates.
- Each piece of data (e.g., product id) belongs to only one Uniform Resource Identifier (URI).

## Example: CEX.IO
- **CEX.IO**, a cryptocurrency exchange, provides REST API for developers.
- It offers bitcoin and other crypto prices, and market data in a simple JSON format.
- API calls, request and response parameters, sample requests, and code snippets are documented for developers.

## Conclusion
- **REST APIs** offer a flexible and uniform interface between components.
- They are stateless, scalable, and communicate using HTTP methods (POST, GET, PUT, DELETE).
- REST defines how applications communicate within a network.

<!-- /MarkdownTOC -->
</details>

---

<a id="api_gateway"></a>
# Introductin to API Gateway
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

# Introduction to API Gateway

## Overview
This video introduces **API Gateway**, explaining its **purpose**, **benefits**, **drawbacks**, and **available products**.

## What is an API Gateway?

### Definition
- An **API Gateway** is a management tool sitting between a client and backend services.
- It aggregates various services and returns the appropriate result.

### Usage
- Protects APIs from malicious usage or overuse with authentication and rate limiting.
- Understands API usage through analytics and monitoring.
- Can monetize APIs using a billing system.
- Presents a single point of contact to various microservices.
- Allows seamless addition or removal of APIs.

## Benefits of Using an API Gateway

- **Insulates Clients**: Hides application's partitioning into microservices.
- **Optimal API**: Provides the best API for each client.
- **Reduces Round Trips**: Allows retrieval of data from multiple services in a single request.
- **Standard Protocol**: Provides a standard communication protocol with the external world.

## Drawbacks of Using an API Gateway

- **Maintenance**: An additional component that needs development and upkeep.
- **Single Point of Failure**: If not designed carefully, it can become a bottleneck.
- **Response Time**: Can increase due to the additional network step.

## Available API Gateway Products

### Managed Products
- **IBM DataPower Gateway**: High-security application gateway.
- **Google**: Offers Apigee or Cloud Endpoints.
- **Microsoft Azure** and **Amazon AWS**: Provide gateways on their platforms.

### Open Source Options
- **Kong**: Top in popularity.
- **Apache APISIX**
- **Tyk**: Also has a managed version.
- **Gloo**: Available as an enterprise version.

## Conclusion
- An **API Gateway** acts as the door to backend services.
- It enables plugging additional services while providing unified access.
- Hides backend complexity and eases scalability or replacement of services.
- Multiple managed and open source API Gateway products are available to choose from.

<!-- /MarkdownTOC -->
</details>

---

<a id="creating_rest_api"></a>
# Creating REST APIs
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->



<!-- /MarkdownTOC -->
</details>

---

<a id="api_request"></a>
# Making API Request using cURL and Postman
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->



<!-- /MarkdownTOC -->
</details>

---

<a id="swagger"></a>
# Documenting and Testing REST API with Swagger
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->



<!-- /MarkdownTOC -->
</details>

---

<a id="binary"></a>
# 
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->



<!-- /MarkdownTOC -->
</details>

---
