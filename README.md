# Error Handling 

This smart contract demonstrates different error handling techniques using the `require`, `assert`, and `revert` statements. It is important to properly handle errors in smart contracts to ensure the security and integrity of the blockchain.

## Description

The contract keeps track of balances in a mapping called 'balances'.
The mapping maps addresses to uint values, allowing us to store a numeric balance for each address.

### deposit function

The deposit function takes in an amount (_amount) and increments the balance mapping for msg.sender by that amount.
This "deposits" new tokens into the user's account balance.

### withdrawRequire function

First it validates that the balance for msg.sender is sufficient to withdraw the requested _amount using require.
If not enough balance, it will revert with an error message.
If there is enough balance, it decrements the mapping value by _amount to "withdraw" that amount.

### withdrawAssert function

Similar to withdrawRequire, but uses assert to check the balance condition.
If assertion fails, the transaction is reverted without a custom message.

### withdrawRevert function

Uses an if statement to check the balance condition.
If balance is insufficient, it reverts with a custom error message, and also returns the remaining gas back to the caller.
Otherwise, decrements the balance to withdraw the tokens. 

## Execution
To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/ 
Then compile this required file, and then deploy it.

## License
This project is licensed under the MIT License - see Copyright (c) 2023 shafiulla70
