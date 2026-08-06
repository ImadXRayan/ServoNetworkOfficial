# Servo Network

**A Web3 marketplace for local and professional services, with on-chain escrow on Polygon.**

Servo Network connects buyers with service providers. Buyers can discover or request services, providers can deliver them, and supported crypto payments are locked in a smart-contract vault until release or refund. The product combines a React/Vite web application, a Supabase application layer, wallet-based payments, and Polygon smart contracts.

> **Documentation status:** Draft for public review. Facts are sourced from the private production repository at commit `74255b0` and the public documentation repository at commit `1f40c57`, reviewed on 2026-08-06. Nothing in this package has been published. Items marked **Unverified** or **TODO** must be confirmed before release.

## Start here

| Document | What you will learn |
|---|---|
| [Project overview](docs/OVERVIEW.md) | The project’s purpose, audience, value proposition, and current scope |
| [How Servo works](docs/HOW_IT_WORKS.md) | The buyer/provider journey from discovery to settlement |
| [Whitepaper](docs/WHITEPAPER.md) | Product, architecture, trust model, economics, roadmap, and risks |
| [Escrow system](docs/ESCROW.md) | Funding, delivery, release, refunds, auto-release, and reconciliation |
| [Dispute resolution](docs/DISPUTE_RESOLUTION.md) | Evidence, freezes, administrative decisions, and on-chain settlement |
| [Smart contracts & addresses](docs/SMART_CONTRACTS.md) | Verified production addresses, roles, and retired deployments |
| [Tokenomics](docs/TOKENOMICS.md) | Source-backed SVO supply, allocation, utility, and controls |
| [Networks & deployment](docs/NETWORKS_AND_DEPLOYMENT.md) | Production chain, supported assets, and verification guidance |
| [Security](SECURITY.md) | Trust boundaries, controls, limitations, and responsible reporting |
| [FAQ](docs/FAQ.md) | Plain-language answers to common questions |
| [Glossary](docs/GLOSSARY.md) | Definitions of platform and blockchain terms |
| [Contributing](CONTRIBUTING.md) | How to propose safe documentation improvements |

## What the platform is for

Servo is designed for real-world services such as delivery, repair, tutoring, pet care, consulting, freelance work, and other buyer-provider agreements. Its central goal is to reduce payment uncertainty: supported payments are recorded and held on-chain, while the application manages service discovery, orders, messages, delivery states, evidence, and authorization.

The system does **not** remove every trusted party. The current dispute process is platform-administered, the backend authorizes settlement direction through signed vouchers, and contract owners retain emergency and configuration powers. Future DAO or community-jury arbitration is a roadmap concept, not current functionality.

## Current production foundation

- Marketplace web application with service listings, orders, messaging, delivery, and reviews.
- Polygon Mainnet (`chainId 137`) settlement for supported escrow payments.
- Escrow support for Polygon USDC, Polygon USDT, and SVO.
- SVO token, presale, signed-voucher airdrop, staking, and order-escrow contracts.
- Email, social, and wallet-based authentication; configurable KYC gates.
- Supabase-backed application data, authorization, Edge Functions, and reconciliation.

## Important notices

- This repository is documentation, not financial, legal, or investment advice.
- Smart contracts and crypto assets involve loss, key-management, market, operational, and regulatory risks.
- “Verified” in the contracts document means source/address consistency in the reviewed repository and its stated PolygonScan links. It does not mean independently audited.
- **Unverified:** No evidence reviewed for this package establishes a completed CertiK or other third-party audit, a live DAO, a live bug-bounty program, or a production multisignature treasury. Do not claim these publicly without evidence.

## Official links

- Website: [servo.network](https://servo.network)
- X: [@xServoNetwork](https://x.com/xServoNetwork)
- Telegram: [t.me/servonetwork](https://t.me/servonetwork)
- Email: `contact@servo.network`
- **TODO:** Confirm the official Discord invite and preferred public support email before publication.

