---
label: Quick Start
---

# Run a Worker - Quick Start

_Insert Video Here_

## Clone autoloop-worker repo

## Install dependencies

```shell
yarn
```

## Set Credentials

- Create a `.env` file with RPC URL & wallet private key (see `.env-example`)

## Register worker

- Register wallet as AutoLoop worker. Make sure you have enough CKB to cover the registration fee (0.001 + tx gas). This fee is refunded immediately, but must be present to verify funds can be transferred to the worker.

```shell
yarn register-controller
```

## Run your worker

```shell
yarn start
```
