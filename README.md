from pathlib import Path
import shutil

base = Path("/mnt/data/mern-book-inventory-readme")
assets = base / "screenshots"
assets.mkdir(parents=True, exist_ok=True)

# Copy the uploaded screenshots into the README package.
srcs = [
    Path("/mnt/data/829ef109-0a19-453d-85e7-7ba820248b1e.png"),
    Path("/mnt/data/a1f93559-a88d-423c-979e-cb7284c41c7a.png"),
    Path("/mnt/data/770eaa0d-94dc-4721-a5a9-4093155b5dde.png"),
    Path("/mnt/data/b7676fbd-f833-4f06-b84b-ae66984a0be2.png"),
    Path("/mnt/data/12feb437-208c-42ec-a06e-d8e5f2227c1c.png"),
    Path("/mnt/data/c9525915-0e13-4a1d-8049-f844601505d6.png"),
]

for i, src in enumerate(srcs, 1):
    shutil.copy2(src, assets / f"book-store-{i}.png")

readme = """# 📚 Book Inventory & Book Store — MERN Stack

A modern **Book Inventory and Online Book Store** web application built with the **MERN Stack (MongoDB, Express.js, React.js, Node.js)**.

The application provides a clean interface for discovering books, searching for books, viewing best sellers, exploring other books, and presenting a simple book-selling experience.

## ✨ Features

- 🏠 Modern responsive home page
- 🔎 Book search interface
- 📚 Best Seller Books section
- 🛒 Add-to-cart interface
- 📖 Other Books section
- 💰 Buy and sell books
- 📊 Book statistics / platform information
- ⭐ Customer reviews section
- 📱 Responsive navigation
- 🎨 Clean and user-friendly UI
- 🔗 MERN-based frontend and backend architecture

## 🛠️ Tech Stack

### Frontend
- React.js
- HTML5
- CSS3
- JavaScript
- React Router

### Backend
- Node.js
- Express.js

### Database
- MongoDB
- Mongoose

### Development Tools
- VS Code
- Git & GitHub
- npm

## 📂 Project Structure

```text
book-inventory/
│
├── client/                 # React frontend
│   ├── public/
│   └── src/
│       ├── components/
│       ├── pages/
│       ├── assets/
│       ├── App.jsx
│       └── main.jsx
│
├── server/                 # Node.js + Express backend
│   ├── controllers/
│   ├── models/
│   ├── routes/
│   ├── middleware/
│   └── server.js
│
├── screenshots/
├── .gitignore
└── README.md
