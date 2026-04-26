# 💸 Expense Tracker

A clean, intuitive expense tracking application to help you manage your personal finances, monitor spending habits, and stay on top of your budget.

---

## 📋 Table of Contents

- [Features](#features)
- [Demo](#demo)
- [Tech Stack](#tech-stack)
- [Getting Started](#getting-started)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [API Reference](#api-reference)
- [Contributing](#contributing)
- [License](#license)

---

## ✨ Features

- ➕ **Add / Edit / Delete** expenses and income entries
- 🗂️ **Category Management** — tag expenses (Food, Travel, Bills, etc.)
- 📊 **Dashboard Overview** — visual summary of income vs. expenses
- 📅 **Date Filtering** — view expenses by day, week, month, or custom range
- 💰 **Budget Alerts** — set limits per category and get notified
- 📤 **Export to CSV** — download your transaction history
- 🌙 **Dark / Light Mode** toggle
- 🔒 **Authentication** — secure login with JWT

---

## 🚀 Demo

> 🔗 [Live Demo](https://your-demo-link.com) *(replace with your deployed URL)*

![Expense Tracker Screenshot](./assets/screenshot.png)

---

## 🛠️ Tech Stack

| Layer      | Technology          |
|------------|---------------------|
| Frontend   | React.js / Next.js  |
| Styling    | Tailwind CSS        |
| Backend    | Node.js + Express   |
| Database   | MongoDB / PostgreSQL |
| Auth       | JWT + bcrypt        |
| Charts     | Chart.js / Recharts |
| Deployment | Vercel / Railway    |

> ⚙️ *Adjust the stack above to match your actual implementation.*

---

## 🏁 Getting Started

### Prerequisites

Make sure you have the following installed:

- [Node.js](https://nodejs.org/) `>= 18.x`
- [npm](https://www.npmjs.com/) or [yarn](https://yarnpkg.com/)
- [MongoDB](https://www.mongodb.com/) or your preferred database

---

## 📦 Installation

### 1. Clone the repository

```bash
git clone https://github.com/your-username/expense-tracker.git
cd expense-tracker
```

### 2. Install dependencies

```bash
# Install frontend dependencies
cd client
npm install

# Install backend dependencies
cd ../server
npm install
```

### 3. Configure environment variables

Create a `.env` file in the `server/` directory:

```env
PORT=5000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret_key
NODE_ENV=development
```

Create a `.env.local` file in the `client/` directory:

```env
NEXT_PUBLIC_API_URL=http://localhost:5000/api
```

### 4. Start the development servers

```bash
# Start backend (from /server)
npm run dev

# Start frontend (from /client)
npm run dev
```

Visit `http://localhost:3000` in your browser.

---

## 🧭 Usage

1. **Register / Login** — Create an account or sign in.
2. **Add a Transaction** — Click the `+` button, fill in amount, category, date, and note.
3. **View Dashboard** — See your spending breakdown in charts and summaries.
4. **Filter & Search** — Narrow down transactions by date, category, or keyword.
5. **Set Budgets** — Go to Settings → Budget to define monthly limits per category.
6. **Export Data** — Click Export to download your transactions as a `.csv` file.

---

## 📁 Project Structure

```
expense-tracker/
├── client/                  # Frontend (React / Next.js)
│   ├── components/          # Reusable UI components
│   ├── pages/               # App routes
│   ├── hooks/               # Custom React hooks
│   ├── context/             # Global state (AuthContext, etc.)
│   ├── utils/               # Helper functions
│   └── styles/              # Global styles / Tailwind config
│
├── server/                  # Backend (Node.js / Express)
│   ├── controllers/         # Route logic
│   ├── models/              # Database schemas
│   ├── routes/              # API endpoints
│   ├── middleware/          # Auth, error handling
│   └── config/              # DB connection, env setup
│
├── .gitignore
├── README.md
└── package.json
```

---

## 📡 API Reference

### Auth

| Method | Endpoint             | Description          |
|--------|----------------------|----------------------|
| POST   | `/api/auth/register` | Register a new user  |
| POST   | `/api/auth/login`    | Login & get token    |

### Transactions

| Method | Endpoint                   | Description                  |
|--------|----------------------------|------------------------------|
| GET    | `/api/transactions`        | Get all transactions          |
| POST   | `/api/transactions`        | Create a new transaction      |
| PUT    | `/api/transactions/:id`    | Update a transaction          |
| DELETE | `/api/transactions/:id`    | Delete a transaction          |

### Categories

| Method | Endpoint               | Description             |
|--------|------------------------|-------------------------|
| GET    | `/api/categories`      | Get all categories       |
| POST   | `/api/categories`      | Create a new category    |

> 🔐 All transaction and category routes require a valid Bearer token in the `Authorization` header.

---

## 🤝 Contributing

Contributions are welcome! Here's how to get started:

1. Fork the repository
2. Create a new branch: `git checkout -b feature/your-feature-name`
3. Make your changes and commit: `git commit -m "feat: add your feature"`
4. Push to your branch: `git push origin feature/your-feature-name`
5. Open a Pull Request

Please follow the [Conventional Commits](https://www.conventionalcommits.org/) standard for commit messages.

---

## 📄 License

This project is licensed under the [MIT License](./LICENSE).

---

## 🙌 Acknowledgements

- [Chart.js](https://www.chartjs.org/) — for beautiful charts
- [Tailwind CSS](https://tailwindcss.com/) — for rapid UI development
- [Heroicons](https://heroicons.com/) — for clean SVG icons

---

> Made with ❤️ by [Your Name](https://github.com/your-username)
