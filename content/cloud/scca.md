---
title: "SCCA"
date: 2019-08-12T16:58:33-04:00
draft: false
---
## Secure Cloud Computing Architecture

The [SCCA](/glossary/#scca) is the DoD's draft concept for providing cyber mission capabilities in the cloud.  This document does not generate many (any?) new requirements for a DoD system, but it centralizes a number of different existing requiremetns and gives them group names.  
For example, the SCCA architecture requires a 'VDSS' (Virtual Datacenter Security Stack), which is a virtual network configuration that provides IDS/IPS functionality, break and inspect, and other network based security services to protect the enclave in the cloud environment (what they call the 'mission owner space').  ALL of the requirements for a VDSS exist for an on-prem DoD enclave as well - spread across STIGs, CTOs and other guidance documents.  The SCCA simply groups them all together in one place as a quick reference.

### VDSS - Virtual Datacenter Security Stack

Boundary defense requirements - IDS, IPS, break and inspect, WAF, etc.

### VDMS - Virtual Datacenter Management Services

Datacenter management services - HBSS, AD, patch management, etc.  This is ...not cloud related at all.

### CAP - Cloud Access Point

The Cloud Access Point is the bridge between the DoD NIPR network and the cloud providers for Impact Level 4/5/6 workloads.  It is similiar to the VDSS, but oriented to protect the DoDIN from a compormise of the cloud provider network.

### TCCM - Trusted Cloud Credential Manager

The Trusted Cloud Credential Manager is the main 'new' requirement in the SCCA.  The SCCA acknowledges that by definition, administrative 'account owner' credentials in cloud environments (such as an AWS Root account, or a the Office365 Administrator account) present a singificant, _net new_ risk to DoD systems.  There is no 'master account' for an on-prem datacenter that can terminate everything, including backups.  There is in IaaS environments.  TCCM is a process and personnel component of the architecutre, rather than a technical component, and governs how cloud environment credentials are utilized and protected by the DoD consumers.
