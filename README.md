## 🧩 Assessment Sections

---

## 1. Network Architecture Design

Design a secure multi-VPC AWS network architecture that includes:

- DR and Production VPCs  
- AWS Transit Gateway  
- Palo Alto firewall for centralized security  
- Shared Services VPC  
- Site-to-Site VPN to on-premises  
- Segmentation between environments  
- Outbound traffic inspection through the firewall  

**Deliverables:**

- A high-level network architecture diagram  
- A routing flow description (VPC ↔ TGW ↔ Palo Alto ↔ Internet/On-Prem)  
- Explanation of segmentation and security controls (Security Groups, NACLs, firewall policies)

---

## 2. AWS Networking Implementation

Choose **one** of the following scenarios and describe how you would implement it in AWS:

- A new VPC that must be integrated into an existing Transit Gateway architecture  
- A new Site-to-Site VPN using Transit Gateway  
- A VPC Peering connection with a vendor or partner  

**Include:**

- Required AWS resources  
- Route table updates  
- Security configurations  
- Palo Alto considerations (zones, NAT, policies)  
- (Optional) IaC code examples

---

## 3. Palo Alto Firewall Configuration

You must onboard a new AWS-hosted application with the following requirements:

- Only HTTPS inbound access from an office IP range  
- Outbound access only to specific third-party APIs  
- Full session logging and monitoring  

**Describe how you would configure:**

- Address objects and groups  
- Security policies  
- NAT rules  
- Log forwarding profiles  
- Best practices for maintainable and secure firewall rule design  

---

## 4. Troubleshooting Scenarios

> **Important:**  
> These scenarios are reasoning and analysis exercises only.  
> You are **not** required to deploy or modify any real resources in AWS or on Palo Alto devices.  
> Focus on explaining **how** you would investigate and solve the issues, not on actually implementing changes.

### 4.1 AWS–On-Prem Connectivity Issue  
An EC2 instance in the Production VPC cannot reach an on-prem server over a Site-to-Site VPN through Transit Gateway.

**Explain your full troubleshooting process**, including (but not limited to):  
- Transit Gateway routing and route tables  
- VPC route tables and subnet configuration  
- Firewall rules and security controls (AWS Security Groups, NACLs, Palo Alto policies)  
- On-prem routing and firewall considerations  
- Use of VPC Flow Logs, CloudWatch, and Palo Alto logs  
- Any diagnostic commands or tools you would use (ping, traceroute, test traffic, etc.)

---

### 4.2 Palo Alto IPSec Tunnel Error  
A VPN tunnel between Palo Alto and AWS fails to establish. The error is:

> **"No proposal chosen"**

Without changing any real configuration, **describe**:  
- The most likely root causes of this error  
- Which parameters you would compare on both sides (Palo Alto and AWS)  
- The step-by-step process you would follow to validate and correct the mismatch  

---

### 4.3 Asymmetric Routing  
An application in AWS experiences intermittent failures, and Palo Alto logs show **session mismatches**.

**Explain**, at a conceptual and procedural level:

- How asymmetric routing can occur in AWS + Transit Gateway topologies  
- What indicators or logs you would review to confirm asymmetric routing  
- What changes you would propose (for example, routing adjustments, design changes, firewall behavior) to fix the issue permanently

---

## 5. Scalability

Explain how you would scale:

- AWS network components (VPCs, TGW attachments, VPN redundancy)  
- Palo Alto firewalls (HA, active/passive, autoscaling, VM-Series load balancing)

---

## 6. Security Best Practices

Describe the security measures you would implement across:

- AWS networking (subnet design, SGs, NACLs)  
- Palo Alto firewalls (zones, security policies, threat prevention)  
- IAM roles and least privilege  
- Data encryption (at rest and in transit)  
- Monitoring (CloudWatch, Flow Logs, PAN logs, CloudTrail)

---

## 7. Cost Management

Provide a brief cost analysis of your proposed architecture, touching on:

- Transit Gateway pricing  
- NAT Gateway usage  
- Palo Alto licensing/cost considerations  
- Data transfer and VPN costs  

Propose **cost optimization strategies** without compromising security.

---