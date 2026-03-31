# Smart Contracts to Deploy on Base Chain

A collection of simple Solidity smart contract examples for learning and deploying on the Base blockchain.

## Overview

This repository contains 16 basic Solidity smart contracts (MUGI01.sol through MUGI16.sol) designed as educational examples for developers learning to deploy on Base Chain. Each contract demonstrates fundamental Solidity concepts with minimal complexity.

## Contracts

| Contract | Description | State Variable |
|----------|-------------|----------------|
| MUGI01.sol | Basic storage contract | `x = 101` |
| MUGI02.sol | Basic storage contract | `x = 102` |
| MUGI03.sol | Basic storage contract | `x = 103` |
| MUGI04.sol | Basic storage contract | `x = 104` |
| MUGI05.sol | Basic storage contract | `x = 105` |
| MUGI06.sol | Basic storage contract | `x = 106` |
| MUGI07.sol | Basic storage contract | `x = 107` |
| MUGI08.sol | Basic storage contract | `x = 108` |
| MUGI09.sol | Basic storage contract | `x = 109` |
| MUGI10.sol | Basic storage contract | `x = 110` |
| MUGI11.sol | Basic storage contract | `x = 111` |
| MUGI12.sol | Basic storage contract | `x = 112` |
| MUGI13.sol | Basic storage contract | `x = 113` |
| MUGI14.sol | Basic storage contract | `x = 114` |
| MUGI15.sol | Basic storage contract | `x = 115` |
| MUGI16.sol | Basic storage contract | `x = 116` |

## Prerequisites

- [Node.js](https://nodejs.org/) (v16 or higher)
- [Hardhat](https://hardhat.org/) or [Foundry](https://book.getfoundry.sh/)
- A Base network RPC endpoint
- A wallet with ETH on Base for gas fees

## Quick Start

### 1. Clone the Repository

```bash
git clone https://github.com/Mugi-wara2048/Smart-Contracts-To-Deploy-On-Base-Chain.git
cd Smart-Contracts-To-Deploy-On-Base-Chain
```

### 2. Install Dependencies

Using Hardhat:
```bash
npm install --save-dev hardhat
```

Using Foundry:
```bash
curl -L https://foundry.paradigm.xyz | bash
foundryup
```

### 3. Configure Environment

Create a `.env` file:
```env
PRIVATE_KEY=your_private_key_here
BASE_RPC_URL=https://mainnet.base.org
```

### 4. Deploy a Contract

Using Hardhat:
```bash
npx hardhat run scripts/deploy.js --network base
```

Using Foundry:
```bash
forge create --rpc-url $BASE_RPC_URL --private-key $PRIVATE_KEY src/MUGI01.sol:C1
```

## Base Network Details

| Network | Chain ID | RPC URL | Explorer |
|---------|----------|---------|----------|
| Base Mainnet | 8453 | https://mainnet.base.org | https://basescan.org |
| Base Sepolia | 84532 | https://sepolia.base.org | https://sepolia.basescan.org |

## Contract Structure

Each contract follows this simple pattern:

```solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.20;

contract C1 {
    uint public x = 101;
}
```

- **SPDX-License-Identifier**: MIT license for open-source usage
- **Pragma**: Solidity version 0.8.20 or higher
- **State Variable**: Public unsigned integer `x`

## Learning Path

These contracts are ideal for:

1. **First Deployment**: Practice deploying to Base testnet/mainnet
2. **Gas Estimation**: Compare deployment costs across contracts
3. **State Reading**: Learn to call `x()` to read contract state
4. **Verification**: Practice verifying contracts on BaseScan

## Verification

After deployment, verify your contract on BaseScan:

```bash
# Using Hardhat
npx hardhat verify --network base DEPLOYED_CONTRACT_ADDRESS

# Using Foundry
forge verify-contract --chain-id 8453 DEPLOYED_CONTRACT_ADDRESS src/MUGI01.sol:C1
```

## Security Considerations

⚠️ **Important**: These contracts are for educational purposes only:
- No access controls
- No upgradeability
- Minimal functionality
- Not audited

Do not use in production without proper security review.

## Contributing

Contributions are welcome! Please:
1. Fork the repository
2. Create a feature branch
3. Submit a pull request

## Resources

- [Base Documentation](https://docs.base.org/)
- [Solidity Documentation](https://docs.soliditylang.org/)
- [Base Faucet (Sepolia)](https://www.coinbase.com/faucets/base-ethereum-goerli-faucet)
- [BaseScan](https://basescan.org/)

## License

MIT License - see individual contract files for details.

---

**Happy Building on Base! 🚀**