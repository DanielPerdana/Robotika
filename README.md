# 🤖 Robotika Learning Repository - Kegiatan Perkuliahan

Selamat datang di repositori ini! Repository ini dibuat sebagai dokumentasi dan penyimpanan progres belajar penulis dalam bidang **ROBOTIKA**, baik dalam bentuk source code, catatan eksperimen.

# Ringkasan Pertemuan

## Pertemuan 1
### Pengantar Mata Kuliah Robotik
Di pertemuan perdana, kami mengikuti sesi perkenalan dengan dosen pengampu, Bapak Basuki Rahmat. Selanjutnya diperkenalkan gambaran umum bidang robotik, termasuk skema perkuliahan, ketentuan tugas UTS, serta rencana pelaksanaan UAS yang akan ditempuh sepanjang mata kuliah ini.

## Pertemuan 2
### Instalasi dan Persiapan Arduino IDE
Pada pertemuan kedua, fokus belajar beralih pada pemasangan Arduino IDE sebagai software utama untuk pemrograman mikrokontroler. Kami juga mempelajari cara menambahkan library–library penting dan melakukan konfigurasi dasar yang dibutuhkan pada IDE.

## Pertemuan 3
### Praktik Awal Arduino IDE dengan ITCLab
Di pertemuan ketiga, kami langsung mencoba menjalankan kode contoh dari Pak Basuki. Program tersebut mengendalikan mesin ITCLab untuk memutar “gerigi” dengan kecepatan yang dipercepat, lalu diperlambat hingga berhenti. Kegiatan ini memperkenalkan dasar pengaturan kecepatan motor melalui pemrograman.
### Dokumentasi
<img src="./Dokumentasi ITCLab dan IMCLab/ITCLab Test.jpeg" alt="Praktik Arduino IDE Dengan ITCLab" height="300"/>

## Pertemuan 4
### Mengoperasikan LED menggunakan Arduino IDE dan ITCLab
Pada pertemuan keempat, kami praktik menyalakan dan mematikan LED dengan kode yang tersedia. Materi utamanya adalah memahami penggunaan pin digital pada Arduino dan proses upload program ke board lewat ITCLab.
### Dokumentasi
<img src="./Dokumentasi ITCLab dan IMCLab/IMCLab Test.jpeg" alt="Praktik Arduino IDE Dengan ITCLab" height="300"/>

## Pertemuan 5
### Kontrol Motor dengan IMCLab
Pembelajaran dilanjutkan dengan praktik kendali motor melalui IMCLab. Kami mendalami penggunaan pin PWM serta prinsip dasar menggerakkan motor dengan mikrokontroler menggunakan Arduino IDE.

## Pertemuan 6
### Pengenalan IoT dan Aplikasi MQTT Panel
Materi pada pertemuan keenam beralih ke konsep Internet of Things (IoT). Kami diminta memasang aplikasi MQTT Panel di smartphone, kemudian belajar menghubungkan Arduino IDE dengan protokol MQTT via library PubSubClient. Untuk medium jaringan, digunakan hotspot smartphone dengan memasukkan SSID dan kata sandi ke dalam kode.

## Pertemuan 7
### Praktik Kontrol Robot BNU V2 via IoT MQTT Panel
Di pertemuan ketujuh, kami mengendalikan robot BNU V2 secara langsung melalui aplikasi MQTT Panel. Perintah dikirim lewat protokol MQTT dan diinterpretasikan menjadi aksi nyata pada robot, sehingga kami memperoleh pengalaman praktis komunikasi IoT dengan robotika.
### Dokumentasi
<img src="./Dokumentasi ITCLab dan IMCLab/BNUV2-IoT-MQTT-Panel.jpeg" alt="Praktik Arduino IDE Dengan ITCLab" height="300"/>

# Praktek Menggunakan Arduino

##  iMcLab.ino
Sketch Arduino ini mendemonstrasikan dasar-dasar pengendalian arah dan kecepatan motor DC menggunakan PWM. 
Motor akan bergerak maju dan mundur secara bergantian dengan kecepatan penuh, berhenti di antaranya, dan meningkatkan kecepatan secara bertahap dalam kondisi tertentu.

## itclab-07.ino
Firmware Arduino ini digunakan untuk mengendalikan iTCLab Shield melalui perintah serial. 
Pengguna dapat mengatur output PWM untuk dua saluran (Q1 dan Q2) serta LED, dan membaca suhu dari dua sensor (T1 dan T2). 
Perintah dikirim melalui antarmuka serial dan sistem merespons dengan mengatur output atau mengirim data suhu. 
Termasuk logika keamanan yang akan mematikan output secara otomatis jika suhu sensor melebihi batas tertentu, serta mendukung perintah versi dan stop.

