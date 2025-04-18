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
Django_App is a **Django web application** containing multiple apps (**core, dashboard, reports**) with static views. The project is **containerized using Docker** and supports **automated deployment with Jenkins**.  

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
pip install -r requirements.txt
python manage.py runserver
```
➡️ Open http://127.0.0.1:8000/ in your browser.

---

### 🐳 Run with Docker
#### **1️⃣ Build the Docker Image**
```sh
docker build -t studentproject .
```

#### **2️⃣ Run the Container**
```sh
docker run -p 8000:8000 studentproject
```

➡️ Open http://127.0.0.1:8000/ in your browser.

---

### 📌 CI/CD Pipeline (Jenkins)
#### **1️⃣ Create a Jenkinsfile**
This project includes a Jenkinsfile that:

Pulls code from GitHub

Builds a Docker image

Pushes the image to Docker Hub

#### **2️⃣ Push Docker Image to Docker Hub**
```sh
docker tag studentproject your-dockerhub-username/studentproject:v1
docker push your-dockerhub-username/studentproject:v1
```
➡️ Now anyone can pull it using:

```sh
docker pull your-dockerhub-username/studentproject:v1
```

---


# **Final Assignment : Flask Web Application with Bootstrap, GitHub, and Docker**


**<b>Part1: Flask Application</b>**
1. Displays a "Hello, World!" message on the homepage.
2. Has a second route that displays a form to accept a user's name and age, and returns a greeting message with these inputs.
3. Implements basic error handling for invalid inputs.


```bash 
 error = None
    if request.method == 'POST':
        name = request.form['name'].strip()
        age = request.form['age'].strip()

        # Implements basic error handling for invalid inputs.
        # Validate name: only letters and spaces
        if not name or not re.match("^[A-Za-z ]+$", name):
            error = "Please enter a valid name (letters and spaces only)."
        elif not age.isdigit() or int(age) <= 0:
            error = "Please enter a valid positive age."
        else:
            return render_template('greet.html', name=name, age=age)
 
```


### Links
GitHub Repository: [Github Repo URL](https://github.com/SRCEM-AIM-Class-A/A64_viraj_yawale.git)

Docker Hub Image: [DockerHub Repo URL](https://hub.docker.com/repository/docker/virajyawale/software_lab_3/tags)

