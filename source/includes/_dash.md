# DASH

Call                                                                                | Description
------------------------------------------------------------------------------------|----------------------------------------------------------------------------------
[dash_getbestblockhash](#dash_getbestblockhash)                                       | Returns the hash of the best (tip) block in the longest blockchain.





## dash_getbestblockhash

Returns the hash of the best (tip) block in the longest blockchain.

### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '[]' https://api.oracleminer.com/xrs/dash_getbestblockhash
```

```plaintext
blocknet-cli xrService dash_getbestblockhash
```
<code class="api-call">dash_getbestblockhash</code>

This call does not take parameters.


### Response

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
0000000000000010c6fa35baf25373ddc11dafa3c8bfd6f18b4d443a7fee4b31
```

```plaintext
{
  "reply": "0000000000000010c6fa35baf25373ddc11dafa3c8bfd6f18b4d443a7fee4b31",
  "error": null,
  "id": 1,
  "uuid": "90918252-1FFD-49D7-8B4F-97E48E87F678"
}
```

Parameter      | Type          | Description
---------------|---------------|-------------
reply          | string        | The block hash hex encoded.
error          | string        | API error code.
id             | int           | ID number.
uuid           | string        | The response ID, which can be used to view this response again with [xrGetReply](https://api.blocknet.co/#xrgetreply).
