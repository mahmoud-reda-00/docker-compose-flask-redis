# Flask + Redis with Docker Compose & ci/cd ( GitHub Actions )

A simple multi-container application built with **Flask** and **Redis**, containerized using **Docker** and automated with **GitHub Actions CI**.

## 🚀 Features

* Flask web application
* Redis integration
* Dockerized application
* Docker Compose orchestration
* Automated CI pipeline with GitHub Actions
* Docker image automatically pushed to Docker Hub

---

## 🛠️ Tech Stack

* Python
* Flask
* Redis
* Docker
* Docker Compose
* GitHub Actions
* Docker Hub

---

## 📂 Project Structure

```text
.
├── .github/
│   └── workflows/
│       └── docker-ci.yml
├── templates/
│   └── index.html
├── app.py
├── Dockerfile
├── docker-compose.yml
├── requirements.txt
└── README.md
```

---

## 🏗️ Architecture

```text
Browser
    │
    ▼
Flask Container
    │
    ▼
Redis Container
```

---

## ⚙️ CI Pipeline

Every push to the **main** branch automatically triggers GitHub Actions.

Pipeline Steps:

* Checkout repository
* Build Docker image
* Start containers using Docker Compose
* Run Integration Test
* Login to Docker Hub
* Push Docker Image

---

## ▶️ Run Locally

```bash
git clone https://github.com/mahmoud-reda-00/docker-compose-flask-redis.git

cd docker-compose-flask-redis

docker compose up --build
```

Open:

```
http://localhost:5000
```

---

## 🧪 Integration Test

The CI pipeline verifies that:

* Flask starts successfully.
* Redis is running.
* Containers communicate correctly.
* The application responds over HTTP.

---

## 🐳 Docker Hub

Docker Image:

```
mv7moud/flask-redis-app:latest
```

Pull the image:

```bash
docker pull mv7moud/flask-redis-app:latest
```

Run:

```bash
docker run -p 5000:5000 mv7moud/flask-redis-app:latest
```

---

## 📚 What I Learned

* Writing Dockerfiles
* Multi-container applications
* Docker Compose networking
* Flask & Redis integration
* GitHub Actions
* CI Pipelines
* Docker Hub automation

---

## 👤 Author

Mahmoud Reda Hassan Saafan

GitHub:
https://github.com/mahmoud-reda-00

Docker Hub:
https://hub.docker.com/u/mv7moud
