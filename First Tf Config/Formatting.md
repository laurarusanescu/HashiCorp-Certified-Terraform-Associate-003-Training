# Lesson 3.3 – Formatting Terraform Code  

![Terraform](https://img.shields.io/badge/Terraform-fmt-blueviolet?logo=terraform)
![Lesson](https://img.shields.io/badge/Lesson-3.3-lightblue)

---

## 📌 Why Formatting Matters  

- Terraform is **lenient** about whitespace, indentation, and curly brace placement.  
- Misaligned code will **still run** but may be harder to read or maintain.  
- Following **Terraform standards** (2-space indentation) makes code easier to share and collaborate on.  

---

## 🛠️ The `terraform fmt` Command  

- **`terraform fmt`** automatically reformats `.tf` files.  
- Corrects:  
  - Indentation (2 spaces)  
  - Curly brace alignment  
  - Extra spaces  
- After running, Terraform reports which files were updated (e.g., `main.tf`).  

👉 Running it again on already-formatted files produces **no output**.  

---

## 📖 Command Options  

- `terraform fmt -h` → Displays help for the command.  
- Useful options:  
  - **`-check`** → Only checks formatting, makes no changes.  
  - **`-recursive`** → Formats files in subdirectories as well as current directory.  
  - **`-diff`** → Displays differences made during formatting.  

---

## ✅ Best Practices  

- Run **`terraform fmt`** regularly to keep code consistent.  
- Use **2-space indentation** as standard.  
- Before committing to Git, ensure code is formatted for team readability.  
- Consider adding `terraform fmt -check` as part of a **CI/CD pipeline** to enforce formatting.  

---

## 🔑 Takeaway  

Formatting doesn’t affect whether Terraform code runs, but it:  
- Improves **readability**.  
- Ensures **consistency** across teams.  
- Aligns with **industry standards** expected by developers and engineers.  
