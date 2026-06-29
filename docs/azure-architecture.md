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