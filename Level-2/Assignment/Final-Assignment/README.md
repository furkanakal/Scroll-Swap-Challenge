# Level 2: What is `swapExactTokensForTokens()` from Uniswap V2 Router?

Welcome to Level 2 of your swapping contract development adventure! After getting the fundamentals of our swap contract in Level-1, now we will explore a function from Uniswap V2 Router contract. Let's begin!

## Objective

Your task is to understand the `swapExactTokensForTokens()` from Uniswap V2 Router to use it in your basic swap contract.

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

## Final Thoughts

Remember, these levels are more than just a coding assignment. It's about understanding the fundamentals, being meticulous with your work, and taking pride in what you build. That's exactly why this extra level exists. It's crucial to cover the logical flow behind the code we write.
