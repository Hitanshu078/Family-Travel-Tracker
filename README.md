🌍 Travel Tracker App

A simple web app that allows users to track the countries they have visited. Each user can add visited countries, switch between users, and personalize their view with colors.

🚀 Features

User-specific visited country tracking

Add new users with custom color themes

PostgreSQL integration for persistent data

EJS templating for dynamic UI rendering

💠 Tech Stack

Node.js

Express.js

PostgreSQL

EJS

HTML/CSS

📦 Setup Instructions

Clone the Repository

git clone https://github.com/your-username/travel-tracker.git
cd travel-tracker

Install Dependencies

npm install

Configure Environment Variables
Create a .env file and set the following:

USERNAME=your_pg_username
HOST=localhost
DATABASE=world
PASSWORD=your_pg_password
PORT=5432

Set Up PostgreSQL Tables

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

Run the Server

node index.js

Visit the App
Open your browser at http://localhost:3000

🧪 Sample Data

To test quickly, insert some country data:

INSERT INTO countries (country_code, country_name) VALUES ('IN', 'India'), ('US', 'United States'), ('FR', 'France');

📄 License

MIT

