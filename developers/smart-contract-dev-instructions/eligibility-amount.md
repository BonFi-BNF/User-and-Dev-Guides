---
description: This guide describes the BNF Staking Pool Eligibility Amount
---

# Eligibility Amount

## **Smart contract e**ligibility amount

**Steps to set eligibility amount in Rookie and Professional Staking Pools:**

Eligibility amount checks the user's eligibility status for the Professional User Tier.

1. Smart contract function ‘setEligibilityAmount’ needs to be invoked to set the new Eligibility amount for the Professional User Tier.

```text
“function setEligibilityAmount(uint256 amount_) public onlyOwner{}”
```

2. setEligibilityAmount function takes one uint256 input variable.

Case 1: New Eligibility Amount – 5000 tokens

‘5000000000000000000000’ needs to be passed as input to the function.

* Once the user has staked an amount greater than the eligibility amount, the eligibility status from this pool will be ‘true’, and after withdrawal, the status will change to ‘false’.



