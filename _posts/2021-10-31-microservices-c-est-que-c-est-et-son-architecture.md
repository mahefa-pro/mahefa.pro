---
layout: post
title:  "Microservices : C'est que c'est et son architecture"
date:   2021-10-31 20:22:21 +0300
categories: microservice
image: "/assets/images/wso2-apim.gif"
author: "Mahefa Abel"
---

![WSO2 APIM](/assets/images/wso2-apim.gif)

## What are Microservices?

**Microservices**  is a service-oriented architecture pattern wherein applications are built as a collection of various smallest independent service units. It is a  [software engineering](https://www.guru99.com/what-is-software-engineering.html)  approach that focuses on decomposing an application into single-function modules with well-defined interfaces. These modules can be independently deployed and operated by small teams that own the entire lifecycle of the service.

The term “micro” refers to the sizing of a microservice which must be manageable by a single development team ( 5 to 10 developers). In this methodology, big applications are divided into smallest independent units.

## What is Microservice Architecture?

**Microservice Architecture**  is an architectural development style that allows building applications as a collection of small autonomous services developed for a business domain. It is a variant of structural style architecture that helps arrange applications as a loosely coupled service collection. The Microservice Architecture contains fine-grained services and lightweight protocols.

Let’s take an example of e-commerce application developed with microservice architecture. In this Microservices architecture example, each microservice is focused on single business capability. Search, Rating & Review and Payment each have their instance (server) and communicate with each other.

![Microservices Architecture](https://cdn.guru99.com/images/tableau/060818_0716_Microservic2.png)

## Microservices vs. Monolithic Architecture

## Microservice Challenges

-   MicroServices rely on each other, and they will have to communicate with each other.
-   Compared to monolithic systems, there are more services to monitor which are developed using different  [programming languages](https://www.guru99.com/best-programming-language.html).
-   As it is a distributed system, it is an inherently complex model.
-   Different services will have its separate mechanism, resulting in a large amount of memory for an unstructured data.
-   Effective management and teamwork required to prevent cascading issues
-   Reproducing a problem will be a difficult task when it’s gone in one version, and comes back in the latest version.
-   Independent Deployment is complicated with Microservices.
-   Microservice architecture brings plenty of operations overhead.

-   It is difficult to manage application when new services are added to the system
-   A wide array of skilled professionals is required to support heterogeneously distributed microservices
-   Microservice is costly, as you need to maintain different server space for different business tasks.
## Microservices Tools

### 1) Wiremock: Testing Microservices

WireMock is a flexible library for stubbing and mocking web services. It can configure the response returned by the HTTP API when it receives a specific request. It is also y used for testing Microservices.

**Download link:**  [**http://wiremock.org/**](http://wiremock.org/)

### 2) Docker

Docker is open source project that allows us to create, deploy, and run applications by using containers. By using these containers, developers can run an application as a single package. It allows you to ship libraries and other dependencies in one package.

**Download link:**  [**https://www.docker.com/**](https://www.docker.com/)

### 3) Hystrix

Hystrix is a fault tolerance java library. This tool is designed to separate points of access to remote services, systems, and 3rd-party libraries in a distributed environment like Microservices. It improves overall system by isolating the failing services and preventing the cascading effect of failures.

**Download Link:**  [https://github.com/Netflix/Hystrix](https://github.com/Netflix/Hystrix)