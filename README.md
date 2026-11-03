# Dylan's apps (Windows installers)

Private downloads for friends. Pick an app, open its release page, download the `.exe` and run it.
Everything here is for **Windows 10/11, 64-bit**.

| App | What it does | Download | Admin prompt? |
|---|---|---|---|
| **LiteRGB 1.4.0** | Lightweight RGB control that replaces Razer Synapse / Corsair iCUE / Armoury Crate lighting | [LiteRGB release](https://github.com/slidlawyer5-source/app-downloads/releases/tag/litergb-v1.4.0) | No |
| **ClearQueue 3.1.0** | Network tool: Upload Guard (stops uploads from lagging your games), speed test, NAT & ports, VPN check | [ClearQueue release](https://github.com/slidlawyer5-source/app-downloads/releases/tag/clearqueue-v3.1.0) | Yes (installs a background service) |
| **Social Hub 1.0.0** | Self-hosted chat with voice, video and screen share for our group | [Social Hub release](https://github.com/slidlawyer5-source/app-downloads/releases/tag/socialhub-v1.0.0) | No |

## "Windows protected your PC"

The installers aren't code-signed yet, so Windows SmartScreen will warn about an unknown publisher.
Click **More info**, then **Run anyway**. Your browser may also ask you to **Keep** the download.

## Checking a download is safe

Every installer was scanned with Microsoft Defender before upload (no threats found). Each release has a
`SHA256SUMS` file. To check you got the exact same file, open PowerShell in your Downloads folder and run:

```powershell
Get-FileHash .\LiteRGB-Setup-1.4.0-x64.exe
```

The `Hash` it prints must match the one on the release page (upper or lower case doesn't matter).

| File | SHA-256 |
|---|---|
| LiteRGB-Setup-1.4.0-x64.exe | `85d24ae55e646ea8ee5f92cb0b0bd2d5ec4e590b80133dca765f96888ab833bf` |
| ClearQueue-Setup-3.1.0-x64.exe | `85ccab067ba9f2988ee07520de5e8c845b7836a9d973f213f206062085c89e92` |
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
