# Wallet Guide

Create and manage Namada wallets including shielded keys.

## Creating a Wallet

1. Launch Valley of Namada:
   ```bash
   bash <(curl -s https://raw.githubusercontent.com/hubofvalley/Mainnet-Guides/main/Namada/resources/valleyofNamada.sh)
   ```
2. Select **"Wallet/Key Interactions"** → **"Create Wallet"**
3. Enter a wallet prefix (e.g., `mywallet`)

This creates:
- Transparent key: `mywallet`
- Shielded key: `mywallet-shielded`
- Shielded payment address: `mywallet-shielded-addr`

> ⚠️ **Important**: Write down your mnemonic and store it securely - this is the only time it will be shown!

## Restoring a Wallet

1. Launch Valley of Namada
2. Select **"Wallet/Key Interactions"** → **"Restore Wallet"**
3. Enter wallet prefix and mnemonic

## Shielded Payment Addresses

Create additional shielded payment addresses:

1. Launch Valley of Namada
2. Select **"Wallet/Key Interactions"** → **"Create Shielded Payment Address"**
3. Select an existing shielded key
4. Enter an alias prefix

## Viewing Wallets

1. Launch Valley of Namada
2. Select **"Wallet/Key Interactions"** → **"Show Wallet"**

Displays:
- Transparent keys
- Implicit addresses
- Shielded keys
- Shielded addresses

## Query Balance

1. Launch Valley of Namada
2. Select **"Wallet/Key Interactions"** → **"Query Balance"**
3. Choose:
   - Query your own wallet
   - Query another address
4. Select address type (transparent or shielded)

## Transfers

### Transparent Transfer

1. Launch Valley of Namada
2. Select **"Token Interactions"** → **"Transfer (Transparent)"**
3. Enter source wallet, target address, amount, and token

### Shielding (Transparent → Shielded)

1. Launch Valley of Namada
2. Select **"Token Interactions"** → **"Shield Tokens"**

### Unshielding (Shielded → Transparent)

1. Launch Valley of Namada
2. Select **"Token Interactions"** → **"Unshield Tokens"**

### Shielded Transfer

1. Launch Valley of Namada
2. Select **"Token Interactions"** → **"Transfer (Shielded)"**

## Deleting Wallets

1. Launch Valley of Namada
2. Select **"Wallet/Key Interactions"** → **"Delete Wallets"**
3. Enter comma-separated aliases to delete
4. Confirm deletion

## Related Documentation

- [Validator Node Guide](validator-node.md)
- [Staking Guide](staking.md)
