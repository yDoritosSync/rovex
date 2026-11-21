# Rovex

**Every Roblox account you own, one click away.** Rovex is a free Windows app to manage and launch several Roblox accounts: launch them together, keep alts light, rejoin after kicks, and see where your friends are playing.

**Download:** [rovexlauncher.com](https://rovexlauncher.com), or the latest installer on the [Releases page](https://github.com/yDoritosSync/rovex/releases/latest) (`Rovex-Setup.exe`). Windows 10 and 11. Rovex updates itself.

This repository only hosts the installers and the [update log](CHANGELOG.md). Rovex's source code is private.

## What it does
- Launch many accounts together, in your order, into the same game, server or private server. Save groups as presets.
- Alt mode: low FPS, lowest graphics, muted, minimized and lower CPU priority for alts.
- Auto-rejoin after kicks, disconnects and crashes.
- Friends radar across all your accounts, with alerts when a starred friend starts playing.
- Smart servers: checks servers before joining, hops within your region, shows location and uptime.
- Health monitor and Windows notifications.

## How it's made
- **Rust** for everything that matters: launching, the Roblox web APIs, encryption, updates. Fast, and light on CPU and RAM.
- **Tauri 2** for the desktop app. The interface is plain HTML, CSS and JavaScript drawn by Windows' own WebView2, so there's no bundled browser and the installer is about 11 MB.
- **Your accounts stay on your PC**, encrypted with Windows' own protection (DPAPI), or with your master password (Argon2id + XChaCha20-Poly1305). There is no Rovex server.
- **Signed updates**: every installer is checked (SHA-256 + Ed25519 signature) before Rovex installs it.
- **No injection, no exploits**: Rovex opens the official Roblox client the normal way.

## Not affiliated with Roblox
Rovex is not affiliated with, endorsed or sponsored by Roblox Corporation. "Roblox" is a trademark of Roblox Corporation. Running several Roblox windows isn't officially supported by Roblox and may stop working after a Roblox update. Use it at your own risk.

© 2026 yDoritosSync. All rights reserved. Free to use; don't redistribute, resell or modify it.
