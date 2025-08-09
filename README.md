# Ansible Apache Project

This project automates the installation and configuration of the **Apache HTTP Server** on remote servers using **Ansible**.  
It is designed to be a beginner-friendly example for understanding **Ansible Playbooks**, **inventory management**, and **Jinja2 templating**.

-------------------------------------------

## 📌 Project Overview

The playbook performs the following tasks:
- Installs Apache HTTP Server.
- Ensures the service is started and enabled on boot.
- Deploys a custom HTML page with server details using **Ansible facts**.
- Displays:
  - Operating System
  - Deployment Time

--------------------------------------------

## 🛠️ Technologies Used

- **Ansible** – Configuration management tool.
- **YAML** – Playbook definition.
- **Jinja2** – Templating engine for dynamic HTML.
- **Apache HTTP Server** – Web server for hosting pages.
- **Linux** – Target host OS.

---------------------------------------------

## 📂 Project Structure

ansible-apache-project/
│
├── inventory # Ansible inventory file with target hosts
├── apache.yml # Main Ansible Playbook
├── templates/
│ └── index.html.j2 # Jinja2 HTML template for the web page
└── README.md # Project documentation

-----------------------------------------------
## 🚀 How to Run

1️⃣ **Clone the Repository**
```bash
git clone https://github.com/Attiq2/ansible-apache-project.git
cd ansible-apache-project
