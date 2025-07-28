# OurToken

A simple ERC20 smart contract built with Solidity and Foundry framework.

## Description

OurToken is a standard ERC20 token implementation using OpenZeppelin contracts as the foundation. The token has the name "OurToken" with the symbol "OT".

## Features

- ✅ ERC20 standard compliance
- ✅ Customizable initial supply
- ✅ Transfer and approval functionality
- ✅ Built with OpenZeppelin for security

## Technologies Used

- **Solidity**: ^0.8.18
- **OpenZeppelin Contracts**: ERC20 implementation
- **Foundry**: Development framework and testing
- **Forge**: Build and testing tools

## Project Structure

```
├── src/
│   └── OurToken.sol          # Main token contract
├── script/
│   └── DeployOurToken.s.sol  # Deployment script
└── test/
    └── OurTokenTest.t.sol    # Unit tests
```

## Contract Details

### OurToken.sol

The main contract implementing the ERC20 token:

- **Name**: "OurToken"
- **Symbol**: "OT"
- **Initial Supply**: Determined at deployment
- **Decimals**: 18 (ERC20 default)

### DeployOurToken.s.sol

Deployment script with configuration:

- **Initial Supply**: 1,000 tokens (1000 ether in wei)
- Uses Foundry's broadcast for deployment

## Installation and Setup

1. Clone this repository
2. Install dependencies:
   ```bash
   forge install
   ```

3. Build contracts:
   ```bash
   forge build
   ```

## Testing

Run all tests:
```bash
forge test
```

Run tests with verbose output:
```bash
forge test -vv
```

### Test Coverage

This project includes tests for:

- ✅ Balance verification after transfer
- ✅ Allowance and transferFrom functionality
- ✅ Deployment verification

## Deployment

Deploy to local network:
```bash
forge script script/DeployOurToken.s.sol --rpc-url <RPC_URL> --private-key <PRIVATE_KEY> --broadcast
```

Deploy to testnet (example: Sepolia):
```bash
forge script script/DeployOurToken.s.sol --rpc-url $SEPOLIA_RPC_URL --private-key $PRIVATE_KEY --broadcast --verify --etherscan-api-key $ETHERSCAN_API_KEY
```

## Usage

After deployment, you can interact with the contract using:

1. **Foundry Cast**:
   ```bash
   cast call <CONTRACT_ADDRESS> "balanceOf(address)" <ADDRESS>
   ```

2. **Web3 libraries** (ethers.js, web3.py, etc.)

3. **Frontend applications**

## Security

- Contract uses OpenZeppelin's audited ERC20 implementation
- Follows best practices for smart contract development
- All functions use proper access control

## License

MIT License - see LICENSE file for full details.

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## Contact

If you have any questions or suggestions, please open an issue in this repository.