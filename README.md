# Terraform-IAC
# 📘 Terraform + AWS: Introduction to Infrastructure as Code (IaC)

## 🔧 What is IaC (Infrastructure as Code)?

Infrastructure as Code is the practice of managing and provisioning infrastructure using code instead of manual processes. It allows you to define, deploy, and manage infrastructure using configuration files.

### ✅ **Advantages of IaC:**

* **Consistency:** Reduces human errors and configuration drift.
* **Automation:** Enables automated deployments.
* **Version Control:** Track changes and rollback using Git.
* **Scalability:** Easily replicate environments.
* **Speed:** Faster provisioning of infrastructure.

## 🛠️ Popular IaC Tools

* **Terraform** (by HashiCorp) ✅
* AWS CloudFormation
* Ansible
* Pulumi
* Chef / Puppet

## 🌍 What is Terraform?

Terraform is an open-source IaC tool developed by HashiCorp. It enables you to define both cloud and on-prem resources in human-readable configuration language called HCL (HashiCorp Configuration Language).

### ✅ **Advantages of Terraform:**

* Supports multiple cloud providers (AWS, Azure, GCP, etc.)
* Declarative language (HCL)
* Open-source and extensible
* State management
* Modular and reusable

---

## ⚙️ Setting Up Terraform with AWS

### 1. **Install Terraform CLI**

* Download from: [https://www.terraform.io/downloads](https://www.terraform.io/downloads)
* Verify: `terraform -v`

### 2. **Install AWS CLI and Configure**

* Download from: [https://docs.aws.amazon.com/cli/latest/userguide/install-cliv2.html](https://docs.aws.amazon.com/cli/latest/userguide/install-cliv2.html)
* Configure:

```bash
aws configure
```

Enter AWS Access Key, Secret Key, Region, and Output format.

### 3. **Install VS Code**

* Download from: [https://code.visualstudio.com/](https://code.visualstudio.com/)

### 4. **Install Terraform Extension for VS Code**

* Search for "HashiCorp Terraform" in extensions
* Install for syntax highlighting, formatting, and IntelliSense

---

## 🧪 Basic Terraform CLI Commands

| Command              | Description                                                    |
| -------------------- | -------------------------------------------------------------- |
| `terraform init`     | Initializes working directory and downloads required providers |
| `terraform plan`     | Shows what actions Terraform will take without applying them   |
| `terraform apply`    | Applies the configuration and creates the infrastructure       |
| `terraform destroy`  | Destroys all resources defined in the configuration            |
| `terraform validate` | Validates Terraform files syntax                               |
| `terraform fmt`      | Formats Terraform code                                         |
| `terraform state`    | Interact with the Terraform state                              |

---

## 🌐 Types of Terraform Providers

1. **Official Providers** – Maintained by HashiCorp (e.g., AWS, Azure, Google)
2. **Partner Providers** – Maintained by technology partners (e.g., Datadog, Kubernetes)
3. **Community Providers** – Maintained by the open-source community

---

## 🧱 Types of Terraform Configuration Blocks

| Block      | Purpose                                        |
| ---------- | ---------------------------------------------- |
| `provider` | Defines cloud provider details                 |
| `resource` | Describes infrastructure to create             |
| `variable` | Accepts dynamic input from user                |
| `output`   | Displays values after apply                    |
| `module`   | Groups reusable Terraform code                 |
| `data`     | Reads existing external data                   |
| `locals`   | Defines local variables within a configuration |

---

## 🚀 What Happens When You Run `terraform init`?

* Downloads the provider plugins
* Initializes backend configuration (if any)
* Prepares the working directory for other commands

## ⚙️ What Happens During `terraform apply`?

* Reads current infrastructure state
* Compares it with desired state (defined in code)
* Plans changes
* Applies the changes
* Updates the state file

---

## 📁 What is Backend in Terraform?

A backend defines **where Terraform stores its state file**.

### Common backends:

* Local (default)
* AWS S3 (with optional DynamoDB for state locking)
* Terraform Cloud
* Remote HTTP backends

---

## 🧾 What is State File (`terraform.tfstate`)?

* Tracks the current state of infrastructure
* Required for Terraform to determine changes

### Types of State:

* **Local state** – Stored in your working directory
* **Remote state** – Stored in a remote backend (e.g., S3, Terraform Cloud)

---

## 🔐 What is `.terraform.lock.hcl`?

* Locks the provider versions used in your project
* Ensures consistent and reproducible builds
* Created during `terraform init`

---

