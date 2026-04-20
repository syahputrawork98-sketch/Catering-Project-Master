# 🎨 KANBAN FRONTEND - Module [ADMIN]

Fokus: Kontrol sistem tingkat tinggi, analisis finansial, dan manajemen tata kelola.

---

## 🏗️ UI/UX Atomic Status Board

| Phase | Component / Feature | Atom Detail | Status |
| :--- | :--- | :--- | :--- |
| **03** | **Admin Portal** | Unified Dark Sidebar + Master Hub | [x] DONE |
| **07** | **System Control Hub** | Revenue Stats + Total Users Grid | [x] DONE |
| **07** | **B2B Creator Hub** | Manual Instansi Registration Tool | [x] DONE |
| **08** | **Financial Charts** | Revenue Trends (Bar/Line Chart) | [ ] PLANNED |

---

## 📝 Micro-Atomic Technical Checklist (Learning Resource)

### Phase 03 & 07: Control Center (Done)
- [x] **Master Layout Implementation**
    - [x] **File**: `src/routes/admin/+layout.svelte`.
    - [x] **Design**: Apply **High-Contrast Dark Sidebar** for Super Admin role.
    - [x] **Sync**: Coordinate sidebar items: "Control Hub", "Users", and "Finance".
- [x] **Admin Dash Home**
    - [x] **File**: `src/routes/admin/+page.svelte`.
    - [x] **Aesthetics**: Use `zinc-800/50` cards with `brand-primary` accents.
    - [x] **Stats**: Display 3 main KPI cards: Revenue, Instansi Count, and Total Users.

### Phase 07: B2B Operational Tools (Done)
- [x] **B2B Account Creator UI**
    - [x] **File**: `src/routes/admin/+page.svelte`.
    - [x] **UX**: Dedicated form for Admin to create Instansi accounts manually.
    - [x] **Logic**: Pass `INSTANSI` category as hidden/fixed input.

### Phase 07.5: Dashboard Stability (In Progress)
- [ ] **Data Safety Sweep**
    - [ ] Implement null-safety for `user.name` and other dynamic fields.
    - [ ] Resolve "Super Admin" layout type mismatch in sidebar.

### Phase 08: Puzzle Masa Depan (Planned)
- [ ] **Profit & Loss Dashboard**
    - [ ] Aggregating raw menu costs against selling price.
- [ ] **Audit Trail Viewer**
    - [ ] View critical status changes and by whom they were edited.
