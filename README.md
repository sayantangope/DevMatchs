<div align="center">
  <h1>⚡ DevMatchs</h1>

  <p align="center">
    <em>Tinder for Developers — Discover. Connect. Build Together.</em>
  </p>

  <p align="center">
    <img src="https://img.shields.io/github/last-commit/sayantangope/DevMatchs?style=default&logo=git&logoColor=white&color=6366f1" alt="last-commit">
    <img src="https://img.shields.io/github/languages/top/sayantangope/DevMatchs?style=default&color=6366f1&logo=javascript&logoColor=white" alt="repo-top-language">
    <img src="https://img.shields.io/badge/submodules-2-6366f1?style=default" alt="submodules">
    <img src="https://img.shields.io/badge/deployed-AWS-FF9900?style=default&logo=amazonaws&logoColor=white" alt="deployed on aws">
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
- [🏗️ Architecture](#️-architecture)
- [📁 Project Structure](#-project-structure)
- [🚀 Getting Started](#-getting-started)
- [🔄 Working with Submodules](#-working-with-submodules)
- [📌 Project Roadmap](#-project-roadmap)
- [🔰 Contributing](#-contributing)
- [🎗 License](#-license)
- [👨‍💻 Author](#-author)

</details>

<hr>

## 📍 Overview

**DevMatchs** is a **Tinder-style matchmaking platform for developers** — swipe through profiles, send connection requests, and chat one-on-one with developers who match your vibe and stack. Unlock premium features via **Razorpay** payments, get notified via **AWS SES** emails, and enjoy a real-time experience powered by **Socket.IO**.

This is the **parent repository** that links the frontend and backend as independent Git submodules. It serves as a single entry point to clone and understand the full project — setup instructions live in each submodule's own README.

| Submodule | Repository | Description |
|---|---|---|
| `frontend/` | [DevMatchs-web](https://github.com/sayantangope/DevMatchs-web) | React 19 SPA — feed, chat, profile, premium |
| `backend/` | [DevMatchs-server](https://github.com/sayantangope/DevMatchs-server) | Express v5 REST API + Socket.IO server |

---

## 👾 Features

### 🃏 Developer Feed & Matching
- Swipe-style developer feed — browse profiles and send **Interested** or **Ignored** requests
- Each card shows name, photo, age, gender, skills, and bio
- Feed automatically excludes already-connected or previously-interacted developers

### 📨 Connection Requests
- Send connection requests with `interested` or `ignored` status to any developer in the feed
- Review incoming requests — **accept** or **reject** with one click from your dashboard
- Email notification fired via **AWS SES** on every new connection request received
- Dedicated pending requests view to manage your queue

### 💬 Real-time One-to-One Chat
- Private chat rooms scoped per accepted connection pair
- Messages delivered instantly via **Socket.IO** — no page refresh needed
- Full chat history persisted in MongoDB and loaded when you open a conversation
- Only mutually accepted connections can open a chat — no unsolicited messages

### 👤 Profile Management
- Rich developer profiles with name, age, gender, about, skills, and photo
- Edit profile details anytime from a dedicated edit page
- Skills rendered as tags for quick scanning by other developers

### 💳 Premium Membership (Razorpay)
- **Silver** and **Gold** membership tiers
- Secure order creation and checkout flow via **Razorpay**
- Backend webhook verifies payment and upgrades `isPremium` + `membershipType` on the user
- Premium unlocks additional platform features and visibility boosts

### 🔐 Authentication & Sessions
- JWT-based auth stored in HTTP-only cookies
- Passwords hashed with **bcrypt**
- Protected routes on both frontend and backend
- Auto-logout on token expiry

### 📧 Email Notifications (AWS SES)
- Transactional emails sent via **AWS SES** (region: `ap-south-1`)
- Triggered automatically on connection request events
- Configured using `@aws-sdk/client-ses`

### ⏰ Scheduled Jobs
- Background **cron jobs** via `node-cron` for periodic cleanup and maintenance tasks

---

## 🛠️ Languages & Technologies

### 🌐 Frontend — [DevMatchs-web](https://github.com/sayantangope/DevMatchs-web)

![React](https://img.shields.io/badge/React_19-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white)
![Redux Toolkit](https://img.shields.io/badge/Redux_Toolkit-764ABC?style=for-the-badge&logo=redux&logoColor=white)
![React Router](https://img.shields.io/badge/React_Router_v7-CA4245?style=for-the-badge&logo=reactrouter&logoColor=white)
![TailwindCSS](https://img.shields.io/badge/TailwindCSS-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white)
![DaisyUI](https://img.shields.io/badge/DaisyUI-5A0EF8?style=for-the-badge&logo=daisyui&logoColor=white)
![Axios](https://img.shields.io/badge/Axios-5A29E4?style=for-the-badge&logo=axios&logoColor=white)
![Socket.io](https://img.shields.io/badge/Socket.io-010101?style=for-the-badge&logo=socketdotio&logoColor=white)

### ⚙️ Backend — [DevMatchs-server](https://github.com/sayantangope/DevMatchs-server)

![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)
![Express v5](https://img.shields.io/badge/Express_v5-000000?style=for-the-badge&logo=express&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white)
![Mongoose](https://img.shields.io/badge/Mongoose_v9-880000?style=for-the-badge&logoColor=white)
![Socket.io](https://img.shields.io/badge/Socket.io-010101?style=for-the-badge&logo=socketdotio&logoColor=white)
![JWT](https://img.shields.io/badge/JWT-000000?style=for-the-badge&logo=jsonwebtokens&logoColor=white)
![Razorpay](https://img.shields.io/badge/Razorpay-02042B?style=for-the-badge&logo=razorpay&logoColor=3395FF)
![AWS SES](https://img.shields.io/badge/AWS_SES-FF9900?style=for-the-badge&logo=amazonaws&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)

### ☁️ Infrastructure & Deployment

![AWS](https://img.shields.io/badge/Deployed_on_AWS-FF9900?style=for-the-badge&logo=amazonaws&logoColor=white)
![MongoDB Atlas](https://img.shields.io/badge/MongoDB_Atlas-47A248?style=for-the-badge&logo=mongodb&logoColor=white)

---

## 🏗️ Architecture

```
                  ┌──────────────────────────────┐
                  │         React 19 SPA          │
                  │  Vite · Redux · DaisyUI · RRv7│
                  └──────────────┬───────────────┘
                                 │  REST API (Axios)
                                 │  WebSocket (Socket.IO)
                  ┌──────────────▼───────────────┐
                  │       Express v5 Server        │
                  │   JWT Auth · bcrypt · cron     │
                  └──────┬──────────┬─────────────┘
                         │          │
            ┌────────────▼──┐  ┌────▼──────────────┐
            │  MongoDB Atlas │  │     AWS SES        │
            │  (Mongoose v9) │  │  Email Notifs      │
            └───────────────┘  └───────────────────┘
                         │
            ┌────────────▼──────────────┐
            │     Razorpay Gateway       │
            │  Orders · Webhook · Premium│
            └───────────────────────────┘
```

---

## 📁 Project Structure

```
DevMatchs/                          ← Parent repo (this)
├── frontend/                       → DevMatchs-web (React SPA)
│   └── src/
│       ├── components/             # Feed, Chat, Profile, Requests, Premium...
│       ├── utils/
│       │   ├── socket.js           # Socket.IO singleton client
│       │   └── slices/             # Redux — userSlice, feedSlice, connectionSlice, requestSlice
│       └── constants/constants.js  # BASE_URL config
│
├── backend/                        → DevMatchs-server (Express API)
│   └── src/
│       ├── models/                 # User, ConnectionRequest, Chat, Payment
│       ├── routes/                 # auth, profile, request, user, chat, payment
│       └── utils/                  # socket.js, sendEmail, razorpay, cronjob, validate
│
└── README.md
```

> Each subdirectory is an independent Git submodule. For full source structure and setup steps, see each repo's own README.

---

## 🚀 Getting Started

Clone this repo with all submodules in one command:

```bash
git clone --recurse-submodules https://github.com/sayantangope/DevMatchs.git
```

For environment variables, full setup, and run instructions refer to each submodule:

- ⚙️ **Backend setup** → [DevMatchs-server README](https://github.com/sayantangope/DevMatchs-server#readme)
- 🌐 **Frontend setup** → [DevMatchs-web README](https://github.com/sayantangope/DevMatchs-web#readme)

---

## 🔄 Working with Submodules

**Pull latest from both submodules:**
```bash
git submodule update --remote
```

**Commit submodule pointer updates in parent:**
```bash
git add .
git commit -m "chore: update submodules to latest"
git push
```

**Push changes made inside a submodule then sync parent:**
```bash
cd frontend        # or backend
git add . && git commit -m "feat: your change"
git push origin main
cd ..
git add frontend
git commit -m "chore: bump frontend submodule"
git push
```

---

## 📌 Project Roadmap

### ✅ Completed
- [x] JWT authentication with bcrypt
- [x] Developer swipe feed with Interested / Ignored requests
- [x] Accept / reject incoming connection requests
- [x] Real-time one-to-one chat via Socket.IO
- [x] Profile view and edit
- [x] Razorpay premium membership (Silver & Gold)
- [x] AWS SES email notifications on connection events
- [x] Scheduled cron jobs for maintenance
- [x] Deployed on AWS

### 🔜 Upcoming
- [ ] Profile photo upload via AWS S3
- [ ] Swipe animations on developer cards
- [ ] Push notifications
- [ ] Admin dashboard
- [ ] Docker Compose for one-command local setup
- [ ] CI/CD pipeline with GitHub Actions

---

## 🔰 Contributing

Contributions are welcome! Please direct them to the correct submodule repo:

- **Frontend changes** → [DevMatchs-web](https://github.com/sayantangope/DevMatchs-web)
- **Backend changes** → [DevMatchs-server](https://github.com/sayantangope/DevMatchs-server)
- **Project-wide issues** → open an issue here

<details>
<summary>Contribution Steps</summary>

1. Fork the relevant submodule repository
2. Create a feature branch: `git checkout -b feature/amazing-feature`
3. Commit your changes: `git commit -m 'feat: add amazing feature'`
4. Push and open a Pull Request against the original repo

</details>





---

## 👨‍💻 Author

**Sayantan Gope**
- GitHub: [@sayantangope](https://github.com/sayantangope)

<div align="center">
  <br>
  <p><strong>Made with ❤️ by Sayantan Gope</strong></p>
  <p><em>Check it Out!!. ⚡</em></p>
</div>
