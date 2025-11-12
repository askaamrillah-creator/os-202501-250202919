
# Laporan Praktikum Minggu [2]
Topik: arsitektur sistem oprasi
---

## Identitas
- **Nama**  : [aska asofri amrillah]  
- **NIM**   : [250202919]  
- **Kelas** : [1ikra]

---

## Tujuan
1.Menjelaskan konsep dan fungsi system call dalam sistem operasi.
2.Mengidentifikasi jenis-jenis system call dan fungsinya.
3.Mengamati alur perpindahan mode user ke kernel saat system call terjadi.
4.Menggunakan perintah Linux untuk menampilkan dan menganalisis system call.

---

## Dasar Teori
Arsitektur sistem operasi adalah struktur atau rancangan internal yang menjelaskan bagaimana komponen-komponen OS disusun dan saling berinteraksi untuk mengelola sumber daya komputer (CPU, memori, penyimpanan, perangkat I/O) dan melayani pengguna serta program aplikasi.
Komponen utama dalam arsitektur OS:
1. Kernel
Inti dari sistem operasi — berjalan di “mode kernel”.
Mengontrol semua sumber daya perangkat keras.
Menyediakan layanan dasar seperti:
Manajemen proses
Manajemen memori
Manajemen file system
Manajemen perangkat I/O
Komunikasi antar proses (IPC)
2. System Call Interface (SCI)
“Jembatan” antara program aplikasi dan kernel.
Misalnya saat program butuh membaca file, dia memanggil system call read() ke kernel.
3. User Space / User Interface
Tempat aplikasi pengguna berjalan (misalnya: browser, editor teks).
Termasuk juga shell atau GUI.
4. Device Drivers
Modul/modul yang menghubungkan kernel dengan perangkat keras.
Contoh: driver printer, keyboard, disk, jaringan.
5. File System
Mengatur cara data disimpan dan diakses di media penyimpanan.

---

## Langkah Praktikum
1. menjalankan perintah dengan menggunakan software ubuntu.  
2. Perintah yang dijalankan.
   strace ls
   strace -e trace=open, read, write, close cat /etc/passwd
   dmesg | tail -n 10
4. File dan kode yang dibuat.
   
6. Commit message yang digunakan.

---

## Kode / Perintah
Tuliskan potongan kode atau perintah utama:
strace ls
strace -e trace=open, read, write, close cat /etc/passwd
dmesg | tail -n 10

---
## Hasil Eksekusi
Sertakan screenshot hasil percobaan atau diagram:
![Screenshot hasil](screenshots/example.png)

---

## Analisis
- Jelaskan makna hasil percobaan.  
- Hubungkan hasil dengan teori (fungsi kernel, system call, arsitektur OS).  
- Apa perbedaan hasil di lingkungan OS berbeda (Linux vs Windows)?
  
- makna hasil percobaan
  strace (Menangkap system calls (panggilan ke kernel) dan sinyal yang diterima/diterbitkan  proses.)
  strace → alat untuk menelusuri system call yang dipanggil program.
-e trace=open,read,write,close → hanya tampilkan empat system call ini:
open / openat: membuka file
read: membaca isi file
write: menulis data (biasanya ke layar / stdout)
close: menutup file
cat /etc/passwd → program cat menampilkan isi file /etc/passwd.
dmesg	Menampilkan pesan kernel ring buffer — log internal dari kernel Linux tentang perangkat keras, driver, dan aktivitas sistem.
`	` (pipe)
tail -n 10	Menampilkan 10 baris terakhir dari input yang diterimanya.

- Hubungkan hasil dengan teori (fungsi kernel, system call, arsitektur OS).
  strace → menampilkan interaksi user program dengan kernel melalui system call.
dmesg → menampilkan aktivitas kernel dalam mengelola perangkat keras.
Bersama-sama → membuktikan teori arsitektur OS: user space berinteraksi dengan kernel, kernel mengelola hardware, semua diatur agar sistem berjalan aman dan efisien.

- Apa perbedaan hasil di lingkungan OS berbeda (Linux vs Windows)?
Linux: system call lebih transparan dan langsung terlihat dengan strace.
Windows: system call lebih abstrak, perlu tools tambahan (ProcMon, WinDbg) untuk melihat detail serupa.
---

## Kesimpulan
System call (strace) → menampilkan bukti interaksi program user space dengan kernel (file I/O, proses, dll.).
Kernel log (dmesg) → menampilkan aktivitas kernel dalam mengelola perangkat keras dan sistem, membantu debugging.
Arsitektur OS universal: user space → kernel → hardware tetap sama, tapi implementasi dan tools berbeda antara Linux dan Windows.
Praktik & teori saling mendukung: Dengan strace dan dmesg, kita bisa melihat secara nyata bagaimana arsitektur OS bekerja di level kernel dan system call.
---

## Quiz
1. [apa fungsi utama system call dalam sistem oprasi?]  
  Fungsi utama system call dalam sistem operasi sangat fundamental, karena mereka menjadi jembatan antara program (user space) dan kernel (kernel space).
2. [sebutkan 4 katagori system call yang umum digunakan]  
   1.manajemen proses
   2.manajemen file
   3.manajemen memori
   4.kontrol sistem
3. [mengapa system call tidak bisa di panggil langsung oleh system program]  
   System call tidak bisa dipanggil langsung karena user program berjalan di user space, bukan kernel space.

---

## Refleksi Diri
Tuliskan secara singkat:
- Apa bagian yang paling menantang minggu ini?  
- Bagaimana cara Anda mengatasinya?
  

---

**Credit:**  
_Template laporan praktikum Sistem Operasi (SO-202501) – Universitas Putra Bangsa_
