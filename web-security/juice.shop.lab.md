# 🧃 OWASP Juice Shop Lab Setup

## 🚀 Deployment
Aplikasi dieksekusi di lokal menggunakan Docker:
```bash
docker run -d -p 3000:3000 --name juiceshop bkimminich/juice-shop

Completed Challenges:
    - [x] **Admin Login (SQL Injection):** Berhasil login sebagai admin tanpa password menggunakan payload `' OR 1=1--` pada form login email.
    - [x] **Confidential Document (Sensitive Data Exposure):** Berhasil menemukan dan mengunduh dokumen rahasia `acquisitions.md` melalui direktori penyimpanan terbuka `/ftp`.
    - [x] **Poison Null Byte:** Berhasil mengunduh file sensitif bertipe terlarang (`.bak`) menggunakan teknik URL encoding `%2500.md` pada direktori `/ftp`.
    - [x] **DOM XSS:** Berhasil mengeksekusi script pemicu pop-up alert menggunakan payload `<iframe src="javascript:alert(`xss`)">` pada kolom pencarian.
    