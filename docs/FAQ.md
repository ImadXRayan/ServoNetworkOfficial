# Frequently Asked Questions

## What is Servo Network?

Servo is a marketplace for local and professional services. It combines conventional marketplace features with Polygon-based escrow for supported crypto payments.

## Is Servo fully decentralized?

No. Escrow custody and settlement enforcement are on-chain, but the product currently relies on application services for order state and vouchers, administrators for disputes, and owners for contract configuration and emergency controls.

## Which network is used for escrow?

Polygon Mainnet (`chainId 137`). Wallet support for other chains does not imply escrow deployment there.

## Which assets can fund escrow?

The reviewed production record lists native Polygon USDC, Polygon USDT, and SVO.

## Who holds the money during an order?

For supported on-chain orders, the escrow smart contract holds the funded tokens. They are not held in a platform bank account.

## How does a provider get paid?

After completion is authorized, the provider requests a signed voucher and submits a batch claim to the vault. The contract pays the provider and sends the configured fee to treasury.

## What happens if a buyer does not respond?

The reviewed application schedules authorization for auto-release seven days after delivery. This timing is application-managed; the on-chain claim must still occur.

## What happens in a dispute?

Normal transitions and auto-release stop. A platform administrator reviews available evidence and selects release or refund. DAO/community arbitration is not currently live.

## Are refunds charged a platform fee?

The reviewed escrow contract returns the recorded amount to the buyer without a fee.

## Has Servo been independently audited?

**Unverified.** The reviewed source contains audit claims in a website page but no supporting report was established during this review. Do not claim an audit until a verifiable report is linked.

## What is SVO?

SVO is a fixed-supply, 18-decimal ERC-20 utility token on Polygon used across the Servo ecosystem. See [Tokenomics](TOKENOMICS.md).

## Is SVO an investment?

This documentation provides technical and product information, not financial or investment advice. Crypto assets are high risk.

