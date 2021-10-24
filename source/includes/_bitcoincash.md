# BitcoinCash

Call                                                                                | Description
------------------------------------------------------------------------------------|----------------------------------------------------------------------------------
[bch_getbestblockhash](#bch_getbestblockhash)                                         | Returns the hash of the best (tip) block in the longest blockchain.





## bch_getbestblockhash

Returns the hash of the best (tip) block in the longest blockchain.

### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '[]' https://api.oracleminer.com/xrs/bch_getbestblockhash
```

```plaintext
blocknet-cli xrService bch_getbestblockhash
```
<code class="api-call">bch_getbestblockhash</code>

This call does not take parameters.


### Response

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
0000000000000000022112799fd96c6a310af1ccdf7e8de698a384e6675f3aa0
```

```plaintext
{
  "reply": "0000000000000000022112799fd96c6a310af1ccdf7e8de698a384e6675f3aa0",
  "error": null,
  "id": 1,
  "uuid": "013E3DB2-1827-4318-87F1-D36164CFED96"
}
```

Parameter      | Type          | Description
---------------|---------------|-------------
reply          | string        | The block hash hex encoded.
error          | string        | API error code.
id             | int           | ID number.
uuid           | string        | The response ID, which can be used to view this response again with [xrGetReply](https://api.blocknet.co/#xrgetreply).
