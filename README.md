# MyToken Smart Contract

## Introduction
This is a simple Solidity smart contract for creating and managing a basic ERC-20 token named "META" with the symbol "MTA". It allows users to mint new tokens and burn existing tokens.

## License
This smart contract is licensed under the MIT License. 
// SPDX-License-Identifier: MIT pragma solidity 0.8.18;

## Prerequisites
Before deploying and using this smart contract, you need the following:

- An Ethereum development environment such as Remix, Truffle, or Hardhat.
- An Ethereum wallet or a development account to interact with the contract.

## Contract Details

### Public Variables
The following public variables are available in the contract:

- `tokenname`: A string representing the name of the token, set to "META".
- `tokenabbrev`: A string representing the token's abbreviation or symbol, set to "MTA".
- `totalsupply`: An unsigned integer representing the total supply of tokens in circulation, initialized to 0.

### Mapping Variable
The contract uses a mapping to keep track of token balances of different addresses:

- `balances`: A mapping that associates an Ethereum address with the corresponding token balance. Users can query this mapping to check their token balance.

### Mint Function
The `mint` function allows the contract owner to create new tokens and assign them to a specified address.

#### Function Signature
```solidity
function mint(address _address, uint _value) public
```

#### Parameters
- `_address`: The Ethereum address to which the new tokens will be assigned.
- `_value`: The number of tokens to mint and add to the specified address.

### Burn Function
The `burn` function allows the contract owner to remove tokens from a specific address.

#### Function Signature
```solidity
function burn(address _address, uint _value) public
```

#### Parameters
- `_address`: The Ethereum address from which the tokens will be burned.
- `_value`: The number of tokens to burn from the specified address.

### Important Notes
- The `mint` function increases the total supply and the balance of the specified address.
- The `burn` function reduces the total supply and the balance of the specified address. The function only allows burning an amount equal to or less than the balance of the address.

## Usage
To use this smart contract, you can follow these steps:

1. Deploy the `MyToken` contract on the Ethereum network of your choice using your preferred development environment.
2. Interact with the contract using the available functions:
   - Call the `mint` function to create and assign new tokens to specific addresses.
   - Call the `burn` function to remove tokens from specific addresses.
## Authors
21bcs3833

