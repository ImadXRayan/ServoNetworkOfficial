# Security

## Security model

Servo uses layered controls across clients, the application/database layer, and Polygon contracts. Web and mobile clients are untrusted. Authentication identifies a user; server/database authorization determines what the user may do; blockchain receipts, state, and events prove supported token movement.

## Key controls found in the reviewed source

- Row Level Security and separation of private profile/KYC data.
- Validated database procedures and Edge Functions for financial state changes.
- Exact receipt and event verification before confirming escrow activity.
- Single-use wallet-login and settlement nonces.
- Didit webhook HMAC and replay-window validation.
- OpenZeppelin token and escrow primitives, including safe transfers, pausing, reentrancy protection, and ownership.
- Escrow collateral accounting through `totalEscrowed`.
- Signed vouchers scoped to caller, orders, nonce, action, contract, and chain.

## Privileged roles

Owners and signers are material trust boundaries. Depending on the contract, owners can pause, configure tokens/caps, update signer or treasury, change fees within a hard ceiling, manage token blacklisting and limits, and perform other administrative functions. Operational security should use key separation, minimal balances, transaction review, monitoring, and tested rotation procedures.

## Important limitations

- This document is an engineering review, **not an independent audit or certification**.
- **Unverified:** a completed CertiK or other third-party audit.
- **Unverified:** a public bug-bounty program and stated reward pool.
- **Unverified:** production multisignature ownership for every privileged role.
- Presale KYC is documented as an application/UI gate; direct contract calls are not contract-level KYC gated.
- A compromised escrow signer cannot invent amounts, but can authorize improper settlement direction or timing for funded deals.
- Administrators currently decide disputes.

## Reporting a vulnerability

Please do not disclose an exploitable issue publicly before maintainers can respond.

**TODO before publication:** add a dedicated security contact, supported encryption key, expected acknowledgment window, disclosure policy, and bug-bounty status. Until those exist, use `contact@servo.network` and clearly mark the process as provisional.

Never include private keys, seed phrases, access tokens, personal data, or live exploit funds in a report.

