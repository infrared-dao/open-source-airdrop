# Infrared Airdrop Methodology
Open sourcing the airdrop data and scripts so anyone can verify our reward program for testnet loyalty

We analyzed bartio testnet activity of our nearly 400k users from the start of the network on June 5th up to the end of November.

The eligibility critera were designed to reward the most engaged users and counteract obvious sybil wallets trying to farm the airdrop.

We created 5 different roles based on different types of activity, each worth 1-3 points, for a maximum possible 10 points per user.


## Roles and Points
- **"Power User"**
    - Made at least 15 txs (stake, unstake, or reward claim) through any Infrared Vaults
    - Worth 1 point
    - 17,452 users held this role
- **"BGT Delegator"**
    - Delegated at least 15 BGT to the Infrared Validator (and had at least 3 txs on Infrared Vaults)
    - Worth 1 point 
    - 12,797 users held this role
- **"iBGT Lover"**
    - Held at least 1 iBGT in wallet, staked at least 1 iBGT to the Infrared iBGT Vault (and made at least 3 reward claims from the iBGT Infrared Vault)
    - Worth 2 points
    - 3,178 users held this role
- **"iBGT Enjoyoor"**
    - Held at least 2 iBGT in wallet, used at least 2 iBGT with any bArtio partner protocols (and made at least 2 reward claims from the iBGT Infrared Vault)
    - Worth 3 points
    - 2,655 users held this role
- **"Infrared is Key"**
    - Held the “Infrared is Key” Role on Discord
    - Worth 3 points 
    - 130 users held this role


## Point Distribution

A user who was able to hold all roles would get a total of 10 points.  Most users ended up with 0 points.

| Total Points    |    Num Users |
| :-------------- | -----------: |
| 1 point         | 21,404 users |
| 2 points        | 2,231 users  |
| 3 points        | 1,102 users  |
| 4 points        | 469 users    |
| 5 points        | 242 users    |
| 6 points        | 1,059 users  |
| 7 points        | 843 users    |
| 8 points        | 2 users      |
| 9 points        | 9 users      |
| 10 points       | 35 users     |

These points were then squared and normalized by the sum across all users to get a final relative weight.

The specific addresses with their roles and final weights can be found in the /data/roles_points_weights.csv file.


## Summary Stats

For context, here are some high level stats about certain activities:

- Nearly 400,000 unique wallets interacted with vaults, iBGT, or the validator
- 135,158 users made at least one tx with any Infrared Vault
- 56,573 users held any amount of iBGT and staked to the iBGT vault
- 31,566 users delegated any amount of native BGT to the validator and made at least one vault claim


## Open Sourcing the Code

The golang scripts used to pull the raw chain activity and several python scripts used to summarize and score it will be added to this public repo shortly.

Our goal is that anyone should be able to run and verify the same analysis we performed here and get the same results for testnet.

Thank you for taking part in the testnet and join Infrared on the main net where the profits are real!
