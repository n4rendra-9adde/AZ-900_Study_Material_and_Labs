# **1. Basic Cloud Concepts**

## **1.1 What is Cloud Computing**

>The cloud is someone else's computer that we can utilize through the internet.
#### **Shared responsibility Model:**

>The **Shared Responsibility Model** explains **who is responsible for what** in cloud security and operations.
#### **Responsibility Depends on Service Type (IaaS / PaaS / SaaS)**

##### ***IaaS (Infrastructure as a Service)***
Microsoft: Hardware, network, datacenter  
Customer: OS, apps, data, workloads, security settings
##### ***PaaS (Platform as a Service)***
Microsoft: Hardware + OS + runtime  
Customer: Applications, identities, data, access policies
##### ***SaaS (Software as a Service)***
Microsoft: Almost everything  
Customer: Users, identity access, data input
![[Pasted image 20250926172650.png]]

### **CapEx vs OpEx (Azure Cost Concepts)**

#### ***1. CapEx (Capital Expenditure)***

**Traditional IT model (On-premise)**.

You **buy** the hardware and infrastructure upfront.

###### Characteristics:

- Large one-time upfront investment
    
- Long-term financial commitment
    
- Includes servers, storage, network devices, datacenter setup
    
- Low ongoing cost after purchase
    
- Hardware becomes outdated over time
    

##### Examples:

- Buying servers for on-prem datacenter
    
- Purchasing network switches & firewalls
    
- Buying storage arrays
    
- Building a cooling system or UPS

### **2. OpEx (Operational Expenditure)**

**Cloud model (Ex: Azure)**.

You **pay-as-you-go** based on usage.

###### Characteristics:

- No upfront cost
    
- Pay monthly/annually depending on consumption
    
- Flexible and scalable
    
- Easy budgeting because cost is predictable
    
- Suitable for dynamic workloads
    

###### Examples in Azure:

- Paying per hour for a Virtual Machine
    
- Paying for Storage based on consumption
    
- Paying per TB for bandwidth
    
- Paying for Azure SQL on a monthly basis
    
- Paying for serverless function executions

---

## **1.2 Cloud Deployment Models**

#### ***1. Public cloud***
It is a computing services offered  by a 3rd party providers over the public internet, making them available to anyone who wants to use or  purchase them.
Example in this case Azure owns the hardware and infra they will allow the users to access this.

#### ***2. Private cloud***
Private cloud is defined as computing services offered either over the internet or in a private internal network and only to select users instead of general public.

#### ***3. Hybrid cloud*** 
Computing environment that combines a private cloud with a public cloud 

---
## **1.3 Cloud Service Types**

1. **IaaS** - Computing, Storage, Networking.  Example is Azure VM, Azure storage, Virtual Networking(Ingress and egress bandwidth cost will be there),  etc. . Pay by the second, Many choices in CPU speeds, RAM optimizations
2. **PaaS** - Middleware development tools, DB and more.  Example : Azure app services, Managed storage, Azure SQL DB, Azure front door, Firewall, Load balancer
3. **SaaS** - Full pledged cloud apps. Ex : O365. OneDrive etc.

---
## **1.4 Cloud Benefits**
#### ***High Availability (HA)***
Its a ability of a system to remain operational to users during planned or unplanned outages.
**HA is conscious efforts to avoid the obvious sources of downtime.**

**Planned outages:** 
- OS Updates
- Application updates
- Hardware replacements
- Migrating to a  new hosting provider

**Unplanned Outages:**
- H/W failure
- Network disruption
- Power outage
- Natural disaster (Earthquake, etc)
- Cyber attacks 
- Software Bugs
- Poor scaling and architecture design

#### ***Methods to mitigate Planned outages***
- Gradual deployment strategy
- Testing and Monitoring the deployment
- Small deployments
- Frequent deployments
- Automations
- Easy roll back plans

#### ***Methods to mitigate Un Planned outages***
- Every single core components should have redundancy
- Use azure built in features for availability
	- Availability sets
	- Availability zones
	- Cross region load balancer/ Front door
- Constant health Monitoring  / Probes
- Automation - Automating the deployments, Scale up - Scale down etc.
- Having strong security practices
- Be geographically distributed
- Disaster recovery plan
- Testing that disaster recovery plan
- Load testing
### ***Scalability***
The ability of a system to accommodate increasing the demand by either adding or removing the resources as needed. Also this is called **Elasticity

**Why it is needed:**
Ability of a system to automatically adjust resources based on traffic demand without requiring changes to the application or system design. This helps reduce operational costs and minimize human errors, and indirectly contributes to improved availability and reliability.
#### ***Vertical Scaling***
Also called Scaling up or Scaling down
Adding more resources to a single server 
Increase the amount of memory, the number of CPUs
Here an upper limit is there, in Azure 96 vCPUs and 384GB memory
It does not improve the
#### ***Horizontal Scaling***
Also called as Scaling in and scaling out.
Adding more server to a system
Here there is no scaling limit, scaling complexity is high
It improves the HA
#### ***Impact on system cost***
Adding more resources to system adds to cost
This optimizes the reduce in the cost
#### ***Elasticity Benefits:***
The ability of a system to **quickly and easily** scale up or down the amount of resources that a system uses in response to changing demand.
Also called autoscaling.
The system monitors some metrics such as CPU utilization and once it reaches the threshold it will increase or decrease the resources.

**Why is it needed?**
- More efficient and cost effective use of resources
- Minimizes the computing waste 
- Self hosted system tend to have a large percentage of over provisioned resources for anticipated future growth.

### ***Reliability***
Reliability relating to Availability,  Reliability, and Predictability
Availability: to be accessible when the user needed
Reliability: The ability of a system to **recover from failures**
	There are many different failures that can occur 
		- H/W failure
		- Network disruption
		- Power outage
		- Large scale regional outage

**How is it achieved?**
- Auto scaling
- Avoid single point of failure (If you are running on the VM try to use multiple VMs)
- Multi region deployments
- Data backup and replication
- Health probes and replication

### ***Predictability***
Ability to forecast and control the performance and behavior of a system 
Includes the ability to predict the future cost.

**Why is it needed?**
Predictability gives you the confidence that the system will continue to perform at the expected level in the future

How is it achieved?
- Auto scaling
- Load balancing
- Different instance types, sizes, pricing tiers
- Cost management tools
- API to predict the pricing patterns and health monitoring

### ***Serverless***
Serverless means we don't manage the servers, we only handle writing and running the code and auto scales CPU and memory based on usage
Example : SQL DB
Bill will be generated as per the actual usage

---
