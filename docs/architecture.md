# RPCMMS v3 – System Architecture Overview

This document provides a high-level overview of the **RPCMMS v3 architecture**.

The goal is to explain how the system is structured, how it scales, and how it supports both
**SaaS-based deployment** and **optional on-premise installations**, without exposing proprietary implementation details.

---

## Architectural Principles

RPCMMS v3 is designed around the following core principles:

- **SaaS-first by default**
- **Modular and scalable**
- **Secure and isolated per customer**
- **Designed for harsh industrial environments**
- **Simple to operate, complex where it matters**

The architecture supports growth from a single rig or site to large multi-site operations.

---

## High-Level Architecture

At a conceptual level, RPCMMS consists of four main layers:

1. **Client Layer (Frontend)**
2. **Application Layer (Backend Services)**
3. **Data Layer**
4. **Infrastructure & Deployment Layer**

Each layer is designed to scale independently.

---

## Client Layer (Frontend)

The client layer provides access to RPCMMS through a modern web interface.

Key characteristics:
- Web-based UI accessible via standard browsers
- Optimised for desktop, tablet, and mobile use
- Designed for technicians, supervisors, and management
- Role-based access and permissions

The frontend focuses on **clarity, speed, and usability**, especially in operational environments.

---

## Application Layer (Backend Services)

The application layer contains the core business logic of RPCMMS.

Responsibilities include:
- Work request and work order processing
- Planned maintenance scheduling
- Asset hierarchy management
- Inventory and spare parts tracking
- Safety, permits, and compliance logic
- Reporting and audit trails

This layer is designed as a set of modular services to allow controlled expansion over time.

---

## Data Layer

The data layer manages all persistent system data.

Key concepts:
- Strongly structured asset hierarchy
- Clear relationships between assets, work, and inventory
- Historical traceability for maintenance and compliance
- Logical separation of customer data

Data integrity and auditability are treated as first-class requirements.

---

## SaaS Deployment Model (Default)

In the SaaS model:

- RPCMMS is hosted in a secure cloud environment
- Multiple customers are supported using isolated tenants
- Each tenant has logically separated data
- Updates and improvements are rolled out centrally

Benefits:
- Rapid onboarding
- Lower total cost of ownership
- Automatic updates
- Predictable subscription model

---

## On-Premise / Dedicated Server Deployment (Optional)

For customers with strict security or regulatory requirements, RPCMMS supports deployment on:

- Customer-owned servers
- Dedicated private cloud environments

In this model:
- Each customer receives a fully isolated system instance
- Update cycles are controlled by agreement
- Infrastructure responsibility is shared according to contract

Functionally, the system remains consistent with the SaaS version.

---

## Security & Access Control

RPCMMS architecture incorporates:

- Role-based access control
- Separation of operational and administrative functions
- Secure authentication mechanisms
- Audit logging for critical actions

Security is designed into the system, not added as an afterthought.

---

## Scalability & Future Growth

The architecture supports:

- Expansion from single-site to multi-site deployments
- Integration with external systems (ERP, procurement, reporting)
- Future predictive maintenance and analytics capabilities
- Incremental feature rollout without major redesign

---

## Architectural Scope

This document intentionally focuses on **conceptual architecture**.

Detailed implementation, technology choices, and proprietary logic
are documented separately and not exposed in public repositories.
