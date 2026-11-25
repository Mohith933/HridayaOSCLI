# 🌸 Hridaya OS CLI

[![npm version](https://img.shields.io/npm/v/hridaya-os.svg)](https://www.npmjs.com/package/hridaya-os)
[![Downloads](https://img.shields.io/npm/dw/hridaya-os.svg)](https://www.npmjs.com/package/hridaya-os)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

> A human-friendly CLI — type naturally, no strict commands needed.
> Works on Windows, Mac, Linux and Android (Termux).

## 🚀 Install

```bash
npm install -g hridaya-os
```

```bash
hridaya
```
---

---

## 🖨️ Driver & Hardware Management

> 🛡️ Read-only diagnostics for inspection, plus safe software-level repairs for stuck spool queues and error-state peripherals without altering system binaries or hardware.

```text
`check printers`           → Check connected printers & spooler
`check spooler`            → Check print spooler service
`check audio`              → Check Windows Audio service (`Audiosrv`)
`check bluetooth`          → Check connected Bluetooth devices
`check peripherals`        → Scan for problematic USB / PnP devices
`fix print spooler`        → Purge stuck print jobs & restart spooler 
`fix peripherals`          → Software-reset error-state peripherals 
```

## 🛡️ Security Management

> 🛡️ Read-only, always — Hridaya OS is not antivirus and never changes a setting for you. It only reports what's currently on or off, so you know what to go fix yourself.

```text
check my security           → Full Security Overview
check windows defender      → Check Antivirus and real-time protection status
check firewall              → Verify Windows Firewall profiles
check bitlocker             → Audit disk encryption and volume protection
check sandbox               → Analyze system isolation and sandbox readiness
```
---

## 🖥️ Application Management

> Fix common application errors in seconds — no searching through forums.
> ⚠️ Windows only | 🔒 Official links only — no cracks, no piracy.

```text
scan app photoshop.exe      → check application requirements
fix app photoshop.exe       → show what's missing + fix links
fix error msvcp140.dll      → common DLL fix
list apps                   → 18 supported applications
```

**31 Supported Applications** — Adobe Photoshop, Premiere Pro, Illustrator,
After Effects, AutoCAD, Autodesk 3ds Max, Microsoft Word, Microsoft Excel,
VLC Media Player, OBS Studio, Visual Studio Code, 7-Zip, WinRAR,
HandBrake, Blender, Discord, Spotify and Zoom and more.

---

## 🎮 Game Management
> Fix DLL errors in seconds — no YouTube, no ChatGPT detours.
> ⚠️ Windows only | 🔒 Official links only — no cracks, no piracy.

```
check my system             → one unified scan across apps, games, and dev runtimes together
scan my system              → full PC game-readiness check
scan game gta_sa.exe        → check all requirements
fix game gta_sa.exe         → show what's missing + fix links
fix error d3dx9_43.dll      → instant DLL fix
fix error 0xc000007b        → error code fix
fix all games               → fixes 90% of errors in one go
check directx               → DirectX version + legacy runtime
check visual c++            → all VC++ versions
list games                  → 36 supported games
what games can i play       → check which supported games will run
```

**76 Supported Games** — GTA series, NFS, Max Payne, CS, Minecraft, Valorant,
Witcher, Assassin's Creed, Batman Arkham, RDR2, Cyberpunk, Elden Ring, PUBG,
Fortnite, FIFA, Rocket League, Hogwarts Legacy, Mortal Kombat 11 and more.

---

## 💿 Disk Management

```
show disk space                      → all drives with usage bars
what's taking up space               → largest folders ranked
how much space is downloads using    → specific folder size
find duplicate files                 → finds wasted space
clean temp files                     → safely deletes junk
empty recycle bin                    → instant cleanup
save disk report                     → saves .txt report
warn me when disk goes below 5GB     → background watcher
start disk history                   → tracks over time
show larger files                    → find files over 1GB
```

---

## 💾 Memory Management

```
what's eating my memory              → top RAM hungry apps
kill whatever is eating my RAM       → kills heaviest process
show memory usage                    → total, used, free
save memory report                   → saves .txt report
compare chrome and discord memory    → side by side
warn me when RAM goes above 80%      → background watcher
start memory history                 → tracks every 60 seconds
system info                          → OS, CPU, cores, uptime
kill chrome                          → kill a specific application
list running processes               → list all active processes
```

---

## 📁 File Management

```
create a folder named projects
delete the folder named old
copy file notes.txt to backup/notes.txt
move folder work to archive/work
arrange my files                     → auto sorts images, videos, code
create 3 folders named a, b, c
read the file notes.txt
write Hello World to notes.txt
list all files
open notes.txt
hide notes.txt
unhide notes.txt
show hidden files
search for notes.txt
how big is notes.txt
count files
clear folder projects
go to downloads
zip projects
unzip projects.zip

```

---

## 🚀 Project Scaffolding

```
create a react app named myapp
create a next.js project named blog
create an express app named api
create a django project named site
create a node project named tool
create a spring boot app named svc
create a vite app named myapp
create a fastapi project named api    
create a nestjs project named backend   
create a flutter app named myapp
create a react native app named myapp

```
> 💡 **New in v5.7.0:** If you leave out the project name (e.g. just `create a streamlit dashboard`), Hridaya OS will now ask you for one instead of failing silently.
> 💡 **Pro Tip:** We keep the default menu concise so you aren't buried in choices. However, Hridaya OS also supports **SvelteKit, Astro, Bun, Remix, Hono, Elysia, and T3**. Just type `create a <framework> app named <name>` and it will scaffold automatically!
---

---

## 🐛 Reporting an Unrecognized Error (v5.9.0)

> 💡 Hit an error Hridaya OS doesn't know? Report it instead of losing it.

| What you want to do | Type this naturally |
| --- | --- |
| Report an error | `report error msvcp140.dll crashes photoshop on launch` |
| Report a bug     | `report bug fortnite won't start after update` |

Being honest about how this actually works: Hridaya OS is a solo-maintained, offline CLI tool with **no backend server** — there's no live crowd-sourced database silently collecting reports. What actually happens: your report is saved locally to `~/.hridaya/reports.json` so it's never lost, and a pre-filled GitHub Issue is opened in your browser (the real place these get triaged — see the [Issues page](https://github.com/Mohith933/HridayaOS/issues)). Nothing is sent anywhere unless you click "Submit new issue" yourself.

---

## 🗂️ Project Structure

```
hridaya-os/
├── index.js         ← CLI entry point
├── parser.js        ← Understands natural language
├── fileSystem.js    ← File & folder management
├── memory.js        ← Memory management
├── disk.js          ← Disk management
├── game.js          ← Game management
├── gameDB.js        ← Game requirements database 
├── app.js           ← Application management 
├── detector.js      ← Real-Time Detection Engine
├── appDB.js         ← Application requirements database 
├── scaffolder.js    ← Project scaffolding
├── reportIssue.js   ← Local + GitHub error reporting
├── unifiedScan.js   ← "check my system" unified diagnostics
├── checkForUpdate.js ← Background npm update check
├── winRuntime.js    ← Shared Windows runtime detection, used by app.js + game.js
├── security.js      ← Security hygiene checks, read-only
├── guardrails.js    ← Final Security Guardrails & Input Hardening
├── drivers.js       ← Real-World Hardware & Driver Diagnostics (v7.0.0)
├── scripts/
│   └── verify-db.js ← Database integrity check, runs before every publish
└── package.json     ← Project configuration
```

---

## 🗺️ Roadmap — v7.x.0 Evolution

### ✅ v7.1.0 — Software-Level Spooler & Peripheral Fixes 
Adds safe software-level repairs to clear stuck `.SHD`/`.SPL` print spool files, restart the Print Spooler service, and software-reset problematic PnP peripheral devices by `InstanceId`.

--- 

### ✅ v7.2.0 — Modern Game Engine & Emerging Stack Scaffolding (Current Version)
Expands `scaffolder.js` with ready-to-run starter templates for modern indie/web game development (**Phaser 3**, **Three.js + Vite**, **Kaboom/Kaplay**, **Godot 4 GDScript starter**) alongside emerging AI/full-stack templates (**MCP Server**, **TanStack Start**, **FastAPI + LangGraph**).

---

### 🎯 v7.3.0 — Exact Game DLL & Runtime Error Mapper (GTA 6 & Classic Titles)
Maps exact missing/corrupted `.dll` and runtime errors across modern AAA titles (such as **GTA 6** and contemporary engines) and classic PC games so users get the exact official fix instead of wasting time searching random forums or risky DLL sites:
* **Visual C++ Redistributable (`vcruntime140.dll`, `vcruntime140_1.dll`, `msvcp140.dll`, `msvcp140_1.dll`)** — Maps to official Microsoft Visual C++ Redistributable (x64 & x86) repair/install guidance.
* **DirectX 11 / 12 & DXGI (`d3d12.dll`, `d3d11.dll`, `dxgi.dll`, `d3dcompiler_47.dll`)** — Maps to Windows Update, GPU driver checks, and system file checks (`sfc /scannow`) rather than fake standalone "DirectX 12" downloads.
* **Legacy DirectX 9 / XInput (`d3dx9_43.dll`, `xinput1_3.dll`, `xinput1_4.dll`, `d3dcompiler_43.dll`)** — Maps to the official DirectX End-User Runtime installer for older games.
* **Clear Fix Guidance** — Explains *why* the error happens, which official runtime package fixes it, and why users should avoid copying random `.dll` files from untrusted sites.

---

### 🩹 v7.4.0 — Pain-Remover & One-Shot Diagnostic Triage
Eliminates everyday terminal and PC setup friction so users go straight from an error message to a working fix:
* **Plain-English Error Triage** — Translates cryptic launch errors, missing runtime prompts, and service/permission blocks into clear next steps without jargon.
* **Safe Verification & Repair Flow** — Guides users through official runtime repairs, game file verification, and safe system checks step by step.
* **Zero-Fluff Actionable Output** — Highlights the exact command or official installer needed first so users don't lose hours guessing.

--- 

## ⭐ Support Hridaya OS

If Hridaya OS saved your time fixing games/apps, support in 2 ways:

**1. ⭐ Star the project:**
https://github.com/Mohith933/HridayaOSCLI

**2. ▶️ Subscribe on YouTube for new features & tutorials:**
https://www.youtube.com/@mohithsaib

Bug reports and feature requests are always welcome! 🚀


## ☕ Support the Creator

If Hridaya OS has saved you time or made your workflow easier, consider buying me a Sunday coffee ☕ via GPay:

<p align="center">
  <img src="GooglePay_QR(1).png" alt="GPay QR Code" width="250"/>
</p>

*Thank you for supporting independent open-source development! 🌸*

---

Made with Mohith Sai ❤️ — Hridaya OS — a terminal that speaks human!
