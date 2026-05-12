# foxora-memory-den-releases

Public release artifacts and auto-update manifest for [Foxora Memory Den](https://github.com/xBesh/foxora-memory-den).

## Auto-update channel

The Memory Den app fetches `latest.json` on every launch and compares its installed
version against `version` here. If a newer version is published, the app downloads
the platform-specific artifact, verifies its minisign signature against the pubkey
baked into the binary at build time (`AFF5029D5C004F1B`), and installs it.

## Layout

```
v1.0.0/
  mac/
    foxora-memory-den_1.0.0_aarch64.dmg     # manual download (Apple Silicon)
    foxora-memory-den-aarch64.app.tar.gz    # auto-update payload
    foxora-memory-den-aarch64.app.tar.gz.sig
latest.json                                  # the manifest clients fetch
```

## Manual download

| Architecture | macOS | Download |
|---|---|---|
| Apple Silicon (M1+) | 11+ | [foxora-memory-den_1.0.0_aarch64.dmg](https://raw.githubusercontent.com/xBesh/foxora-memory-den-releases/main/v1.0.0/mac/foxora-memory-den_1.0.0_aarch64.dmg) |

All releases are signed with `Developer ID Application: Madhav Parashar (A65TNJAWCQ)`,
notarized by Apple, and stapled (offline-validatable).
