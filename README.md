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


OTLSScan is a TLS/SSL configuration and certificate auditor that probes the handshake, enumerates protocols and ciphers, and decodes the X.509 chain with a pure-stdlib ASN.1 parser. It builds a protocol support matrix from SSLv3 to TLS 1.3, flags weak ciphers, checks HSTS and redirects, and produces a weighted A+ to F grade. It offers Mozilla modern/intermediate/old remediation snippets for Nginx, Apache, Caddy, HAProxy and Lighttpd, plus threaded batch scanning.

---

## ✨ Features


- Handshake probe (negotiated protocol, cipher, key-exchange bits, ALPN, session reuse, RTT)
- Protocol support matrix SSLv3 to TLS 1.3 with optional openssl s_client fallback for legacy protocols
- Per-suite cipher enumeration with server-preference and forward-secrecy ratio
- Pure-stdlib X.509 decoder (subject, SAN, validity, key size, EC curve, signature alg, EKU, OCSP, SCT)
- Weak-cipher heuristics, chain analysis, HSTS/redirect cross-check and offline PEM / openssl-ciphers analysis
- Weighted A+..F grade, Mozilla remediation profiles for 5 servers and threaded batch scanning

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage


```bash
./OTLSScan -t example.com:443
./OTLSScan --batch hosts.txt --format csv -o tls.csv --workers 8
./OTLSScan -t example.com --protocols --cert
./OTLSScan --pem server.pem --host example.com
./OTLSScan --help
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
