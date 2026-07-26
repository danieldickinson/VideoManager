# VideoManager

A Windows app for downloading, organising and remastering video — subscriptions that pull new videos
automatically, AI upscaling, VR180 conversion, trimming and tagging, all in one library.

This repository is the **download home**. The source is private; every release below records the
exact commit it was built from.

## Download

Grab the newest [release](../../releases) and pick the file matching your PC — Windows Settings ▸
System ▸ About ▸ *System type* tells you which:

| File | For |
|---|---|
| `VideoManager-<version>-win-x64.msi` | Intel / AMD PCs. The normal choice. |
| `VideoManager-<version>-win-arm64.msi` | Windows on ARM (Snapdragon, and similar). |
| `…-win-x64.zip` / `…-win-arm64.zip` | The same build as a portable folder — no installer, unzip anywhere and run the `.exe` inside. |

The MSIs install per-machine, upgrade in place over an older version, and appear in Add/Remove
Programs under the calendar version.

Setup is unsigned, so Windows SmartScreen will warn on first run — *More info ▸ Run anyway*.

### Requirements

Windows 10 or 11, plus the **Microsoft Edge WebView2 Runtime** — preinstalled on Windows 11 and on
current Windows 10. If an installer stops and tells you it's missing, install the free
[Evergreen Bootstrapper](https://developer.microsoft.com/microsoft-edge/webview2/) and run it again.

### WinGet

Each release also ships a WinGet manifest for local installs:

```
winget install --manifest <folder containing the release's manifest>
```

## Updating

Run the newer installer — it upgrades in place. VideoManager can also do it for you: **Settings ▸
Check for VideoManager updates** shows what changed and installs it on request. The optional daily
check is off until you turn it on, sends nothing but an anonymous request for this repository's
releases, and never installs anything on its own.

Bundled components (ffmpeg, yt-dlp, Deno) update on their own faster cadence and are never downgraded
by an app upgrade — yt-dlp in particular self-updates, because it breaks whenever its target sites
change.

## Versioning

`YY.M.DDBB` — year since 2000, month, then the day × 100 plus that day's build counter. So
`26.7.2401` is the first build cut on 24 July 2026 and `26.7.2402` the second. Later releases are
always numerically larger.

Releases up to **26.7.2505** were published in the shared
[danieldickinson/releases](https://github.com/danieldickinson/releases) repo and remain there;
everything from 26.7.2701 onward lives here.

## Status

A personal project, shared as-is — no warranty and no support promise.
