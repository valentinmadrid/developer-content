---
date: Jul 29, 2023
difficulty: intro
title: "Solana faucets to get SOL tokens for development"
description: "A list of the most common ways to get devnet and testnet SOL tokens for Solana development. Including: airdrop, web3.js, POW faucet, and more."
tags:
  - faucet
keywords:
  - faucet
  - blockchain
  - devnet
  - testnet
---

# Solana faucets to get SOL tokens for development

This is a collection of the different ways for developers to acquire SOL on
Solana's testing networks, the Solana devnet and testnet.

## 1. Solana Airdrop

_Available on Devnet and Testnet_

This is the base way of acquiring SOL, but it can be subject to rate limits when
there is a high number of airdrops.

Here are three different ways of requesting airdrops with it:

### Using the Solana CLI:

`solana airdrop 2`

### Using web3.js:

```js
const connection = new Connection("https://api.devnet.solana.com");
connection.requestAirdrop();
```
See more: [`requestAirdrop()`](https://solana-labs.github.io/solana-web3.js/classes/Connection.html#requestAirdrop) documentation inside web3.js.
## 2. Web Faucet

_Available for Devnet_

A web faucet hosted by Solana Foundation that has lower rate limits.

[faucet.solana.com](https://faucet.solana.com)

## 3. RPC Provider Faucets

_Available for Devnet_

RPC Providers can opt in to distributing Devnet SOL via their Devnet Validators.

_\*If you are an RPC Provider and want to distribute SOL please get in touch
here_

Currently Supported:

1. [Helius](https://www.helius.dev/)
2. [QuickNode](https://www.quicknode.com/chains/sol)

### Using the Solana CLI

Specify your [Cluster](https://docs.solana.com/clusters) to be your RPC provider's URL.

`solana config set --url <your RPC url>`

Then you can request an airdrop like you would in the first option in this
guide.

`solana airdrop 2`

### Using Web3.js

```js
const connection = new Connection("your RPC url");
connection.requestAirdrop();
```

## 4. Proof of work Faucet

_Available for Devnet_

This is a proof of work Faucet where Devnet SOL can be distributed to you thanks
to your computing power.

**Install the Devnet POW Crate:**

`cargo install devnet-pow`

**Start mining devnet SOL**

`devnet-pow mine`

_⚠️ The [POW Faucet](https://github.com/jarry-xiao/proof-of-work-faucet) is maintained by Ellipsis Labs_

## 5. Discord Faucet

The LamportDAO community has set up a Devnet Faucet Discord BOT.

You can join the LamportDAO Discord by clicking
[here](https://discord.gg/JBVrJgtFkq).

After that, head to a channel made for BOT commands and run send this message:

`/drop <address> <amount>`
