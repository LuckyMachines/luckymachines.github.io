---
label: Pricing
---

# AutoLoop Pricing

## Maximum Gas

AutoLoop enables you to define the maximum amount of gas for a transaction. It is essential to set this value sufficiently high to ensure your transaction gets successfully processed. The maximum gas value specifies the most computational work you're willing to expend to add a transaction to the Ethereum blockchain.

## Gas Price

Beyond the maximum gas limit, you can stipulate the maximum gas price as well. Our worker nodes continually work to provide you the best possible gas price, always staying within the confines of your defined limit. Bear in mind, Ethereum's gas prices can fluctuate, so allowing a higher limit offers more adaptability.

## Depositing and Withdrawing Gas

AutoLoop facilitates depositing Ether into your account, which can cover the gas costs for your transactions. You can also withdraw your deposited Ether as per your requirements. Remember, each transaction you execute through AutoLoop consumes gas, so ensure you have an adequate deposit of Ether to manage these costs.

## Pricing

AutoLoop pricing leverages the Ethereum network's gas system. Each transaction executed via AutoLoop uses gas, and the total cost corresponds to the gas consumed multiplied by the gas price.

AutoLoop applies a service fee to the contract. This total fee is a percentage of the gas used by the transaction, divided between the controller (the entity executing the function or "progressing the loop") and the AutoLoop protocol itself. These proportions are determined by the CONTROLLER_FEE_PORTION and PROTOCOL_FEE_PORTION variables.

For a detailed understanding of the cost, consider this formula:

```
fee = [gasUsed * tx.gasPrice * (1 + feeRate) + (149440 * tx.gasPrice)]
```

This formula allows you to estimate the cost of running our service, including both the gas costs and the AutoLoop fees.

Note that the total cost of using AutoLoop, i.e., executing a function or "progressing the loop," will be debited from your balance so always maintain an adequate amount of Ether deposited to cover both the gas costs and fees.
