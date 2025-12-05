# MyToken (MTK)

## Overview
MyToken is a simple ERC-20 compatible token built on the Ethereum blockchain for learning and demonstration purposes.  
This project teaches the fundamentals of smart contracts, token standards, and blockchain interactions using Remix IDE.

## Token Details
- **Name:** MyToken  
- **Symbol:** MTK  
- **Decimals:** 18  
- **Total Supply:** 1,000,000 MTK (1,000,000 × 10¹⁸ units)

## Features
- ✔ Full ERC-20 standard implementation  
- ✔ Transfer tokens between accounts  
- ✔ Approve other accounts to spend tokens  
- ✔ Transfer tokens on behalf of another user  
- ✔ Transparent event logging (Transfer & Approval)  
- ✔ Balance and allowance tracking  
- ✔ Safe input validation (zero-address protection, balance checks)

## Smart Contract Functions

### ### 1. Public State Variables
- `name` – Token name  
- `symbol` – Token ticker  
- `decimals` – Number of decimal places  
- `totalSupply` – Total supply of tokens  

### 2. Core ERC-20 Functions
| Function | Description |
|---------|-------------|
| `balanceOf(address)` | Returns the balance of a given address |
| `transfer(to, value)` | Transfer tokens from caller to another address |
| `approve(spender, value)` | Allow a spender to use your tokens |
| `allowance(owner, spender)` | Check remaining approved amount |
| `transferFrom(from, to, value)` | Transfer tokens using approved allowance |

### 3. Events
| Event | Trigger |
|-------|---------|
| `Transfer(from, to, value)` | Emitted on transfers |
| `Approval(owner, spender, value)` | Emitted when approval is set |

### 4. Optional Helper Functions
- `getTotalSupply()` – Returns the total supply  
- `getTokenInfo()` – Returns name, symbol, decimals, and total supply  

---

## Deployment Instructions (Remix IDE)

1. Open https://remix.ethereum.org  
2. Create file: **MyToken.sol**  
3. Compile using Solidity **0.8.x**  
4. Go to **Deploy & Run Transactions**  
5. Select **Remix VM (Prague)** environment  
6. In constructor input, enter initial supply:  
1000000000000000000000000
7. Click **Deploy**  
8. Interact with the deployed contract

---

## Testing Steps Performed

### ✔ Basic Checks
- name → MyToken  
- symbol → MTK  
- decimals → 18  
- totalSupply → 1,000,000 × 10¹⁸  
- balanceOf(owner) returns full supply  

### ✔ Transfer Testing
- Sent 1 token successfully between accounts  
- Balances updated correctly  
- Transfer event emitted  

### ✔ Approve & transferFrom
- Approve(Account A → Account B, 5 tokens)  
- transferFrom(Account A → Account C, 5 tokens) successful  
- Allowance decreased to 0  

### ✔ Edge Case Failures (correct behavior)
- Transfer to zero address → reverted  
- Transfer more than balance → reverted  
- transferFrom without approval → reverted  

---

## Conclusion
This project demonstrates a working ERC-20 token that follows the Ethereum token standard.  
It is fully functional, safe, and suitable as a beginner blockchain portfolio project.

---

## Author
**Pavani Sri**  
Blockchain Beginner • Smart Contract Developer (in progress)

s
