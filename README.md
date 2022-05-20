# 🌊TUGAS AKHIR KELOMPOK PEMOS TEAM 20🌊
_Repository_ ini dibuat untuk memenuhi Tugas Akhir Kelompok Praktikum Pemodelan Oseanografi 2022. _Repository_ ini memuat file berupa _script python_ (py) yang digunakan untuk memproses beberapa pemodelan oseanografi seperti Adveksi-Difusi dan Hidrodinamika. Pengerjaan _repository_ ini menggunakan bahasa pemrograman _python_ yang dapat dilakukan pada beberapa _platform_ seperti _Google Collaboratory_ atau _Jupyter Notebook_. _Mandatory library_ yang digunakan kali ini adalah _Numpy, Matplotlib, Python, Sys, Siphon_ dan _Pprint_. Seluruh _script_ yang dibuat adalah hasil Team 20 Oseanografi 2020. Semoga dapat bermanfaat!

# 🙋🏼‍♀️1. AUTHORS (TEAM 20)🙋🏼‍♂️
1. Doding Akka Damanik
2. Azalya Besari Noerazzahra Tilaar
3. Umar Abdul Aziz
4. Clarisa Wulandari
5. Ananda Annisa Fitriani
6. M. Zanugera Alamsyah 26050120120015 A
7. Olivia Rebeka Vera Wati Sinaga

# 🗒️2. CARA PENGGUNAAN SCRIPT🗒️
1. Pengguna dapat membuka folder _Kumpulan Script_ pada _repository_ ini. Di dalamnya terdapat 3 _script_, bisa dibuka salah satu.
![1](https://user-images.githubusercontent.com/105897134/169439922-6bd9c427-5733-41fc-80cb-f50c3f0425c6.png)
2. Tampilan _script_ akan muncul seperti gambar di bawah ini. 
![2](https://user-images.githubusercontent.com/105897134/169441338-d7256c02-e782-4407-aea9-a395260713d6.png)
3. Script dapat di-_copy_ untuk nantinya dipergunakan dan disesuaikan di _Jupyter Notebook_ maupun _Google Collaboratory._

# 🧮3. METODE PENGERJAAN📝
1. Modul 2: Adveksi-Difusi 2 Dimensi
2. Modul 3: Model Hidrodinamika 1 Dimensi Sederhana
3. Modul 4: Model Hidrodinamika 2 Dimensi

## 📒**3.1. Modul 2: Adveksi-Difusi 2 Dimensi**📒

### 📌Definisi dan Persamaan📌

Adveksi 2 dimensi adalah proses pergerakan substansi atau materi oleh fluida akibat dipengaruhi gaya-gaya tertentu dalam arah vertikal dan horizontal.

Difusi 2 dimensi adalah proses penyebaran substansi atau materi oleh fluida akibat dipengaruhi gaya-gaya tertentu dalam arah vertikal dan horizontal.

Persamaan adveksi-difusi merupakan persamaan matematis yang dirancang untuk mempelajari fenomena transpor polutan. Persamaan adveksi-difusi dua dimensi merupakan model matematika yang menggambarkan proses transportasi suatu zat yang dipengaruhi gaya dalam dua dimensi. Persamaannya secara umum sebagai berikut:

### 📌Metode Diskritisasi Beserta Hasilnya📌
Diskritisasi persamaan adveksi-difusi 2 dimensi menggunakan metode eksplisit upstream dimana persamaan beda hingga dengan metode ini menggunakan pendekatan beda maju untuk turunan waktu, sedangkan untuk turunan ruang dilakukan dengan melihat arah kecepatan u.
Jika u > 0, turunan ruang menggunakan beda mundur. Jika u < 0, digunakan pendekatan beda maju. Berikut adalah hasil diskritisasi untuk persamaan adveksi 2 dimensi.
