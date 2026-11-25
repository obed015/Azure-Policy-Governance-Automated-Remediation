# Azure Policy Governance & Automated Remediation

A personal Azure cloud engineering project exploring how cloud governance, security compliance and automated resource remediation can be implemented using Azure Policy and Infrastructure as Code.

The project combines Azure Management Groups, custom policy definitions, policy initiatives, managed identities, RBAC, Bicep, Azure Monitor, Log Analytics and KQL to detect, monitor and remediate non-compliant Azure resources.

---

## Architecture Overview

![Enterprise Architecture](docs/architecture/cloud-policy-architecture.webp)

---

## Project Summary

This project was built in my personal Azure tenant to develop a practical understanding of Azure governance, policy management, security compliance and automated remediation.

The implementation uses management-group-scoped custom Azure Policy definitions and initiatives to evaluate storage account configurations and identify resources that do not meet defined security requirements.

Azure Policy's Audit and Modify effects are used to explore compliance detection and automated remediation, with managed identities and Azure RBAC providing the permissions required to correct non-compliant resource configurations.

The governance and monitoring infrastructure is defined using Bicep, with Azure Monitor, Log Analytics, KQL, Azure Workbooks and Action Groups providing compliance reporting, monitoring and notifications.

Throughout the project, I tested policy behaviour, investigated deployment and monitoring issues, configured remediation permissions and verified resource configuration changes using the Azure Portal and Azure CLI.

The project was designed to help me understand how Azure governance controls are implemented, monitored, troubleshot and maintained in practice.

---

## Key Objectives

* Enforce governance policies across Azure environments
* Detect non-compliant resources automatically
* Remediate insecure configurations
* Centralize compliance logging
* Visualize compliance using dashboards
* Trigger alerts when violations occur

---

## Technologies Used

* Azure Policy
* Azure Management Groups
* Azure Monitor
* Log Analytics Workspace
* Azure Monitor Workbooks
* Azure Monitor Alerts
* Managed Identity
* Bicep
* Azure CLI

---

## Core Features

### Policy Enforcement

Azure Policy initiatives enforce security controls including:

* Disabling public blob access
* Auditing public network exposure
* Enforcing secure storage settings

Policies are deployed at the **Management Group scope**, ensuring consistent governance.

---

### Automated Remediation

Non-compliant resources are corrected automatically using:

* Azure Policy **Modify** effects
* System-assigned Managed Identity
* Policy remediation tasks

---

### Compliance Monitoring

Compliance data is collected using:

* Azure Policy logs
* Log Analytics Workspace
* Azure Monitor Workbooks

Dashboards provide real-time compliance visibility.

---

### Alerting

Azure Monitor Alerts detect policy violations and trigger administrative notifications.

---

## Architecture Layers

1. Management Group Governance
2. Policy Definitions and Initiative
3. Policy Assignment with Managed Identity
4. Subscription and Resource Group Layer
5. Resource Evaluation and Remediation
6. Monitoring and Visualization
7. Alerting and Notifications

---

## Deployment Evidence

Deployment screenshots are stored in:

```text
docs/screenshots/
```

These include:

* Policy compliance states
* Remediation execution
* Workbook dashboards
* Alert notifications
* CLI validation outputs

---

## Live Project Walkthrough

Architecture Overview:
https://oowusu.com/cloud-policy-compliance-dashboard.html

Technical Deep Dive:
https://oowusu.com/cloud-policy-compliance-dashboard-deepdive.html

---

## Deployment Approach

Infrastructure was deployed using **Bicep modules** to enable consistent and repeatable governance configuration across Azure environments.

---

## Learning Outcomes

* Azure governance implementation
* Policy-based remediation workflows
* Infrastructure as Code using Bicep
* Azure Monitor and Log Analytics integration
* Workbook dashboard creation
* Azure CLI automation

---

## License

MIT License
