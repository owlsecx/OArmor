# 🛡️ OArmor

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-informational?style=flat-square&logo=linux&logoColor=white&color=0a0c10"/>
  <img src="https://img.shields.io/badge/Category-ONetwork%20%2F%20Layer%202-cyan?style=flat-square"/>
  <img src="https://img.shields.io/badge/Dependencies-None%20(stdlib)-yellow?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-Proprietary-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-v1.0-cyan?style=flat-square"/>
</p>

> **OArmor** is a powerful ARP packet crafter and network prober. It allows crafting and transmitting ARP Request, Reply, Gratuitous, and Probe frames, performing ARP sweeps, decoding raw frames with colored hex dumps, OUI vendor lookup, and exporting in Binary, Hex, and TXT formats.

**Requires root privileges for transmission. Pure standard library implementation.**

---

## 📌 Overview

OArmor gives full control over Layer 2 ARP traffic. It is designed for advanced network reconnaissance, ARP spoofing simulations (authorized only), IP conflict testing, and forensic analysis of ARP frames.

It features a clean terminal interface with colored hex dumps, detailed field summaries, and multiple export options.

---

## 🖥️ Modules

| # | Module               | Description |
|---|----------------------|-------------|
| **[1]** | **ARP Request**      | Classic "Who has <IP>?" lookup |
| **[2]** | **ARP Reply**        | Spoofed reply ("<IP> is at <MAC>") |
| **[3]** | **Gratuitous ARP**   | Announce IP ownership (broadcast) |
| **[4]** | **ARP Probe**        | RFC 5227 IP conflict probe (sender IP = 0.0.0.0) |
| **[5]** | **Decode Frame**     | Parse raw hex → detailed colored breakdown |
| **[6]** | **ARP Sweep**        | Who-has scan over IP range or CIDR |

---

## 📊 Key Features

- **Full ARP Frame Crafting** — Request, Reply, Gratuitous, Probe
- **Colored Hex Dump** — Ethernet header (orange), ARP packet (cyan), padding (dim)
- **OUI Vendor Database** — 50+ common vendors (VMware, Apple, Cisco, TP-Link, etc.)
- **Detailed Field Summary** — Operation, MACs, IPs, vendor, size, timestamps
- **Transmission** — Raw Layer 2 socket (requires root)
- **Export Options**:
  - Binary (.bin) — raw frame bytes
  - Hex (.hex) — space-separated hex with metadata
  - TXT (.txt) — human-readable report with hex dump
- **ARP Sweep** — Fast scanning with delay control
- **Clean UI** — Professional colored output and help system

---

## ⚙️ Requirements

- **Linux** (AF_PACKET socket support)
- **Root / sudo** for frame transmission
- No external Python packages required (pure stdlib)

**Standalone executable** — Runs as `./OArmor` when built with PyInstaller.

---

## 🚀 Usage

```bash
sudo ./OArmor


Typical Workflow:

Choose a crafting module [1–4]
Enter MAC/IP parameters
Review the detailed colored frame breakdown
Choose to Transmit (root required) or Save to file
Use [5] Decode Frame to analyze captured raw hex
Use [6] ARP Sweep for network discovery

Important: Transmission requires root privileges.

📁 Output

Live Terminal — Colored hex dump + field summary
Reports (saved in oarmor_reports/):
oarmor_YYYYMMDD_HHMMSS.bin — Raw binary frame
oarmor_YYYYMMDD_HHMMSS.hex — Hex dump with metadata
oarmor_YYYYMMDD_HHMMSS.txt — Full human-readable report



📦 Part of OwlSec Toolkit
This tool is part of the OwlSec suite — a collection of 300+ security and privacy tools.
🔗 owlsec.org

©️ License
Proprietary — © Khaled S. Haddad
Tools are distributed as pre-built executables. Source code is proprietary.
AUTHORISED DEFENSIVE NETWORK TESTING & LAYER 2 ANALYSIS USE ONLY
