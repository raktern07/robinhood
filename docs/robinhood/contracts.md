# Robinhood Chain Contract Addresses

# Robinhood Chain Contract Addresses

Reference for official contract addresses on Robinhood Chain Testnet.

## Token Contracts (L2)

| Contract | Address |
|----------|---------|
| WETH | `0x7943e237c7F95DA44E0301572D358911207852Fa` |
| TSLA | `0xC9f9c86933092BbbfFF3CCb4b105A4A94bf3Bd4E` |
| AMZN | `0x5884aD2f920c162CFBbACc88C9C51AA75eC09E02` |
| PLTR | `0x1FBE1a0e43594b3455993B5dE5Fd0A7A266298d0` |
| NFLX | `0x3b8262A63d25f0477c4DDE23F83cfe22Cb768C93` |
| AMD | `0x71178BAc73cBeb415514eB542a8995b82669778d` |

## L2 Bridge & Gateways

| Contract | Address |
|----------|---------|
| L2 Gateway Router | `0x77bF00A6A90c600f214b34BAFBB7918c0cF113A8` |
| L2 ERC20 Gateway | `0x8689aFB9086734e12beA6b5DF541a1da252Ea32a` |
| L2 WETH Gateway | `0x5A8F55202A625D12FFCb76F857FE4563bC8Ce413` |
| L2 WETH | `0x7943e237c7F95DA44E0301572D358911207852Fa` |
| L2 Multicall | `0xa432504b6F04Cafe775b09D8AA92e8dbe41Ec7a8` |

## Precompiles

Arbitrum precompiles are at fixed addresses on every L2 chain.

| Contract | Address |
|----------|---------|
| ArbSys | `0x0000000000000000000000000000000000000064` |
| ArbInfo | `0x0000000000000000000000000000000000000065` |
| ArbGasInfo | `0x000000000000000000000000000000000000006C` |
| ArbRetryableTx | `0x000000000000000000000000000000000000006E` |
| NodeInterface | `0x00000000000000000000000000000000000000C8` |
| ... | See `robinhood-contracts.ts` for full list |

## Usage

```typescript
import { ROBINHOOD_CONTRACTS } from './robinhood-contracts';

const wethAddress = ROBINHOOD_CONTRACTS.WETH;
```