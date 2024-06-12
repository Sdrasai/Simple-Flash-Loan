# Simple Flash Loan Project

This project demonstrates how to create a simple flash loan contract using the Aave protocol on the Sepolia Ethereum testnet.

## Overview

Flash loans are a type of uncollateralized loan that must be borrowed and repaid within the same transaction. They are primarily used for arbitrage, collateral swaps, and other advanced trading strategies. This project utilizes Aave's flash loan feature to perform such operations.

## Step-by-Step Guide

This is my first attempt at testing a flash loan on the Aave platform using Solidity. I followed the [QuickNode guide](https://www.quicknode.com/guides/defi/lending-protocols/how-to-make-a-flash-loan-using-aave), which uses the Polygon Mumbai network. However, I preferred the Ethereum Sepolia testnet because I have previous experience with it and it better suits my needs.

### Prerequisites

- An Ethereum wallet (e.g., MetaMask)
- Sepolia Ethereum testnet ETH (for deploying and interacting with contracts). You can get some from the [Sepolia Faucet](https://faucets.chain.link/sepolia).
- QuickNode account (optional, for accessing the Ethereum node)
- Aave testnet addresses can be found [here](https://docs.aave.com/developers/deployed-contracts/v3-testnet-addresses).

### Deployment and Interaction

1. **Writing and Deploying the Contract:**
   - Use Remix IDE with the environment set to "Injected Provider - MetaMask."
   - Deploy the contract on the Aave PoolAddressesProvider with the address `0x012bAC54348C0E635dCAc9D5FB99f06F24136C9A`.
   - Ensure you have some Sepolia ETH for transaction fees.

2. **Obtaining Test Tokens:**
   - Go to the [Aave Staging Faucet](https://staging.aave.com/faucet/) and connect your wallet.
   - Request some USDC test tokens.

3. **Funding the Contract:**
   - Transfer at least 1 USDC to your deployed contract by copying its address and making the transfer.

4. **Executing the Flash Loan:**
   - In Remix IDE, call the `fn_RequestFlashLoan` function.
   - Pass the USDC Testnet Mintable ERC20 Aave address `0x94a9D9AC8a22534E3FaCa9F4e7F2E2cf85d5E4C8` in `_token`.
   - Pass `10000000` in `_amount`.
   - Press "transact" to execute the flash loan.

### Using Hardhat

I used Hardhat in this repository to manage dependencies and compile the `SimpleFlashLoan.sol` contract, as VS Code couldn't resolve the import files.

1. **Install Dependencies:**

   ```bash
   npm init -y
   npx hardhat init
   npm install @aave/core-v3

   
