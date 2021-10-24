# Ethereum Classic

Call                                                                                | Description
------------------------------------------------------------------------------------|----------------------------------------------------------------------------------
[etc_accounts](#etc_accounts)                                                       | Returns a list of addresses owned by the client.
[etc_blockNumber](#etc_blocknumber)                                                 | Returns the number of the most recent block.
[etc_call](#etc_call)                                                               | Executes a new message call immediately without creating a transaction on the block chain.
[etc_chainId](#etc_chainid)                                                         | Returns the EIP155 chain ID used for transaction signing at the current best block. Null is returned if not available.
[etc_estimateGas](#etc_estimategas)                                                 | Makes a call or transaction, which won’t be added to the blockchain and returns the used gas, which can be used for estimating the used gas.
[etc_gasPrice](#etc_gasprice)                                                       | Returns the current gas price in wei.
[etc_getBalance](#etc_getbalance)                                                   | Returns the balance of the account of given address.
[etc_getBlockByHash](#etc_getblockbyhash)                                           | Returns information about a block by hash.
[etc_getBlockByNumber](#etc_getblockbynumber)                                       | Returns information about a block by block number.
[etc_getBlockTransactionCountByHash](#etc_getblocktransactioncountbyhash)           | Returns the number of transactions in a block from a block matching the given block hash.
[etc_getBlockTransactionCountByNumber](#etc_getblocktransactioncountbynumber)       | Returns the number of transactions in a block from a block matching the given block number.
[etc_getCode](#etc_getcode)                                                         | Returns code at a given address.
[etc_getFilterChanges](#etc_getfilterchanges)                                       | Polling method for a filter, which returns an array of logs which occurred since last poll.
[etc_getFilterLogs](#etc_getfilterlogs)                                             | Returns an array of all logs matching filter with given id.
[etc_getLogs](#etc_getlogs)                                                         | Returns an array of all logs matching a given filter object.
[etc_getStorageAt](#etc_getstorageat)                                               | Returns the value from a storage position at a given address.
[etc_getTransactionByBlockHashAndIndex](#etc_gettransactionbyblockhashandindex)     | Returns information about a transaction by block hash and transaction index position.
[etc_getTransactionByBlockNumberAndIndex](#etc_gettransactionbyblocknumberandindex) | Returns information about a transaction by block number and transaction index position.
[etc_getTransactionByHash](#etc_gettransactionbyhash)                               | Returns the information about a transaction requested by transaction hash.
[etc_getTransactionCount](#etc_gettransactioncount)                                 | Returns the number of transactions sent from an address.
[etc_getTransactionReceipt](#etc_gettransactionreceipt)                             | Returns the receipt of a transaction by transaction hash.
[etc_getUncleByBlockHashAndIndex](#etc_getunclebyblockhashandindex)                 | Returns information about a uncle of a block by hash and uncle index position.
[etc_getUncleByBlockNumberAndIndex](#etc_getunclebyblocknumberandindex)             | Returns information about a uncle of a block by number and uncle index position.
[etc_getUncleCountByBlockHash](#etc_getunclecountbyblockhash)                       | Returns the number of uncles in a block from a block matching the given block hash.
[etc_getUncleCountByBlockNumber](#etc_getunclecountbyblocknumber)                   | Returns the number of uncles in a block from a block matching the given block number.
[etc_getWork](#etc_getwork)                                                         | Returns the hash of the current block, the seedHash, and the boundary condition to be met (“target”).
[etc_hashrate](#etc_hashrate)                                                       | Returns the number of hashes per second that the node is mining with.
[etc_mining](#etc_mining)                                                           | Returns `true` if client is actively mining new blocks.
[etc_newBlockFilter](#etc_newblockfilter)                                           | Creates a filter in the node, to notify when a new block arrives. To check if the state has changed, call [etc_getFilterChanges](#etc_getfilterchanges). 
[etc_newFilter](#etc_newfilter)                                                     | Creates a filter object, based on filter options, to notify when the state changes (logs). To check if the state has changed, call [etc_getFilterChanges](#etc_getfilterchanges).
[etc_newPendingTransactionFilter](#etc_newpendingtransactionfilter)                 | Creates a filter in the node, to notify when new pending transactions arrive. To check if the state has changed, call [etc_getFilterChanges](#etc_getfilterchanges).
[etc_protocolVersion](#etc_protocolversion)                                         | Returns the current ethereum protocol version.
[etc_sendRawTransaction](#etc_sendrawtransaction)                                   | Creates new message call transaction or a contract creation for signed transactions.
[etc_submitWork](#etc_submitwork)                                                   | Used for submitting a proof-of-work solution.
[etc_subscribe](#etc_subscribe)                                                     | Starts a subscription (on WebSockets / IPC / TCP transports) to a particular event. For every event that matches the subscription a JSON-RPC notification with event details and subscription ID will be sent to a client.
[etc_syncing](#etc_syncing)                                                         | Returns an object with data about the sync status or `false`.
[etc_uninstallFilter](#etc_uninstallfilter)                                         | Uninstalls a filter with given id. Should always be called when watch is no longer needed. Additonally Filters timeout when they aren’t requested with [etc_getFilterChanges](#etc_getfilterchanges) for a period of time.
[etc_unsubscribe](#etc_unsubscribe)                                                 | Unsubscribes from a subscription.
[etc_net_listening](#etc_net_listening)                                             | Returns `true` if client is actively listening for network connections.
[etc_net_peerCount](#etc_net_peercount)                                             | Returns number of peers currenly connected to the client.
[etc_net_version](#etc_net_version)                                                 | Returns the current network protocol version.
[etc_web3_clientVersion](#etc_web3_clientversion)                                   | Returns the current client version.
[etc_web3_sha3](#etc_web3_sha3)                                                     | Returns Keccak-256 (not the standardized SHA3-256) of the given data.





## etc_accounts

Returns a list of addresses owned by the client.

### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '[]' https://api.oracleminer.com/xrs/etc_accounts
```

```plaintext
blocknet-cli xrService etc_accounts
```
<code class="api-call">etc_accounts</code>

This call does not take parameters.


### Response

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
{
  "id": 1,
  "jsonrpc": "2.0",
  "reply": [
  ],
  "uuid": "0C47E765-69C9-48A4-83A8-6B4499F6F7B5"
}
```

```plaintext
{
  "jsonrpc": "2.0",
  "id": 1,
  "result": []
}
```

Parameter            | Type          | Description
---------------------|---------------|-------------
reply                | string        | List of addresses owned by the client.
jsonrpc              | string        | JSON RPC version.
id                   | int           | ID number.
uuid                 | string        | The response ID, which can be used to view this response again with [xrGetReply](https://api.blocknet.co/#xrgetreply).





## etc_blockNumber

Returns the number of the most recent block.


### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '[]' https://api.oracleminer.com/xrs/etc_blockNumber
```

```plaintext
blocknet-cli xrService etc_blockNumber
```
<code class="api-call">etc_blockNumber</code>

This call does not take parameters.


### Response

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
0xa1b6be
```

```plaintext
{
  "reply": "0xa1b6be",
  "uuid": "AB392D84-3789-45D5-BE0A-25371EB3B56C"
}
```

Parameter            | Type          | Description
---------------------|---------------|-------------
reply                | string        | Integer of the current block number the client is on.
jsonrpc              | string        | JSON RPC version.
id                   | int           | ID number.
uuid                 | string        | The response ID, which can be used to view this response again with [xrGetReply](https://api.blocknet.co/#xrgetreply).





## etc_call

> Sample Data

```cli
{
  "from": "0x407d73d8a49eeb85d32cf465507dd71d507100c1",
  "to": 0xa94f5374fce5edbc8e2a8697c15331677e6ebf0b",
  "gas": "0x76c0",
  "gasPrice": "0x9184e72a000",
  "value": "0x186a0",
  "data": "0xd46e8dd67c5d32be8d46e8dd67c5d32be8058bb8eb970870f072445675058bb8eb970870f072445675",
  "block_parameter": "latest"
}
```
Executes a new message call immediately without creating a transaction on the block chain.


### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '["0x407d73d8a49eeb85d32cf465507dd71d507100c1","0xa94f5374fce5edbc8e2a8697c15331677e6ebf0b","0x76c0","0x9184e72a000","0x186a0","0xd46e8dd67c5d32be8d46e8dd67c5d32be8058bb8eb970870f072445675058bb8eb970870f072445675","latest"]' https://api.oracleminer.com/xrs/etc_call
```

```plaintext
blocknet-cli xrService etc_call 0x407d73d8a49eeb85d32cf465507dd71d507100c1 0xa94f5374fce5edbc8e2a8697c15331677e6ebf0b 0x76c0 0x9184e72a000 0x186a0 0xd46e8dd67c5d32be8d46e8dd67c5d32be8058bb8eb970870f072445675058bb8eb970870f072445675 latest
```
<code class="api-call">etc_call [from] [to] [gas] [gasPrice] [value] [data] [block_parameter]</code>

Parameter       | Type       | Description
----------------|------------|-------------
from            | string     | The address the transaction is sent from.
to              | string     | The address the transaction is directed to.
gas             | string     | Integer of the gas provided for the transaction execution. etc_call consumes zero gas, but this parameter may be needed by some executions.
gasPrice        | string     | Integer of the gas price used for each paid gas.
value           | string     | Integer of the value sent with this transaction.
data            | string     | Hash of the method signature and encoded parameters.
block_parameter | string     | Integer block number, or the string 'latest', 'earliest' or 'pending'.


### Response Parameters

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
0x
```

```plaintext
{
    "reply" : "0x",
    "uuid" : "A59DE810-5A28-4B52-83BE-A697F231BC75"
}
```

Parameter            | Type          | Description
---------------------|---------------|-------------
reply                | string        | The return value of the executed contract.
jsonrpc              | string        | JSON RPC version.
id                   | int           | ID number.
uuid                 | string        | The response ID, which can be used to view this response again with [xrGetReply](https://api.blocknet.co/#xrgetreply).





## etc_chainId

Returns the EIP155 chain ID used for transaction signing at the current best block. `null` is returned if not available.

### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '[]' https://api.oracleminer.com/xrs/etc_chainId
```

```plaintext
blocknet-cli xrService etc_chainId
```
<code class="api-call">etc_chainId</code>

This call does not take parameters.


### Response

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
0x3d
```

```plaintext
{
    "reply" : "0x3d",
    "uuid" : "9DB1FFE3-8088-4B8D-BA7B-F4CB622C9E87"
}
```

Parameter            | Type          | Description
---------------------|---------------|-------------
reply                | string        | EIP 155 Chain ID, or `null`, if not available.
jsonrpc              | string        | JSON RPC version.
id                   | int           | ID number.
uuid                 | string        | The response ID, which can be used to view this response again with [xrGetReply](https://api.blocknet.co/#xrgetreply).





## etc_estimateGas

> Sample Data

```cli
{
  "from": "0x407d73d8a49eeb85d32cf465507dd71d507100c1",
  "to": 0xa94f5374fce5edbc8e2a8697c15331677e6ebf0b",
  "gas": "0x76c0",
  "gasPrice": "0x9184e72a000",
  "value": "0x186a0",
  "data": "0xd46e8dd67c5d32be8d46e8dd67c5d32be8058bb8eb970870f072445675058bb8eb970870f072445675"
}
```
Makes a call or transaction, which won’t be added to the blockchain and returns the used gas, which can be used for estimating the used gas.


### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '["0x407d73d8a49eeb85d32cf465507dd71d507100c1","0xa94f5374fce5edbc8e2a8697c15331677e6ebf0b","0x76c0","0x9184e72a000","0x186a0","0xd46e8dd67c5d32be8d46e8dd67c5d32be8058bb8eb970870f072445675058bb8eb970870f072445675"]' https://api.oracleminer.com/xrs/etc_estimateGas
```

```plaintext
blocknet-cli xrService etc_estimateGas 0x407d73d8a49eeb85d32cf465507dd71d507100c1 0xa94f5374fce5edbc8e2a8697c15331677e6ebf0b 0x76c0 0x9184e72a000 0x186a0 0xd46e8dd67c5d32be8d46e8dd67c5d32be8058bb8eb970870f072445675058bb8eb970870f072445675
```
<code class="api-call">etc_estimateGas [from] [to] [gas] [gasPrice] [value] [data]</code>

Parameter       | Type       | Description
----------------|------------|-------------
from            | string     | The address the transaction is sent from.
to              | string     | The address the transaction is directed to.
gas             | string     | Integer of the gas provided for the transaction execution. etc_call consumes zero gas, but this parameter may be needed by some executions.
gasPrice        | string     | Integer of the gas price used for each paid gas.
value           | string     | Integer of the value sent with this transaction.
data            | string     | Hash of the method signature and encoded parameters.


### Response Parameters

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
0x5cec
```

```plaintext
{
    "reply" : "0x5cec",
    "uuid" : "55EFC78E-1DA0-49B6-A50F-152BDB8B1972"
}
```

Parameter            | Type          | Description
---------------------|---------------|-------------
reply                | string        | The amount of gas used.
jsonrpc              | string        | JSON RPC version.
id                   | int           | ID number.
uuid                 | string        | The response ID, which can be used to view this response again with [xrGetReply](https://api.blocknet.co/#xrgetreply).





## etc_gasPrice

Returns the current price per gas in wei.

### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '[]' https://api.oracleminer.com/xrs/etc_gasPrice
```

```plaintext
blocknet-cli xrService etc_gasPrice
```
<code class="api-call">etc_gasPrice</code>

This call does not take parameters.


### Response

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
0x7d2b7500
```

```plaintext
{
  "reply": "0x7d2b7500",
  "uuid": "50787091-3412-427B-A57F-B52A8CA139B3"
}
```

Parameter            | Type          | Description
---------------------|---------------|-------------
reply                | string        | Integer of the current gas price in wei.
jsonrpc              | string        | JSON RPC version.
id                   | int           | ID number.
uuid                 | string        | The response ID, which can be used to view this response again with [xrGetReply](https://api.blocknet.co/#xrgetreply).





## etc_getBalance

> Sample Data

```cli
{
  "address": "0x407d73d8a49eeb85d32cf465507dd71d507100c1",
  "block_parameter": "latest"
}
```
Returns the balance of the account of given address.


### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '["0x407d73d8a49eeb85d32cf465507dd71d507100c1","latest"]' https://api.oracleminer.com/xrs/etc_getBalance
```

```plaintext
blocknet-cli xrService etc_getBalance 0x407d73d8a49eeb85d32cf465507dd71d507100c1 latest
```
<code class="api-call">etc_getBalance [address] [block_parameter]</code>

Parameter       | Type       | Description
----------------|------------|-------------
address         | string     | The address to check for balance.
block_parameter | string     | Integer block number, or the string 'latest', 'earliest' or 'pending'.


### Response Parameters

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
0x0
```

```plaintext
{
  "reply": "0x0",
  "uuid": "7A8F4A63-1F09-4C1C-92C8-856F60434F17"
}
```

Parameter            | Type          | Description
---------------------|---------------|-------------
reply                | string        | Integer of the current balance in wei.
jsonrpc              | string        | JSON RPC version.
id                   | int           | ID number.
uuid                 | string        | The response ID, which can be used to view this response again with [xrGetReply](https://api.blocknet.co/#xrgetreply).





## etc_getBlockByHash

> Sample Data

```cli
{
  "block_hash": "0xfa533223775214de507f353a9521efb0efbc320896dcdf916f59b3ee21fa95e5",
  "show_tx_details: "false"
}
```
Returns information about a block by hash.


### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '["0xfa533223775214de507f353a9521efb0efbc320896dcdf916f59b3ee21fa95e5","false"]' https://api.oracleminer.com/xrs/etc_getBlockByHash
```

```plaintext
blocknet-cli xrService etc_getBlockByHash 0xfa533223775214de507f353a9521efb0efbc320896dcdf916f59b3ee21fa95e5 false
```
<code class="api-call">etc_getBlockByHash [block_hash] [show_tx_details]</code>

Parameter       | Type       | Description
----------------|------------|-------------
block_hash      | string     | Hash of a block.
show_tx_details | boolean    | If `true` it returns the full transaction objects, if `false` only the hashes of the transactions.


### Response Parameters

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
{
  "difficulty": "0x55df223d798c",
  "extraData": "0x457468436c6173736963534f4c4f2f326d696e6572735f4555",
  "gasLimit": "0x7a1200",
  "gasUsed": "0x288d4",
  "hash": "0xfa533223775214de507f353a9521efb0efbc320896dcdf916f59b3ee21fa95e5",
  "logsBloom": "0x00000000040000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000020000000000000000000000000000000000000000000000000000000000000000000000000000000",
  "miner": "0x004730417cd2b1d19f6be2679906ded4fa8a64e2",
  "mixHash": "0x339524959536643c1f72f4f1140a69c3ca057a9a4c55f21c89a5d3d4beb922be",
  "nonce": "0x020e440024a7d767",
  "number": "0xa1b6ed",
  "parentHash": "0x3103ab603f123e95bcde94d17b0977e9c45ccab9d266e96ba09d86e12a23973a",
  "receiptsRoot": "0x9e97821961dd9ffb5f37bae8b20722babc7e69faca2aa4e226b35f345ed11089",
  "sha3Uncles": "0x0825350393455e7b9a875393c748204649ea5633c5190e3535d2d6256464705f",
  "size": "0x77d",
  "stateRoot": "0xf1732f44ff21fc80ad0d816aa09ceab64c8d4c7bee3d8e160b3f1930912f956f",
  "timestamp": "0x5ee78d43",
  "totalDifficulty": "0x353b446579379d05d0",
  "transactions": [
    "0xed95cb266bf6a49821c660f98a5a127325f0dab40b4b80bf46b9ce453e9aa76f",
    "0xc9878f273f95f4c0496a4dfc3e29585ef9781c12283a32f3c0374112e62520bf",
    "0x921b69941d359911eca0afd24a075c19addf4b169071da15126170dfa44b72a9",
    "0x246ec280d94a14b4778a58b2888257f7e0d794834dddbe2abc843ba5c91fbdc6",
    "0x440fca453bc0379fb949d197974af89a0921ab0a3a0213a4a0c91a4d213c2ff6"
  ],
  "transactionsRoot": "0x95652b78325fb1ca88764ed29728a942b0b7229c3c198991694742bdfc0de7ce",
  "uncles": [
    "0xb4dfa97579cef4d5aac862e49095bb01d06bf43e3fd5ade9c37a0fd83c9c4e9c"
  ]
}
```

```plaintext
{
  "reply": {
    "difficulty": "0x55df223d798c",
    "extraData": "0x457468436c6173736963534f4c4f2f326d696e6572735f4555",
    "gasLimit": "0x7a1200",
    "gasUsed": "0x288d4",
    "hash": "0xfa533223775214de507f353a9521efb0efbc320896dcdf916f59b3ee21fa95e5",
    "logsBloom": "0x00000000040000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000020000000000000000000000000000000000000000000000000000000000000000000000000000000",
    "miner": "0x004730417cd2b1d19f6be2679906ded4fa8a64e2",
    "mixHash": "0x339524959536643c1f72f4f1140a69c3ca057a9a4c55f21c89a5d3d4beb922be",
    "nonce": "0x020e440024a7d767",
    "number": "0xa1b6ed",
    "parentHash": "0x3103ab603f123e95bcde94d17b0977e9c45ccab9d266e96ba09d86e12a23973a",
    "receiptsRoot": "0x9e97821961dd9ffb5f37bae8b20722babc7e69faca2aa4e226b35f345ed11089",
    "sha3Uncles": "0x0825350393455e7b9a875393c748204649ea5633c5190e3535d2d6256464705f",
    "size": "0x77d",
    "stateRoot": "0xf1732f44ff21fc80ad0d816aa09ceab64c8d4c7bee3d8e160b3f1930912f956f",
    "timestamp": "0x5ee78d43",
    "totalDifficulty": "0x353b446579379d05d0",
    "transactions": [
      "0xed95cb266bf6a49821c660f98a5a127325f0dab40b4b80bf46b9ce453e9aa76f",
      "0xc9878f273f95f4c0496a4dfc3e29585ef9781c12283a32f3c0374112e62520bf",
      "0x921b69941d359911eca0afd24a075c19addf4b169071da15126170dfa44b72a9",
      "0x246ec280d94a14b4778a58b2888257f7e0d794834dddbe2abc843ba5c91fbdc6",
      "0x440fca453bc0379fb949d197974af89a0921ab0a3a0213a4a0c91a4d213c2ff6"
    ],
    "transactionsRoot": "0x95652b78325fb1ca88764ed29728a942b0b7229c3c198991694742bdfc0de7ce",
    "uncles": [
      "0xb4dfa97579cef4d5aac862e49095bb01d06bf43e3fd5ade9c37a0fd83c9c4e9c"
    ]
  },
  "uuid": "721F5D58-B792-4A86-85F0-1AD272C7E661"
}
```

Parameter            | Type          | Description
---------------------|---------------|-------------
author               | string        | The address of the author of the block.
difficulty           | string        | Integer of the difficulty for this block.
extraData            | string        | The ‘extra data’ field of this block.
gasLimit             | string        | The maximum gas allowed in this block.
gasUsed              | string        | The total used gas by all transactions in this block.
hash                 | string        | Hash of the block. `null` when its pending block.
logsBloom            | string        | The bloom filter for the logs of the block. `null` when its pending block.
miner                | string        | Alias of ‘author’.
mixHash              | string        | The mix hash.
nonce                | string        | Hash of the generated proof-of-work. `null` when its pending block. Missing in case of PoA.
number               | string        | The block number. `null` when its pending block.
parentHash           | string        | Hash of the parent block.
receiptsRoot         | string        | The root of the receipts trie of the block.
sealFields           | Array         | Array of seal fields.
sha3Uncles           | string        | SHA3 of the uncles data in the block.
size                 | string        | Integer the size of this block in bytes. 
stateRoot            | string        | The root of the final state trie of the block.
timestamp            | string        | The unix timestamp for when the block was collated.
totalDifficulty      | string        | Integer of the total difficulty of the chain until this block.
transactions         | Array         | Array of transaction objects, or 32 Bytes transaction hashes depending on the last given parameter.
transactionsRoot     | string        | The root of the transaction trie of the block.
uncles               | Array         | Array of uncle hashes.
jsonrpc              | string        | JSON RPC version.
id                   | int           | ID number.
uuid                 | string        | The response ID, which can be used to view this response again with [xrGetReply](https://api.blocknet.co/#xrgetreply).





## etc_getBlockByNumber

> Sample Data

```cli
{
  "block_parameter": "0xa1b6ed",
  "show_tx_details: "false"
}
```
Returns information about a block by block number.


### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '["0xa1b6ed","false"]' https://api.oracleminer.com/xrs/etc_getBlockByNumber
```

```plaintext
blocknet-cli xrService etc_getBlockByNumber 0xa1b6ed false
```
<code class="api-call">etc_getBlockByNumber [block_parameter] [show_tx_details]</code>

Parameter       | Type       | Description
----------------|------------|-------------
block_parameter | string     | Integer block number, or the string 'latest', 'earliest' or 'pending'.
show_tx_details | boolean    | If `true` it returns the full transaction objects, if `false` only the hashes of the transactions.


### Response Parameters

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
{
  "difficulty": "0x55df223d798c",
  "extraData": "0x457468436c6173736963534f4c4f2f326d696e6572735f4555",
  "gasLimit": "0x7a1200",
  "gasUsed": "0x288d4",
  "hash": "0xfa533223775214de507f353a9521efb0efbc320896dcdf916f59b3ee21fa95e5",
  "logsBloom": "0x00000000040000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000020000000000000000000000000000000000000000000000000000000000000000000000000000000",
  "miner": "0x004730417cd2b1d19f6be2679906ded4fa8a64e2",
  "mixHash": "0x339524959536643c1f72f4f1140a69c3ca057a9a4c55f21c89a5d3d4beb922be",
  "nonce": "0x020e440024a7d767",
  "number": "0xa1b6ed",
  "parentHash": "0x3103ab603f123e95bcde94d17b0977e9c45ccab9d266e96ba09d86e12a23973a",
  "receiptsRoot": "0x9e97821961dd9ffb5f37bae8b20722babc7e69faca2aa4e226b35f345ed11089",
  "sha3Uncles": "0x0825350393455e7b9a875393c748204649ea5633c5190e3535d2d6256464705f",
  "size": "0x77d",
  "stateRoot": "0xf1732f44ff21fc80ad0d816aa09ceab64c8d4c7bee3d8e160b3f1930912f956f",
  "timestamp": "0x5ee78d43",
  "totalDifficulty": "0x353b446579379d05d0",
  "transactions": [
    "0xed95cb266bf6a49821c660f98a5a127325f0dab40b4b80bf46b9ce453e9aa76f",
    "0xc9878f273f95f4c0496a4dfc3e29585ef9781c12283a32f3c0374112e62520bf",
    "0x921b69941d359911eca0afd24a075c19addf4b169071da15126170dfa44b72a9",
    "0x246ec280d94a14b4778a58b2888257f7e0d794834dddbe2abc843ba5c91fbdc6",
    "0x440fca453bc0379fb949d197974af89a0921ab0a3a0213a4a0c91a4d213c2ff6"
  ],
  "transactionsRoot": "0x95652b78325fb1ca88764ed29728a942b0b7229c3c198991694742bdfc0de7ce",
  "uncles": [
    "0xb4dfa97579cef4d5aac862e49095bb01d06bf43e3fd5ade9c37a0fd83c9c4e9c"
  ]
}
```

```plaintext
{
  "reply": {
    "difficulty": "0x55df223d798c",
    "extraData": "0x457468436c6173736963534f4c4f2f326d696e6572735f4555",
    "gasLimit": "0x7a1200",
    "gasUsed": "0x288d4",
    "hash": "0xfa533223775214de507f353a9521efb0efbc320896dcdf916f59b3ee21fa95e5",
    "logsBloom": "0x00000000040000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000020000000000000000000000000000000000000000000000000000000000000000000000000000000",
    "miner": "0x004730417cd2b1d19f6be2679906ded4fa8a64e2",
    "mixHash": "0x339524959536643c1f72f4f1140a69c3ca057a9a4c55f21c89a5d3d4beb922be",
    "nonce": "0x020e440024a7d767",
    "number": "0xa1b6ed",
    "parentHash": "0x3103ab603f123e95bcde94d17b0977e9c45ccab9d266e96ba09d86e12a23973a",
    "receiptsRoot": "0x9e97821961dd9ffb5f37bae8b20722babc7e69faca2aa4e226b35f345ed11089",
    "sha3Uncles": "0x0825350393455e7b9a875393c748204649ea5633c5190e3535d2d6256464705f",
    "size": "0x77d",
    "stateRoot": "0xf1732f44ff21fc80ad0d816aa09ceab64c8d4c7bee3d8e160b3f1930912f956f",
    "timestamp": "0x5ee78d43",
    "totalDifficulty": "0x353b446579379d05d0",
    "transactions": [
      "0xed95cb266bf6a49821c660f98a5a127325f0dab40b4b80bf46b9ce453e9aa76f",
      "0xc9878f273f95f4c0496a4dfc3e29585ef9781c12283a32f3c0374112e62520bf",
      "0x921b69941d359911eca0afd24a075c19addf4b169071da15126170dfa44b72a9",
      "0x246ec280d94a14b4778a58b2888257f7e0d794834dddbe2abc843ba5c91fbdc6",
      "0x440fca453bc0379fb949d197974af89a0921ab0a3a0213a4a0c91a4d213c2ff6"
    ],
    "transactionsRoot": "0x95652b78325fb1ca88764ed29728a942b0b7229c3c198991694742bdfc0de7ce",
    "uncles": [
      "0xb4dfa97579cef4d5aac862e49095bb01d06bf43e3fd5ade9c37a0fd83c9c4e9c"
    ]
  },
  "uuid": "EAF6B252-D72F-495F-85CC-FCFD9816B39E"
}
```

Parameter            | Type          | Description
---------------------|---------------|-------------
author               | string        | The address of the author of the block.
difficulty           | string        | Integer of the difficulty for this block.
extraData            | string        | The ‘extra data’ field of this block.
gasLimit             | string        | The maximum gas allowed in this block.
gasUsed              | string        | The total used gas by all transactions in this block.
hash                 | string        | Hash of the block. `null` when its pending block.
logsBloom            | string        | The bloom filter for the logs of the block. `null` when its pending block.
miner                | string        | Alias of ‘author’.
mixHash              | string        | The mix hash.
nonce                | string        | Hash of the generated proof-of-work. `null` when its pending block. Missing in case of PoA.
number               | string        | The block number. `null` when its pending block.
parentHash           | string        | Hash of the parent block.
receiptsRoot         | string        | The root of the receipts trie of the block.
sealFields           | Array         | Array of seal fields.
sha3Uncles           | string        | SHA3 of the uncles data in the block.
size                 | string        | Integer the size of this block in bytes. 
stateRoot            | string        | The root of the final state trie of the block.
timestamp            | string        | The unix timestamp for when the block was collated.
totalDifficulty      | string        | Integer of the total difficulty of the chain until this block.
transactions         | Array         | Array of transaction objects, or 32 Bytes transaction hashes depending on the last given parameter.
transactionsRoot     | string        | The root of the transaction trie of the block.
uncles               | Array         | Array of uncle hashes.
jsonrpc              | string        | JSON RPC version.
id                   | int           | ID number.
uuid                 | string        | The response ID, which can be used to view this response again with [xrGetReply](https://api.blocknet.co/#xrgetreply).





## etc_getBlockTransactionCountByHash

> Sample Data

```cli
{
  "block_hash": "0xfa533223775214de507f353a9521efb0efbc320896dcdf916f59b3ee21fa95e5"
}
```
Returns the number of transactions in a block from a block matching the given block hash.


### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '["0xfa533223775214de507f353a9521efb0efbc320896dcdf916f59b3ee21fa95e5"]' https://api.oracleminer.com/xrs/etc_getBlockTransactionCountByHash
```

```plaintext
blocknet-cli xrService etc_getBlockTransactionCountByHash 0xfa533223775214de507f353a9521efb0efbc320896dcdf916f59b3ee21fa95e5
```
<code class="api-call">etc_getBlockTransactionCountByHash [block_hash]</code>

Parameter       | Type       | Description
----------------|------------|-------------
block_hash      | string     | Hash of a block.


### Response Parameters

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
0x5
```

```plaintext
{
  "reply": "0x5",
  "uuid": "2B32BCD6-1232-4B29-9AB8-A161A6A8F6D8"
}
```

Parameter            | Type          | Description
---------------------|---------------|-------------
reply                | string        | Integer of the number of transactions in this block.
jsonrpc              | string        | JSON RPC version.
id                   | int           | ID number.
uuid                 | string        | The response ID, which can be used to view this response again with [xrGetReply](https://api.blocknet.co/#xrgetreply).





## etc_getBlockTransactionCountByNumber

> Sample Data

```cli
{
  "block_parameter": "latest"
}
```
Returns the number of transactions in the block with the given block number.


### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '["latest"]' https://api.oracleminer.com/xrs/etc_getBlockTransactionCountByNumber
```

```plaintext
blocknet-cli xrService etc_getBlockTransactionCountByNumber latest
```
<code class="api-call">etc_getBlockTransactionCountByNumber [block_parameter]</code>

Parameter       | Type       | Description
----------------|------------|-------------
block_parameter | string     | Integer block number, or the string 'latest', 'earliest' or 'pending'.


### Response Parameters

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
0x0
```

```plaintext
{
  "reply": "0x0",
  "uuid": "E08A539D-FA98-4A98-963E-6AC0D76960DD"
}
```

Parameter            | Type          | Description
---------------------|---------------|-------------
reply                | string        | Integer of the number of transactions in this block.
jsonrpc              | string        | JSON RPC version.
id                   | int           | ID number.
uuid                 | string        | The response ID, which can be used to view this response again with [xrGetReply](https://api.blocknet.co/#xrgetreply).





## etc_getCode

> Sample Data

```cli
{
  "address": "0xa94f5374fce5edbc8e2a8697c15331677e6ebf0b",
  "block_parameter": "latest"
}
```
Returns code at a given address.


### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '["0xa94f5374fce5edbc8e2a8697c15331677e6ebf0b","latest"]' https://api.oracleminer.com/xrs/etc_getCode
```

```plaintext
blocknet-cli xrService etc_getCode 0xa94f5374fce5edbc8e2a8697c15331677e6ebf0b latest
```
<code class="api-call">etc_getCode [address] [block_parameter]</code>

Parameter       | Type       | Description
----------------|------------|-------------
address         | string     | Address.
block_parameter | string     | Integer block number, or the string 'latest', 'earliest' or 'pending'.


### Response Parameters

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
0x
```

```plaintext
{
  "reply": "0x",
  "uuid": "C9220DA9-5D7D-4CDB-8D8D-FD73EEABF572"
}
```

Parameter            | Type          | Description
---------------------|---------------|-------------
reply                | string        | The code from the given address.
jsonrpc              | string        | JSON RPC version.
id                   | int           | ID number.
uuid                 | string        | The response ID, which can be used to view this response again with [xrGetReply](https://api.blocknet.co/#xrgetreply).





## etc_getFilterChanges

> Sample Data

```cli
{
  "filter_id": "0x3cc4e57bf1fe5c0476b4a7092abfd52"
}
```
Polling method for a filter, which returns an array of logs which occurred since last poll.


### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '["0x3cc4e57bf1fe5c0476b4a7092abfd52"]' https://api.oracleminer.com/xrs/etc_getFilterChanges
```

```plaintext
blocknet-cli xrService etc_getFilterChanges 0x3cc4e57bf1fe5c0476b4a7092abfd52
```
<code class="api-call">etc_getFilterChanges [filter_id]</code>

Parameter       | Type       | Description
----------------|------------|-------------
filter_id       | string     | Filter id.


### Response Parameters

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
[
  "0x271c6b55462ded4eb79cddff750cb2417bba286712718d9323d604a54a16abf5"
]
```

```plaintext
{
  "reply": [
    "0x271c6b55462ded4eb79cddff750cb2417bba286712718d9323d604a54a16abf5"
  ],
  "uuid": "2C6DC8D0-A4DF-4207-8A99-A8238075FBB6"
}
```

Parameter            | Type          | Description
---------------------|---------------|-------------
reply                | Array         | Array of log objects, or an empty array if nothing has changed since last poll.
- logIndex           | string        | Integer of the log index position in the block. `null` when its pending.
- blockNumber        | string        | The block number. `null` when its pending.
- blockHash          | string        | Hash of the block where this log was in. `null` when its pending.
- transactionHash    | string        | Hash of the transactions this log was created fom. `null` when its pending.
- transactionIndex   | string        | Integer of the transactions index position log was created from. `null` when its pending.
- address            | string        | Address from which this log originated.
- data               | string        | Contains the non-indexed arguments of the log.
- topics             | Array         | Array of indexed log arguments.
jsonrpc              | string        | JSON RPC version.
id                   | int           | ID number.
uuid                 | string        | The response ID, which can be used to view this response again with [xrGetReply](https://api.blocknet.co/#xrgetreply).





## etc_getFilterLogs

> Sample Data

```cli
{
  "filter_id": "0x7d67f3962be4cf2197806f4520245f6e"
}
```
Returns an array of all logs matching filter with given id.


### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '["0x7d67f3962be4cf2197806f4520245f6e"]' https://api.oracleminer.com/xrs/etc_getFilterLogs
```

```plaintext
blocknet-cli xrService etc_getFilterLogs 0x7d67f3962be4cf2197806f4520245f6e
```
<code class="api-call">etc_getFilterLogs [filter_id]</code>

Parameter       | Type       | Description
----------------|------------|-------------
filter_id       | string     | Filter id.


### Response Parameters

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
{
  [
    {
      "logIndex": "0x1",
      "blockNumber": "0x1b4",
      "blockHash": "0x8216c5785ac562ff41e2dcfdf5785ac562ff41e2dcfdf829c5a142f1fccd7d",
      "transactionHash": "0xdf829c5a142f1fccd7d8216c5785ac562ff41e2dcfdf5785ac562ff41e2dcf",
      "transactionIndex": "0x0",
      "address": "0x16c5785ac562ff41e2dcfdf829c5a142f1fccd7d",
      "data": "0x0000000000000000000000000000000000000000000000000000000000000000",
      "topics": ["0x59ebeb90bc63057b6515673c3ecf9438e5058bca0f92585014eced636878c9a5"]
    },
    ...
  ]
}
```

```plaintext
{
    "reply" : [
    {
      "logIndex": "0x1",
      "blockNumber": "0x1b4",
      "blockHash": "0x8216c5785ac562ff41e2dcfdf5785ac562ff41e2dcfdf829c5a142f1fccd7d",
      "transactionHash": "0xdf829c5a142f1fccd7d8216c5785ac562ff41e2dcfdf5785ac562ff41e2dcf",
      "transactionIndex": "0x0",
      "address": "0x16c5785ac562ff41e2dcfdf829c5a142f1fccd7d",
      "data": "0x0000000000000000000000000000000000000000000000000000000000000000",
      "topics": ["0x59ebeb90bc63057b6515673c3ecf9438e5058bca0f92585014eced636878c9a5"]
    },
    ...
  ]
    "uuid" : "B38785C9-3949-4E4A-BFAE-052CAE333D3A"
}
```

Parameter            | Type          | Description
---------------------|---------------|-------------
reply                | Array         | Array of log objects, or an empty array if nothing has changed since last poll.
- logIndex           | string        | Integer of the log index position in the block. `null` when its pending.
- blockNumber        | string        | The block number. `null` when its pending.
- blockHash          | string        | Hash of the block where this log was in. `null` when its pending.
- transactionHash    | string        | Hash of the transactions this log was created fom. `null` when its pending.
- transactionIndex   | string        | Integer of the transactions index position log was created from. `null` when its pending.
- address            | string        | Address from which this log originated.
- data               | string        | Contains the non-indexed arguments of the log.
- topics             | Array         | Array of indexed log arguments.
jsonrpc              | string        | JSON RPC version.
id                   | int           | ID number.
uuid                 | string        | The response ID, which can be used to view this response again with [xrGetReply](https://api.blocknet.co/#xrgetreply).





## etc_getLogs

Returns an array of all logs matching a given filter object. **(Work in progress)**

### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '["a","1"]' https://api.oracleminer.com/xrs/etc_getLogs
```

```plaintext
blocknet-cli xrService etc_getLogs a 1
```
<code class="api-call">etc_getLogs [a] [1]</code>

Parameter       | Type       | Description
----------------|------------|-------------
a               | string     | abc
1               | string     | abc


### Response Parameters

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell

```

```plaintext

```

Parameter            | Type          | Description
---------------------|---------------|-------------
reply                |               | 
jsonrpc              | string        | JSON RPC version.
id                   | int           | ID number.
uuid                 | string        | The response ID, which can be used to view this response again with [xrGetReply](https://api.blocknet.co/#xrgetreply).





## etc_getStorageAt

> Sample Data

```cli
{
  "address": "0x407d73d8a49eeb85d32cf465507dd71d507100c1",
  "storage_position": "0x0",
  "block_parameter": "0x2"
}
```
Returns the value from a storage position at a given address.


### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '["0x407d73d8a49eeb85d32cf465507dd71d507100c1","0x0","0x2"]' https://api.oracleminer.com/xrs/etc_getStorageAt
```

```plaintext
blocknet-cli xrService etc_getStorageAt 0x407d73d8a49eeb85d32cf465507dd71d507100c1 0x0 0x2
```
<code class="api-call">etc_getStorageAt [address] [storage_position] [block_parameter]</code>

Parameter        | Type       | Description
-----------------|------------|-------------
address          | string     | Address of the code.
storage_position | string     | Integer of the position in the storage.
block_parameter  | string     | Integer block number, or the string 'latest', 'earliest' or 'pending'.


### Response Parameters

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
0x0000000000000000000000000000000000000000000000000000000000000000
```

```plaintext
{
  "reply": "0x0000000000000000000000000000000000000000000000000000000000000000",
  "uuid": "A6393979-8A29-4704-AF40-C514E03590A3"
}
```

Parameter            | Type          | Description
---------------------|---------------|-------------
reply                | string        | The value at this storage position.
jsonrpc              | string        | JSON RPC version.
id                   | int           | ID number.
uuid                 | string        | The response ID, which can be used to view this response again with [xrGetReply](https://api.blocknet.co/#xrgetreply).





## etc_getTransactionByBlockHashAndIndex

> Sample Data

```cli
{
  "block_hash": "0xfa533223775214de507f353a9521efb0efbc320896dcdf916f59b3ee21fa95e5",
  "tx_index_position": "0x0"
}
```
Returns information about a transaction by block hash and transaction index position.


### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '["0xfa533223775214de507f353a9521efb0efbc320896dcdf916f59b3ee21fa95e5","0x0"]' https://api.oracleminer.com/xrs/etc_getTransactionByBlockHashAndIndex
```

```plaintext
blocknet-cli xrService etc_getTransactionByBlockHashAndIndex 0xfa533223775214de507f353a9521efb0efbc320896dcdf916f59b3ee21fa95e5 0x0
```
<code class="api-call">etc_getTransactionByBlockHashAndIndex [block_hash] [tx_index_position]</code>

Parameter         | Type       | Description
------------------|------------|-------------
block_hash        | string     | Hash of a block.
tx_index_position | string     | Integer of the transaction index position.


### Response Parameters

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
{
  "blockHash": "0xfa533223775214de507f353a9521efb0efbc320896dcdf916f59b3ee21fa95e5",
  "blockNumber": "0xa1b6ed",
  "from": "0xe83f5955195ff3f41f3eca1d25ce3af149e55271",
  "gas": "0x186a0",
  "gasPrice": "0x3b9aca00",
  "hash": "0xed95cb266bf6a49821c660f98a5a127325f0dab40b4b80bf46b9ce453e9aa76f",
  "input": "0x0f2c9329000000000000000000000000fbb1b73c4f0bda4f67dca266ce6ef42f520fbb98000000000000000000000000e592b0d8baa2cb677034389b76a71b0d1823e0d1",
  "nonce": "0x2e1",
  "to": "0xe94b04a0fed112f3664e45adb2b8915693dd5ff3",
  "transactionIndex": "0x0",
  "value": "0x16d5f10461fe400",
  "v": "0x9d",
  "r": "0x2e51848a59292658e44ccfb8b6d5a916cf44e01f84c947bb930fffc38670e38f",
  "s": "0x68e2269d9f6b3e4cb32b8e160c218d784a52507d3b11feb2ca8e14b92d59d07b"
}
```

```plaintext
{
  "reply": {
    "blockHash": "0xfa533223775214de507f353a9521efb0efbc320896dcdf916f59b3ee21fa95e5",
    "blockNumber": "0xa1b6ed",
    "from": "0xe83f5955195ff3f41f3eca1d25ce3af149e55271",
    "gas": "0x186a0",
    "gasPrice": "0x3b9aca00",
    "hash": "0xed95cb266bf6a49821c660f98a5a127325f0dab40b4b80bf46b9ce453e9aa76f",
    "input": "0x0f2c9329000000000000000000000000fbb1b73c4f0bda4f67dca266ce6ef42f520fbb98000000000000000000000000e592b0d8baa2cb677034389b76a71b0d1823e0d1",
    "nonce": "0x2e1",
    "to": "0xe94b04a0fed112f3664e45adb2b8915693dd5ff3",
    "transactionIndex": "0x0",
    "value": "0x16d5f10461fe400",
    "v": "0x9d",
    "r": "0x2e51848a59292658e44ccfb8b6d5a916cf44e01f84c947bb930fffc38670e38f",
    "s": "0x68e2269d9f6b3e4cb32b8e160c218d784a52507d3b11feb2ca8e14b92d59d07b"
  },
  "uuid": "33D9CAB4-635E-4215-94A1-53C6BD747F52"
}
```

Parameter            | Type          | Description
---------------------|---------------|-------------
blockHash            | string        | Hash of the block where this transaction was in. `null` when its pending.
blockNumber          | string        | Block number where this transaction was in. `null` when its pending.
chainId              | string        | The chain id of the transaction, if any.
condition            | string        | (optional) conditional submission, Block number in block or timestamp in time or `null`.
creates              | string        | Creates contract hash.
from                 | string        | Address of the sender.
gas                  | string        | Gas provided by the sender.
gasPrice             | string        | Gas price provided by the sender in Wei.
hash                 | string        | Hash of the transaction.
input                | string        | The data send along with the transaction.
nonce                | string        | The number of transactions made by the sender prior to this one.
publicKey            | string        | Public key of the signer.
r                    | string        | The R field of the signature.
raw                  | string        | Raw transaction data.
s                    | string        | The S field of the signature.
standardV            | string        | The standardised V field of the signature (0 or 1).
to                   | string        | Address of the receiver. `null` when its a contract creation transaction.
transactionIndex     | string        | Integer of the transactions index position in the block. `null` when its pending.
v                    | string        | The standardised V field of the signature.
value                | string        | Value transferred in Wei.
jsonrpc              | string        | JSON RPC version.
id                   | int           | ID number.
uuid                 | string        | The response ID, which can be used to view this response again with [xrGetReply](https://api.blocknet.co/#xrgetreply).





## etc_getTransactionByBlockNumberAndIndex

> Sample Data

```cli
{
  "block_parameter": "0xa1b71d",
  "tx_index_position": "0x0"
}
```
Returns information about a transaction by block number and transaction index position.


### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '["0xa1b71d","0x0"]' https://api.oracleminer.com/xrs/etc_getTransactionByBlockNumberAndIndex
```

```plaintext
blocknet-cli xrService etc_getTransactionByBlockNumberAndIndex 0xa1b71d 0x0
```
<code class="api-call">etc_getTransactionByBlockNumberAndIndex [block_parameter] [tx_index_position]</code>

Parameter         | Type       | Description
------------------|------------|-------------
block_parameter   | string     | Integer block number, or the string 'latest', 'earliest' or 'pending'.
tx_index_position | string     | Integer of the transaction index position.


### Response Parameters

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
{
  "blockHash": "0xedb4e816d15f3e2f96b25887f05270c5dbd7dea628915ccda7b8d18ebc97c194",
  "blockNumber": "0xa1b71d",
  "from": "0xb09991c60c991c0fccde4b50b1100b05b8988e2d",
  "gas": "0xea60",
  "gasPrice": "0x4e3b29200",
  "hash": "0xd2cc7541921b83ede4fb93fd3337c11727a0d37d947ca3b546b706258f01edf6",
  "input": "0xad5632e60000000000000000000000000000000000000000000000000000000000000020000000000000000000000000000000000000000000000000000000000000004037346530616334363261333139343434353366613537323462363235363033303065323233636339373238303465336538363935393437393434356537383764",
  "nonce": "0x2bdef",
  "to": "0x888157b2f8f6263f820cddcca95a4c614a01df03",
  "transactionIndex": "0x0",
  "value": "0x0",
  "v": "0x9e",
  "r": "0x3bd762f367fe09d6e1b37abf75e84fc3deb205eaf5ba64204f4c2a82a9c0a146",
  "s": "0x3b6f586a3bd001c5e98549baff5948d20dca57a25e6b2529002d9612821961a2"
}
```

```plaintext
{
  "reply": {
    "blockHash": "0xedb4e816d15f3e2f96b25887f05270c5dbd7dea628915ccda7b8d18ebc97c194",
    "blockNumber": "0xa1b71d",
    "from": "0xb09991c60c991c0fccde4b50b1100b05b8988e2d",
    "gas": "0xea60",
    "gasPrice": "0x4e3b29200",
    "hash": "0xd2cc7541921b83ede4fb93fd3337c11727a0d37d947ca3b546b706258f01edf6",
    "input": "0xad5632e60000000000000000000000000000000000000000000000000000000000000020000000000000000000000000000000000000000000000000000000000000004037346530616334363261333139343434353366613537323462363235363033303065323233636339373238303465336538363935393437393434356537383764",
    "nonce": "0x2bdef",
    "to": "0x888157b2f8f6263f820cddcca95a4c614a01df03",
    "transactionIndex": "0x0",
    "value": "0x0",
    "v": "0x9e",
    "r": "0x3bd762f367fe09d6e1b37abf75e84fc3deb205eaf5ba64204f4c2a82a9c0a146",
    "s": "0x3b6f586a3bd001c5e98549baff5948d20dca57a25e6b2529002d9612821961a2"
  },
  "uuid": "E6EF0A63-D8E1-4A66-A6DE-8FB86A05149B"
}
```

Parameter            | Type          | Description
---------------------|---------------|-------------
blockHash            | string        | Hash of the block where this transaction was in. `null` when its pending.
blockNumber          | string        | Block number where this transaction was in. `null` when its pending.
chainId              | string        | The chain id of the transaction, if any.
condition            | string        | (optional) conditional submission, Block number in block or timestamp in time or `null`.
creates              | string        | Creates contract hash.
from                 | string        | Address of the sender.
gas                  | string        | Gas provided by the sender.
gasPrice             | string        | Gas price provided by the sender in Wei.
hash                 | string        | Hash of the transaction.
input                | string        | The data send along with the transaction.
nonce                | string        | The number of transactions made by the sender prior to this one.
publicKey            | string        | Public key of the signer.
r                    | string        | The R field of the signature.
raw                  | string        | Raw transaction data.
s                    | string        | The S field of the signature.
standardV            | string        | The standardised V field of the signature (0 or 1).
to                   | string        | Address of the receiver. `null` when its a contract creation transaction.
transactionIndex     | string        | Integer of the transactions index position in the block. `null` when its pending.
v                    | string        | The standardised V field of the signature.
value                | string        | Value transferred in Wei.
jsonrpc              | string        | JSON RPC version.
id                   | int           | ID number.
uuid                 | string        | The response ID, which can be used to view this response again with [xrGetReply](https://api.blocknet.co/#xrgetreply).





## etc_getTransactionByHash

> Sample Data

```cli
{
  "tx_hash": "0xed95cb266bf6a49821c660f98a5a127325f0dab40b4b80bf46b9ce453e9aa76f"
}
```
Returns the information about a transaction requested by transaction hash.


### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '["0xed95cb266bf6a49821c660f98a5a127325f0dab40b4b80bf46b9ce453e9aa76f"]' https://api.oracleminer.com/xrs/etc_getTransactionByHash
```

```plaintext
blocknet-cli xrService etc_getTransactionByHash 0xed95cb266bf6a49821c660f98a5a127325f0dab40b4b80bf46b9ce453e9aa76f
```
<code class="api-call">etc_getTransactionByHash [tx_hash]</code>

Parameter       | Type       | Description
----------------|------------|-------------
tx_hash         | string     | Hash of a transaction.


### Response Parameters

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
{
  "blockHash": "0xfa533223775214de507f353a9521efb0efbc320896dcdf916f59b3ee21fa95e5",
  "blockNumber": "0xa1b6ed",
  "from": "0xe83f5955195ff3f41f3eca1d25ce3af149e55271",
  "gas": "0x186a0",
  "gasPrice": "0x3b9aca00",
  "hash": "0xed95cb266bf6a49821c660f98a5a127325f0dab40b4b80bf46b9ce453e9aa76f",
  "input": "0x0f2c9329000000000000000000000000fbb1b73c4f0bda4f67dca266ce6ef42f520fbb98000000000000000000000000e592b0d8baa2cb677034389b76a71b0d1823e0d1",
  "nonce": "0x2e1",
  "to": "0xe94b04a0fed112f3664e45adb2b8915693dd5ff3",
  "transactionIndex": "0x0",
  "value": "0x16d5f10461fe400",
  "v": "0x9d",
  "r": "0x2e51848a59292658e44ccfb8b6d5a916cf44e01f84c947bb930fffc38670e38f",
  "s": "0x68e2269d9f6b3e4cb32b8e160c218d784a52507d3b11feb2ca8e14b92d59d07b"
}
```

```plaintext
{
  "reply": {
    "blockHash": "0xfa533223775214de507f353a9521efb0efbc320896dcdf916f59b3ee21fa95e5",
    "blockNumber": "0xa1b6ed",
    "from": "0xe83f5955195ff3f41f3eca1d25ce3af149e55271",
    "gas": "0x186a0",
    "gasPrice": "0x3b9aca00",
    "hash": "0xed95cb266bf6a49821c660f98a5a127325f0dab40b4b80bf46b9ce453e9aa76f",
    "input": "0x0f2c9329000000000000000000000000fbb1b73c4f0bda4f67dca266ce6ef42f520fbb98000000000000000000000000e592b0d8baa2cb677034389b76a71b0d1823e0d1",
    "nonce": "0x2e1",
    "to": "0xe94b04a0fed112f3664e45adb2b8915693dd5ff3",
    "transactionIndex": "0x0",
    "value": "0x16d5f10461fe400",
    "v": "0x9d",
    "r": "0x2e51848a59292658e44ccfb8b6d5a916cf44e01f84c947bb930fffc38670e38f",
    "s": "0x68e2269d9f6b3e4cb32b8e160c218d784a52507d3b11feb2ca8e14b92d59d07b"
  },
  "uuid": "8E760756-DACB-4719-9414-45740BE8A2C5"
}
```

Parameter            | Type          | Description
---------------------|---------------|-------------
blockHash            | string        | Hash of the block where this transaction was in. `null` when its pending.
blockNumber          | string        | Block number where this transaction was in. `null` when its pending.
chainId              | string        | The chain id of the transaction, if any.
condition            | string        | (optional) conditional submission, Block number in block or timestamp in time or `null`.
creates              | string        | Creates contract hash.
from                 | string        | Address of the sender.
gas                  | string        | Gas provided by the sender.
gasPrice             | string        | Gas price provided by the sender in Wei.
hash                 | string        | Hash of the transaction.
input                | string        | The data send along with the transaction.
nonce                | string        | The number of transactions made by the sender prior to this one.
publicKey            | string        | Public key of the signer.
r                    | string        | The R field of the signature.
raw                  | string        | Raw transaction data.
s                    | string        | The S field of the signature.
standardV            | string        | The standardised V field of the signature (0 or 1).
to                   | string        | Address of the receiver. `null` when its a contract creation transaction.
transactionIndex     | string        | Integer of the transactions index position in the block. `null` when its pending.
v                    | string        | The standardised V field of the signature.
value                | string        | Value transferred in Wei.
jsonrpc              | string        | JSON RPC version.
id                   | int           | ID number.
uuid                 | string        | The response ID, which can be used to view this response again with [xrGetReply](https://api.blocknet.co/#xrgetreply).





## etc_getTransactionCount

> Sample Data

```cli
{
  "address": "0x407d73d8a49eeb85d32cf465507dd71d507100c1",
  "block_parameter": "latest"
}
```
Returns the number of transactions sent from an address.


### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '["0x407d73d8a49eeb85d32cf465507dd71d507100c1","latest"]' https://api.oracleminer.com/xrs/etc_getTransactionCount
```

```plaintext
blocknet-cli xrService etc_getTransactionCount 0x407d73d8a49eeb85d32cf465507dd71d507100c1 latest
```
<code class="api-call">etc_getTransactionCount [address] [block_parameter]</code>

Parameter       | Type       | Description
----------------|------------|-------------
address         | string     | The address.
block_parameter | string     | Integer block number, or the string 'latest', 'earliest' or 'pending'.


### Response Parameters

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
0x0
```

```plaintext
{
  "reply": "0x0",
  "uuid": "FC3C5BBC-AC96-4CC7-B394-CC9EA19EB9CC"
}
```

Parameter            | Type          | Description
---------------------|---------------|-------------
reply                | string        | Integer of the number of transactions send from this address.
jsonrpc              | string        | JSON RPC version.
id                   | int           | ID number.
uuid                 | string        | The response ID, which can be used to view this response again with [xrGetReply](https://api.blocknet.co/#xrgetreply).





## etc_getTransactionReceipt

> Sample Data

```cli
{
  "tx_hash": "0xed95cb266bf6a49821c660f98a5a127325f0dab40b4b80bf46b9ce453e9aa76f"
}
```
Returns the receipt of a transaction by transaction hash.

**Note:** Receipt not available for pending transactions. 


### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '["0xed95cb266bf6a49821c660f98a5a127325f0dab40b4b80bf46b9ce453e9aa76f"]' https://api.oracleminer.com/xrs/etc_getTransactionReceipt
```

```plaintext
blocknet-cli xrService etc_getTransactionReceipt 0xed95cb266bf6a49821c660f98a5a127325f0dab40b4b80bf46b9ce453e9aa76f
```
<code class="api-call">etc_getTransactionReceipt [tx_hash]</code>

Parameter       | Type       | Description
----------------|------------|-------------
tx_hash         | string     | Hash of a transaction.


### Response Parameters

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
{
  "blockHash": "0xfa533223775214de507f353a9521efb0efbc320896dcdf916f59b3ee21fa95e5",
  "blockNumber": "0xa1b6ed",
  "contractAddress": null,
  "cumulativeGasUsed": "0x8db3",
  "from": "0xe83f5955195ff3f41f3eca1d25ce3af149e55271",
  "gasUsed": "0x8db3",
  "logs": [
    {
      "address": "0xe94b04a0fed112f3664e45adb2b8915693dd5ff3",
      "topics": [
        "0x23919512b2162ddc59b67a65e3b03c419d4105366f7d4a632f5d3c3bee9b1cff"
      ],
      "data": "0x000000000000000000000000e592b0d8baa2cb677034389b76a71b0d1823e0d1",
      "blockNumber": "0xa1b6ed",
      "transactionHash": "0xed95cb266bf6a49821c660f98a5a127325f0dab40b4b80bf46b9ce453e9aa76f",
      "transactionIndex": "0x0",
      "blockHash": "0xfa533223775214de507f353a9521efb0efbc320896dcdf916f59b3ee21fa95e5",
      "logIndex": "0x0",
      "removed": false
    }
  ],
  "logsBloom": "0x00000000040000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000020000000000000000000000000000000000000000000000000000000000000000000000000000000",
  "status": "0x1",
  "to": "0xe94b04a0fed112f3664e45adb2b8915693dd5ff3",
  "transactionHash": "0xed95cb266bf6a49821c660f98a5a127325f0dab40b4b80bf46b9ce453e9aa76f",
  "transactionIndex": "0x0"
}
```

```plaintext
{
  "reply": {
    "blockHash": "0xfa533223775214de507f353a9521efb0efbc320896dcdf916f59b3ee21fa95e5",
    "blockNumber": "0xa1b6ed",
    "contractAddress": null,
    "cumulativeGasUsed": "0x8db3",
    "from": "0xe83f5955195ff3f41f3eca1d25ce3af149e55271",
    "gasUsed": "0x8db3",
    "logs": [
      {
        "address": "0xe94b04a0fed112f3664e45adb2b8915693dd5ff3",
        "topics": [
          "0x23919512b2162ddc59b67a65e3b03c419d4105366f7d4a632f5d3c3bee9b1cff"
        ],
        "data": "0x000000000000000000000000e592b0d8baa2cb677034389b76a71b0d1823e0d1",
        "blockNumber": "0xa1b6ed",
        "transactionHash": "0xed95cb266bf6a49821c660f98a5a127325f0dab40b4b80bf46b9ce453e9aa76f",
        "transactionIndex": "0x0",
        "blockHash": "0xfa533223775214de507f353a9521efb0efbc320896dcdf916f59b3ee21fa95e5",
        "logIndex": "0x0",
        "removed": false
      }
    ],
    "logsBloom": "0x00000000040000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000020000000000000000000000000000000000000000000000000000000000000000000000000000000",
    "status": "0x1",
    "to": "0xe94b04a0fed112f3664e45adb2b8915693dd5ff3",
    "transactionHash": "0xed95cb266bf6a49821c660f98a5a127325f0dab40b4b80bf46b9ce453e9aa76f",
    "transactionIndex": "0x0"
  },
  "uuid": "B61C5E6A-4B1C-499E-96EA-1CDB37099DAE"
}
```

Parameter            | Type          | Description
---------------------|---------------|-------------
blockHash            | string        | Hash of the block where this transaction was in.
blockNumber          | string        | Block number where this transaction was in.
contractAddress      | string        | The contract address created, if the transaction was a contract creation, otherwise `null`.
cumulativeGasUsed    | string        | The total amount of gas used when this transaction was executed in the block.
from                 | string        | The address of the sender.
gasUsed              | string        | The amount of gas used by this specific transaction alone.
logs                 | Array         | Array of log objects, which this transaction generated.
logsBloom            | string        | A bloom filter of logs/events generated by contracts during transaction execution. Used to efficiently rule out transactions without expected logs.
status               | string        | `0x0` indicates transaction failure , `0x1` indicates transaction success. Set for blocks mined after Byzantium hard fork EIP609, `null` before.
to                   | string        | Address of the receiver. `null` when its a contract creation transaction.
transactionHash      | string        | Hash of the transaction.
transactionIndex     | string        | Integer of the transactions index position in the block.
jsonrpc              | string        | JSON RPC version.
id                   | int           | ID number.
uuid                 | string        | The response ID, which can be used to view this response again with [xrGetReply](https://api.blocknet.co/#xrgetreply).





## etc_getUncleByBlockHashAndIndex

> Sample Data

```cli
{
  "block_hash": "0xfa533223775214de507f353a9521efb0efbc320896dcdf916f59b3ee21fa95e5",
  "uncleindex_position": "0x0"
}
```
Returns information about a uncle of a block by hash and uncle index position.

**Note:** An uncle doesn’t contain individual transactions.

### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '["0xfa533223775214de507f353a9521efb0efbc320896dcdf916f59b3ee21fa95e5","0x0"]' https://api.oracleminer.com/xrs/etc_getUncleByBlockHashAndIndex
```

```plaintext
blocknet-cli xrService etc_getUncleByBlockHashAndIndex 0xfa533223775214de507f353a9521efb0efbc320896dcdf916f59b3ee21fa95e5 0x0
```
<code class="api-call">etc_getUncleByBlockHashAndIndex [block_hash] [uncle_index_position]</code>

Parameter            | Type       | Description
---------------------|------------|-------------
block_hash           | string     | Hash of a block.
uncle_index_position | string     | Integer of the uncle index position.


### Response Parameters

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
{
  "difficulty": "0x55df223d798c",
  "extraData": "0x505059452d7374726174756d2d65752d32",
  "gasLimit": "0x7a3083",
  "gasUsed": "0x0",
  "hash": "0xb4dfa97579cef4d5aac862e49095bb01d06bf43e3fd5ade9c37a0fd83c9c4e9c",
  "logsBloom": "0x00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000",
  "miner": "0xdf7d7e053933b5cc24372f878c90e62dadad5d42",
  "mixHash": "0x1b8653c21d2044696ec63548440b7cfc0974c73fd07ae3c89b6d32a670a9e94f",
  "nonce": "0x508ea234130d6487",
  "number": "0xa1b6ec",
  "parentHash": "0x42c22180f4565d13ba3f6b9a3077c7b663c53619a761987d0691e148f53d3a29",
  "receiptsRoot": "0x56e81f171bcc55a6ff8345e692c0f86e5b48e01b996cadc001622fb5e363b421",
  "sha3Uncles": "0x1dcc4de8dec75d7aab85b567b6ccd41ad312451b948a7413f0a142fd40d49347",
  "size": "0x216",
  "stateRoot": "0x21f386e61ad1087e4501fc4f89ea71aea843cf1c12743767f7815a4f5439f9a7",
  "timestamp": "0x5ee78d35",
  "transactionsRoot": "0x56e81f171bcc55a6ff8345e692c0f86e5b48e01b996cadc001622fb5e363b421",
  "uncles": []
}
```

```plaintext
{
  "reply": {
    "difficulty": "0x55df223d798c",
    "extraData": "0x505059452d7374726174756d2d65752d32",
    "gasLimit": "0x7a3083",
    "gasUsed": "0x0",
    "hash": "0xb4dfa97579cef4d5aac862e49095bb01d06bf43e3fd5ade9c37a0fd83c9c4e9c",
    "logsBloom": "0x00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000",
    "miner": "0xdf7d7e053933b5cc24372f878c90e62dadad5d42",
    "mixHash": "0x1b8653c21d2044696ec63548440b7cfc0974c73fd07ae3c89b6d32a670a9e94f",
    "nonce": "0x508ea234130d6487",
    "number": "0xa1b6ec",
    "parentHash": "0x42c22180f4565d13ba3f6b9a3077c7b663c53619a761987d0691e148f53d3a29",
    "receiptsRoot": "0x56e81f171bcc55a6ff8345e692c0f86e5b48e01b996cadc001622fb5e363b421",
    "sha3Uncles": "0x1dcc4de8dec75d7aab85b567b6ccd41ad312451b948a7413f0a142fd40d49347",
    "size": "0x216",
    "stateRoot": "0x21f386e61ad1087e4501fc4f89ea71aea843cf1c12743767f7815a4f5439f9a7",
    "timestamp": "0x5ee78d35",
    "transactionsRoot": "0x56e81f171bcc55a6ff8345e692c0f86e5b48e01b996cadc001622fb5e363b421",
    "uncles": [
    ]
  },
  "uuid": "96C93F30-48ED-4ECF-9BA3-067EE63221B3"
}
```

Parameter            | Type          | Description
---------------------|---------------|-------------
author               | string        | The address of the author of the block.
difficulty           | string        | Integer of the difficulty for this block.
extraData            | string        | The ‘extra data’ field of this block.
gasLimit             | string        | The maximum gas allowed in this block.
gasUsed              | string        | The total used gas by all transactions in this block.
hash                 | string        | Hash of the block. `null` when its pending block.
logsBloom            | string        | The bloom filter for the logs of the block. `null` when its pending block.
miner                | string        | Alias of ‘author’.
mixHash              | string        | The mix hash.
nonce                | string        | Hash of the generated proof-of-work. `null` when its pending block. Missing in case of PoA.
number               | string        | The block number. `null` when its pending block.
parentHash           | string        | Hash of the parent block.
receiptsRoot         | string        | The root of the receipts trie of the block.
sealFields           | Array         | Array of seal fields.
sha3Uncles           | string        | SHA3 of the uncles data in the block.
size                 | string        | Integer the size of this block in bytes. 
stateRoot            | string        | The root of the final state trie of the block.
timestamp            | string        | The unix timestamp for when the block was collated.
totalDifficulty      | string        | Integer of the total difficulty of the chain until this block.
transactions         | Array         | Array of transaction objects, or 32 Bytes transaction hashes depending on the last given parameter.
transactionsRoot     | string        | The root of the transaction trie of the block.
uncles               | Array         | Array of uncle hashes.
jsonrpc              | string        | JSON RPC version.
id                   | int           | ID number.
uuid                 | string        | The response ID, which can be used to view this response again with [xrGetReply](https://api.blocknet.co/#xrgetreply).





## etc_getUncleByBlockNumberAndIndex

> Sample Data

```cli
{
  "block_parameter": "0xa1b6ed",
  "uncle_index_position": "0x0"
}
```
Returns information about a uncle of a block by number and uncle index position.

**Note:** An uncle doesn’t contain individual transactions.

### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '["0xa1b6ed","0x0"]' https://api.oracleminer.com/xrs/etc_getUncleByBlockNumberAndIndex
```

```plaintext
blocknet-cli xrService etc_getUncleByBlockNumberAndIndex 0xa1b6ed 0x0
```
<code class="api-call">etc_getUncleByBlockNumberAndIndex [block_parameter] [uncle_index_position]</code>

Parameter            | Type       | Description
---------------------|------------|-------------
block_parameter      | string     | Integer block number, or the string 'latest', 'earliest' or 'pending'.
uncle_index_position | string     | Integer of the uncle index position.


### Response Parameters

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
{
  "difficulty": "0x55df223d798c",
  "extraData": "0x505059452d7374726174756d2d65752d32",
  "gasLimit": "0x7a3083",
  "gasUsed": "0x0",
  "hash": "0xb4dfa97579cef4d5aac862e49095bb01d06bf43e3fd5ade9c37a0fd83c9c4e9c",
  "logsBloom": "0x00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000",
  "miner": "0xdf7d7e053933b5cc24372f878c90e62dadad5d42",
  "mixHash": "0x1b8653c21d2044696ec63548440b7cfc0974c73fd07ae3c89b6d32a670a9e94f",
  "nonce": "0x508ea234130d6487",
  "number": "0xa1b6ec",
  "parentHash": "0x42c22180f4565d13ba3f6b9a3077c7b663c53619a761987d0691e148f53d3a29",
  "receiptsRoot": "0x56e81f171bcc55a6ff8345e692c0f86e5b48e01b996cadc001622fb5e363b421",
  "sha3Uncles": "0x1dcc4de8dec75d7aab85b567b6ccd41ad312451b948a7413f0a142fd40d49347",
  "size": "0x216",
  "stateRoot": "0x21f386e61ad1087e4501fc4f89ea71aea843cf1c12743767f7815a4f5439f9a7",
  "timestamp": "0x5ee78d35",
  "transactionsRoot": "0x56e81f171bcc55a6ff8345e692c0f86e5b48e01b996cadc001622fb5e363b421",
  "uncles": []
}
```

```plaintext
{
  "reply": {
    "difficulty": "0x55df223d798c",
    "extraData": "0x505059452d7374726174756d2d65752d32",
    "gasLimit": "0x7a3083",
    "gasUsed": "0x0",
    "hash": "0xb4dfa97579cef4d5aac862e49095bb01d06bf43e3fd5ade9c37a0fd83c9c4e9c",
    "logsBloom": "0x00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000",
    "miner": "0xdf7d7e053933b5cc24372f878c90e62dadad5d42",
    "mixHash": "0x1b8653c21d2044696ec63548440b7cfc0974c73fd07ae3c89b6d32a670a9e94f",
    "nonce": "0x508ea234130d6487",
    "number": "0xa1b6ec",
    "parentHash": "0x42c22180f4565d13ba3f6b9a3077c7b663c53619a761987d0691e148f53d3a29",
    "receiptsRoot": "0x56e81f171bcc55a6ff8345e692c0f86e5b48e01b996cadc001622fb5e363b421",
    "sha3Uncles": "0x1dcc4de8dec75d7aab85b567b6ccd41ad312451b948a7413f0a142fd40d49347",
    "size": "0x216",
    "stateRoot": "0x21f386e61ad1087e4501fc4f89ea71aea843cf1c12743767f7815a4f5439f9a7",
    "timestamp": "0x5ee78d35",
    "transactionsRoot": "0x56e81f171bcc55a6ff8345e692c0f86e5b48e01b996cadc001622fb5e363b421",
    "uncles": [
    ]
  },
  "uuid": "B3F0A367-0F6D-43D8-A2DB-DF5C430147D6"
}
```

Parameter            | Type          | Description
---------------------|---------------|-------------
author               | string        | The address of the author of the block.
difficulty           | string        | Integer of the difficulty for this block.
extraData            | string        | The ‘extra data’ field of this block.
gasLimit             | string        | The maximum gas allowed in this block.
gasUsed              | string        | The total used gas by all transactions in this block.
hash                 | string        | Hash of the block. `null` when its pending block.
logsBloom            | string        | The bloom filter for the logs of the block. `null` when its pending block.
miner                | string        | Alias of ‘author’.
mixHash              | string        | The mix hash.
nonce                | string        | Hash of the generated proof-of-work. `null` when its pending block. Missing in case of PoA.
number               | string        | The block number. `null` when its pending block.
parentHash           | string        | Hash of the parent block.
receiptsRoot         | string        | The root of the receipts trie of the block.
sealFields           | Array         | Array of seal fields.
sha3Uncles           | string        | SHA3 of the uncles data in the block.
size                 | string        | Integer the size of this block in bytes. 
stateRoot            | string        | The root of the final state trie of the block.
timestamp            | string        | The unix timestamp for when the block was collated.
totalDifficulty      | string        | Integer of the total difficulty of the chain until this block.
transactions         | Array         | Array of transaction objects, or 32 Bytes transaction hashes depending on the last given parameter.
transactionsRoot     | string        | The root of the transaction trie of the block.
uncles               | Array         | Array of uncle hashes.
jsonrpc              | string        | JSON RPC version.
id                   | int           | ID number.
uuid                 | string        | The response ID, which can be used to view this response again with [xrGetReply](https://api.blocknet.co/#xrgetreply).





## etc_getUncleCountByBlockHash

> Sample Data

```cli
{
  "block_hash": "0xb4dfa97579cef4d5aac862e49095bb01d06bf43e3fd5ade9c37a0fd83c9c4e9c"
}
```
Returns the number of uncles in a block from a block matching the given block hash.


### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '["0xb4dfa97579cef4d5aac862e49095bb01d06bf43e3fd5ade9c37a0fd83c9c4e9c"]' https://api.oracleminer.com/xrs/etc_getUncleCountByBlockHash
```

```plaintext
blocknet-cli xrService etc_getUncleCountByBlockHash 0xb4dfa97579cef4d5aac862e49095bb01d06bf43e3fd5ade9c37a0fd83c9c4e9c
```
<code class="api-call">etc_getUncleCountByBlockHash [block_hash]</code>

Parameter       | Type       | Description
----------------|------------|-------------
block_hash      | string     | Hash of a block.


### Response Parameters

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
0x0
```

```plaintext
{
  "reply": "0x0",
  "uuid": "DDBB2C26-2174-4361-9B93-016FAA0A8C55"
}
```

Parameter            | Type          | Description
---------------------|---------------|-------------
reply                | string        | Integer of the number of uncles in this block.
jsonrpc              | string        | JSON RPC version.
id                   | int           | ID number.
uuid                 | string        | The response ID, which can be used to view this response again with [xrGetReply](https://api.blocknet.co/#xrgetreply).





## etc_getUncleCountByBlockNumber

> Sample Data

```cli
{
  "block_parameter": "latest"
}
```
Returns the number of uncles in a block from a block matching the given block number.


### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '["latest"]' https://api.oracleminer.com/xrs/etc_getUncleCountByBlockNumber
```

```plaintext
blocknet-cli xrService etc_getUncleCountByBlockNumber latest
```
<code class="api-call">etc_getUncleCountByBlockNumber [block_parameter]</code>

Parameter       | Type       | Description
----------------|------------|-------------
block_parameter | string     | Integer block number, or the string 'latest', 'earliest' or 'pending'.


### Response Parameters

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
0x0
```

```plaintext
{
  "reply": "0x0",
  "uuid": "60D3660B-D3FD-490A-A0F6-04D3E52F80B8"
}
```

Parameter            | Type          | Description
---------------------|---------------|-------------
reply                | string        | Integer of the number of uncles in this block.
jsonrpc              | string        | JSON RPC version.
id                   | int           | ID number.
uuid                 | string        | The response ID, which can be used to view this response again with [xrGetReply](https://api.blocknet.co/#xrgetreply).




## etc_getWork

Returns the hash of the current block, the seedHash, and the boundary condition to be met (“target”).

### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '[]' https://api.oracleminer.com/xrs/etc_getWork
```

```plaintext
blocknet-cli xrService etc_getWork
```
<code class="api-call">etc_getWork</code>

This call does not take parameters.


### Response

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
{
  "jsonrpc": "2.0",
  "id": 1,
  "error": {
    "code": -32000,
    "message": "no mining work available yet"
  }
}
```

```plaintext
{
  "code": 1002,
  "error": {
    "code": -32000,
    "message": "no mining work available yet"
  },
  "id": 1,
  "jsonrpc": "2.0",
  "uuid": "14795E53-6FE3-4745-9781-89BFF949E495"
}
```

Parameter            | Type          | Description
---------------------|---------------|-------------
reply                | Array         | Array of current block header pow-hash, seed hash used for the DAG, boudary condition ("target") 2^256/difficulty and the current block number.
jsonrpc              | string        | JSON RPC version.
id                   | int           | ID number.
uuid                 | string        | The response ID, which can be used to view this response again with [xrGetReply](https://api.blocknet.co/#xrgetreply).

**Note:** This call will not return any mining work.





## etc_hashrate

Returns the number of hashes per second that the node is mining with.

### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '[]' https://api.oracleminer.com/xrs/etc_hashrate
```

```plaintext
blocknet-cli xrService etc_hashrate
```
<code class="api-call">etc_hashrate</code>

This call does not take parameters.


### Response

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
0x0
```

```plaintext
{
  "reply": "0x0",
  "uuid": "72A73E68-79B0-412D-8AC0-EC23946B4864"
}
```

Parameter            | Type          | Description
---------------------|---------------|-------------
reply                | string        | Number of hashes per second.
jsonrpc              | string        | JSON RPC version.
id                   | int           | ID number.
uuid                 | string        | The response ID, which can be used to view this response again with [xrGetReply](https://api.blocknet.co/#xrgetreply).

**Note:** This call will only return `0x0` as the mining hash rate.





## etc_mining

Returns `true` if client is actively mining new blocks.

### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '[]' https://api.oracleminer.com/xrs/etc_mining
```

```plaintext
blocknet-cli xrService etc_mining
```
<code class="api-call">etc_mining</code>

This call does not take parameters.


### Response

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
{
  "jsonrpc": "2.0",
  "id": 1,
  "result": false
}
```

```plaintext
{
  "id": 1,
  "jsonrpc": "2.0",
  "reply": false,
  "uuid": "A4933FAF-99DA-4E3B-8B87-ACE377CE0C58"
}
```

Parameter            | Type          | Description
---------------------|---------------|-------------
reply                | boolean       | `true` if the client is mining, otherwise `false`
jsonrpc              | string        | JSON RPC version.
id                   | int           | ID number.
uuid                 | string        | The response ID, which can be used to view this response again with [xrGetReply](https://api.blocknet.co/#xrgetreply).

**Note:** This call will only return `false`.





## etc_newBlockFilter

Creates a filter in the node, to notify when a new block arrives. To check if the state has changed, call [etc_getFilterChanges](#etc_getfilterchanges).

### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '[]' https://api.oracleminer.com/xrs/etc_newBlockFilter
```

```plaintext
blocknet-cli xrService etc_newBlockFilter
```
<code class="api-call">etc_newBlockFilter</code>

This call does not take parameters.


### Response

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
0x3cc4e57bf1fe5c0476b4a7092abfd52
```

```plaintext
{
  "reply": "0x3cc4e57bf1fe5c0476b4a7092abfd52",
  "uuid": "4582ADA3-B81F-488F-9B49-DC9E17B84E50"
}
```

Parameter            | Type          | Description
---------------------|---------------|-------------
reply                | string        | A filter id.
jsonrpc              | string        | JSON RPC version.
id                   | int           | ID number.
uuid                 | string        | The response ID, which can be used to view this response again with [xrGetReply](https://api.blocknet.co/#xrgetreply).





## etc_newFilter

> Sample Data

```cli
{
  "fromBlock": "0xa1b774",
  "toBlock": "latest",
  "address": "0x8888f1f195afa192cfee860698584c030f4c9db1",
  "topics": "null"
}
```
Creates a filter object, based on filter options, to notify when the state changes (logs). To check if the state has changed, call [etc_getFilterChanges](#etc_getfilterchanges).


### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '["0xa1b774","latest","0x8888f1f195afa192cfee860698584c030f4c9db1","null"]' https://api.oracleminer.com/xrs/etc_newFilter
```

```plaintext
blocknet-cli xrService etc_newFilter 0xa1b774 latest 0x8888f1f195afa192cfee860698584c030f4c9db1 null
```
<code class="api-call">etc_newFilter [fromBlock] [toBlock] [address] [topics]</code>

Parameter       | Type               | Description
----------------|--------------------|-------------
fromBlock       | string             | Integer block number, or 'latest' for the last mined block or 'pending', 'earliest' for not yet mined transactions.
toBlock         | string             | Integer block number, or 'latest' for the last mined block or 'pending', 'earliest' for not yet mined transactions.
address         | string             | Contract address or a list of addresses from which logs should originate.
topics          | Array              | Topics are order-dependent. It’s possible to pass in null to match any topic, or a subarray of multiple topics of which one should be matching.



### Response Parameters

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
0x7d67f3962be4cf2197806f4520245f6e
```

```plaintext
{
  "reply": "0x7d67f3962be4cf2197806f4520245f6e",
  "uuid": "619D7E07-B6F2-49D5-B3F3-49E8D5E030AB"
}
```

Parameter            | Type          | Description
---------------------|---------------|-------------
reply                | string        | The filter id.
jsonrpc              | string        | JSON RPC version.
id                   | int           | ID number.
uuid                 | string        | The response ID, which can be used to view this response again with [xrGetReply](https://api.blocknet.co/#xrgetreply).





## etc_newPendingTransactionFilter

Creates a filter in the node, to notify when new pending transactions arrive. To check if the state has changed, call [etc_getFilterChanges](#etc_getFilterChanges).

### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '[]' https://api.oracleminer.com/xrs/etc_newPendingTransactionFilter
```

```plaintext
blocknet-cli xrService etc_newPendingTransactionFilter
```
<code class="api-call">etc_newPendingTransactionFilter</code>

This call does not take parameters.


### Response

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
0xcb4a28c9cec1b3dde618f07a75c83019
```

```plaintext
{
  "reply": "0xcb4a28c9cec1b3dde618f07a75c83019",
  "uuid": "B7ADF7FC-7484-490E-863F-66AE965FCF6E"
}
```

Parameter            | Type          | Description
---------------------|---------------|-------------
reply                | string        | A filter id.
jsonrpc              | string        | JSON RPC version.
id                   | int           | ID number.
uuid                 | string        | The response ID, which can be used to view this response again with [xrGetReply](https://api.blocknet.co/#xrgetreply).






## etc_protocolVersion

Returns the current Ethereum protocol version.

### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '[]' https://api.oracleminer.com/xrs/etc_protocolVersion
```

```plaintext
blocknet-cli xrService etc_protocolVersion
```
<code class="api-call">etc_protocolVersion</code>

This call does not take parameters.


### Response

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
0x41
```

```plaintext
{
  "reply": "0x41",
  "uuid": "67FF949C-0E5B-493B-A6AC-9B54F8643833"
}
```

Parameter            | Type          | Description
---------------------|---------------|-------------
reply                | string        | The current Ethereum protocol version.
jsonrpc              | string        | JSON RPC version.
id                   | int           | ID number.
uuid                 | string        | The response ID, which can be used to view this response again with [xrGetReply](https://api.blocknet.co/#xrgetreply).





## etc_sendRawTransaction

> Sample Data

```cli
{
  "tx_data": "0xf86c8085098bca5a008307a1209437ede5f23cdcecfba18331126668ef705ea78489872386f26fc100008025a04058f161da3a3b028d2a0cbb98f3d22045f97a41150506cb9a52cbf0238622e8a077b6880c0d4c2c1c4ebe23c51d86954aebafaa766cd38806d299997f3face0dd"
}
```
Submits a signed transaction to the Ethereum network.


### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '["0xf86c8085098bca5a008307a1209437ede5f23cdcecfba18331126668ef705ea78489872386f26fc100008025a04058f161da3a3b028d2a0cbb98f3d22045f97a41150506cb9a52cbf0238622e8a077b6880c0d4c2c1c4ebe23c51d86954aebafaa766cd38806d299997f3face0dd"]' https://api.oracleminer.com/xrs/etc_sendRawTransaction
```

```plaintext
blocknet-cli xrService etc_sendRawTransaction 0xf86c8085098bca5a008307a1209437ede5f23cdcecfba18331126668ef705ea78489872386f26fc100008025a04058f161da3a3b028d2a0cbb98f3d22045f97a41150506cb9a52cbf0238622e8a077b6880c0d4c2c1c4ebe23c51d86954aebafaa766cd38806d299997f3face0dd
```
<code class="api-call">etc_sendRawTransaction [tx_data]</code>

Parameter       | Type       | Description
----------------|------------|-------------
tx_data         | string     | The signed transaction data


### Response Parameters

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
0xbb4e52e164889e0f9a7228792ab18ba866a32934f0f136e0e563fdfaaefd34dc
```

```plaintext
{
    "reply" : "0xbb4e52e164889e0f9a7228792ab18ba866a32934f0f136e0e563fdfaaefd34dc",
    "uuid" : "8DD65AE9-D82A-4DDE-B614-E5CCB69995DA"
}
```

Parameter            | Type          | Description
---------------------|---------------|-------------
reply                | string        | The transaction hash, or the zero hash if the transaction is not yet available.
jsonrpc              | string        | JSON RPC version.
id                   | int           | ID number.
uuid                 | string        | The response ID, which can be used to view this response again with [xrGetReply](https://api.blocknet.co/#xrgetreply).





## etc_submitWork

> Sample Data

```cli
{
  "nonce": "0x0000000000000001",
  "pow_hash": "0x1234567890abcdef1234567890abcdef1234567890abcdef1234567890abcdef",
  "mix_digest": "0xD1FE5700000000000000000000000000D1FE5700000000000000000000000000"
}
```
Used for submitting a proof-of-work solution.


### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '["0x0000000000000001","0x1234567890abcdef1234567890abcdef1234567890abcdef1234567890abcdef","0xD1FE5700000000000000000000000000D1FE5700000000000000000000000000"]' https://api.oracleminer.com/xrs/etc_submitWork
```

```plaintext
blocknetdx-cli xrService etc_submitWork 0x0000000000000001 0x1234567890abcdef1234567890abcdef1234567890abcdef1234567890abcdef 0xD1FE5700000000000000000000000000D1FE5700000000000000000000000000
```
<code class="api-call">etc_submitWork [nonce] [pow_hash] [mix_digest]</code>

Parameter       | Type       | Description
----------------|------------|-------------
nonce           | string     | The nonce found (64 bits).
pow_hash        | string     | The header’s pow-hash (256 bits)
mix_digest      | string     | The mix digest (256 bits).

### Response Parameters

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
{
  "jsonrpc": "2.0",
  "id": 1,
  "result": false
}
```

```plaintext
{
  "id": 1,
  "jsonrpc": "2.0",
  "reply": false,
  "uuid": "A0795786-6E04-49D9-B1B3-C0DE8614FEFF"
}
```

Parameter            | Type          | Description
---------------------|---------------|-------------
reply                | boolean       | `true` if the provided solution is valid, otherwise `false`.
jsonrpc              | string        | JSON RPC version.
id                   | int           | ID number.
uuid                 | string        | The response ID, which can be used to view this response again with [xrGetReply](https://api.blocknet.co/#xrgetreply).





## etc_subscribe

> Sample Data

```cli
{
  "param": ""
}
```
Starts a subscription (on WebSockets / IPC / TCP transports) to a particular event. For every event that matches the subscription a JSON-RPC notification with event details and subscription ID will be sent to a client. **(Work in progress)**


### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '[""]' https://api.oracleminer.com/xrs/etc_subscribe
```

```plaintext
blocknet-cli xrService etc_subscribe [param]
```
<code class="api-call">etc_subscribe []</code>

Parameter       | Type       | Description
----------------|------------|-------------
param           | string     | Description


### Response Parameters

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell

```

```plaintext

```
`RESPONSE` - WIP





## etc_syncing

Returns an object with data about the sync status or `false`.

### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '[]' https://api.oracleminer.com/xrs/etc_syncing
```

```plaintext
blocknet-cli xrService etc_syncing
```
<code class="api-call">etc_syncing</code>

This call does not take parameters.


### Response

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
{
  "jsonrpc": "2.0",
  "id": 1,
  "result": false
}
```

```plaintext
{
  "id": 1,
  "jsonrpc": "2.0",
  "reply": false,
  "uuid": "C1780F99-3001-4524-AA37-C2B0D75A46E4"
}
```

Parameter            | Type          | Description
---------------------|---------------|-------------
reply                | boolean       | An object with sync status data or `false`, when not syncing.
jsonrpc              | string        | JSON RPC version.
id                   | int           | ID number.
uuid                 | string        | The response ID, which can be used to view this response again with [xrGetReply](https://api.blocknet.co/#xrgetreply).





## etc_uninstallFilter

> Sample Data

```cli
{
  "filter_id": "0xcb4a28c9cec1b3dde618f07a75c83019"
}
```
Uninstalls a filter with given id. Should always be called when watch is no longer needed. Additonally filters timeout when they aren’t requested with [etc_getFilterChanges](#etc_getfilterchanges) for a period of time.


### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '["0xcb4a28c9cec1b3dde618f07a75c83019"]' https://api.oracleminer.com/xrs/etc_uninstallFilter
```

```plaintext
blocknet-cli xrService etc_uninstallFilter 0xcb4a28c9cec1b3dde618f07a75c83019
```
<code class="api-call">etc_uninstallFilter [filter_id]</code>

Parameter       | Type       | Description
----------------|------------|-------------
filter_id       | string     | Filter id.


### Response Parameters

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
true
```

```plaintext
{
  "reply": true,
  "uuid": "D7C9B5EA-2C7B-4FA4-9C8A-6EF3CB94316C"
}
```

Parameter            | Type          | Description
---------------------|---------------|-------------
reply                | boolean       | `true` if the filter was successfully uninstalled, otherwise `false`.
jsonrpc              | string        | JSON RPC version.
id                   | int           | ID number.
uuid                 | string        | The response ID, which can be used to view this response again with [xrGetReply](https://api.blocknet.co/#xrgetreply).





## etc_unsubscribe

> Sample Data

```cli
{
  "subscription_id": "0xb53c4832f1dca4a5"
}
```
Unsubscribes from a subscription.


### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '["0xb53c4832f1dca4a5"]' https://api.oracleminer.com/xrs/etc_unsubscribe
```

```plaintext
blocknet-cli xrService etc_unsubscribe 0xb53c4832f1dca4a5
```
<code class="api-call">etc_unsubscribe [subscription_id]</code>

Parameter       | Type       | Description
----------------|------------|-------------
subscription_id | string     | Subscription id.


### Response Parameters

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
true
```

```plaintext
{
  "reply": true,
  "uuid": "B9DBCB02-9D64-474A-85EF-0C155EDB3E95"
}
```

Parameter            | Type          | Description
---------------------|---------------|-------------
reply                | boolean       | `true` if the subscription was cancelled, otherwise `false`.
jsonrpc              | string        | JSON RPC version.
id                   | int           | ID number.
uuid                 | string        | The response ID, which can be used to view this response again with [xrGetReply](https://api.blocknet.co/#xrgetreply).





## etc_net_listening

Returns `true` if client is actively listening for network connections.

### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '[]' https://api.oracleminer.com/xrs/etc_net_listening
```

```plaintext
blocknet-cli xrService etc_net_listening
```
<code class="api-call">etc_net_listening</code>

This call does not take parameters.


### Response

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
true
```

```plaintext
{
  "reply": true,
  "uuid": "7123F256-AFAB-46EB-B11E-71A211ACA11F"
}
```

Parameter            | Type          | Description
---------------------|---------------|-------------
reply                | boolean       | `true` when listening, otherwise `false`.
jsonrpc              | string        | JSON RPC version.
id                   | int           | ID number.
uuid                 | string        | The response ID, which can be used to view this response again with [xrGetReply](https://api.blocknet.co/#xrgetreply).





## etc_net_peerCount

Returns number of peers currenly connected to the client.

### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '[]' https://api.oracleminer.com/xrs/etc_net_peerCount
```

```plaintext
blocknet-cli xrService etc_net_peerCount
```
<code class="api-call">etc_net_peerCount</code>

This call does not take parameters.


### Response

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
0x53
```

```plaintext
{
  "reply": "0x53",
  "uuid": "DD64201E-708A-4B7F-A28F-7879264CA3BE"
}
```

Parameter            | Type          | Description
---------------------|---------------|-------------
reply                | string        | Integer of the number of connected peers.
jsonrpc              | string        | JSON RPC version.
id                   | int           | ID number.
uuid                 | string        | The response ID, which can be used to view this response again with [xrGetReply](https://api.blocknet.co/#xrgetreply).





## etc_net_version

Returns the current network protocol version.

### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '[]' https://api.oracleminer.com/xrs/etc_net_version
```

```plaintext
blocknet-cli xrService etc_net_version
```
<code class="api-call">etc_net_version</code>

This call does not take parameters.


### Response

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
1
```

```plaintext
{
  "reply": 1,
  "uuid": "02704202-D77D-4A20-8E77-E1F20E149E7B"
}
```

Parameter            | Type          | Description
---------------------|---------------|-------------
reply                | string        | The current network protocol version.
jsonrpc              | string        | JSON RPC version.
id                   | int           | ID number.
uuid                 | string        | The response ID, which can be used to view this response again with [xrGetReply](https://api.blocknet.co/#xrgetreply).





## etc_web3_clientVersion

Returns the current client version.

### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '[]' https://api.oracleminer.com/xrs/etc_web3_clientVersion
```

```plaintext
blocknet-cli xrService etc_web3_clientVersion
```
<code class="api-call">etc_web3_clientVersion</code>

This call does not take parameters.


### Response

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
CoreGeth/v1.11.4-stable-478a00cd/linux-amd64/go1.14.3
```

```plaintext
{
  "reply": "CoreGeth/v1.11.4-stable-478a00cd/linux-amd64/go1.14.3",
  "uuid": "E42C5C90-B219-4973-B4EB-5BDCB1F15978"
}
```

Parameter            | Type          | Description
---------------------|---------------|-------------
reply                | string        | The current client version.
jsonrpc              | string        | JSON RPC version.
id                   | int           | ID number.
uuid                 | string        | The response ID, which can be used to view this response again with [xrGetReply](https://api.blocknet.co/#xrgetreply).





## etc_web3_sha3

> Sample Data

```cli
{
  "sha3_data": "0x68656c6c6f20776f726c64"
}
```
Returns Keccak-256 (not the standardized SHA3-256) of the given data.


### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '["0x68656c6c6f20776f726c64"]' https://api.oracleminer.com/xrs/etc_web3_sha3
```

```plaintext
blocknet-cli xrService etc_web3_sha3 0x68656c6c6f20776f726c64
```
<code class="api-call">etc_web3_sha3 [sha3_data]</code>

Parameter       | Type       | Description
----------------|------------|-------------
sha3_data       | string     | The data to convert into a SHA3 hash.


### Response Parameters

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
0x47173285a8d7341e5e972fc677286384f802f8ef42a5ec5f03bbfa254cb01fad
```

```plaintext
{
  "reply": "0x47173285a8d7341e5e972fc677286384f802f8ef42a5ec5f03bbfa254cb01fad",
  "uuid": "7A340C49-3A26-4145-928B-F2BF494B3D06"
}
```

Parameter            | Type          | Description
---------------------|---------------|-------------
reply                | string        | The Keccak-256 hash of the given string.
jsonrpc              | string        | JSON RPC version.
id                   | int           | ID number.
uuid                 | string        | The response ID, which can be used to view this response again with [xrGetReply](https://api.blocknet.co/#xrgetreply).