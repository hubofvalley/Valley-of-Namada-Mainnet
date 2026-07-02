# Valley of Namada Mainnet - Usage Guide

How to run the tool, how to navigate it, and what every menu option does.

## Running the tool

```bash
bash <(curl -s https://raw.githubusercontent.com/hubofvalley/Valley-of-Namada-Mainnet/main/resources/valleyofNamada.sh)
```

Or from a local clone:

```bash
bash resources/valleyofNamada.sh
```

Run it as the user that owns the Namada node files. The script stores environment variables in `~/.bash_profile`.

## Navigation

- Choose an option by typing number + letter together, for example `2d`, or type the number first and then the letter when prompted.
- Namada has transparent keys, shielded keys, and shielded payment addresses. Pick the matching wallet operation carefully.
- After exiting, run `source ~/.bash_profile` so exported variables apply to the current shell.

## Menu options explained

| Option | What it does | When to use | Destructive / risk |
|---|---|---|---|
| 1a. Deploy/re-Deploy Validator Node | Installs or reinstalls the Namada validator node. | First setup or clean redeploy. | Yes - may replace services and data. Backup keys first. |
| 1b. Update Namada Binary Version | Updates Namada binary. | Required binary upgrade. | Medium. |
| 1c. Show Validator Node Status | Shows local validator node status and sync height. | Health check. | No. |
| 1d. Show Validator Node Logs | Tails validator node logs. | Debugging. | No. |
| 1e. Apply Snapshot | Applies snapshot. | Speed up sync or recover data. | Yes - can replace chain data. |
| 1f. Add Seeds | Updates seed configuration. | Connectivity repair. | Low. |
| 1g. Add Peers | Updates peer configuration. | Connectivity repair. | Low. |
| 2a. Create Wallet | Creates transparent key, shielded key, or shielded payment address. | First wallet setup. | Sensitive - mnemonic/key material. |
| 2b. Restore Wallet | Restores transparent/shielded wallet material. | Recover existing wallet. | Sensitive. |
| 2c. Show Wallet | Lists/shows wallet keys or addresses. | Verify wallet aliases/addresses. | No, but do not expose sensitive output. |
| 2d. Query Balance | Queries balances. | Check funds. | No. |
| 2e. Create Validator | Registers validator. | Initial validator creation. | Yes - on-chain transaction. |
| 2f. Transfer (Transparent) | Sends transparent NAM. | Normal transfer. | Yes - on-chain transaction. |
| 2g. Delegate NAM | Delegates stake. | Stake to validator. | Yes - on-chain transaction. |
| 2h. Undelegate NAM | Starts undelegation. | Reduce/remove stake. | Yes - on-chain transaction. |
| 2i. Redelegate NAM | Moves stake to another validator. | Change delegation target. | Yes - on-chain transaction. |
| 2j. Withdraw Unbonded NAM | Withdraws unbonded tokens. | After unbonding period. | Yes - on-chain transaction. |
| 2k. Claim Rewards | Claims staking rewards. | Collect rewards. | Yes - on-chain transaction. |
| 2l. Vote Proposal | Votes on governance proposal. | Governance participation. | Yes - on-chain transaction. |
| 2m. Create Another Shielded Payment Address | Creates extra shielded payment address. | Need another receiving address. | Sensitive. |
| 2n. Transfer (Shielding) | Moves funds into shielded pool. | Shield transparent funds. | Yes - on-chain transaction. |
| 2o. Transfer (Shielded to Shielded) | Sends shielded funds to shielded address. | Private transfer. | Yes - on-chain transaction. |
| 2p. Transfer (Unshielding) | Moves shielded funds to transparent address. | Unshield funds. | Yes - on-chain transaction. |
| 2q. Delete Wallet | Deletes keys or addresses. | Remove local wallet material. | Yes - destructive. Backup first. |
| 3a. Deploy Namada Indexer | Installs Namada indexer. | Run indexer service. | Medium. |
| 3b. Apply Namada Indexer Snapshot | Applies indexer snapshot. | Speed up/recover indexer. | Yes - can replace indexer data. |
| 3c. Show Namada Indexer Logs | Tails indexer logs. | Debug indexer. | No. |
| 4a. Deploy Namada MASP Indexer | Installs MASP indexer. | Run MASP indexer service. | Medium. |
| 4b. Apply Namada MASP Indexer Snapshot | Applies MASP indexer snapshot. | Speed up/recover MASP indexer. | Yes - can replace data. |
| 4c. Show Namada MASP Indexer Logs | Tails MASP indexer logs. | Debug MASP indexer. | No. |
| 5a. Restart Validator Node | Restarts validator service. | After config/binary changes. | Low - downtime. |
| 5b. Restart Namada Indexer | Restarts indexer service. | Indexer maintenance. | Low. |
| 5c. Restart Namada MASP Indexer | Restarts MASP indexer. | MASP maintenance. | Low. |
| 5d. Stop Validator Node | Stops validator service. | Maintenance. | Medium - validator offline. |
| 5e. Stop Namada Indexer | Stops indexer. | Maintenance. | Medium. |
| 5f. Stop Namada MASP Indexer | Stops MASP indexer. | Maintenance. | Medium. |
| 5g. Backup Validator Key | Copies validator key to `$HOME`. | Before upgrades/delete/redeploy. | No, but protect backup. |
| 5h. Backup Namada Indexer database | Backs up indexer database. | Before indexer maintenance. | No. |
| 5i. Backup Namada MASP Indexer database | Backs up MASP database. | Before MASP maintenance. | No. |
| 5j. Delete Validator Node | Deletes validator node. | Decommission or clean reinstall. | Yes - destructive. Backup first. |
| 5k. Delete Namada Indexer | Deletes indexer service/data. | Decommission indexer. | Yes - destructive. |
| 5l. Delete Namada MASP Indexer | Deletes MASP service/data. | Decommission MASP indexer. | Yes - destructive. |
| 6. Install the Namada App | Installs CLI app only, without running a node. | Need CLI transactions only. | Medium - binary install. |
| 7. Open Cubic Slashing Rate Monitoring Tool | Opens CSR monitoring helper. | Monitor Namada cubic slashing rate. | No. |
| 8. Show Grand Valley's Endpoints | Prints endpoints and links. | Reference. | No. |
| 9. Show Guidelines | Shows in-tool guidance. | First-time use. | No. |
| 10. Exit | Leaves the script. | Done. | No. |

## Recommended first-time flow

1. Run `1a`, then monitor with `1c` and `1d` until healthy.
2. Create or restore wallet material with `2a`/`2b`.
3. Register validator with `2e`, then back up key with `5g`.
4. Use `2g` for delegation and `2k` for rewards after confirming addresses and amounts.
5. Add indexers only if required for your workflow.

## Safety notes

- Wallet delete and node delete are destructive. Backup before using `2q` or `5j`.
- Shielded flows are harder to inspect after the fact. Double-check aliases and addresses.
- Any staking, transfer, vote, or reward claim submits an on-chain transaction.
