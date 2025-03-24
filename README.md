# A64_viraj_yawale
<h2>SL-3 Lab assignment</h2>

# **Assignment 1: Flask Web Application with Bootstrap, GitHub, and Docker**


**Objective:** 
The goal of this assignment is to create a simple Flask web application with Bootstrap
styling. You will commit the project to a GitHub repository, dockerize the application, and
push the Docker image to Docker Hub.

DockerHub repository : 
```bash 
docker pull virajyawale/software_lab_3:assignment1 
```

# **Assignment 2: Build a Multi-App Django Project and Deploy with Docker**

**Objective:** 
Create a Django application with the following requirements:
• The project must have multiple apps.<br>
• No database should be used.<br>
• Include a Dockerfile to containerize the application.<br>
• Write a Jenkinsfile to automate the build pipeline.<br>
• Push the Docker image to Docker Hub.<br>



### 📌 Project Overview  
StudentProject is a **Django web application** containing multiple apps (**core, dashboard, reports**) with static views. The project is **containerized using Docker** and supports **automated deployment with Jenkins**.  

---

### 🚀 Features  
- **Multi-app Django project** (Core, Dashboard, Reports)  
- **Static pages** with Bootstrap-based UI  
- **No database required** (Only templates & views)  
- **Containerized with Docker**  
- **CI/CD integration with Jenkins**  
- **Docker image hosted on Docker Hub**  

---

### 🛠 How to Run the Project  

#### **1️⃣ Clone the Repository**  
```sh
git clone https://github.com/SRCEM-AIM-Class-A/A64_viraj_yawale.git
cd Assignment2
```

#### **2️⃣ Run with Django (Without Docker)**
```sh
Copy
Edit
pip install -r requirements.txt
python manage.py runserver
```
➡️ Open http://127.0.0.1:8000/ in your browser.