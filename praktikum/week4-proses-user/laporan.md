
# Laporan Praktikum Minggu [4]
Topik: [Manajemen Proses dan User di Linux]

---

## Identitas
- **Nama**  : [Rivan Ahmad Ardiansyah]  
- **NIM**   : [220202715]  
- **Kelas** : [1 IKRB]

---

## Tujuan
Tuliskan tujuan praktikum minggu ini.   
> Menjelaskan konsep proses dan user dalam sistem operasi Linux.

---

## Dasar Teori
Tuliskan ringkasan teori (3–5 poin) yang mendasari percobaan.
>1. Membuat dan mengatur proses (process management).
Mengelola user, group, serta hak akses pengguna.
2. Menampilkan, menghentikan, dan mengontrol proses yang sedang berjalan.
3. Menghubungkan konsep user management dengan keamanan sistem operasi.

---

## Langkah Praktikum
1. Tugas ini, mahasiswa mampu:

Menjelaskan konsep proses dan user dalam sistem operasi Linux.
Menampilkan daftar proses yang sedang berjalan dan statusnya.
Menggunakan perintah untuk membuat dan mengelola user.
Menghentikan atau mengontrol proses tertentu menggunakan PID.
Menjelaskan kaitan antara manajemen user dan keamanan sistem.
C. Langkah Pengerjaan
Setup Environment

Gunakan Linux (Ubuntu/WSL).
Pastikan Anda sudah login sebagai user non-root.
Siapkan folder kerja:
praktikum/week4-proses-user/
Eksperimen 1 – Identitas User Jalankan perintah berikut:

whoami
id
groups
Jelaskan setiap output dan fungsinya.
Buat user baru (jika memiliki izin sudo):
sudo adduser praktikan
sudo passwd praktikan
Uji login ke user baru.
Eksperimen 2 – Monitoring Proses Jalankan:

ps aux | head -10
top -n 1
Jelaskan kolom penting seperti PID, USER, %CPU, %MEM, COMMAND.
Simpan tangkapan layar top ke:
praktikum/week4-proses-user/screenshots/top.png
Eksperimen 3 – Kontrol Proses

Jalankan program latar belakang:
sleep 1000 &
ps aux | grep sleep
Catat PID proses sleep.
Hentikan proses:
kill <PID>
Pastikan proses telah berhenti dengan ps aux | grep sleep.
Eksperimen 4 – Analisis Hierarki Proses Jalankan:

pstree -p | head -20
Amati hierarki proses dan identifikasi proses induk (init/systemd).
Catat hasilnya dalam laporan.

---

## Kode / Perintah
Tuliskan potongan kode atau perintah utama:
```bash
whoami
id
groups
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
1. Mempelajari konsep proses dan manajemen user dalam sistem operasi Linux.
2. ksperimen dilakukan melalui penggunaan perintah dasar seperti ps, top, kill, adduser, passwd, id, dan groups.

---

## Quiz
1. [Apa fungsi dari proses init atau systemd dalam sistem Linux?]  
   **Jawaban:Fungsi utama dari proses init atau systemd dalam sistem Linux adalah sebagai proses pertama (PID 1) yang dijalankan oleh kernel untuk menginisialisasi sistem dan bertindak sebagai manajer layanan yang memulai, mengawasi, dan menghentikan semua layanan sistem lainnya.**  
2. [Apa perbedaan antara kill dan killall?]  
   **Jawaban:Perbedaan utamanya adalah kill menghentikan proses tunggal berdasarkan ID Proses (PID), sedangkan killall menghentikan semua proses yang berjalan berdasarkan nama perintah program tersebut.**  
3. [Mengapa user root memiliki hak istimewa di sistem Linux?]  
   **Jawaban:User root memiliki hak istimewa di sistem Linux karena ia adalah Super User atau administrator utama yang memiliki kontrol penuh dan tak terbatas untuk menjalankan tugas-tugas kritis pada seluruh sistem.**  

---

## Refleksi Diri
Tuliskan secara singkat:
- Apa bagian yang paling menantang minggu ini?  
lumayan rumit eksperimennya
- Bagaimana cara Anda mengatasinya?  
dijalani dengan santai
---

**Credit:**  
_Template laporan praktikum Sistem Operasi (SO-202501) – Universitas Putra Bangsa_
