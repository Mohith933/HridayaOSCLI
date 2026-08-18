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
└── package.json     ← Project configuration
```

---

## 🗺️ Roadmap — v5.x.0 Continuous Improvement

### ✅ v5.8.0 — Diagnostics Depth: Dev Runtimes, Games & Anti-Cheat (Current Release)
- **Developer Environment Diagnostics:** Cross-platform checks for Node.js, Python, Rust, Go, and Java — works on Windows, macOS, and Linux, since a missing runtime matters everywhere, not just Windows. Automatically included in `scan app`/`fix app` for apps that need one (e.g. DBeaver needs Java).
- **Game Detection Accuracy Pass:** Found and fixed real bugs while auditing `game.js` against `app.js`'s v5.6.0 fixes — VC++ 2017/2019 were missing entirely from the check list (any game requiring them, like GTA Trilogy: Definitive Edition, always failed the check even when correctly installed), .NET 4.0/4.5/4.8 all checked the same registry key and reported identically, and all DLL/DirectX paths were hardcoded to `C:\Windows` instead of resolving the real system drive.
- **Cross-Platform Game Scanning:** `scan game` no longer refuses entirely on macOS/Linux — Java-based games (Minecraft Java Edition) now get a real Java check on any OS, while Windows-only checks (DirectX, DLLs) are skipped cleanly with a clear note instead of a blanket error.
- **Anti-Cheat Conflict Detection:** New check for Vanguard (Valorant), Easy Anti-Cheat (Fortnite, Apex, Rocket League), and BattlEye (PUBG, Destiny 2) — flags whether the anti-cheat service is actually running, and whether known-conflicting tools (Cheat Engine, Process Hacker, x64dbg) are open at the same time.

### 📅 v5.9.0 — Trust & Data Integrity (Next Release)
- **Automated Database Verification:** A `verify-db` check run before every publish that catches duplicate keys/names automatically — the kind of bug that let Genshin Impact and Stardew Valley silently exist twice in `gameDB.js` until it was caught by hand in v5.6.0.
- **Community-Contributed Error Reports:** A structured way for users to submit a DLL/error Hridaya OS doesn't recognize yet, since no solo maintainer can personally hit every error on every OS/language setup worldwide.
- **Steam Deck / Proton Compatibility Notes:** Flag known Linux/Proton quirks for games that have them.

### 📅 v5.10.0 — Unified Diagnostics
- **One Unified Scan:** A single `check my system` command that runs app, game, and dev-runtime diagnostics together and reports back in one place, instead of three separate commands.
- **Self-Update Awareness:** Hridaya OS checks its own npm version on start and tells you if a newer release exists.
- **Usage-Driven Scaffolding Stacks:** New scaffolding stacks get added based on what people actually type and fail to match, not guesses.

---

## ⭐ Support Hridaya OS

If Hridaya OS helps you, you can support the project in two ways:

⭐ Star the project on GitHub
https://github.com/Mohith933/HridayaOS

▶️ Subscribe on YouTube for new features, tutorials and release updates.
https://www.youtube.com/@mohithsaib

Bug reports and feature requests are always welcome.

---

Made with Mohith Sai ❤️ — Hridaya OS — a terminal that speaks human!
