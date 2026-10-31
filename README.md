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
├── reportIssue.js   ← Local + GitHub error reporting (v5.9.0)
├── unifiedScan.js   ← "check my system" unified diagnostics (v5.10.0)
├── checkForUpdate.js ← Background npm update check (v5.10.0)
├── winRuntime.js    ← Shared Windows runtime detection, used by app.js + game.js (v5.12.0)
├── security.js      ← Security hygiene checks, read-only (v6.0.0)
├── scripts/
│   └── verify-db.js ← Database integrity check, runs before every publish (v5.9.0)
└── package.json     ← Project configuration
```

---

## 🗺️ Roadmap — v6.x.0 Continuous Improvement

### ✅ v6.8.0 — Deep Security Diagnostics & Command Hardening (Current Release)

Enhances Defender, Firewall, BitLocker, and Sandbox checks with deep-dive read-only diagnostics while enforcing strict input sanitization, 300-char boundary limits, and sub-process execution timeouts across all CLI modules.

---

### 📅 v6.9.0 — Project Scaffolding Expansion (Next Release)

Focuses on expanding and smoothing out the project scaffolding module (adding more frameworks, modern boilerplates, and streamlined setup flows).

---

### 📅 v6.10.0 — Final Security Polish & Guardrail (Coming Soon)

The final component of the security update arc. Implements safe final guardrails, error-handling polish for permission queries, and ensures zero OS-burden or risky registry edits remain.

---

## ⭐ Support Hridaya OS

If Hridaya OS saved your time fixing games/apps, support in 2 ways:

**1. ⭐ Star the project:**
https://github.com/Mohith933/HridayaOSCLI

**2. ▶️ Subscribe on YouTube for new features & tutorials:**
https://www.youtube.com/@mohithsaib

Bug reports and feature requests are always welcome! 🚀

---

Made with Mohith Sai ❤️ — Hridaya OS — a terminal that speaks human!
