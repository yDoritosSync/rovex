# Rovex update log

Every Rovex update and what changed, newest first. Rovex shows these notes after it updates
(and any time in Settings › About › Update log). Rovex is in beta: updates are named, not numbered.

<!--
How to add an update (publish-release.ps1 uses this file for the GitHub release notes):
## <headline people see, e.g. "Faster launches">
_<internal version from tauri.conf.json / Cargo.toml> · <YYYY-MM-DD>_
### New / ### Fixed / ### Changed / ### Removed, each with "- " lines.
Internal versions: 0.1.0 = Beta 0.1, then 0.2.0, 0.3.0… (bugfix-only updates may use 0.1.1).
They must always increase and are only for the updater: people never see them.
The history from before Rovex (Orbit) is archived in docs/orbit-changelog-archive.md.
-->

## Your launcher, leveled up
_0.2.0 · 2026-11-23_

### New
- **In-game overlay**: a small card over Roblox with what's playing in Spotify or any music app. Click it to open the big player, drag it anywhere, resize it, and press Ctrl+Alt+M to hide or show it. It also has tabs for your server (rejoin, new server, copy join link), your online friends and your open accounts. Turn it on in Settings › Appearance.
- **Spotify**: connect your account on Spotify's own page in your browser, then browse your playlists, liked songs and search, and play any song from the overlay. Like songs, change the volume, shuffle, repeat and see what's up next. Playing from Rovex needs Spotify Premium.
- **Control Rovex from your phone**: scan a QR code with a phone on the same Wi-Fi to see your accounts, start presets and games, close or rejoin accounts and watch live snapshots. Your Roblox logins never leave your PC. Turn it on in Settings › Phone.
- **Library**: search, sort and filter your games, see how long you played each one and with which account, switch between grid and list, and group games into your own collections.
- **Live**: a page with live previews of every Roblox window. Click one to jump to it.
- **Region Selector**: press Pick a region on any game to open a 3D globe of Roblox's datacenters, pick a city and join the best server there in one click.
- **Server list**: each server shows its region, who's in it, ping and free slots. Filter by region and sort by players or ping.
- **Most played**: the Launchpad shows the games you played most in the past 24 hours, 7 days, 30 days or all time, for all accounts or just one.
- **Graph**: a Players tab that maps your accounts, your friends and the games they're in, like a constellation. Drag, zoom and click anyone to see more.
- **Profiles**: right-click a friend and choose View profile to see when they joined, their friends and followers, what they're playing, which of your accounts know them and your mutual friends.
- **Window names**: each Roblox window shows its account in the title, with its own small icon, so you always know which window is which.
- **Server notification**: when you join, see where the server is, how long it's been up and its ID.
- **Graphics profiles**: save Roblox's graphics, volume and FPS as named profiles and switch between them in one click.
- **Fast Flags**: pick the graphics API, anti-aliasing and the other options Roblox allows, without editing files.
- **Clean up**: free space by clearing Roblox's old logs and caches, by hand or automatically.
- **Roblox app options**: stop Roblox running in the background, and close Roblox when you leave a game.
- **Open Roblox links with Rovex**: game links from your browser or Discord go through Rovex, so they never block your other accounts. Turn it on in Settings › Launching.
- **Developer news**: an optional News page with Roblox Developer Forum announcements and release notes, with a notification when new ones come out. Turn it on in Settings › About & help.

### Changed
- **A new look**: the logo assembles itself when the installer and the app open, installing shows an orbit around the planet, and the first time you open Rovex you get a short welcome.
- **Private servers**: they now show their real owner, with the owner's name and Roblox picture.
- **Join bar**: one Play button, plus a small menu for Smallest, Together, Server ID, Private link and Follow user.
- **Playing one account**: Roblox opens maximized, like a normal window. Several accounts still tile.
- **Relaunching**: an account that's already playing closes its old window first, instead of opening a second Roblox.
- **Roblox open outside Rovex**: Roblox left in the background, opened before Rovex, or opened from your browser or Discord no longer blocks you. Rovex recognises which account it is and offers to close it.
- **Several accounts at once**: the first time you turn it on, Rovex explains that Roblox doesn't officially support it and could block it later.
- **Streamer mode**: game names, icons and banners from your history, presets and friends are hidden too.
- **Your main account's settings**: closing an alt no longer changes your main account's graphics and volume.
- **Running menu**: shows Closing… while a window closes, and the list no longer jumps around under your mouse.
- **Playing together**: the accounts you pick are remembered, even after playing with just one.
- **Friends radar**: fills in account by account and waits while you're launching, so it no longer slows anything down.
- **Chat**: scroll or pick between all your accounts, not just the first three.
- **Private server links**: links and codes are now encrypted on your PC.
- **Uninstalling**: Delete my data now removes everything, including Spotify and phone connections.

### Fixed
- **Private server links**: Roblox's new share links joined with error 524. They now work for every account you send.
- **Account status**: accounts said Playing or Running when they weren't. Rovex now checks the window on your PC and Roblox itself, and says Playing on another device when that's the case.
- **Server regions**: many servers showed no region. Regions now load in seconds, servers on screen fill in first, and full servers say Full and are checked again later.
- **Friends**: names sometimes didn't load, and the Graph sometimes missed friends from your other accounts.
- **Per-account FPS**: now wins over the global Roblox default.
- **Pages flashing**: pages flashed when they opened with a custom background, and the search icon disappeared.
- **Spacing**: between names, the verified tick and avatars.
- **Uninstaller**: it only removes Rovex's own files, never anything else in the folder you chose, plus Rovex's Start menu, desktop and taskbar shortcuts.
- **Safer saving**: a damaged file is recovered from its backup, password changes are all-or-nothing, changing your background never loses the old one, and exports never overwrite each other.
- **Smaller fixes**: lots of them, for stability, speed and streamer mode.

### Coming soon
- **Discord**: show the game you're playing on your Discord profile, with an optional join button.

## Rovex is here
_0.1.0 · 2026-11-22_

### New
- **The first Rovex beta.** A launcher to manage and play on all your Roblox accounts at once.
- **Launch many accounts together**, in your order, into the same game, server or private server. Save a group as a **preset** and start it from the Launchpad or the tray icon, even with Rovex closed.
- **Alt mode**: alts start with low FPS, lowest graphics, muted, minimized and at lower CPU priority, so your main game stays smooth.
- **Auto-rejoin**: kicked, disconnected or crashed accounts go back to their server, or to another one of the same game if it filled up.
- **Friends radar**: everyone who's friends with any of your accounts in one list. Star a friend to get a notification when they start playing, and join them in one click.
- **Smart servers**: Rovex checks servers before joining, hops to smooth ones in your region, shows each server's location and uptime, and remembers the last servers each account joined.
- **Health monitor**: RAM and CPU of every Roblox window, with a warning when your PC is struggling.
- **Windows notifications** for expired sessions, failed joins, friends who start playing and new updates.
- **Safe by design**: accounts are encrypted on your PC (Windows protection or a master password), updates are signed, and streamer mode hides names, avatars and Robux.
- Import accounts from Roblox Account Manager or from a `.rovex` backup.
