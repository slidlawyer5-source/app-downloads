# Dylan's apps (Windows installers)

Downloads for friends. Pick an app, open its release page, download the `.exe` and run it.
Everything here is for **Windows 10/11, 64-bit**.

| App | What it does | Download | Admin prompt? |
|---|---|---|---|
| **LiteRGB 1.5.0** | Lightweight RGB control that replaces Razer Synapse / Corsair iCUE / Armoury Crate lighting | [LiteRGB release](https://github.com/slidlawyer5-source/app-downloads/releases/tag/litergb-v1.5.0) | No |
| **ClearQueue 3.2.0** | Network tool: Upload Guard (stops uploads from lagging your games), speed test, NAT & ports, VPN check | [ClearQueue release](https://github.com/slidlawyer5-source/app-downloads/releases/tag/clearqueue-v3.2.0) | Yes (installs a background service) |
| **Social Hub 1.0.0** | Self-hosted chat with voice, video and screen share for our group | [Social Hub release](https://github.com/slidlawyer5-source/app-downloads/releases/tag/socialhub-v1.0.0) | No |

## Updates

LiteRGB 1.5.0+ and ClearQueue 3.2.0+ have a **Check for updates** button that downloads the newest version from this page, checks its SHA-256 and installs it. No GitHub account needed.

## "Windows protected your PC"

The installers aren't code-signed yet, so Windows SmartScreen will warn about an unknown publisher.
Click **More info**, then **Run anyway**. Your browser may also ask you to **Keep** the download.

## Checking a download is safe

Every installer was scanned with Microsoft Defender before upload (no threats found). Each release has a
`SHA256SUMS` file. To check you got the exact same file, open PowerShell in your Downloads folder and run:

```powershell
Get-FileHash .\LiteRGB-Setup-1.5.0-x64.exe
```

The `Hash` it prints must match the one on the release page (upper or lower case doesn't matter).

| File | SHA-256 |
|---|---|
| LiteRGB-Setup-1.5.0-x64.exe | `9d594826b8dcd18b1b2af6a5f84126c92b600e5903752fecb5cc168215ce24a6` |
| ClearQueue-Setup-3.2.0-x64.exe | `de85cb658ae9baa69c7e9701aec9fcec5498b5b5d4bb76bb6360f658798ba578` |
| SocialHub-Setup-1.0.0.exe | `8200efd0697f26584c4b8a01c4195f48152810826d9462e344790374a3cee0bc` |

## Notes per app

- **LiteRGB:** close Razer Synapse, iCUE, Armoury Crate or other RGB apps first, or they'll fight over the lights.
  Tested devices: Razer Basilisk V3, Corsair K55 RGB PRO, ASUS Aura motherboards. Other devices
  (Windows Dynamic Lighting devices, other Razer gear) get basic lighting and show as "Untested". Tell Dylan what works.
- **ClearQueue:** Upload Guard starts **off**. Turn it on in the app. To remove it, use
  Windows Settings > Apps so it can undo its network changes.
- **Social Hub:** only the person **hosting** the hub needs to install it. Everyone else just opens the
  invite link Dylan sends in a browser.

Uninstall any app from **Windows Settings > Apps**.
