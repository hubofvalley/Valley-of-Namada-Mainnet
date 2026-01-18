<p align="center">
  <img src="resources/namadagrandvalley.png" alt="Valley of Namada Logo" width="500">
</p>

<h1 align="center">Valley of Namada Mainnet</h1>

<p align="center">
  <strong>A comprehensive toolkit for deploying and managing Namada validator nodes on mainnet</strong>
</p>

<p align="center">
  <a href="https://namada.net" target="_blank">Namada</a> •
  <a href="https://docs.namada.net" target="_blank">Official Docs</a> •
  <a href="https://github.com/hubofvalley" target="_blank">Grand Valley</a>
</p>

---

## 🚀 Overview

Valley of Namada Mainnet is an open-source project by **Grand Valley** that provides automated scripts for deploying and managing Namada validator nodes on mainnet, including shielded transactions and MASP indexer support.

## 📋 System Requirements

| Category | Requirements |
|----------|--------------|
| CPU | 8+ cores |
| RAM | 32+ GB |
| Storage | 500+ GB NVMe SSD |
| Bandwidth | 100+ MBit/s |

## ⚡ Quick Start

Run the main interactive menu:

```bash
bash <(curl -s https://raw.githubusercontent.com/hubofvalley/Mainnet-Guides/main/Namada/resources/valleyofNamada.sh)
```

## 📦 Features

### Node Operations
- Deploy/re-deploy validator node
- Update Namada version
- Apply snapshot
- Add seeds/peers
- Show status and logs

### Wallet Management
- Create/restore wallets
- Shielded keys and payment addresses
- Query balances (transparent & shielded)
- Transfer tokens

### Staking Operations
- Delegate to validators
- Self-delegate
- Unstake tokens

### Indexer Services
- Namada Indexer installation
- MASP Indexer installation

## 🔧 Current Versions

| Component | Version |
|-----------|---------|
| Namada | v1.0.0 - v201.0.7 |
| CometBFT | v0.37.15 |
| Namada Indexer | v4.1.0 |
| MASP Indexer | v1.4.7 |
| Chain | namada.5f5de2dd1b88cba30586420 |

## 🌐 Grand Valley Public Endpoints

| Type | URL |
|------|-----|
| Cosmos RPC | `https://lightnode-rpc-mainnet-namada.grandvalleys.com` |
| EVM RPC | `https://lightnode-json-rpc-mainnet-namada.grandvalleys.com` |
| Cosmos WebSocket | `wss://lightnode-rpc-mainnet-namada.grandvalleys.com/websocket` |
| Seed | `tcp://65882ea69f4146d8cc83564257252f4711d3e05e@seed-mainnet-namada.grandvalleys.com:56656` |
| Peer | `tcp://3879583b9c6b1ac29d38fefb5a14815dd79282d6@peer-mainnet-namada.grandvalleys.com:38656` |
| Indexer | `https://indexer-mainnet-namada.grandvalleys.com` |
| MASP Indexer | `https://masp-indexer-mainnet-namada.grandvalleys.com` |
| Namadillo | `https://valley-of-namadillo.grandvalleys.com` |

## 🔐 Privacy & Security

- **No external data storage** - All operations run locally
- **No phishing links** - All URLs are for legitimate Namada operations
- **Open source** - Full audit trail available
- Namada's MASP provides shielded transactions for privacy

## 📖 Documentation

For detailed documentation, see the [docs/](docs/) folder.

## 🔗 Links

**Namada:**
- [Website](https://namada.net) | [Docs](https://docs.namada.net) | [X/Twitter](https://twitter.com/namada)

**Grand Valley:**
- [GitHub](https://github.com/hubofvalley) | [X/Twitter](https://x.com/bacvalley) | [Mainnet Guide](https://github.com/hubofvalley/Mainnet-Guides/tree/main/Namada)

**Validators & Explorers:**
- [Explorer75](https://explorer75.org/namada/validators/tnam1qyplu8gruqmmvwp7x7kd92m6x4xpyce265fa05r6)
- [Valopers](https://namada.valopers.com/validators/tnam1qyplu8gruqmmvwp7x7kd92m6x4xpyce265fa05r6)
- [Shielded.live](https://shielded.live/validators/9FB9AC991FE50B76FB1E4FFEDCC47E6BF13F58FED9B0079400D4F043DD16D207)

## 📧 Contact

Email: letsbuidltogether@grandvalleys.com

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
