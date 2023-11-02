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

# Creating REST APIs

## Overview
This video teaches how to **create a RESTful API in Python** and **host it using Flask**.

## Python
- **Python** is versatile, used for web development, scientific computing, AI, and machine learning.
- Supports web development through frameworks like **Flask**.

## Flask

### Introduction
- **Flask** is a micro web framework known for scalability and simplicity.
- Flask applications are lightweight and non-opinionated about databases or template engines.
- Suitable for creating RESTful APIs.

### Installation
- Ensure **Python 3** and **pip** (Python package manager) are installed.
- Install Flask using `pip install` command.

### Creating a Flask Application

#### Hello World App
- Create `hello.py` file and run the Flask server.
- The "Hello World" response is visible at `127.0.0.1:5000`.

#### Products Microservice
- Create `products.py` file for the products microservice.
- Define imports and create a default list of products (not persisted in a database).
- Define the **GET** method to retrieve all products, which implicitly returns HTTP status `200` (OK).

## Conclusion
- **Flask** is ideal for hosting Python web applications as microservices.
- A RESTful API can be easily created and hosted using Flask and Python.

<!-- /MarkdownTOC -->
</details>

---

<a id="api_request"></a>
# Making API Request using cURL and Postman
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

# Making API Requests using cURL and Postman

## Overview
This video demonstrates how to make HTTP requests using **cURL** and **Postman**.

## cURL

### Introduction
- **cURL** (Client URL) is a command line tool for data transfer over various network protocols.
- Developed in 1998, it is widely used for downloading files, endpoint testing, debugging, and error logging.
- Supports protocols such as HTTP, HTTPS, FTP, and IMAP.

### Usage
- **Example Command**: `curl -X <HTTP_METHOD> <URL> -H <HEADERS>`
- **Options**:
  - `-x`: Specifies the HTTP method (e.g., GET).
  - `-H`: Defines headers (e.g., specifying JSON data).
- **Output**: A list of products returned in JSON format from the product’s microservice.

## Postman

### Introduction
- **Postman** is an API platform with user-friendly tools for creating, testing, sharing, and documenting APIs.
- Simplifies API lifecycle management and collaboration.
- Supports HTTP requests like GET, POST, PUT, and PATCH, and can convert API calls to code in languages like JavaScript and Python.

### Example
- The **WhatsApp Business Platform Cloud API** uses Postman to create a streamlined, developer-friendly experience.
- Onboarding time is reduced to minutes due to automation and pre-filled data.

### Usage
- Postman can be downloaded or used online.
- **Example Request**:
  1. Open a new tab in Postman.
  2. Set request type to GET and specify the URL of the microservice.
  3. Click on "Send" to analyze the output.
  4. Save the request in the workspace for future use.

## Conclusion
- **cURL** is used for transferring data with URLs, either at the command line or in scripts.
- **Postman** is a versatile platform for building and testing APIs, known for its simplicity and popularity.

<!-- /MarkdownTOC -->
</details>

---

<a id="swagger"></a>
# Documenting and Testing REST API with Swagger
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

# Documenting and Testing REST APIs with Swagger

## Overview
This video explains how to use **Swagger** to document and test REST APIs.

## API Documentation

### Importance
- API documentation acts as a reference manual for effective system integration.
- Ensures consistent communication between different systems.

### Swagger and OpenAPI
- **Swagger** automates API documentation creation, ensuring adherence to OpenAPI specifications.
- Describes the API structure, allowing automatic generation of interactive UI and API documentation.
- The structure is defined in a JSON or YAML file adhering to OpenAPI specifications.
- **OpenAPI Specification**: A standard, language-agnostic interface to RESTful APIs that is both human and machine-readable.

## Implementing Swagger with Flask

### Flask-Swagger-UI
- **Flask Swagger UI** enhances Flask's capabilities to describe and visualize REST APIs.
- Installation: `pip install flask-swagger-ui`

### Setup and Configuration
- Import `swagger_ui_blueprint` and define basic configuration, such as:
  - Path where Swagger will be available (e.g., `products/docs`).
  - Path where the swagger file is served.
  - Name for the Swagger UI instance.
- Register the blueprint with the Flask app.
- Expose the `swagger.json` file, which holds the API definition, via a route.

### API Definition with Swagger
- Define the API (e.g., product microservice) with Swagger, specifying:
  - Model and path for retrieving the product list.
  - Properties of the Product object.

## Testing with Swagger

### Benefits
- Swagger UI enables testing of the API directly from the documentation.
- Provides detailed information on supported functions, requests, and responses.
- Displays content such as terms of service, contact information, and license information.

### Example
- The video demonstrates testing a GET method to retrieve all products using Swagger UI.

## Conclusion
- **Swagger** aids in both documenting and testing APIs.
- **OpenAPI Specification** provides a standardized representation of APIs.
- Integration with Flask is facilitated through `flask-swagger-ui`.

<!-- /MarkdownTOC -->
</details>

---
