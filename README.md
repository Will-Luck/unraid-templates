# Unraid Community Applications templates

This repository hosts the Unraid Community Applications (CA) XML templates for projects published under [Will-Luck](https://github.com/Will-Luck).

Once a template is added to the [Community Applications](https://forums.unraid.net/topic/38582-plug-in-community-applications/) feed, the apps are searchable from the **Apps** tab inside Unraid.

## Apps

| App | Image | Template |
| --- | ----- | -------- |
| [iplayer-arr](https://github.com/Will-Luck/iplayer-arr) | `ghcr.io/will-luck/iplayer-arr:latest` | [`iplayer-arr.xml`](iplayer-arr.xml) |

### iplayer-arr

BBC iPlayer Newznab indexer and SABnzbd-compatible download client for Sonarr. Calls the BBC iBL API directly and remuxes HLS to MP4 with ffmpeg. Includes an optional WireGuard VPN client for use outside the UK.

- **Web UI**: `http://[unraid-ip]:8191`
- **Volumes**: `/config` (appdata), `/downloads` (finished media)
- **Required env**: `TZ`
- **Optional VPN env**: `VPN_ENABLED`, `VPN_PROVIDER`, `VPN_CONF`, `VPN_LAN_NETWORK`, `VPN_PIA_USER`, `VPN_PIA_PASS`, `VPN_PIA_PREFERRED_REGION`, `VPN_HEALTHCHECK_ENABLED`

> BBC iPlayer requires a UK IP address. Outside the UK, set `VPN_ENABLED=true` and configure a UK VPN endpoint in the advanced section of the template.

## Manual install (before CA approval)

While this repo is being reviewed for inclusion in the CA feed, you can still install the templates manually:

1. Copy the raw URL of the XML template, e.g.:
   ```
   https://raw.githubusercontent.com/Will-Luck/unraid-templates/main/iplayer-arr.xml
   ```
2. In Unraid, go to **Docker → Add Container**.
3. In the **Template** field at the top, paste the URL and press **Tab**.
4. Adjust ports/paths as needed and click **Apply**.

## Licence

Templates in this repository are released under the MIT licence. The applications they describe carry their own licences -- see the linked project pages.
