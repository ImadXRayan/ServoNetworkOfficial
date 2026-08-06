# How Servo Network Works

## Typical order lifecycle

1. A buyer browses a listing or posts a need.
2. The parties agree on scope, price, and delivery expectations in the platform.
3. For an on-chain order, the buyer approves the selected token and funds the Polygon escrow vault.
4. The application verifies the successful transaction and matching `Funded` event before marking payment confirmed.
5. The provider accepts, performs, and marks the service delivered.
6. The buyer approves completion, requests changes, or opens a dispute.
7. On release, the provider obtains a scoped signed voucher and calls the vault to collect. On refund, the buyer follows the equivalent refund path.
8. The application confirms or reconciles the blockchain result.

## Order states

The reviewed application documents this normal path:

`pending_payment → paid → accepted → in_progress → delivered → completed`

Branches include cancellation before payment, `redo_requested`, voluntary refund, and `disputed`. A dispute freezes normal transitions and auto-release until resolution.

## Supported settlement assets

The production escrow deployment record allows native Polygon USDC, Polygon USDT, and SVO. Each asset has its own decimals and per-deal cap. Support for other assets or chains must not be assumed from wallet display support.

## Fees and timing

The escrow contract defaults to a 5% fee on successful release and no fee on refund. The application documentation states a reduced 2% seller fee for SVO stakers; **TODO: verify the production rule and its enforcement path before publishing that discount as guaranteed**. Delivery currently schedules application-level auto-release after seven days; the provider still claims through the vault settlement path.

## Roles and responsibilities

- **Buyer:** defines the need, funds escrow, reviews delivery, and may request changes or dispute.
- **Provider:** accepts work, delivers it, and claims an authorized release.
- **Application:** calculates authoritative order values, enforces transitions, verifies events, and issues scoped vouchers.
- **Administrator:** reviews current disputes and records release/refund outcomes.
- **Smart contract:** stores funded deal data and enforces allowed assets, caller, voucher, nonce, state, fee, and transfer rules.

