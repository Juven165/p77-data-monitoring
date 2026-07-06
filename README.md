# ⛽ P77 Fuel Inventory Monitoring

## 📖 Overview

**P77 Fuel Inventory Monitoring** is a web-based application developed to simplify fuel inventory reporting across P77 Petroleum Distribution Inc. stations.

The system allows station staff to submit daily fuel tank measurements using dipstick readings. Based on the submitted fuel volume, the system automatically calculates the remaining fuel capacity for each tank, eliminating the need for manual Excel computations.

The application includes secure authentication features such as **Email Verification**, **Password Reset via Email**, and **Cloudflare Turnstile CAPTCHA** to help protect against spam and unauthorized registrations.

The system is deployed on **DigitalOcean** with **PostgreSQL** as the production database and is accessible through a secure company subdomain.

Staff users can submit fuel inventory reports, view their station's report history, and monitor recent submissions through a simple dashboard. Administrators can manage stations, clusters, users, and monitor fuel inventory reports from all stations in real time.

---

## ✨ Features

### 👷 Staff
- Secure Login & Logout
- Email Verification
- Password Reset
- Submit Fuel Inventory Report
- Automatic Fuel Remaining Calculation
- View Recent Reports
- Dashboard Statistics

### 👨‍💼 Administrator
- Dashboard
- User Management
- Station Management
- Cluster Management
- Assign Users to Stations
- Fuel Inventory Monitoring
- Reports Overview
- Notification System

---

## 🛠️ Built With

- Python
- Django
- PostgreSQL
- Bootstrap 5
- HTML5
- CSS3
- JavaScript
- DigitalOcean
- Cloudflare Turnstile

---

## ⚙️ How It Works

Each fuel tank has a predefined maximum capacity.

Example:

Tank Capacity: **16,000 Liters**

Current Fuel Reading: **9,000 Liters**

Remaining Capacity:

```
16,000 - 9,000 = 7,000 Liters
```

This calculation helps the company determine how much fuel can still be delivered to each station.

---

## 👨‍💻 Developed By

**Juven T. Pinoy**

Bachelor of Science in Information Technology

Carlos Hilado Memorial State University

Class of 2025

---

## ⚙️ Installation

### 1. Clone the repository

```bash
git clone https://github.com/Juven165/p77-data-monitoring.git
```

### 2. Navigate to the project directory

```bash
cd p77-data-monitoring
```

### 3. Create a virtual environment

```bash
python -m venv venv
```

### 4. Activate the virtual environment

**Windows**

```bash
venv\Scripts\activate
```

**macOS / Linux**

```bash
source venv/bin/activate
```

### 5. Install project dependencies

```bash
pip install -r requirements.txt
```

### 6. Configure environment variables

Create a `.env` file in the project root.

Example:

```env
SECRET_KEY=your_secret_key
DEBUG=True

DATABASE_NAME=your_database_name
DATABASE_USER=your_database_user
DATABASE_PASSWORD=your_database_password
DATABASE_HOST=localhost
DATABASE_PORT=5432

EMAIL_HOST_USER=your_email@gmail.com
EMAIL_HOST_PASSWORD=your_app_password

TURNSTILE_SITE_KEY=your_cloudflare_site_key
TURNSTILE_SECRET_KEY=your_cloudflare_secret_key
```

### 7. Apply database migrations

```bash
python manage.py migrate
```

### 8. Create a superuser

```bash
python manage.py createsuperuser
```

### 9. Run the development server

```bash
python manage.py runserver
```

Open your browser and visit:

```
http://127.0.0.1:8000/
```
  
