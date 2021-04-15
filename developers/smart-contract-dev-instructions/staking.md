---
description: This guide describes the staking process in BonFi Staking Pools
---

# Staking

## Before you begin

**Prerequisite**: 

To complete the staking process, users need to complete 2 transactions: 

1. Spend limit approval
2. Staking pool token deposit/lock

## **Staking methodology**

Currently, the BonFi platform offers the following staking pools: 

* Rookie
* Professional
* Legendary
* Liquidity 
* NULS/BNF Credit Mining

Users have no limitations in the number of tokens they can stake; however, not all pools are accessible freely. The BonFi platform uses a tier system that requires users to join the Professional Tier before unlocking full platform features. By default, all users are in the Rookie Tier with limited platform access. To join the Professional Tier, a user must stake a **minimum of 2500 BNF** in the Rookie or Professional Staking Tier.

**Professional Tier user unlocks the following platform features:** 

* Full access to the BonFi platform, incl. the BonVest and all DeFi offerings
* Access to the Legendary staking pool

**In order to complete the staking process successfully, users are required to complete 2 steps/smart contract interactions:**

1. Spend limit approval for any of the available staking pools
2. Thereafter, users can call the `Stake`function and approve the amount to be staked using `stake(uint256)` in the staking pool 

After the staking is successful, users can view their staking details using the`userDeposits`function with their wallet address. This function returns the user staked amount, user staked time, and the status of withdrawal.

Users can stake only once in any of the available staking pools, using the same wallet address. Users need to wait until the staking contract's maturity date before withdrawing to stake more tokens. After a successful withdrawal, the user can deposit tokens again in the same staking pool.

