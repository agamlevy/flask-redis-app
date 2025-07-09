# 🚀 Flask + Redis – Dockerized Web App

This is a **simple full-stack Docker project** combining:

- 🐍 **Flask** (Python micro web framework)
- 🔴 **Redis** (used here as a counter backend)
- 🐳 **Docker Compose** (to manage both services)

---

## 🖥️ What It Does

Every time someone accesses the root URL (`/`), a counter is incremented in Redis and shown on the page.

Example output:
Hello! This page has been viewed 14 times.

---

## 📁 File Structure

flask-redis-docker-app/
├── app.py # Flask app code
├── requirements.txt # Python dependencies
├── Dockerfile # Instructions to build Flask image
├── docker-compose.yml # Connects Flask + Redis containers
└── README.md # You're here!

---

## ⚙️ How to Run

```bash
# From inside the project folder:
sudo docker-compose up --build

Then go to http://localhost:5000
If you're on another device in the same WiFi network (like a phone),
use your computer's local IP instead of localhost.
---

🧠 Key Concepts

build:	Build a Docker image from your own Dockerfile
image:	Use a public image (e.g., Redis from Docker Hub)
depends_on:	Make sure Redis starts before Flask
Flask route /	This is the default homepage
__name__ == "__main__"	Makes sure the app runs only when executed directly
r.incr('hits')	Increments a counter inside Redis

🔗 Example Browser View
![image](https://github.com/user-attachments/assets/22289dea-5119-4cbb-857e-3a11bd04b8da)

✅ Requirements

Docker

Docker Compose

Internet connection (to pull the Redis image)
