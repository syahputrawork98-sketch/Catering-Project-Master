# ⚙️ KANBAN BACKEND - Module [ADMIN]

Fokus: Keamanan tingkat tinggi, agregasi finansial, dan otoritas sistem pusat.

---

## 🏗️ Data Logic Atomic Status Board

| Phase | Logic / API Detail | Atom Detail | Status |
| :--- | :--- | :--- | :--- |
| **03** | **Role Hierarchy** | ADMIN has access to all routes | [x] DONE |
| **07** | **System Stats API** | Global SQL aggregation across tables | [x] DONE |
| **07** | **B2B Manual Provisioning** | Manual INSERT with hashed passwords | [x] DONE |
| **08** | **Profit Calculation** | grandTotal - menu cost aggregates | [ ] PLANNED |

---

## 📝 Micro-Atomic Technical Checklist (Learning Resource)

### Phase 03 & 07: Control & Stats (Done)
- [x] **Global Statistics Loader**
    - [x] **File**: `src/routes/admin/+page.server.ts`.
    - [x] **Aggregation**: Multi-table count for total users, instansi count, and total revenue.
    - [x] **Security**: Rigid check: `if (session.user.role !== 'ADMIN') throw error(403)`.
- [x] **Master User Audit**
    - [x] **Query**: Get latest 5 registrations with `orderBy: [desc(users.id)]`.

### Phase 07: Account Authority (Done)
- [x] **Manual Instansi Creator**
    - [x] **File**: `src/routes/admin/+page.server.ts`.
    - [x] **Logic**: Receive `instansiName`, `phone`, and `password`.
    - [x] **Security**: Use `argon2` to hash before storage.
    - [x] **Integrity**: Set status to `ACTIVE` by default for staff-created accounts.

### Phase 07.5: Otoritas & Policy (In Progress)
- [ ] **Policy Augmentation**
    - [ ] Update `Session` type declarations to include `Admin` specific fields.
    - [ ] Tighten `rbacHandle` for financial data protection.

### Phase 08: Puzzle Masa Depan (Planned)
- [ ] **Financial Reporting Engine**
    - [ ] Scheduled monthly report generation logic.
- [ ] **System Health Monitor**
    - [ ] Real-time active session monitoring.
