# RetailX-Store-Chain

# RetailX – Secure Azure Retail Architecture

Secure, production-grade Azure architecture for a multi-location retail organization implementing network segmentation, Private Endpoints, identity-based access control, Defender for Cloud protection, and centralized monitoring aligned with enterprise cloud standards.

# **Architecture Pattern**
Public retail web application with fully private backend services using:
- Virtual Network segmentation.
- Private Endpoints.
- Managed Identity authentication.
- RBAC-controlled access.
- Microsoft Defender for Cloud.
- Centralized monitoring and alerting.

# **Architecture Overview**
 The environment follows a secure layered retail-grade design:
 - Public-facing App Service (HTTPS enforced).
 - Private Azure SQL Database (Orders & Transactions).
 - Private Storage Account (Inventory & Receipts).
 - Private Key Vault (Secret Management).
 - Subnet segmentation (Web + Data + Management).
 - NSG-controlled private subnets.
 - Private DNS zone integration.
 - Centralized Log Analytics workspace.
 - Azure Monitor alerts.
 - Microsoft Defender for Cloud security posture management.

# **Security by Design Principles**
- Zero public exposure of backend services.
- Least privilege RBAC model (group-based only).
- Managed Identity instead of stored credentials.
- Private DNS resolution for all data services.
- HTTPS-only application layer.
- NSG-enforced subnet isolation.
- Defender for Cloud security posture monitoring.
- Centralized logging and alerting.

# **Phase 0 – Resource Organization**
- Dedicated resource groups (Net, App, Data, Sec, Ops).
- Consistent tagging model.
- Environment classification (Confidential – Retail Data).

# **Phase 1 – Identity & RBAC**
- Microsoft Entra ID security groups.
- Group-based RBAC assignments.
- Separation of duties (Admins / Engineers / Auditors).
- No direct user role assignments.

# **Phase 2 – Network Segmentation**
- Virtual Network with segmented subnets.
- Separate Web, Data, and Management subnets.
- NSG applied to private subnets.
- Private DNS zones configured.
- Private connectivity foundation established.
  
# **Phase 3 – Application Layer**
- Azure App Service (Premium tier).
- System-assigned Managed Identity enabled.
- VNet Integration configured.
- HTTPS-only enforced.
 
# **Phase 4 – Secure SQL Deployment**
- Azure SQL Database (General Purpose tier).
- Public network access disabled.
- Private Endpoint configured.
- Private DNS integration.
- Defender for SQL enabled.

# **Phase 5 – Secure Storage Deployment**
- Azure Storage Account (Standard LRS).
- Public access disabled.
- Private Endpoint configured.
- Blob soft delete and versioning enabled.
- Defender for Storage enabled.

# **Phase 6 – Secrets Management**
- Azure Key Vault (RBAC model).
- Public access disabled.
- Private Endpoint configured.
- Managed Identity access (Key Vault Secrets User).
- Secure storage of connection strings and API secrets.

# **Phase 7 – Monitoring & Threat Detection**
- Log Analytics workspace deployed.
- Diagnostic settings streaming from all services.
- Azure Monitor alert rules configured:
     - App availability.
     - SQL CPU threshold.
     - Storage anomaly detection.
- Microsoft Defender for Cloud posture review.

# **Phase 8 – Production Validation**
- Confirmed zero public exposure of backend services.
- Verified private endpoint DNS resolution.
- Validated Managed Identity authentication.
- Reviewed Defender security recommendations.
- Confirmed operational alert functionality.

# **Operational Impact**

Formal security validation checklist executed post-deployment.

This deployment demonstrates:

- Enterprise retail-grade Azure security architecture.
- Zero Trust networking principles.
- Identity-based service-to-service authentication.
- Proactive security posture management.
- Threat detection and monitoring readiness.
- Production-ready governance structure.

#  **Deployment Specifications**
| Component          | Configuration                      |
| ------------------ | ---------------------------------- |
| Region             | Canada Central                     |
| Environment        | Production                         |
| Architecture Model | Segmented VNet (Web + Data + Mgmt) |
| Network Model      | Private Endpoints + Private DNS    |
| Identity Model     | Entra ID + Managed Identity        |
| Monitoring         | Log Analytics + Azure Monitor      |
| Security Posture   | Microsoft Defender for Cloud       |
| Access Control     | RBAC (Group-Based)                 |
