# Lesson 2.2 – What is Terraform?  


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

  # Lesson 2.3 – Why Use Terraform?  


---

## 🚀 Reasons to Use Terraform  

1. **Quick & Efficient**  
   - Replicate and modify infrastructure rapidly.  
   - Automates provisioning and changes.  

2. **Multi-Cloud Support**  
   - Works with AWS, Azure, Google Cloud, VMware, and many more providers.  
   - Single tool to manage hybrid and multi-cloud environments.  

3. **Human-Readable Language (HCL)**  
   - Terraform uses **HCL – HashiCorp Configuration Language**.  
   - Benefits:  
     - Easy to read and understand.  
     - Easy to write (well-documented block types, identifiers, expressions).  
   - **Limitation**: Only built-in functions are supported (no custom/user-defined functions).  
     - Over 100 built-in functions available.  

4. **State Management**  
   - Terraform tracks resource changes via **state files**.  
   - Benefits:  
     - Ensures consistent runs across teams and time.  
     - Maintains dependencies between resources.  
   - State is stored in a local or remote **`.tfstate`** file.  

5. **Version Control Integration**  
   - Configurations can be committed to Git (GitHub, GitLab, Bitbucket, etc.).  
   - Enables safe **collaboration** and **change history tracking**.  

---

## ✅ Key Takeaways  

- Terraform = **quick, efficient, multi-cloud automation tool**.  
- Uses **HCL** for human-readable and declarative configs.  
- **State management** ensures consistency and reliability.  
- Integrates smoothly with **version control systems** for team collaboration.  

