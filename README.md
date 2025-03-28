# ZKPig Node Setup Guide

This guide will help you set up a ZKPig node to contribute to the zkEVM network either on Sepolia or Mainnet.

---

## Prerequisites

- A Linux-based VPS with at least:
  - 2 CPU cores
  - 4 GB RAM
  - 30+ GB Disk
- `curl`, `wget`, and basic terminal usage

---

## 1. Download the Binary

```bash
wget https://github.com/kkrt-labs/zk-pig/releases/download/v0.4.0/zkpig-linux-amd64
chmod +x zkpig-linux-amd64
mv zkpig-linux-amd64 /usr/local/bin/zkpig
```

---

## 2. Run on Sepolia Testnet

```bash
zkpig run \
  --chain-id 11155111 \
  --chain-rpc-url https://ethereum-sepolia-rpc.publicnode.com
```

🛠 If this RPC doesn't work, try one from Alchemy or Blast with archive node support.

---

## 3. Run on Ethereum Mainnet

```bash
zkpig run \
  --chain-id 1 \
  --chain-rpc-url https://eth-mainnet.g.alchemy.com/v2/YOUR_KEY
```

---

## 4. Optional: Run as a service

You can set up `zkpig` as a systemd service for auto-restart and background operation.

---

## Notes

- The tool listens on ports 8080 and 8081
- Prover input generation is filtered to every 5th block by default (`--filter-modulo`)

---

## Contribution

Feel free to open issues, PRs, or suggest improvements for automating this setup or supporting more environments.
