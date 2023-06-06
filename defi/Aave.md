# AAVE

### Chainlink Multisig

[All Aave implementations utilize Chainlink as their only source of truth.](https://docs.aave.com/developers/core-contracts/aaveoracle#aaveoracle) There is no double-checking of the data received from Chainlink, and there is no backup plan in case of a Chainlink failure. 

All Chainlink price feed oracles are owned by a 4-of-9 multisig. The signers are unknown. Therefore, all Aave deposits that are utilized as loan collateral are subject to the security and integrity of the unknown signers to this multisig.

### Aave Multisigs on L2 Implementations

Most of Aave’s L2 implentations are owned by multisigs. This is not readily apparent to users without a [deep dive into Aave’s docs](https://docs.aave.com/developers/deployed-contracts/v3-mainnet).

Aave includes the following text 👇 in their docs regarding its L2 multisigs (Arbitrum shown as an example), however there is no way to verify whether or not Aave team holds keys to the multisig.

<kbd>
<img width="773" src="https://github.com/chrisblec/cipher/assets/17037450/b878ec9c-ab7b-4774-a9b1-ec51b59fce77">
</kbd>

For more detail, visit https://blec.report/aave/.
