# Level 2: Building the Contract

Welcome to Level 2 of your swapping contract development adventure! After grasping the fundamentals in Level 1, now you are ready to start building your contract. Let's begin!

## Objective

Your task is to build the `swap()` function that is the main ingredient of the contract. While doing so, you'll need to use some external resources like `swapExactTokensForTokens()` from Uniswap V2 Router (recall Level 1).

## Build the Contract

1. As you'll use Uniswap V2 Router, you need to define the contract address of it.
2. For non-WETH cases, you'll need to add an intermediary step into the swapping path, so you need to define WETH address too.
3. Build the function:
    a. Recall from the ERC20 mission that you need token approval.
    b. Define the swapping path.
    c. Specify the conditional for the case where no token is WETH.
    d. Call `swapExactTokensForTokens()`.
4. Define the needed interface for the router.
5. Define the needed interface for WETH.

## Deploy the Contract

Use the relevant Foundry command to deploy and verify your contract! If you don't remember; no worries, check [Foundry-Exercise](./Foundry-Exercise.md).