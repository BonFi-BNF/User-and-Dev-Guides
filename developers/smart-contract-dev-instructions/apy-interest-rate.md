---
description: This guide specifies APY Rate Settings for DeFi Offerings
---

# APY Rate

## APY rate m**ethodology**

**Steps to set the interest rate according to the APY changes in smart contracts \(Owner\).**

1. Smart contract function ‘setRate’ needs to be invoked to set the interest rate, which can be done only by the contract owner. 

```text
function setRate(uint256 rate_) public onlyOwner{}
```

_2. setRate_ function takes one _uint64_ variable input, and this is the new interest rate to be used multiplied by 100.

### Interest rate calculator:

Case 1: New APY: 8%

For 1 month lock period: \(8/12\) = 0.67 \* 100 = 67

‘67’ needs to be passed as input to the _setRate_ function for the contract with a 1 month lock period.

Case 2: New APY: 12%

For 3-month lock period: \(12/12\) \* 3 = 3 \*100 = 300

‘300’ needs to be passed as input to the _setRate_ function for the contract with a 3-month lock period.

Case 3: New APY: 45%

For 60 day lock period: \(45/365\) \* 60 = 7.39 \* 100 = 739

‘739’ needs to be passed as input to the _setRate_ function for the contract with a 60 day lock period.

1. Once the staking pool's interest rate is adjusted, the new interest rate can be viewed using the ‘index’ and the ‘rates’ function.
2. _Index_ – the current change in the effective interest rate of the pool.
3. _Rates_ – the read function that returns the effective interest rate and the timestamp it was added to the pool \(takes index as input\).
4. When the user stakes in the current pool, the pool's current index will be linked with the staking function, which is used for the reward calculation.

