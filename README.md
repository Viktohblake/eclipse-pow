# eclipse-pow
A Simple Guide to Collecting Bitz on Eclipse

# What is $BITZ?

- It is the first ePOW commodity token that anyone can mine on Eclipse
- 5m max supply
- Not related to $ES
- NOT pre-mined + ZERO team/insider allocations
- You can mine it using Solana CLI or wait for the web app miner UI

# Prerequisites
Make sure you have a Eclipse wallet set up and funded with ETH on Eclipse
Have a computer with terminal access

# Setup Steps
Note: For Windows OS you must first download WSL (https://ubuntu.com/desktop/wsl)

### 1. Install Rust:
    curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh

**Note: When prompted chooose option 1 and then run this:**
    
    source $HOME/.cargo/env

### 2. Install Solana CLI:
     curl --proto '=https' --tlsv1.2 -sSfL https://solana-install.solana.workers.dev | bash
     
**Note: After successful inststall, add Solana to your PATH (the installer will provide instructions for this) or optionally restart your termial.**

### 3. Create a local keypair/Wallet
    solana-keygen new

**This will create a new keypair and store it in the default location (~/.config/solana/id.json).**
**Take note of your public key and phrase (displayed after generation).**

### 4. Set the rpc to Eclipse mainnet:
    solana config set --url https://bitz-000.eclipserpc.xyz/

### 5. Fund your wallet (the newly created public key address) with a minimum of 0.0005eth

**You can view your address by running:**   

    solana address

**You can view your balance by running:**   

    solana balance

### 6. Install Bitz using Cargo:
    cargo install bitz
    
**Note: If you run into an error like _command not found_ during bitz installation try running the below:**
    source $HOME/.cargo/env
    
    export PATH="$HOME/.cargo/bin:$PATH"

### 7. RUN BITZ
    bitz collect

**You should see something like this:**
<img width="568" alt="Screenshot 2025-04-12 at 13 47 24" src="https://github.com/user-attachments/assets/62b518ff-cbc0-427d-b108-14b254e00f48" />


## Other useful commands
### To maximize your bitz collection, add more cores:
    bitz collect --cores 8
### Claim your bitz: 
    bitz claim
### Check your balance:
    bitz account
### Look up all commands:
    bitz --help

# THANK YOU 🤩
# ECLIPSE EVERYTHING 
