<h1 align="center">Sling402</h1>

<p align="center">
  <strong>X402 Payment Protocol on Solana · $S402</strong>
</p>

<p align="center">
  <a href="https://sling402.io"><img src="https://img.shields.io/badge/LIVE-sling402.io-white?style=flat-square&labelColor=FF5722&color=111111" alt="Live"></a>
  <a href="https://x.com/Sling402"><img src="https://img.shields.io/badge/@Sling402-000000?style=flat-square&logo=x&logoColor=white" alt="X"></a>
  <img src="https://img.shields.io/badge/Solana-Compatible-000000?style=flat-square&logo=solana&logoColor=white" alt="Solana">
  <img src="https://img.shields.io/badge/Agents-12-FF5722?style=flat-square&labelColor=000000" alt="Agents">
  <img src="https://img.shields.io/badge/Protocol-X402-FF5722?style=flat-square&labelColor=000000" alt="X402">
  <img src="https://img.shields.io/badge/License-MIT-white?style=flat-square&labelColor=000000" alt="License">
</p>

---

## What is Sling402?

Sling402 is the **X402 payment protocol** built on Solana. It uses `HTTP 402 Payment Required` to enable instant, private, machine-to-machine and peer-to-peer payments. No KYC. No middlemen. No hidden markups.

12 autonomous payment agents run the infrastructure — routing, settling, and verifying X402 transactions 24/7 without human intervention.

---

## How X402 Works

**Step 1** — Client requests a paid resource.

**Step 2** — Server responds with `402 Payment Required`:

```json
{
  "x402Version": 1,
  "scheme": "exact",
  "network": "solana-mainnet",
  "maxAmountRequired": "1000",
  "payTo": "EPgK11Qa7Xectz...Mib2zD",
  "resource": "/api/premium-data"
}
```

**Step 3** — Client pays on Solana, retries with `X-PAYMENT` header containing the transaction signature.

**Step 4** — Server verifies on-chain, returns the resource. Done.

---

## Payment Agents

| Agent | Role | Description |
|---|---|---|
| **Meridian** | Router | Payment path optimization |
| **Conduit** | Channel | Payment channel management |
| **Arbiter** | Disputes | Dispute resolution & refunds |
| **Nexus** | Bridge | Cross-chain operations |
| **Lattice** | LP | Liquidity provisioning |
| **Cipher** | Privacy | Encryption & privacy layer |
| **Prism** | Optimizer | Fee optimization |
| **Relay** | Relay | Transaction broadcasting |
| **Sentinel** | Security | Fraud detection |
| **Vaultr** | Escrow | Escrow & custody |
| **Beacon** | Oracle | Price feeds & rate oracle |
| **Fulcrum** | Settlement | Settlement engine |

Each agent has its own Solana wallet. On-chain verifiable. Always on.

---

## Token Model

| Token | Type | Supply | Purpose |
|---|---|---|---|
| **$S402** | Native | 1,000,000,000 | X402 payment fees & settlements |
| **$wS402** | Wrapped | Unlimited | DeFi integrations, 10,000:1 conversion |

### Supply Allocation

| Pool | % | Amount | Purpose |
|---|---|---|---|
| Agent Operations | 35% | 350,000,000 | Payment agent wallets |
| Protocol Reserve | 20% | 200,000,000 | Network incentives |
| DEX Liquidity | 15% | 150,000,000 | Trading pair liquidity |
| Team | 15% | 150,000,000 | 6-month lock, linear vest |
| Faucet | 10% | 100,000,000 | 1,000 per wallet, no refill |
| Development | 5% | 50,000,000 | Protocol upgrades |

**Total: 1,000,000,000 $S402** — fixed, no inflation.

---

## Deploy to Render

| Setting | Value |
|---|---|
| **Environment** | Node |
| **Build Command** | `npm install` |
| **Start Command** | `node server.js` |

### Environment Variables

| Key | Value | Required |
|---|---|---|
| `PUBLIC_URL` | `https://sling402.io` | Optional |
| `ANTHROPIC_API_KEY` | `sk-ant-api03-...` | Optional |
| `OPENAI_API_KEY` | `sk-...` | Optional |

`PORT` is set automatically by Render. API keys are optional.

---

## Run Locally

```bash
npm install
node server.js
```

Open `http://localhost:3000` — Enter password — Explore.

---

## Add to Wallet

| Field | Value |
|---|---|
| **RPC URL** | `https://sling402.io/rpc` |
| **Network** | Sling402 |
| **Symbol** | S402 |
| **Decimals** | 9 |

Supports: **Phantom** · **Backpack** · **Solflare**

---

## API Endpoints

| Method | Endpoint | Description |
|---|---|---|
| `POST` | `/api/auth` | Password authentication |
| `GET` | `/api/chain` | Chain stats |
| `GET` | `/api/blocks?page=1` | Paginated blocks |
| `GET` | `/api/block/:slot` | Block details |
| `GET` | `/api/transactions?page=1` | Paginated transactions |
| `GET` | `/api/tx/:sig` | Transaction details |
| `GET` | `/api/account/:pubkey` | Account info |
| `GET` | `/api/wallet/:pubkey` | Wallet balance |
| `POST` | `/api/faucet/claim` | Claim 1,000 S402 |
| `GET` | `/api/faucet/status` | Faucet pool balance |
| `GET` | `/api/tokens` | All tokens |
| `GET` | `/api/agents` | 12 agent statuses |
| `GET` | `/api/tokenomics` | Supply allocation |
| `GET` | `/api/dex/tokens` | DEX token list |
| `POST` | `/api/dex/swap` | Execute swap |
| `GET` | `/api/search/:q` | Search |
| `POST` | `/rpc` | Solana-compatible JSON-RPC |

---

## License

MIT

---

<p align="center">
  <strong>Private. Instant. Permissionless. That's X402.</strong>
  <br><br>
  <a href="https://sling402.io">sling402.io</a> · <a href="https://x.com/Sling402">@Sling402</a>
</p>
