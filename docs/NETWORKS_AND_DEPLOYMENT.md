# Networks and Deployment

## Production settlement network

Servo’s reviewed marketplace contracts are deployed on **Polygon Mainnet**, chain ID `137`. Polygon is EVM-compatible and was selected in the project documentation for lower fees and faster confirmations than Ethereum Mainnet.

The web wallet configuration can display or connect to Polygon, Ethereum, and BNB Smart Chain. That does **not** mean marketplace escrow is deployed on all three networks. The reviewed production escrow address and settlement verification are Polygon-specific.

## Supported escrow assets

| Asset | Decimals | Deployment-record cap per deal |
|---|---:|---:|
| Native Polygon USDC | 6 | 5,000 USDC |
| Polygon USDT | 6 | 5,000 USDT |
| SVO | 18 | 125,000 SVO |

Caps are owner-configurable contract settings. Verify current on-chain values before presenting them as permanent.

## Deployment verification checklist

Before any public release:

1. Compare every address with the current production deployment JSON.
2. Compare frontend, backend shared configuration, and public docs.
3. Confirm the expected chain ID and bytecode/source status on PolygonScan.
4. Read owner, signer, treasury, fee, token allow-list, caps, and pause state from chain.
5. Check that retired addresses are not referenced by live routes.
6. Run contract tests and the repository address-consistency check.
7. Perform a small-value end-to-end funding and settlement smoke test.

## Environment boundaries

Public client configuration may contain public project identifiers. Private keys, service-role credentials, voucher-signing keys, webhook secrets, OAuth secrets, and deployment credentials must remain server- or CI-only and must never enter this documentation repository.

## Unverified publication items

- Current frontend and backend deployment commit hashes.
- Current Cloudflare and Supabase production release identifiers.
- Live on-chain values at the eventual publication time.