## pid.py
File Python ini mendefinisikan kelas iTCLab untuk mengelola komunikasi serial dengan perangkat Arduino dalam eksperimen kontrol suhu dan akuisisi data. 
Mendukung pembacaan suhu (T1 dan T2), pengendalian output (heater dan LED melalui PWM), penyimpanan data ke file teks, serta penanganan koneksi secara otomatis dengan deteksi port. 
Dirancang untuk digunakan dalam eksperimen robotika dan kontrol proses, menggunakan library pyserial dan numpy.


## MQTT-Based Temperature Control Sketch
Sketch ini dirancang untuk sistem pengendalian suhu dengan kemampuan pemantauan dan pengendalian jarak jauh berbasis MQTT.

# 🤖 Robot BNU: Deteksi Objek Real-time dengan PyTorch dan MobileNet

### Kelompok Peneliti

| Nama                | NIM         |
| ------------------- | ----------- |
| Yudhistira Nanda K. | 22081010055 |
| Daniel Perdana M.   | 22081010064 |
| Ferry Hasan         | 22081010085 |
| Suwito              | 22081010102 |
| Jerry Ramadhani C.  | 22081010140 |

## 📌 Deskripsi Singkat Proyek

Proyek ini bertujuan untuk membangun kode program untuk identifikasi objek melalui kamera secara realtime berbasis CNN (Convolutional Neural Network) menggunakan arsitektur MobileNet dari 91 kategori objek yang sudah di pre-trained. Berikut dokumen [Proposal PKM-KC ](<./Proposal PKM - KC 2025 Robotika.pdf>).

## 📝 Pendahuluan

<div style="display: flex; justify-content: space-between; gap: 10px;">
  <img src="./Dokumentasi Final Project/BNUxAI Test.jpeg" alt="Robot BNU + ML + AI 1" height="300"/>
  <img src="./Dokumentasi Final Project/ROBOT-BNU-AI.png" alt="Robot BNU + ML + AI 2" height="300"/>
  <img src="./Dokumentasi Final Project/default-ROBOT-BNU.jpeg" alt="Robot BNU + ML + AI 3" height="300"/>
</div>

Proyek ROBOT BNU ini adalah sistem robotik cerdas yang mampu melakukan deteksi objek secara real-time. Menggunakan model **SSDLite320-MobileNetV3-Large** dari PyTorch, robot dapat mengidentifikasi berbagai objek di lingkungannya melalui kamera. Informasi ini kemudian digunakan untuk mengirim perintah ke mikrokontroler Arduino, memungkinkan robot bereaksi, terutama untuk menghindari tabrakan.

Proyek ini adalah contoh penerapan **Artificial Intelligence (AI)** dan **Machine Learning (ML)** dalam robotika, membangun dasar untuk perilaku otonom yang lebih kompleks.

## ⭐ Fitur Utama

- Deteksi objek **real-time** menggunakan webcam.
- Memanfaatkan model **SSDLite320-MobileNetV3-Large** untuk inferensi yang efisien.
- Berkomunikasi dengan Arduino melalui port serial.
- Logika sederhana untuk **menghindari tabrakan**: robot berhenti jika objek terlalu dekat.
- Menampilkan kotak pembatas, nama kelas, dan skor keyakinan pada umpan video.

## ⚙️ Cara Kerja

1.  **Inisialisasi:** Menghubungkan Arduino, memuat model SSDLite-MobileNet, dan daftar nama kelas.
2.  **Pemrosesan Video:** Mengambil frame dari webcam, mengubah ukurannya, dan mengonversinya menjadi tensor untuk model.
3.  **Deteksi Objek:** Model memproses tensor dan menghasilkan kotak pembatas, skor, serta label objek yang terdeteksi.
4.  **Logika Kontrol:**
    - Jika terdeteksi `__background__` (tidak ada objek relevan), kirim `0` (berhenti/idle).
    - Jika objek terdeteksi dan ketinggian kotak pembatas **lebih dari 800 piksel** (objek sangat dekat, \< 1 meter), kirim `4` (henti darurat).
    - Jika objek terdeteksi tapi tidak terlalu dekat, kirim `1` (maju).
5.  **Komunikasi Arduino:** Perintah (`'0'`, `'1'`, atau `'4'`) dikirim ke Arduino hanya jika ada perubahan perintah.
6.  **Visualisasi:** Menampilkan hasil deteksi pada umpan video.

