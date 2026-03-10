# MashaGuard

**Runtime JavaScript Protection & Threat Intelligence Platform**

MashaGuard adalah platform perlindungan aset intelektual web yang beroperasi secara real-time. Sistem ini mendeteksi, mengidentifikasi, dan merespons upaya inspeksi ilegal, pencurian kode, serta manipulasi sesi  tanpa ketergantungan pada obfuscation statis.

---

## Overview

Proteksi tradisional berbasis obfuscation bersifat pasif dan dapat dibalik. MashaGuard mengambil pendekatan berbeda: sistem aktif memantau perilaku runtime, mengumpulkan data forensik dari sesi mencurigakan, dan mengeksekusi respons terkunci sebelum penyerang mendapatkan akses yang berarti.

Setiap integrasi bersifat multi-tenant dan terisolasi. Data log, konfigurasi, dan identitas penyerang tersimpan secara terpisah per akun.

---

## Core Capabilities

**Active Threat Detection**
Pemicu deteksi mencakup pembukaan DevTools, resize window mencurigakan, dan eksekusi debugger. Respons dieksekusi secara sekuensial dan dikonfirmasi server sebelum lockdown aktif.

**Deep Forensic Collection**
Setiap sesi yang terdekteksi akan dikumpulkan profilnya secara menyeluruh:
- Canvas, Audio, dan Font Fingerprinting
- WebRTC Local IP Capture
- GPU & Hardware Hashing
- VPN, Proxy, Tor, dan Datacenter Detection
- Timezone Mismatch Analysis (indikator VPN kuat)
- Server-side IP Intelligence

**AI-Driven Interaction**
Sesi yang terkunci dapat berinteraksi dengan AI Brain dirancang untuk membingungkan dan mendokumentasikan respons penyerang secara otomatis.

**Visual Command Center**
Dashboard real-time berbasis Glassmorphism untuk memantau log serangan, mengekspor data forensik (CSV), dan mengonfigurasi tingkat agresivitas serta kick timeout per akun.

---
## Security

MashaGuard beroperasi dengan prinsip bahwa sistem proteksi itu sendiri harus tahan inspeksi. Beberapa lapisan yang diterapkan:

Untuk melaporkan kerentanan keamanan, lihat [SECURITY.md](./SECURITY.md).

---

## Versioning

Platform ini mengikuti [Semantic Versioning](https://semver.org). Riwayat perubahan tersedia di [CHANGELOG.md](./CHANGELOG.md).

**Versi saat ini**: `2.2.0`

---

## Support & Contact

- Website: [mg.dgxo.my.id](https://dgxo.my.id)
- Email: [contact@dgxo.my.id](mailto:contact@dgxo.my.id)
- Security Reports: [security@dgxo.my.id](mailto:security@dgxo.my.id)

---

*MashaGuard is a product of DGameXO. All rights reserved.*
