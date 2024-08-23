## Nodes

Node is a term from graph theory or distributed systems; it is a single participant in a network. The nodes communicate with each other according to the protocol and in a [peer-to-peer](https://en.wikipedia.org/wiki/Peer-to-peer) manner forming the whole blockchain network. Different kinds of nodes serve different purpose, for example:

- **Validator nodes** secure the network by proposing new blocks and voting on the validity of new blocks
- **RPC (Remote Procedure Call) nodes** do not participate in voting, they query the network and post new transactions

## Validator clients

TODO

## Protocol

Protocol is a common set of rules network nodes must follow. It defines things like

- communication between P2P (peer-to-peer) nodes,
- transaction format for network participants,
- any special features,
- and everything else for the network to operate correctly and for the users to know how to transact over the network.

An essential part of a good protocol for a decentralized blockchain network is the proper incentive setup; this creates the need for its native coin.

## Coin

Coins are used to motivate participation in the network. They are usually awarded to miners or validators with every new block for their role in securing the network and validating transactions. Without the proper incentives, any decentralized blockchain network falls apart.

!!! info

    The Solana blockchain's native currency is **SOL**. Within Solana, the smallest unit is called a **lamport**, where **1 SOL** equals **1,000,000,000 lamports**.
