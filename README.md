# 🏦 TrustChain

A decentralized protocol that aggregates **on-chain user behavior** — including transaction history, staking habits, and DeFi interactions — into a **transparent and trustable crypto credit score**.  
The system is designed to **encourage accountability** and **enable fairer financial decisions** in the decentralized ecosystem.

---

## 🚀 Overview

Traditional credit scoring is **opaque, centralized, and prone to privacy risks**.  
This protocol uses **on-chain verifiable data** to create a **trustless credit scoring system** without exposing sensitive personal data.

**Key Features:**
- Transparent **on-chain smart contracts** for score calculation.
- **ZK (Zero-Knowledge) circuits** for privacy-preserving verification.
- Decentralized **data indexer** to gather activity across chains.
- Flexible scoring logic — governance can update weight factors.
- Can be integrated into **DeFi lending platforms**, DAOs, and decentralized identity systems.

---

## 📌 Use Case

**Example:**  
- Alice wants to borrow 500 USDC from a DeFi lending platform.  
- Instead of KYC or centralized credit checks, the platform queries Alice’s **on-chain credit score** from this protocol.  
- The score is computed based on her:
  - Wallet transaction volume & frequency
  - Staking & liquidity provision history
  - Loan repayment history in DeFi
- Alice has a high score → gets a lower interest rate.  
- Bob has low or no score → gets smaller borrow limits or higher interest.

---

## 🏗 Architecture

                 ┌────────────────────────────┐
                 │      User Wallet(s)         │
                 └──────────────┬──────────────┘
                                │
           ┌────────────────────┴────────────────────┐
           │           Indexer (The Graph)           │
           │  - Aggregates DeFi transactions         │
           │  - Normalizes staking & loan data       │
           └────────────────────┬────────────────────┘
                                │
           ┌────────────────────┴────────────────────┐
           │      Scoring Engine (Python)             │
           │  - Applies scoring formula               │
           │  - Generates proof (ZK circuit)          │
           └────────────────────┬────────────────────┘
                                │
           ┌────────────────────┴────────────────────┐
           │     Smart Contracts (Solidity)           │
           │  - Store scores & proofs                 │
           │  - Allow dApps to query securely         │
           └────────────────────┬────────────────────┘
                                │
                 ┌──────────────┴──────────────┐
                 │      DeFi Applications      │
                 │  - Lending platforms        │
                 │  - Governance DAOs          │
                 │  - Decentralized ID (DID)   │
                 └─────────────────────────────┘


---

## 🛠 Tech Stack

### **Smart Contracts**
- **Solidity** (Hardhat framework)
- **OpenZeppelin** libraries (Ownable, AccessControl, ERC20/721)
- **Ethers.js** for interactions

### **Indexing**
- **The Graph** for data aggregation
- Subgraph mappings in TypeScript

### **Scoring Engine**
- **Python** for score computation
- **Pandas / NumPy** for data handling
- **PyCryptography** for hashing & verification

### **ZK Circuits**
- **Circom** or **Halo2** for proof generation
- **SnarkJS** for proof verification

### **Frontend** (Integration-ready)
- React / Next.js (Optional dApp UI)
- TailwindCSS for styling

---





