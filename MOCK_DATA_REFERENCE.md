# 🧠 Gourmet Hub: Mock Data Reference (Brain Component)

Dokumen ini adalah referensi cepat untuk data yang telah diisi (*seeded*) ke dalam sistem. Gunakan data ini untuk pengujian fungsionalitas dan verifikasi halaman **Reporting**.

---

## 👥 Akun & Kredensial (Untuk Login)

Semua akun di bawah ini menggunakan password default: `password123`.

| Role | Nama | No. Telepon | Kategori | Keterangan |
| :--- | :--- | :--- | :--- | :--- |
| **ADMIN** | Gourmet Admin | `081234567890` | PUBLIK | Akses penuh ke Control Hub & Finance. |
| **CS** | CS Sarah | `081234567891` | PUBLIK | Akses ke Order Management & Stock. |
| **USER** | Budi Santoso | `081234567892` | PUBLIK | Akun pelanggan retail biasa. |
| **USER** | Andi (Pegawai RSUD) | `081234567893` | INSTANSI_PEGAWAI | Akun Pegawai (Retail di Kantor). |
| **USER** | Procurement Pertamina | `081234567894` | INSTANSI_BISNIS | Akun B2B (Bisnis Khusus). |


---

## 🍱 Menu & Jadwal

Terdapat 5 menu utama yang telah didaftarkan:
1.  **Nasi Liwet Special** (Rp 35.000 - Daily)
2.  **Beef Wellington Gourmet** (Rp 150.000 - Paket)
3.  **Salmon Glazed Mustard** (Rp 95.000 - Daily)
4.  **Ayam Bakar Taliwang** (Rp 45.000 - Daily)
5.  **Buffet Nusantara A** (Rp 2.500.000 - Paket)

*Jadwal harian telah disebar secara acak untuk rentang **H-7 sampai H+7** dari hari ini.*

---

## 📈 Estimasi Finansial (Sample)

Untuk keperluan **Phase 08 (Reporting)**, data berikut telah digenerate secara acak:

- **Orders**: ± 20-25 pesanan historis selama 30 hari terakhir.
- **Statuses**: Tercampur antara `PENDING`, `PAID`, `SHIPPED`, `COMPLETED`, dan `CANCELLED`.
- **Expenses**: ± 15 pengeluaran operasional (Belanja Bahan, Logistik, Gaji).

> [!TIP]
> Di halaman **Admin Finance (Reports)**, Anda akan melihat grafik **Monthly Revenue** dan perhitungan **Profit Margin** yang dihitung secara real-time dari data di atas.

---
*Dikelola oleh System Seeding Engine - 2026.*
