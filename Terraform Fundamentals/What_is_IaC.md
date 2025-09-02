# Lesson 2.1 – What is IaC?  
---

## 📌 Definition  

- **IaC = Infrastructure as Code**  
- Code used to **provision resources** such as:  
  - Virtual Machines (e.g., AWS EC2 instances)  
  - Network infrastructure (gateways, subnets, security groups)  
  - Users & access control (e.g., AWS IAM users)  
- Works **on cloud and on-premises** infrastructure.  

In essence, **technology infrastructure is modeled with code**, which ensures:  
- **Consistency & reliability** across environments  
- **Repeatability** of work  

---

## 📝 Key Characteristics  

- Infrastructure setup is handled via **human-readable configuration files**.  
- Example: `main.tf` with blocks for:  
  - `terraform` → providers & version  
  - `provider` → configuration for AWS  
  - `resource` → defines resources (e.g., IAM users)  

Compared to traditional programming (C++, JS), Terraform’s declarative code is **simpler and more human-friendly**.  

---

## ⚖️ Core Principles of IaC  

1. **Versioned Infrastructure**  
   - Infrastructure configurations should be versioned (e.g., Git, GitHub, GitLab).  
   - Enables history tracking and collaboration.  

2. **Idempotence**  
   - Running the same config multiple times produces the **same result**.  
   - Terraform only applies changes when necessary.  
   - Ensures consistent state every time.  

3. **Self-Describing Infrastructure**  
   - Code **explains itself** (declarative).  
   - Example: a `resource` block clearly states the resources being provisioned.  
   - Infrastructure state can be read from code & Terraform state files.  

---

## 🔑 Additional Principles  

- **Easily Re-creatable Systems** – Stand up or tear down infra quickly.  
- **Repeatable Processes** – Run the same code multiple times reliably.  
- **Disposable Systems** – Destroy resources at will (be cautious!).  
- **Self-Documentation** – Code itself acts as documentation (plus comments).  
- **Ever-Evolving Design** – Infrastructure can be changed incrementally.  
  - Example: Changing a user count from 3 → 20 in code.  
- **Generic Modules** – Reusable code blocks, community-provided or custom.  

---

## ✅ Takeaways  

- IaC allows infrastructure to be: **consistent, reliable, repeatable, and automated**.  
- Terraform implements IaC with **declarative, human-readable code**.  
- Understanding IaC principles is **essential before diving deeper** into Terraform.  
