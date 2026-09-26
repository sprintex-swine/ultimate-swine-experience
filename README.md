# Ultimate SWINE Experience — SWINE Addon

**A companion app for SWINE HD that helps you track your matches, review your play, organize teams and run bots.** It runs alongside the game on Windows. You do not need programming knowledge to use it.

## Download and install

1. Open the [latest release](https://github.com/sprintex-swine/ultimate-swine-experience/releases/latest).
2. Under **Assets**, download the file named **SwineAddon-<version>-Setup.exe**. For version 0.2.0, this is **SwineAddon-0.2.0-Setup.exe**. You do not need the source-code ZIP or the `.sha256` file to install the app.
3. Run the installer and follow the instructions.
4. Open **SWINE Addon** from the Windows Start menu, then start your supported SWINE HD game. The addon connects to the game automatically.

You need **64-bit Windows 10 (version 1809 or newer) or Windows 11**, plus your own supported SWINE HD installation. The game and its maps are not included. You do **not** need to install Python, Node.js, Git or any development tools. The installer includes the addon's required components.

The interface currently uses Hungarian labels. The sections below include those labels so you can find your way around.

## What can it do?

### Your personal dashboard — Kezdőlap

See an overview of your recorded team matches:

- Number of matches and average damage per minute.
- Average and best **APM** (actions per minute, a measure of how actively you use the controls).
- Overall **K/D ratio** (enemy units destroyed compared with your own units lost).
- Average number of rocket and mortar units, excluding the opening minute.
- Average idle percentage and your highest damage in a single match.
- Dates and maps for your damage and APM records.
- A win-rate gauge and a daily chart of wins and losses for your **last seven days with matches**. Days without matches are skipped.

The dashboard leaves out spectator matches, 1v1 matches and matches with an uncertain result. Its win/loss figures use the addon's recorded result assessment and may not always match an official game result. Older matches may not contain every statistic; missing measurements are not treated as zero.

### Live statistics and match history — Meccsek

Follow your performance while playing using small on-screen panels, then review saved match and player statistics afterwards. History includes team sizes, match length and win/loss highlighting. You can export statistics to an Excel file and send a statistics summary to the game chat.

For on-screen panels, use the game in windowed or borderless windowed mode. Start the addon **before the match begins** so it can capture the full match.

### Match recording and replay

Multiplayer match recording is enabled by default and can be switched off in Settings. Recordings are saved as `.swr` files, which can be shared with other addon users.

Select a recorded match in the history to replay it, or open a `.swr` file someone has sent you. Replay controls let you pause, change playback speed, move through the recording and switch between your side's view, the opponents' view and the whole map.

Replay playback needs a compatible game version and the map used in the recording. Create an empty lobby that you host and follow the app's preparation messages. Seeking backwards reloads the match and advances to the selected point, so it is not always instant. New recordings contain match-duration data; older recordings use an estimate.

### Team setup — Lobby

When you host a lobby, the addon helps you arrange teams using player ratings, choose a map and select starting positions. Ratings are editable directly in the player table. Missing ratings are highlighted, and team suggestions become available once everyone has a rating.

These are ratings you enter for balancing teams, not an official online ranking. The controls remain disabled until you are the host.

### Built-in bots — Botok

Choose between **Classic** and **Team Player** bots. The addon launches separate game windows for them; you join those windows to the lobby and select the Bot army. The bot components are included, so no separate developer software is needed.

### Connection troubleshooting — Lag Elemző

The Lag Analyzer reads the game's log and presents connection-related events in a table. It can help you investigate lag and see which players are associated with packet re-request events. These counts are diagnostic clues, not a direct packet-loss percentage or proof that one player caused the lag.

## Keeping the app up to date

Open **Beállítások → Frissítések keresése** (Settings → Check for updates). If a newer release is available, the app asks whether you want to install it. After you confirm, it downloads and checks the installer, closes the app, updates it and starts it again. A progress window explains what is happening.

Finish any match, replay or active bot session before updating. You do not need to uninstall the old version first. You can also download the latest installer and install it over your existing installation.

## Where are my matches stored?

Statistics and replay files are stored locally in your Windows user data folder:

```text
%LOCALAPPDATA%\SwineAddon\SWINE Addon
```

You can paste this path into the address bar of File Explorer. Replay files are in the `replays` subfolder. Updates preserve your saved data and settings. Uninstalling the app also leaves saved user data in place.

## If something does not work

- Make sure the addon is running before you start a match.
- Check that the game version is supported. The addon cannot connect to every modified game executable.
- If a replay will not start, check that its map is installed and that you are hosting an empty lobby.
- For a problem with the app, [open an issue](https://github.com/sprintex-swine/ultimate-swine-experience/issues) and describe what you were doing, your addon version and any error message. Avoid sharing private information in public logs or screenshots.

This repository distributes the Windows installer and release information. Always download installers from the [Releases page](https://github.com/sprintex-swine/ultimate-swine-experience/releases), where the current version is published.
