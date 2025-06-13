📚 Library Management System

This is a web-based **Library Management System** developed in **PHP and MySQL**. It allows admins to manage books and users to sign up, log in, and view issued books. The system includes password recovery, captcha verification, and basic account security features.

---

### 🧩 Features

* 📖 **User Signup/Login**
* 🔐 **Admin Login**
* 📬 **Password Recovery**
* 🔑 **Change Password**
* 📄 **Captcha Verification**
* 📚 **Issued Books Display**
* 🧾 **Check Username Availability**
* 🏠 **Dashboard for Admin**
* 🚪 **Logout Functionality**

---

### 📂 Project Structure

| File                       | Purpose                                  |
| -------------------------- | ---------------------------------------- |
| `signup.php`               | User registration form and backend       |
| `adminlogin.php`           | Admin login interface and validation     |
| `dashboard.php`            | Admin dashboard after login              |
| `user-forgot-password.php` | Password reset for users                 |
| `change-password.php`      | Change password functionality            |
| `logout.php`               | Session logout and redirection           |
| `check_availability.php`   | AJAX call to check username availability |
| `captcha.php`              | Captcha generation script                |
| `issued-books.php`         | Lists books issued to the logged-in user |
| `config.php`               | Database connection settings             |

---

### ⚙️ Requirements

* PHP 7.x or higher
* MySQL 5.x or higher
* Apache/Nginx Web Server
* A browser (Chrome, Firefox, etc.)

---

### 🚀 Setup Instructions

1. **Clone the Repository**

```bash
git clone https://github.com/yourusername/library-management-system.git
cd library-management-system
```

2. **Import the Database**

* Import the provided `.sql` file into your MySQL server using phpMyAdmin or MySQL CLI:

```bash
mysql -u root -p library_db < database.sql
```

3. **Configure Database**

* Open `config.php` and update with your local DB credentials:

```php
$host = 'localhost';
$user = 'root';
$password = '';
$database = 'library_db';
```

4. **Run the Application**

* Place the project folder in your web server's root directory (e.g., `htdocs` for XAMPP).
* Visit `http://localhost/library-management-system/signup.php` to get started.

---

### 🔐 Security Considerations

* Basic form validation and session management is included.
* Captcha is used to prevent automated signups.
* Passwords should ideally be hashed using `password_hash()` instead of plain MD5 (for better security).
* SQL injection protection needs prepared statements (review existing code if not yet implemented).

---

### 📌 To Do

* Add role-based access (Librarian/User)
* Book catalog management
* Book issue/return system with due date handling
* Pagination for book lists
* Email notifications (for due books, etc.)
