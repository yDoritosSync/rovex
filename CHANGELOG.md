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

## A cleaner Rovex
_0.3.0 · 2026-11-24_

### New
- **A new in-game overlay**: it now shows your account, the game (with its icon and banner) and how many friends you can join, and lets your clicks go through to the game everywhere else. Click it, or press its shortcut (Ctrl+Shift+O unless you picked another one), to open it, and Esc to go back to the game. Four tabs (Server, Friends, Accounts, Media), "Bring here" to pull another of your accounts into your server, and a progress card that stays while you rejoin, with buttons when something goes wrong. Pick its corner, opacity, shortcut, or hide it in a game from its "…" menu.
- **Open roblox.com as an account**: from an account's menu, open the Roblox website already signed in as that account, in its own window.
- **Session health**: a dot next to each account shows if it's signed in, hasn't been used in a while, or needs you to log in again (one click).
- **Hide alts from the taskbar**: hide an account's Roblox window from the taskbar and Alt+Tab. Bring them all back from the tray or the running list.
- **Pending Robux**: see the Robux that's still pending, per account and in total, in the Robux overview.
- **Shortcuts**: press ? to see them all. Ctrl+Enter plays and Ctrl+. stops launching.
- **Groups in Who plays**: add or remove a whole group of accounts in one click, and reorder with Alt+arrows.
- **Reduce motion**: a setting in Settings › Appearance.
- **Your Discord plan for clips**: Copy now knows if you have Nitro, so it only warns when a clip is too big for your plan (20 MB free, 50 MB Nitro Basic, 500 MB Nitro). The Discord app on your PC tells Rovex which plan you have (never your login), or you can pick it yourself in Settings › Roblox.
- **Timeline**: from an account's menu, see when it joined, left, was kicked, lost connection or crashed, why, and what to do about it. Accounts and the running list also show why an account dropped. It stays on your PC, and you can turn it off in Settings › Privacy.
- **Roblox problems**: Rovex tells you when Roblox itself is having problems, what's affected and since when. Before several accounts start you can choose to wait, and they start by themselves when it's back. Auto-rejoin waits too.
- **For this game**: a game can remember who plays it, its graphics profile, region and private server. Play uses them, and you can still play with someone else just once. An account's own FPS always wins, and your normal settings go back afterwards.
- **Account checkup**: see which accounts have 2-step verification and a verified email, and fix it in one click. Rovex only reads whether it's on, and never keeps the email.
- **What Rovex talked to**: Settings › Privacy lists every site Rovex contacted this session, and why.
- **Desktop shortcuts**: start a preset or an account from your desktop (right-click a preset, or use an account's menu). There's a command line too: `--preset`, `--account`, `--close-all` and `--show`.
- **Game updates**: starred games show "Updated 5 min ago". You can also turn on a notification, which tells you when you're still on an older server.
- **Move to a new PC**: one encrypted backup file with your accounts, presets, alts, games, private server links, settings and history. Importing shows what it adds first, and nothing on the PC is removed. You'll find it in Settings › Privacy & security › Backup, with a small reminder when you haven't made one in a while.
- **Before accounts start**: Rovex says which accounts need to log in or are already playing, and if your PC may not have room for all of them. Fix it there, or start just the ready ones.
- **Several screens**: Arrange can use this screen, all of them or one by name, and give your alts a screen of their own. Presets can have their own. Too many windows to fit are piled neatly, and Rovex says how many fit.
- **While you were away**: after 20 minutes or more, Home shows who dropped and why, who was rejoined, who is still playing and for how long. You can turn it off in Settings.
- **Update when they're closed**: an update now says which accounts are playing, and can wait until you close them.
- **Tips**: short tips show up the first time you open a page, and you can turn them off anytime.

### Changed
- **A simpler sidebar**: Home, Library, Friends, Accounts and Clips. Private servers are a tab in Library, Chat is a tab in Friends, and the live previews are the Windows tab in Accounts. Search is in the top bar (Ctrl+K).
- **Who plays**: pick who plays in one place, at the top right. Every Play button now says who's playing, like "Play · 3 accounts", and each account on the Accounts page has a Plays switch. The checkboxes are only for doing things to several accounts at once.
- **Home**: a smaller banner, with your presets right under it.
- **Tutorial**: 4 quick steps (add your account, pick a game, choose who plays, press Play), and nothing starts by itself.
- **Adding an account**: the Roblox website and Quick Login come first. Username and password, session cookies and imports are under Advanced, with a warning to never paste your cookie anywhere someone asks for it.
- **Easier to read**: faint text, checkboxes and input borders have more contrast, and text on buttons stays readable whatever accent color you pick.
- **Update notifications**: Rovex now looks for updates every 30 minutes. When one comes out you get a Windows notification with its name. Click it to see what's new and update in one click.
- **Phone control**: what your phone and PC send each other is now encrypted, so you need to scan the QR code once more on each phone. Phones you haven't used in 30 days are disconnected, you can disconnect all of them at once, and Rovex won't open phone control on a public Wi-Fi unless you allow it. While Rovex is locked, phones wait until you unlock it.
- **A smaller download**: Rovex's installer is about a third smaller, so updates arrive faster. It also checks Rovex before installing it, and your old Rovex stays until the new one is in place.
- **Auto-rejoin decides by the reason**: it goes back by itself after a lost connection, a server shutdown or a crash. After a kick, or when the account joined somewhere else, Rovex says why and asks first. Many accounts rejoin one after the other, with one message. Rejoining after an idle kick has its own setting.
- **For this game, everywhere**: what a game remembers also counts from presets, desktop shortcuts, clips and your phone.
- **Safer backups**: new backup files need a password of 10 characters and only hold saved Roblox passwords if you tick it. Older files still import.
- **Several accounts at once**: the notice is clearer about the risk.
- **Under the hood**: a big cleanup of Rovex's code, so fixes and new features come faster.

### Fixed
- **Turbo and FPS**: Turbo no longer drops you to 60 FPS. Every account keeps its own FPS, graphics and volume: accounts with the same settings open together, one group after the other. If you change your FPS in Roblox, Rovex keeps it.
- **Launching several accounts**: one that breaks no longer stops the others, and Play goes back to normal afterwards.
- **Why it rejoined**: auto-rejoin messages now say the reason in plain words.
- **Auto-rejoin**: it no longer takes a kick, a lost connection or a crash for leaving the game. A short internet or Roblox outage no longer makes it give up (it keeps trying for up to 30 minutes), it won't close another account's window to rejoin, and accounts that dropped before Rovex started aren't rejoined by surprise.
- **Starting an account closed the others**: when Roblox tries out another version on one of your accounts, its installer could run on every launch (also from "Bring here" and Rejoin) and close every Roblox window. Rovex now opens the right version directly, which is also faster, and asks first when a real Roblox update would close the others.
- **Private servers**: Rejoin and auto-rejoin go back to the private server the right way.
- **Wrong game**: Retry could start a different game, a private link could carry over to another game, and two accounts could claim the same window.
- **After restarting Rovex while you play**: several accounts work again once one Roblox window closes, not only after all of them.
- **Log ins**: an account's renewed session is no longer lost when you lock Rovex during a call, or quit Rovex after changing something in "Open roblox.com as".
- **Finding Roblox**: also when it's installed for the whole PC, and Rovex explains it when only the Microsoft Store version is there.
- **Clips clean-up**: it never switches to every game by itself once the picked game's clips are gone.
- **Updates**: a shortcut that can't be updated no longer shows as a failed update.
- **Stop**: it now stops every account that's still starting, including fast and parallel launches, and closed windows no longer come back.
- **Rejoin**: "Rejoin this server" puts you back in the same server, and "Back to previous server" is a separate choice.
- **Launching after a wait**: accounts that waited for others before starting no longer fail with an expired join ticket.
- **FPS, graphics and volume per account**: if they couldn't be set when an account starts, Rovex tries again and tells you, instead of starting it as if nothing happened.
- **Safer files**: when another program is using Roblox's settings file, Rovex tries again instead of overwriting it directly, which could leave it half written.
- **Closing Roblox**: Rovex now checks and closes exactly the same Roblox process, so another program can't be closed by mistake.
- **Spotify in the overlay**: much less lag. Next shows the next song right away when Rovex knows it, changes you make in the Spotify app show up almost at once, playing from Rovex starts sooner, and playlists with thousands of songs scroll smoothly. It also asks Spotify less often.
- **Most played**: a game that moves you between several places, like Grand Piece Online, is now listed once, with its whole time. Your Library, the game's page and the Clips game filter count it as one game too, including time from before this update.
- **Chat**: when it can't load, it no longer asks Roblox again and again.
- **Clips**: folders with thousands of videos now show the newest ones, and the Game filter opens.
- **Home**: the arrows on the banner no longer cover the Play button.
- **Settings**: changing a setting is instant again, even with a big library.
- **Crashes**: if something goes wrong inside Rovex, it's written to the log instead of closing the whole app.

## Clips, private servers and Robux
_0.2.2 · 2026-11-23_

### New
- **Clips**: watch your Roblox clips from Medal, Roblox, NVIDIA, Xbox Game Bar or your own folders right in Rovex. Each clip shows the game and the account you were playing on when you recorded it. Click the game to open its page, see which of your other accounts were there, play the game again with the same account, copy a clip and paste it straight into Discord, and trim it to the part that matters. A Storage view shows how much space your clips take per game and can move old ones to the Recycle Bin. Games show their clips on their page and in the Library, and the overlay tells you when a new clip is saved while you play.
- **Private servers**: one page with every private server your accounts own or can join, across all your games. See who owns it, whether it's active or when it renews, and join with any of your accounts that can get in.
- **Robux overview**: see the total Robux of all your accounts on the Launchpad, how it changed over the last 7 and 30 days, a chart over time and how much each account has. Click the Robux card, or the total on the Accounts page, to open it. Your history stays on your PC.
- **Help improve Rovex**: you can choose to share anonymous usage stats, like which features are used and whether something crashed. It's off unless you say yes, never includes your accounts, names, games or friends, and you can change it anytime in Settings › About & help. See rovexlauncher.com/privacy.html.

### Changed
- **A new logo**: Rovex has a new look, with a new app icon, and the opening and installer animations to match.
- **Friends in the overlay**: a refresh button next to the search, and the list now updates every minute instead of every five.

## Discord, YouTube and a real tutorial
_0.2.1 · 2026-11-23_

### New
- **Discord**: show the game you're playing on your Discord profile, with the server's region and an optional join button. Main account only, and off until you turn it on in Settings › Roblox, where a short guide shows how to set it up.
- **YouTube in the overlay**: watch YouTube without leaving the game. Pop the video out into a small player over Roblox, drag and resize it, make it see-through, or let your clicks go through it to the game.
- **Tutorial**: a hands-on tutorial walks you through adding your accounts, your main account, playing several at once, joining games and presets. It picks up where you left off, and you can restart it from Settings › About & help.
- **Your own Spotify app**: a step-by-step guide in Settings › Appearance › Spotify to connect Spotify through your own free Spotify app.

### Changed
- **Spotify for everyone**: if Spotify doesn't let your account use Rovex's direct connection, the overlay opens Spotify's own player instead, with your playlists and search.

### Fixed
- **Adding your first account**: the Launchpad now shows it right away, with its name, Robux and games, and it becomes your main account.
- **Update log window**: the Close button no longer sits on top of the text when the notes are long.

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
