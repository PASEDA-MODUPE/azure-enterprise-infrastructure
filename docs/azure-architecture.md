# Azure Architecture - Frost Retail

## Overview

This document defines the high-level Azure architecture for Frost Retail’s cloud environment.

The goal is to design a secure, scalable, and highly available infrastructure that supports both the company’s internal operations and its public e-commerce platform.

---

## High-Level Architecture

The proposed Azure environment will include the following core components:

### 1. Networking Layer
- Azure Virtual Network (VNet)
- Subnets for workload separation
- Network Security Groups (NSGs)
- Azure Firewall (for centralized security)
- Azure Bastion (secure VM access)

### 2. Compute Layer
- Virtual Machines for application hosting
- Availability options for high availability

### 3. Storage Layer
- Azure Storage Account (Blob + Files)
- Backup storage for application data

### 4. Identity Layer
- Microsoft Entra ID for identity management
- Role-Based Access Control (RBAC)

### 5. Monitoring Layer
- Azure Monitor
- Log Analytics Workspace

---

## Design Principles

- Security by default
- Least privilege access
- High availability
- Scalability
- Cost awareness

---

## Status

Initial architecture draft (v1)

## Resource Organization

### Resource Groups
- rg-frost-networking
- rg-frost-compute
- rg-frost-security
- rg-frost-storage
- rg-frost-monitoring

### Naming Convention
<frost>-<service>-<environment>-<region>

Example:
frost-vm-prod-eus

### Region Strategy
Primary region: East US