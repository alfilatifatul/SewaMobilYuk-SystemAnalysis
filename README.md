# SewaMobilYuk — System Design & Architecture 🚗

Repository ini isinya dokumen analisis dan perancangan sistem buat aplikasi **SewaMobilYuk** (platform rental mobil online). Semua diagram di sini dibuat sebagai cetak biru (*blueprint*) arsitektur sistem sebelum nanti masuk ke tahap *coding*.

---

## 📌 Status Proyek & Spesifikasi
* **Fase:** Tahap 1 — Analisis & Perancangan Sistem (*System Design*)
* **Metode:** *Object-Oriented Analysis and Design* (OOAD)
* **Tools:** StarUML

---

## 👥 Aktor & Hak Akses Sistem
Biar struktur datanya efisien dan interaksinya gampang, sistem ini dirancang dengan menyatukan aktor utama ke dalam satu peran yang terintegrasi (**User/Pengguna**). Ini detail hak aksesnya:

| Aktor | Peran Utama | Fitur yang Bisa Diakses |
| :--- | :--- | :--- |
| **Pelanggan** *(Customer)* | Pesan layanan sewa mobil secara mandiri. | Cari mobil, reservasi, dan konfirmasi pembayaran. |
| **Admin** | Kelola operasional bisnis & validasi data. | Manajemen data mobil, pantau transaksi, dan verifikasi pembayaran. |

---

## 📊 Rancangan Diagram Sistem

Ini visualisasi alur bisnis dan interaksi sistem yang sudah dimodelkan pakai StarUML:

### 1. Use Case Diagram
Diagram ini memetakan hubungan dan batasan antara pengguna sama fungsi-fungsi utama di sistem SewaMobilYuk. Fokus utamanya ada di manajemen data mobil (armada), proses reservasi, sampai pencatatan transaksi pembayaran.

![Use Case Diagram](usecase-rental.png)

### 2. Activity Diagram
Diagram ini menggambarkan alur kerja pengguna secara visual di dalam sistem biar logika bisnisnya jelas.

> 💡 **Catatan Validasi Sistem:**
> Penanganan alur logika pas proses krusial kayak autentikasi dibuat ketat. Alur "No" (waktu login gagal) terlihat jelas secara visual dengan panah yang balik ke atas (halaman input awal) biar pengguna validasi ulang.

![Activity Diagram](activity-rental.png)


## 🛠️ Rencana Fitur Utama (Scope of Work)
Mengacu ke hasil analisis diagram di atas, ini modul-modul utama yang bakal diimplementasikan pas tahap pengembangan kode nanti:
* **Autentikasi & Otorisasi:** Sistem login terpusat buat User (Pelanggan & Admin).
* **Manajemen Armada:** Fitur CRUD (Create, Read, Update, Delete) data mobil khusus buat Admin.
* **Manajemen Reservasi:** Alur pemesanan mobil secara *real-time* oleh Pelanggan.
* **Sistem Pembayaran:** Pencatatan riwayat transaksi dan konfirmasi pembayaran.
