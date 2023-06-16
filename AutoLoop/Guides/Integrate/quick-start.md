---
label: Quick Start
---

# AutoLoop Integration - Quick Start

[!embed](https://www.youtube.com/embed/UZ3DOq8zsWc)

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

Open the AutoLoop Dashboard:

- [Godwoken](https://autoloop-godwoken.luckymachines.io/)
- [Godwoken Testnet](https://autoloop-godwoken-testnet.luckymachines.io/)

### Connect your wallet

![](/images/al/click-connect.png)

### Select Register Contract

![](/images/al/click-register.png)

### Choose Settings and Funding Amount

![](/images/al/registration-details.png)

### Register Contract

![](/images/al/click-final-register.png)

### Manage Registered Contracts

![Click on contract address to manage](/images/al/click-contract-address.png)
