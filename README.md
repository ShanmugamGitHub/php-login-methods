1. Create database: login_methods
2. Import database.sql in phpMyAdmin
3. Update /core/db.php with your MySQL username/password/port

core/db.php
$host = "localhost";
$user = "root";
$pass = "";
$dbname = "login_methods";
$port = 3307; // change to their XAMPP port (usually 3306)

**Start with**
http://localhost/login_methods_project/index.php


**Project Sructure**
login_methods_project/
│
├─ index.php                     → Main menu (choose login method)
│
├─ core/
│   ├─ db.php                    → Database connection
│   ├─ auth.php                  → Register + login functions
│   └─ session.php               → Session helpers
│
├─ methods/
│   ├─ method1_form_login/
│   │    ├─ register.php
│   │    └─ login.php
│   │
│   ├─ method2_token_based/
│   │    ├─ login.php
│   │    ├─ dashboard.php
│   │    ├─ verify.php
│   │    └─ jwt_helper.php
│   │
│   ├─ method3_oauth/
│   │    ├─ config.php
│   │    ├─ login.php
│   │    └─ callback.php
│   │
│   └─ method4_passwordless/
│        ├─ request_link.php
│        ├─ verify_link.php
│        └─ email_template.php
│
├─ phpmailer/                    → PHPMailer library
│
└─ database/
     └─ login_methods.sql        → Exported MySQL database
