---
label: Quick Start
---

# Run a Worker - Quick Start

[![AutoLoop Worker Quick Start Video](https://img.youtube.com/vi/LvE5kftHXKk/hqdefault.jpg)](https://youtu.be/LvE5kftHXKk)

## Clone autoloop-worker repo

```shell
gh repo clone LuckyMachines/autoloop-worker
```

## Move into directory

```shell
cd autoloop-worker
```

## Install dependencies

```shell
yarn
```

## Set Credentials

- Create a `.env` file with RPC URL & wallet private key (see `.env-example`)

```shell
cp .env-example .env
```

```env
PRIVATE_KEY_TESTNET=<YOUR TESTNET PRIVATE KEY>
CHAIN_ID_TESTNET=71401
RPC_URL_TESTNET=https://v1.testnet.godwoken.io/rpc
PRIVATE_KEY=<YOUR PRIVATE KEY>
CHAIN_ID=71402
RPC_URL=https://v1.mainnet.godwoken.io/rpc
```

## Create `controller.config.json`

```shell
cp controller.config.example.json controller.config.json
```

```json
{
  "test": {
    "network": "godwoken_test",
    "allowList": [],
    "blockList": []
  },
  "main": {
    "network": "godwoken",
    "allowList": [],
    "blockList": []
  },
  "testMode": true
}
```

## Register worker

- Register wallet as AutoLoop worker. Make sure you have enough CKB to cover the registration fee (0.001 + tx gas). This fee is refunded immediately, but must be present to verify funds can be transferred to the worker.

```shell
yarn register-controller
```

## Run your worker

```shell
yarn start
```
