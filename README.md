<div align="center">

<img src="images/sportarr.png" width="120" alt="Sportarr">

# Sportarr Unraid Templates

Official Unraid Community Applications templates for [Sportarr](https://github.com/Sportarr/Sportarr),
published and maintained by the Sportarr project.

<p>
  <a href="https://github.com/Sportarr/Sportarr/releases/latest"><img src="https://img.shields.io/github/v/release/Sportarr/Sportarr?style=flat&label=release&color=blueviolet" alt="Latest release"></a>
  <a href="https://hub.docker.com/r/sportarr/sportarr"><img src="https://img.shields.io/badge/docker-sportarr%2Fsportarr-2496ED?style=flat&logo=docker&logoColor=white" alt="Docker"></a>
  <a href="https://discord.gg/YjHVWGWjjG"><img src="https://img.shields.io/badge/discord-join-7289da?style=flat&logo=discord&logoColor=white" alt="Discord"></a>
  <a href="https://sportarr.net"><img src="https://img.shields.io/badge/website-sportarr.net-blue?style=flat" alt="Website"></a>
</p>

</div>

Sportarr is a sports PVR for Usenet and BitTorrent: it monitors sports leagues
and events across hundreds of sports, grabs and organizes releases with
automatic quality upgrades, records live events from IPTV, and keeps Plex,
Jellyfin, and Emby libraries correctly identified through dedicated metadata
agents.

![Sportarr Dashboard](https://raw.githubusercontent.com/Sportarr/Sportarr/main/docs/images/dashboard.png)

## Install via Community Applications

Search for "sportarr" on the Apps tab and install.

## Install via template repository

Add this repository under Docker > Template Repositories:

```
https://github.com/Sportarr/unraid-templates
```

Then create the container from the Sportarr template.

## Configuration

| Setting | Default | Purpose |
|---|---|---|
| Web UI port | `1867` | The Sportarr web interface |
| `/config` | `/mnt/user/appdata/sportarr` | Database, settings, and logs |
| `/data` | `/mnt/user/data` | Media library root; add your sports library as a root folder inside Sportarr under this mount, and keep downloads under the same mount so imports can hardlink |
| `PUID` / `PGID` | `99` / `100` | User and group the container runs as (nobody:users) |
| `UMASK` | `022` | Permission mask for created files |
| `TZ` | `UTC` | Timezone; keeps event air times and the calendar correct |

## Support

- [Discord](https://discord.gg/YjHVWGWjjG)
- [GitHub issues](https://github.com/Sportarr/Sportarr/issues)
- [Documentation](https://github.com/Sportarr/Sportarr#readme)
