# Liquity

### Oracle Risk

Liquity is an immutable protocol which cannot be modified or stopped by its creators. However, embedded in that immutable code is a call to Chainlink’s ETH/USD price feed. This price feed is ***not*** immutable and can be tampered with by a 4-of-9 multisig controlled by Chainlink.

Liquity’s immutable code does include a “sanity check” that would be automatically utilized if Chainlink’s price feed stopped updating or sent very flawed data. In that case, the smart contract would look to the Tellor ETH/USD oracle for price data.

Outside of this oracle risk, funds deposited into a Liquity CDP cannot be tampered with by anyone other than the owner of the depositing wallet, outside of protocol-driven liquidations and redemptions.
