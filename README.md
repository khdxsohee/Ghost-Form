<div align="center">

  <img src="public/images/ghostform.png" alt="Ghost Form Logo" width="100" />

  # Ghost Form

  ### *A privacy-first, open-source form backend for static websites.*

  <br/>

  [![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)](https://nodejs.org/)
  [![Prisma](https://img.shields.io/badge/Prisma-2D3748?style=for-the-badge&logo=prisma&logoColor=white)](https://www.prisma.io/)
  [![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)](https://www.mysql.com/)
  [![License](https://img.shields.io/badge/License-MIT-green.svg?style=for-the-badge)](LICENSE)

  <br/>

  [Live Demo](#) • [Documentation](#) • [Report Bug](https://github.com/khdxsohee/Ghost-Form/issues) • [Request Feature](https://github.com/khdxsohee/Ghost-Form/issues)

</div>

---

## 🌟 About The Project

Frontend developers often struggle to handle form submissions on static websites without relying on paid, third-party services. **Ghost Form** solves this by providing a lightweight, self-hosted backend that seamlessly captures, stores, and manages form submissions. 

Built with a focus on **developer experience** and **data privacy**, it features a premium, spacious UI and a robust Node.js + Prisma backend. No more monthly fees or data sharing with third parties!

---

## ✨ Features

- 🔒 **Privacy-First**: Your data stays on your own server. Zero third-party tracking.
- ⚡ **Lightweight & Fast**: Built with vanilla Node.js, Express, and Prisma ORM.
- 🎨 **Premium UI**: Modern, spacious design with 16dp rounded corners and clean aesthetics.
- 🎛️ **Dynamic Form Creation**: Create unlimited forms instantly via the dashboard UI (no coding required).
- 📊 **Built-in Dashboard**: View, filter, and manage all submissions in a clean, responsive table.
- 📥 **One-Click CSV Export**: Download your form data instantly for offline use.
- ⚡ **Integration Guide**: Built-in code snippets (HTML & JS) with one-click copy for instant website integration.
- 🛡️ **Spam Protection Ready**: Architecture supports easy addition of honeypot fields and rate limiting.

---

## 📸 Screenshots

### 📝 Form Submission Page
<img width="1348" height="636" alt="Form Submission Page" src="https://github.com/user-attachments/assets/3c824867-2be5-43b4-9498-c779aa54ac32" />
*A clean, modern form ready to be embedded in any static website.*

### 📊 Admin Dashboard & Integration Guide
<img width="1349" height="635" alt="Admin Dashboard" src="https://github.com/user-attachments/assets/2801a9af-3f67-4095-8eec-89f78ee6050f" />
*Create forms dynamically, copy endpoints, and view submissions with a single click.*

---

## 🛠️ Tech Stack

- **Backend**: Node.js, Express.js
- **Database**: MySQL
- **ORM**: Prisma
- **Frontend**: Vanilla JavaScript, HTML5, Custom CSS (Tailwind-inspired design system)

---

## 🚀 Getting Started

Follow these simple steps to get Ghost Form running on your local machine.

### 📋 Prerequisites
Make sure you have the following installed:
- **Node.js** (v18 or higher) - [Download here](https://nodejs.org/)
- **MySQL Database** (e.g., XAMPP, MySQL Workbench, or a cloud provider like PlanetScale)

### ⚙️ Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/khdxsohee/Ghost-Form.git
   cd Ghost-Form
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Create the Database**  
   Open your MySQL client (e.g., phpMyAdmin in XAMPP) and run:
   ```sql
   CREATE DATABASE ghost_form;
   ```

4. **Set up Environment Variables**  
   Create a `.env` file in the root directory and add your database connection string.  
   *(Note: If using XAMPP, the default password is empty, so leave it blank after the colon)*
   ```env
   DATABASE_URL="mysql://root:YOUR_PASSWORD@localhost:3306/ghost_form"
   PORT=3000
   ```

5. **Push the Database Schema**
   ```bash
   npx prisma db push
   ```
   *(This will create the `Form` and `Submission` tables in your database).*

6. **Start the Server**
   ```bash
   node src/server.js
   ```
   The server will start on `http://localhost:3000`.

---

## 💡 How to Use (3 Easy Steps)

1. **Go to the Dashboard**: Open `http://localhost:3000/dashboard.html`
2. **Create a Form**: Click "✨ Create New Form", give it a name (e.g., `contact-us`), and click Create.
3. **Integrate**: Click the "⚡ Integration Guide" dropdown, copy the HTML code, and paste it into your website. That's it!

---

## 📡 API Endpoints

| Method | Endpoint | Description |
| :--- | :--- | :--- |
| `GET` | `/api/forms` | Fetch a list of all created forms and their submission counts |
| `POST` | `/api/forms` | Create a new form (Requires `{ "slug": "your-form-name" }` in body) |
| `POST` | `/api/submit/:slug` | Submit data to a specific form endpoint |
| `GET` | `/api/submissions/:slug` | Fetch all submissions for a specific form |

---

## 🔧 Troubleshooting

- **Error: `Cannot find module '.prisma/client'`**  
  → Run `npx prisma generate` and then `npx prisma db push`.
- **Error: `Access denied for user 'root'`**  
  → Check your `.env` file. If using XAMPP, ensure the URL is `mysql://root:@localhost:3306/ghost_form` (notice the empty password).
- **Error: `Unknown database 'ghost_form'`**  
  → You forgot to create the database. Run `CREATE DATABASE ghost_form;` in your MySQL client.

---

## 🗺️ Roadmap

- [x] **Month 1**: Core backend, Prisma MySQL integration, Premium UI Dashboard, Dynamic Form Creation, and CSV Export.
- [ ] **Month 2**: Email notifications (Nodemailer) and advanced spam protection (Honeypot).
- [ ] **Month 3**: Webhooks support (Discord/Zapier) and Docker deployment configuration.

---

## 🤝 Contributing

Contributions are what make the open-source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📄 License

Distributed under the **MIT License**. See `LICENSE` for more information.

---

<div align="center">
  <sub>Built with ❤️ by <a href="https://github.com/khdxsohee">khdxsohee</a></sub>
</div>

---
