# HRM System


Download Link For Project file and folder
https://drive.google.com/drive/folders/1ptPh9TTzDiGH3zU51X1_B_XRA2z-067T?usp=sharing


# HRM Website Installation Guide

## System Requirements

Before installing the application, ensure your hosting server meets the following requirements:

### Web Server

* Apache, Nginx, or another compatible web server
* Apache **mod_rewrite** module enabled

### PHP Requirements

* PHP 8.x (as required by your Laravel version)
* PHP cURL Extension enabled
* PHP FileInfo Extension enabled (required for image uploads)

### Database

* MySQL Database Server

### Internet Connection

* Active internet connection (required for email services and other online integrations)

---

# Installation Steps

## Step 1: Upload Project Files

1. Log in to your hosting control panel (such as cPanel).
2. Open **File Manager**.
3. Navigate to the **public_html** directory.
4. Upload the **main-file.zip** file.
5. Extract the ZIP file inside the **public_html** directory.

The folder structure should now contain all Laravel project files.

---

## Step 2: Create a Database

1. Open **MySQL Databases** from your hosting control panel.
2. Create a new database.
3. Create a new database user.
4. Assign the user to the database with **All Privileges**.

---

## Step 3: Import Database

1. Open **phpMyAdmin**.
2. Select the newly created database.
3. Click **Import**.
4. Choose the **database.sql** file.
5. Click **Import**.

Wait until the import process completes successfully.

---

## Step 4: Configure Environment File

Open the **.env** file located in the project root and update the following values:

```env
APP_NAME=HRM
APP_ENV=production
APP_KEY=base64:22/aK6fNUbF9u0kTeh7i+63Z3z6NqUKusjjdRNVaMaA=
APP_DEBUG=false

DB_HOST=localhost
DB_DATABASE=enter_your_db
DB_USERNAME=enter_your_db_user
DB_PASSWORD="enter_db_password"

APP_URL="https://yourdomain.com"
```

Replace:

* **enter_your_db** with your database name.
* **enter_your_db_user** with your database username.
* **enter_db_password** with your database password.
* **https://yourdomain.com** with your website URL.

---

## Step 5: Set File Permissions (if required)

Ensure the following directories are writable by the web server:

```
storage/
bootstrap/cache/
```

Recommended permissions:

* Directories: **755**
* Files: **644**

---

## Step 6: Access Your Website

Open your web browser and visit:

```
https://yourdomain.com
```

The HRM application should now be installed and ready to use.

---

# Troubleshooting

### White Screen or 500 Internal Server Error

* Verify the `.env` file configuration.
* Confirm the database credentials are correct.
* Ensure `storage` and `bootstrap/cache` are writable.

### Database Connection Error

* Check:

  * Database Name
  * Database Username
  * Database Password
  * Database Host (`localhost`)

### Images Cannot Upload

Enable the **PHP FileInfo** extension.

### Email Not Working

* Configure the SMTP settings in the `.env` file.
* Ensure the server has an active internet connection.

### 404 Not Found

* Enable Apache **mod_rewrite**.
* Confirm that `.htaccess` is present in the project directory.

---

# Support

If you experience any installation issues, please contact the software provider with the following information:

* Domain Name
* PHP Version
* Error Message (if any)
* Screenshot of the issue

This will help us resolve your issue more quickly.



<img width="1024" height="1536" alt="poster" src="https://github.com/user-attachments/assets/c083c392-9824-4be9-aee5-a39179692d03" />



by Sayan

by Anupama

by Tiyasa 
by prince
