# 🛡️ HeLa Stealth

**Privacy-preserving stablecoin payment gateway on HeLa blockchain.**

HeLa Stealth allows merchants to accept stablecoin payments with complete privacy. By generating one-time stealth payment addresses for every invoice, a merchant's main wallet transaction history remains shielded on public block explorers.

![HeLa Landing Page](C:\Users\risha\.gemini\antigravity\brain\3dda39d3-ba76-43d0-8223-e95083e6a228\hela_landing_page_final_1773542514094.png)

---

## Live Deployment (HeLa Testnet)

The project is fully operational on the **HeLa Testnet**.

### Smart Contracts
| Contract | Address |
|----------|---------|
| **HUSD** | `0xEf3cA15C04e82b90B01AF9EccE1A0C620E74E0b3` |
| **StealthRegistry** | `0x71741409c2F568735748D40F232Be35d43a48661` |
| **FeeManager** | `0xEA5399958B5848eBd835F888f4310e6b7D84B0Fb` |
| **PrivacyPool** | `0x098abE69A28b897d18E998a5F73Fc777e48fe365` |
| **PaymentRouter** | `0x15334Ef0e00F29F5ecCb03D765982F1282B05df8` |

---

## Key Features

1. **HeLa Brand Alignment**: Sleek, professional UI with the HeLa teal palette and glassmorphism.
2. **Stealth Payments**: One-time invoice IDs and stealth vaults protect user privacy.
3. **One-Chain Privacy**: Leverages HeLa's native privacy features on a single, intelligent blockchain.
4. **Seamless UX**: Unified "Connect Wallet" flow and high-impact hero design.

![Merchant Dashboard](C:\Users\risha\.gemini\antigravity\brain\3dda39d3-ba76-43d0-8223-e95083e6a228\merchant_dashboard_final_verify_1773542852945.png)

---

## Quick Start (Local Development)

### Prerequisites
- Node.js ≥ 18
- MetaMask browser extension
- HeLa testnet HLUSD

### 1. Install Dependencies
```bash
npm install && cd backend && npm install && cd ../frontend && npm install
```

### 2. Configure & Run
```bash
# Backend
cd backend && cp .env.example .env && npm start

# Frontend
cd frontend && cp .env.example .env && npm run dev
```

---

## Security & Architecture

- **One-time addresses**: Invoices are single-use, preventing linkability.
- **Atomic Operations**: Router handles deposit and release in a single transaction.
- **HeLa Privacy**: Built to leverage the unique privacy-preserving capabilities of the HeLa blockchain.

---

Built for the **HeLa Hackathon** 🚀
rotocol fee (default 0.00402 HUSD) |

## API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| `POST` | `/merchant/register` | Register merchant on-chain |
| `POST` | `/invoice/create` | Create payment invoice |
| `GET` | `/invoice/status/:id` | Check invoice status |
| `GET` | `/merchant/invoices/:address` | List merchant invoices |

## Security

- **One-time addresses**: Invoices are single-use, burned after payment
- **Replay protection**: Nonce-based invoice IDs prevent replay attacks
- **ReentrancyGuard**: Payment functions protected against reentrancy
- **Access control**: Mint is owner-only, invoices are merchant-only

## HeLa Chain Config

| Property | Value |
|----------|-------|
| Chain ID | `666888` |
| RPC | `https://testnet-rpc.helachain.com` |
| Explorer | `https://testnet-blockexplorer.helachain.com` |
| Currency | `HLUSD` |

---

Built for hackathon deployment on **HeLa blockchain** 🚀
