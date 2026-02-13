# Robinhood Chain Integration

# Robinhood Chain Integration

This module provides configuration for the Robinhood Chain testnet.

## Overview

Robinhood Chain Testnet is an Arbitrum Orbit Layer 2 built on Ethereum, using ETH as the native gas token.

## Network Details

- **Chain ID**: 46630
- **RPC URL**: https://rpc.testnet.chain.robinhood.com
- **WebSocket**: wss://feed.testnet.chain.robinhood.com
- **Explorer**: https://explorer.testnet.chain.robinhood.com
- **Faucet**: Deposit testnet funds via the official faucet or bridge Sepolia ETH

## Usage

```typescript
import { robinhoodTestnet } from './lib/chains';
import { createConfig } from 'wagmi';

const config = createConfig({
  chains: [robinhoodTestnet],
  // ... other config
});
```

## Resources

- [Robinhood Chain Explorer](https://explorer.testnet.chain.robinhood.com)