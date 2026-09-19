# Vault AI Workspace and SafeVault Architecture

**Updated:** 2026-09-18

| Component | Responsibility |
| --- | --- |
| BlackVault Public Network | Ecosystem identity, application framework, and documentation |
| SafeVault | Homebase, external wallet connections, asset presentation, review, and account authorization |
| Vault AI | Workspace assistance, approved knowledge, public-data discovery, evidence explanation, and prepared handoffs |
| Discovery/claim backend | Provider requests, contract-specific eligibility checks, and structured evidence |
| Wallet execution infrastructure | Validate holder authorization, submit approved operations, and return execution evidence |

Workspace administrator permissions, VLT contract-owner powers, and individual wallet authority are separate. Signing credentials remain within the holder's chosen wallet/authentication system. Future automated execution requires separately enabled, limited, revocable permissions enforced by the actual account execution layer.

## Wallet context for the agent

SafeVault has two wallet layers:

1. **Homebase — the primary BlackVault smart account.** A user signs in to the BlackVault application to reach their Homebase workspace, assets, activity, and account controls. The approved product direction starts with a holder-controlled smart account. Application login, account initialization, and blockchain authorization are separate operations.
2. **Connected external wallets — an optional second layer.** Existing compatible wallets retain their own addresses, networks, balances, and permissions. Connecting one enables supported visibility and interaction; moving assets into Homebase is a separately authorized transfer.

The primary design uses an ERC-4337-style account model. Optional EIP-7702 support for compatible external EOAs is a separate integration proposal. A connected wallet is not evidence of an active delegation. Account deployment timing, gas arrangements, authentication/recovery, and infrastructure providers remain implementation selections.

Assets remain recorded on their respective blockchains. Homebase brings those records into a coordinated interface; signing in does not merge accounts or transfer balances.

## Botpress implementation scope

Configure the agent's knowledge sources, behavioral instructions, workflows, tool bindings, and evidence/case records. Integrations with code repositories, documents, browsers, scheduling, and devices require supported tools and scoped user authorization. A proposed connector is listed as planned until it has been connected and exercised.

Knowledge and workflow preparation can progress before live API endpoints exist. Treat provider connectivity, scan-service availability, wallet execution, and browser-extension release as separate states.

## Asset evidence

| Finding | Required interpretation |
| --- | --- |
| Asset visible | A holding or transfer was observed at a particular address and chain. |
| Candidate claim | A contract or protocol indicator supports further investigation. |
| Validated eligibility | A supported contract adapter has checked the exact network, wallet entitlement, token, amount, recipient, required proof, relevant state, and a current simulation where applicable. |
| Confirmed recovery | Execution succeeded and the expected asset movement or protocol outcome was verified. |

A positive token balance, an ABI method name, or source-code verification alone does not establish claim eligibility. Preserve evidence sources, the queried block/time, and scan coverage. An unavailable provider or unsupported protocol produces an incomplete/unsupported result rather than a conclusion that no assets exist. Unknown values remain explicitly pending.

## Network context

| Context | Network | Configuration status |
| --- | --- | --- |
| Vault Coin (VLT) | Ethereum mainnet, `1` | Production proxy and deployment receipt pending |
| FUNTOKEN (FUN) | Sepolia, `11155111` | Three recorded deployments; shared canonical address pending owner selection |
| Initial Vault AI recovery workflow | Ethereum mainnet, `1` | First supported claim contract and live connection pending validation |
| FUN discovery and development | Sepolia, `11155111` | Separate, explicitly selected testnet context |

Identify every asset by chain ID and full contract address. A token symbol alone is insufficient. Additional networks require their own supported provider and contract configuration.

Authentication/recovery choices, deployment timing, gas arrangements, providers, and final account-contract addresses remain configuration decisions. Record their resolution with a source and date.
