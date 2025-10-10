
# Laporan Praktikum Minggu [X]
Topik: "Arsitektur Sistem Operasi dan Kernel"

---

## Identitas
- **Nama**  : Rivan Ahmad Ardiansyah
- **NIM**   : 220202715 
- **Kelas** : 1 IKRB

---

## Tujuan
 Menjelaskan peran sistem operasi dalam arsitektur komputer

---

## Dasar Teori
Perbedaan mode eksekusi kernel mode dan user mode.
Mekanisme system call (panggilan sistem).
Perbandingan model arsitektur OS seperti monolithic kernel, layered approach, dan microkernel.

---

## Langkah Praktikum
1. Setup Environment

Pastikan Linux (Ubuntu/WSL) sudah terinstal.
Pastikan Git sudah dikonfigurasi dengan benar:
git config --global user.name "Nama Anda"
git config --global user.email "email@contoh.com"

2. Diskusi Konsep

Baca materi pengantar tentang komponen OS.
Identifikasi komponen yang ada pada Linux/Windows/Android.

3. Eksperimen Dasar Jalankan perintah berikut di terminal:

uname -a
whoami
lsmod | head
dmesg | head
Catat dan analisis modul kernel yang tampil.

4. Membuat Diagram Arsitektur

Buat diagram hubungan antara User → System Call → Kernel → Hardware.
Gunakan draw.io atau Mermaid.
Simpan hasilnya di:
praktikum/week1-intro-arsitektur-os/screenshots/diagram-os.png

5. Penulisan Laporan

Tuliskan hasil pengamatan, analisis, dan kesimpulan ke dalam laporan.md.
Tambahkan screenshot hasil terminal ke folder screenshots/.

6. Commit & Push

git add .
git commit -m "Minggu 1 - Arsitektur Sistem Operasi dan Kernel"
git push origin main
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
![Screenshot hasil](./screenshots/week1-into-arsitektur-os.pngg)

---

## Analisis
- Jelaskan makna hasil percobaan. 
  
 uname -a (Identitas Sistem)
Perintah ini berfungsi sebagai kartu identitas lengkap dari sistem Anda. Hasilnya memberitahu Anda nama inti sistem operasi (Kernel Linux), versi kernel yang spesifik (misalnya, 5.15.0), dan arsitektur perangkat keras (misalnya, x86_64 untuk 64-bit). Maknanya adalah Anda bisa memastikan kompatibilitas driver atau perangkat lunak yang Anda coba instal.

whoami (Identitas Pengguna)
Makna dari perintah ini sangat langsung: ia mengonfirmasi siapa Anda dalam konteks sistem. Hasilnya menampilkan nama akun pengguna yang sedang menjalankan sesi saat itu. Hal ini sangat penting untuk mengetahui tingkat hak akses yang Anda miliki—apakah Anda pengguna biasa atau memiliki hak administrator penuh (root).

lsmod | head (Driver Kernel Aktif)
Perintah ini memberikan cuplikan tentang komponen perangkat keras utama apa saja yang sedang didukung dan aktif saat ini. Hasilnya adalah daftar modul kernel (atau driver) yang dimuat ke memori. Misalnya, Anda akan melihat modul untuk kartu suara atau jaringan. Maknanya adalah Anda dapat memverifikasi apakah driver penting seperti audio atau Wi-Fi telah dimuat dengan benar.

dmesg | head (Riwayat Boot)
Perintah ini adalah log awal sistem Anda, menampilkan pesan yang dikumpulkan kernel sejak komputer dinyalakan. Hasilnya mencakup informasi tentang deteksi hardware, inisialisasi CPU, dan detail proses startup. Maknanya adalah alat diagnostik utama untuk melacak dan mendiagnosis kegagalan yang mungkin terjadi pada tahap boot awal sebelum sistem logging biasa dimulai. 
- Hubungkan hasil dengan teori (fungsi kernel, system call, arsitektur OS).  

System Call: Seberapa sering programmu mengetuk pintu gerbang untuk meminta layanan. Semakin sering, semakin besar biaya perpindahan mode .

Fungsi Kernel: Seberapa bagus inti OS mengelola sumber daya (I/O, CPU, Memori) setelah pintu dibuka. Kinerja buruk = fungsi kernel lelet.

Arsitektur OS: Apakah kesalahan fatal pada satu bagian merusak seluruh sistem atau hanya komunikasi antar layanan yang melambat .
- Apa perbedaan hasil di lingkungan OS berbeda (Linux vs Windows)?  
  
 1. File Naming 
