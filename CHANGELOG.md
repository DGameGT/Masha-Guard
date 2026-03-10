# Changelog

All notable changes to MashaGuard are documented in this file.

Format follows [Keep a Changelog](https://keepachangelog.com/en/1.0.0/). This project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

---

## [2.2.0] — 2026-03-10

### Added
- **Advanced Forensic Suite**: New `advanced.js` module implementing WebRTC Local IP capture, Audio Fingerprinting, and Font Enumeration.
- **Threat Intelligence**: Server-side detection for VPN, Tor exit nodes, Cloudflare, and datacenter/hosting IP ranges.
- **Strike-First Logic**: Forensic data is now transmitted to and confirmed by the server before lockdown is fully activated, eliminating premature lock conditions.
- **Double-Locked Handshake**: Introduction of `HANDSHAKE_SECRET` as a second authentication layer — this secret is never transmitted over the network.
- **Timezone Mismatch Detection**: Cross-references browser system time against IP geolocation to flag VPN usage with high confidence.
- **Dev Reset Parameter**: `?reset=1` URL parameter to clear Prison/Logged state during development and testing.

### Changed
- **Dashboard Privacy**: IP address column removed from the public-facing log table. Full IP data remains available via CSV export only.
- **CSV Export**: Enhanced export output to include complete forensic detail — IP address, coordinates, and VPN status.
- **Kick Timeout UI**: Fixed synchronization issue between numeric input and slider control in timeout settings.

---

## [2.1.0] — 2026-03-10

### Added
- **Glassmorphism UI**: Full visual identity overhaul of the dashboard.
- **Rate Limiting**: Request throttling applied to authentication and AI Chat endpoints.
- **Dynamic Host Detection**: `masha.js` SDK now automatically resolves its origin host, removing the need for manual server URL configuration.

---

## [2.0.0] — 2026-03-10

- Initial release of MashaGuard V2. Introduced multi-tenant architecture, layered service pattern, and Zod-based input validation.

---

*MashaGuard is a product of DGameXO. All rights reserved.*