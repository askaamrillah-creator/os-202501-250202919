
# Laporan Praktikum Minggu 6
Topik: Penjadwalan CPU – Round Robin (RR) dan Priority Scheduling

---

## Identitas
- **Nama**  : aska asofri amrillah  
- **NIM**   : 250202919
- **Kelas** : 1ikra

---

## Tujuan
1. Mahasiswa mampu menghitung waiting time dan turnaround time pada algoritma RR dan Priority.
2. Mahasiswa mampu menyusun tabel hasil perhitungan dengan benar dan sistematis.
3. Mahasiswa mampu membandingkan performa algoritma RR dan Priority.
4. Mahasiswa mampu menjelaskan pengaruh time quantum dan prioritas terhadap keadilan eksekusi proses.
5. Mahasiswa mampu menarik kesimpulan mengenai efisiensi dan keadilan kedua algoritma.


---

## Dasar Teori
Penjadwalan CPU adalah mekanisme sistem operasi yang menentukan urutan proses yang akan dijalankan oleh CPU agar penggunaan sumber daya menjadi efisien dan adil.

Algoritma Round Robin (RR) memberikan waktu eksekusi (time quantum) yang sama kepada setiap proses secara bergantian. Jika waktu habis dan proses belum selesai, proses tersebut akan kembali ke antrian untuk menunggu giliran berikutnya.

Algoritma Priority Scheduling mengeksekusi proses berdasarkan tingkat prioritasnya. Proses dengan prioritas lebih tinggi akan dijalankan terlebih dahulu dibandingkan proses dengan prioritas rendah.

Ukuran time quantum berpengaruh terhadap kinerja sistem. Jika terlalu kecil, sistem sering berpindah proses sehingga tidak efisien; jika terlalu besar, proses lain akan menunggu terlalu lama.

Kelemahan Priority Scheduling adalah bisa menyebabkan starvation, yaitu ketika proses dengan prioritas rendah terus tertunda karena selalu kalah dengan proses berprioritas tinggi.


---

## Langkah Praktikum
Langkah-langkah yang dilakukan.
1.) Buka Aplikasi Excel/Google Sheets untuk membuat perhitungan.

2.)Siapkan Data Proses

Gunakan contoh data berikut (boleh dimodifikasi sesuai kebutuhan):

Proses	Burst Time	Arrival Time	Priority
P1	5	0	2
P2	3	1	1
P3	8	2	4
P4	6	3	3
3.) Mengerjakan Eksperimen 1 – Round Robin (RR)

Gunakan time quantum (q) = 3.
Hitung waiting time dan turnaround time untuk tiap proses.
Simulasikan eksekusi menggunakan Gantt Chart (manual atau spreadsheet).
Catat sisa burst time tiap putaran.
4.) Mengerjakan Eksperimen 2 – Priority Scheduling (Non-Preemptive)

Urutkan proses berdasarkan nilai prioritas (angka kecil = prioritas tinggi).
Lakukan perhitungan manual.
Buat tabel perbandingan hasil RR dan Priority.
5.) Mengerjakan Eksperimen 3 – Analisis Variasi Time Quantum (Opsional)

Ubah quantum menjadi 2 dan 5.
Amati perubahan nilai rata-rata waiting time dan turnaround time.
Buat tabel perbandingan efek quantum.
6.) Melakukan Dokumentasi
Buat tabel perbandingan seperti berikut:


7.) Kemudian melakukan commit dan push ketika sudah selesai.
 2. Perintah yang dijalankan.
 Round Robin :
- Waiting Time  
1. Waiting Time = Finish Time - Arrival Time - Burst Time
2. Waiting Time = Turnaround Time - Burst Time

- Turnaround Time 
1. Turnaround Time = Waiting Time + Burst Time
2. Turnaround Time = Finish Time - Arrival Time

Priority Scheduling (Non-Preemptive):
WT[i] = waktu mulai eksekusi - Arrival[i]
TAT[i] = WT[i] + Burst[i]


   Rata-rata Waiting Time = Total Waiting Time
                            ___________________
                               Jumlah Proses
   Rata-rata Turnaround Time = Total Turnaround Time
                               ______________________
                                   Jumlah Proses
3. File dan kode yang dibuat.
aporan.md, Hasil_Experimen-1.png, Hasil_Eksperimen-2.png, Hasil_Experimen-3_q=2.png, Hasil_Experimen-3_q=5.png
4. Commit message yang digunakan --> Minggu 6 - CPU Scheduling RR & Priority
---

## Kode / Perintah
Potongan kode atau perintah utama:
Round Robin :
- Waiting Time  
1. Waiting Time = Finish Time - Arrival Time - Burst Time
2. Waiting Time = Turnaround Time - Burst Time

- Turnaround Time 
1. Turnaround Time = Waiting Time + Burst Time
2. Turnaround Time = Finish Time - Arrival Time

Priority Scheduling (Non-Preemptive):
WT[i] = waktu mulai eksekusi - Arrival[i]
TAT[i] = WT[i] + Burst[i]


   Rata-rata Waiting Time = Total Waiting Time
                            ___________________
                               Jumlah Proses
   Rata-rata Turnaround Time = Total Turnaround Time
                               ______________________
                                   Jumlah Proses
																	 
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
1. [Pertanyaan 1]  
   **Jawaban:**  
2. [Pertanyaan 2]  
   **Jawaban:**  
3. [Pertanyaan 3]  
   **Jawaban:**  

---

## Refleksi Diri
Tuliskan secara singkat:
- Apa bagian yang paling menantang minggu ini?  
- Bagaimana cara Anda mengatasinya?  

---

**Credit:**  
_Template laporan praktikum Sistem Operasi (SO-202501) – Universitas Putra Bangsa_
