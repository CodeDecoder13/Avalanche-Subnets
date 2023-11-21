# Avalanche-Subnets

# **ERC20 and Vault Contracts**

This repository contains two Solidity smart contracts: `ERC20` and `Vault`. Below, you'll find a brief description of each contract and its functionality.

## **ERC20 Contract**

### **Overview**
The `ERC20` contract is an implementation of the ERC-20 token standard. It represents a fungible token with the following properties:

- **Name**: Solidity by Example
- **Symbol**: SOLBYEX
- **Decimals**: 18
- **Total Supply**: Variable, initialized to 0

### **Functions**
1. **`transfer`**
   - Allows an account to transfer tokens to another account.
   
2. **`approve`**
   - Allows an account to approve another account to spend tokens on its behalf.

3. **`transferFrom`**
   - Allows an approved spender to transfer tokens from one account to another.

4. **`mint`**
   - Allows the contract owner to create new tokens and add them to their balance.

5. **`burn`**
   - Allows an account to burn (destroy) a specified number of their tokens.

### **Events**
- **`Transfer`**: Triggered when tokens are transferred between accounts.
- **`Approval`**: Triggered when an approval for token transfer is granted.

## **Vault Contract**

### **Overview**
The `Vault` contract acts as a vault for storing ERC-20 tokens securely. It implements a mechanism to deposit and withdraw tokens while minting and burning corresponding shares for users.

### **Constructor**
- **`constructor`**: Initializes the contract with the address of the ERC-20 token to be stored in the vault.

### **Functions**
1. **`deposit`**
   - Allows users to deposit ERC-20 tokens into the vault.
   - It calculates the number of shares to mint based on the user's deposit and existing shares.

2. **`withdraw`**
   - Allows users to withdraw ERC-20 tokens from the vault by burning shares.
   - It calculates the amount of tokens to be withdrawn based on the number of shares burned.

### **State Variables**
- **`token`**: Stores the address of the ERC-20 token that the vault holds.
- **`totalSupply`**: Tracks the total number of shares in the vault.
- **`balanceOf`**: A mapping that records the number of shares held by each user.
