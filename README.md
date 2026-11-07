# PQWERAI Wallet — release downloads

Download builds of the PQWERAI Wallet for Windows and the wallet command-line tool. This repository contains
release files only. The wallet and the PQWERAI blockchain are developed in a private repository.

> **Private testnet software.** PQWERAI runs as a private test network. Coins on it (PQAI) have no value. Do not
> store real funds, and do not use these builds with a seed or key you use anywhere else.

## Downloads

Go to the [Releases](../../releases) page. The latest release is **0.6.0** (pre-release).

| File | For |
| --- | --- |
| `PQWERAI-Wallet-0.6.0-win-x64.msi` | Windows 10/11 x64 installer |
| `PQWERAI-Wallet-0.6.0-win-x64-portable.zip` | Windows 10/11 x64, no installation (unzip and run `PQWERAI.Wallet.exe`) |
| `pqwerai-wallet-cli-0.6.0-linux-x64.tar.gz` | Wallet command-line tool for Linux x64 |
| `SHA256SUMS` | Checksums of the files above |

## Verify your download

Compare the SHA-256 of the file you downloaded with the line in `SHA256SUMS`:

```powershell
Get-FileHash .\PQWERAI-Wallet-0.6.0-win-x64.msi -Algorithm SHA256
```

```bash
sha256sum -c SHA256SUMS --ignore-missing
```

Only run a file whose checksum matches exactly.

## Connecting to a network

The wallet connects to a PQWERAI node that you choose; it does not include one. A node address and the network
details are provided by the network operator.

## Licence

No open-source licence has been chosen yet for the wallet's own code, so all rights are reserved for now. The
wallet includes third-party components under the MIT licence; their notices are in `THIRD-PARTY-NOTICES.txt` in
this repository and inside every download.
