---
label: Networks
---

# Supported Networks

- [Godwoken](#godwoken)
  - [Testnet](#godwoken-testnet)
  - [Mainnet](#godwoken-mainnet)
- [Ethereum](#ethereum)
  - [Testnet](#sepolia-testnet)

# Parameters

**FeeRate % (baseFee):** This percentage compensates the AutoLoop Network for maintaining you automation loop. Every time your contract executes progressLoop(), the contract balance is reduced by the cost plus this fee rate percentage.

**Default Gas Limit (maxGasDefault):** The maximum amount of gas that can be used by the client contract’s progressLoop() function + fees. You can set an upper limit on each contract from the AutoLoop dashboard, but this number must not exceed gasLimit() on the AutoLoop contract.

**Default Max Gas Price (maxGasPriceDefault):** The maximum gas price that can be used by the client contract’s performUpkeep function for the on-chain transaction. You can set an upper limit on your upkeep during registration, but this number must not exceed gasThreshold() on the AutoLoop contract.

# Network Settings

## Godwoken

### Godwoken Testnet

|                       |                                              |
| --------------------- | -------------------------------------------- |
| AutoLoop Address      | "0x231131411F3E0FEa07fd3fAC6f24C87aEE8a57e9" |
| Registry Address      | "0x1eB69dc3AC3D5BfE159930735a0E248b8959A659" |
| Registrar Address     | "0x57D884821754CB5d5A73ff142127b7182e4834D9" |
| Fee Rate              | 70%                                          |
| Default Gas Limit     | 1,000,000                                    |
| Default Max Gas Price | 40,000 gwei                                  |

### Godwoken Mainnet

|                       |                                              |
| --------------------- | -------------------------------------------- |
| AutoLoop Address      | "0xBB2E62b3c50C9087f9db6f991148B7871Bd3dBC0" |
| Registry Address      | "0x233641cFC9b8D01618c5982b5B4511e855Ae8213" |
| Registrar Address     | "0xCEb3F8A47b694EeB1970be1B4aD4003eB0a7edEA" |
| Fee Rate              | 70%                                          |
| Default Gas Limit     | 1,000,000                                    |
| Default Max Gas Price | 40,000 gwei                                  |

## Ethereum

### Sepolia Testnet

|                       |                                              |
| --------------------- | -------------------------------------------- |
| AutoLoop Address      | "0xe53C418aA170abB87D6449403EA70FD6C82Bc9c2" |
| Registry Address      | "0xB9B408F892bCE310Ebbf257f932D461CA81c4738" |
| Registrar Address     | "0x86c45946b0dDF290d8ab9931C2d09a26481d4e72" |
| Fee Rate              | 15%                                          |
| Default Gas Limit     | 1,000,000                                    |
| Default Max Gas Price | 100 gwei                                     |
