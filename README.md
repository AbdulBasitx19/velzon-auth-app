# 🔐 Velzon Auth App - Laravel Manual Authentication

A fully functional Laravel authentication system built from scratch (without Laravel Breeze or Jetstream) integrated with the beautiful **Velzon Admin Theme**. 

This repository demonstrates a complete **Manual Authentication Flow** (Login, Logout, and Route Protection) using Laravel's core features, combined with a professional, production-ready UI.

---

## ✨ Key Features

- ✅ **Manual Authentication**: Custom `LoginController` handling login logic, validation, and `Auth::attempt()`.
- ✅ **Session Management**: Secure session regeneration and invalidation on login/logout.
- ✅ **Route Protection**: Dashboard protected using Laravel's built-in `auth` middleware.
- ✅ **Velzon UI Integration**: Beautiful, responsive login page and dashboard using the Velzon Admin Theme.
- ✅ **Pure MVC Architecture**: Clean separation of Routes, Controllers, and Blade Views.

---

## 📦 IMPORTANT: Download Theme Assets

Due to GitHub's file size limits, the theme's static assets are hosted externally.

🔗 **Google Drive Link:** [Velzon Theme Assets](https://drive.google.com/drive/folders/1m_QJfs4-TQ0vzx1bCQw_AeKkJceOPkSG?usp=sharing)

**Setup Instructions:**
1. Download the `assets` folder from the Drive link.
2. Place it directly inside the `public/` directory.
   - **Correct Path:** `your-project/public/assets/`

---

## 🚀 Installation & Setup

### 1. Clone the Repository
```bash
git clone https://github.com/AbdulBasitx19/velzon-auth-app.git
cd velzon-auth-app
```
### 2.Install Dependencies
```bash
composer install
```
### 3. Setup Environment
```bash
cp .env.example .env
php artisan key:generate
```
### 4. Database Setup
Update your .env file with your database credentials:
DB_CONNECTION=mysql
DB_DATABASE=velzon_auth
DB_USERNAME=root
DB_PASSWORD=

Run migrations to create the users and sessions tables:
```bash
php artisan migrate
```

### 5. Create a Test User (via Tinker)
```bash
php artisan tinker
App\Models\User::create(['name' => 'Test User', 'email' => 'test@example.com', 'password' => bcrypt('password123')])
exit
```
### 6. Download Assets
Follow the "Download Theme Assets" instructions above.

### 7. Start the Server
```bash
php artisan serve
```

📂 Project Structure
app/Http/Controllers/
└── LoginController.php       # Handles Login & Logout logic

resources/views/
├── auth/
│   ├── auth-master.blade.php # Layout for auth pages
│   ├── head-css.blade.php    # Auth specific CSS
│   ├── scripts.blade.php     # Auth specific JS
│   ├── footer.blade.php      # Auth footer
│   └── pages/
│       └── login.blade.php   # The Login UI form
│
└── layouts/                  # Main Dashboard UI components
    ├── master.blade.php
    ├── topbar.blade.php
    ├── sidebar.blade.php
    └── ...


### 📄 License
This project is for educational and portfolio purposes. The Velzon theme is subject to its original licensing terms by Themesbrand.

Built with ❤️ using Laravel 11+ and clean MVC practices.