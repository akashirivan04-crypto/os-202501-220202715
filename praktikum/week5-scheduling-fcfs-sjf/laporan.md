
# Laporan Praktikum Minggu [5]
Topik: [Penjadwalan CPU – FCFS dan SJF]

---

## Identitas
- **Nama**  : [Rivan Ahmad Ardiansyah]  
- **NIM**   : [220202715]  
- **Kelas** : [1 IKRB]

---

## Tujuan
Tuliskan tujuan praktikum minggu ini.  
> Mahasiswa akan mempelajari algoritma penjadwalan CPU (CPU Scheduling) menggunakan dua pendekatan dasar:

1. FCFS (First Come First Served)
2. SJF (Shortest Job First)

---

## Dasar Teori
Tuliskan ringkasan teori (3–5 poin) yang mendasari percobaan.
1. Menghitung waiting time dan turnaround time untuk algoritma FCFS dan SJF.
2. Menyajikan hasil perhitungan dalam tabel yang rapi dan mudah dibaca.
3. Membandingkan performa FCFS dan SJF berdasarkan hasil analisis.

---

## Langkah Praktikum
1. Siapkan Data Proses Gunakan tabel proses
2. Eksperimen 1 – FCFS (First Come First Served) 
3. Eksperimen 2 – SJF (Shortest Job First)
4. CEksperimen 3 – Visualisasi Spreadsheet (Opsional)
5. Analisis



---

## Kode / Perintah
Tuliskan potongan kode atau perintah utama:
```bash
Waiting Time (WT) = waktu mulai eksekusi - Arrival Time
Turnaround Time (TAT) = WT + Burst Time
| P1 | P2 | P3 | P4 |
0    6    14   21   24
---

## Hasil Eksekusi
Sertakan screenshot hasil percobaan atau diagram:
![Screenshot hasil](screenshots/example.png)

---

## Analisis
- Jelaskan makna hasil percobaan.  
>SJF terbukti lebih efisien (waktu tunggu rata-rata 6.25) dibandingkan FCFS (8.75) untuk data ini, karena SJF memprioritaskan tugas-tugas pendek sehingga mengurangi waktu tunggu total dalam antrian.
- Hubungkan hasil dengan teori (fungsi kernel, system call, arsitektur OS).  
>Keputusan penjadwalan (seperti FCFS dan SJF) adalah fungsi utama dari CPU Scheduler di Kernel Sistem Operasi yang bekerja dengan data PCB dan dipicu oleh System Call untuk menentukan proses mana yang menggunakan CPU.
- Apa perbedaan hasil di lingkungan OS berbeda (Linux vs Windows)?  
>Perbedaan hasil penjadwalan antara Linux (menggunakan CFS yang fokus pada keadilan) dan Windows (menggunakan penjadwalan berbasis prioritas) disebabkan oleh algoritma kernel yang berbeda, di mana Windows memprioritaskan responsivitas foreground sementara Linux menargetkan distribusi waktu CPU yang merata.

---

## Kesimpulan
Tuliskan 2–3 poin kesimpulan dari praktikum ini.
>Tujuan utamanya adalah memahami bagaimana sistem operasi menentukan urutan eksekusi proses, serta bagaimana waiting time dan turnaround time memengaruhi performa sistem.

Mahasiswa akan melakukan simulasi dan perbandingan hasil perhitungan kedua algoritma ini menggunakan tabel observasi manual atau spreadsheet (Excel/Google Sheets) — tanpa perlu melakukan instalasi atau pemrograman tambahan.

---

## Quiz
1. [Apa perbedaan utama antara FCFS dan SJF?]  
   **Jawaban:Perbedaan utama antara FCFS dan SJF adalah kriteria penjadwalan: FCFS mengeksekusi proses berdasarkan urutan kedatangan (siapa yang datang duluan), sedangkan SJF mengeksekusi proses berdasarkan waktu eksekusi terpendek**  
2. [Mengapa SJF dapat menghasilkan rata-rata waktu tunggu minimum?]  
   **Jawaban:SJF menghasilkan rata-rata waktu tunggu minimum karena selalu memprioritaskan penyelesaian proses terpendek lebih dulu, yang secara efektif meminimalkan waktu tunggu untuk proses-proses pendek dan menggeser waktu tunggu yang besar hanya kepada proses yang sudah panjang.**  
3. [Apa kelemahan SJF jika diterapkan pada sistem interaktif?]  
   **Jawaban:Kelemahan SJF pada sistem interaktif adalah risiko starvation (kelaparan) pada proses yang lebih panjang karena selalu mendahulukan proses interaktif yang sangat singkat.**  

---

## Refleksi Diri
Tuliskan secara singkat:
- Apa bagian yang paling menantang minggu ini?  
>saat melakukan pengerjaan
- Bagaimana cara Anda mengatasinya?  
>bertanya dengan ahlimya

---

**Credit:**  
_Template laporan praktikum Sistem Operasi (SO-202501) – Universitas Putra Bangsa_
