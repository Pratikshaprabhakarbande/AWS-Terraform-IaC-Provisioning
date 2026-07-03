
# 🏗️ Automated AWS Infrastructure Provisioning via Terraform

<div align="center">
  <img src="https://img.shields.io/badge/IaC-Terraform-5835CC?style=for-the-badge&logo=terraform" alt="Terraform"/>
  <img src="https://img.shields.io/badge/Cloud-AWS-FF9900?style=for-the-badge&logo=amazon-aws" alt="AWS"/>
  <img src="https://img.shields.io/badge/Language-HCL-blue?style=for-the-badge" alt="HCL"/>
</div>

## 📌 Project Overview
This DevSecOps project demonstrates the core principles of **Infrastructure as Code (IaC)**. It utilizes Terraform to automate the secure provisioning and management of cloud infrastructure on Amazon Web Services (AWS). This approach eliminates manual console configurations, ensuring deployments are repeatable, version-controlled, and highly scalable.

### 🎯 Key Objectives
- **Automated Deployment:** Provision complete network and compute environments using declarative configuration files.
- **Security by Design:** Implement strict AWS Security Group rules to control inbound and outbound traffic, mimicking enterprise-level least-privilege principles.
- **State Management:** Utilize Terraform state files to track resource changes and maintain infrastructure consistency.

---

## 🛠️ Tech Stack & Provider
*   **Language:** HashiCorp Configuration Language (HCL)
*   **Infrastructure Tool:** Terraform (CLI)
*   **Cloud Provider:** AWS (Amazon Web Services)
*   **Resources Provisioned:** EC2 Instances, Virtual Private Cloud (VPC), Subnets, Route Tables, and Security Groups.

---

## 🚀 Key Features

*   **Modular Configuration:** Uses `variables.tf` to parameterize the deployment, making the code reusable across different environments (Dev, Staging, Prod).
*   **Idempotent Operations:** Ensures that running the code multiple times results in the exact same desired state without duplicating resources.
*   **Secure Networking:** Configures custom VPCs rather than relying on default AWS networks, demonstrating a strong understanding of cloud networking boundaries.
*   **One-Click Teardown:** Ability to safely and completely destroy all provisioned resources to prevent unexpected cloud billing costs.

---

## ⚙️ Installation & Usage

### Prerequisites
1. Install the [Terraform CLI](https://developer.hashicorp.com/terraform/downloads).
2. Install the [AWS CLI](https://aws.amazon.com/cli/) and configure it with an IAM user that has programmatic access (`aws configure`).

### Deployment Steps

```bash
# 1. Clone the repository
git clone [https://github.com/Pratikshaprabhakarbande/terraform-first-project.git](https://github.com/Pratikshaprabhakarbande/terraform-first-project.git)
cd terraform-first-project

# 2. Initialize the working directory (downloads the AWS provider)
terraform init

# 3. Validate the syntax of the Terraform files
terraform validate

# 4. Generate an execution plan to preview changes before applying
terraform plan

# 5. Execute the actions proposed in the plan (Type 'yes' to confirm)
terraform apply

# 6. Destroy all remote objects managed by this configuration (Crucial for avoiding AWS charges)
terraform destroy
