# 🎯 Discord Project Manager Bot

Bot ini adalah asisten manajemen proyek berbasis Discord. Dibuat menggunakan Python dan SQLite, bot ini memungkinkan pengguna untuk menyimpan, memperbarui, dan mengelola proyek mereka langsung dari Discord.

## 🚀 Fitur Utama

- Menambahkan proyek baru dengan nama, link, dan status
- Menampilkan semua proyek pengguna
- Mengupdate informasi proyek (nama, deskripsi, link, atau status)
- Menghapus proyek
- Menambahkan keterampilan ke proyek tertentu
- Modal & tombol interaktif (menggunakan `discord.ui`)
- Penyimpanan data menggunakan SQLite (`project.db`)

## 🛠 Struktur Proyek

```
📁 project/
├── alter.py           # Menambahkan kolom baru ke tabel proyek
├── bot.py             # Inti bot: semua command !start, !info, !new_project, dll
├── config.py          # Menyimpan konfigurasi (nama DB dan TOKEN)
├── logic.py           # Fungsi-fungsi database (CRUD proyek, status, skill)
├── modal.py           # Interaksi UI seperti tombol dan modal form
├── tes.py             # Contoh skrip testing sederhana
└── project.db         # File database SQLite
```

## ⚙️ Instalasi

1. **Clone repositori ini**  
   ```bash
   git clone https://github.com/username/project-manager-bot.git
   cd project-manager-bot
   ```

2. **Buat virtual environment dan install dependensi**
   ```bash
   python -m venv venv
   source venv/bin/activate  # Untuk Linux/Mac
   venv\Scripts\activate     # Untuk Windows
   pip install -r requirements.txt
   ```

3. **Edit `config.py`**  
   Ganti `'token sendiri'` dengan token asli bot Discord kamu.

4. **Inisialisasi database**  
   Jalankan file `logic.py` untuk membuat tabel dan data default:
   ```bash
   python logic.py
   ```

5. **Jalankan bot**
   ```bash
   python bot.py
   ```

## 🧪 Perintah Bot

- `!start` — Mulai interaksi dengan bot
- `!info` — Tampilkan semua perintah
- `!new_project` — Tambah proyek baru
- `!projects` — Tampilkan semua proyek
- `!update_projects` — Ubah detail proyek
- `!skills` — Tambahkan keterampilan ke proyek
- `!delete` — Hapus proyek
- `!test` — Tampilkan tombol & modal (dari `modal.py`)

## 💾 Catatan Database

Tabel-tabel dalam `project.db`:
- `projects`
- `skills`
- `status`
- `project_skills`

Untuk menambahkan kolom baru ke tabel proyek (seperti `Screenshoot`), gunakan `alter.py`.

## 📜 Lisensi

Proyek ini bersifat open-source dan bebas digunakan untuk tujuan pembelajaran atau pengembangan lebih lanjut.

---

**Dibuat oleh**: Malik Althaf
