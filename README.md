# Ansible-addressbook-deploy
# 📦 Ansible Project: Java + Docker + Nginx Deployment

This project automates the setup of a Java Maven build server, Docker deployment of a web application, and Nginx installation using Ansible.

## 🧩 Components

- **L1:** Java + Maven Build Server Setup
- **L2:** Docker Installation & WAR Deployment in Tomcat
- **L3:** Nginx Setup via Ansible Role

## 📁 Folder Structure

- `inventory` – Defines target nodes (build, app, nginx)
- `l1_build_java.yml` – Installs Java, Maven, Git & builds WAR
- `l2_docker_deploy.yml` – Installs Docker, builds & runs app container
- `l3_nginx_role.yml` – Uses a role to install and configure Nginx
- `roles/` – Contains the `nginx` Ansible role
- `files/` – (Optional) for static WARs or configs

## 🚀 How to Run

```bash
# L1: Setup Java Maven Build Server
ansible-playbook -i inventory l1_build_java.yml

# L2: Docker Deploy WAR in Tomcat
ansible-playbook -i inventory l2_docker_deploy.yml

# L3: Nginx Role
ansible-playbook -i inventory l3_nginx_role.yml
