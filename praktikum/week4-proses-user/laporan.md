
# Laporan Praktikum Minggu [X]
Topik: [manajemen proses dan user linux]

---

## Identitas
- **Nama**  : [aska asofri amrillah]  
- **NIM**   : [250202919]  
- **Kelas** : [1ikra]

---

## Tujuan
1. Menjelaskan konsep proses dan user dalam sistem operasi Linux.
2. Menampilkan daftar proses yang sedang berjalan dan statusnya.
3. Menggunakan perintah untuk membuat dan mengelola user.
4. Menghentikan atau mengontrol proses tertentu menggunakan PID.
5. Menjelaskan kaitan antara manajemen user dan keamanan sistem.

---

## Dasar Teori
Tuliskan ringkasan teori (3–5 poin) yang mendasari percobaan.

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
1. [apa fungsi dari proses init atau systemd dalam system linux?]
   fungsi dari proses init diantarnya:
   - menjalankan proses booting
   - mengtur services dan daemon
   - menentukan run level atau target
   - memantau proses
   - manajemen shutdown dan reboot 
3. [apa perbedaan antara kill dan killall]  
   kill (mengirimkan sinyal ke proses tertentu berdasarkan PID proces ID)
   killall (mengirim signal ke semua proses yang memiliki nama tertentu)
5. [mengapa user root memiliki hak istimewa dalam sistem linux?]  
   user root memiliki hak istimewa karena bertindak sebagai superuser yang mengontrol seluruh sistem, termsuk       file,proses, hardware, dan layanan penting.

---

## Refleksi Diri
Tuliskan secara singkat:
- Apa bagian yang paling menantang minggu ini?  
- Bagaimana cara Anda mengatasinya?  

---

**Credit:**  
_Template laporan praktikum Sistem Operasi (SO-202501) – Universitas Putra Bangsa_
