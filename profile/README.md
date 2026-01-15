# Malgist

**AI-Driven, Non-Custodial DeFi Portfolio Management on Mantle Network.**

![Dashboard Screenshot](path/to/screenshot.png)

## Project Overview

Malgist is an intelligence layer designed to abstract the complexity of DeFi yield farming. It functions as a non-custodial decision support system that helps users construct, monitor, and optimize cross-protocol portfolios based on their specific risk profiles.

Unlike automated vaults that pool funds, Malgist keeps the user in control. The AI suggests strategies and rebalancing actions, but all transactions are executed directly from the user's wallet to the blockchain.

## The Problem

* **Fragmentation:** Liquidity is scattered across lending, staking, and LP protocols, making portfolio tracking difficult.
* **Cognitive Load:** Optimizing yield requires constant monitoring of APY fluctuations, LTV ratios, and market risks.
* **Manual Inefficiency:** Users often miss rebalancing opportunities due to the time and complexity required to analyze multiple protocols manually.

## Core Features

* **Intent-Based Strategy:** Users define high-level goals (e.g., "Stable Yield," "Aggressive Growth"). The AI engine maps these intents to specific protocol allocations.
* **Non-Custodial Architecture:** Malgist never holds user funds. The platform acts solely as an interface and calculation engine; the user retains full custody of their private keys.
* **Unified Dashboard:** Aggregates positions from multiple protocols (Lending, Staking, DEXs) into a single performance view.
* **Smart Rebalancing:** Continuous monitoring of on-chain data to detect suboptimal positions and suggest corrective transactions.

## Architecture & Repositories

Malgist follows a modular architecture distributed across the following repositories:

* **[malgist-app](https://github.com/malgist/malgist-app)** (Current): The primary interface and DApp logic (Next.js, Wagmi).
* **[malgist-backend](https://github.com/malgist/malgist-backend)**: The off-chain computation engine and AI integration.
* **[malgist-contract](https://github.com/malgist/malgist-contract)**: Solidity smart contracts deployed on Mantle Network.

## Tech Stack

* **Frontend:** Next.js, TypeScript, Tailwind CSS
* **Web3 Integration:** Wagmi, RainbowKit, Viem
* **Backend/AI:** Python/Node.js (for off-chain logic and LLM orchestration)
* **Blockchain:** Mantle Network

## Getting Started

### Prerequisites
* Node.js (v18 or higher)
* Yarn or npm

### Installation

1.  Clone the repository:
    ```bash
    git clone [https://github.com/malgist/malgist-app.git](https://github.com/malgist/malgist-app.git)
    cd malgist-app
    ```

2.  Install dependencies:
    ```bash
    npm install
    ```

3.  Configure environment variables:
    Rename `.env.example` to `.env.local` and populate the required keys:
    ```bash
    NEXT_PUBLIC_WALLET_CONNECT_ID=your_id_here
    NEXT_PUBLIC_API_URL=your_backend_url
    ```

4.  Run the development server:
    ```bash
    npm run dev
    ```

## Hackathon Scope

This MVP was developed for the **[Insert Hackathon Name]**.
* **Implemented:** Core dashboard UI, Wallet connection, AI strategy generation flow, and Mantle network integration.
* **In Progress:** Real-time on-chain data indexing and automated execution pipelines.

## License

Distributed under the MIT License.
