# 🦉 OTLSScan

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-OScan-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0.0-cyan?style=flat-square"/>
</p>

> **OTLSScan** — TLS/SSL Configuration Auditor

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview

TLS/SSL configuration & certificate auditor

---

## ✨ Features

- TLS handshake probe — negotiated protocol, cipher, key-exchange bits, ALPN (h2/http1.1), compression, session-ticket / session-reuse hints, RTT timing
- Protocol support matrix — SSLv3 → TLS 1.3 using pinned min/max contexts (stdlib) with optional openssl s_client fallback for legacy protocols
- Cipher enumeration — per-suite TLS 1.2 handshake probes against the local OpenSSL cipher list, server-preference detection, forward-secrecy ratio
- Pure-stdlib DER/ASN.1 X.509 decoder — subject, issuer, SAN, validity, key type/size, EC curve, signature algorithm, basic constraints, key usage, EKU, AIA/OCSP, CRL DP, SCT presence, must-staple
- Chain analysis — order, self-signed root sent, intermediate expiry, weak signature in chain
- Weak cipher heuristics (NULL/EXPORT/RC4/3DES/DES/ CBC-SHA1/anon/PSK/SRP/CAMELLIA/IDEA/SEED/MD5) plus offline `openssl ciphers -v` paste analyser
- HSTS / HTTP→HTTPS redirect cross-check (urllib)
- Weighted A+…F grade engine with caps & subscores
- Remediation — Mozilla modern/intermediate/old profiles for Nginx, Apache, Caddy, HAProxy, Lighttpd
- Threaded batch scan of host:port lists + summary
- Export TXT / CSV / JSON, clipboard, ~/OTLSScan
- Full CLI mode (-t host[:port], --batch, --json ...)

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OTLSScan
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
