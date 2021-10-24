# Litecoin

Call                                                                                | Description
------------------------------------------------------------------------------------|----------------------------------------------------------------------------------
[ltc_getbestblockhash](#ltc_getbestblockhash)                                         | Returns the hash of the best (tip) block in the longest blockchain.





## ltc_getbestblockhash

Returns the hash of the best (tip) block in the longest blockchain.

### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '[]' https://api.oracleminer.com/xrs/ltc_getbestblockhash
```

```plaintext
blocknet-cli xrService ltc_getbestblockhash
```
<code class="api-call">ltc_getbestblockhash</code>

This call does not take parameters.


### Response

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
fca6ab6e4bbc6ce32966141642ed0d0d3321e221d977bb179701b7f9072deb9a
```

```plaintext
{
  "reply": "fca6ab6e4bbc6ce32966141642ed0d0d3321e221d977bb179701b7f9072deb9a",
  "error": null,
  "id": 1,
  "uuid": "1A242BB0-DFC5-4DFE-85C8-AD6B876BC959"
}
```

Parameter      | Type          | Description
---------------|---------------|-------------
reply          | string        | The block hash hex encoded.
error          | string        | API error code.
id             | int           | ID number.
uuid           | string        | The response ID, which can be used to view this response again with [xrGetReply](https://api.blocknet.co/#xrgetreply).
