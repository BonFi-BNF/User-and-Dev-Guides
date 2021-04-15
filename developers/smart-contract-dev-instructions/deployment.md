---
description: This guide delineates BNF token staking pool deployment details
---

# Deployment

## **Smart contracts**

While deploying the BNF token staking pools, the following constructor elements need to be passed.

<table>
  <thead>
    <tr>
      <th style="text-align:left"><b>Arguments</b>
      </th>
      <th style="text-align:left"><b>Type</b>
      </th>
      <th style="text-align:left"><b>DESCRIPTION</b>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><b>name_</b>
      </td>
      <td style="text-align:left">String</td>
      <td style="text-align:left">Name of the smart contract.</td>
    </tr>
    <tr>
      <td style="text-align:left"><b>tokenAddress_</b>
      </td>
      <td style="text-align:left">Address</td>
      <td style="text-align:left">Smart contract address of the BNF/UNI-v2 token.</td>
    </tr>
    <tr>
      <td style="text-align:left"><b>rewardTokenAddress_*</b>
      </td>
      <td style="text-align:left">Address</td>
      <td style="text-align:left">
        <p>Smart contract address of the</p>
        <p>reward token(BNF).</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b>rate_</b>
      </td>
      <td style="text-align:left">Uint</td>
      <td style="text-align:left">The effective interest rate of the staking pool is multiplied by 100.</td>
    </tr>
    <tr>
      <td style="text-align:left"><b>lockduration_</b>
      </td>
      <td style="text-align:left">Uint</td>
      <td style="text-align:left">The lock period in days.</td>
    </tr>
  </tbody>
</table>

\* - ‘_RewardTokenAddress\__’ is only applicable in the case of the Liquidity Staking pool, where the UNI-v2 token\(tokenAddress\_\) is staked into the contract and the rewards are paid out in BNF\(rewardTokenAddress\_\).

