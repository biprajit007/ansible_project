
# Nginx Load Balancer Setup with Ansible

This repository contains an Ansible playbook designed to automatically configure an **Nginx Load Balancer**, distributing incoming HTTP requests evenly across five backend web servers.

---

## 📌 Overview

The provided Ansible playbook handles:

- ✅ **Installation of Nginx** on the designated load balancer host.
- ✅ Automated **Nginx configuration** as a reverse-proxy load balancer.
- ✅ Efficient load distribution among five backend servers.

---

## 🚀 Project Structure

```
nginx-loadbalancer-ansible/
├── hosts                      # Inventory of servers
├── loadbalancer.yml           # Main Ansible playbook
└── templates
    └── nginx_lb.conf.j2       # Nginx configuration template
```

---

## 🔧 Requirements

Ensure the following prerequisites are met:

- **Ansible** installed on your local control machine:

```bash
sudo apt install ansible
```

- **SSH key-based authentication** configured on all remote hosts.
- **Ubuntu/Debian-based Linux servers** for load balancer and backend hosts.

---

## ⚙️ Configuration Steps

Update the `hosts` file to reflect your server IP addresses or domain names:

```ini
[loadbalancer]
lb.example.com ansible_host=192.168.1.10

[webservers]
web1.example.com ansible_host=192.168.1.21
web2.example.com ansible_host=192.168.1.22
web3.example.com ansible_host=192.168.1.23
web4.example.com ansible_host=192.168.1.24
web5.example.com ansible_host=192.168.1.25
```

---

## ▶️ Running the Playbook

Run the following command to deploy the load balancer:

```bash
ansible-playbook -i hosts loadbalancer.yml
```

---

## 🧪 Testing the Setup

Test your load balancer by navigating to:

```
http://<loadbalancer-ip-address>/
```

You should see the load balancing in action across your backend servers.



- **Email:** your.email@example.com  
- **GitHub:** [github.com/your-username](https://github.com/your-username)

---

*Please replace placeholder text (`your.email@example.com`, `your-username`) with your actual contact information before uploading to GitHub.*
