# PQWERAI Wallet — release downloads

Download builds of the PQWERAI Wallet for Windows and the wallet command-line tool for Linux. This repository
contains release files only. The wallet and the PQWERAI blockchain are developed in a private repository.

> **Test-network software.** PQAI and QAI on the PQWERAI test network have no value. Do not store real funds, and
> do not use a seed, key or passphrase that you use anywhere else. Public testnet and mainnet remain not ready.

## Downloads

The newest published build is **[0.8.10](https://github.com/peppez07/pqwerai-wallet-releases/releases/tag/v0.8.10)**,
released **17 November 2026** as a **pre-release**. Every version is published as a pre-release, so GitHub shows no
"Latest" badge: the newest version is always at the top of the [Releases page](https://github.com/peppez07/pqwerai-wallet-releases/releases)
and on [pqwerai.com/downloads](https://pqwerai.com/downloads/).

| File | For | SHA-256 |
| --- | --- | --- |
| [`PQWERAI-Wallet-0.8.10-win-x64.msi`](https://github.com/peppez07/pqwerai-wallet-releases/releases/download/v0.8.10/PQWERAI-Wallet-0.8.10-win-x64.msi) | Windows 10/11 x64 installer (per user, no admin rights) | `6a8ab984aa58ccd932beaae97713f26b53e5e6d9956902f400fdc112d270105b` |
| [`PQWERAI-Wallet-0.8.10-win-x64-portable.zip`](https://github.com/peppez07/pqwerai-wallet-releases/releases/download/v0.8.10/PQWERAI-Wallet-0.8.10-win-x64-portable.zip) | Windows 10/11 x64, no installation (unzip and run `PQWERAI.Wallet.exe`) | `c8d5c73f77ce659b33cafe0eefcea6cfde16558d6564c40c2702a53d1eac6599` |
| [`pqwerai-wallet-cli-0.8.10-linux-x64.tar.gz`](https://github.com/peppez07/pqwerai-wallet-releases/releases/download/v0.8.10/pqwerai-wallet-cli-0.8.10-linux-x64.tar.gz) | Wallet command-line tool for Linux x64, with `qai-wallet` | `7fa62c60f8a0280e4a61bbf5d185b202bd3678fa9f599d6fc043c0db80f864d3` |
| [`SHA256SUMS`](https://github.com/peppez07/pqwerai-wallet-releases/releases/download/v0.8.10/SHA256SUMS) | Checksums of the release files | |

## Known issue in 0.8.10 and earlier: your own node stops at block 34,785

The default mode is not affected: the wallet starts online through the public RPC and works normally.

If you turned on **Run my own node**, that node stops following test network 20777 at block **34,785**, where the
IPFS storage reward (block split 67 / 18 / 1 / 9 / 5) started. Released wallets do not pass that network upgrade to
the node. Until the next release, turn **Run my own node** off so the wallet uses the public connection again. The fix is in the main code
and comes with **0.8.11**.

## Coming next: 0.8.11

Approved and in preparation; it is not published yet.

- The own-node fix above: the wallet starts its node with the network's IPFS reward upgrade.
- The Windows node is bundled with the wallet (`pqwerai-core`, its command-line tool and the hash worker), with the
  complete source code of those programs attached to the release.

## Latest news

### 17 November 2026 — Wallet 0.8.10

- **Use your own documents with AI** (AI Workflows → Datasets & RAG): load text, Markdown, JSON or CSV files, split
  and index them in a knowledge base, and get answers that cite the passages they come from. A new template,
  **Ask your documents (RAG)**, puts it together.
- **LoRA adapters** (AI Workflows → AI Models): add up to 8 LoRA adapters to a compatible base model and merge them
  on your PC. The built-in Bonsai 2 model cannot take a LoRA. New template: **LoRA style**.
- Everything runs on your PC; nothing is uploaded unless you add an IPFS step yourself.

[0.8.10 release notes](https://github.com/peppez07/pqwerai-wallet-releases/releases/tag/v0.8.10)

### 16 November 2026 — Wallet 0.8.9

- **AI sharing gets priority over mining:** when you share your PC for AI and mine at the same time, mining drops to
  Idle priority so AI requests get the CPU first. On by default; you can turn it off on the AI Sharing page.
- **17 more AI Workflows nodes and 4 templates**, including Summarize, Classify, Extract Fields, Translate and a new
  Text & Data category. Step-by-step guide: [pqwerai.com/wallet/workflows](https://pqwerai.com/wallet/workflows/).
- The Node page shows the test network's new block split (67 / 18 / 1 / 9 / 5 since block 34,785).

[0.8.9 release notes](https://github.com/peppez07/pqwerai-wallet-releases/releases/tag/v0.8.9)

### 16 November 2026 — Wallet 0.8.8

- **AI Workflows** (new page, Ctrl+Shift+8): build AI workflows on a canvas from models, prompts, agents, data, tools,
  IPFS, contracts and payments. Steps that spend PQAI or sign a transaction always ask for your approval.
- **Safer recurring payments:** a recurring permission can now only pay a recipient; "call mode" is refused.

[0.8.8 release notes](https://github.com/peppez07/pqwerai-wallet-releases/releases/tag/v0.8.8)

### 16 November 2026 — Wallet 0.8.7

- **AI Sharing works on test network 20777:** the AI contracts are deployed and the wallet knows their addresses.
  Models are checked against the on-chain registry before any download.
- Choose a **model pool** on the AI Sharing page; new official PQWERAI logo.

[0.8.7 release notes](https://github.com/peppez07/pqwerai-wallet-releases/releases/tag/v0.8.7)

Older versions: [0.8.6](https://github.com/peppez07/pqwerai-wallet-releases/releases/tag/v0.8.6) (Smart-contract
Studio languages, AI Model Pools), [0.8.0](https://github.com/peppez07/pqwerai-wallet-releases/releases/tag/v0.8.0)
(QAI page, Quantum Smart Accounts) and [all releases](https://github.com/peppez07/pqwerai-wallet-releases/releases).

## Verify your download

Download `SHA256SUMS` from the **same release** as your chosen file. Compare its SHA-256 with the matching line:

```powershell
Get-FileHash .\PQWERAI-Wallet-0.8.10-win-x64.msi -Algorithm SHA256
```

On Linux, put the archive and `SHA256SUMS` in the same directory, then run:

```bash
sha256sum -c SHA256SUMS --ignore-missing
```

Only run a file whose checksum matches exactly.

## Connecting to a network

The wallet starts **online by default**: it connects to the public test-network RPC (`rpc-testnet.pqwerai.com`, with
`rpc-testnet2.pqwerai.com` as failover) and checks the chain ID (20777) and genesis hash before it shows anything.
Running your own node is optional (**Run my own node**); see the known issue above. Releases up to
0.8.10 include **no Core node binary**.

## Current limitations

- The binaries are **not code-signed**, so Windows SmartScreen may warn.
- The in-app update feed is inactive; download updates from this repository's Releases page.
- Multi-host model execution has not been verified, and pooled on-chain settlement is not implemented.
- The node software's WASM contract VM still needs a denial-of-service fix; it is not part of these releases.
- These releases have had author review only, **not an independent security audit**.

## Licence

No open-source licence has been chosen yet for the wallet's own code, so all rights are reserved for now. The
wallet includes third-party components under the MIT licence; their notices are in `THIRD-PARTY-NOTICES.txt` in
this repository and inside every download.
