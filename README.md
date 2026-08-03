# NSFRG's DCS Crew Chief — Release Depot

**This repository holds releases only. There is no source code here.**

Crew Chief gets your PC ready to fly DCS World, then puts it back exactly how it was.

It shuts down the background apps that inject themselves into DCS — overlays like RTSS, Discord
and Steam are a leading cause of stutter and crashes in VR — launches your support apps in the
right order, watches the flight, and restores everything afterwards.

It does **not** modify core DCS files, and it is multiplayer safe.

---

## Download

Grab the newest **`app-*`** release from the [Releases page](../../releases).

Crew Chief checks this depot on launch and will offer updates itself, so this is normally a
first-install step only.

## What's in a release

| Asset | What it is | Size |
|---|---|---|
| `CrewChief-*.zip` | The application. This is what updates most often. | small |
| `OptimizationBundle-*.zip` | DLSS libraries, NVIDIA Inspector profiles and DCS performance mods. Changes rarely. | large |

The two are versioned separately so a routine app update does not re-download the bundle.

## Installing

1. Unzip somewhere you can write to — for example `C:\Games\Tools\Crew Chief`.
   **Avoid `C:\Program Files`**, which needs administrator rights to write logs and settings.
2. Run `NullsetForge.CrewChief.exe`.
3. First run walks you through setup and explains what each step does.

Your settings, logbook and crash reports live in the install folder and are never overwritten by
an update.

## Windows will warn you the first time

Crew Chief is **not code-signed**, so Windows SmartScreen will show a blue
*"Windows protected your PC"* box the first time you run it.

That is expected. It means the file has no purchased signing certificate — not that anything is
wrong with it. To continue: click **More info**, then **Run anyway**.

### Updates are signed, even though the app isn't

Every release asset carries a **cryptographic signature** in its notes, made with a private key
that never leaves the developer's machine.

Crew Chief verifies that signature before applying any automatic update, and refuses anything it
cannot prove came from us. So while Windows can't vouch for the app on first download, an update
**cannot** be swapped for something malicious — not by a compromised depot, and not by anything
sitting between you and GitHub.

That is a different and stronger guarantee than a checksum, which only tells you the file
downloaded intact.

## Requirements

- Windows 10 or 11
- [WebView2 Runtime](https://developer.microsoft.com/microsoft-edge/webview2/) — already present on
  most Windows 11 machines
- DCS World, Standalone or Steam

## Something went wrong?

Crash reports are written to `Resources\_Logs\DCS Crash Logs` inside your install folder, one
folder per crash. Open the newest one, press **Copy prompt**, paste it into an AI assistant and
drag `dcs.log` in behind it — the report is built to be handed over exactly that way.

## Licence

Closed source, free for personal use. See [EULA.txt](EULA.txt).

---

[Nullset Forge](https://nullsetforge.com)
