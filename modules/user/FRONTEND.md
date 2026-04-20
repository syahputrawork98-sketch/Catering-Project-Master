# Module [USER / CUSTOMER] - Implementation Checklist

## 1. Login & Registration
- [x] **A. Proses Pendaftaran**
    - [x] **Frontend**: Form input (Nama, No Telp, Pass) dengan Svelte 5 Runes.
    - [x] **Frontend**: Dropdown pilihan "Instansi vs Umum".
    - [x] **Backend**: Validasi duplikasi nomor telepon (Database unique constraint).
    - [x] **Backend**: Password Hashing (Argon2id).
- [x] **B. Proses Login**
    - [x] **Frontend**: Form login & Feedback error.
    - [x] **Backend**: JWT Session Management (Auth.js Strategy: JWT).

## 2. Dashboard Catalog (`/dashboard`)
- [x] **A. Katalog Menu Harian**
    - [x] **Frontend**: UI Framework & Grid System (High-Aesthetic).
    - [x] **Frontend**: Sidebar Navigation (Orders, Menu, Profile) - *Ready*.
    - [x] **Frontend**: Premium Card Menu (Foto, Nama, Info Stok).
    - [ ] **Backend**: Query menu `available_date = TODAY`.
- [x] **B. Sistem Keranjang**
    - [x] **Frontend**: Sidebar Cart Drawer (Sliding UI - High-End).
    - [x] **Frontend**: Sinkronisasi LocalStorage (Persistent Store).
    - [ ] **Backend**: Validasi stok sisa di server saat klik "Add to Cart".

## 3. Checkout & Payment (`/dashboard/checkout`)
- [x] **A. Finalisasi Checkout**
    - [x] **Frontend**: Rincian Biaya (Total Harga Pokok + PPN).
    - [x] **Frontend**: Tombol "Konfirmasi Pesanan" (Premium Layout).
    - [ ] **Backend**: Store `price_snapshot` dan `tax_snapshot`.
    - [ ] **Backend**: Update stok otomatis (PostgreSQL Transaction).

## 4. Tracking & History (`/dashboard/orders`)
- [x] **A. Monitoring Status Aktif**
    - [x] **Frontend**: Visual Stepper (Ordered -> Paid -> Delivered).
    - [x] **Frontend**: Status Badge dinamis (OrderStatusBadge).
    - [ ] **Frontend**: Tombol "Download Bon PDF" (Planned).
- [x] **B. Riwayat Belanja (History)**
    - [x] **Frontend**: Premium Card List (Gourmet Aesthetic).
    - [ ] **Backend**: Query riwayat per `user_id`.
