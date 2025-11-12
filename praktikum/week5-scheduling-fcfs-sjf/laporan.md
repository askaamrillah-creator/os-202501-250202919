
# Laporan Praktikum Minggu [X]
Topik: [penjadwalan CPU-FCFS dan SJF]

---

## Identitas
- **Nama**  : [aska asofri amrillah]  
- **NIM**   : [250202919]  
- **Kelas** : [1ikra]

---

## Tujuan
1. Menghitung waiting time dan turnaround time untuk algoritma FCFS dan SJF.
2. Menyajikan hasil perhitungan dalam tabel yang rapi dan mudah dibaca.
3. Membandingkan performa FCFS dan SJF berdasarkan hasil analisis.
4. Menjelaskan kelebihan dan kekurangan masing-masing algoritma.
5. Menyimpulkan kapan algoritma FCFS atau SJF lebih sesuai digunakan.
---

## Dasar Teori
- FCFS (First-Come, First-Served)
  FCFS adalah algoritma CPU yang menjalankan proses berdasarkan urutan kedatangan. proses yang datang lebih dulu akan di proses terlebih dahulu. Cara kerja FCFS ini adalah proses masuk ke antrian ready (ready queue) sesuai waktu kedatangannya kemudian, CPU mengeksekusi proses yang berada di depan antrian sampai selesai, setelah proses selesai, CPU mengambil proses selanjutnya di antrian.
  Kelebihan-kekurangan
Sederhana dan mudah di implementasikan-bisa terjadi convoy effect: proses pendek menunggu lama karena proses panjang di depan.
adil karena di proses berdasarkan urutan kedatangan - tidak efisien untuk sistem interaktif atau real time.
- SJF  (Shortes Job First)
  SJF adalah algoritma penjadwalan CPU yang menjalankan proses dengan burst time paling pendek terlebih dahulu. Cara kerja SJF CPU melihat semua proses yang siap di eksekusi, kemudian CPU memilih proses dengan waktu eksekusi (CPU burst) paling pendek, menjalankan proses tersebut hingga selesai (untuk non-preemtive) atau bisa di hentikan jika ada proses baru lebih pendek (untuk preemtive, di sebut SRTF-Shortest Remaining Time First).
  Kekurangan-Kelebihan
  Mengurangi average waiting time di banding FCFS - sulit di prediksi karena CPU burst harus di ketahui sebelumnya, lebih efisien untuk sistem batch - bisa terjadi starvation proses panjang bisa menunggu lama.

---

## Langkah Praktikum
1. Langkah-langkah yang dilakukan.  
2. Perintah yang dijalankan.  
3. File dan kode yang dibuat.  
4. Commit message yang digunakan.

---

## Kode / Perintah
Tuliskan potongan kode atau perintah utama:
```bash
uname -a
lsmod | head
dmesg | head
```

---

## Hasil Eksekusi
Sertakan screenshot hasil percobaan atau diagram:
![Screenshot hasil](screenshots/example.png)

---

## Analisis
- Jelaskan makna hasil percobaan.  
- Hubungkan hasil dengan teori (fungsi kernel, system call, arsitektur OS).  
- Apa perbedaan hasil di lingkungan OS berbeda (Linux vs Windows)?  

---

## Kesimpulan
Tuliskan 2–3 poin kesimpulan dari praktikum ini.

---

## Quiz
1. [apa perbedaan utama antara FCFS dan SJF]  
   Jika FCFS mengeksekusi proses sesuai urutan datang, tanpa memperhatikan lamanya proses, tetapi jika SJF mengeksekusi proses yang durasinya lebih pendek lebih dulu.  
2. [mengapa SJF dapat menghasilkan rata rata waktu tunggu minimum]  
   karena cara kerja nya selalu memprioritaskan proses yang paling cepat selesai
3. [apa kelemahan SJF jika di terapkan pada sistem interaktif]  
   Kelemahanya jika di terapka di sistem interaktif cukup segnifikan karena karakteristik dari SJF memprioritaskan proses yang paling singkat, berikut beberapa kelemahanya:
   1. Starvation (kelaparan Proses)
   2. Sulit memprediksi burst Time
   3. Tidak responsip untuk pengguna
   4. Overhead penghitungan
      

---

## Refleksi Diri
Tuliskan secara singkat:
- Apa bagian yang paling menantang minggu ini?  
- Bagaimana cara Anda mengatasinya?  

---

**Credit:**  
_Template laporan praktikum Sistem Operasi (SO-202501) – Universitas Putra Bangsa_