Linux: Sensitif Huruf Besar/Kecil (Data.txt 

= data.txt). Jika kode Anda salah kapitalisasi, program akan gagal.
Windows: Tidak Sensitif Huruf Besar/Kecil (Data.txt ≈ data.txt). Lebih pemaaf.

2. Kinerja & Stabilitas 
Linux: Lebih cepat dan stabil untuk server dan komputasi berat karena kernel-nya lebih ramping dan manajemen memorinya efisien.
Windows: Cenderung lebih berat dan dapat melambat dari waktu ke waktu karena banyak layanan berjalan di latar belakang.

3. Keamanan & Izin 
Linux: Sistem izin sangat ketat (sudo diperlukan). Program lebih sulit merusak sistem secara tidak sengaja.
Windows: Izin pengguna secara historis lebih longgar, membuat sistem lebih rentan terhadap malware.

---

## Kesimpulan
1. OS itu Sang Kepala Sekolah, Kernel adalah Staf Inti: Sistem Operasi (OS) bertindak sebagai manajer utama, memastikan semua perangkat keras (CPU, memori, printer) bisa dipakai bergantian dan adil oleh semua program. 

2. Pembagian Kewenangan (Mode Kernel vs. Mode Pengguna): Ada dua tingkat izin dalam sistem: Mode Kernel dan Mode Pengguna. Kernel bekerja di Mode Kernel, yang berarti ia punya akses dan kendali penuh terhadap semua sumber daya dan perintah. 

3. Filosofi Struktur: Monolitik vs. Mikrokernel: Arsitektur Kernel bukanlah satu jenis saja. Ada dua pendekatan utama:
Monolitik: Semua layanan inti (manajemen file, driver) ada di dalam Kernel itu sendiri. Ini membuatnya cepat tapi sulit diperbaiki atau dimodifikasi karena semua terikat jadi satu.
Mikrokernel: Hanya fungsi paling dasar yang ada di Kernel. Layanan lain dipindahkan ke luar (ruang pengguna) sebagai modul terpisah. Ini membuatnya lebih stabil dan fleksibel karena jika satu layanan rusak, Kernel dan layanan lainnya tetap berjalan, meski kinerjanya bisa sedikit lebih lambat.

---

## Quiz
1. Sebutkan tiga fungsi utama sistem operasi. 
   
a. Manajemen Proses
Sistem operasi bertanggung jawab untuk mengelola semua proses yang berjalan di dalam sistem. Fungsi ini meliputi penjadwalan proses, pengalokasian sumber daya, dan pengawasan status proses. Proses adalah unit dasar eksekusi dalam sistem komputer, dan sistem operasi memastikan bahwa setiap proses memperoleh sumber daya yang dibutuhkan seperti CPU, memori, dan I/O dengan efisien.

b. Manajemen Memori
Memori adalah komponen penting dalam sistem komputer, dan sistem operasi bertugas untuk mengelola memori dengan efisien. Fungsi manajemen memori mencakup pengalokasian memori untuk proses yang berjalan, pengaturan kapasitas memori, serta pengelolaan memori virtual.

c. Manajemen File
Manajemen file adalah fungsi lain yang penting dari sistem operasi. Ini mencakup penciptaan, penghapusan, pembacaan, dan penulisan file, serta pengelolaan struktur direktori.

2. Jelaskan perbedaan antara kernel mode dan user mode.

Kernel Mode (Mode Istimewa):

Kekuasaan Penuh: Kode yang berjalan di sini (inti OS dan driver penting) memiliki hak akses tak terbatas. Mereka bisa mengakses semua hardware dan memori sistem secara langsung.

Risiko Tinggi: Jika terjadi kesalahan (bug atau crash) di mode ini, seluruh sistem operasi akan lumpuh.

User Mode (Mode Terbatas):

Kekuasaan Terbatas: Semua aplikasi biasa  berjalan di sini. Mereka tidak bisa mengakses hardware atau memori inti OS secara langsung.

Keamanan: Jika sebuah aplikasi crash di mode ini, OS hanya mematikan aplikasi itu saja, dan sistem akan tetap berjalan stabil.
3. Sebutkan contoh OS dengan arsitektur monolithic dan microkernel.

Linux, MS-DOS, Unix
 

---

## Refleksi Diri
Tuliskan secara singkat:
- Apa bagian yang paling menantang minggu ini?  
- ( ketika menginstall wsl bikin pusing )
- Bagaimana cara Anda mengatasinya?  
- ( dengan cara melihat tutorial di youtube dan bertanya kepada teman )

---

**Credit:**  
_Template laporan praktikum Sistem Operasi (SO-202501) – Universitas Putra Bangsa_
