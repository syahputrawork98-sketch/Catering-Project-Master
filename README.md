# 🍱 Gourmet Hub: Premium Catering System

Selamat datang di **Gourmet Hub**, platform katering hibrida (B2B & B2C) yang dirancang khusus untuk kebutuhan instansi dan publik dengan estetika premium dan performa tinggi.

---

## 🏗️ Filosofi Workspace: Brain & Muscles

Proyek ini dipisahkan secara tegas antara tata kelola (Brain) dan eksekusi (Muscles):

1.  **🧠 The Brain (Root)**: Command Center pengerjaan.
    *   **Master Control**: [PROGRESS_KANBAN_MASTER.md](PROGRESS_KANBAN_MASTER.md) (Satu-satunya sumber kebenaran pengerjaan).
    *   **Master SOP**: [WORKFLOW.md](WORKFLOW.md) (Protokol "7-Langkah Emas").
    *   **Modular Kanban**: Folder `modules/` berisi detail teknis sub-atomik per modul.
2.  **💪 The Muscles (`catering-fullstack/`)**: 
    *   Implementasi kode menggunakan Svelte 5 (Runes), Drizzle ORM, Auth.js, dan Tailwind 4.

---

## 📂 Peta Navigasi Unit Kerja (Sub-Atomic)

| Module | Frontend (UI/UX) | Backend (Logic/Data) |
| :--- | :--- | :--- |
| **Public** | [KANBAN_FRONTEND.md](modules/public/KANBAN_FRONTEND.md) | [KANBAN_BACKEND.md](modules/public/KANBAN_BACKEND.md) |
| **User** | [KANBAN_FRONTEND.md](modules/user/KANBAN_FRONTEND.md) | [KANBAN_BACKEND.md](modules/user/KANBAN_BACKEND.md) |
| **CS** | [KANBAN_FRONTEND.md](modules/cs/KANBAN_FRONTEND.md) | [KANBAN_BACKEND.md](modules/cs/KANBAN_BACKEND.md) |
| **Admin** | [KANBAN_FRONTEND.md](modules/admin/KANBAN_FRONTEND.md) | [KANBAN_BACKEND.md](modules/admin/KANBAN_BACKEND.md) |

---

## 🛠️ Tech Stack & Standard
- **Front-end**: Svelte 5 (Runes based).
- **Styling**: Tailwind CSS 4 (Vibrant Gourmet).
- **Database**: PostgreSQL with Drizzle ORM.
- **Auth**: Auth.js (JWT Strategy + RBAC).
- **Infrastruktur**: Docker Compose (Database & pgAdmin).

---
*Dikelola dengan disiplin tinggi oleh Master Documentation Lead.*