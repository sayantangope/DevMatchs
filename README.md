<div align="center">
  <h1>⚡ DevMatchs</h1>

  <p align="center">
    <em>Connect. Collaborate. Build. — Where developers find their perfect team.</em>
  </p>

  <p align="center">
    <img src="https://img.shields.io/github/last-commit/sayantangope/DevMatchs?style=default&logo=git&logoColor=white&color=6366f1" alt="last-commit">
    <img src="https://img.shields.io/github/languages/top/sayantangope/DevMatchs?style=default&color=6366f1" alt="repo-top-language">
    <img src="https://img.shields.io/badge/submodules-2-6366f1?style=default" alt="submodules">
  </p>

  <p align="center">
    🌐 <a href="https://github.com/sayantangope/DevMatchs-web" target="_blank">Frontend Repo</a> &nbsp;|&nbsp;
    ⚙️ <a href="https://github.com/sayantangope/DevMatchs-server" target="_blank">Backend Repo</a>
  </p>
</div>

<br>

<details>
<summary>Table of Contents</summary>

- [📍 Overview](#-overview)
- [👾 Features](#-features)
- [🛠️ Languages & Technologies](#️-languages--technologies)
- [📁 Project Structure](#-project-structure)
- [🚀 Getting Started](#-getting-started)
  - [☑️ Prerequisites](#-prerequisites)
  - [⚙️ Installation](#-installation)
  - [🤖 Usage](#-usage)
- [🔄 Working with Submodules](#-working-with-submodules)
- [📌 Project Roadmap](#-project-roadmap)
- [🔰 Contributing](#-contributing)
- [🎗 License](#-license)
- [👨‍💻 Author](#-author)

</details>

<hr>

## 📍 Overview

**DevMatchs** is the parent repository for the DevMatchs full-stack platform. It does not contain source code directly — instead, it links the **frontend** and **backend** as independent Git submodules, each with their own version control lifecycle.

This repository serves as a single entry point to:
- Clone and set up the entire project in one command
- Keep frontend and backend versions in sync
- Simplify local development across both services

| Submodule | Repository | Description |
|---|---|---|
| `frontend/` | [DevMatchs-web](https://github.com/sayantangope/DevMatchs-web) | React-based web application |
| `backend/` | [DevMatchs-server](https://github.com/sayantangope/DevMatchs-server) | Node.js / Express REST API |

---

## 👾 Features

### 🤝 Developer Matching
- **Swipe-style Connect** — Browse developer profiles and send connection requests, just like a dating app but for building teams and collaborations
- **Smart Matching** — Get matched with developers based on tech stack, interests, and project goals
- **Explore Feed** — Discover developers nearby or globally who are open to collaborating

### 📨 Connection Requests
- **Send Requests** — Reach out to any developer with a connection request
- **Review Requests** — Accept or decline incoming requests from your dashboard
- **Pending Queue** — Track all sent and received requests in one place

### 💬 One-to-One Chat
- **Real-time Messaging** — Instant chat powered by **Socket.io** once a connection is accepted
- **Private Conversations** — Secure, direct messaging between matched developers only
- **Live Status** — See when your connection is online or was last active

### 👤 Profile Management
- **Rich Developer Profiles** — Showcase your skills, tech stack, GitHub, portfolio, and bio
- **Update Anytime** — Edit your profile details, avatar, and availability status
- **Role & Expertise Tags** — Label yourself as Frontend, Backend, Full Stack, ML Engineer, etc.

### 🔐 Authentication & Access
- **Secure Auth** — Protected routes with role-based access control
- **Profile Completion Flow** — Guided onboarding for new users before accessing the platform
- **Persistent Sessions** — Stay logged in across visits

---

## 🛠️ Languages & Technologies

### 🌐 Frontend — [DevMatchs-web](https://github.com/sayantangope/DevMatchs-web)

![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white)
![TailwindCSS](https://img.shields.io/badge/TailwindCSS-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white)
![DaisyUI](https://img.shields.io/badge/DaisyUI-5A0EF8?style=for-the-badge&logo=daisyui&logoColor=white)
![Socket.io](https://img.shields.io/badge/Socket.io-010101?style=for-the-badge&logo=socketdotio&logoColor=white)

### ⚙️ Backend — [DevMatchs-server](https://github.com/sayantangope/DevMatchs-server)

![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)
![Express](https://img.shields.io/badge/Express.js-000000?style=for-the-badge&logo=express&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Socket.io](https://img.shields.io/badge/Socket.io-010101?style=for-the-badge&logo=socketdotio&logoColor=white)

---

## 📁 Project Structure

```
DevMatchs/
├── frontend/          →  DevMatchs-web  (React app)
├── backend/           →  DevMatchs-server (Node/Express API)
└── README.md
```

> **Note:** Each subdirectory is a Git submodule pointing to a separate repository. Changes to frontend or backend must be committed inside their respective repos first, then updated here.

---

## 🚀 Getting Started

### ☑️ Prerequisites

Ensure your environment meets the following requirements before cloning:

- **Git**: v2.x or higher (with submodule support)
- **Node.js**: v16.x or higher
- **npm**: v8.x or higher

### ⚙️ Installation

#### 1. Clone with All Submodules

```bash
git clone --recurse-submodules https://github.com/sayantangope/DevMatchs.git
cd DevMatchs
```

If you already cloned without submodules, initialize them manually:

```bash
git submodule update --init --recursive
```

#### 2. Backend Setup

```bash
cd backend
npm install
```

Create a `.env` file in the `backend/` directory with the required environment variables. Refer to the [DevMatchs-server README](https://github.com/sayantangope/DevMatchs-server) for the full list.

#### 3. Frontend Setup

```bash
cd ../frontend
npm install
```

Create a `.env` file in the `frontend/` directory. Refer to the [DevMatchs-web README](https://github.com/sayantangope/DevMatchs-web) for the full list.

---

### 🤖 Usage

#### Run Backend

```bash
cd backend
npm run dev
# API server starts at http://localhost:8000
```

#### Run Frontend

```bash
cd frontend
npm run dev
# App runs at http://localhost:5173 (or as configured)
```

> Run both terminals simultaneously for full-stack local development.

---

## 🔄 Working with Submodules

### Pull Latest Changes from Both Submodules

```bash
git submodule update --remote
```

### After Updating Submodules, Sync in Parent Repo

```bash
git add .
git commit -m "chore: update submodules to latest"
git push
```

### Make Changes to a Submodule

Navigate into the submodule, make changes, then commit and push **inside that repo**:

```bash
cd frontend
# make your changes
git add .
git commit -m "feat: your change"
git push origin main
```

Then update the parent repo to track the new commit:

```bash
cd ..
git add frontend
git commit -m "chore: bump frontend submodule"
git push
```

---

## 📌 Project Roadmap

- [x] **Parent repo with Git submodule setup**
- [x] **Frontend submodule linked** (DevMatchs-web)
- [x] **Backend submodule linked** (DevMatchs-server)
- [ ] One-command startup script (`npm run dev` from root)
- [ ] Docker Compose for full-stack containerized deployment
- [ ] CI/CD pipeline with GitHub Actions
- [ ] Monorepo migration (optional alternative to submodules)

---

## 🔰 Contributing

Contributions are welcome! Since this is a submodule-based repository, please follow the correct workflow:

1. **For frontend changes** → contribute to [DevMatchs-web](https://github.com/sayantangope/DevMatchs-web)
2. **For backend changes** → contribute to [DevMatchs-server](https://github.com/sayantangope/DevMatchs-server)
3. **For project-wide structure** → open an issue or PR here

<details>
<summary>General Contribution Steps</summary>

1. Fork the relevant submodule repository.
2. Clone your fork locally.
3. Create a feature branch:
   ```bash
   git checkout -b feature/your-feature-name
   ```
4. Make and test your changes.
5. Commit with a clear message:
   ```bash
   git commit -m "feat: describe your change"
   ```
6. Push and open a Pull Request against the original repo.

</details>

---

## 🎗 License

This project is licensed under the **MIT License**.

You are free to use, modify, and distribute this project with attribution.

---

## 👨‍💻 Author

**Sayantan Gope**

- GitHub: [@sayantangope](https://github.com/sayantangope)

<div align="center">
  <br>
  <p><strong>Made with ❤️ by Sayantan Gope</strong></p>
  <p><em>Connect. Collaborate. Build. ⚡</em></p>
</div>
