# Guide to Level-1

Let's get you equipped. This guide will go over setting up your development environment, constant product formula, and initializing the contract.

## Foundry

Starting point is setting up a new Foundry project to deploy our contract to Scroll Sepolia Testnet and verify it.

If you need help regarding with Foundry, please see: [Foundry-Exercise](./Foundry-Exercise.md).

## Constant Product Formula

The constant product formula is used to calculate how much token B will be received by a user who sends $a$ amount of token A:

$$ a \cdot b = k $$

Here;
- $a$ denotes the amount of token A,
- $b$ denotes the amount of token B, and
- $k$ is a constant (always).

### How does it work?

Let's say Alice wants to swap her 1 ETH to DAI.

1. Alice goes to ETH/DAI pool.
- For the sake of simplicity, let us assume there are 10 ETH and 25,000 DAI in the pool. Therefore
$$k = (10) \times (25,000) = (250,000)$$.

2. Alice sends her 1 ETH to the pool.
- Now, the pool has 11 ETH and 25,000 DAI.
- The pool sends such amount of DAI to Alice that $k$ remains constant.
$$(11) \times (25,000 - amountDAI) = 250,000$$
$$amountDAI = 2,272.73$$.

3. Alice receives 2,272.73 DAI for 1 ETH she had.
- Now the pool has 11 ETH and 22,727.27 DAI.
- If you multiply these two numbers, you get the same $k=250,000$.

## The Essence of the `swapExactTokensForTokens()`

```solidity
function swapExactTokensForTokens(
  uint amountIn,
  uint amountOutMin,
  address[] calldata path,
  address to,
  uint deadline
) external returns (uint[] memory amounts) {

}
```

Swaps an exact amount of input tokens for as many output tokens as possible, along the route determined by the path. The first element of path is the input token, the last is the output token, and any intermediate elements represent intermediate pairs to trade through (if, for example, a direct pair does not exist).

## Solidity

The syntax you will need for this assignment is limited to:
1. Variables
2. Functions

## Further Reading

1. [A Comprehensive Deep Dive to AMMs](https://medium.com/@arbnom/navigating-the-defi-landscape-a-comprehensive-deep-dive-to-amms-954020ec23b)