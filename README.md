# SewaMobilYuk - System Design & Architecture 🚗

Repository ini berisi dokumentasi analisis dan perancangan sistem untuk aplikasi **SewaMobilYuk**, sebuah platform manajemen penyewaan mobil secara online. Dokumentasi ini dibuat sebagai cetak biru (blueprint) arsitektur sistem sebelum masuk ke tahap pengembangan kode (coding).

## 📌 Status Proyek
* **Fase:** Tahap 1 - Analisis & Perancangan Sistem (System Design)
* **Tools Perancangan:** StarUML
* 
## 👥 Aktor Sistem
Untuk menjaga efisiensi jembatan data dan kemudahan interaksi, sistem ini dirancang dengan menyatukan aktor utama ke dalam sebuah peran yang terintegrasi (User/Pengguna), yang nantinya mencakup:
1. **Pelanggan (Customer):** Melakukan pencarian armada, reservasi mobil, dan melakukan konfirmasi pembayaran.
2. **Admin:** Mengelola data ketersediaan mobil (armada), memantau transaksi, dan memverifikasi pembayaran.

---

## 📊 Rancangan Diagram Sistem

Berikut adalah visualisasi alur bisnis dan interaksi sistem yang dirancang menggunakan StarUML:

### 1. Use Case Diagram
Diagram ini memetakan hubungan dan batasan antara pengguna dengan fungsi-fungsi utama yang disediakan oleh sistem SewaMobilYuk, seperti manajemen mobil, pemesanan (reservasi), hingga pencatatan data transaksi pembayaran.

![Use Case Diagram](usecase-rental.png)

### 2. Activity Diagram
Diagram ini menggambarkan alur kerja pengguna secara visual di dalam sistem. Rancangan ini memastikan penanganan alur logika berjalan dengan baik, termasuk kejelasan visual pada alur validasi seperti penanganan skenario "gagal login" yang akan mengarahkan pengguna kembali ke halaman input awal.

![Activity Diagram](activity-rental.png)
