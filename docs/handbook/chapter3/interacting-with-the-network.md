## RPC Nodes

Any user who chooses to interact with the network must communicate with one of the network’s nodes through a Remote Procedure Call (RPC) endpoint. The available [RPC methods](https://solana.com/docs/rpc) are listed in the Solana documentation.

The methods vary from simple queries, such as retrieving specific account information, or checking the state of the network, to sending transactions that modify state of the blockchain.

!!! example

    _Request of the **getBlockHeight** method:_

    ```bash
    curl http://localhost:8899 -X POST -H "Content-Type: application/json" -d '{"jsonrpc":"2.0","id":1,"method":"getBlockHeight"}'
    ```

    _Response of the **getBlockHeight** method:_

    ```json
    { "jsonrpc": "2.0", "result": 0, "id": 1 }
    ```

!!! important

    The ability to send transactions is crucial because is the only way we can alter data on the blockchain. All write operations, including account creation or transfer of tokens are done through transactions.

!!! info

    While users can interact with the blockchain through RPCs, it is not required. There are several libraries that provide convenient interfaces for languages such as JavaScript, Rust and Python.
