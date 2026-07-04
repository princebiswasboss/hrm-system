# HRM Website Installation Guide (Laravel)

## Project Download

Download the complete project files from the link below:

**Project Files:**
https://drive.google.com/drive/folders/1ptPh9TTzDiGH3zU51X1_B_XRA2z-067T?usp=sharing

---

# Human Resource Management System (HRM)

This Human Resource Management System (HRM) is developed using the **Laravel Framework**. The application provides employee management, attendance, leave management, payroll, department management, user authentication, role-based access control, and various HR administration features.

Follow the steps below to install the application on your web hosting server.

---

# System Requirements

Before installing the application, ensure that your hosting environment meets the following requirements.

## Web Server

* Apache 2.4+ (Recommended)
* Nginx (Supported)
* Apache **mod_rewrite** enabled

## PHP Requirements

* PHP **8.x**
* BCMath Extension
* Ctype Extension
* cURL Extension
* DOM Extension
* FileInfo Extension
* JSON Extension
* Mbstring Extension
* OpenSSL Extension
* PDO Extension
* Tokenizer Extension
* XML Extension
* ZIP Extension

## Database

* MySQL 5.7+ or MySQL 8.x
* MariaDB 10.3+

## Other Requirements

* Composer (Only required for local development)
* Active Internet Connection (Required for Email Services and External Integrations)

---

# Installation Guide

## Step 1: Download the Project

Download the project from the Google Drive link provided above.

The downloaded package contains:

* Laravel Project Files
* SQL Database Backup

---

## Step 2: Upload Project Files

1. Log in to your hosting control panel (cPanel, Plesk, DirectAdmin, etc.).
2. Open **File Manager**.
3. Navigate to the **public_html** directory.
4. Upload **main-file.zip**.
5. Extract the ZIP file inside **public_html**.

After extraction, the Laravel project files should be available inside your hosting directory.

---

## Step 3: Create a Database

1. Open **MySQL Databases**.
2. Create a new database.
3. Create a database user.
4. Assign the user to the database.
5. Grant **All Privileges**.

---

## Step 4: Import the Database

1. Open **phpMyAdmin**.
2. Select the database you created.
3. Click **Import**.
4. Select the **database.sql** file included in the project package.
5. Click **Import**.

Wait until the import process completes successfully.

---

## Step 5: Configure the Environment File

Open the **.env** file located in the project root directory.

Update the following values:

```env
APP_NAME=HRM
APP_ENV=production
APP_KEY=base64:22/aK6fNUbF9u0kTeh7i+63Z3z6NqUKusjjdRNVaMaA=
APP_DEBUG=false

APP_URL=https://yourdomain.com

DB_CONNECTION=mysql
DB_HOST=localhost
DB_PORT=3306
DB_DATABASE=your_database_name
DB_USERNAME=your_database_user
DB_PASSWORD=your_database_password
```

Replace the following values with your hosting information:

* `your_database_name`
* `your_database_user`
* `your_database_password`
* `https://yourdomain.com`

---

## Step 6: Configure Storage Permissions

Laravel requires write permission for the following directories:

```
storage/
bootstrap/cache/
```

Recommended Permissions

| Item        | Permission |
| ----------- | ---------- |
| Directories | 755        |
| Files       | 644        |

---

## Step 7: Laravel Optimization (Optional)

If you have SSH access, execute the following commands:

```bash
php artisan config:cache
php artisan route:cache
php artisan view:cache
php artisan optimize
```

These commands improve application performance.

---

## Step 8: Visit Your Website

Open your browser and visit:

```
https://yourdomain.com
```

If everything has been configured correctly, the HRM application will load successfully.

---

# Default Login

Use the administrator credentials provided by the software provider after installation.

If no credentials are provided, please contact the developer.

---

# Troubleshooting

## HTTP 500 Internal Server Error

Possible causes:

* Incorrect `.env` configuration
* Wrong database credentials
* Missing PHP extensions
* Storage permission issues
* Corrupted upload

Solution:

* Verify the `.env` file.
* Confirm PHP version compatibility.
* Ensure required PHP extensions are enabled.
* Set proper permissions on `storage` and `bootstrap/cache`.

---

## Database Connection Failed

Verify:

* Database Name
* Database Username
* Database Password
* Database Host (`localhost`)
* Database Port (`3306`)

---

## 404 Not Found

Ensure that:

* Apache `mod_rewrite` is enabled.
* `.htaccess` exists.
* The domain points to the correct Laravel public directory.

---

## Images Cannot Upload

Enable the following PHP extension:

* FileInfo

Also ensure the `storage` directory is writable.

---

## Email Not Working

Configure SMTP settings inside the `.env` file.

Example:

```env
MAIL_MAILER=smtp
MAIL_HOST=your_mail_host
MAIL_PORT=587
MAIL_USERNAME=your_email
MAIL_PASSWORD=your_password
MAIL_ENCRYPTION=tls
MAIL_FROM_ADDRESS=your_email@example.com
MAIL_FROM_NAME=HRM
```

---

## Permission Denied

If the application cannot create cache or upload files, ensure:

```
storage/
bootstrap/cache/
```

have write permission.

---

# Project Structure

```
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
├── .env
├── artisan
└── composer.json
```

---

# Support

If you encounter any issues during installation, please provide the following information when contacting support:

* Domain Name
* PHP Version
* Laravel Version
* MySQL Version
* Error Message
* Screenshot of the Error
* Hosting Provider

Providing these details will help us diagnose and resolve your issue more efficiently.

---

# Development Team

**Project:** Human Resource Management System (HRM)

**Framework:** Laravel

**Developed By**

* Sayan
* Anupama
* Tiyasa
* Prince

---

© Human Resource Management System (HRM)

Built with the Laravel Framework.
