<div align="center">

**🇮🇩 Bahasa Indonesia** | [🇬🇧 English](README.en.md)

# 🎙️ VoiceChat BE
### Proximity Voice Chat untuk Minecraft Bedrock Server

Ngobrol pakai suara asli langsung di dalam Minecraft Bedrock — tanpa Discord, tanpa ribet.
Cukup join server, dapat kode, buka app, langsung connect.

[![Platform](https://img.shields.io/badge/platform-Minecraft%20Bedrock-1abc9c)]()
[![App](https://img.shields.io/badge/app-Android-3ddc84)]()
[![Status](https://img.shields.io/badge/status-development-yellow)]()
[![License](https://img.shields.io/badge/license-MIT-blue)]()

[Download](#-download) •
[Cara Install](#-cara-install) •
[Cara Pakai](#-cara-pakai) •
[FAQ / Troubleshooting](#-faq--troubleshooting)

</div>

---

## 📖 Tentang

**VoiceChat BE** adalah sistem voice chat pihak ketiga untuk server **Minecraft Bedrock Edition**, dibuat khusus untuk **Minecraft Bedrock Community**. Beda dari Discord, voice chat ini terintegrasi langsung dengan gameplay:

- Room voice otomatis mengikuti lokasi kamu di server (island, base, dungeon, dll — tergantung konfigurasi server).
- Join lewat token yang di-generate langsung dari dalam game, tanpa perlu invite/link manual.
- Ringan, jalan di background, dan tetap connect walau layar HP mati atau app di-*minimize*.

Sistem ini terdiri dari 3 bagian:

| Komponen | Fungsi |
|---|---|
| 🧩 **Addon Minecraft Bedrock** | Dipasang di client Minecraft kamu. Menghasilkan token sesi voice chat & mendeteksi room berdasarkan posisi in-game. |
| 📱 **App VoiceChat BE (Android)** | Tempat kamu benar-benar ngobrol — connect ke room, mic, mute, deafen, dll. |
| ☁️ **Backend** | Menjembatani addon & app: validasi token, manajemen room, signaling voice (WebRTC). |

---

## ⬇️ Download

> File tersedia di halaman **[Releases](../../releases/latest)** repo ini.

| File | Deskripsi |
|---|---|
| `VoiceChatBE-Addon-vX.X.mcaddon` | Addon untuk Minecraft Bedrock (client) |
| `voicechat-bedrock-v1.1.apk` | App Android VoiceChat BE |

> ⚠️ Karena APK ini di luar Play Store, Android akan menampilkan peringatan **"install dari sumber tidak dikenal"** — ini normal, cukup izinkan untuk lanjut install.

---

## 🛠️ Cara Install

### 1. Install Addon di Minecraft Bedrock
1. Download file `.mcaddon` dari [Releases](../../releases/latest).
2. Buka file tersebut (otomatis kebuka lewat Minecraft) → tunggu proses import selesai.
3. Buka Minecraft → **Settings → Global Resources / Behavior Packs** → aktifkan **VoiceChat BE Addon** untuk world/server yang kamu mau.
4. Masuk ke server Bedrock seperti biasa.

### 2. Install App VoiceChat BE (Android)
1. Download `voicechat-bedrock-v1.1.apk` dari [Releases](../../releases/latest).
2. Buka file APK-nya → izinkan **"Install from unknown sources"** kalau diminta.
3. Install seperti app biasa, lalu buka.
4. Saat pertama kali dibuka, app akan minta beberapa izin — **izinkan semua** supaya voice chat jalan lancar:

   | Izin | Kenapa dibutuhkan |
   |---|---|
   | 🎤 Mikrofon | **Wajib** — supaya suara kamu bisa didengar orang lain |
   | 🔔 Notifikasi | Menampilkan status "sedang di voice call" saat app di-background |
   | 🔋 Battery Optimization | Supaya panggilan gak putus otomatis saat layar mati / app diminimize |

---

## 🎮 Cara Pakai

1. Masuk ke server Bedrock di Minecraft (addon harus sudah aktif).
2. Jalankan command / interaksi in-game untuk generate **token sesi voice chat** (kode unik, sekali pakai).
3. Salin token tersebut.
4. Buka app **VoiceChat BE** di HP → tempel token → **Join**.
5. Otomatis masuk ke voice room sesuai posisi kamu di server. Ngobrol seperti biasa!
6. Untuk keluar: tekan tombol **Leave** di app, atau **Leave Call** langsung dari notifikasi tanpa perlu buka app-nya.

---

## ❓ FAQ / Troubleshooting

**Suara saya tidak terdengar orang lain**
Cek izin mikrofon di HP: `Settings → Apps → VoiceChat BE → Permissions → Microphone → Allow`.

**Panggilan putus sendiri saat layar mati**
Pastikan izin **battery optimization** sudah di-disable untuk app ini (lihat bagian *Cara Install* di atas), atau cek manual di `Settings → Battery → App battery usage → VoiceChat BE → Unrestricted`.

**Token tidak valid / expired**
Token sesi hanya berlaku sementara. Generate ulang token dari dalam game kalau sudah kelamaan tidak dipakai.

**APK diblokir "Play Protect"**
Wajar, karena app di luar Play Store. Tap **"Install anyway"** / **"More details" → "Install anyway"**.

---

## 📄 License

MIT — bebas dipakai & dimodifikasi, sertakan atribusi.

<div align="center">

Dibuat untuk **Minecraft Bedrock Community** 🌌

</div>
