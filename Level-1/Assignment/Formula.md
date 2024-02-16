# Constant Product Formula

The constant product formula is used to calculate how much token B will be received by a user who sends $a$ amount of token A:

$$ a \cdot b = k $$

Here;
- $a$ denotes the amount of token A,
- $b$ denotes the amount of token B, and
- $k$ is a constant (always).

## How does it work?

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