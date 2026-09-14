# Sistem Informasi Laboratorium (SILAB)

SILAB adalah aplikasi berbasis web yang dirancang untuk mengelola penjadwalan, peminjaman, dan pemantauan aktivitas di laboratorium (khususnya untuk kegiatan praktikum). Sistem ini dibangun untuk mempermudah administrator dalam mengelola jadwal agar tidak terjadi bentrok, memantau penggunaan barang habis pakai (BHP), serta menyediakan akses ke dokumen Standard Operating Procedure (SOP).

## ✨ Fitur Utama

### 1. 📅 Manajemen Jadwal & Peminjaman Lab
- **Dashboard Interaktif**: Menampilkan ringkasan jadwal hari ini, tingkat penggunaan lab (grafik persentase), riwayat peminjaman terbaru, dan log BHP terakhir.
- **Form Peminjaman**: Pengguna dapat memesan jadwal lab dengan menentukan tanggal, waktu mulai dan selesai, mata kuliah, serta tujuan (Praktikum, Penelitian, Ujian, dll).
- **Sistem Status Dinamis**: Setiap peminjaman memiliki siklus status yang jelas:
  - 🟡 **Menunggu (Pending)**
  - 🟢 **Disetujui (Approved)**
  - 🔴 **Ditolak (Rejected)**
  - ⚪ **Dibatalkan (Cancelled)** — Jadwal yang dibatalkan tidak dihapus melainkan disimpan sebagai rekam jejak dan pengingat untuk di-*reschedule*.
- **Filter Fleksibel**: Admin dapat mencari dan menyaring data jadwal berdasarkan tanggal tertentu atau status peminjaman untuk memudahkan pelacakan.

### 2. 🗓️ Kalender Penjadwalan
- Tampilan kalender bulanan yang memudahkan melihat lab mana saja yang sedang dipakai pada tanggal tertentu.
- Sistem indikator titik warna (hijau untuk jadwal aktif, oranye untuk jadwal pending).
- Klik pada tanggal untuk melihat detail rincian praktikum secara *pop-up*.

### 3. 📦 Log Barang Habis Pakai (BHP)
- Pencatatan pemakaian barang-barang di laboratorium (seperti alkohol, masker, sarung tangan, dll).
- Berguna untuk memantau stok dan melacak barang apa saja yang digunakan pada setiap sesi praktikum.

### 4. 📄 Manajemen SOP
- Direktori untuk mengunggah dan mengelola dokumen Standard Operating Procedure (SOP) laboratorium.
- Membantu asisten lab dan mahasiswa untuk dengan mudah mengunduh panduan praktikum sebelum kelas dimulai.

## 🛠️ Teknologi yang Digunakan

- **Backend**: [Django](https://www.djangoproject.com/) (Python)
- **Frontend**: HTML5, CSS3 (Vanilla), dan Vanilla JavaScript
- **Database**: SQLite (default Django, dapat dikonfigurasi ke PostgreSQL/MySQL)

## 🚀 Panduan Instalasi & Menjalankan Lokal

Pastikan komputer Anda sudah terinstal **Python (versi 3.8 atau lebih baru)** dan **Git**.

1. **Clone repository ini:**
   ```bash
   git clone https://github.com/xamiuz/silab.git
   cd silab
   ```

2. **Buat Virtual Environment (Sangat Disarankan):**
   ```bash
   python -m venv env
   
   # Untuk Windows:
   env\Scripts\activate
   
   # Untuk macOS/Linux:
   source env/bin/activate
   ```

3. **Instal dependensi:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Jalankan Migrasi Database:**
   ```bash
   python manage.py makemigrations
   python manage.py migrate
   ```

5. **Buat akun Superuser (Admin):**
   ```bash
   python manage.py createsuperuser
   ```
   *Ikuti instruksi untuk memasukkan username, email, dan password.*

6. **Jalankan Server Lokal:**
   ```bash
   python manage.py runserver
   ```

7. **Akses Aplikasi:**
   Buka browser Anda dan akses: `http://127.0.0.1:8000/`

## 👨‍💻 Kontributor

Proyek ini dikembangkan dan dikelola oleh **[xamiuz](https://github.com/xamiuz)**.

---
*Dibuat untuk mempermudah administrasi laboratorium secara digital.*
