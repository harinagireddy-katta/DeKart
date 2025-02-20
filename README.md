# **Decentralized Marketplace with Smart Contract Escrow System**  

## **Overview**  
Traditional e-commerce platforms face issues such as:
- Lack of transparency in transactions.
- Centralized control over listings, payments, and fees.
- Fraudulent activities, including disputes over payments and product authenticity.  

Our project solves these problems by building a **decentralized e-commerce marketplace** that ensures **trustless and transparent transactions using blockchain and smart contracts**.

---

## **Key Features**  
✅ **Decentralized Trustless Transactions**: Removes intermediaries, enabling direct buyer-seller interaction.  
✅ **Escrow Protection**: Payments are held securely until both parties confirm transaction completion.  
✅ **Real-Time Bidding**: A fair auction system for competitive product pricing.  
✅ **Blockchain Transparency**: Immutable records ensure fraud prevention.  
✅ **Secure Smart Contracts**: Automates transactions and dispute resolution.  

---

## **Technology Stack**
| Layer       | Technology Used |
|-------------|----------------|
| **Frontend** | React.js, Vite, MetaMask Integration |
| **Backend**  | Node.js, Express.js, MongoDB |
| **Blockchain** | Solidity (Smart Contracts), Ethers.js |
| **Network** | Sepolia Testnet (Ethereum) |

---

## **Project Architecture**  

### **1. User Flow**
1. **User Authentication & Wallet Connection**:  
   - Users sign in and connect their MetaMask wallet.  

2. **Product Listing**:  
   - Sellers add products via the smart contract.  
   - Products are listed on the blockchain with unique IDs.  

3. **Bidding & Purchase**:  
   - Buyers place bids or purchase directly using ETH and DeK tokens.  
   - Funds are locked in an **escrow smart contract** for security.  

4. **Transaction Completion**:  
   - Payment is **released** once the buyer confirms product receipt.  
   - In case of **dispute**, funds remain locked until resolved.  

---

## **Smart Contracts**
### **1. `DeKToken.sol`**  
- Implements an **ERC-20** token.  
- Used for transactions, cashback rewards, and premium access.  

### **2. `Marketplace.sol`**  
- **Manages product listings**, bidding, and purchases.  
- **Interacts with Escrow.sol** to secure payments.  

### **3. `Escrow.sol`**  
- Holds **ETH and DeK tokens** in escrow.  
- Prevents fraud by ensuring funds are only released upon buyer confirmation.  

---

## **How to Run the Project**  

### **1. Clone the Repository**  
```sh
git clone https://github.com/yourusername/decentralized-marketplace.git
cd decentralized-marketplace
```

### **2. Install Dependencies**  
```sh
npm install
```

### **3. Compile & Deploy Smart Contracts**  
```sh
npx hardhat compile
npx hardhat run scripts/deploy.js --network sepolia
```

### **4. Run the Frontend**
```sh
npm run dev
```

---

## **Smart Contract Interactions**
### **1. Adding a Product**
```js
await marketplace.addProduct("Laptop", "Electronics", ethers.parseEther("2"));
```

### **2. Buyer Purchases Product**
```js
await marketplace.connect(buyer).buyProduct(1, ethers.parseEther("5"), { value: ethers.parseEther("0.5") });
```

### **3. Seller Confirms & Withdraws Funds**
```js
await escrow.releaseFunds();
```

---

## **Impact of the Project**  
### **On Users**  
- **Buyers**: Secure payments, fraud prevention, and transparent transactions.  
- **Sellers**: Direct access to customers without high platform fees.  

### **On Society**  
- Encourages **decentralization in e-commerce**.  
- Promotes **trustless transactions**, reducing reliance on centralized entities.  

### **On the Market**  
- Disrupts traditional platforms by **eliminating intermediaries**.  
- Provides a **cost-effective** and **secure** alternative to centralized marketplaces.  

---

## **Future Enhancements**
🚀 **Decentralized Dispute Resolution**  
🚀 **Cross-Chain Payment Support**  
🚀 **Integration of NFTs for Product Ownership**  
🚀 **AI-based Reputation System for Buyers & Sellers**  

---
