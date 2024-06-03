# ERC20 and Vault Contracts

## Overview

This repository contains two smart contracts: an ERC20 token contract and a Vault contract. The ERC20 contract implements the standard ERC20 token functionality, while the Vault contract provides a secure way to deposit, withdraw, and manage these tokens.

## Table of Contents

- [ERC20 Contract](#erc20-contract)
  - [Features](#features)
  - [Functions](#functions)
  - [Events](#events)
- [Vault Contract](#vault-contract)
  - [Features](#features-1)
  - [Functions](#functions-1)
  - [Events](#events-1)
- [Setup and Deployment](#setup-and-deployment)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
  - [Deployment](#deployment)
- [Testing](#testing)
- [License](#license)

## ERC20 Contract

### Features

- **Standard ERC20 Compliance**: Implements all mandatory functions and events of the ERC20 standard.
- **Minting and Burning**: Supports minting new tokens and burning existing tokens.
- **Allowance Mechanism**: Allows users to approve third parties to spend tokens on their behalf.

### Functions

- **`totalSupply()`**: Returns the total supply of tokens.
- **`balanceOf(address account)`**: Returns the balance of tokens for a specific account.
- **`transfer(address recipient, uint256 amount)`**: Transfers tokens to a recipient.
- **`allowance(address owner, address spender)`**: Returns the remaining number of tokens that a spender is allowed to spend on behalf of an owner.
- **`approve(address spender, uint256 amount)`**: Sets the amount of tokens that a spender is allowed to spend.
- **`transferFrom(address sender, address recipient, uint256 amount)`**: Transfers tokens from one account to another using an allowance mechanism.
- **`mint(address to, uint256 amount)`**: Mints new tokens to a specified account.
- **`burn(uint256 amount)`**: Burns a specified amount of tokens from the caller's account.

### Events

- **`Transfer(address indexed from, address indexed to, uint256 value)`**: Emitted when tokens are transferred.
- **`Approval(address indexed owner, address indexed spender, uint256 value)`**: Emitted when a new allowance is set.

## Vault Contract

### Features

- **Secure Token Storage**: Allows users to deposit and withdraw ERC20 tokens securely.
- **Ownership and Access Control**: Ensures only authorized users can perform sensitive actions.
- **Balance Tracking**: Maintains records of user balances and total deposits.

### Functions

- **`deposit(uint256 amount)`**: Deposits a specified amount of tokens into the vault.
- **`withdraw(uint256 amount)`**: Withdraws a specified amount of tokens from the vault.
- **`getBalance(address account)`**: Returns the balance of a specific user's deposits in the vault.
- **`totalDeposits()`**: Returns the total amount of tokens deposited in the vault.

### Events

- **`Deposited(address indexed account, uint256 amount)`**: Emitted when tokens are deposited.
- **`Withdrawn(address indexed account, uint256 amount)`**: Emitted when tokens are withdrawn.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
