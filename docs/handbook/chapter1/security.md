# Consensus

To agree on a certain state of a blockchain, network nodes need to reach a consensus. We assume there are malicious nodes in the network. Therefore, the system must be able to withstand not only simple node failures but also attacks to a certain extent. BFT ([Byzantine Fault Tolerant](https://en.wikipedia.org/wiki/Byzantine_fault)) is thus a desired property of such a distributed system.
Currently, only three viable consensus families can be used in practice. The first is the classic PBFT-like (Practical BFT) algorithm family. The second is a so-called Nakamoto consensus, which couples a Sybil protection mechanism of Proof-of-Work with the longest-chain rule, a novel consensus invented by Satoshi Nakamoto for Bitcoin in 2008. The third and newest family of consensus protocols known today is called Snow. Yet it is better known by its implementation name – Avalanche Consensus, introduced in 2018 and used for the Avalanche cryptocurrency.

# Sybil Resistance

To prevent a single entity from taking over the network, there must be a mechanism put in place so that no one can just spawn more nodes that can mine or vote (depending on the network) and thus subvert the network reputation system. These dishonest nodes would be able to out-vote honest nodes and start censoring transactions, approving invalid transactions, or changing the entire protocol.
Currently, the two most common Sybil resistance mechanisms are PoW (Proof-of-Work) and PoS (Proof-of-Stake). The former employs a model where miners in the network are given a chance to mine a block that is proportional to their hashing power in the network and is used in Bitcoin. The latter is a type of model for voting-based networks, where a validator is given the power of their vote proportionally to staked coins.

# Security

Consensus and Sybil resistance mechanism are often confused as the same thing, which is not true and is worth pointing out. One works in conjunction with the other. Let’s look at how this works in both PoW-based and PoS-based networks.
Consider what makes Bitcoin, a PoW-based network, theoretically secure – it is the fact that only the longest chain is respected, also commonly known as the longest chain rule. This is why the consensus is called, as mentioned before, the Nakamoto consensus.
For a PoS-based network, the Sybil resistance mechanism is usually associated with a variant of a PBFT-like algorithm or the novel Avalanche consensus.
