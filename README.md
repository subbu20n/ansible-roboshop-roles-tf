##![Roboshop](https://github.com/subbu20n/Ansible-Roboshop/blob/main/robot%20shop.png)

# Roboshop Microservices Deployment using Ansible Roles

This repository contains a real-time implementation of **Ansible Roles** to automate the deployment of the **Roboshop microservices-based e-commerce application**.

> 🛠️ This project is inspired by actual infrastructure automation work I perform as a DevOps Engineer. It reflects real-world practices used to manage scalable, repeatable, and secure microservice deployments using Ansible.

---

## 🚀 Project Goals

- Automate the deployment of each Roboshop microservice using Ansible roles
- Follow a **modular, reusable, and environment-agnostic structure** 
- Secure secrets and credentials using **Ansible Vault**
- Make the deployment **scalable, maintainable, and production-ready**

---
    
## 🛒 What is Roboshop?    

Roboshop is an open-source **e-commerce application** designed using a **microservices architecture**. Each component (frontend, user, payment, cart, etc.) runs independently and communicates over internal services.

### Microservices Managed:

- Catalogue
- Cart
- User
- Payment
- Shipping
- RabbitMQ
- Redis
- MongoDB
- MySQL
- Frontend (Nginx)

---

## 📚 Key Ansible Concepts Demonstrated

| Concept             | Description                                                                 |
|---------------------|-----------------------------------------------------------------------------|
| `Roles`             | Used for each microservice to modularize tasks                              |
| `Playbooks`         | Top-level execution files to call roles                                     |
| `Variables`         | `defaults`, `vars`, `group_vars`, `host_vars` for flexible config           |
| `Templates`         | Jinja2 templates for dynamic configuration files                            |
| `Handlers`          | Restarting services upon changes                                            |
| `Loops`             | Repeating tasks like package installation or user creation                  |
| `Tags`              | Enable partial playbook execution                                           |
| `Conditionals`      | Control task flow based on environment or state                             |
| `Ansible Vault`     | Secure secrets management (`db passwords`, `api keys`)                      |
| `Crontab`           | Schedule periodic jobs (optional but included where needed)                 |
| `Error Handling`    | Using `ignore_errors`, `failed_when`, and `block/rescue`                    |

---

## 📁 Repository Structure

```

Ansible-Roboshop-Roles/
├── roles/
│   ├── catalogue/
│   ├── cart/
│   ├── user/
│   ├── payment/
│   ├── shipping/
│   ├── mysql/
│   ├── mongodb/
│   ├── rabbitmq/
│   ├── redis/
│   └── nginx/
├── playbooks/
│   ├── payment.yml
│   └── all-services.yml
├── inventory/
│   └── hosts.ini
├── group\_vars/
│   └── all.yml
├── host\_vars/
│   └── service-specific vars
├── vault/
│   └── secrets.yml
├── templates/
│   └── nginx.conf.j2
└── README.md

````

---

## ⚙️ Example Usage

```

# Deploy the payment microservice
ansible-playbook -i inventory/hosts.ini playbooks/payment.yml

````

---

## 🧰 Real-World Skills Demonstrated

* **Microservices orchestration** using Ansible roles
* **Secure automation** using Vault and environment-specific variables
* **DevOps best practices** like modular code, version control, and idempotent deployments
* **Troubleshooting and iterative execution** using tags and handlers

---

## 📌 Use Cases

* Multi-service e-commerce application deployment
* Role-based Ansible automation in cloud/on-prem environments
* CICD integration for Ansible playbooks (can be extended to Jenkins or GitHub Actions)
* Infrastructure automation showcase for interviews and portfolios

---

## 👨‍💼 About Me

I’m currently working as a **DevOps Engineer**, and this project reflects the type of automation I deliver in real-world environments. This repository demonstrates my practical knowledge of Ansible, microservices deployment, infrastructure-as-code, and secure configuration management.

Feel free to connect:

* [LinkedIn](https://www.linkedin.com/in/subbarayudu-nandyala/)
* [GitHub](https://github.com/subbu20n)