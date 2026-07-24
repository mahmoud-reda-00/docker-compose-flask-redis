# Flask + Redis with Docker Compose

A simple web application built with **Flask** and **Redis**, containerized using **Docker** and orchestrated with **Docker Compose**.

The application counts the number of visits using Redis and displays the current visitor count on the web page.

---

## 🚀 Features

- Flask web application
- Redis as an in-memory database
- Dockerized application
- Docker Compose orchestration
- Automatic communication between containers

---

## 🏗️ Project Structure

```
.
├── app.py
├── Dockerfile
├── docker-compose.yml
├── requirements.txt
├── templates/
│   └── index.html
└── README.md
```

---

## 🛠️ Technologies Used

- Python
- Flask
- Redis
- Docker
- Docker Compose

---

## 📦 Prerequisites

Before running the project, make sure you have:

- Docker
- Docker Compose

---

## ▶️ Run the Application

Clone the repository:

```bash
git clone https://github.com/your-username/flask-redis-docker.git
cd flask-redis-docker
```

Build and start the containers:

```bash
docker compose up --build
```

Open your browser:

```
http://localhost:5000
```

---

## 🧱 Services

### Web

- Built from the local Dockerfile
- Runs the Flask application
- Exposes port **5000**

### Redis

- Uses the official Redis Alpine image
- Stores the visitor counter

---

## 🔄 How It Works

1. User visits the application.
2. Flask receives the request.
3. Flask sends an increment request to Redis.
4. Redis increases the `hits` counter.
5. Flask displays the updated number on the page.

---

## 🏛️ Architecture

```
+-----------+
|  Browser  |
+-----------+
      |
      v
+----------------+
| Flask Container|
+----------------+
      |
      v
+----------------+
| Redis Container|
+----------------+
```

---

## 📋 Docker Compose

```yaml
services:
  web:
    build: .
    ports:
      - "5000:5000"
    depends_on:
      - redis

  redis:
    image: redis:alpine
```

---

## 🧹 Stop the Application

```bash
docker compose down
```

To remove containers, networks, and volumes:

```bash
docker compose down -v
```

---

## 📸 Demo

After opening:

```
http://localhost:5000
```

You will see something like:

```
Hello from Flask!

Visitor Count: 25
```

Each page refresh increments the counter stored in Redis.

---

## 📚 Learning Objectives

This project demonstrates:

- Building Docker images
- Writing Dockerfiles
- Using Docker Compose
- Running multi-container applications
- Container networking
- Service discovery using Docker DNS
- Integrating Flask with Redis

---

## 👨‍💻 Author

Mahmoud Reda Hassan Saafan

GitHub: https://github.com//mahmoud-reda-00
LinkedIn: https://linkedin.com/in/mahmoud-saafan-8178b2247
