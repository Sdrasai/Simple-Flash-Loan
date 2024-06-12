# Simple Flash Loan Project

This project demonstrates how to create a simple flash loan contract using the Aave protocol on the Sepolia Ethereum testnet. 

## Overview

Flash loans are a type of uncollateralized loan that must be borrowed and repaid within the same transaction. They are primarily used for arbitrage, collateral swaps, and other advanced trading strategies. This project utilizes Aave's flash loan feature to perform such operations.

This is my first try for testing a flash loan of Aave platform using Solidity language. I was doing it by reading QuickNode guides about how to make a Flash Loan using Aave, this is the link:
https://www.quicknode.com/guides/defi/lending-protocols/how-to-make-a-flash-loan-using-aave
in this guide Polygun Mumbai network was used but I prefer the Etheruem Sepolia because as far as I undrestod it is not free...by the way I had some experince before with Sepolia so it was easier for me too.
you can find test net address here https://docs.aave.com/developers/deployed-contracts/v3-testnet-addresses

in this flash loan I used Rimex IDE for writing and deploying the contract with the envirement of injected provider metamask and MetaMask browser wallet
I deploy the contract on PoolAddressesProvider-Aave with this address 0x012bAC54348C0E635dCAc9D5FB99f06F24136C9A
you should have some SepoliaEth for paying the transaction ( you can get some in https://faucets.chain.link/sepolia )
after that you should go to https://staging.aave.com/faucet/ for some USDC faucets you should connect your wallet and after that you should send at least 1 USDC to thr contract that you deployed by copy the contract address and make the transfer.
And then in the remix IDE you should call the fn_RequestFlashLoan fanction and pass the USDC-TestnetMintableERC20-Aave with this address 0x94a9D9AC8a22534E3FaCa9F4e7F2E2cf85d5E4C8 in _token and pass 10000000 in _amount and after that you can press transact, and Doneeee...You did your first flash loan. 
## Prerequisites

- An Ethereum wallet (e.g., MetaMask)
- Sepolia Ethereum testnet ETH (for deploying and interacting with contracts)
- QuickNode account (optional, for accessing the Ethereum node)

## Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/simple-flash-loan.git
cd simple-flash-loan
