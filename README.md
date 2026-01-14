# Lokihub Services

This repository hosts static configuration and discovery files used by [Lokihub](https://github.com/flokiorg/lokihub).

## Contents

*   **`services.json`**: Directory of recommended community services (Explorers, Swap Services, Relays, etc.) that users can select during setup.
*   **`rates.json`**: Current exchange rates and currency symbols (e.g., FLC/USD).
*   **`currencies.json`**: List of supported fiat currencies.
*   **`info.json`**: General information and motd (message of the day).

## Usage

Lokihub fetches these files to provide up-to-date defaults and service options to users tailored for the Flokicoin ecosystem.

## Usage

### Adding an LSP

To add a Lightning Service Provider (LSP) to `services.json`, add an entry to the `lsp` array with the following structure:

```json
{
  "name": "My LSP",
  "uri": "pubkey@host:port",
  "description": "Supports JIT Channels & Inbound Liquidity"
}
```
