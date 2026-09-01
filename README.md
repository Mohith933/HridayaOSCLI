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
├── scripts/
│   └── verify-db.js ← Database integrity check, runs before every publish (v5.9.0)
└── package.json     ← Project configuration
```
---

## 🗺️ Roadmap — v5.x.0 Continuous Improvement

### ✅ v5.10.0 — Unified Diagnostics (Current Release)
- **One Unified Scan:** A single `check my system` command that composes the already-tested app/game/runtime checks into one report, instead of requiring three separate commands. Reuses existing logic rather than duplicating it, so a future fix to any individual check automatically applies here too.
- **Self-Update Awareness:** Hridaya OS checks npm in the background on startup and tells you if a newer version exists — advisory only, never auto-updates, never blocks startup, fails silently offline (no new dependency added — uses Node's built-in `https` module).
- **Usage-Driven Scaffolding Stacks:** Not a one-time coding task — this is an ongoing practice of watching what people actually type and fail to match, and adding stacks based on real demand rather than guesses.

### 📅 v5.11.0 — Game Diagnostics: GPU & Driver Awareness (Next Release)
- **GPU Driver Version Awareness:** Detect the installed GPU driver version and flag known-outdated drivers as a "crash on launch" cause — a large share of real game crashes trace back to this, and it's a different failure mode than a missing DLL or VC++ Redistributable.
- **Steam Deck / Proton Coverage Expansion:** Extend v5.9.0's Linux/Proton compatibility notes to more titles as they're verified against real sources, not guessed.
- **Community Report Follow-Through:** Close detection-accuracy gaps surfaced through v5.9.0's `report error` feature — the reporting pipeline only has value if reports actually turn into fixes.

### 📅 v5.12.0 — App Diagnostics: Version-Aware Runtime Checks
- **Version-Specific Runtime Requirements:** v5.8.0 added yes/no runtime detection (is Node installed at all); this adds the next layer — is the *right version* installed (e.g. "Node 18+ required"), since many modern dev tools have real minimum-version requirements that "installed" alone doesn't capture.
- **Cloud & Container Tooling:** Extend `appDB.js` with AWS CLI, Azure CLI, gcloud, kubectl, and Docker Compose — a natural continuation of v5.6.0's dev-tools category (DBeaver, Postman, Docker Desktop).

### 📅 v5.13.0 — Scaffolding: Rust & Go Backend Stacks
- **Closes a loop from v5.8.0:** that release added Rust and Go to the dev-runtime diagnostics, but there's still no way to scaffold *into* either language. This adds a Rust backend stack (Axum) and a Go backend stack (Gin) — the runtime check and the scaffold finally match up.

---

## ⭐ Support Hridaya OS

If Hridaya OS saved your time fixing games/apps, support in 3 ways:

**1. ⭐ Star the project:**
https://github.com/Mohith933/HridayaOSCLI

**2. ❤️ Direct UPI Support (No Fees):**

📱 **Scan & Pay - GPay / PhonePe / Paytm:**

![UPI QR](GooglePay_QR(1).png)

**UPI ID:** `bmstpt1@okaxis`
*How to pay: GPay Open -> Scan QR -> Pay ₹99/₹199*

**3. ▶️ Subscribe on YouTube for new features & tutorials:**
https://www.youtube.com/@mohithsaib

Bug reports and feature requests are always welcome! 🚀

---

Made with Mohith Sai ❤️ — Hridaya OS — a terminal that speaks human!
