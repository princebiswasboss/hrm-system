# HRM (Human Resource Management System)

A modern Human Resource Management System (HRM) built with Laravel to simplify and automate employee management, attendance tracking, leave management, payroll visibility, and HR administration.

---

# Features

* Employee Management
* Department Management
* Attendance Management
* Leave Management
* Payroll Management
* Role-Based Access Control
* Dashboard & Reports
* User Authentication
* Profile Management
* Notifications
* Image Upload Support
* Secure Laravel Backend

---

# Technology Stack

* Laravel
* PHP
* MySQL
* Bootstrap
* HTML5
* CSS3
* JavaScript

---

# Server Requirements

Before installation, ensure your server meets the following requirements.

## Web Server

* Apache
* Nginx
* Any Laravel-compatible web server

## PHP

* PHP 8.x (or the version required by your Laravel release)

Required PHP Extensions:

* BCMath
* Ctype
* cURL
* FileInfo
* JSON
* Mbstring
* OpenSSL
* PDO
* Tokenizer
* XML

## Database

* MySQL 5.7+
* MariaDB 10+

## Other Requirements

* Apache mod_rewrite enabled
* Internet connection (required for email services)

---

# Installation

## 1. Upload Files

Upload the `main-file.zip` file to your server.

Extract it inside the `public_html` directory.

Example:

```text
public_html/
│
├── app/
├── bootstrap/
├── config/
├── database/
├── public/
├── resources/
├── routes/
├── storage/
├── vendor/
├── artisan
└── .env
```

---

## 2. Create Database

Create a MySQL database from your hosting control panel.

Example:

Database Name

```
hrm_database
```

Database User

```
hrm_user
```

Database Password

```
your_password
```

---

## 3. Import Database

Open **phpMyAdmin**.

Select your database.

Click **Import**.

Upload:

```
database.sql
```

Wait until the import is completed successfully.

---

## 4. Configure Environment

Open the `.env` file.

Update the following values.

```env
APP_NAME=HRM
APP_ENV=production
APP_KEY=base64:22/aK6fNUbF9u0kTeh7i+63Z3z6NqUKusjjdRNVaMaA=
APP_DEBUG=false

DB_HOST=localhost
DB_DATABASE=enter_your_db
DB_USERNAME=enter_your_db_user
DB_PASSWORD="enter_db_password"

APP_URL=https://yourdomain.com
```

Replace:

* `enter_your_db`
* `enter_your_db_user`
* `enter_db_password`
* `https://yourdomain.com`

with your actual hosting details.

---

## 5. Folder Permissions

Make the following folders writable.

```
storage/
bootstrap/cache/
```

Recommended permissions:

Directories

```
755
```

Files

```
644
```

---

## 6. Visit Your Website

Open your browser.

```
https://yourdomain.com
```

Your HRM application is now ready to use.

---

# Default Login

Use the administrator credentials provided with your purchase or configured during installation.

---

# Project Structure

```
app/
bootstrap/
config/
database/
public/
resources/
routes/
storage/
vendor/
artisan
.env
composer.json
```

---

# Troubleshooting

## HTTP 500 Error

* Verify your `.env` file.
* Check PHP version compatibility.
* Confirm file permissions.
* Ensure all required PHP extensions are enabled.

---

## Database Connection Failed

Verify:

* Database Host
* Database Name
* Database Username
* Database Password

---

## Images Not Uploading

Enable the PHP **FileInfo** extension.

---

## Email Not Working

Configure SMTP settings in the `.env` file.

Ensure your server has internet access.

---

## 404 Error

Enable Apache `mod_rewrite`.

Ensure the `.htaccess` file exists in the project root/public directory as required by your deployment.

---

# Security Recommendations

* Set `APP_DEBUG=false` in production.
* Keep your `.env` file private.
* Use HTTPS.
* Create regular database backups.
* Keep PHP and server software up to date.

---

# License

This software is licensed. Redistribution, resale, modification, or sharing without permission is prohibited.

---

# Support

If you encounter any installation or configuration issues, please provide the following information when requesting support:

* Domain Name
* PHP Version
* MySQL Version
* Error Screenshot
* Error Message
* Server/Hosting Provider

This information will help us resolve your issue more quickly.

---

## Thank You

Thank you for choosing the **HRM (Human Resource Management System)**. We hope it helps streamline your organization's HR operations efficiently.
