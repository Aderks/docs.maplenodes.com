# Horizen

Call                                                                                | Description
------------------------------------------------------------------------------------|----------------------------------------------------------------------------------
[zen_getbestblockhash](#zen_getbestblockhash)                                         | Returns the hash of the best (tip) block in the longest blockchain.





## zen_getbestblockhash

Returns the hash of the best (tip) block in the longest blockchain.

### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '[]' https://api.oracleminer.com/xrs/zen_getbestblockhash
```

```plaintext
blocknet-cli xrService zen_getbestblockhash
```
<code class="api-call">zen_getbestblockhash</code>

This call does not take parameters.


### Response

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
00000000038da97de3af385e83af6376bd1275075e5c7ea14f0278db286af2d2
```

```plaintext
{
  "reply": "00000000038da97de3af385e83af6376bd1275075e5c7ea14f0278db286af2d2",
  "error": null,
  "id": 1,
  "uuid": "6102E957-7490-49AC-A002-A5D5DC700B64"
}
```

Parameter      | Type          | Description
---------------|---------------|-------------
reply          | string        | The block hash hex encoded.
error          | string        | API error code.
id             | int           | ID number.
uuid           | string        | The response ID, which can be used to view this response again with [xrGetReply](https://api.blocknet.co/#xrgetreply).
