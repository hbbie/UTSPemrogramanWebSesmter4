Mantap, ini kita upgrade ke **level portfolio cybersecurity + ada gambar langsung tampil di README (super keren & meyakinkan dosen)** 🔥
Tinggal **copy sekali langsung jadi** 👇

---

````markdown
# 🛡️ SQL Injection Login Lab

<p align="center">
  <img src="https://img.shields.io/badge/PHP-8.x-blue?style=flat-square&logo=php">
  <img src="https://img.shields.io/badge/MySQL-Database-orange?style=flat-square&logo=mysql">
  <img src="https://img.shields.io/badge/Security-SQL%20Injection-red?style=flat-square">
  <img src="https://img.shields.io/badge/Type-Cybersecurity%20Lab-green?style=flat-square">
  <img src="https://img.shields.io/badge/Status-Completed-brightgreen?style=flat-square">
</p>

<p align="center">
  <b>Simulasi serangan SQL Injection pada sistem login web dan implementasi teknik pencegahannya</b>
</p>

---

## 📌 Overview

Project ini merupakan **mini cybersecurity lab** yang mensimulasikan bagaimana serangan SQL Injection dapat mengeksploitasi sistem login sederhana.

Melalui pendekatan eksperimen, project ini menunjukkan:
- bagaimana celah keamanan terjadi  
- bagaimana attacker memanfaatkannya  
- dan bagaimana developer dapat memperbaikinya  

---

## 🧪 Experiment Flow

### 🔹 1. Input SQL Injection

<img src="images/screenshot1.png" width="700">

📌 Payload:
```sql
admin' --
````

👉 User mencoba memasukkan input berbahaya ke dalam form login.

---

### 🔹 2. Login Berhasil (Bypass)

<img src="images/screenshot2.png" width="700">

⚠️ Sistem mengizinkan login tanpa password karena query dimanipulasi.

---

### 🔹 3. Setelah Perbaikan

<img src="images/screenshot3.png" width="700">

✅ Sistem sudah aman — SQL Injection tidak lagi berhasil.

---

## 🔍 How It Works

Query awal:

```sql
SELECT * FROM users WHERE username='$username' AND password='$password';
```

Setelah injection:

```sql
SELECT * FROM users WHERE username='admin' -- ' AND password='...';
```

💡 Bagian password diabaikan → login berhasil

---

## 🛡️ Security Fix

Perbaikan dilakukan dengan:

```php
$stmt = $conn->prepare("SELECT * FROM users WHERE username=? AND password=?");
$stmt->bind_param("ss", $username, $password);
$stmt->execute();
```

✔ Input tidak bisa memanipulasi query
✔ Sistem menjadi lebih aman

---

## 🏗️ Project Structure

```
sql-injection-login-lab/
├── images/
│   ├── screenshot1.png
│   ├── screenshot2.png
│   └── screenshot3.png
├── login.php
├── proses_login_vulnerable.php
├── proses_login_secure.php
├── dashboard.php
├── koneksi.php
├── logout.php
├── database.sql
├── style.css
└── README.md
```

---

## ⚙️ Tech Stack

* PHP (Native)
* MySQL
* HTML & CSS
* XAMPP

---

## 🚀 Run Locally

```bash
git clone https://github.com/username/sql-injection-login-lab.git
```

1. Pindahkan ke `htdocs`
2. Import `database.sql`
3. Jalankan:

```
http://localhost/sql-injection-login-lab/login.php
```

---

## 🔐 Security Insight

> "Security is not about complexity, it's about correctness."

Kesalahan kecil dalam query bisa membuka celah besar.

---

## ⚠️ Disclaimer

Project ini hanya untuk pembelajaran dan eksperimen lokal.
Tidak untuk digunakan dalam aktivitas ilegal.

---

## 👨‍💻 Author

* Nama: **(Isi Nama Kamu)**
* Kelas: **(Isi Kelas Kamu)**

---

## ⭐ Portfolio Note

Project ini dapat digunakan sebagai:

* 📂 Portfolio Cybersecurity
* 📘 Dokumentasi pembelajaran Web Security
* 🧪 Mini Lab SQL Injection

---

<p align="center">
  <b>🚀 Practice Makes Secure</b>
</p>
```

---

## 🧠 Cara Biar Gambarnya Muncul di GitHub

1. Buat folder:

```
images/
```

2. Masukkan screenshot kamu:

* `screenshot1.png` (form + payload)
* `screenshot2.png` (login berhasil)
* `screenshot3.png` (login gagal)

3. Upload ke GitHub (drag & drop)

---

