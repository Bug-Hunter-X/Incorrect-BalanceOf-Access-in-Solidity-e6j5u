# Incorrect BalanceOf Access in Solidity

This repository demonstrates a common error in Solidity smart contracts: incorrect access to a balance mapping.

The `bug.sol` file contains a flawed implementation of a token contract's `balanceOf` function.  It attempts to directly access the `balanceOf` variable, instead of using a mapping lookup. This leads to unexpected behavior and potentially incorrect balances. 

The `bugSolution.sol` file provides the corrected implementation, showing the correct way to access balances using a mapping lookup.

## How to Reproduce the Bug

1. Compile `bug.sol`. 
2. Deploy the contract. 
3. Try to get the balance of an address. The result will be incorrect.

## Solution

The corrected `balanceOf` function in `bugSolution.sol` correctly accesses the balance from the mapping.