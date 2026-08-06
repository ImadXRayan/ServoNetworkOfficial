# Escrow System

## Design

`SVOEscrowVault` records each funded order’s buyer, provider, asset, amount, and state. The settlement voucher contains the caller, order list, nonce, action, vault, and chain—not an amount. Amounts are read from the deal recorded during funding.

## Funding

The buyer calls `fund(orderId, seller, token, amount)`. The contract requires a new order identifier, an allowed token, a nonzero amount within that token’s cap, and a nonzero provider. It records state before transferring tokens with `SafeERC20`. The application only confirms payment after checking chain `137`, the receipt, vault, parties, token, amount, and exact event.

## Release

The provider calls `claimBatch` with one or more order IDs and a single-use signed voucher. For each funded deal, the contract changes state, decreases tracked collateral, sends the net payout to the provider, sends the configured fee to treasury, and emits `Released`.

## Refund

The buyer calls `refundBatch` with an authorized voucher. The contract returns the recorded amount in full, charges no fee, and emits `Refunded`.

## Auto-release

The reviewed application sets an `auto_release_at` timestamp when delivery is recorded, using a seven-day default. This is an application authorization process, not an autonomous timer inside the smart contract. The provider’s on-chain claim and matching event remain necessary to prove funds moved.

## Safety controls

- `SafeERC20`, `ReentrancyGuard`, and `Pausable`.
- Token allow-list and token-specific deal caps.
- Single funding per order ID and single-use voucher nonces.
- Caller, action, vault, and chain binding in signatures.
- State updated before external token transfer.
- `totalEscrowed[token]` protects open collateral from `recoverStray`.
- Contract fee ceiling of 20%; configured default is 5%.

## Trust and limitations

The owner can change the signer, treasury, fee, supported-token settings, caps, and pause state. A compromised authorized signer cannot invent a larger amount, but may wrongly authorize the timing or direction of an otherwise funded deal. Key separation, monitoring, and rapid signer rotation are therefore essential.

Contract address: see [Smart Contracts](SMART_CONTRACTS.md).

