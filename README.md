# Jenkins Pipeline: Scheduled Python Script Execution

This repository contains a Jenkins pipeline that automatically executes a Python script (`view_machine_data.py`) on a schedule. The pipeline polls the source code repository every minute and runs the script if any changes are detected.

---

## 📜 Pipeline Overview

### **Key Features**
- **Build History Control** – Keeps only the **last 2 builds** to save disk space.
- **Execution Timeout** – Automatically stops the pipeline if it runs longer than **1 minute**.
- **SCM Polling** – Checks the repository for changes **every minute** (`* * * * *`).
- **Python Script Execution** – Runs:
  ```bash
  python3 view_machine_data.py
