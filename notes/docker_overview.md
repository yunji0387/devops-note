# Table of Contents
1. [Containerization: An Overview with Focus on Docker](#overview)
2. [Introduction to Docker: Summary](#docker)
3. [Building and Running Containers: Summary](#building_docker)
4. [Introduction to Docker Objects: Summary](#docker_object)
5. [Docker Architecture: Summary](#docker_architecture)
6. [Docker Cheat Sheet](./docker_cheat_sheet.pdf)

<a id="overview"></a>
# Containerization: An Overview with Focus on Docker
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

## Introduction
- **Containerization** is a lightweight alternative to full machine virtualization that involves encapsulating an application and its dependencies into a container.
- **Docker**, introduced in 2013, has become the leading platform for containerization, allowing applications to run in a self-sufficient environment.

## Core Concepts
- **Containers:**
  - Run applications in a resource-isolated process.
  - Share the host system's OS kernel, reducing overhead.
- **Images:**
  - Read-only templates used to create containers.
  - Include the application and all its dependencies.
- **Dockerfile:**
  - Text document containing all the commands to assemble an image.
  - Automates the process of Docker image creation.

## Benefits of Using Docker
- **Consistency and Reproducibility:**
  - Eliminate the "it works on my machine" problem.
  - Ensure consistency across multiple development, testing, and deployment environments.
- **Isolation:**
  - Containers interact with each other through well-defined channels.
  - Application processes are separated, enhancing security.
- **Portability:**
  - Containers can run on any system that has Docker installed, regardless of the underlying infrastructure.
- **Microservices:**
  - Facilitate the breakdown of applications into microservices for improved scalability and maintainability.

## Docker Architecture
- **Docker Daemon:**
  - Background service running on the host computer handling building, running, and distributing Docker containers.
- **Docker Client:**
  - The primary user interface to Docker, accepting commands from the user and communicating with the Docker daemon.
- **Docker Hub:**
  - A registry of Docker images.
  - Users can upload and download different Docker images from the hub.

## Conclusion
- Docker simplifies deployment, scaling, and operations by enabling independence between applications and infrastructure.
- It accelerates development, enhances the scalability of applications, and improves resource utilization.

<!-- /MarkdownTOC -->
</details>

---

<a id="docker"></a>
# Introduction to Docker: Summary
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

## Overview
- **Docker** is an open platform for developing, shipping, and running applications within containers, providing an isolated workspace known as a "container."
- Initially released in 2013, Docker has become integral for developers across various environments due to its simplicity, scalability, and cross-platform support.

## Key Features of Docker
- **Isolation:** Separates applications from the underlying infrastructure.
- **Portability:** Runs consistently across various platforms and environments.
- **Written in Go:** Utilizes Linux kernel features and namespaces technology for its functionality.

## Docker Components and Innovations
- **Complementary Tools:** Docker CLI, Docker Compose, and Prometheus.
- **Plugins:** Various storage plugins for extended functionality.
- **Orchestration Technologies:** Docker Swarm and Kubernetes for managing containerized applications.
- **Development Methodologies:** Supports microservices and serverless architectures.

## Benefits of Docker
- **Consistency:** Provides stable deployments thanks to isolated environments.
- **Rapid Deployment:** High-speed rollouts and scaling with reusable image constructs.
- **Development Acceleration:** Automates and streamlines operations, reducing errors and simplifying maintenance.
- **DevOps Alignment:** Complements Agile and Continuous Integration/Continuous Deployment (CI/CD) practices.
- **Efficient Version Control:** Enhances project tracking, testing, and rollback processes.
- **Collaborative Problem-Solving:** Facilitates a collective approach to addressing issues and scaling solutions.
- **High Portability:** Docker images are platform-independent, ensuring seamless transitions between systems.

## Limitations of Docker
- **Not Suited for High-Security Requirements:** Applications demanding intense security measures may find Docker's isolation insufficient.
- **Performance Intensive Applications:** Not ideal for systems that require high performance.
- **Monolithic Architecture:** Incompatibility with single-tiered software systems.
- **Rich GUI-Based Applications:** Limitations with complex graphical user interfaces.
- **Certain Desktop Applications:** Not designed for standard or limited-function desktop applications.

## Conclusion
- Docker revolutionizes the development, shipment, and deployment of applications by ensuring consistency, flexibility, and efficiency across multiple environments and platforms.
- However, it's crucial to consider Docker's limitations in the context of high-security, high-performance requirements, and specific architectural needs.

<!-- /MarkdownTOC -->
</details>

---

<a id="building_docker"></a>
# Building and Running Containers: Summary
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

## Objectives
- Construct a container image using a Dockerfile.
- Initiate a running container from an image.
- Recognize essential Docker commands.

## Process Overview
1. Crafting a Dockerfile.
2. Building a container image using the Dockerfile.
3. Initiating a running container from the image.

## Creating a Dockerfile
A basic Dockerfile may include:
- `FROM`: Specifies the base image.
- `CMD`: Outputs "Hello World!" to the terminal.

```Dockerfile
FROM <base-image>
CMD echo "Hello World!"
```

## Building the Container Image
Execute the docker build command:

- `--tag` or `-t`: To name the image and tag (e.g., `my-app:v1`).
- `.`: Refers to the current directory containing the Dockerfile.
```bash
docker build --tag my-app:v1 .
```

Post-build, look for confirmation messages:

- "Successfully built <image id>": Image creation confirmation.
- "Successfully tagged my-app:v1": Image tagging confirmation.

## Verifying the Image Creation
Use the `docker images` command:
```bash
docker images
```

## Creating and Running the Container
Initiate a container using the `docker run` command:
```docker
docker run my-app:v1
```
This prints: "Hello, world!!".

## Managing Containers and Images
`docker ps -a`: Lists all containers.
`docker push`: Uploads an image to a registry.
`docker pull`: Retrieves an image from a registry.

## Key Takeaways
`docker build`: Assembles a container image from a Dockerfile.
`docker run`: Creates and runs a container from an image.
Essential Docker commands: `build`, `images`, `run`, `pull`, and `push`.

## Conclusion
This tutorial covered the process of creating a Docker container, from Dockerfile to execution, using core Docker commands.

<!-- /MarkdownTOC -->
</details>

---

<a id="docker_object"></a>
# Introduction to Docker Objects: Summary
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

This summary outlines the core concepts of Docker objects, highlighting Dockerfiles, images, containers, and their functionalities, as well as networking, storage, and plugin integrations within the Docker ecosystem.

## Docker Objects Overview

- **Dockerfile**: A plaintext file containing instructions to build a Docker image.
- **Images**: Read-only templates used to create containers.
- **Containers**: Runnable instances of Docker images.
- **Networks**: Communication constructs that isolate container communications.
- **Storage Volumes**: Tools for data persistence beyond a container's lifecycle.
- **Plugins**: Extend Docker's functionality, often integrating third-party additions.

## Essential Dockerfile Instructions

- `FROM`: Specifies the base image (e.g., an OS or language stack).
- `RUN`: Executes commands, forming new image layers.
- `CMD`: Sets default command for the container. Only the final CMD in a Dockerfile is considered.

## Docker Images

- Composed via instructions from a Dockerfile.
- Structured in layers for efficient modification and storage.
- Shared layers promote space efficiency and quicker transfers.
- Immutable, with changes during the run time written to a new, top-most writable layer.

## Naming Docker Images

- **Format**: `hostname/repository/tag`
- **Hostname**: Registry's identity (e.g., `docker.io` for Docker Hub).
- **Repository**: Grouping of related images.
- **Tag**: Specific image version or variant identifier.

_Example_: `docker.io/ubuntu:18.04` implies Docker Hub's Ubuntu image version 18.04.

## Docker Containers

- Active, mutable instances of images.
- Interactable via the Docker API or CLI for creation, modification, starting, or stopping.
- Isolated from each other and the host, ensuring security.
- Capable of network, storage, and state modifications.

## Networking and Storage

- **Networks**: Enable isolated communications between containers.
- **Volumes and Bind Mounts**: Ensure data persistence even after a container ceases.
- **Storage Plugins**: Allow external storage solutions integration.

## Conclusion

Docker's comprehensive ecosystem, from building images with Dockerfiles to the runtime management of containers, provides robust, isolated, and secure application deployment facilitated by networks and persistent storage solutions.

<!-- /MarkdownTOC -->
</details>

---

<a id="docker_architecture"></a>
# Docker Architecture: Summary
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

This document serves as a quick reference guide to the fundamentals of Docker architecture, encompassing its components and the containerization process.

## Overview of Docker Components

- **Docker Client**: Interface for users, utilizing the command line or REST APIs.
- **Docker Host**: Environment where the containers are built, run, and managed.
- **Docker Registry**: Storage system for container images.

## Detailed Component Features

### Docker Client

- Communicates user instructions to the Docker daemon.
- Can interact with local or remote Docker daemons.

### Docker Host

- Contains the `dockerd` daemon that processes commands.
- Manages Docker components, including:
  - Images: Read-only templates used to create containers.
  - Containers: Runnable Docker images instances.
  - Namespaces: Layer of isolation (e.g., pid, net).
  - Networks: Isolated networks for containers to communicate.
  - Storage: Persistent data stored in volumes.
  - Plugins and Add-ons: Extend Docker capabilities.

### Docker Registry

- Stores Docker images.
- Can be public (like Docker Hub) or private (for secure, enterprise-level storage).
- Hosted by third-party providers or self-hosted solutions.

## Containerization Process

1. **Build**: Create a container image from a Dockerfile or base image.
2. **Push**: Store the new image in the specified registry.
3. **Run**: Launch a new container from the image. If the image isn't locally available, Docker pulls it from the registry.

## Docker Architecture Workflow

- The **Client** sends a command, such as `docker run`, to the **Docker Host**.
- The **Docker daemon (dockerd)** within the host receives and processes the command.
- If an image is needed and not locally available, the host communicates with the **Registry** to pull the image.
- The daemon manages the lifecycle of the image's container.

## Conclusion

The Docker architecture streamlines application deployment through its client-server model, involving the Docker client, host (daemon), and registry. This structure simplifies building, storing, and running containerized applications, providing robustness, isolation, and security in managing and deploying software environments.

<!-- /MarkdownTOC -->
</details>

---

<a id="binary"></a>
## 
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->



<!-- /MarkdownTOC -->
</details>

---
