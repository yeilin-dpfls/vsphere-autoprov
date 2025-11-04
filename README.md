# vsphere-autoprov
Ansible-based automation system for provisioning and configuring virtual machines (VyOS, Server) on VMware vSphere.Ansible-based automation system for provisioning and configuring virtual machines (VyOS, Server) on VMware vSphere


# 🚀 vSphere AutoProv
> **Ansible-based automation system for provisioning and configuring virtual machines (VyOS & Server) on VMware vSphere.**

![VMware + Ansible](https://github.com/ansible/ansible/raw/devel/docs/docsite/rst/images/ansible_vsphere.png)

---

## ✨ Overview

**vSphere AutoProv** is a fully automated provisioning framework that leverages **Ansible** to deploy and configure **VyOS routers** and **Linux servers** on **VMware vSphere**.  
It simplifies complex multi-VM setups into a single, repeatable playbook — ideal for building lab environments, infrastructure templates, or production-ready systems.

---

## 🧩 Features

- ⚙️ **Automated VM Provisioning** — Create, clone, and power on VMs on vSphere automatically.  
- 🌐 **VyOS Configuration** — Apply network configurations dynamically (interfaces, routes, firewall, etc).  
- 🖥️ **Server Initialization** — Configure OS settings, users, SSH keys, and packages with Ansible roles.  
- 🔁 **Idempotent Design** — Run playbooks multiple times without side effects.  
- 📦 **Modular Roles** — Clean role-based structure for easy maintenance and expansion.  

---

## 🏗️ Architecture

```mermaid
flowchart TD
    A[Ansible Controller] -->|Ansible Playbook| B[vSphere API]
    B --> C[VM Template (VyOS)]
    B --> D[VM Template (Server)]
    C --> E[Configured VyOS Router]
    D --> F[Configured Application Server]

📁 Project Structure
pgsql
코드 복사
vsphere-autoprov/
├── inventory/
│   ├── hosts.ini
│   └── group_vars/
├── roles/
│   ├── vyos/
│   └── server/
├── playbooks/
│   ├── deploy_vyos.yaml
│   ├── deploy_server.yaml
│   └── site.yaml
├── ansible.cfg
└── README.md

🚀 Quick Start
1️⃣ Prerequisites
VMware vSphere (vCenter)

Ansible ≥ 2.15

Python packages: pyvmomi, community.vmware

SSH access to target systems

2️⃣ Configuration
Edit inventory/hosts.ini and update your vSphere credentials:

ini
코드 복사
[vsphere]
vcenter.example.com ansible_user=administrator@vsphere.local ansible_password=secret
3️⃣ Run the playbook
bash
코드 복사
ansible-playbook -i inventory/hosts.ini playbooks/site.yaml

🖼️ Screenshots
VM Deployment	VyOS Configuration

⚡ Example Output
bash
코드 복사
PLAY [Deploy VyOS and Server VMs on vSphere] **********************************

TASK [Create VM from template] ************************************************
changed: [vcenter.example.com -> localhost]

TASK [Configure VyOS routing] *************************************************
ok: [vyos-router]

TASK [Setup server user accounts] *********************************************
changed: [app-server]

🧠 Tech Stack
Category	Technology
Automation	Ansible
Virtualization	VMware vSphere
Networking	VyOS
Scripting	Python, YAML

🛠️ Roadmap
 Support for vSphere Datastore Clusters

 Terraform integration

 Dynamic inventory generation

 Role for Windows Server provisioning

🤝 Contributing
Pull requests are welcome!
For major changes, please open an issue first to discuss what you’d like to improve.


## 이름들 작성 해주세요
🧭 Author
Kim Seongchan
💼 Automation Engineer | ☁️ Infrastructure & Network Specialist
📧 Contact: your.email@example.com
