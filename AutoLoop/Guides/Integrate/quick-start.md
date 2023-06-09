---
label: Quick Start
---

# AutoLoop Integration - Quick Start

[![AutoLoop Quick Start Video](https://img.youtube.com/vi/UZ3DOq8zsWc/hqdefault.jpg)](https://youtu.be/UZ3DOq8zsWc)

## Inherit from AutoLoopCompatible.sol

```solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.7;

import "@luckymachines/autoloop/contracts/AutoLoopCompatible.sol";

contract NumberGoUp is AutoLoopCompatible {
    // ... contract code
}
```

## Add required methods

```solidity
function shouldProgressLoop()
    external
    view
    returns (bool loopIsReady, bytes memory progressWithData)
{
    loopIsReady = (block.timestamp - lastTimeStamp) > interval;
    // pass a loop ID to avoid running the same update twice
    progressWithData = bytes(abi.encode(_loopID));
}

function progressLoop(bytes calldata progressWithData) external {
    // decode the data sent from shouldProgressLoop()
    uint256 loopID = abi.decode(progressWithData, (uint256));

    // re-check logic
    if ((block.timestamp - lastTimeStamp) > interval && loopID == _loopID) {
        updateNumber();
        ++_loopID;
    }
}
```

## Register AutoLoop compatible contract

Open your [AutoLoop dashboard](https://auto-loop-ui-godwoken.vercel.app/)

### Connect your wallet

_Insert Screenshot Here_

### Select Register Contract

_Insert Screenshot Here_

### Choose Settings and Funding Amount

_Insert Screenshot Here_

### Register Contract

_Insert Screenshot Here_

### Manage Registered Contracts

_Insert Screenshot Here_
