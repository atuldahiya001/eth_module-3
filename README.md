# eth_module-3
# AtulDeepuToken Solidity Smart Contract

This repository contains a Solidity smart contract named `AtulDeepuToken`, implementing an ERC-20 token on the Ethereum blockchain. The contract provides functionalities for token creation, transfers, minting, and burning.

## Token Details

- **Name:** AtuldeepuToken
- **Symbol:** ADT
- **Decimals:** 16
- **Total Supply:** 10,000,000,000,000,000 ADT (10 * 10^16)

## Contract Owner

The contract is owned by the address that deploys it, which is set as the initial owner. The owner has exclusive access to certain functions using the `onlyOwner` modifier.

## Functions

### Constructor

The constructor initializes the token's basic details, including its name, symbol, and decimal places. It also sets the initial total supply and allocates this supply to the contract deployer. Additionally, it calls the `_mintTokens` function to allocate an extra 30 * 10^16 ADT tokens to the contract deployer.

### Minting

The contract owner can mint new tokens using the `mint` function. Minted tokens are allocated to a specified address. The function internally calls the `_mintTokens` function to handle the minting process.

### Burning

Token holders can burn their own tokens using the `burn` function. Burning tokens reduces the total supply and the balance of the token holder.

### Transfer

The `transfer` function allows token holders to transfer ADT tokens to another address. It requires a valid destination address and checks if the sender has a sufficient balance to make the transfer.

## Events

The contract emits two types of events:

- `Transfer`: Emitted when tokens are transferred from one address to another. Includes information about the sender, recipient, and transferred amount.
- `Mint`: Emitted when new tokens are minted and allocated to a specific address. Includes information about the recipient and minted amount.

## Modifiers

### `onlyOwner`

A modifier that restricts access to certain functions, allowing them to be executed only by the contract owner.

## Security Considerations

This smart contract provides basic ERC-20 functionality, including token transfers, minting, and burning. However, before deploying this contract to a production environment, thorough testing and security auditing are recommended to ensure the contract's robustness and protect against potential vulnerabilities.

 
