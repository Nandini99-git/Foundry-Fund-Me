# Foundry Fund Me

A decentralized funding smart contract built with Solidity and Foundry.

This project allows users to fund the contract with ETH while enforcing a minimum USD-denominated contribution using Chainlink Price Feeds. The contract tracks contributors and allows only the contract owner to withdraw funds.

## About

This project was built while learning Solidity, Foundry, smart contract development, deployment workflows, testing, and blockchain security concepts.

The project includes deployment scripts, unit tests, integration tests, mock contracts, Chainlink integrations, and CI testing workflows.

## Features

* Accept ETH contributions
* Minimum USD funding requirement
* Chainlink Price Feed integration
* Owner-only withdrawals
* Custom errors and modifiers
* Fallback and receive functions
* Foundry deployment scripts
* Unit and integration testing
* Local Anvil deployment
* Sepolia deployment support
* GitHub Actions automated testing

## Technologies Used

* Solidity
* Foundry
* Anvil
* Chainlink Price Feeds
* Foundry DevOps
* Alchemy RPC
* Sepolia Testnet
* Git & GitHub
* GitHub Actions
* WSL

## Project Structure

```text
src/
├── FundMe.sol
├── PriceConverter.sol

script/
├── DeployFundMe.s.sol
├── DeployStorageFun.s.sol
├── HelperConfig.s.sol
├── Interactions.s.sol

test/
├── FundMeTest.t.sol
├── FundMeDeploy.t.sol
├── integration/
│   └── InteractionsTest.t.sol
├── mock/
│   └── MockV3Aggregator.sol
├── ZkSyncDevOps.t.sol
```

## What I Learned

Through this project I gained hands-on experience with:

* Solidity smart contract development
* Foundry development workflow
* Local blockchain testing with Anvil
* Smart contract deployment using Forge scripts
* Chainlink oracle integration
* Unit and integration testing
* Environment variable management
* Private key security practices
* Transaction broadcasting and on-chain execution
* Git and GitHub workflows
* Basic Layer 2 and Foundry zkSync development concepts

## Requirements

* Git
* Foundry
* Alchemy RPC URL
* Testnet ETH (for deployment)

## Installation

```bash
git clone https://github.com/Nandini99-git/Foundry-Fund-Me.git
cd Foundry-Fund-Me
forge install
```

## Testing

Run all tests:

```bash
forge test
```

Generate gas report:

```bash
forge snapshot
```

Generate coverage:

```bash
forge coverage
```

## Deployment

Start a local Anvil node:

```bash
anvil
```

Deploy locally:

```bash
forge script script/DeployFundMe.s.sol
```

Deploy to Sepolia:

```bash
forge script script/DeployFundMe.s.sol \
--rpc-url $SEPOLIA_RPC_URL \
--private-key $PRIVATE_KEY \
--broadcast
```

## Future Goals

* Explore smart contract security testing
* Learn vulnerability analysis and auditing techniques
* Improve gas optimization knowledge
* Deploy additional projects to testnets
* Continue learning Layer 2 ecosystems and blockchain security

## Disclaimer

This repository was created for educational purposes as part of my Solidity, Foundry, and blockchain security learning journey.
