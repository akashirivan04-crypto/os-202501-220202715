
# Laporan Praktikum Minggu [X]
Topik: [Tuliskan judul topik, misalnya "Arsitektur Sistem Operasi dan Kernel"]

---

## Identitas
- **Nama**  : [Rivan Ahmad Ardiansyah]
- **NIM**   : [220202715]  
- **Kelas** : [1 IKRB]

---

## Tujuan

Tuliskan tujuan praktikum minggu ini.

Tujuan utama dari praktikum ini adalah agar mahasiswa mampu mengoperasikan perintah Linux dasar dengan benar, memahami sistem izin (permission), dan mendokumentasikan hasilnya dalam format laporan Git.

---

## Dasar Teori
Tuliskan ringkasan teori (3–5 poin) yang mendasari percobaan.
1. Menggunakan perintah ls, pwd, cd, cat untuk navigasi file dan direktori.
2. Menggunakan chmod dan chown untuk manajemen hak akses file.
3. Menjelaskan hasil output dari perintah Linux dasar.

---

## Langkah Praktikum
1. Setup Environment

Gunakan Linux (Ubuntu/WSL).
Pastikan folder kerja berada di dalam direktori repositori Git praktikum:
praktikum/week3-linux-fs-permission/
Eksperimen 1 – Navigasi Sistem File Jalankan perintah berikut:

pwd
ls -l
cd /tmp
ls -a
Jelaskan hasil tiap perintah.
Catat direktori aktif, isi folder, dan file tersembunyi (jika ada).
Eksperimen 2 – Membaca File Jalankan perintah:

cat /etc/passwd | head -n 5
Jelaskan isi file dan struktur barisnya (user, UID, GID, home, shell).
Eksperimen 3 – Permission & Ownership Buat file baru:

echo "Hello <NAME><NIM>" > percobaan.txt
ls -l percobaan.txt
chmod 600 percobaan.txt
ls -l percobaan.txt
Analisis perbedaan sebelum dan sesudah chmod.
Ubah pemilik file (jika memiliki izin sudo):
sudo chown root percobaan.txt
ls -l percobaan.txt
Catat hasilnya.
Eksperimen 4 – Dokumentasi

Ambil screenshot hasil terminal dan simpan di:
praktikum/week3-linux-fs-permission/screenshots/
Tambahkan analisis hasil pada laporan.md.
Commit & Push

git add .
git commit -m "Minggu 3 - Linux File System & Permission"
git push origin main

---

## Kode / Perintah
Tuliskan potongan kode atau perintah utama:
pwd
ls -l
cd /tmp
ls -a
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
untuk mempelajari pengelolaan file dan direktori menggunakan perintah dasar Linux.
agar mengoperasikan perintah Linux dasar dengan benar

---

## Quiz
1. [Apa fungsi dari perintah chmod?]  
   **Jawaban:Fungsi dari perintah chmod adalah untuk mengubah hak akses (izin) pengguna (pemilik, grup, atau lainnya) terhadap sebuah file atau direktori di sistem operasi berbasis Unix/Linux.**  
2. [Apa arti dari kode permission rwxr-xr--?]  
   **Jawaban:Kode permission rwxr-xr-- berarti pemilik memiliki hak baca, tulis, dan eksekusi (rwx), grup hanya memiliki hak baca dan eksekusi (r-x), dan pengguna lain hanya memiliki hak baca (r--).**  
3. [Jelaskan perbedaan antara chown dan chmod.]  
   **Jawaban:chown digunakan untuk mengubah kepemilikan berkas (siapa pemilik dan grupnya), sementara chmod digunakan untuk mengubah izin akses berkas (apa yang boleh dilakukan oleh pemilik, grup, dan lainnya: baca, tulis, eksekusi).**  

---

## Refleksi Diri
Tuliskan secara singkat:
- Apa bagian yang paling menantang minggu ini?  
bagian linuxnya
- Bagaimana cara Anda mengatasinya?  
mengikuti alur perintah dengan teliti

---

**Credit:**  
_Template laporan praktikum Sistem Operasi (SO-202501) – Universitas Putra Bangsa_
