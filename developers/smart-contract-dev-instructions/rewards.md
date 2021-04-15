---
description: This guide describes the BonFi DeFi Offering Rewards Distribution Process
---

# Rewards

## Before you begin

**Prerequisite**: 

In order to issue and distribute rewards, a reward allowance needs to be added to the staking pool\(s\). 

## **Rewards methodology**

Rewards need to be manually added to the smart contracts using the `addReward`function.

Once the allowance is added to the staking pool\(s\) from the token contract, pass the reward amount as `parameter(uint256)` to the `addReward` function. All staking pools have `totalReward` and `rewardBalance` read functions. These read functions show the total Rewards added to the smart contract to date and the current balance of rewards the smart contract holds.

Also, users can check the `stakedTotal` and `stakedBalance` read functions. These functions show the total tokens staked in the pool to date and the smart contract's current staked balance. These functions determine the required reward tokens for each staking pool.

Anyone can add rewards to the staking pools. However, this process is managed by the BonFi DAO Council.

### **Reward Calculation:**

Rewards are calculated at the time of user withdrawal. This calculation will take care of all the effective interest rate changes during the user active lock period and calculate the reward accordingly. The calculation will discard any changes in the effective interest rate during the passive lock period \(User lock duration expired but hasn’t un-staked\).

