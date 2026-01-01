# Geunaseh Jeumala - Website Organisasi

Website organisasi Geunaseh Jeumala dengan fitur CMS lengkap, AI Personal Agent, dan sistem event management.

## 🌟 Fitur Utama

### Public Website
- **Beranda** - Hero section dengan animasi bintang, program unggulan, event terbaru, artikel terbaru
- **Tentang** - Efek Galaxy dengan nama anggota sebagai bintang yang bergerak dengan parallax
- **Filosofi** - Penjelasan makna nama dan nilai-nilai organisasi
- **Event** - Daftar event dengan form pendaftaran
- **Artikel** - Blog dengan tags dan kategori
- **Galeri** - Koleksi gambar dan video
- **Dokumentasi/Kegiatan/Laporan** - Berbagai tipe dokumen

### Admin Dashboard
- **Autentikasi** dengan Secret Code: `<Mavecode300107>`
- **Dashboard** - Statistik dan quick actions
- **Halaman** - Edit konten halaman (hero, deskripsi, dll)
- **Artikel** - CRUD dengan tags
- **Media** - Manajemen gambar/video
- **Dokumen** - Dokumentasi, kegiatan, laporan
- **Event** - CRUD event + lihat peserta terdaftar + export CSV
- **AI Agent** - Task management dengan natural language input (mock)
- **Anggota** - Manajemen data anggota untuk efek Galaxy

## 🚀 Cara Menjalankan

### Prerequisites
- Node.js 18+
- Python 3.11+
- MongoDB

### Install Dependencies

```bash
# Frontend
cd frontend
yarn install

# Backend
cd backend
pip install -r requirements.txt
```

### Environment Variables

**Backend (.env)**
```
MONGO_URL="mongodb://localhost:27017"
DB_NAME="geunaseh_jeumala"
JWT_SECRET="your-secret-key"
CORS_ORIGINS="*"
```

**Frontend (.env)**
```
REACT_APP_BACKEND_URL=http://localhost:8001
```

### Run Development

```bash
# Backend
cd backend
uvicorn server:app --reload --port 8001

# Frontend
cd frontend
yarn start
```

## 👤 Default Admin

Untuk testing, Anda bisa membuat akun admin dengan:
- **Username**: bebas
- **Password**: bebas
- **Secret Code**: `<Mavecode300107>` (WAJIB)

Atau gunakan akun yang sudah dibuat:
- **Username**: admin
- **Password**: admin123
- **Secret Code**: `<Mavecode300107>`

## 📁 Struktur Project

```
/app/
├── backend/
│   ├── server.py          # FastAPI backend dengan semua API routes
│   ├── requirements.txt
│   ├── uploads/           # File uploads storage
│   └── .env
├── frontend/
│   ├── src/
│   │   ├── App.js         # Main React application
│   │   ├── index.css      # Global styles + animations
│   │   └── components/ui/ # shadcn/ui components
│   ├── tailwind.config.js
│   └── package.json
└── README.md
```

## 🎨 Teknologi

- **Frontend**: React 19, Tailwind CSS, shadcn/ui, Framer Motion
- **Backend**: FastAPI, Motor (async MongoDB), JWT Auth
- **Database**: MongoDB
- **Styling**: Gradient hijau tua bergradasi kebiruan (#013220 ke #005f73)

## ✨ Fitur Animasi

- Custom cursor dengan efek glow
- Scroll animations (fade-in, slide-up)
- Hover effects pada cards
- Galaxy effect dengan parallax pada halaman About
- Star twinkling animations
- Page transitions dengan fade

## 📝 API Endpoints

### Auth
- `POST /api/auth/signup` - Daftar admin baru (requires secretCode)
- `POST /api/auth/login` - Login admin (requires secretCode)
- `GET /api/auth/me` - Get current user

### Content
- `GET/POST /api/pages` - Manage page content
- `GET/POST/PUT/DELETE /api/articles` - Articles CRUD
- `GET/POST/DELETE /api/media` - Media CRUD
- `GET/POST/PUT/DELETE /api/documents` - Documents CRUD

### Events
- `GET/POST/PUT/DELETE /api/events` - Events CRUD
- `POST /api/events/{id}/register` - Register for event
- `GET /api/events/{id}/registrations` - Get registrations (admin)

### Tasks (AI Agent)
- `GET/POST/PUT/DELETE /api/tasks` - Tasks CRUD
- `POST /api/ai-agent` - Natural language to task (mock)

### Others
- `GET /api/members` - Get members for Galaxy effect
- `POST /api/upload` - Upload file
- `POST /api/seed` - Seed sample data

## 🔒 Security

- Password hashing dengan bcrypt
- JWT token authentication
- Secret code validation untuk akses admin
- Protected routes di frontend dan backend

## 📱 Responsive

Website ini fully responsive untuk:
- Desktop (1920px+)
- Tablet (768px - 1024px)
- Mobile (< 768px)

---

© 2025 Geunaseh Jeumala. All rights reserved.
