# Bitcoin

Call                                                                                | Description
------------------------------------------------------------------------------------|----------------------------------------------------------------------------------
[btc_getbestblockhash](#btc_getbestblockhash)                                         | Returns the hash of the best (tip) block in the longest blockchain.
[btc_getdifficulty](#btc_getdifficulty)                                               | Returns the proof-of-work difficulty as a multiple of the minimum difficulty.
[btc_getmempoolinfo](#btc_getmempoolinfo)                                             | Returns details on the active state of the TX memory pool.
[btc_getrawmempool](#btc_getrawmempool)                                               | Returns all transaction ids in memory pool as a json array of string transaction ids.





## btc_getbestblockhash

Returns the hash of the best (tip) block in the longest blockchain.

### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '[]' https://api.oracleminer.com/xrs/btc_getbestblockhash
```

```plaintext
blocknet-cli xrService btc_getbestblockhash
```
<code class="api-call">btc_getbestblockhash</code>

This call does not take parameters.


### Response

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
000000000000000000005d80d86f215d33c0a40431995b34a70b99e10c051b66
```

```plaintext
{
  "reply": "000000000000000000005d80d86f215d33c0a40431995b34a70b99e10c051b66",
  "error": null,
  "id": 1,
  "uuid": "26617438-8E55-47A0-BF56-AD0BA3F3B07D"
}
```

Parameter      | Type          | Description
---------------|---------------|-------------
reply          | string        | The block hash hex encoded.
error          | string        | API error code.
id             | int           | ID number.
uuid           | string        | The response ID, which can be used to view this response again with [xrGetReply](https://api.blocknet.co/#xrgetreply).





## btc_getdifficulty

Returns the proof-of-work difficulty as a multiple of the minimum difficulty.

### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '[]' https://api.oracleminer.com/xrs/btc_getdifficulty
```

```plaintext
blocknet-cli xrService btc_getdifficulty
```
<code class="api-call">btc_getdifficulty</code>

This call does not take parameters.


### Response

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
12948593420946.38085938
```

```plaintext
{
  "reply": 12948593420946.38085938,
  "error": null,
  "id": 1,
  "uuid": "5F6189F0-F967-4ABA-8EF5-4F29815C20F6"
}
```

Parameter      | Type          | Description
---------------|---------------|-------------
reply          | int           | The proof-of-work difficulty as a multiple of the minimum difficulty.
error          | string        | API error code.
id             | int           | ID number.
uuid           | string        | The response ID, which can be used to view this response again with [xrGetReply](https://api.blocknet.co/#xrgetreply).





## btc_getmempoolinfo

Returns details on the active state of the TX memory pool.

### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '[]' https://api.oracleminer.com/xrs/btc_getmempoolinfo
```

```plaintext
blocknet-cli xrService btc_getmempoolinfo
```
<code class="api-call">btc_getmempoolinfo</code>

This call does not take parameters.


### Response

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
{
  "size": 14558,
  "bytes": 9808191,
  "usage": 35145408,
  "maxmempool": 300000000,
  "mempoolminfee": 1e-05,
  "minrelaytxfee": 1e-05
}
```

```plaintext
{
  "reply": {
    "size": 2617,
    "bytes": 839397,
    "usage": 3985568,
    "maxmempool": 300000000,
    "mempoolminfee": 0.00001000,
    "minrelaytxfee": 0.00001000
  },
  "error": null,
  "id": 1,
  "uuid": "65E0A3B8-4331-4A3B-ABC6-ACC95469149D"
}
```

Parameter      | Type          | Description
---------------|---------------|-------------
size           | int           | Current tx count.
bytes          | int           | Sum of all virtual transaction sizes as defined in BIP 141. Differs from actual serialized size because witness data is discounted.
usage          | int           | Total memory usage for the mempool.
maxmempool     | int           | Maximum memory usage for the mempool.
mempoolminfee  | int           | Minimum fee rate in BTC/kB for tx to be accepted. Is the maximum of minrelaytxfee and minimum mempool fee.
minrelaytxfee  | int           | Current minimum relay fee for transactions.
error          | string        | API error code.
id             | int           | ID number.
uuid           | string        | The response ID, which can be used to view this response again with [xrGetReply](https://api.blocknet.co/#xrgetreply).





## btc_getrawmempool

Returns all transaction ids in memory pool as a json array of string transaction ids.

### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '[]' https://api.oracleminer.com/xrs/btc_getrawmempool
```

```plaintext
blocknet-cli xrService btc_getrawmempool
```
<code class="api-call">btc_getrawmempool</code>

This call does not take parameters.


### Response

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
[
    "17ba38d8eb3222326e39f35e41e6abeceb565af6a8493f7cf4b3ed02b52d5b7d",
    "cb41bdddde68716e0525ca113674edad61a2390ecf308e893771155566b2f10a",
    "a5d9ecbbf5b831d86f9833318e5aad3550a685085937cfafb6c3d1e68d49ecb0",
    "e5e244de37a8c7f6df1a666d0423f3d33d34cde514a7d07edfc63f5512385ab1",
    "91935682ec8fc0e09bc57df7d97781c7bb9c3332a187d13e1a05afa42bdbb4ae",
    "c9457944824c87b6cbc5ffd3bb93b5e0c4ce0b3d897d480e11043d13c20ba078",
    "61a08e39d8fae46aa4317b442956669ca10cbd6c402769f6cbec0e74824bf455",
    "8e635215167e68b43629c230716cb606dfe80cb1a9b6fac242cc21eff706a874",
    "eea9e333a54b35d384a467a3cc5d3740e6e3ced88fa892bf020cc25a0b1c16ff",
    "03e8d1556632e966fbbb91dd0ae1e7706f421a9dc537e0545f93ebee0522bbb7",
    "66822976ec0a26eab0b1badacec7c3532824acd8837d39b4379de973a6093159",
    "56ee70f2b05039ea958218ed025a0416b52a0656f16256381d0327966d089495",
    "e88a3a9ed3abae3edcc0bc523189942f8804665ddece81772d9853c1fc8ad951",
    "3570eb312f63f4d48b0e187c41d3d9a652225d72baee938050311d09ddc40fe2",
    "d266331fb70854b006903b16ab4682a655709264dfc248a46b40fb23bdb78c68",
    "f0e8aad1579d2cfb986783e4fbd8f1bf94c0f9fee4d4b5eb8090c2b27b283d2c",
    "891a7f0e015af8b7834edc9ecb2f30ebf7a6df412014563961d462b9d482e122",
    "cf931eb303ede6250ab3a842e2c24dbe525b692a8111748bec9fe6d2f4c98903",
    "5c51a7e9415ad62e68b230b5994ce22941f80f3cd135983333a9cda2f0d2b179",
    "e017794d3886c69a6778ab29755deb9068b49921b0a24a5979402c3bd23d644a",
    "36baa7ceb9e7aae0cfe5909b7314fc3e641cb1c0d229024caff8f7584f348363",
    "05e922e1d706f2fbf06710656d4651e155b9e18ecc7cfe3bbe327968702a6c95",
    "e971f414940e81fd641f1574a5978198d04f1906298e14232c531f068ad4a2c0",
    "f235bc10ea18c1ef46e013cfefc3eec21119119089f11d994e69957dc8b4feea",
    "89bcd7150f189cfe4fc0e15b5cd00cbfa217574d46f8b3c8b453976a0671235c",
    "e51384daf2cac8bcd33a2fe658bac237e022dcf330b4ffe9c8c7ffe7ec247e8e",
    "da7ee51ee7e31209b532de27998ff43f28d97689e97482efbf1f4e284978a944",
    "eeca6311fb89d6c9269d467d56c4bd6ece7d7e07cf7f11483af5c2d8f2d4cc06",
    "efa548b20fbe2d3e7b100ef1d378cb5598841a4f8cf8565364270cbc9d370eda",
    "d47af92fe2cb5c07ac9f7400fbd7b0e8cb36ff248dea17c4fa607c80e667ae9f",
    "3f04d056acd80c42fc61f439b14be1fa2cf4615b61120ee86a386a16e06bc09b",
    "cef2f27ecd74e9d8b7cf5ed5766aab23bbfbc5b4a73a7bd02ddd1e736a44fccd",
    "884f712c1397460a9559d9b9d775927149d80eb19ee13eee7f44698f31464b1d",
    "1012b50fb7f1806077608581d9990b7eadfdcc5ec407d9c9e001a211a1f343f3",
    "5031f7324cbad9cf7d657e84323d711e7767e2a688491981f8ab374469299dbc",
    "52c94a511b09ae36e3cf91ca6b3718d43a60d992b4ae7abd037395cad6c88899",
    "81c01a51a8002faf5dac63f6cf72cfd069a71a1cfb6fd51bde3c9f3a14096841",
    "4c10b27af95cfa81b06c58517a95549cafdf6d50ee70edc4cf102060355927b0",
    "c2b5f2b0e495c630e02cfac78aae40f697d848fef1c82e976e398c40e435fa87",
    "62087c7e8cd3b7a6f26ecd513806242e83761905c146d596e1490be7ab68cd3d",
    "9fb778d84d9eac7cf40a2f27dd1f0e341b348ea8e2fb8e576bfe1825ca3ec10e",
    "05dd3a3a7c54bd680f88d637cf6a74482974eb8146353575a303536268a20126",
    "924c47948ec263dbebe05c01ab005f250156a7f32e65a5d2901d5bb2563b6023",
    "ab922b9fa56355297bf7d1d8b0a59e106cab4050895544d0139233ea35ca8216",
    "e5fe44405aa1543ec1f86231e1fe95695dec11f76e2b2487c3d0326df7d93002",
    "22016af02f47948e6558ceedb6c7c5b628dc7b82130405af184f950e34ad4aea",
    "d0008e7d60f24b9327fd11b90814e1057915a269e219e2f6af70910bf8f5dce6",
    "f34e2d00af6fc4cb4a9d34cf2dadbf0b391deb1c41285c22495825134daea01a",
    "65dfa11b615845b06be60e3d4c61b2cf8ab79cd851519817efced0f719bd119e",
    "bd181f1687ab187d32765c21f361714e1eab495e63121485b8cd1568d2b3d6e1",
    "3e888e4a1cfedd9f2b37ebf4589e2b619a588017f837c43b078151c8dc208736",
    "76c74e76ab617bc16f1196c4a294217bfa2da0384380e57119045ad219134420",
    "c06bce9f78ed5c1e04e318e4e352281a627a3883242f4141b420ee31717c01ff",
    "4c476e00810d7be1113bef4e65c24b73fe2220828e6dd60ceafa8cee7866665d",
    "80484d277614bda83beebbffde8ba5dd00cd1d706ce661d1e1c13ed2d02a8a7f",
    "2667a2d2ae05689d7bbb07ddf3d3b1f3c8748262e886e5903a7a69b51f02b138",
    "674ece416c56e28af1785fe38960b83fdc6da0995d246d963495b89affad7f4b",
    "392f61c9fb698a33515fea27dc27a5ad0636cf40c26b832ac90b74f9970f70d6",
    "6f2294a3f79ee1f9f2618a83b55cc0ff4abd2a1b7b101e562f5ed9d417e1a054",
    "1b62ac4b8ac98e5511330531ea7ed805a4439d7d986ddb688e09589c5907be75",
    "492e228643904d97c69e522392bae4df62f6d0e6faf471f52feeca2e6a96924a",
    "ba0dae5db8afeacec72a776613ab3ce9d7cc2fff597a84f4d2063334a30fd451",
    "1cd27be911c9ea918571fc45b68139fc8d86e9e76f62d316422d0e0142e3a3c0",
    "2fa4f25a1c75b2bbcfa5985f3a6c754a5450635afab74f04d360c57e91bfd27a",
    "fe169b3f254f739a40b12c73dd7779fd26453442c6c78ab4e2774d3a60d4b916",
    "9f9f0ea0ec9d9decef632b9ff4d6897e6855db50b88277eef3ae955664f83521",
    "591ec66e0f9e8a60e61644de8dac15a957308425bd108e961b86bce7c8c851f0",
    "4de7fbc04ad91bf32b55c4c55e019c91a373715e4f87d4421dbf12102b25e5e2",
    "bcfb3e4b69242ede0bedd4aa7eb620a283617086c3c7ec4246f0c4cb0ffa04e2",
    "d87ee599a10a066e10fa1937e90bd799ce81b64dccde73b2c026d0205462dcd9",
    "f64b5a69697ebf6a043e41d7b6ee7ed0cdc76dd57b3b0898e5a9658cadcf54be",
    "5f9a58ea5bb1179985495cee6c84f4ec38ba1e55930f054abbb340097c31b7b8",
    "46a9025cfcb7c9858f05bdc2a93dd901388acc23d2f0b81c23e0895370fc57af",
    "561c69384a093ab0d442801ea10e3e466ba0593eed3c40591ef222e6671891a6",
    "04bfb226a878f7740b03d76fc3a78229d5544077ab7473ade33cb2037f88de9e",
    "b4313fc3c4ad841e8559b15c8c4e7029188eacb080f29b5b52612efc000a3a8f",
    "510561137c6672b551252b5fe37be88ea9fcfaf66da7fd91c5dd9ccc3515a269",
    "4a9d01481a8b614f3a76a43fa7989c8eaf4828a6e66e44b6b36697e63aab9366",
    "bb71c7acaa1a5a95cf51ee0c219e2f531ceea6c1201ad502bbfe9c6bd49fc848",
    "22fe05bc2e3194d619ba3663601b3943fba90ee5a04bdc08865531bb1ca95a0b",
    "525e5ad00823774babeabebfac4b184ae2fac31667e6171f7b35b3b2b5ecd701",
    "b3e4404c0ee27b71f6d5de095b181f57401c886a07b9d9bee21fb36b844c562b",
    "1b0574dd79050f9f13556009036cf86568182603756965865a25c5ef9dfe29eb",
    "46c831c4e8d9e0e3b007ee77887c0466a3db07d20ac8b1b563eeeae0ceeb7868",
    "0a4b79bad64c943d0356a187861072b133c09696e4593adc230a7bd919735a68",
    "12d17f6650b91d45b64e05d855232cf659c6d4c5c80abeaef51c75f07f67983c",
    "b518455e8eb6b59802616ef1f3fe8efdefafc3d285aeec2a515cc5cc7e991c1f",
    "5fd17d6975fc74ffb0afcd8e8db2d85432127e101eebff9a6652147e9cd41901",
    "430db060347ce6a0bd53549559163518a5957b5c119b80f3f6d5143a915c1e00",
    "73f526b378fa97d15a7298c9decb8167206a0b9cd0a69182dadcc59ba5ea12c3",
    "c82426f035a975376de0105f99f1c8975a96e271bd8afc5faba2cdb341c1e72d",
    "7bb92709a32da0dd1e305340f04ae64cedc0f7649d229b13a27fabf232b84109",
    "cc862813adc069016951c6ddfb28c139e61f6910dcd3e99eeed7ef0c18b16b56",
    "f2e3fc64365eebef7e78ccbfe33cf4f07fd80012990c304e2b9195aa0e0bbf91",
    "29c2079b27454b30aaba3117024110f553eb70d842fd9f445811849fa10cd747",
    "34890a32e62000feb00ffb783aa82d90b3f1e1be7e38e5c57419127f8e1d1527",
    "453bb778d2efbdc7b1899e4a9d6e307bfba839e44b89f7acb386a7979a5fed49",
    "a95169c10f697f81495b4a667f8e9bbac0b066c55bdb9a5b7474d272202d8bb4",
    "3e7cf469321445a61196b98624821716a89e17c61b3d46b36085dc12a1cd6128",
    "3b7e4a36556c9940d2eb040b50190dcadc10920aca341382e173a30a3f47e2c7",
    "0eb65c579e520fe84c93d3d94fccbfb264703072b4c2961114e1db55c81ba8ac",
    "0885f2f55739b65549dd9ac65d0779c3bf7b7351900472f771ebc257b0adb1a0",
    "d2b9c30b28f6aa95c875f1e4367df78ed0c17fc597ff694a9e958bf16f7b0f3b",
    "8babb8f47d9aae3e64a54ae4388bc049857337098c778152f57585db0badee5a",
    "ce6615056fba391874e1f9b6309cba20df8a71af01d5f3b94d0bd033a6647e98",
    "565506af163ac7432b4c5117a771dbbe825ff49cbabbff87063c9d0cf8ef8aa0",
    "0036c0c6133b182caed1904c699d5aeb5038b1d6beea803e4a36d92772f68fd9",
    "67fa1b16e0701dee7c05b926c1651573cea6b31a39d51c82e9eff78b4346ac17",
    "09ab2d35e6b877bde17754a97fa4c70d66b10f6ddf08d69eafc6e75113d2ffd3",
    "c2255383fde8c3a052139e6d74383f49c95fee7b152b2547392187a1d98fe55b",
    "bf44af55702020dc284a72ac22b9be646e9ebbafa4f70a9ce7a23b8bb7d9c3a7",
    "e06f747a6364da16a640a13ddd01240927cd21c631bbf9210ccfd5bb75088558",
    "b1bcb7c4f0c8ee3213fc0dc612e5c8a7af37ee1bccfac6ed5726bac2bc37270c",
    "7c1fb8d023b89eac3197086ebd25e5e09730a9cfdcfdf25c292f840b6c09425d",
    "ca9b5e17e8670635676864b0f341878dab82b847f51b3ba170263565a454e09e",
    "a38f0f3a63c1e99f0acef185a214313543d4c771540a8144fbed944a23432b90",
    "1ee17aaee6ca7bd218146f7969602f92b0ba8693dfbff0a51025dde5aa9b237b",
    "21b1a5b2cbad022c6b4f046102cba72343bf31bd0ca62f0452c91776954995a8",
    "9aa89ec792d0c005600fb9f5444f509b342711ebff2a208eea57c7e65f5951de",
    "39b3f08f90071d94587a1fcb0275a369a71617772689dece55f9c775124a6cd0",
    "6e5a8e064aaba19a7c9e9862314a952e92d2a3eff3c78770746776635c359f69",
    "c63375bc6ddd34cd4731fc142843c84b64f99ffb2bdeb69f4f9f86418fdb3cac",
    "dbae3ea4094f7ea71131c9b5d460d31070089d06a99d125c827044fcdf6e0528",
    "..."
]
```

```plaintext
{
  "reply": [
    "17ba38d8eb3222326e39f35e41e6abeceb565af6a8493f7cf4b3ed02b52d5b7d",
    "cb41bdddde68716e0525ca113674edad61a2390ecf308e893771155566b2f10a",
    "a5d9ecbbf5b831d86f9833318e5aad3550a685085937cfafb6c3d1e68d49ecb0",
    "e5e244de37a8c7f6df1a666d0423f3d33d34cde514a7d07edfc63f5512385ab1",
    "91935682ec8fc0e09bc57df7d97781c7bb9c3332a187d13e1a05afa42bdbb4ae",
    "c9457944824c87b6cbc5ffd3bb93b5e0c4ce0b3d897d480e11043d13c20ba078",
    "61a08e39d8fae46aa4317b442956669ca10cbd6c402769f6cbec0e74824bf455",
    "8e635215167e68b43629c230716cb606dfe80cb1a9b6fac242cc21eff706a874",
    "eea9e333a54b35d384a467a3cc5d3740e6e3ced88fa892bf020cc25a0b1c16ff",
    "03e8d1556632e966fbbb91dd0ae1e7706f421a9dc537e0545f93ebee0522bbb7",
    "66822976ec0a26eab0b1badacec7c3532824acd8837d39b4379de973a6093159",
    "56ee70f2b05039ea958218ed025a0416b52a0656f16256381d0327966d089495",
    "e88a3a9ed3abae3edcc0bc523189942f8804665ddece81772d9853c1fc8ad951",
    "3570eb312f63f4d48b0e187c41d3d9a652225d72baee938050311d09ddc40fe2",
    "d266331fb70854b006903b16ab4682a655709264dfc248a46b40fb23bdb78c68",
    "f0e8aad1579d2cfb986783e4fbd8f1bf94c0f9fee4d4b5eb8090c2b27b283d2c",
    "891a7f0e015af8b7834edc9ecb2f30ebf7a6df412014563961d462b9d482e122",
    "cf931eb303ede6250ab3a842e2c24dbe525b692a8111748bec9fe6d2f4c98903",
    "5c51a7e9415ad62e68b230b5994ce22941f80f3cd135983333a9cda2f0d2b179",
    "e017794d3886c69a6778ab29755deb9068b49921b0a24a5979402c3bd23d644a",
    "36baa7ceb9e7aae0cfe5909b7314fc3e641cb1c0d229024caff8f7584f348363",
    "05e922e1d706f2fbf06710656d4651e155b9e18ecc7cfe3bbe327968702a6c95",
    "e971f414940e81fd641f1574a5978198d04f1906298e14232c531f068ad4a2c0",
    "f235bc10ea18c1ef46e013cfefc3eec21119119089f11d994e69957dc8b4feea",
    "89bcd7150f189cfe4fc0e15b5cd00cbfa217574d46f8b3c8b453976a0671235c",
    "e51384daf2cac8bcd33a2fe658bac237e022dcf330b4ffe9c8c7ffe7ec247e8e",
    "da7ee51ee7e31209b532de27998ff43f28d97689e97482efbf1f4e284978a944",
    "eeca6311fb89d6c9269d467d56c4bd6ece7d7e07cf7f11483af5c2d8f2d4cc06",
    "efa548b20fbe2d3e7b100ef1d378cb5598841a4f8cf8565364270cbc9d370eda",
    "d47af92fe2cb5c07ac9f7400fbd7b0e8cb36ff248dea17c4fa607c80e667ae9f",
    "3f04d056acd80c42fc61f439b14be1fa2cf4615b61120ee86a386a16e06bc09b",
    "cef2f27ecd74e9d8b7cf5ed5766aab23bbfbc5b4a73a7bd02ddd1e736a44fccd",
    "884f712c1397460a9559d9b9d775927149d80eb19ee13eee7f44698f31464b1d",
    "1012b50fb7f1806077608581d9990b7eadfdcc5ec407d9c9e001a211a1f343f3",
    "5031f7324cbad9cf7d657e84323d711e7767e2a688491981f8ab374469299dbc",
    "52c94a511b09ae36e3cf91ca6b3718d43a60d992b4ae7abd037395cad6c88899",
    "81c01a51a8002faf5dac63f6cf72cfd069a71a1cfb6fd51bde3c9f3a14096841",
    "4c10b27af95cfa81b06c58517a95549cafdf6d50ee70edc4cf102060355927b0",
    "c2b5f2b0e495c630e02cfac78aae40f697d848fef1c82e976e398c40e435fa87",
    "62087c7e8cd3b7a6f26ecd513806242e83761905c146d596e1490be7ab68cd3d",
    "9fb778d84d9eac7cf40a2f27dd1f0e341b348ea8e2fb8e576bfe1825ca3ec10e",
    "05dd3a3a7c54bd680f88d637cf6a74482974eb8146353575a303536268a20126",
    "924c47948ec263dbebe05c01ab005f250156a7f32e65a5d2901d5bb2563b6023",
    "ab922b9fa56355297bf7d1d8b0a59e106cab4050895544d0139233ea35ca8216",
    "e5fe44405aa1543ec1f86231e1fe95695dec11f76e2b2487c3d0326df7d93002",
    "22016af02f47948e6558ceedb6c7c5b628dc7b82130405af184f950e34ad4aea",
    "d0008e7d60f24b9327fd11b90814e1057915a269e219e2f6af70910bf8f5dce6",
    "f34e2d00af6fc4cb4a9d34cf2dadbf0b391deb1c41285c22495825134daea01a",
    "65dfa11b615845b06be60e3d4c61b2cf8ab79cd851519817efced0f719bd119e",
    "bd181f1687ab187d32765c21f361714e1eab495e63121485b8cd1568d2b3d6e1",
    "3e888e4a1cfedd9f2b37ebf4589e2b619a588017f837c43b078151c8dc208736",
    "76c74e76ab617bc16f1196c4a294217bfa2da0384380e57119045ad219134420",
    "c06bce9f78ed5c1e04e318e4e352281a627a3883242f4141b420ee31717c01ff",
    "4c476e00810d7be1113bef4e65c24b73fe2220828e6dd60ceafa8cee7866665d",
    "80484d277614bda83beebbffde8ba5dd00cd1d706ce661d1e1c13ed2d02a8a7f",
    "2667a2d2ae05689d7bbb07ddf3d3b1f3c8748262e886e5903a7a69b51f02b138",
    "674ece416c56e28af1785fe38960b83fdc6da0995d246d963495b89affad7f4b",
    "392f61c9fb698a33515fea27dc27a5ad0636cf40c26b832ac90b74f9970f70d6",
    "6f2294a3f79ee1f9f2618a83b55cc0ff4abd2a1b7b101e562f5ed9d417e1a054",
    "1b62ac4b8ac98e5511330531ea7ed805a4439d7d986ddb688e09589c5907be75",
    "492e228643904d97c69e522392bae4df62f6d0e6faf471f52feeca2e6a96924a",
    "ba0dae5db8afeacec72a776613ab3ce9d7cc2fff597a84f4d2063334a30fd451",
    "1cd27be911c9ea918571fc45b68139fc8d86e9e76f62d316422d0e0142e3a3c0",
    "2fa4f25a1c75b2bbcfa5985f3a6c754a5450635afab74f04d360c57e91bfd27a",
    "fe169b3f254f739a40b12c73dd7779fd26453442c6c78ab4e2774d3a60d4b916",
    "9f9f0ea0ec9d9decef632b9ff4d6897e6855db50b88277eef3ae955664f83521",
    "591ec66e0f9e8a60e61644de8dac15a957308425bd108e961b86bce7c8c851f0",
    "4de7fbc04ad91bf32b55c4c55e019c91a373715e4f87d4421dbf12102b25e5e2",
    "bcfb3e4b69242ede0bedd4aa7eb620a283617086c3c7ec4246f0c4cb0ffa04e2",
    "d87ee599a10a066e10fa1937e90bd799ce81b64dccde73b2c026d0205462dcd9",
    "f64b5a69697ebf6a043e41d7b6ee7ed0cdc76dd57b3b0898e5a9658cadcf54be",
    "5f9a58ea5bb1179985495cee6c84f4ec38ba1e55930f054abbb340097c31b7b8",
    "46a9025cfcb7c9858f05bdc2a93dd901388acc23d2f0b81c23e0895370fc57af",
    "561c69384a093ab0d442801ea10e3e466ba0593eed3c40591ef222e6671891a6",
    "04bfb226a878f7740b03d76fc3a78229d5544077ab7473ade33cb2037f88de9e",
    "b4313fc3c4ad841e8559b15c8c4e7029188eacb080f29b5b52612efc000a3a8f",
    "510561137c6672b551252b5fe37be88ea9fcfaf66da7fd91c5dd9ccc3515a269",
    "4a9d01481a8b614f3a76a43fa7989c8eaf4828a6e66e44b6b36697e63aab9366",
    "bb71c7acaa1a5a95cf51ee0c219e2f531ceea6c1201ad502bbfe9c6bd49fc848",
    "22fe05bc2e3194d619ba3663601b3943fba90ee5a04bdc08865531bb1ca95a0b",
    "525e5ad00823774babeabebfac4b184ae2fac31667e6171f7b35b3b2b5ecd701",
    "b3e4404c0ee27b71f6d5de095b181f57401c886a07b9d9bee21fb36b844c562b",
    "1b0574dd79050f9f13556009036cf86568182603756965865a25c5ef9dfe29eb",
    "46c831c4e8d9e0e3b007ee77887c0466a3db07d20ac8b1b563eeeae0ceeb7868",
    "0a4b79bad64c943d0356a187861072b133c09696e4593adc230a7bd919735a68",
    "12d17f6650b91d45b64e05d855232cf659c6d4c5c80abeaef51c75f07f67983c",
    "b518455e8eb6b59802616ef1f3fe8efdefafc3d285aeec2a515cc5cc7e991c1f",
    "5fd17d6975fc74ffb0afcd8e8db2d85432127e101eebff9a6652147e9cd41901",
    "430db060347ce6a0bd53549559163518a5957b5c119b80f3f6d5143a915c1e00",
    "73f526b378fa97d15a7298c9decb8167206a0b9cd0a69182dadcc59ba5ea12c3",
    "c82426f035a975376de0105f99f1c8975a96e271bd8afc5faba2cdb341c1e72d",
    "7bb92709a32da0dd1e305340f04ae64cedc0f7649d229b13a27fabf232b84109",
    "cc862813adc069016951c6ddfb28c139e61f6910dcd3e99eeed7ef0c18b16b56",
    "f2e3fc64365eebef7e78ccbfe33cf4f07fd80012990c304e2b9195aa0e0bbf91",
    "29c2079b27454b30aaba3117024110f553eb70d842fd9f445811849fa10cd747",
    "34890a32e62000feb00ffb783aa82d90b3f1e1be7e38e5c57419127f8e1d1527",
    "453bb778d2efbdc7b1899e4a9d6e307bfba839e44b89f7acb386a7979a5fed49",
    "a95169c10f697f81495b4a667f8e9bbac0b066c55bdb9a5b7474d272202d8bb4",
    "3e7cf469321445a61196b98624821716a89e17c61b3d46b36085dc12a1cd6128",
    "3b7e4a36556c9940d2eb040b50190dcadc10920aca341382e173a30a3f47e2c7",
    "0eb65c579e520fe84c93d3d94fccbfb264703072b4c2961114e1db55c81ba8ac",
    "0885f2f55739b65549dd9ac65d0779c3bf7b7351900472f771ebc257b0adb1a0",
    "d2b9c30b28f6aa95c875f1e4367df78ed0c17fc597ff694a9e958bf16f7b0f3b",
    "8babb8f47d9aae3e64a54ae4388bc049857337098c778152f57585db0badee5a",
    "ce6615056fba391874e1f9b6309cba20df8a71af01d5f3b94d0bd033a6647e98",
    "565506af163ac7432b4c5117a771dbbe825ff49cbabbff87063c9d0cf8ef8aa0",
    "0036c0c6133b182caed1904c699d5aeb5038b1d6beea803e4a36d92772f68fd9",
    "67fa1b16e0701dee7c05b926c1651573cea6b31a39d51c82e9eff78b4346ac17",
    "09ab2d35e6b877bde17754a97fa4c70d66b10f6ddf08d69eafc6e75113d2ffd3",
    "c2255383fde8c3a052139e6d74383f49c95fee7b152b2547392187a1d98fe55b",
    "bf44af55702020dc284a72ac22b9be646e9ebbafa4f70a9ce7a23b8bb7d9c3a7",
    "e06f747a6364da16a640a13ddd01240927cd21c631bbf9210ccfd5bb75088558",
    "b1bcb7c4f0c8ee3213fc0dc612e5c8a7af37ee1bccfac6ed5726bac2bc37270c",
    "7c1fb8d023b89eac3197086ebd25e5e09730a9cfdcfdf25c292f840b6c09425d",
    "ca9b5e17e8670635676864b0f341878dab82b847f51b3ba170263565a454e09e",
    "a38f0f3a63c1e99f0acef185a214313543d4c771540a8144fbed944a23432b90",
    "1ee17aaee6ca7bd218146f7969602f92b0ba8693dfbff0a51025dde5aa9b237b",
    "21b1a5b2cbad022c6b4f046102cba72343bf31bd0ca62f0452c91776954995a8",
    "9aa89ec792d0c005600fb9f5444f509b342711ebff2a208eea57c7e65f5951de",
    "39b3f08f90071d94587a1fcb0275a369a71617772689dece55f9c775124a6cd0",
    "6e5a8e064aaba19a7c9e9862314a952e92d2a3eff3c78770746776635c359f69",
    "c63375bc6ddd34cd4731fc142843c84b64f99ffb2bdeb69f4f9f86418fdb3cac",
    "dbae3ea4094f7ea71131c9b5d460d31070089d06a99d125c827044fcdf6e0528",
    ...
  ],
  "error": null,
  "id": 1,
  "uuid": "27337A41-62E6-462A-B2B0-D3E74177320E"
}
```

Parameter      | Type          | Description
---------------|---------------|-------------
reply          | int           | JSON array of the transaction ids.
error          | string        | API error code.
id             | int           | ID number.
uuid           | string        | The response ID, which can be used to view this response again with [xrGetReply](https://api.blocknet.co/#xrgetreply).
