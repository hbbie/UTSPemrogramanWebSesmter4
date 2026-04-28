# UTSPemrogramanWebSesmter4
# 🛡️ SQL Injection Login Lab

<p align="center">
  <img src="https://img.shields.io/badge/PHP-8.x-blue?style=for-the-badge&logo=php">
  <img src="https://img.shields.io/badge/MySQL-Database-orange?style=for-the-badge&logo=mysql">
  <img src="https://img.shields.io/badge/Security-SQL%20Injection-red?style=for-the-badge&logo=hackthebox">
  <img src="https://img.shields.io/badge/Status-Learning-green?style=for-the-badge">
</p>

<p align="center">
  <b>Eksperimen sederhana untuk memahami celah keamanan SQL Injection pada sistem login web</b>
</p>

---

## 📌 Tentang Project

Project ini merupakan simulasi sederhana untuk mempelajari bagaimana **SQL Injection** dapat mengeksploitasi sistem login berbasis web.

Dalam project ini, saya membangun dua versi sistem:
- ❌ **Versi Rentan (Vulnerable)** → bisa dibypass login  
- ✅ **Versi Aman (Secure)** → menggunakan prepared statement  

Project ini dibuat sebagai bagian dari tugas **Pemrograman Web**.

---

## 🎯 Tujuan

- Memahami konsep SQL Injection secara langsung  
- Melakukan simulasi serangan pada form login  
- Menganalisis dampak dari celah keamanan  
- Mengimplementasikan metode pencegahan  
- Meningkatkan awareness keamanan web  

---

## 🧪 Skenario Eksperimen

### 1️⃣ Login Normal
Username: admin
Password: 12345

✅ Login berhasil

---

### 2️⃣ SQL Injection (Bypass Login)

Payload:
```sql
admin' --
