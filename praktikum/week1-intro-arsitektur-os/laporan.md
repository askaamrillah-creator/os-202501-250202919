
# Laporan Praktikum Minggu [1]
Topik: [Arsitektur Sistem Operasi dan Kernel]
---

## Identitas
- **Nama**  : [Aska ASofri Amrillah]  
- **NIM**   : [250202919]  
- **Kelas** : [1IKRA]

---

## Tujuan
mengetahui tentang Arsitektur Sistem Operasi dan Kernel, dan juga pembuatan akun dalam ubuntu
---

## Dasar Teori
  Arsitektur Sistem Operasi dan Kernel
kode/perintah yang digunakan dalam praktikum:
uname -a → identifikasi kernel & arsitektur OS
lsmod | head → modularitas kernel & device driver
dmesg | head → proses booting & logging internal kernel

---

## Langkah Praktikum
1. Langkah-langkah yang dilakukan.  
2. Perintah yang dijalankan.  
3. File dan kode yang dibuat.  
4. Commit message yang digunakan.
   Pertama install ubuntu di microsoft store, jika sudah lalu klik tombol windows+R pada keyboard, lalu masukan kata "cmd".
lalu masukan perintah
wsl  --install  → untuk install ubuntu itu tadi, tunggu sampai selesai.
jika sudan selesai kemudian buat akun di ubuntu dengan kode:
uname -a  → membuat user name saya (aska), lalu masukan pasword, tunggu sampai selesai kemudian masukan kode kedua:
lsmod | head , →  modularitas kernel & device driver, tunggu sampai kode nya selesai, kemudia masukan kode yang ke tiga :
dmesg | head , → proses booting & logging internal kernel, tunggu sampai prosesnya selesai
jika proses yang ketika sudah selesai maka akun yang di baut itu sudah jadi.

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
jawaban:
- 1. lsmod (list modules) berfungsi untuk menampilkan modul-modul yang aktif.
  2. | head: Simbol | (pipe) mengirimkan output dari lsmod ke perintah head, yang kemudian hanya menampilkan 10 baris pertama dari daftar tersebut agar lebih mudah dibaca.
  3. dmesg (display message) mencetak semua pesan yang dihasilkan oleh kernel Linux, terutama selama proses startup (booting). Pesan ini berisi informasi penting tentang perangkat keras yang terdeteksi, driver yang dimuat, dan kesalahan (error) apa pun yang mungkin terjadi.
     | head: Sama seperti sebelumnya, ini membatasi output hanya pada 10 baris pertama, yang biasanya menunjukkan pesan-pesan paling awal saat sistem mulai menyala.
-uname -a → identifikasi kernel & arsitektur OS

lsmod → modularitas kernel & device driver

dmesg → proses booting & logging internal kernel

uname -a → identifikasi kernel & arsitektur OS

lsmod → modularitas kernel & device driver

dmesg → proses booting & logging internal kernel

Dengan memahami outputnya, kita bisa menghubungkan praktik Linux dengan teori inti sistem operasi seperti system call interface, kernel space/user space separation, dan modular kernel design
---

## Kesimpulan
Tuliskan 2–3 poin kesimpulan dari praktikum ini.

---

## Quiz
1. [tiga fungsi utama sistem operasi.]  
   Jawaban:Manajemen Sumber Daya,Menyediakan Antarmuka (Interface) ,Platform untuk Menjalankan Aplikasi
2. [Jelaskan perbedaan antara kernel mode dan user mode.]  
   Jawaban:Kernel mode dan user mode adalah dua mode operasi fundamental dari sebuah CPU yang digunakan oleh sistem operasi untuk melindungi dirinya sendiri dan komponen sistem penting lainnya dari kerusakan yang tidak disengaja oleh program aplikasi.
Perbedaan utamanya terletak pada tingkat hak akses terhadap perangkat keras dan memori sistem.
3. [Sebutkan contoh OS dengan arsitektur monolithic dan microkernel.]  
   Jawaban:Contoh sistem operasi (OS) dengan arsitektur monolitik yaitu Linux dan Windows 9x, sedangkan contoh OS dengan arsitektur mikrokernel adalah QNX, Symbian, dan MINIX. 

---

## Refleksi Diri
Tuliskan secara singkat:
- Apa bagian yang paling menantang minggu ini?  
- Bagaimana cara Anda mengatasinya?  
  Yang paling emnantang di minggu pertama adalah cara memahami penggunaan akun github dan juga cara eksekusi.
  cara saya mengatasinya dangan terus mencoba dan tanya kepada teman yang sudah faham bagaimana cara melakukan nya.
---

**Credit:**  
_Template laporan praktikum Sistem Operasi (SO-202501) – Universitas Putra Bangsa_
