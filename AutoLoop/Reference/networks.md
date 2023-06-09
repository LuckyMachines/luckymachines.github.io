---
label: Networks
---

# Supported Networks

- Ethereum
  - Sepolia testnet
- Polygon
  - Mumbai testnet
- Godwoken
  - Testnet
  - Mainnet

# Parameters

FeeRate % (baseFee): This percentage compensates the AutoLoop Network for maintaining you automation loop. Every time your contract executes progressLoop(), the contract balance is reduced by the cost plus this fee rate percentage.

Default Gas Limit (maxGasDefault): The maximum amount of gas that can be used by the client contract’s progressLoop() function + fees. You can set an upper limit on each contract from the AutoLoop dashboard, but this number must not exceed gasLimit() on the AutoLoop contract.

Default Max Gas Price (maxGasPriceDefault): The maximum gas price that can be used by the client contract’s performUpkeep function for the on-chain transaction. You can set an upper limit on your upkeep during registration, but this number must not exceed gasThreshold() on the AutoLoop contract.

# Network Settings

## Godwoken

### Godwoken Testnet

| Item                  | Value                                        |
| --------------------- | -------------------------------------------- |
| AutoLoop Address      | "0xef431960720c9bE6d37FF17E0d0Ce016c4072543" |
| Registry Address      | "0x1C03fABf5bceB4555B4B1343C74d7143c698D551" |
| Registrar Address     | "0x1D4c4a27077636E29167aaEF6555c6dbf54284F3" |
| Fee Rate              | 70%                                          |
| Default Gas Limit     | 1,000,000                                    |
| Default Max Gas Price | 40,000 gwei                                  |

### Godwoken Mainnet

| Item                  | Value       |
| --------------------- | ----------- |
| AutoLoop Address      | "0x000"     |
| Registry Address      | "0x000"     |
| Registrar Address     | "0x000"     |
| Fee Rate              | 70%         |
| Default Gas Limit     | 1,000,000   |
| Default Max Gas Price | 40,000 gwei |
