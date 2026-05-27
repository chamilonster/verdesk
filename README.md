# Verdesk

**The modulated vision and control layer for AI agents.** Verdesk is a local MCP server for Windows that hands AI agents *deltas* — not full screenshots — together with plain text and UI Automation. Result: **89–93% fewer vision tokens** on a typical session, with no loss of control.

→ Landing: **[verdesk.app](https://verdesk.app)**
→ EULA: [LICENSE](./LICENSE)
→ Skill for Claude Code: [chamilonster/verdesk-skill](https://github.com/chamilonster/verdesk-skill)

---

## Install

1. Grab the latest setup from **[Releases](https://github.com/chamilonster/verdesk/releases/latest)** (`Verdesk_x.y.z_x64-setup.exe`, ~197 MB — bundles WebView2 offline so it works on stripped Windows installs too).
2. Run it. Windows SmartScreen may warn (not code-signed yet) — *More info* → *Run anyway*.
3. Verdesk lives in your tray. First run opens **Settings** for onboarding.

Verify the download (optional, recommended):

```powershell
Get-FileHash Verdesk_x.y.z_x64-setup.exe -Algorithm SHA256
```

Compare against `SHA256SUMS.txt` on the same Release.

> Portable variant: `verdesk.exe` (15 MB, no installer, no admin needed) is also published on each Release.

---

## Connect Claude Code (Local mode)

Verdesk runs an MCP server on loopback. Add it to your client:

```bash
claude mcp add --transport http verdesk http://127.0.0.1:47802/mcp
```

That's it — your AI agent now has `look`, `capture`, `act_uia`, `extract_text`, profiles and the rest.

For **LAN** (same network) and **WAN** (over the internet via SSH tunnel or Tailscale), see *Settings → Acceso*. Both require a **Pro** license.

---

## Pro features

| | Free | Pro ($49/year) |
|---|:---:|:---:|
| Modulated vision pipeline (deltas, hashing, buffer, history) | ✓ | ✓ |
| All base tools (`look`, `capture`, `act_uia`, profiles, …) | ✓ | ✓ |
| Local-mode MCP server | ✓ | ✓ |
| Remote access (LAN / WAN) | — | ✓ |
| `run_command` tool | — | ✓ |
| Commercial use | — | ✓ (1 developer · up to 3 devices) |

→ **[Buy Pro](https://clevercat.lemonsqueezy.com/checkout/buy/785996c1-daa0-47e1-a720-4fd1e660e496)** — $49/year subscription. Pay with card, receive a license key by email, paste it in *Settings → Licencia*.

---

## Compatibility

- Windows 10 / 11 (x64)
- Works with **Claude Code**, **GPT** (any MCP-compatible client) and **local models**
- No telemetry · No account required · Single executable

---

## Reporting bugs

Open an issue with: Verdesk version (*Settings → About*), Windows version, mode (Local/LAN/WAN) and steps to reproduce.

Security vulnerabilities: see [SECURITY.md](./.github/SECURITY.md).

---

## License

Verdesk is **proprietary, source-available only for the prebuilt binaries** distributed here. The full EULA is in [LICENSE](./LICENSE).

© clever.cat — Camilo Brossard · `camilo.brossard@gmail.com`
