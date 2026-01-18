# Validator Node Guide

Deploy and manage a Namada validator node on mainnet.

## System Requirements

| Category | Requirements |
|----------|--------------|
| CPU | 8+ cores |
| RAM | 32+ GB |
| Storage | 500+ GB NVMe SSD |
| Bandwidth | 100+ MBit/s |
| OS | Ubuntu 22.04/24.04 (recommended) |

## Installation

1. Launch Valley of Namada:
   ```bash
   bash <(curl -s https://raw.githubusercontent.com/hubofvalley/Mainnet-Guides/main/Namada/resources/valleyofNamada.sh)
   ```
2. Select **"Node Interactions"** → **"Deploy Validator Node"**
3. Follow the interactive prompts

### What Gets Installed

| Component | Details |
|-----------|---------|
| **namadad** | Namada node daemon |
| **namadad.service** | Systemd service |
| **Data directory** | `$HOME/.local/share/namada` |

## Creating a Validator

1. Launch Valley of Namada
2. Select **"Validator/Key Interactions"** → **"Create Validator"**
3. Enter:
   - Validator name
   - Commission rate (e.g., 0.05)
   - Max commission rate change (e.g., 0.05)
   - Security contact email
   - Wallet name/alias

## Updating

1. Launch Valley of Namada
2. Select **"Node Interactions"** → **"Update Namada Version"**

## Service Management

| Action | Menu Path |
|--------|-----------|
| Show status | **"Node Interactions"** → **"Show Validator Status"** |
| Show logs | **"Node Interactions"** → **"Show Validator Logs"** |
| Restart | **"Node Management"** → **"Restart Validator Node"** |
| Stop | **"Node Management"** → **"Stop Validator Node"** |
| Delete | **"Node Management"** → **"Delete Validator Node"** |

## Adding Seeds/Peers

1. Launch Valley of Namada
2. Select **"Node Interactions"** → **"Add Seeds"** or **"Add Peers"**
3. Choose manual entry or Grand Valley's endpoints

## Backup

1. Launch Valley of Namada
2. Select **"Node Management"** → **"Backup Validator Key"**

This copies `priv_validator_key.json` to your `$HOME` directory.

## Related Documentation

- [Wallet Guide](wallets.md)
- [Staking Guide](staking.md)
- [Snapshots Guide](snapshots.md)
