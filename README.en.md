<div align="center">

[🇮🇩 Bahasa Indonesia](README.md) | **🇬🇧 English**

# 🎙️ VoiceChat BE
### Proximity Voice Chat for Minecraft Bedrock Servers

Talk with real voice directly inside Minecraft Bedrock — no Discord, no hassle.
Just join the server, get a code, open the app, and connect.

[![Platform](https://img.shields.io/badge/platform-Minecraft%20Bedrock-1abc9c)]()
[![App](https://img.shields.io/badge/app-Android-3ddc84)]()
[![Status](https://img.shields.io/badge/status-development-yellow)]()
[![License](https://img.shields.io/badge/license-MIT-blue)]()

[Download](#-download) •
[Installation](#-installation) •
[How to Use](#-how-to-use) •
[FAQ / Troubleshooting](#-faq--troubleshooting)

</div>

---

## 📖 About

**VoiceChat BE** is a third-party proximity voice chat system for **Minecraft Bedrock Edition** servers, built specifically for **AstraviaSMP**. Unlike Discord, this voice chat is tied directly into gameplay:

- Voice rooms follow your in-game location automatically (island, base, dungeon, etc. — depending on server config).
- Join using a token generated directly in-game — no manual invites or links needed.
- Lightweight, runs in the background, and stays connected even when the screen is off or the app is minimized.

The system has 3 parts:

| Component | Purpose |
|---|---|
| 🧩 **Minecraft Bedrock Addon** | Installed on your Minecraft client. Generates the voice session token & detects rooms based on your in-game position. |
| 📱 **VoiceChat BE App (Android)** | Where the actual talking happens — connect to a room, mic, mute, deafen, etc. |
| ☁️ **Backend** | Bridges the addon & app: token validation, room management, WebRTC voice signaling. |

---

## ⬇️ Download

> Files are available on this repo's **[Releases](../../releases/latest)** page.

| File | Description |
|---|---|
| `VoiceChatBE-Addon-vX.X.mcaddon` | Addon for Minecraft Bedrock (client) |
| `voicechat-bedrock-v1.1.apk` | VoiceChat BE Android app |

> ⚠️ Since this APK is outside the Play Store, Android will show an **"install from unknown sources"** warning — this is expected, just allow it to continue.

---

## 🛠️ Installation

### 1. Install the Addon in Minecraft Bedrock
1. Download the `.mcaddon` file from [Releases](../../releases/latest).
2. Open the file (it opens automatically in Minecraft) → wait for the import to finish.
3. Open Minecraft → **Settings → Global Resources / Behavior Packs** → enable **VoiceChat BE Addon** for the world/server you want.
4. Join the AstraviaSMP server as usual.

### 2. Install the VoiceChat BE App (Android)
1. Download `voicechat-bedrock-v1.1.apk` from [Releases](../../releases/latest).
2. Open the APK file → allow **"Install from unknown sources"** if prompted.
3. Install it like a normal app, then open it.
4. On first launch, the app will ask for a few permissions — **allow all of them** so voice chat works properly:

   | Permission | Why it's needed |
   |---|---|
   | 🎤 Microphone | **Required** — so others can hear your voice |
   | 🔔 Notifications | Shows an "in voice call" status while the app is in the background |
   | 🔋 Battery Optimization | Prevents the call from auto-disconnecting when the screen turns off / app is minimized |

---

## 🎮 How to Use

1. Join the AstraviaSMP server in Minecraft (the addon must be enabled).
2. Run the in-game command / interaction to generate a **voice session token** (a unique, single-use code).
3. Copy that token.
4. Open the **VoiceChat BE** app on your phone → paste the token → **Join**.
5. You'll automatically join the voice room matching your position on the server. Start talking!
6. To leave: tap **Leave** in the app, or tap **Leave Call** directly from the notification without opening the app.

---

## ❓ FAQ / Troubleshooting

**Others can't hear me**
Check the microphone permission on your phone: `Settings → Apps → VoiceChat BE → Permissions → Microphone → Allow`.

**Call disconnects on its own when the screen turns off**
Make sure **battery optimization** is disabled for this app (see the *Installation* section above), or check manually at `Settings → Battery → App battery usage → VoiceChat BE → Unrestricted`.

**Token invalid / expired**
Session tokens are only valid temporarily. Generate a new one in-game if it's been unused for too long.

**APK blocked by "Play Protect"**
This is expected since the app is outside the Play Store. Tap **"Install anyway"** / **"More details" → "Install anyway"**.

---

## 🧱 Tech Stack

- **Addon**: Minecraft Bedrock Scripting API (`@minecraft/server`)
- **App**: Next.js + Capacitor (Android WebView + native foreground service for background calls)
- **Backend**: Go, PostgreSQL, WebRTC signaling via Socket.IO

---

## 📄 License

MIT — free to use and modify, attribution appreciated.

<div align="center">

Built for **AstraviaSMP** 🌌

</div>
