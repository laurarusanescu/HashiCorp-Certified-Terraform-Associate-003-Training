# Lesson 2.2 – What is Terraform?  

![Terraform](https://img.shields.io/badge/Terraform-CLI-blueviolet?logo=terraform)
![Lesson](https://img.shields.io/badge/Lesson-2.2-lightblue)

---

## 📌 Definition  

- **Terraform** is **HashiCorp’s Infrastructure as Code (IaC) utility**.  
- It is installed locally and run through the **Terraform Core (Terraform CLI)**.  
- CLI commands include:  
  - `terraform init` → initialize working directory  
  - `terraform plan` → preview execution plan  
  - `terraform apply` → create/update infrastructure  

---

## 🏗️ Providers  

- **Providers = services or systems** Terraform interacts with to build infrastructure.  
- Examples:  
  - Cloud: AWS, Azure, Google Cloud  
  - Virtualization: VMware  
  - Many more (hundreds available)  

👉 Providers expose their **APIs** so Terraform can communicate and build resources automatically.  

---

## 📖 Characteristics of Terraform  

- **Declarative language**  
  - You describe **what** the infrastructure should look like, not **how** to build it.  
  - Terraform handles the backend steps.  
- **Human-readable configuration files**  
  - Simplifies coding and improves clarity.  
- **Lifecycle management**  
  - Build, modify, and destroy infrastructure automatically.  

---

## 🎯 When to Use Terraform  

✅ Best for:  
- Infrastructure that is **provisioned often** (e.g., dev/test environments).  
- Infrastructure that will be **modified frequently** (e.g., scaling, evolving production).  
- Multi-cloud or hybrid-cloud setups.  

❌ Not ideal for:  
- **One-off builds** (e.g., a single web server you’ll never change).  
- Long-term static infrastructure that rarely changes.  

---

## ✅ Takeaways  

- Terraform = **IaC utility by HashiCorp**.  
- Uses **providers** to build infrastructure across many platforms.  
- Declarative, easy-to-read code.  
- Best suited for **dynamic, repeatable, or evolving infrastructure**, not static one-off deployments.  
