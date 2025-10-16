## Kandidat Developer Juke

Membuat REST API berbasis **Java** + Spring Boot (MVC) | **Golang** boleh
Mengelola data CRUD sederhana
Menjalankan aplikasi di Docker
Kalo bisa jangan minta generate dari AI ya

## 🧩 Case Soal: Employee Management REST API
## 📘 Deskripsi Kasus
Perusahaan  bernama "Juke" ingin membuat sistem sederhana untuk mengelola data karyawan.
Mereka meminta kamu membuat REST API berbasis Java (Spring Boot) / Golang dengan konsep MVC (Model-View-Controller).
Aplikasi ini nantinya akan dijalankan menggunakan Docker.

## 🎯 Tujuan Utama

Kandidat dapat membuat REST API sesuai prinsip MVC.
Dapat melakukan operasi CRUD pada entity “Employee”.
API bisa dijalankan di container Docker.
(Opsional): menambahkan validasi, exception handling, dan dokumentasi API (Swagger).

## 🧱 Spesifikasi Teknis

1. Bahasa & Framework
Java 17+ atau Golang

2. Struktur MVC minimal:
src/
 ├── controller/
 ├── service/
 ├── repository/
 └── model/

## 📋 Entity: Employee
Field	Type	Keterangan
id	Long	auto increment
name	String	nama lengkap
email	String	harus unik
position	String	jabatan karyawan
salary	Double	gaji karyawan
createdAt	LocalDateTime	waktu data dibuat

## 🔌 Endpoint REST API
Method	Endpoint	Deskripsi
GET	/api/employees	Menampilkan semua karyawan
GET	/api/employees/{id}	Menampilkan detail 1 karyawan
POST	/api/employees	Menambahkan data karyawan baru
PUT	/api/employees/{id}	Mengubah data karyawan
DELETE	/api/employees/{id}	Menghapus data karyawan

## ⚙️ Fungsi Tambahan (Opsional)
Validasi input menggunakan @Valid (misal: email tidak boleh kosong, salary > 0).
Global error handling (@ControllerAdvice).
Dokumentasi Swagger (misal: springdoc-openapi-ui).
Gunakan logging sederhana (@Slf4j).

## 🐳 Deploy di Docker
Buat file Dockerfile di root project dengan contoh berikut:
Buat Docker compose agar tinggal di run

## 🧠 Penilaian (Total 100 poin)
Kriteria	Bobot
Struktur kode rapi & sesuai MVC	20
Endpoint CRUD berfungsi dengan benar	30
Validasi input & error handling	5
Dokumentasi Swagger	5
Dockerfile berfungsi (aplikasi bisa jalan di container)	20
Bisa menjelaskan apa yang dibuat 20

## 📦 Output yang Diminta
Source code project (GitHub - Jika belum punya bisa buat dulu)
File Dockerfile, Docker compose
Petunjuk cara menjalankan project di file README.md