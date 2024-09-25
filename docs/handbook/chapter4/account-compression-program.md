## Merkle Tree

A merkle tree is a data structure that organizes data into a tree-like form.

- Each **leaf node** inside this tree represents a hash of some data.
- Each **non-leaf node** represents a hash of its child nodes.

The root is a compact representation of all data stored in the tree. Merkle trees allows us to easily verify integrity of the data without having to store all of it on-chain.

!!! info

    The account compression program uses a special type of merkle tree called [concurrent merkle tree](https://spl.solana.com/account-compression/concepts).

??? note "Tree Terminology"

    - **Leaf node** is a node that does not have any children in the tree.
    - **Root node** is the top-most node of a tree, which does not have a parent.

## Account Compression Program

Minting a single NFT may be relatively inexpensive, however, the cost of storing the asset's data on-chain can quickly become uneconomical as the quantity increases. The **Account Compression Program** is an on-chain system designed to address the rising concern of storage costs on Solana. The solution lies in storing a compressed hash of the asset data on-chain, while the actual data is stored off-chain in a database.
