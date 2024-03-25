# Guide

Let's get you equipped! This guide will go over how staking reward works and what kind of new functions you will have.

## Rewarding

Your contract, at the end of the day, will receive some tokens to be staked and let some reward token be accumulated. Users will be able to claim their rewards whenever they want.

### New Variables

- Two ERC20 interfaces to represent:
    - staking token and
    - reward token.

- Reward rate to use in the formula.

- Two integers to represent:
    - last update time,
    - stored reward per token.

- Three mappings to represent:
    - paid reward token amount for each user,
    - reward amount for each user,
    - staking amount for each user.

- `constructor()`:
    - define the tokens that will be used for staking and rewards.

### Events

Two events called:
- `Staked()` and
- `Withdrawn()`.

These will be your logs to keep track of stakings and withdrawals.

### `rewardPerToken()`

This function will represent the formula that you will use to calculate how much reward will be accumulated over time.

> **Example:** s_rewardPerTokenStored + (((block.timestamp - s_lastUpdateTime) * REWARD_RATE * 1e18) / s_totalSupply)

### `earned()`

This function, taking a user address as the input, will be used to return the amount of reward the user has.

### `claimReward()`

This one will be used to transfer the rewards of a user to their address. You need to make sure that this function is reentrancy-resistant.

## Solidity

1. Interfaces
2. Variables
3. Mappings
4. Functions
5. Events
