# 🦉 OArmor

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-ONetwork-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.1-cyan?style=flat-square"/>
</p>

> **OArmor** — ARP Packet Crafter & Network Prober

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview

OArmor is a standard-library ARP packet crafter and network prober for Layer-2 work on authorised networks. It builds and transmits ARP Request, Reply, Gratuitous and Probe frames, sweeps the local network and resolves vendors through an OUI lookup. Captured frames can be hex-decoded and dumped in colour, then exported to binary, hex or TXT for analysis.

---

## ✨ Features

- Craft and transmit ARP Request / Reply / Gratuitous / Probe frames
- Network ARP sweep with host discovery
- OUI-based vendor lookup for discovered MAC addresses
- Hex decoding of ARP frames with coloured dump output
- Export captured data to binary, hex and TXT
- No external dependencies — Python standard library only

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OArmor
./OArmor --interfaces
./OArmor --help
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
