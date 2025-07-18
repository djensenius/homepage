# Homepage Configuration

This repository contains configuration files for [Homepage](https://gethomepage.dev), a modern, fully static, fast, secure, and customizable dashboard for your homelab.

## Overview

Homepage is a highly customizable application dashboard and homepage. This repository contains the YAML configuration files that define the layout, services, widgets, and other settings for your Homepage instance.

## Configuration Files

### Core Configuration Files

#### `settings.yaml`
**Purpose**: General application settings and layout configuration
- **Title**: Sets the page title (currently "FluxHaus")
- **Stats**: Enables/disables statistics display
- **Providers**: API keys for weather services (OpenWeatherMap, WeatherAPI)
- **Layout**: Defines the structure and organization of service groups

**Key Features**:
- Responsive layout with customizable columns
- Group-based organization (Group A, Group B, Group C)
- Header visibility controls
- Row and column styling options

#### `services.yaml`
**Purpose**: Defines all the services displayed on your homepage
- **Organization**: Services are organized into groups (Network, Media, Other Containers, etc.)
- **Widgets**: Each service can have an associated widget showing live data
- **Links**: Direct links to service web interfaces

**Service Categories**:
- **Network**: Pi-hole, UniFi, TrueNAS, Portainer, Tailscale, Homebridge
- **Media**: Plex, Komga, AudioBookShelf
- **Other Containers**: Watchtower, Radarr, Sonarr, Readarr, Mylar, SABnzbd, qBittorrent, Prowlarr
- **System Monitoring**: Glances widgets for CPU, memory, disk usage, network stats

#### `widgets.yaml`
**Purpose**: Configures information widgets displayed on the homepage
- **Search Widget**: Custom search provider (Kagi) with autocomplete
- **Weather Widget**: OpenMeteo weather information for Kitchener
- **System Monitoring**: Glances integration for server statistics

#### `bookmarks.yaml`
**Purpose**: Defines bookmark collections for quick access to frequently used sites
- **Developer Tools**: GitHub repositories and development resources
- **General Bookmarks**: Commonly accessed websites

### Integration Configuration Files

#### `docker.yaml`
**Purpose**: Docker integration settings (currently commented out)
- **Host Configuration**: Docker daemon host and port
- **Socket Configuration**: Docker socket path for local installations

#### `kubernetes.yaml`
**Purpose**: Kubernetes cluster integration (minimal configuration)
- Used for connecting to Kubernetes clusters to display pod and service information

#### `proxmox.yaml`
**Purpose**: Proxmox Virtual Environment integration (commented out)
- **URL**: Proxmox server URL
- **Authentication**: Token-based authentication setup

### Customization Files

#### `custom.css`
**Purpose**: Custom CSS styling (currently empty)
- Override default Homepage styles
- Add custom themes or branding

#### `custom.js`
**Purpose**: Custom JavaScript functionality (currently empty)
- Add custom behavior or integrations
- Extend Homepage functionality

## Environment Variables

This configuration uses several environment variables for API keys and sensitive information:

- `HOMEPAGE_VAR_PIHOLE_API_KEY`: Pi-hole API key
- `HOMEPAGE_VAR_UNIFI_KEY`: UniFi controller API key
- `HOMEPAGE_VAR_TRUENAS_KEY`: TrueNAS API key
- `HOMEPAGE_VAR_PORTAINER_KEY`: Portainer API key
- `HOMEPAGE_VAR_TAILSCALE_KEY`: Tailscale API key
- `HOMEPAGE_VAR_HOMEBRIDGE_USER`: Homebridge username
- `HOMEPAGE_VAR_HOMEBRIDGE_PASSWORD`: Homebridge password
- `HOMEPAGE_VAR_PLEX_TOKEN`: Plex authentication token
- `HOMEPAGE_VAR_KOMGA_TOKEN`: Komga API token
- `HOMEPAGE_VAR_AUDIOBOOKSHELF_KEY`: AudioBookShelf API key
- `HOMEPAGE_VAR_WATCHTOWER_KEY`: Watchtower API key
- `HOMEPAGE_VAR_RADARR_TOKEN`: Radarr API token
- `HOMEPAGE_VAR_SONARR_TOKEN`: Sonarr API token
- `HOMEPAGE_VAR_READARR_TOKEN`: Readarr API token
- `HOMEPAGE_VAR_MYLAR3_KEY`: Mylar3 API key
- `HOMEPAGE_VAR_SABNZB_KEY`: SABnzbd API key
- `HOMEPAGE_VAR_QBITTORRENT_USER`: qBittorrent username
- `HOMEPAGE_VAR_QBITTORRENT_PASSWORD`: qBittorrent password
- `HOMEPAGE_VAR_PROWLARR_KEY`: Prowlarr API key

## Setup Instructions

1. **Clone this repository** to your Homepage configuration directory
2. **Set environment variables** for all the API keys and credentials listed above
3. **Update IP addresses** in the configuration files to match your local network setup
4. **Customize services** by modifying `services.yaml` to match your homelab setup
5. **Adjust widgets** in `widgets.yaml` based on your monitoring preferences
6. **Configure bookmarks** in `bookmarks.yaml` with your frequently accessed sites

## Network Configuration

The current configuration assumes the following network setup:
- **Main Server**: 192.168.1.87 (running most services)
- **NAS**: 192.168.1.205 (TrueNAS and Plex)
- **Router**: 192.168.1.1 (UniFi controller)

Update these IP addresses to match your network topology.

## Service Integration

### Widget Types Supported
- **Pi-hole**: Network-wide ad blocking statistics
- **UniFi**: Network equipment monitoring
- **TrueNAS**: NAS storage and pool information
- **Portainer**: Docker container management
- **Tailscale**: VPN connection status
- **Homebridge**: HomeKit accessory management
- **Plex**: Media server statistics
- **Komga**: Comic book library management
- **AudioBookShelf**: Audiobook library management
- **Watchtower**: Docker container updates
- **Radarr/Sonarr/Readarr**: Media automation tools
- **Mylar**: Comic book automation
- **SABnzbd**: Usenet downloader
- **qBittorrent**: BitTorrent client
- **Prowlarr**: Indexer management
- **Glances**: System monitoring

## Documentation Links

- **Homepage Documentation**: [https://gethomepage.dev](https://gethomepage.dev)
- **Configuration Guide**: [https://gethomepage.dev/configs/](https://gethomepage.dev/configs/)
- **Services Configuration**: [https://gethomepage.dev/configs/services/](https://gethomepage.dev/configs/services/)
- **Widgets Configuration**: [https://gethomepage.dev/configs/info-widgets/](https://gethomepage.dev/configs/info-widgets/)
- **Bookmarks Configuration**: [https://gethomepage.dev/configs/bookmarks/](https://gethomepage.dev/configs/bookmarks/)
- **Settings Configuration**: [https://gethomepage.dev/configs/settings/](https://gethomepage.dev/configs/settings/)
- **Docker Integration**: [https://gethomepage.dev/configs/docker/](https://gethomepage.dev/configs/docker/)

## License

This configuration is released under the MIT License. See [LICENSE](LICENSE) for details.

## Contributing

Feel free to submit issues and enhancement requests for this configuration setup.