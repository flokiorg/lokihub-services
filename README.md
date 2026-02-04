# Lokihub Services

This repository hosts static configuration and discovery files used by [Lokihub](https://github.com/flokiorg/lokihub).

## Contents

*   **`services.json`**: Directory of recommended community services (Explorers, Swap Services, Relays, etc.) that users can select during setup.
*   **`rates.json`**: Current exchange rates and currency symbols (e.g., FLC/USD).
*   **`currencies.json`**: List of supported fiat currencies.
*   **`info.json`**: General information and motd (message of the day).


## Usage

Lokihub fetches these files to provide up-to-date defaults and service options to users tailored for the Flokicoin ecosystem.

### Service Schemas

**General Services (Explorers, Relays, Swap Services)**

Most services use `url` for their web address:

```json
{
  "name": "Service Name",
  "url": "https://service.url",
  "description": "Brief description"
}
```

**Suggesting a Messageboard**

Messageboards use `nwc` for the connection string (e.g., `nostr+walletconnect://...`):

```json
{
  "name": "Funrun Board",
  "nwc": "nostr+walletconnect://pubkey?relay=...",
  "description": "Collects zaps for Funrun game winner distributions"
}
```

### Adding an LSP

To add a Lightning Service Provider (LSP) to `services.json`, add an entry to the `lsps` array. Note that LSPs use `connection` for the connection string and `url` for the website:

```json
{
  "name": "My LSP",
  "connection": "pubkey@host:port",
  "url": "https://my-lsp-website.com",
  "description": "Supports JIT Channels & Inbound Liquidity"
}
```

## Contributing

We welcome contributions to the directory! To add or update a service:

1.  **Fork the repository.**
2.  **Edit `services.json`** to include your service. Please ensure:
    *   The `url` is valid and accessible.
    *   The `description` is concise and accurate.
    *   For LSPs, the `connection` is a valid Lightning connection string.
3.  **Validate your JSON** to ensure there are no syntax errors.
4.  **Submit a Pull Request** with a brief description of your changes.

