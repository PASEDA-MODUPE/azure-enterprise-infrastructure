# Azure Architecture - Frost Retail

## Overview
This document defines the Azure architecture for Frost Retail’s cloud environment.  
The goal is to build a secure, scalable, and well-structured infrastructure.

---

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

---

## Network Design

### Virtual Network
vnet-frost-prod-eus

### Subnets
- subnet-web (public-facing applications)
- subnet-app (business logic layer)
- subnet-db (databases)
- subnet-mgmt (administration access)

---

## Design Principles
- Security by default
- Least privilege access
- High availability
- Scalability
- Cost awareness

---

## Status
Initial architecture design completed (v1)

## Deployment Status

### Virtual Network
- vnet-frost-prod-eus created successfully

### Subnets
- subnet-web (10.0.1.0/24)
- subnet-app (10.0.2.0/24)
- subnet-db (10.0.3.0/24)
- subnet-mgmt (10.0.4.0/24)

### Status
Network foundation deployed in Azure

## Deployment Evidence

### Virtual Network
The Virtual Network (`vnet-frost-prod-eus`) was successfully deployed in Azure.

See deployment screenshot:

![VNet Overview](../screenshots/vnet-overview.png)

## Compute Deployment

### Virtual Machine

- **Name:** vm-web-01
- **Operating System:** Ubuntu Server 24.04 LTS
- **Region:** East US
- **Resource Group:** rg-frost-compute
- **Virtual Network:** vnet-frost-prod-eus
- **Subnet:** subnet-web
- **Status:** Running

### Deployment Evidence

![VM Overview](../screenshots/vm-web-01-overview.png)