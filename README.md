# 🌍 Travel Tracker App

Welcome to the **Travel Tracker App** — a clean and interactive way to track countries visited by different users, complete with personalized color themes.

---

## 🚀 Features

✨ Track countries visited per user  
🎨 Custom color themes per user  
👥 Add and switch between users  
🛢️ PostgreSQL-powered persistence  
📄 EJS-based dynamic UI rendering  

---

## 🛠️ Tech Stack

- **Backend**: Node.js, Express.js  
- **Frontend**: HTML, CSS, EJS  
- **Database**: PostgreSQL  

---

## 📦 Setup Instructions

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/Hitanshu078/Family-Travel-Tracker.git
cd travel-tracker
```

### 2️⃣ Install Dependencies
```bash
npm install
```

### 3️⃣ Environment Configuration
Create a `.env` file:
```env
USERNAME=your_pg_username
HOST=localhost
DATABASE=world
PASSWORD=your_pg_password
PORT=5432
```

### 4️⃣ Set Up the PostgreSQL Tables
Run these SQL queries in your PostgreSQL shell:
```sql
CREATE TABLE users (
  id SERIAL PRIMARY KEY,
  name TEXT,
  color TEXT
);

CREATE TABLE visited_countries (
  id SERIAL PRIMARY KEY,
  country_code TEXT,
  user_id INTEGER REFERENCES users(id)
);

CREATE TABLE countries (
  country_code TEXT PRIMARY KEY,
  country_name TEXT
);
```

### 5️⃣ Launch the App
```bash
node index.js
```

### 6️⃣ Open in Browser
[http://localhost:3000](http://localhost:3000)

---

## 🌐 Sample Data
Add a few countries to get started:
```sql
INSERT INTO countries (country_code, country_name) 
VALUES ('IN', 'India'), ('US', 'United States'), ('FR', 'France');
```

---

## 📄 License

[MIT License](https://opensource.org/licenses/MIT)

---

> Built with ❤️ to help you visualize your global adventures!
