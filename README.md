# FundMe Smart Contract

A decentralized funding smart contract built with Solidity and Foundry.

This project allows users to fund the contract with ETH while enforcing a minimum USD-denominated contribution using Chainlink Price Feeds. The contract tracks contributors and allows only the contract owner to withdraw funds.

## About The Project

This project was built as part of my Solidity and blockchain security learning journey while exploring smart contract development, deployment workflows, oracle integration, and secure key management practices.

## Features

* Accept ETH contributions
* Minimum USD-denominated funding requirement
* Chainlink Price Feed integration
* Owner-only withdrawal functionality
* Custom errors and modifiers
* Fallback and receive functions
* Deployment using Foundry scripts
* Local testing with Anvil
* Testnet deployment support

## Technologies Used

* Solidity
* Foundry
* Anvil
* Chainlink Price Feeds
* Alchemy RPC
* Sepolia Testnet
* Git & GitHub
* WSL

## Contract Overview

### FundMe.sol

Main funding contract that:

* Accepts ETH contributions
* Tracks funders and contribution amounts
* Validates minimum contribution value in USD
* Restricts withdrawals to the contract owner

### PriceConverter.sol

Library used to:

* Fetch ETH/USD prices through Chainlink
* Convert ETH amounts into USD values
* Support funding validation logic

## What I Learned

Through this project I gained hands-on experience with:

* Solidity smart contract development
* Foundry development workflow
* Local blockchain testing using Anvil
* Deploying contracts through Forge scripts
* Transaction broadcasting and on-chain execution
* Environment variable management
* Private key security practices
* Chainlink oracle integration
* Smart contract project structure
* Basic Layer 2 and Foundry zkSync workflows

## Project Structure

src/

* FundMe.sol
* PriceConverter.sol

script/

* DeployFundMe.s.sol
* Interactions.s.sol

test/

* FundMeTest.t.sol

## Requirements

* Git
* Foundry
* Alchemy RPC URL
* Sepolia testnet ETH (optional for deployment)

## Installation

Clone the repository:

```bash
git clone https://github.com/Nandini99-git/Foundry-Fund-Me
cd fundme
```

Install dependencies:

```bash
forge install
```

## Testing

Run all tests:

```bash
forge test
```

Generate coverage:

```bash
forge coverage
```

## Deployment

Deploy locally using Anvil:

```bash
anvil
forge script script/DeployFundMe.s.sol
```

Deploy to Sepolia:

```bash
forge script script/DeployFundMe.s.sol \
--rpc-url $SEPOLIA_RPC_URL \
--private-key $PRIVATE_KEY \
--broadcast
```

## Future Improvements

* Additional security-focused testing
* Expanded integration tests
* Gas optimization
* Support for multiple funding assets
* Further smart contract security analysis

## Disclaimer

This project was built for educational and learning purposes while studying Solidity, Foundry, blockchain security, and smart contract development.
