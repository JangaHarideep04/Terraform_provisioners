# 🛠️ Terraform EC2 + Flask Deployment (Simple Project)

This project uses **Terraform** to provision a basic **AWS infrastructure** and deploy a **Python Flask application** to an EC2 instance using `remote-exec` and `nohup`.

---

## 📌 Project Overview

- ✅ Creates a **VPC**, **subnet**, and **Internet Gateway**
- ✅ Sets up a **security group** allowing HTTP (80) and SSH (22)
- ✅ Launches a **Ubuntu EC2 instance**
- ✅ Installs Python packages and runs `app.py` using Flask
- ✅ Uses `nohup` so the Flask app keeps running even after provisioning ends

---

## 🧱 Infrastructure Components

| Resource             | Description                           |
|----------------------|---------------------------------------|
| VPC                  | Custom VPC with 192.168.0.0/28 CIDR   |
| Subnet               | Public subnet in ap-south-2a          |
| Internet Gateway     | Enables internet access               |
| Route Table          | Routes traffic to IGW                 |
| Security Group       | Allows inbound SSH and HTTP           |
| EC2 Instance         | Ubuntu instance (t3.micro)            |
| Key Pair             | Used for SSH connection               |

---

## 🔧 Prerequisites

- AWS Account with access credentials
- Terraform installed (`v1.0+`)
- Valid SSH key pair (`.pub` and `.pem`)
- Flask application file: `app.py`

---

## 🚀 How to Use

### 1. Clone the Repository

```bash
git clone <your-repo-url>
cd project-directory

```

----



### 2. Initialize Terraform

terraform init


### 3. Apply Configuration

terraform apply
Approve the plan when prompted.
