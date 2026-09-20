# Vault AI Workspace Copilot™

**Your work. Your context. Vault AI.**  
Powered By Intelligent Design™

**Vault AI Workspace Copilot** is the canonical BlackVault workspace agent/system. **BlackVault Public Network** remains the ecosystem/platform name; **Vault AI** is the short conversational name. Vault AI Workspace Copilot is being developed as a connected workspace assistant for BlackVault Public Network. It helps users understand project information, work with documents and code, organize tasks, and follow evidence through connected workflows.

The current Botpress work configures **Vault AI Workspace Copilot**: its instructions, knowledge, conversation flows, tool interfaces, and case records. The browser extension is a planned interface for that agent and its approved workspace tools.

## The planned experience

| Capability | Intended outcome |
| --- | --- |
| Selected page and project context | Explain the information the user chooses to share |
| Documents and code | Produce reviewable drafts and proposed changes through approved workspace tools |
| Tasks and continuity | Organize work, record progress, and support approved device notifications |
| BlackVault knowledge | Keep product roles, source records, and current decisions easy to retrieve |
| Asset discovery | Explain public balances, transfers, contract records, and possible recovery paths |
| SafeVault handoffs | Prepare evidence and supported action details for wallet review |

## SafeVault relationship

SafeVault has two wallet layers:

1. **Homebase — the primary BlackVault smart account.** A user signs in to the BlackVault application to reach their Homebase workspace, assets, activity, and account controls. The approved product direction starts with a holder-controlled smart account. Application login, account initialization, and blockchain authorization are separate operations.
2. **Connected external wallets — an optional second layer.** Existing compatible wallets retain their own addresses, networks, balances, and permissions. Connecting one enables supported visibility and interaction; moving assets into Homebase is a separately authorized transfer.

The primary design uses an ERC-4337-style account model. Optional EIP-7702 support for compatible external EOAs is a separate integration proposal. A connected wallet is not evidence of an active delegation. Account deployment timing, gas arrangements, authentication/recovery, and infrastructure providers remain implementation selections.

Assets remain recorded on their respective blockchains. Homebase brings those records into a coordinated interface; signing in does not merge accounts or transfer balances.

Vault AI Workspace Copilot provides assistance and evidence. The wallet/account system manages signing credentials and validates authorization. Workspace access, token-owner roles, and a user's wallet permissions remain distinct. The primary workspace is owner-focused; any future user-facing agent must use its own scoped workspace and account access.

## Network context

| Context | Network | Configuration status |
| --- | --- | --- |
| Vault Coin (VLT) | Ethereum mainnet, `1` | Production proxy and deployment receipt pending |
| FUNTOKEN (FUN) | Sepolia, `11155111` | Three recorded deployments; shared canonical address pending owner selection |
| Initial Vault AI recovery workflow | Ethereum mainnet, `1` | First supported claim contract and live connection pending validation |
| FUN discovery and development | Sepolia, `11155111` | Separate, explicitly selected testnet context |

Identify every asset by chain ID and full contract address. A token symbol alone is insufficient. Additional networks require their own supported provider and contract configuration.

FUNTOKEN's documented milestone is a Sepolia token deployment history. It is distinct from Vault Coin's mainnet production lifecycle and from a Vault AI software release.

## What is available in this repository

This public repository contains product documentation. The [architecture brief](docs/ARCHITECTURE.md) describes the agent and wallet relationship, and the [repository listing](Vault-AI-Extension-Public-Deployment-Repo) identifies current documents and planned packaging.

The Botpress configuration and TypeScript discovery-action sources are maintained in the separate application implementation repository. Their presence is a source-code milestone; workspace installation, provider connection, and live recovery support require their own records.

## Development milestones

- Workspace identity and product scope documented.
- SafeVault's primary smart account and optional external connections aligned.
- Botpress instructions, workflow specifications, and discovery source prepared in the application project.
- Next: bind the actual workspace tools and providers, validate their responses, and demonstrate the supported user flows.
- Browser packaging, install instructions, task scheduling, and device pairing remain separate implementation milestones.

## Explore BlackVault

[BlackVault Public Network](https://github.com/blackvault-opps/Blackvault-Public-Network-repo) · [SafeVault](https://github.com/blackvault-opps/SafeVault_deploy-repo) · [FUNTOKEN](https://github.com/blackvault-opps/FUN-TOKEN-ERC-20-Report-Repo)

Repository maintenance follows explicit owner authorization for the requested changes. Publication and deployment are recorded separately.

Updated 2026-09-20. Copyright © 2026 BlackVault Public Network. All rights reserved.
