# 🐝 HiveBox DevOps Project  
**Phase 2 – Step-by-Step Instructions**

Welcome to the **HiveBox DevOps Project**!  
This README will guide you through **Phase 2 (Basic Implementation)** of your DevOps journey.

---


## 📍 Phase 2: Basic Implementation  
*Roadmap Module: Basics – DevOps Core*

### 2.1 Tools Setup

#### 🖥 Install Git
- **Windows**: Download from git-scm.com  
- **macOS**: brew install git or download  
- **Linux**: apt-get install git or yum install git  
Verify: git --version

#### 🖥 Install VS Code
- Download VS Code  
- Recommended extensions: Python, Docker, GitLens, YAML, Kubernetes

#### 🖥 Install Docker
- Windows/macOS: Download Docker Desktop  
- Linux: Follow official guide  

Verify: docker --version

---

### 2.2 Code Implementation

Clone and setup:
git clone https://github.com/YOUR_USERNAME/devops-hands-on-project-hivebox.git
cd devops-hands-on-project-hivebox
git checkout -b phase-2

Project structure:
hivebox/
├── app/
│   ├── __init__.py
│   ├── main.py
│   └── version.py
├── requirements.txt
├── Dockerfile
├── README.md
└── .gitignore

---

### 2.3 Containerization

Dockerfile, build & run steps provided in README.

---

### 2.4 Testing

Run local tests:
python -m app.main

Run Docker container:
docker run --rm hivebox:0.0.1

Verify output: HiveBox version: 0.0.1

---

### 2.5 Final Steps

Commit & push:
git add .
git commit -m "feat: implement Phase 2 - basic version app and Docker container"
git push origin phase-2

Create PR and update board.

---

## 🚀 Next Steps
- Build REST API
- Integrate with openSenseMap
- Add tests and CI/CD
