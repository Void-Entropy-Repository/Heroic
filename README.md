# Heroic Games Launcher — Void Linux Package Source

This repository maintains the XBPS template source and automation workflows to package and build **Heroic Games Launcher** for Void Linux (x86_64).

## Features

- **Automated Scraping**: Daily updates via GitHub Actions checking for new upstream releases of Heroic Games Launcher.
- **Automated Builds**: Integrates with `xbps-src` in a clean Ubuntu-to-Void bridge environment to package, verify, and release the binary.
- **Native Integration**: Installs the binary directly under `/opt/heroic` and registers application icons, desktop entries, and mime types.

## Repository Layout

- `template`: The Void Linux XBPS build template.
- `.github/workflows/scrape-heroic.yml`: Scrapes for new releases, updates version/checksums, and triggers the builder.
- `.github/workflows/build-xbps.yml`: Boots the `xbps-src` environment, builds the `.xbps` package, and deploys it as a GitHub Release.
