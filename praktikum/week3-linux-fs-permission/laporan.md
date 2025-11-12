
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
  (memahami cara membuat file, melihat statusnya, dan melindungi file dari akses pengguna lain dengan pengaturan izin (permission)).

  
  

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
