# Solidity by Example ERC-20 Token Contract

## Overview

This contract represents a basic implementation of the ERC-20 token standard in the Solidity programming language. It provides functionalities for token transfers, approvals, and a basic minting and burning mechanism.

## SPDX-License-Identifier

This contract is licensed under the MIT License. Please refer to the [MIT License](https://opensource.org/licenses/MIT) for the full text.

## Prerequisites

- Solidity version: ^0.8.17

## ERC-20 Token Details

- **Name:** Solidity by Example
- **Symbol:** SOLBYEX
- **Decimals:** 18

## Functions

### `transfer`

solidity
function transfer(address recipient, uint amount) external returns (bool);
Transfers a specified amount of tokens from the sender's account to the recipient's account.

### approve
function approve(address spender, uint amount) external returns (bool);
Approves the spender to spend a specified amount of tokens on behalf of the owner.

### transferFrom
function transferFrom(address sender, address recipient, uint amount) external returns (bool);
Transfers a specified amount of tokens from the sender's account to the recipient's account, provided the sender has been approved by the owner.

### mint
function mint(uint amount) external;
Mints a specified amount of new tokens, adding them to the total supply and the sender's balance.

### burn
function burn(uint amount) external;
Burns a specified amount of tokens, reducing the total supply and the sender's balance.

# Vault Contract for ERC-20 Tokens

## Overview

The Vault contract is designed to securely manage deposits and withdrawals of ERC-20 tokens while issuing and redeeming corresponding shares to participants. This implementation follows the ERC-20 interface for compatibility and transparency.

## SPDX-License-Identifier

This contract is licensed under the MIT License. Please refer to the [MIT License](https://opensource.org/licenses/MIT) for the full text.

## ERC-20 Interface

This contract includes the standard ERC-20 interface as specified by the `IERC20` interface. This allows seamless interaction with the ERC-20 ecosystem.

## Vault Contract

The `Vault` contract manages deposits and withdrawals of ERC-20 tokens while issuing and redeeming shares to participants.

### Constructor

```solidity
constructor(address _token) {
    token = IERC20(_token);
}