## 📋 Perancangan Logika Kontrol dan Komunikasi

- **Logika Kontrol Robot:** Dikembangkan logika sederhana untuk menginterpretasikan hasil deteksi menjadi perintah gerakan robot:
  - Jika tidak ada objek yang terdeteksi relevan (atau deteksi _background_), robot diberi perintah `'0'` (berhenti/idle).
  - Jika objek terdeteksi dan ketinggian kotak pembatas (`bbox_height`) **lebih dari 800 piksel** (diasumsikan objek sangat dekat, mis. kurang dari 1 meter), robot diberi perintah `'4'` (henti darurat). Heuristik ketinggian kotak pembatas ini digunakan sebagai estimasi kasar jarak.
  - Jika objek terdeteksi tetapi ketinggian kotak pembatas di bawah ambang batas (objek tidak terlalu dekat), robot diberi perintah `'1'` (maju).
  - Prioritas diberikan pada deteksi yang menunjukkan bahaya terdekat.
- **Komunikasi Serial:** Pustaka `pyserial` digunakan untuk membangun koneksi serial antara skrip Python dan Arduino. Perintah karakter (`'0'`, `'1'`, `'4'`) dikirim secara efisien, hanya ketika ada perubahan status perintah untuk menghindari transmisi berulang yang tidak perlu.

## 📈 Hasil dan Evaluasi

### A. Deteksi Objek Real-time

Sistem berhasil melakukan deteksi objek secara real-time pada umpan video webcam. Model SSDLite-MobileNetV3-Large menunjukkan performa yang baik dalam mengidentifikasi berbagai objek yang umum ditemukan dalam lingkungan operasional robot, dengan menampilkan kotak pembatas, nama kelas, dan skor kepercayaan secara visual pada _frame_. Kecepatan inferensi model cukup memadai untuk aplikasi real-time, terutama jika didukung oleh GPU.

### B. Respons Robot

Robot menunjukkan kemampuan dasar untuk merespons objek yang terdeteksi:

- **Maju:** Robot dapat bergerak maju ketika tidak ada objek di jalur yang mengindikasikan bahaya.
- **Berhenti (jarak aman):** Robot berhenti ketika objek terdeteksi dan diasumsikan sangat dekat (berdasarkan ketinggian kotak pembatas). Ini menunjukkan kemampuan dasar penghindaran tabrakan.
- **Kontrol Serial:** Komunikasi antara Python dan Arduino berfungsi dengan baik, memastikan perintah kontrol robot diterima dan dieksekusi secara tepat waktu.

### C. Keterbatasan dan Pembelajaran

- **Estimasi Jarak Heuristik:** Penggunaan ketinggian kotak pembatas sebagai proxy untuk estimasi jarak adalah metode yang sederhana namun memiliki keterbatasan akurasi. Faktor-faktor seperti ukuran sebenarnya objek dan sudut pandang kamera dapat memengaruhi interpretasi jarak ini. Untuk estimasi jarak yang lebih presisi, integrasi sensor kedalaman (misalnya, LiDAR atau kamera kedalaman) akan sangat meningkatkan keandalan.
- **Logika Navigasi Sederhana:** Sistem saat ini hanya mendukung perintah "maju" dan "berhenti". Untuk otonomi yang lebih tinggi, diperlukan pengembangan logika navigasi yang lebih kompleks, seperti berbelok untuk menghindari rintangan atau mengikuti jalur.
- **Robustness:** Kondisi pencahayaan yang bervariasi atau lingkungan yang sangat ramai dapat memengaruhi akurasi deteksi dan konsistensi respons robot.

Secara keseluruhan, proyek ROBOT BNU berhasil membangun fondasi yang kuat untuk robot otonom dengan kemampuan deteksi objek real-time. Meskipun ada beberapa area untuk peningkatan, hasil yang dicapai menunjukkan potensi besar penerapan AI/ML dalam sistem robotik.

## ⛓️ Protokol Komunikasi Arduino

- `'0'`: Tidak ada objek terdeteksi / latar belakang. Robot berhenti atau diam.
- `'1'`: Objek terdeteksi, jarak aman. Robot bergerak maju.
- `'4'`: Objek terlalu dekat. Robot segera berhenti.

## 🧪 Peningkatan di Masa Depan

- Navigasi yang lebih canggih (belok kiri/kanan).
- Penanganan banyak objek.
- Estimasi jarak yang lebih akurat dengan sensor kedalaman.
- Peningkatan ketahanan sistem.
- Antarmuka pengguna grafis (GUI).
- Optimasi model lebih lanjut.
- Pelatihan model dengan dataset khusus.
