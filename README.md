# Heroic Games Launcher — Void Linux Package Source

This repository maintains the XBPS template source and automation workflows to package and build **Heroic Games Launcher** for Void Linux (x86_64).

**Native Integration**:
The binary is installed directly under `/opt/heroic` and registers application icons, desktop entries, and mime types.

## Layout

- `template`: The Void Linux XBPS build template.
- `.github/workflows/scrape-heroic.yml`: Scrapes for new releases, updates version/checksums, and triggers the builder.
- `.github/workflows/build-xbps.yml`: Boots the `xbps-src` environment, builds the `.xbps` package, and deploys it as a GitHub Release.
