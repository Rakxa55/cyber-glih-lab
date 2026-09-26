# 🧃 OWASP Juice Shop Lab Setup

## 🚀 Deployment
Aplikasi dieksekusi di lokal menggunakan Docker:
```bash
docker run -d -p 3000:3000 --name juiceshop bkimminich/juice-shop

Completed Challenges:
    - [x] **Admin Login (SQL Injection):** Berhasil login sebagai admin tanpa password menggunakan payload `' OR 1=1--` pada form login email.