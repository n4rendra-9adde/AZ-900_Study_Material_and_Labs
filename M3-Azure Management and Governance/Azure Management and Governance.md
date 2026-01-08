##  **3. Azure Management and Governance**

**2 Types**
-  Management of the cloud 
- Management in the cloud
##### Management of the cloud
Templates
Automation
Scaling 
Monitoring and alerts
self Healing
##### Management in the cloud
Web portal
CLI and scripts
API
Power shell
### **3.1 Azure Management** 

Cost management Factors
1. Resource type: Different service has different pricing like VMs are priced by compute time, storage charges by capacity and redundancy and Networking cost will be calculated by used bandwidth.
2. Usage and Billing model : Pay as u go. Reserved instances and spot pricing
3. Service tiers and configuration
4. Licensing cost
5. Data transfer (Bandwidth): Inbound is free, Outbound is charged after the free quota
6. Idle or Unused: Reserved IP and disks will generate charges

### **3.2 Governance and Compliance**

### **Governance**

> **Governance** in Azure means **establishing rules, policies, and controls** to ensure your cloud resources are **used properly, securely, and cost-effectively** — according to your organization’s standards.

---

### **Compliance**

> **Compliance** ensures that your organization’s cloud environment **meets legal, regulatory, and industry requirements**, such as **GDPR, ISO 27001, HIPAA, SOC 2**, etc.

- **Governance** = “Are we managing Azure resources the right way?”
    
- **Compliance** = “Are we following laws and standards?”
## **Azure Governance Tools and Features**

| **Tool / Service**                         | **Purpose**                                                                                                               |
| ------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------- |
| **Azure Policy**                           | Defines and enforces organizational rules — for example, restrict regions where resources can be created or require tags. |
| **Azure Blueprints**                       | Packages policies, RBAC, and templates together to deploy compliant environments.                                         |
| **Management Groups**                      | Organizes multiple subscriptions into a hierarchy for centralized policy and access management.                           |
| **Resource Locks**                         | Prevents accidental changes or deletions of critical resources.                                                           |
| **Azure Cost Management + Budgets**        | Helps monitor and control cloud spending.                                                                                 |
| **Azure RBAC (Role-Based Access Control)** | Controls who can access what resources, ensuring least-privilege access.                                                  |
| **Azure Tags**                             | Adds metadata (like owner, cost center, or environment) for tracking and governance.                                      |
| Microsoft Purview                          | For data governance                                                                                                       |
