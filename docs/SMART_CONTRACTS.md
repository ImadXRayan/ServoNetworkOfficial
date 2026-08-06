# Smart Contracts and Addresses

All active Servo contracts below are recorded for **Polygon Mainnet (`chainId 137`)** in `Servo Coin/deployments/polygon.json` at private-source commit `74255b0`. PolygonScan links are provided for independent inspection.

| Contract | Address | Purpose |
|---|---|---|
| Servo Coin (`SVOToken`) | [`0xD13BeA2028127a6067ea4CdDE4F6EaA243B82af8`](https://polygonscan.com/address/0xD13BeA2028127a6067ea4CdDE4F6EaA243B82af8) | Fixed-supply ERC-20 token |
| Presale (`SVOPresaleV2`) | [`0x11EE46f9c3bfAbD13DDE3F080B40401b7dA411eB`](https://polygonscan.com/address/0x11EE46f9c3bfAbD13DDE3F080B40401b7dA411eB) | Active SVO presale |
| Airdrop (`SVOAirdropSigned`) | [`0x3aE96E989B587C025df22738355111100c0F9ce8`](https://polygonscan.com/address/0x3aE96E989B587C025df22738355111100c0F9ce8) | Signed-voucher rewards |
| Staking (`SVOStaking`) | [`0xe9A8AB68f3cd39d9cFc5c2e8359a96515D2f8e24`](https://polygonscan.com/address/0xe9A8AB68f3cd39d9cFc5c2e8359a96515D2f8e24) | SVO staking plans |
| Order escrow (`SVOEscrowVault`) | [`0xC1E63463C5129c657E8B1c6d442121f09A361c88`](https://polygonscan.com/address/0xC1E63463C5129c657E8B1c6d442121f09A361c88) | Marketplace payment escrow |

## Referenced third-party tokens

| Asset | Polygon address |
|---|---|
| Native USDC | [`0x3c499c542cEF5E3811e1192ce70d8cC03d5c3359`](https://polygonscan.com/address/0x3c499c542cEF5E3811e1192ce70d8cC03d5c3359) |
| USDT | [`0xc2132D05D31c914a87C6611C10748AEb04B58e8F`](https://polygonscan.com/address/0xc2132D05D31c914a87C6611C10748AEb04B58e8F) |

## Retired deployments

| Contract | Address | Status |
|---|---|---|
| Presale v1 | `0x0996Db280828efB71193C8E1DcfB6Ef2636b7221` | Superseded by V2 |
| Escrow v1 | `0x3B29785096FA2DAd507B94F876F77Fd2f2678ffE` | Retired after token-decimal cap issue; source record states no funded deals |
| Escrow v2 | `0xd117E261913807aaC4cb5FEcD54fF01a5968A308` | Retired after collateral-recovery design issue; source record states all three deals were settled and balances were zero |

## Verification warning

Always compare an address against the current production deployment record, frontend configuration, and PolygonScan before interacting. A matching address does not establish that the contract has received an independent security audit. **Unverified:** third-party audit status.

