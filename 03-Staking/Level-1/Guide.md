# Guide

Let's get you equipped! This guide will go over setting up your development environment, what staking is, how it works.

## Foundry

Starting point is setting up a new Foundry project to deploy our contract to Scroll Sepolia Testnet and verify it.

If you need help regarding with Foundry, please see: [Foundry-Exercise](./Foundry-Exercise.md).

## Staking

Staking is to lock some cryptocurrency tokens to earn reward. We will deep dive into reward part of the mission, but let's go step-by-step.

### `stake()`

`stake()` function, taking the staking amount as the input, is used to deposit some ERC20 tokens to earn reward. But you need to be careful about a few things:
- staking amount has to be greater than zero,
- function has to be reentrancy-resistant.

`stake()` function transfers the denoted amount of ERC20 tokens to the contract and emits an event called `Staked()`.

### `withdraw()`

`withdraw()` function, taking the withdrawal amount as the input, is used to withdraw previously staked ERC20 tokens.

`withdraw()` function transfers the denoted amount of staked ERC20 tokens to the user that call the function and emits an event called `Withdrawn()`.

## Solidity

1. Interfaces
2. Variables
3. Functions
4. Events

## Further Reading

1. [What is Crypto Staking?](https://www.britannica.com/money/what-is-crypto-staking/)
2. [Crypto Staking 101](https://www.coindesk.com/learn/crypto-staking-101-what-is-staking/)