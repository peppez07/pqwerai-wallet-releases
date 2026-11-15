# PQWERAI Wallet — release downloads

Download builds of the PQWERAI Wallet for Windows and the wallet command-line tool for Linux. This repository
contains release files only. The wallet and the PQWERAI blockchain are developed in a private repository.

> **Test-network software.** PQAI and QAI on the PQWERAI test network have no value. Do not store real funds, and
> do not use a seed, key or passphrase that you use anywhere else. Public testnet and mainnet remain not ready.

## Latest news

### 14 November 2026 — Wallet 0.8.6 (pre-release)

- **Smart-contract Studio:** Solidity, Yul, Vyper, Huff, Fe, C++ and C# are supported and checked against the chain's
  EVM and WASM contract VM. Fe, C++ and C# are no longer marked experimental. C# gains structs, enums, `ref`/`out`,
  checked arithmetic and static initializers.
- **Safer contract projects:** attachments cannot overwrite editor code, the contract SDK or bundled OpenZeppelin
  files. Huff includes are restricted to the project. C# and C++ ERC-20 examples add stricter argument, address and
  value checks. ERC-20 examples are available for Solidity, Vyper, Fe, C++ and C#.
- **AI Model Pools:** find, create and join a pool for a specific model. Two federated directories provide failover,
  and the PQWERAI relay connects pool PCs behind NAT while admitting only members listed as ready or active.
  Running one model across several GPU PCs still needs multi-host verification; pooled on-chain settlement is not
  implemented.
- **Node improvements:** the native node service keeps running beyond command deadlines, and automatic peer
  discovery uses signed seed lists.

Read the [full 0.8.6 release notes](https://github.com/peppez07/pqwerai-wallet-releases/releases/tag/v0.8.6) for changes, testing and known limitations.

### 13 November 2026 — Wallet 0.8.0

Added the **QAI** page in Advanced mode, post-quantum Quantum Smart Accounts and the bundled `qai-wallet` signer,
plus native node support on Windows and Linux. QAI contracts are not deployed on a public chain yet; contract
addresses and Core node builds come from the network operator.

See the [0.8.0 release notes](https://github.com/peppez07/pqwerai-wallet-releases/releases/tag/v0.8.0) and [all releases](https://github.com/peppez07/pqwerai-wallet-releases/releases).

## Downloads

The newest published build is **[0.8.6](https://github.com/peppez07/pqwerai-wallet-releases/releases/tag/v0.8.6)**, released **14 November 2026** as a **pre-release**.

| File | For |
| --- | --- |
| [`PQWERAI-Wallet-0.8.6-win-x64.msi`](https://github.com/peppez07/pqwerai-wallet-releases/releases/download/v0.8.6/PQWERAI-Wallet-0.8.6-win-x64.msi) | Windows 10/11 x64 installer (per user, no admin rights) |
| [`PQWERAI-Wallet-0.8.6-win-x64-portable.zip`](https://github.com/peppez07/pqwerai-wallet-releases/releases/download/v0.8.6/PQWERAI-Wallet-0.8.6-win-x64-portable.zip) | Windows 10/11 x64, no installation (unzip and run `PQWERAI.Wallet.exe`) |
| [`pqwerai-wallet-cli-0.8.6-linux-x64.tar.gz`](https://github.com/peppez07/pqwerai-wallet-releases/releases/download/v0.8.6/pqwerai-wallet-cli-0.8.6-linux-x64.tar.gz) | Wallet command-line tool for Linux x64, with `qai-wallet` |
| [`SHA256SUMS`](https://github.com/peppez07/pqwerai-wallet-releases/releases/download/v0.8.6/SHA256SUMS) | Checksums of the release files |

## Verify your download

Download `SHA256SUMS` from the **same release** as your chosen file. Compare its SHA-256 with the matching line:

```powershell
Get-FileHash .\PQWERAI-Wallet-0.8.6-win-x64.msi -Algorithm SHA256
```

On Linux, put the archive and `SHA256SUMS` in the same directory, then run:

```bash
sha256sum -c SHA256SUMS --ignore-missing
```

Only run a file whose checksum matches exactly.

## Connecting to a network

The wallet connects to a PQWERAI node that you choose. It can also manage a native node when you supply a compatible
Core build; **no Core node binary is included** in these downloads. The network operator provides the node address,
network details and any required genesis file or contract addresses.

## Current limitations

- The binaries are **not code-signed**, so Windows SmartScreen may warn.
- The in-app update feed is inactive; download updates from this repository's Releases page.
- Multi-host model execution has not been verified, and pooled on-chain settlement is not implemented.
- The node software's WASM contract VM needs a denial-of-service fix that is not included in wallet 0.8.6.
- These releases have had author review only, **not an independent security audit**.

See the [0.8.6 release notes](https://github.com/peppez07/pqwerai-wallet-releases/releases/tag/v0.8.6) for the published validation results.

## Licence

No open-source licence has been chosen yet for the wallet's own code, so all rights are reserved for now. The
wallet includes third-party components under the MIT licence; their notices are in `THIRD-PARTY-NOTICES.txt` in
this repository and inside every download.
