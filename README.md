# Create-a-node-for-Aztec-Network
How to run a node for Aztec Network
# How to Run a Node for Aztec Network

This repository provides a comprehensive guide to setting up and running a node (sequencer or full node) for the [Aztec Network](https://aztec.network/), a privacy-focused Layer 2 solution on Ethereum. By running a node, you can contribute to the network, earn roles like "Apprentice" on Aztec's Discord, and learn about zero-knowledge rollups.

⚠️ **Disclaimer**: This is an educational guide created by a community member. It is not affiliated with Aztec Network. Always do your own research and follow official documentation.

## Table of Contents
- [Prerequisites](#prerequisites)
- [Hardware Requirements](#hardware-requirements)
- [Setup Instructions](#setup-instructions)
  - [Option 1: Manual Setup](#option-1-manual-setup)
  - [Option 2: Automated Script](#option-2-automated-script)
- [Running the Node](#running-the-node)
- [Registering as a Validator](#registering-as-a-validator)
- [Troubleshooting](#troubleshooting)
- [Resources](#resources)
- [License](#license)

## Prerequisites
- **Operating System**: Ubuntu 20.04+ (or WSL2 on Windows).
- **Docker**: Install Docker and Docker Compose.
- **Ethereum Wallet**: An EVM wallet with a private key and public address (funded with Sepolia ETH for testnet).
- **RPC URLs**: Access to Sepolia testnet RPC and Beacon RPC URLs (e.g., via Infura, Alchemy, or your own Geth/Prysm nodes).
- **Network**: Stable internet with at least 25 Mbps up/down.
- **VPS (Optional)**: A VPS (e.g., Contabo, DigitalOcean) for 24/7 operation.

Install Docker and dependencies:
```bash
sudo apt update
sudo apt install curl iptables build-essential git wget lz4 jq make gcc nano automake autoconf tmux htop nvme-cli libgbm1 pkg-config libssl-dev libleveldb-dev tar clang bsdmainutils ncdu unzip libleveldb-dev -y
sudo curl -L "https://github.com/docker/compose/releases/latest/download/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
