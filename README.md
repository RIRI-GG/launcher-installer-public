<p align="center">
  <img src="https://raw.githubusercontent.com/RIRI-GG/launcher-installer-public/main/assets/riri-logo-1024.png" width="120" alt="RIRI Launcher Logo">
</p>

<h1 align="center">RIRI Launcher</h1>
<p align="center">
  <b>Cross-platform game launcher installer</b><br>
  Native binaries • GPG-signed • Auto-updating
</p>

<p align="center">
  <a href="#download">Download</a> •
  <a href="#installation">Installation</a> •
  <a href="#verification">Verification</a> •
  <a href="#changelog">Changelog</a>
</p>

---

## Download

The latest release is available on the [Releases](../../releases) page.

| Platform | Architecture | Download | Size |
|----------|-------------|----------|------|
| **Windows** | x64 | `riri-launcher-windows-x64.exe` | ~70 MB |
| **macOS** | ARM64 (Apple Silicon) | `riri-launcher-macos-arm64.zip` | ~70 MB |
| **macOS** | x64 (Intel) | `riri-launcher-macos-x64.zip` | ~70 MB |
| **Linux** | x64 | `riri-launcher-linux-x64.tar.gz` | ~70 MB |
| **Linux** | ARM64 | `riri-launcher-linux-arm64.tar.gz` | ~70 MB |

> **Note:** Windows ARM64 devices (Snapdragon/CoPilot+ PC) can run the **x64** build via built-in WOW64 emulation.

---

## Installation

### Windows
1. Download `riri-launcher-windows-x64.exe`
2. Run the executable — no installer needed
3. The launcher will check for updates automatically

### macOS
1. Download the appropriate `.zip` for your Mac (ARM64 for Apple Silicon, x64 for Intel)
2. Extract `RIRI Launcher.app`
3. Drag to Applications or run directly
4. If Gatekeeper blocks the app, right-click → Open

### Linux
1. Download the `.tar.gz` for your architecture
2. Extract: `tar xzf riri-launcher-linux-*.tar.gz`
3. Run: `./riri-launcher-linux-*/riri-launcher`
4. Optionally install the `.desktop` file and icon:
   ```bash
   sudo cp -r riri-launcher-linux-*/usr/share/* /usr/share/
   ```

---

## Verification

All releases are cryptographically signed.

| File | Purpose |
|------|---------|
| `checksums.txt` | SHA-256 checksums for every binary |
| `checksums.txt.asc` | GPG signature (signed by `ci@riri.gg`) |
| `version.json` | Machine-readable release metadata |
| `CHANGELOG.md` | Full changelog from the private source repo |

Verify the GPG signature:
```bash
gpg --verify checksums.txt.asc checksums.txt
```

Then verify your download:
```bash
sha256sum -c checksums.txt
```

---

## System Requirements

| | Minimum |
|---|---|
| **OS** | Windows 10/11, macOS 12+, Ubuntu 22.04+ (or equivalent) |
| **RAM** | 2 GB |
| **Storage** | 150 MB |
| **Internet** | Required for initial download and updates |

---

## Changelog

See [Releases](../../releases) for per-version changelogs, or download `CHANGELOG.md` from any release.

---

## License

See [LICENSE](./LICENSE) for the full RIRI Launcher Software License Agreement.

> This repository contains **only published release binaries**. Source code is maintained in a private repository.

---

<p align="center">
  <sub>© RIRI. All rights reserved.</sub>
</p>
