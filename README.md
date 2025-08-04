Here's the **complete `README.md` file** (with badges, setup, API, and author section) — just **copy and paste this into your `README.md` file**:

---

```markdown
# 📝 backend-todo-app-Docker

![Docker](https://img.shields.io/badge/docker-ready-blue?logo=docker)
![Node.js](https://img.shields.io/badge/node.js-18.x-green?logo=node.js)
![PostgreSQL](https://img.shields.io/badge/postgres-db-blue?logo=postgresql)
![License](https://img.shields.io/badge/license-MIT-lightgrey)

A full-featured **backend REST API for a TODO application**, built using:
- ✅ Node.js + Express
- ✅ PostgreSQL + Prisma ORM
- ✅ Docker + Docker Compose

All user data and todo items are stored in a relational database, with secure JWT-based authentication.

---

## 🚀 Features

- 🔐 User Registration & Login
- 🔑 JWT Auth for protected routes
- 📋 CRUD operations for TODOs
- 🛠 Prisma ORM for PostgreSQL
- 🐳 Dockerized development & DB setup
- 🌱 .env support for easy config

---

## 🛠 Tech Stack

| Layer       | Technology               |
|-------------|---------------------------|
| Backend     | Node.js, Express          |
| Database    | PostgreSQL (via Prisma)   |
| Auth        | JWT + bcryptjs            |
| DevOps      | Docker, Docker Compose    |

---

## 📁 Project Structure

```

.
├── src
│   ├── routes
│   │   ├── authRoutes.js
│   │   └── todoRoutes.js
│   ├── prismaClient.js
│   └── server.js
├── prisma
│   └── schema.prisma
├── Dockerfile
├── docker-compose.yml
└── .env

````

---

## ⚙️ Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/RushiAgrawal2004/backend-todo-app-Docker.git
cd backend-todo-app-Docker
````

### 2 Start Using Docker

```bash
docker-compose up --build
```

> This will spin up:
>
> * A PostgreSQL database
> * The backend server on [http://localhost:5003](http://localhost:5003)

---

## 📮 API Endpoints

### 🔐 Auth Routes

| Method | Endpoint       | Description         |
| ------ | -------------- | ------------------- |
| POST   | /auth/register | Register a new user |
| POST   | /auth/login    | Log in & get token  |

### ✅ TODO Routes (Protected)

| Method | Endpoint    | Description          |
| ------ | ----------- | -------------------- |
| GET    | /todos      | Get all todos        |
| POST   | /todos      | Create new todo      |
| PUT    | /todos/\:id | Update existing todo |
| DELETE | /todos/\:id | Delete todo by ID    |

✅ You must pass the JWT token in headers:
`Authorization: Bearer <token>`

---

## 📚 Prisma ORM

* Models: `User` & `Todo` with relationships
* Migrations auto-run in Docker container
* DB logic abstracted with Prisma Client

---

## 🧪 Testing (Coming Soon)

* ✅ Unit testing (Jest)
* ✅ Swagger/OpenAPI docs
* ✅ CI/CD with GitHub Actions

## 👨‍💻 Author

Built with 💙 by [Rushikesh Agrawal](https://github.com/RushiAgrawal2004)


