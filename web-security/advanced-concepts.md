# 🛡️ Advanced Web Security Concepts

## 1. IDOR (Insecure Direct Object References)
- **Deskripsi:** Celah di mana pengguna bisa melihat atau mengubah data milik pengguna lain hanya dengan mengubah penanda ID pada request data.
- **Letak Vektor Input:** URL Path (`/api/users/105`), Query Parameter (`?id=4820`), atau Request Body JSON (`{"basket_id": 5}`).
- **Pencegahan:** Selalu lakukan pengecekan hak akses (*Access Control Check*) di sisi server untuk memastikan ID yang diminta memang milik akun yang sedang login.

## 2. OS Command Injection
- **Deskripsi:** Celah keamanan yang terjadi ketika input pengguna dilewatkan langsung ke perintah terminal/shell Sistem Operasi server tanpa sanitasi.
- **Letak Vektor Input:** Fitur diagnostik jaringan (seperti input tes `ping`), pemrosesan/konversi file media, atau parameter nama file ekspor.
- **Pencegahan:** Hindari memanggil perintah terminal OS secara langsung, gunakan *parameterized execution* (pemisahan argumen), dan terapkan validasi input yang ketat (seperti regex).