# 🚀 FundMe Smart Contract (Foundry)

A simple crowdfunding smart contract built using **Solidity** and **Foundry**, allowing users to fund ETH and enabling the owner to withdraw funds.

---

## 🧰 Tech Stack

- Solidity  
- Foundry (Forge, Cast, Anvil)  
- Chainlink Price Feeds  
- Sepolia Testnet  

---

## ⚡ Foundry Overview

**Foundry** is a fast, portable, and modular toolkit for Ethereum development written in Rust.

It includes:

- **Forge** → Testing framework  
- **Cast** → CLI for interacting with contracts  
- **Anvil** → Local Ethereum node  
- **Chisel** → Solidity REPL  

📖 Docs: https://book.getfoundry.sh/

---

## 📦 Setup

### 1. Install Foundry
```bash
curl -L https://foundry.paradigm.xyz | bash
foundryup
```

---

## 🔧 Environment Variables

Create a `.env` file in the root directory:

```env
SEPOLIA_RPC_URL=<your_rpc_url>
PRIVATE_KEY=<your_private_key>
ETHERSCAN_API_KEY=<your_etherscan_api_key>
```

### 🔐 Notes:
- **PRIVATE_KEY** → Use a test wallet (⚠️ never use a wallet with real funds)  
- **SEPOLIA_RPC_URL** → Get from Alchemy or Infura  
- **ETHERSCAN_API_KEY** → Optional, used for contract verification  

---

## 💸 Get Testnet ETH

- Visit: https://faucets.chain.link  
- Request Sepolia ETH  
- Check balance in MetaMask  

---

## 🛠️ Usage

### 🔨 Build
```bash
forge build
```

### 🧪 Test
```bash
forge test
```

### 🎨 Format
```bash
forge fmt
```

### ⛽ Gas Snapshot
```bash
forge snapshot
```

---

## 🧪 Local Development

### Start local node:
```bash
anvil
```

---

## 🚀 Deploy Contract

### Deploy to Sepolia:

```bash
forge script script/DeployFundMe.s.sol   --rpc-url $SEPOLIA_RPC_URL   --private-key $PRIVATE_KEY   --broadcast   --verify   --etherscan-api-key $ETHERSCAN_API_KEY
```

---

## 🔍 Interact with Contract

Using **Cast**:

```bash
cast call <contract_address> "retrieve()" --rpc-url $SEPOLIA_RPC_URL
```

---

## 📁 Project Structure

```
├── src/            # Smart contracts
├── script/         # Deployment scripts
├── test/           # Test files
├── lib/            # Dependencies
├── broadcast/      # Deployment logs
```

---

## 🧠 Key Features

- Fund contract with ETH  
- Minimum USD threshold using Chainlink  
- Owner-only withdrawals  
- Gas optimized & tested with Foundry  

---

## 📌 Notes

- Always use **test wallets** for development  
- Never expose your private keys  
- Keep `.env` file out of version control  

---

## 🙌 Acknowledgements

- Chainlink  
- Foundry  
