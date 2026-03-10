# MashaGuard

**Runtime JavaScript Protection & Threat Intelligence Platform**

MashaGuard is a real-time web intellectual asset protection platform. It detects, identifies, and responds to unauthorized inspection attempts, source code theft, and session manipulation — without relying on static obfuscation.

---

## Overview

Traditional obfuscation-based protection is passive and reversible. MashaGuard takes a different approach: the system actively monitors runtime behavior, collects forensic data from suspicious sessions, and executes a lockdown response before an attacker gains meaningful access.

Every integration is multi-tenant and isolated. Log data, configuration, and attacker identity are stored separately per account.

---

## Core Capabilities

**Active Threat Detection**
Detection triggers include DevTools activation, suspicious window resize events, and debugger execution. Responses are executed sequentially and confirmed by the server before lockdown is fully activated.

**Deep Forensic Collection**
Every detected session is profiled comprehensively:
- Canvas, Audio, and Font Fingerprinting
- WebRTC Local IP Capture
- GPU and Hardware Hashing
- VPN, Proxy, Tor, and Datacenter Detection
- Timezone Mismatch Analysis
- Server-side IP Intelligence

**Zero-Exposure Key Transmission**
API Keys are never transmitted over the public network. Authentication uses a double-locked HMAC SHA256 mechanism: the client receives only a short-lived token, verified by the server against a secret that never leaves your backend infrastructure.

**AI-Driven Interaction**
Locked sessions are engaged by an AI Brain powered by Gemini — designed to disorient and automatically document attacker responses.

**Visual Command Center**
A real-time Glassmorphism dashboard for monitoring attack logs, exporting forensic data as CSV, and configuring AI aggressiveness and kick timeout per account.

---

## Integration

Add one line to the `<head>` of your page:

```html
<script src="https://mg.dgxo.my.id/masha.js"></script>
```

The SDK automatically resolves its origin host. No manual configuration is required for standard deployments.

**Handshake Endpoint**

Provision a `/.masha-handshake` endpoint on your server. This endpoint generates an HMAC token using the `HANDSHAKE_SECRET` provided at registration. The token is sent to MashaGuard Server for verification — your API Key is never involved in this transmission.

```
Client Browser  →  /.masha-handshake (your server)  →  HMAC Token
HMAC Token      →  MashaGuard Server                →  Verified / Rejected
```

Full integration documentation is available after account registration.

---

## Security

MashaGuard operates on the principle that a protection system must itself be resistant to inspection. Key security layers include:

- Double-locked HMAC handshake — the shared secret is never transmitted over the network
- Rate limiting on all authentication and AI Chat endpoints
- Strict per-tenant data isolation — no cross-account data access
- Lockdown does not activate until the server confirms forensic data receipt

To report a security vulnerability, refer to [SECURITY.md](./SECURITY.md).

---

## Versioning

This platform follows [Semantic Versioning](https://semver.org). A full history of changes is available in [CHANGELOG.md](./CHANGELOG.md).

**Current version**: `2.2.0`

---

## Support & Contact

- Website: [mg.dgxo.my.id](https://mg.dgxo.my.id)
- Email: [contact@dgxo.my.id](mailto:contact@dgxo.my.id)
- Security Reports: [security@dgxo.my.id](mailto:security@dgxo.my.id)

---

*MashaGuard is a product of DGameXO. All rights reserved.*