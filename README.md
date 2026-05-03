# 📥 M3U8 Video Downloader — Google Colab

Download video dari link M3U8 langsung ke Google Drive menggunakan Google Colab.

---

## ✨ Fitur

- ✅ Download video M3U8 ke Google Drive
- ✅ Otomatis pilih kualitas tertinggi
- ✅ Live progress bar + speed + ETA
- ✅ History & log download per sesi
- ✅ Support Cloudflare protected site (via cookies)
- ✅ Mudah dipakai, tinggal isi link & run

---

## 🚀 Cara Pakai

### 1. Persiapan Cookies
1. Install extension Chrome: **[Get cookies.txt LOCALLY](https://chrome.google.com/webstore/detail/get-cookiestxt-locally/cclelndahbckbenkjhflpdbgdldlbecc)**
2. Buka halaman video di browser → play videonya
3. Klik extension → **Export** → simpan sebagai `cookies.txt`

### 2. Buka Colab
Klik tombol di bawah:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/USERNAME_GITHUB_KAMU/m3u8-downloader/blob/main/m3u8_downloader.ipynb)

### 3. Upload Cookies
1. Di Colab, klik icon 📁 **Files** di panel kiri
2. Upload file `cookies.txt` ke `/content/`

### 4. Run & Download
1. ▶️ **Run Cell 1** → Login Google → Mount Drive
2. Isi parameter:
   - `M3u8_link` → link m3u8 video
   - `Referer_link` → URL halaman video
   - `Download_location` → path simpan di Google Drive
3. ▶️ **Run Cell 2** → Download berjalan otomatis

---

## 📋 Parameter

| Parameter | Contoh | Keterangan |
|---|---|---|
| `M3u8_link` | `https://surrit.com/xxx/video.m3u8` | Link M3U8 video |
| `Referer_link` | `https://missav.ws/en/xxx/` | URL halaman video |
| `Download_location` | `/content/drive/MyDrive/myvideo.mp4` | Lokasi simpan di Drive |
| `Cookies_file` | `/content/cookies.txt` | Path cookies (tidak perlu diubah) |

---

## 📁 Struktur File

```
/content/m3u8_logs/          ← local Colab (hilang saat sesi habis)
    ├── download_history.json
    └── session_log.txt

MyDrive/                     ← Google Drive (permanen)
    └── myvideo.mp4
```

---

## ⚠️ Catatan

- Cookies perlu diupload ulang setiap sesi Colab baru
- Jika muncul error 403, coba export ulang cookies dari browser
- Ganti nama file di `Download_location` setiap download video baru agar tidak tertimpa
- History & log hanya tersimpan selama sesi Colab aktif

---

## 🛠️ Tech Stack

- [yt-dlp](https://github.com/yt-dlp/yt-dlp) — video downloader
- [Google Colab](https://colab.research.google.com) — cloud runtime
- [Google Drive](https://drive.google.com) — penyimpanan hasil download
- Python 3

---

## 📄 License

MIT License — bebas dipakai dan dimodifikasi
