# ⏳ Future Message — Digital Time Capsule

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![MERN Stack](https://img.shields.io/badge/Stack-MERN-blue.svg)](https://www.mongodb.com/mern-stack)
[![React](https://img.shields.io/badge/Frontend-React-61DAFB?logo=react)](https://reactjs.org/)
[![Node.js](https://img.shields.io/badge/Backend-Node.js-339933?logo=node.js)](https://nodejs.org/)

> **"A bridge between today's thoughts and tomorrow's moments."**

**Future Message** is a premium digital time capsule platform built on the MERN stack. It enables users to compose heartfelt messages, attach multimedia memories, and seal them in time. These capsules are automatically delivered to any email inbox on a specific future date, ensuring your most important words arrive exactly when they matter most.ab

---

## 🌟 Key Features

- 🔒 **Secure Time-Locking**: Once a capsule is sealed, it remains encrypted and inaccessible until its designated unlock date.
- 📧 **Automated Email Delivery**: Seamlessly integrated with the Brevo API for reliable delivery to real inboxes.
- 🖼️ **Multimedia Attachments**: Support for high-quality photos, videos, and audio recordings via Cloudinary.
- 🔔 **Intelligent Notifications**: Real-time in-app alerts and email notifications for both creators and recipients.
- 🎨 **Premium Glassmorphism UI**: A stunning, modern interface built with Tailwind CSS v4 and Lucide Icons.
- ⏱️ **Minute-Precision Scheduler**: A robust backend cron job ensures delivery with down-to-the-minute accuracy.
- 👤 **JWT-Based Authentication**: Secure user accounts with robust access and refresh token management.

---

## 🛠️ Tech Stack

| Layer | Technology | Purpose |
|---|---|---|
| **Frontend** | React (Vite) | High-performance, reactive UI |
| **Styling** | Tailwind CSS v4 | Modern, utility-first styling |
| **State** | Zustand | Lightweight & fast state management |
| **Backend** | Node.js + Express | Scalable server architecture |
| **Database** | MongoDB + Mongoose | Flexible document-oriented storage |
| **Email** | Brevo REST API | Reliable transactional email delivery |
| **Media** | Cloudinary | Efficient cloud storage for multimedia |
| **Job Scheduling**| node-cron | Automated background task execution |

---

## 🚀 Getting Started

Follow these steps to set up your own instance of the Digital Time Capsule.

### 1. Prerequisites
- **Node.js** (v18 or higher)
- **MongoDB** (Local or Atlas)
- **Git**

### 2. Installation

Clone the repository and install dependencies for both the client and server:

```bash
# Clone the repository
git clone https://github.com/Jishmitha-2004/future-message.git
cd future-message

# Install root dependencies
npm install

# Install Server dependencies
cd server && npm install

# Install Client dependencies
cd ../client && npm install
```

### 3. Environment Configuration

Create a `.env` file in the `server/` directory and populate it with the following:

```env
# Server Configuration
PORT=5000
NODE_ENV=development
FRONTEND_URL=http://localhost:5173

# Database
MONGO_URI=your_mongodb_connection_string

# Authentication Secrets
JWT_ACCESS_SECRET=your_access_secret
JWT_REFRESH_SECRET=your_refresh_secret
JWT_ACCESS_EXPIRE=15m
JWT_REFRESH_EXPIRE=7d

# Email Service (Brevo API)
SMTP_HOST=smtp-relay.brevo.com
SMTP_PORT=587
SMTP_USER=your_email@domain.com
SMTP_PASS=xkeysib-your-api-key
EMAIL_FROM=your_email@domain.com

# Media Storage (Optional)
CLOUDINARY_CLOUD_NAME=your_cloud_name
CLOUDINARY_API_KEY=your_api_key
CLOUDINARY_API_SECRET=your_api_secret
```

### 4. Launch the Application

From the root directory, run:

```bash
npm run dev
```

The application will launch on [http://localhost:5173](http://localhost:5173).

---

## 📖 How It Works

1.  **Drafting**: Create your capsule with text, images, or audio.
2.  **Sealing**: Set your delivery date and seal the capsule. It is now "Time-Locked."
3.  **Monitoring**: The server's background process continuously checks for capsules ready to unlock.
4.  **Delivering**: At the exact moment, the system triggers the Brevo API to send the content to all recipients.

---

## 📂 Project Structure

```text
future-message/
├── client/          # Vite + React Frontend
│   └── src/
│       ├── components/  # Reusable UI elements
│       ├── pages/       # View components
│       └── store/       # Zustand state stores
├── server/          # Node.js + Express Backend
│   ├── models/      # Mongoose schemas
│   ├── routes/      # API endpoints
│   ├── utils/       # Helpers (Email, Auth)
│   └── server.js    # Entry point
└── package.json     # Global scripts
```

---

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request or open an issue for any bugs or feature requests.

---

## 📜 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

**Created by [Jishmitha](https://github.com/Jishmitha-2004)**
