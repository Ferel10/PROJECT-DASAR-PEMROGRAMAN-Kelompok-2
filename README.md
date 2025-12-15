________________________________________
Toolkit Lengkap Asisten Laboratorium Elektro
Final Project – Dasar Pemrograman
Departemen Teknik Elektro 
Institut Teknologi Sepuluh Nopember (ITS)
________________________________________
Group Identity
Project Title: Toolkit Lengkap Asisten Laboratorium Elektro
Course: Dasar Pemrograman
Lecturer: Pak Arta Kusuma
No	Name	Student ID (NRP)	Study Program
1	Ferel Eulogia Simanjorang	5022251081	Electrical Engineering
2	Hansel Jonggi Napitupulu	5022251066	Electrical Engineering
3	Samuel Julius Steven Sinaga	5022251064	Electrical Engineering
________________________________________
Project Description
Toolkit Lengkap Asisten Laboratorium Elektro adalah sebuah aplikasi berbasis bahasa pemrograman C yang dikembangkan sebagai proyek akhir mata kuliah Dasar Pemrograman di Institut Teknologi Sepuluh Nopember.
Program ini dirancang sebagai Electrical Calculator Kit, yaitu alat bantu berbasis command-line interface (CLI) yang menyediakan berbagai fitur perhitungan rangkaian listrik DC sederhana serta konversi sistem bilangan yang umum digunakan dalam Sistem Digital.
Aplikasi ini ditujukan untuk membantu Asisten Laboratorium dan praktikan dalam melakukan verifikasi cepat terhadap perhitungan manual, baik pada tahap persiapan laporan maupun saat analisis hasil praktikum.
________________________________________
Project Objective
Tujuan pengembangan program ini adalah:
1.	Menerapkan konsep dasar pemrograman menggunakan bahasa C.
2.	Mengembangkan aplikasi interaktif berbasis menu (menu-driven program).
3.	Mengimplementasikan fungsi, percabangan, perulangan, dan pengolahan input.
4.	Membantu mahasiswa memahami dan memverifikasi perhitungan rangkaian listrik DC.
5.	Menyediakan utilitas konversi sistem bilangan untuk mendukung pembelajaran sistem digital.
________________________________________
Program Menu Structure
Program dijalankan melalui terminal dan menggunakan menu utama yang ditampilkan secara berulang hingga pengguna memilih keluar.
Main Menu
•	Verifikasi Rangkaian Elektrik
•	Utilitas Sistem Digital
•	Keluar Program
Verifikasi Rangkaian Elektrik
1.	Kalkulator Hukum Ohm (V = I × R)
2.	Kalkulator Daya Listrik (P = V × I)
3.	Kalkulator Resistor Seri
4.	Kalkulator Resistor Paralel
Utilitas Sistem Digital
5.	Desimal → Biner / Oktal / Heksadesimal
6.	Biner → Desimal
7.	Oktal → Desimal
8.	Heksadesimal → Desimal
________________________________________
Function Documentation
1. Hukum Ohm
Digunakan untuk Kalkulator menghitung salah satu besaran listrik dasar, yaitu tegangan, arus, atau hambatan, berdasarkan dua besaran lainnya.
Rumus yang digunakan:
•	Tegangan: V = I × R
•	Arus: I = V / R
•	Hambatan: R = V / I
________________________________________
2. Kalkulator Daya Listrik
Fungsi ini digunakan untuk menghitung daya listrik yang terdisipasi pada suatu komponen atau rangkaian.
Rumus:
•	P = V × I
________________________________________
3. Resistor Seri
Menghitung nilai hambatan total dari beberapa resistor yang dirangkai secara seri.
Rumus:
•	R_total = R₁ + R₂ + … + Rₙ
________________________________________
4. Resistor Paralel
Menghitung nilai hambatan total dari beberapa resistor yang dirangkai secara paralel.
Rumus:
•	1 / R_total = 1 / R₁ + 1 / R₂ + … + 1 / Rₙ
________________________________________
Number Conversion Module (Sistem Bilangan)
Modul konversi bilangan bertujuan untuk membantu praktikan memahami dan memverifikasi perubahan bilangan antar sistem bilangan yang umum digunakan dalam rangkaian digital, yaitu Desimal (basis 10), Biner (basis 2), Oktal (basis 8), dan Heksadesimal (basis 16).
Seluruh proses konversi dilakukan menggunakan algoritma matematika dasar, tanpa menggunakan fungsi konversi bawaan bahasa C.
________________________________________
5. Desimal ke Biner, Oktal, dan Heksadesimal
Konversi dari bilangan desimal ke basis lain dilakukan menggunakan metode pembagian berulang (remainder method).
Prinsip kerja:
1.	Bilangan desimal dibagi dengan basis tujuan (2, 8, atau 16).
2.	Sisa pembagian dicatat sebagai digit hasil konversi.
3.	Proses diulang hingga hasil bagi bernilai 0.
4.	Urutan digit dibaca dari sisa terakhir ke sisa pertama.
Untuk bilangan heksadesimal, sisa pembagian 10–15 direpresentasikan dengan huruf A–F.
________________________________________
6. Biner ke Desimal
Konversi dari bilangan biner ke desimal dilakukan menggunakan metode nilai posisi (positional notation).
Setiap digit biner dikalikan dengan 2 pangkat posisi digitnya, dimulai dari posisi 0 di sisi kanan, kemudian seluruh hasil dijumlahkan.
Rumus umum:
Nilai Desimal = Σ (digit × 2^posisi)
________________________________________
7. Oktal ke Desimal
Konversi dari bilangan oktal ke desimal menggunakan prinsip yang sama dengan biner ke desimal, namun dengan basis 8.
Rumus:
Nilai Desimal = Σ (digit × 8^posisi)
Input divalidasi agar hanya menerima digit 0 sampai 7.
________________________________________
8. Heksadesimal ke Desimal
Konversi dari bilangan heksadesimal ke desimal menggunakan basis 16 dan mendukung digit 0–9 serta huruf A–F.
Rumus:
Nilai Desimal = Σ (digit × 16^posisi)
Input tidak valid akan ditolak untuk mencegah kesalahan perhitungan.
________________________________________
Input Validation
Untuk menjaga keandalan dan keamanan program, diterapkan validasi input sebagai berikut:
•	Bilangan biner hanya menerima digit 0 dan 1
•	Bilangan oktal hanya menerima digit 0–7
•	Bilangan heksadesimal hanya menerima digit 0–9 dan A–F
•	Nilai resistor dan arus tidak boleh bernilai nol atau negatif

