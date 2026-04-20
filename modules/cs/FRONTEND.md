# Module [CUSTOMER SERVICE (CS)] - Implementation Checklist

## 1. Dashboard CS (`/cs`)
- [/] **A. Portal & Kerangka Dashboard**
    - [x] **Frontend**: Layout Dasar CS Portal (Premium Theme).
    - [x] **Frontend**: Sidebar & Navigation Staff.
    - [x] **Backend**: Proteksi Rute Staff (RBAC Middleware).
- [ ] **B. Notifikasi Pesanan Khusus**
    - [ ] **Frontend**: List "Urgent Requests" dari alur WhatsApp.
    - [ ] **Backend**: Penarikan data pesanan dengan flag `SPECIAL_ORDER`.

## 2. Daily Scheduler (`/cs/scheduler`)
- [ ] **A. Form Input Menu Harian**
    - [x] **Frontend**: Brand-Aligned Form (Nama, Harga, Kategori).
    - [ ] **Frontend**: Komponen Image Picker (Foto Menu).
    - [ ] **Frontend**: Field "Keterangan Tambahan CS".
    - [ ] **Backend**: Script Image Compression & Conversion (WebP).
    - [ ] **Backend**: Proses `UPSERT` data ke tabel DailySchedules.

## 3. Order Monitor (`/cs/orders`)
- [x] **A. Live Order Table**
    - [x] **Frontend**: Tabel interaktif dengan filter Status & Pencarian.
    - [x] **Frontend**: Komponen "Badge Status" (OrderStatusBadge).
    - [ ] **Backend**: Query join `Orders` + `Users` + `OrderItems`.
- [ ] **B. Cetak Rekap Dapur**
    - [ ] **Frontend**: Tombol "Print Rekap" (Print-friendly CSS).
    - [ ] **Backend**: Aggregasi total menu (Contoh: "Total Nasi Ayam: 50 kotak").

## 4. Payment & Management (`/cs/payments`)
- [ ] **A. Verifikasi Pembayaran**
    - [ ] **Frontend**: Galeri Bukti Transfer (Zoom-in modal).
    - [ ] **Frontend**: Tombol Konfirmasi Pembayaran.
    - [ ] **Backend**: Logic update `payment_status` dan `order_status`.
- [ ] **B. Input Akun Instansi Manual**
    - [ ] **Frontend**: Form Pembuatan User (Username, Pass, Dept).
    - [ ] **Backend**: Logic registrasi user oleh CS (Bypass pending status).
