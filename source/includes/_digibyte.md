# Digibyte

Call                                                                                | Description
------------------------------------------------------------------------------------|----------------------------------------------------------------------------------
[dgb_getbestblockhash](#dgb_getbestblockhash)                                         | Returns the hash of the best (tip) block in the longest blockchain.





## dgb_getbestblockhash

Returns the hash of the best (tip) block in the longest blockchain.

### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '[]' https://api.oracleminer.com/xrs/dgb_getbestblockhash
```

```plaintext
blocknet-cli xrService dgb_getbestblockhash
```
<code class="api-call">dgb_getbestblockhash</code>

This call does not take parameters.


### Response

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
2c69b7b743ad47768aee4943b1b0f0821087173f984bacca9d238c8a67e7128c
```

```plaintext
{
  "reply": "2c69b7b743ad47768aee4943b1b0f0821087173f984bacca9d238c8a67e7128c",
  "error": null,
  "id": 1,
  "uuid": "F92D11E6-4CFC-4043-A0A2-58BE4C1FFA73"
}
```

Parameter      | Type          | Description
---------------|---------------|-------------
reply          | string        | The block hash hex encoded.
error          | string        | API error code.
id             | int           | ID number.
uuid           | string        | The response ID, which can be used to view this response again with [xrGetReply](https://api.blocknet.co/#xrgetreply).
