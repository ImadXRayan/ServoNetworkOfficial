# SVO Tokenomics

## Token facts

| Field | Value |
|---|---|
| Name | Servo Coin |
| Symbol | SVO |
| Network | Polygon Mainnet |
| Standard | ERC-20 |
| Decimals | 18 |
| Maximum supply | 1,000,000,000 SVO |
| Contract | `0xD13BeA2028127a6067ea4CdDE4F6EaA243B82af8` |

The reviewed `SVOToken.sol` mints the complete fixed supply at deployment to the token contract and exposes no additional mint function. Tokens are burnable. Burning can reduce circulating and total supply; it cannot increase it.

## Contract-defined initial allocation

| Allocation | SVO | Share |
|---|---:|---:|
| Airdrop | 300,000,000 | 30% |
| Liquidity | 200,000,000 | 20% |
| Treasury | 200,000,000 | 20% |
| Team | 150,000,000 | 15% |
| Marketing | 100,000,000 | 10% |
| Ecosystem | 50,000,000 | 5% |
| **Total** | **1,000,000,000** | **100%** |

This table is taken from constants in the reviewed token contract. It supersedes the illustrative percentages currently present in the public repository.

## Documented utility

- Payment asset in supported marketplace escrow orders.
- Staking through the deployed staking contract.
- Activity rewards through a signed-voucher airdrop contract.
- Presale distribution through `SVOPresaleV2`.
- Application documentation describes a seller-fee reduction for stakers; **TODO: independently verify current eligibility and enforcement before treating this as guaranteed utility**.
- Governance appears as a future concept; it is not established as binding live governance.

## Administrative controls and holder risks

The owner can pause transfers, manage a blacklist, change limit exclusions, adjust anti-whale limits within contract minimums, or permanently disable those limits. Default limits are 1% of supply per transaction and 2% per receiving wallet, with exclusions for defined allocation addresses. These controls create owner-key and governance risk.

## Items not established by the reviewed evidence

- **Unverified:** current circulating supply and balances of allocation wallets.
- **Unverified:** external vesting enforcement for team allocations.
- **Unverified:** liquidity-lock terms or market-making commitments.
- **Unverified:** token listing price, future market value, or investment return.
- **Unverified:** legal or regulatory classification in any jurisdiction.

SVO documentation is informational only and is not financial advice.

