
# Laporan Praktikum Minggu [X]
Topik: [manajemen file dan permission di linux]

---

## Identitas
- **Nama**  : [aska asofri amrillah]  
- **NIM**   : [250202919]  
- **Kelas** : [1ikra]

---

## Tujuan
mahasiswa mampu mengoprasikan perintah linux dasar dengan benar, memahami sistem izin (permission), dan mendokumentasikan hasilnya dalam format laporan git.
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
- navigasi sistem file
  pwd
  ls -1
  cd /tmp
  ls -a
- membaca file
  cat /etc/paswwd | head -n 5
- permission & ownership
  echo "Hello <NAME><NIM>" > percobaan.txt
  ls -l percobaan.txt
  chmod 600 percobaan.txt
  ls -l percobaan.txt

  sudo chown root percobaan.txt
  ls -l percobaan.txt
   

---

## Hasil Eksekusi
Sertakan screenshot hasil percobaan atau diagram:
![Screenshot hasil](screenshots/example.png)

---

## Analisis
- Jelaskan makna hasil percobaan.  
- Hubungkan hasil dengan teori (fungsi kernel, system call, arsitektur OS).  
- Apa perbedaan hasil di lingkungan OS berbeda (Linux vs Windows)?
  analisis
- makna hasil percobaan
  pwd (menampilkan isi folder)
  ls -1 (melihat daftar isi satu baris)
  cd /tmp (pindah ke folder sementara sistem)
  ls -a (melihat semua isi folder)
  
  cat /ets/passwd | head -n 5 (menampilkan isi file yang berisi daftar pengguna, menampilkan 5     baris pertama dari hasil tersebut)
  
  echo "Hello <NAME><NIM>" > percobaan.txt
  ls -l percobaan.txt
  chmod 600 percobaan.txt
  ls -l percobaan.txt
  (memahami cara membuat file, melihat statusnya, dan melindungi file dari akses pengguna lain    dengan pengaturan izin (permission)).

  sudo chown root percobaan.txt  (Mengubah pemilik file menjadi root)
  ls -l percobaan.txt (Melihat status file (izin, pemilik, dll.)

- hubungan dengan (fungsi kernel, system call, arsitektur OS).
  Kernel
  Melakukan semua operasi yang berhubungan dengan file, izin, dan kepemilikan
  System Call
  Menjadi jalur komunikasi antara shell (user space) dan kernel
  Arsitektur OS
  Memisahkan area kerja pengguna (shell) dari area inti (kernel) untuk keamanan dan stabilitas

- perbedaan hasil di lingkungan OS berbeda (Linux vs Windows)
  1. dari aspek filosofi segala sesuatu di linux adalah file sedangkan di windows adalah objek.
  2. dari aspek permission model di linux lebih sederhana (rwx: owner,group,others),  sedangkan      di windows lebih detail (ACL per user atau grop)
  3. dari aspek system call di linux standar industri (posix), sedangkan di windows khusus           windows (win32 API).
  4. Dari kernel linux open source, monolitik sedangkan di windows hybrid, closed source
     
---

## Kesimpulan
Tuliskan 2–3 poin kesimpulan dari praktikum ini.
1. Tujuan Umum Praktik
   Semua perintah (pwd, ls, cd, cat, chmod, chown, dsb.) dapat belajar berinteraksi langsung       antara user dan kernel melalui shell (command line).
2. Proses yang Terjadi di Balik Perintah
   semua perintah yang di jalan kan adalah permintaan ke kernel melalui system call
3. mampu menghubungkan dengan konsep teori OS, jadi mulai memahami perintah dasar linux.

---

## Quiz
1. [apakah fungsi dari perintah chmod?]  
  mengatur izin akses (permissions) untuk pemilik (owner), grup (group), dan pengguna lain       (others) terhadap sebuah file atau folder
2. [apa arti dari kode permission rwxr-xr--?]  
   Kode permission rwxr-xr-- pada Linux/Unix menunjukkan hak akses file untuk tiga kategori        pengguna:
   1. Owner (pemilik) → rwx → boleh baca, tulis, dan eksekusi file.
   2. Group (grup pemilik) → r-x → boleh baca dan eksekusi, tidak bisa menulis.
   3. Others (pengguna lain) → r-- → hanya boleh baca. 
3. [jelaskan perbedaan antara chown dan chmod]  
   - Chown (mengubah siapa yang memiliki file)
   - chmod (mengubah apa yang bisa di lakukan penegguna terhadap file)

---

## Refleksi Diri
Tuliskan secara singkat:
- Apa bagian yang paling menantang minggu ini?  
- Bagaimana cara Anda mengatasinya?  

---

**Credit:**  
_Template laporan praktikum Sistem Operasi (SO-202501) – Universitas Putra Bangsa_
