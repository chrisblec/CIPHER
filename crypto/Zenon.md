# Zenon Network

Zenon Network is a Layer 1 network based on a novel dual-ledger architecture and self-described as driven by the ethos and principles of Bitcoin.

The network was launched by its anonymous founders Professor Z and Mr Kaine via a BitcoinTalk forum post.
An initial placeholder network was used for liquidity and community building while the founders developed the alphanet release.

Shortly after the activation of Taproot on Bitcoin in Nov 2021, alphanet was released and the network migrated from the placeholder network.
In Mar 2022, the founding developers released Accelerator-Z, the protocol level grant program voted on by the network's validators called Pillars.
Since then, development of the network has been taken on by the wider Zenon community incentivized through Accelerator-Z.

The network currently incorporates both PoS and PoW, and is designed to incorporate more PoW in the future.
As with most networks that utilize PoS, various aspects of the network have started out more centralized than others.

## Pillar Election

While the founding developers have described a future consensus architecture utilizing PoW and transaction level virtual voting,
the current consensus mechanism confirms transaction by selecting Pillars via a pseudo-random virtual vote based on delegation weight.

Network participants can delegate their ZNN to a Pillar and receive rewards based on a free-market of Pillar reward sharing.

Every 5 minutes, 30 Pillars are assigned to create a Momentum each following a 10 second interval.
15 of the pillars are uniformly selected from the top 30 pillars by delegation weight.
The remaining 15 are uniformly selected from the unchosen top 30 pillars and the remaining pillars.
This means that currently more than half of the momentums created will be by the top 30 pillars by delegation.

## Sporks

Zenon Network upgrades are facilitated through a protocol level embedded contract for creating and activating "sporks".
A spork is an on-chain object that represents a change in the protocol. Upon creation, a spork is assigned a unique hash ID.
Developers of protocol clients can then use that ID in their implementations to check for spork activation on chain that will trigger changes in client behavior.
After enough network participants upgrade their clients, the spork can be activated on-chain to complete the upgrade with the new protocol changes.
The reference implementation of the protocol go-zenon automatically halts if a spork is activated that it is not configured for.

Currently sporks can only be created by an address controlled by the founding developers.
This means that effectively the founding devs or someone who has compromised the key could halt the network by creating and activating a spork that none of the Pillars have implemented.
Mr Kaine has stated the community will need to develop the functionality for network validators to vote on spork creation and activation.
It is currently under active development.
