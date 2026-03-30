# 📘 Mobile App – “How to Help Teenagers Take a Break from Their Phones, in order to read”

This is a lightweight, and elegant personal portfolio website built with **HTML, CSS, JavaScript, PHP, and MySQL**, from scratch.



It also serves as an educational demo project for running a dynamic website locally and deploying a static version to GitHub Pages.


## 🧩 File & Folder Structure
```
project_root/
│
├── index.php # Homepage
├── contact.php # Contact form (sends emails)
├── login.php # Login and signup form
├── logout.php # Logout form 
├── donate.php # Donation page (PayPal / Bitcoin)
│
├── includes/
│ ├── header.php # Common header section (navbar, logo)
│ ├── footer.php # Common footer section
│ ├── config.php # Database connection settings
│ ├── counter.php # Visitor counter logic
│ ├── register.php # User registration handling
│ ├── login_process.php # Login verification
│
├── assets/
│ ├── style.css # Main CSS styling
│ ├── script.js # JS for burger menu, UI effects
│
├── images/
│ ├── favicon.png # Site icon (little girl with bangs)
│ └── ... # Other images
│
├── data/
│ └── database.sql # SQL script for creating tables
│
└── README.md # Documentation (this file)
```

## 🛠️ How to Run Locally (Full PHP + MySQL Version)

### 1️⃣ Install XAMPP
- Download & install [XAMPP](https://www.apachefriends.org/).
- Start **Apache** and **MySQL** from the XAMPP Control Panel.

### 2️⃣ Move project files
Copy the whole project folder into:
C:\xampp\htdocs\portfolio


### 3️⃣ Create the MySQL Database
- Open your browser → go to `http://localhost/phpmyadmin`
- Create a new database called:
portfolio_db

- Import the SQL file from:
/data/database.sql

(This creates the tables for users, login, and visitor counter.)

### 4️⃣ Configure Database Connection
Open `includes/config.php` and make sure these lines match your setup:

<?php
$host = "localhost";
$user = "root";
$pass = "";
$dbname = "portfolio_db";

$conn = new mysqli($host, $user, $pass, $dbname);
if ($conn->connect_error) {
  die("Connection failed: " . $conn->connect_error);
}
?>

### 5️⃣ Run the Website
In your browser, open:
5️⃣ Run the Website

In your browser, open:
http://localhost/portfolio/
, or just open:
www.thanasis-codes.eu

✅ You should see your homepage, navigation bar, contact form, login, and donate buttons working.

📊 Database Tables (Basic Example):
CREATE TABLE users (
  id INT AUTO_INCREMENT PRIMARY KEY,
  username VARCHAR(100) NOT NULL,
  password VARCHAR(255) NOT NULL
);

CREATE TABLE visits (
  id INT AUTO_INCREMENT PRIMARY KEY,
  ip_address VARCHAR(50),
  visit_time TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);


🚀 Deployment to GitHub Pages (Static Version)

GitHub Pages does not support PHP/MySQL,
so you can only upload the static version (HTML/CSS/JS) for demonstration.

Steps:

1. Upload all .html, .css, .js, and /images/ files to your repo.

2. Go to Settings → Pages → Deploy from branch → main /(root)

3. Your static portfolio will appear at: https://<username>.github.io/portfolio/

👨‍💻 Author

Thanasis Koufos

Web Developer

📧 thanasis.koufos1@gmail.com

🌐 https://github.com/ThanasisSoftwareDeveloper
