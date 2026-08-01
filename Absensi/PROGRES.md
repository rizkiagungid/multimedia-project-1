# [cite_start]📌 Project Context: Website Absensi MM2 (SMAN 01 TAMANSARI) [cite: 83]

## 🎯 Visi & Tujuan
* [cite_start]Membangun sistem web terintegrasi dengan identitas QR Code pada ID Card siswa[cite: 58].
* [cite_start]Mencatat kehadiran siswa secara otomatis, akurat, dan bebas dari manipulasi data[cite: 3, 58, 59].
* [cite_start]Mempercepat proses *check-in* menggunakan pemindaian identitas dalam hitungan detik[cite: 58].

## 🛠️ Tech Stack & Pendekatan
* [cite_start]**Backend Framework:** Laravel[cite: 5].
* [cite_start]**Admin Panel & UI:** Filament v5 [cite: 8] (Dibangun di atas ekosistem TALL Stack: Tailwind CSS, Alpine.js, Livewire, Laravel) [cite_start][cite: 98].
* [cite_start]**Database:** SQLite[cite: 5].
* [cite_start]**Frontend Scanner:** Library JavaScript `html5-qrcode`[cite: 14].
* [cite_start]**Pendekatan Arsitektur:** *Filament-centric*, yang berarti seluruh logika aplikasi (termasuk halaman pemindai kamera) menyatu penuh di dalam ekosistem Filament dan Livewire tanpa harus membangun *route* API yang terpisah[cite: 12, 32].

## 🗄️ Skema Database (Tahap 1 - Selesai)
[cite_start]Ketiga tabel di bawah ini telah berhasil dimigrasi dan saling terhubung menggunakan *Foreign Key Constraint* (`constrained()`) untuk menjaga integritas relasi antar data[cite: 5, 7].
* [cite_start]**Siswa:** Memiliki kolom `id`, `nisn`, dan `nama`[cite: 46].
* [cite_start]**Pertemuan:** Memiliki kolom `id`, `tanggal`, `jam_mulai`, dan `tolerance_time`[cite: 46].
* [cite_start]**LogAbsen:** Memiliki kolom `id`, `siswa_id`, `pertemuan_id`, `waktu_scan`, dan `status`[cite: 46].

## ⚙️ Struktur Filament Admin Panel (Tahap 2 & 3 - Selesai)
* [cite_start]**Resource Data:** Telah di-generate `SiswaResource`, `PertemuanResource`, dan `LogAbsenResource`[cite: 8].
* [cite_start]**Lokalisasi Bahasa:** Menggunakan properti `$pluralModelLabel` untuk mengubah penamaan bahasa Inggris bawaan menjadi bahasa Indonesia[cite: 10].
* [cite_start]**Tampilan Relasi:** Pilihan menu *dropdown* pada Log Absen telah disesuaikan agar menampilkan informasi yang deskriptif seperti tanggal pertemuan[cite: 11].
* [cite_start]**Halaman Frontend:** Telah dibuat Custom Page mandiri bernama `ScanQR` untuk menampung antarmuka kamera pemindai[cite: 13].

## 🚀 Logika Back-End Pemindai (Tahap 4 - Sedang Dikerjakan)
[cite_start]Halaman Custom Page `ScanQR` bertindak sebagai *Livewire Component* seutuhnya[cite: 13, 71]. [cite_start]JavaScript `html5-qrcode` bertugas menangkap kode dari kamera dan langsung memanggil metode PHP di latar belakang menggunakan perintah `$wire.prosesScan(decodedText)`[cite: 14, 38].

**Algoritma Validasi Fungsi `prosesScan($nisn)`:**
1.  [cite_start]**Cek Validitas Siswa:** Mengecek apakah `$nisn` hasil pindaian terdaftar secara sah di dalam tabel `Siswa`[cite: 25].
2.  [cite_start]**Cek Sesi Aktif:** Mencari data `Pertemuan` mana yang sedang aktif untuk hari ini[cite: 25].
3.  **Kalkulasi Waktu & Penentuan Status:**
    * [cite_start]Mencatat `waktu_scan` pada detik pemindaian terjadi[cite: 26].
    * [cite_start]Sistem menghitung batas waktu dengan rumus: `Batas Toleransi` = `jam_mulai` + `tolerance_time`[cite: 26].
    * [cite_start]Jika `waktu_scan` <= `Batas Toleransi` $\rightarrow$ Status diatur menjadi **Hadir**[cite: 27].
    * [cite_start]Jika `waktu_scan` > `Batas Toleransi` $\rightarrow$ Status diatur menjadi **Terlambat**[cite: 27].
4.  [cite_start]**Umpan Balik (Real-time Feedback):** Mengembalikan respons notifikasi sukses atau gagal langsung ke layar Filament Admin tanpa memerlukan *reload* halaman[cite: 77, 80].

## 📋 To-Do List Target Berikutnya
* [cite_start]Menulis secara lengkap logika backend fungsi `$wire.prosesScan` di dalam file komponen `ScanQR.php`[cite: 38].
* [cite_start]Membuat generator gambar QR Code di halaman `SiswaResource` dengan mengandalkan library pihak ketiga seperti `bacon/bacon-qr-code` atau `simplesoftwareio/laravel-qrcode`[cite: 27].