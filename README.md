# 🔍 GoDrive - Eureka Service Registry

## 1. Overview
The **Eureka Service Registry** is a key platform component of the **GoDrive** microservice architecture. It provides service registration and service discovery capabilities, allowing microservices to find and communicate with each other dynamically.

## 2. Core Responsibilities
* **Service Registration:** Every microservice in the GoDrive ecosystem registers its network location with this server upon startup.
* **Service Discovery:** Provides a lookup mechanism for services to find the IP addresses and ports of other services.
* **Health Monitoring:** Keeps track of the "heartbeats" of registered instances to ensure high availability.

---

## 3. Technology Stack
* **Language:** Java 25
* **Framework:** Spring Boot
* **Discovery Engine:** Spring Cloud Netflix Eureka Server

---

## 4. Eureka Dashboard (Mandatory)
The Eureka Web Interface provides a real-time visualization of all registered service instances.

* **Public URL:** [http://34.93.114.63:8761](http://34.93.114.63:8761)

> **Note:** Accessing this dashboard is a mandatory requirement for the ITS 2130 module to verify service status.

---

## 5. High Availability & Reliability
* **Multi-Instance Deployment:** This registry is deployed with multiple instances distributed across different zones (asia-southeast1-a, b, c) to ensure fault tolerance.
* **Process Management:** Managed by **PM2** to ensure the registry starts automatically on VM reboot and restarts upon failure.
