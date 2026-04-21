# Database Schema: Fullstack Catering (SvelteKit + Drizzle)

Rancangan database PostgreSQL menggunakan Drizzle ORM untuk menjamin integritas data operasional katering instansi.

## 📊 Entity Relationship Diagram (ERD) - Conceptual

### 1. Users (Autentikasi & RBAC)
Menyimpan data akun untuk seluruh modul (Admin, CS, User).
- `id`: UUID (PK)
- `name`: String
- `phone`: String (Unique, ID Login)
- `password`: String (Hashed)
- `role`: Enum (`ADMIN`, `CUSTOMER_SERVICE`, `USER`)
- `category`: Enum (`PUBLIK`, `INSTANSI`, `PEGAWAI_INSTANSI`)
- `instansi_name`: String (Nama instansi/bisnis jika kategori bukan Publik)
- `status`: Enum (`PENDING`, `ACTIVE`)
- `created_at`: Timestamp


### 2. Menu Types (Jenis Menu)
Tabel dinamis untuk pengelompokan besar menu (e.g., Daily, Paket, Buffet).
- `id`: UUID (PK)
- `name`: String (e.g., "Menu Daily")
- `slug`: String (Unique)
- `created_at`: Timestamp

### 3. Menu Categories (Kategori Produk)
Tabel dinamis untuk jenis hidangan (e.g., Nasi Kotak, Bento, Snack).
- `id`: UUID (PK)
- `name`: String (e.g., "Nasi Kotak")
- `slug`: String (Unique)
- `created_at`: Timestamp

### 4. Menus (Master Produk)
Setiap menu wajib terikat pada satu Tipe dan satu Kategori.
- `id`: UUID (PK)
- `name`: String
- `description`: Text
- `base_price`: Decimal
- `image`: String (URL/Path Foto)
- `type_id`: UUID (FK -> MenuTypes.id)
- `category_id`: UUID (FK -> MenuCategories.id)
- `created_by`: UUID (FK -> Users.id)
- `created_at`: Timestamp



### 3. DailySchedules (Jadwal Katalog Harian)
- `id`: Serial (PK)
- `menu_id`: UUID (FK -> Menus.id)
- `available_date`: Date (YYYY-MM-DD)
- `supply`: Integer (Porsi awal)
- `current_stock`: Integer (Sisa porsi real-time)

### 4. Orders (Transaksi Utama)
- `id`: UUID (PK)
- `user_id`: UUID (FK -> Users.id)
- `status`: Enum (`PENDING`, `PROCESSING`, `SHIPPED`, `COMPLETED`, `CANCELLED`)
- `total_base_price`: Decimal
- `total_tax`: Decimal
- `grand_total`: Decimal
- `payment_method`: Enum (`CASH`, `TRANSFER`)
- `payment_status`: Enum (`UNPAID`, `PAID`)
- `created_at`: Timestamp

### 5. OrderItems (Snapshot Pesanan)
- `id`: Serial (PK)
- `order_id`: UUID (FK -> Orders.id)
- `menu_id`: UUID (FK -> Menus.id)
- `quantity`: Integer
- `price_snapshot`: Decimal (Penting: Harga saat dipesan)

---

## 🔒 Integritas Data (Constraints)
1. **Stock Check**: `current_stock` wajib memiliki constraint `>= 0` di level database.
2. **Atomic Update**: Pengurangan stok saat checkout harus dilakukan dalam satu **Database Transaction**.
3. **Price Snapshot**: Data `price_snapshot` di `OrderItems` digunakan agar laporan keuangan masa lalu tetap akurat meskipun Admin mengubah harga di tabel `Menus`.

---
*Created by: Chief Architecture Governor*  
*Last Updated: 2026-04-19*
