# Building a Basic Swap Contract

Welcome to Level n of your Smart Contract Development adventure! With a solid grasp of Solidity syntax under your belt, it's now time to put that knowledge into action. Your challenge is to craft an Ethereum lending, borrowing, and repayment contract. This is where theory meets practice, and where you start transforming lines of code into a functional blockchain application. Are you ready to embark on this exciting phase of your journey? Let's begin!

## Objective

Your task is to build a simple Ethereum swap contract. This contract will use Uniswap V2 Router functionality.

## The Essence of the Basic Swap Contract

The Basic Swap Contract is designed to facilitate the very first idea of automated market making (AMM).

**Swap**
- **Functionality:** The `swapExactTokensForTokens()` function from Uniswap V2 Router.
- **How It Works:** When a user calls this function to swap some tokens, the contract checks if one of two tokens to be swapped is WETH. If so, it executes the swap by obeying the constant product formula (If you are not familiar, please see [DeFi-Guide](../DeFi_Guide.md)) directly. If not, then it adds WETH into the path as an intermediary so that the swap is executed in two stages.

## Instructions

### Step 1: Set Up Your Environment
- **Prepare Your Workspace**: Create a New Folder called basic_swap
- **Initialize a New Project**: Start with a clean slate using `forge init`.

If you need help setting up your foundry project or you want to go over the commands of deploying, check out [Foundry-Exercise](./Foundry-Exercise.md)

### Step 2: Write the Contract
- **Uniswap V2 Router and WETH:** As discussed above, we need these two contracts.
- **Swap Function:** Implement a `swap()` function for users to call and execute the swap.
- **Interfaces:** Initialize the needed interfaces for Uniswap V2 Router and WETH.

Stuck? Check [Assignment-Hints](../Assignment-Hints/) for guidance.

Join our [telegram group](https://t.me/+vRIl8Wkm0B0zOTQx) for support.

### Step 3: Compile
- **Ensure Accuracy**: Compile your contract and resolve any errors.

### Step 4: Deploy and Interact
- **Deployment**: Deploy your contract to the Scroll Sepolia network.
- **Verification**: Verify your contract for transparency.
- **Interaction**: Test deposit, withdraw, borrow, and repay functions on Scrollscan.

## Final Thoughts

Remember, this is more than just a coding assignment. It's about understanding the fundamentals, being meticulous with your work, and taking pride in what you build. Each line of code is a step towards mastering smart contract development.

Once you've succesfully deployed your contract, pat yourself on the back. You've just completed Level 1, thats your first step in this journey to becoming smart contract developer.

But wait...how do you know you got it right?

Drop a [scrollscan](https://scrollscan.com/) link to your verified contract in the [telegram group](https://t.me/+vRIl8Wkm0B0zOTQx) and one of us will have a look. We'll reach out either congratulating you or advise.

Whether you got it right or not, the attempt is an achievement. 

Celebrate your journey however you want, by dropping a message in tg or [even tweeting about it](https://twitter.com/intent/tweet?text=I%Cleared%Level%1%Of%The%Level%Up%Challenge!)

Feel free to tag us!
