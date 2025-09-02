# HashiCorp Certified Terraform Associate (003) – Notes  

![Terraform](https://img.shields.io/badge/Terraform-IaC-blueviolet?logo=terraform)
![AWS](https://img.shields.io/badge/Cloud-AWS-orange?logo=amazon-aws)
![Certification](https://img.shields.io/badge/Certification-Terraform%20Associate-success)

Personal notes from the **HashiCorp Certified Terraform Associate (003)** course by Dave Prowse.  

---

## 📘 Course Introduction  

- **Instructor**: Dave Prowse  
- **Goal**: Prepare for and pass the Terraform Associate exam.  
- **Approach**: Hands-on labs, minimal slides, quizzes & exam prep.  
- **Focus**: Learn-by-doing (kinesthetic).  

### Topics Covered  
1. Initial System Setup (Linux VM, VSCode, Terraform install)  
2. Terraform Fundamentals (IaC, workflow, docs)  
3. AWS Configurations with Terraform  
4. Commands, Variables, Modules  
5. Logging, Troubleshooting, Additional Providers  
6. Terraform Cloud  
7. Advanced Terraform (expressions, functions, configs)  
8. Exam Preparation & Tips  

---

## Lesson 2.1 – What is IaC?  

### 📌 Definition  
- **IaC = Infrastructure as Code**  
- Provision infrastructure (VMs, networks, security groups, IAM users) via **code**.  
- Ensures **consistency, reliability, repeatability** across environments.  

### 🧩 Key Principles  
1. **Versioned Infrastructure** – use Git/GitHub for configs.  
2. **Idempotence** – same config applied multiple times yields same result.  
3. **Self-Describing Infrastructure** – declarative code describes resources clearly.  

### 🔑 Additional Principles  
- Re-creatable systems  
- Repeatable processes  
- Disposable systems  
- Self-documentation (code = docs)  
- Ever-evolving design (incremental changes)  
- Generic modules (reusable building blocks)  

### ✅ Takeaway  
IaC allows infra to be **automated, repeatable, disposable, and documented**. Terraform implements IaC in a **declarative, human-readable** way.  

---

## Lesson 2.2 – What is Terraform?  

### 📌 Definition  
- **Terraform = HashiCorp’s IaC utility**.  
- Runs via **Terraform Core (CLI)**.  
- Commands:  
  - `terraform init`  
  - `terraform plan`  
  - `terraform apply`  

### 🏗️ Providers  
- Terraform interacts with **providers** (AWS, Azure, Google Cloud, VMware, etc.).  
- Providers expose APIs; Terraform downloads **provider plugins** to communicate.  

### 📖 Characteristics  
- **Declarative** – you describe *what* infra should look like, not *how*.  
- **Readable configs** – HCL language.  
- **Lifecycle management** – create, modify, destroy resources.  

### 🎯 When to Use  
✅ Use for: frequently changing or reproducible infra (dev, test, hybrid, multi-cloud).  
❌ Avoid for: one-off static setups (e.g., a single web server for years).  

---

## Lesson 2.3 – Why Use Terraform?  

### 🚀 Reasons  
1. **Quick & Efficient** – replicate and modify infra rapidly.  
2. **Multi-Cloud Support** – AWS, Azure, Google Cloud, VMware, and more.  
3. **Human-Readable Language (HCL)**  
   - Easy to read/write, declarative.  
   - ~100 built-in functions available (no user-defined functions).  
4. **State Management**  
   - Terraform tracks resources via `.tfstate` files.  
   - Ensures consistent runs, remembers dependencies.  
5. **Version Control**  
   - Store configs in GitHub/GitLab/Bitbucket.  
   - Enables collaboration and change history.  

### ✅ Takeaway  
Terraform = **fast, efficient, cloud-agnostic IaC** with readable configs, strong state management, and version control integration.  

---

## Lesson 2.5 – How Terraform Works  

### ⚙️ Workflow (3 Steps)  
1. **Write Code** – define infra in `.tf` files.  
2. **Initialize Directory** – `terraform init` downloads provider plugins.  
3. **Apply Infrastructure** – `terraform apply` provisions resources.  

👉 Running `terraform apply` = **Terraform run**.  

---

### 🧩 Code Structure  

#### 1. `terraform` Block  
- Contains:  
  - **`required_version`** – required Terraform version.  
  - **`required_providers`** – specifies providers & versions.  
- Downloads **provider plugins** from HashiCorp.  
- Example: `~> 4.16` means latest minor version only.  

#### 2. `provider` Block  
- Configures how a provider plugin will run.  
- Example:  
  ```hcl
  provider "aws" {
    region = "us-east-2"
  }
