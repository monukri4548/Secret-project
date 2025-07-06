# 🔐 Auth Secrets App

This is a full-stack **authentication app** built with **Node.js**, **Express**, **PostgreSQL**, and **Passport.js**. Users can register, log in (with email/password or Google OAuth), and submit anonymous secrets securely.

---

## 🚀 Features

- 🛡️ Local authentication using **Passport + bcrypt**
- 🔐 **Google OAuth 2.0** login integration
- 💾 Secrets stored securely in a PostgreSQL database
- 🌐 Session management with **express-session**
- 📄 Views rendered using **EJS templates**
- 🧠 Passwords hashed with **bcrypt**
- ✅ Form validation and error handling

---

## 🧩 Tech Stack

- **Frontend**: EJS (Templating)
- **Backend**: Node.js, Express
- **Authentication**: Passport.js (Local + Google OAuth 2.0)
- **Database**: PostgreSQL
- **Middleware**: express-session, body-parser, dotenv
- **Security**: bcrypt hashing

---

## 📁 Project Structure

/auth-secrets-app
│
├── views/ # EJS templates
│ ├── home.ejs
│ ├── login.ejs
│ ├── register.ejs
│ ├── secrets.ejs
│ └── submit.ejs
│
├── public/ # Static files (CSS, images)
│
├── .env # Environment variables
├── index.js # Main application file
├── package.json
└── README.md

---

## ⚙️ Environment Variables (`.env`)

Create a `.env` file in the root with the following variables:

```env
SESSION_SECRET=yourSessionSecret
PG_USER=yourPostgresUsername
PG_HOST=localhost
PG_DATABASE=yourDatabaseName
PG_PASSWORD=yourPostgresPassword
PG_PORT=5432

GOOGLE_CLIENT_ID=yourGoogleClientID
GOOGLE_CLIENT_SECRET=yourGoogleClientSecret


🧠 Database Setup (PostgreSQL)
Run the following SQL to create the required table:
CREATE TABLE users (
  id SERIAL PRIMARY KEY,
  email VARCHAR(255) UNIQUE NOT NULL,
  password VARCHAR(255),
  secret TEXT
);

📦 Installation
git clone https://github.com/your-username/auth-secrets-app.git
cd auth-secrets-app
npm install

🧪 Run the App
node index.js
Visit: http://localhost:3000
