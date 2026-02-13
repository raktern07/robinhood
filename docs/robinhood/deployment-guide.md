# Robinhood Chain Deployment Guide

# Robinhood Chain Deployment Guide

This guide walks through deploying smart contracts to Robinhood Chain, an Arbitrum Orbit Layer 2.
The flow is similar to deploying to Ethereum or other Arbitrum chains.

## Prerequisites

- Node.js (v18+ recommended)
- A wallet with testnet ETH on Robinhood Chain
- A smart contract project using Hardhat, Foundry, or another Ethereum-compatible framework

## Network Configuration

Add Robinhood Chain Testnet to your development environment:

| Parameter | Value |
|-----------|-------|
| Network Name | Robinhood Chain Testnet |
| RPC URL | https://rpc.testnet.chain.robinhood.com |
| Chain ID | 46630 |
| Currency | ETH |
| Block Explorer | https://explorer.testnet.chain.robinhood.com |## Hardhat Setup

### Initialize project (if needed)

```bash
mkdir rh-deploy
cd rh-deploy
npm init -y
npm install --save-dev hardhat
npx hardhat init
```

### Configure network (hardhat.config.ts)

```typescript
networks: {
  robinhood: {
    url: "https://rpc.testnet.chain.robinhood.com",
    accounts: process.env.PRIVATE_KEY ? [process.env.PRIVATE_KEY] : [],
    chainId: 46630,
  },
},
```

Store your private key securely via environment variables (e.g. `.env`).## Example Contract

Create a simple contract to deploy:

```solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.20;

contract HelloRobinhood {
    function hello() external pure returns (string memory) {
        return "Hello, Robinhood Chain!";
    }
}
```## Deploy Script

```bash
npx hardhat run scripts/deploy.ts --network robinhood
```

After deployment, you'll see the contract address in the output.## Verify the Contract

To verify on the Robinhood Chain block explorer, use your tooling's verification plugin.
Verification steps are identical to other Arbitrum chains (Hardhat Etherscan plugin, Foundry verify, etc.).## Interacting With Your Contract

After deployment you can:

- Call contract methods using scripts or a frontend
- Integrate with wallets that support Arbitrum-based chains
- Monitor transactions via the [block explorer](https://explorer.testnet.chain.robinhood.com)

## Resources

- [Robinhood Chain Explorer](https://explorer.testnet.chain.robinhood.com)
- [Robinhood Chain Documentation](https://docs.robinhood.xyz)