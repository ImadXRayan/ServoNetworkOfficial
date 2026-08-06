# Project Overview

## The goal

Servo Network aims to make service commerce more direct and transparent. A buyer needs confidence that payment will not be released before delivery; a provider needs confidence that an agreed payment exists. Servo combines a service marketplace with an on-chain escrow vault so supported funds follow explicit release or refund paths.

## Who it serves

- Buyers looking for local, remote, or professional services.
- Independent providers and freelancers offering those services.
- Crypto-native users who want wallet-to-wallet settlement.
- New users who may begin with conventional sign-in and connect a wallet when required.

## Product layers

1. **Marketplace:** discovery, profiles, listings, requests, offers, orders, messages, delivery, and reviews.
2. **Application authority:** authentication, permissions, order state, prices, evidence, KYC gates, settlement eligibility, and reconciliation.
3. **Blockchain settlement:** Polygon contracts hold supported assets and execute authorized releases or refunds.
4. **SVO ecosystem:** a fixed-supply utility token with payment, staking, airdrop, and presale components.

## What “decentralized” means here

Funds for supported escrow orders are held by a smart contract rather than a platform bank account. Their movement is visible through contract state and events. However, the product is hybrid rather than fully decentralized: application servers determine order eligibility, a signing service authorizes settlement direction, administrators currently resolve disputes, and contract owners can pause or update defined settings.

## Current versus planned

**Implemented in the reviewed source:** web marketplace flows; Polygon escrow; USDC, USDT, and SVO support; administrative dispute resolution; configurable Didit KYC; SVO token, staking, airdrop, and presale contracts.

**Roadmap / not established as live:** binding DAO governance, community-jury arbitration, multi-chain marketplace settlement, and broad native-mobile release.

## What Servo is not

Servo is not a bank, a guarantee that every service will be satisfactory, or a fully trustless arbitration court. On-chain escrow reduces a specific payment risk; identity, evidence quality, administrator decisions, software, keys, price sources, and user wallet security remain relevant trust and risk factors.

