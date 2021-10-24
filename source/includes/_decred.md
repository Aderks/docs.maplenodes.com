# Decred

Call                                                                                | Description
------------------------------------------------------------------------------------|----------------------------------------------------------------------------------
[dcr_getbestblockhash](#dcr_getbestblockhash)                                         | Returns the hash of the best (tip) block in the longest blockchain.





## dcr_getbestblockhash

Returns the hash of the best (tip) block in the longest blockchain.

### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '[]' https://api.oracleminer.com/xrs/dcr_getbestblockhash
```

```plaintext
blocknet-cli xrService dcr_getbestblockhash
```
<code class="api-call">dcr_getbestblockhash</code>

This call does not take parameters.


### Response

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
00000000000000002123c8ce58f48cef57e6f6bf7bdb2ba613b3f0139cf0399d
```

```plaintext
{
  "reply": "00000000000000002123c8ce58f48cef57e6f6bf7bdb2ba613b3f0139cf0399d",
  "jsonrpc": "1.0",
  "error": null,
  "id": 1,
  "uuid": "6891CE9C-E321-46E4-B6E1-224BD5A5301C"
}
```

Parameter      | Type          | Description
---------------|---------------|-------------
reply          | string        | The block hash hex encoded.
jsonrpc        | int           | JSON RPC version.
error          | string        | API error code.
id             | int           | ID number.
uuid           | string        | The response ID, which can be used to view this response again with [xrGetReply](https://api.blocknet.co/#xrgetreply).
