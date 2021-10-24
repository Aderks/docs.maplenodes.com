# Omni Core

Call                                                                                | Description
------------------------------------------------------------------------------------|----------------------------------------------------------------------------------
[omni_getactivations](#omni_getactivations)                                           | Returns pending and completed feature activations.
[omni_getactivecrowdsales](#omni_getactivecrowdsales)                                 | Lists currently active crowdsales.
[omni_getactivedexsells](#omni_getactivedexsells)                                     | Returns currently active offers on the distributed exchange.
[omni_getallbalancesforaddress](#omni_getallbalancesforaddress)                       | Returns a list of all token balances for a given address.
[omni_getallbalancesforid](#omni_getallbalancesforid)                                 | Returns a list of token balances for a given currency or property identifier.
[omni_getbalance](#omni_getbalance)                                                   | Returns the token balance for a given address and property.
[omni_getcrowdsale](#omni_getcrowdsale)                                               | Returns information about a crowdsale.
[omni_getcurrentconsensushash](#omni_getcurrentconsensushash)                         | Returns the consensus hash covering the state of the current block.
[omni_getgrants](#omni_getgrants)                                                     | Returns information about granted and revoked units of managed tokens.
[omni_getinfo](#omni_getinfo)                                                         | Returns various state information of the client and protocol.
[omni_getorderbook](#omni_getorderbook)                                               | List active offers on the distributed token exchange.
[omni_getpayload](#omni_getpayload)                                                   | Get the payload for an Omni transaction.
[omni_getproperty](#omni_getproperty)                                                 | Returns details about the tokens or smart property to lookup.
[omni_getseedblocks](#omni_getseedblocks)                                             | Returns a list of blocks containing Omni transactions for use in seed block filtering.
[omni_getsto](#omni_getsto)                                                           | Get information and recipients of a send-to-owners transaction.
[omni_gettrade](#omni_gettrade)                                                       | Get detailed information and trade matches for orders on the distributed token exchange.
[omni_gettradehistoryforaddress](#omni_gettradehistoryforaddress)                     | Retrieves the history of orders on the distributed exchange for the supplied address.
[omni_gettradehistoryforpair](#omni_gettradehistoryforpair)                           | Retrieves the history of trades on the distributed token exchange for the specified market.
[omni_gettransaction](#omni_gettransaction)                                           | Get detailed information about an Omni transaction.
[omni_listblocktransactions](#omni_listblocktransactions)                             | Lists all Omni transactions in a block.
[omni_listblockstransactions](#omni_listblockstransactions)                           | Lists all Omni transactions in a given range of blocks.
[omni_listpendingtransactions](#omni_listpendingtransactions)                         | Returns a list of unconfirmed Omni transactions, pending in the memory pool.
[omni_listproperties](#omni_listproperties)                                           | Lists all tokens or smart properties.
[omni_listtransactions](#omni_listtransactions)                                       | List wallet transactions, optionally filtered by an address and block boundaries.





## omni_getactivations

Returns pending and completed feature activations.

### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '[]' https://api.oracleminer.com/xrs/omni_getactivations
```

```plaintext
blocknet-cli xrService omni_getactivations
```
<code class="api-call">omni_getactivations</code>

This call does not take parameters.


### Response

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
{
  "pendingactivations": [],
  "completedactivations": [
    {
      "featureid": 1,
      "featurename": "Class C transaction encoding",
      "activationblock": 395000,
      "minimumversion": 1000000
    },
    {
      "featureid": 5,
      "featurename": "DEx integer math update",
      "activationblock": 395000,
      "minimumversion": 1000000
    },
    {
      "featureid": 7,
      "featurename": "Disable crowdsale ecosystem crossovers",
      "activationblock": 395000,
      "minimumversion": 1000000
    },
    {
      "featureid": 6,
      "featurename": "Send All transactions",
      "activationblock": 395000,
      "minimumversion": 1000000
    },
    {
      "featureid": 4,
      "featurename": "Remove grant side effects",
      "activationblock": 394500,
      "minimumversion": 1000000
    },
    {
      "featureid": 2,
      "featurename": "Distributed Meta Token Exchange",
      "activationblock": 400000,
      "minimumversion": 1000000
    },
    {
      "featureid": 8,
      "featurename": "Allow trading all pairs on the Distributed Exchange",
      "activationblock": 438500,
      "minimumversion": 1100000
    },
    {
      "featureid": 14,
      "featurename": "Activate the waiting period for enabling freezing",
      "activationblock": 499200,
      "minimumversion": 30000000
    }
  ]
}
```

```plaintext
{
  "reply": {
	"pendingactivations": [
	],
	"completedactivations": [
	  {
		"featureid": 1,
		"featurename": "Class C transaction encoding",
		"activationblock": 395000,
		"minimumversion": 1000000
	  },
	  {
		"featureid": 5,
		"featurename": "DEx integer math update",
		"activationblock": 395000,
		"minimumversion": 1000000
	  },
	  {
		"featureid": 7,
		"featurename": "Disable crowdsale ecosystem crossovers",
		"activationblock": 395000,
		"minimumversion": 1000000
	  },
	  {
		"featureid": 6,
		"featurename": "Send All transactions",
		"activationblock": 395000,
		"minimumversion": 1000000
	  },
	  {
		"featureid": 4,
		"featurename": "Remove grant side effects",
		"activationblock": 394500,
		"minimumversion": 1000000
	  },
	  {
		"featureid": 2,
		"featurename": "Distributed Meta Token Exchange",
		"activationblock": 400000,
		"minimumversion": 1000000
	  },
	  {
		"featureid": 8,
		"featurename": "Allow trading all pairs on the Distributed Exchange",
		"activationblock": 438500,
		"minimumversion": 1100000
	  },
	  {
		"featureid": 14,
		"featurename": "Activate the waiting period for enabling freezing",
		"activationblock": 499200,
		"minimumversion": 30000000
	  }
	]
  },
  "error": null,
  "id": 1,
  "uuid": "9B0339F9-A611-4852-AFBF-A4200BD232EE"
}
```

Parameter            | Type          | Description
---------------------|---------------|-------------
pendingactivations   | Array         | Array of pending feature activations.
completedactivations | Array         | Array of completed feature activations.
error                | string        | API error code.
id                   | int           | ID number.
uuid                 | string        | The response ID, which can be used to view this response again with [xrGetReply](https://api.blocknet.co/#xrgetreply).





## omni_getactivecrowdsales

Lists currently active crowdsales.

### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '[]' https://api.oracleminer.com/xrs/omni_getactivecrowdsales
```

```plaintext
blocknet-cli xrService omni_getactivecrowdsales
```
<code class="api-call">omni_getactivecrowdsales</code>

This call does not take parameters.


### Response

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
[
  {
    "propertyid": 2147483723,
    "name": "green coin",
    "issuer": "12UPLX4sk2U85QCKxkJ71RCtczUmMLXvAK",
    "propertyiddesired": 2147483720,
    "tokensperunit": "11.00000000",
    "earlybonus": 6,
    "percenttoissuer": 10,
    "starttime": 1406699615,
    "deadline": 1409356140000
  },
  {
    "propertyid": 2147483704,
    "name": "ShoePhone",
    "issuer": "12vPM3chMgXBoyi5tWSjCcUBQvdPxd4QxH",
    "propertyiddesired": 2,
    "tokensperunit": "8686",
    "earlybonus": 28,
    "percenttoissuer": 68,
    "starttime": 1405022172,
    "deadline": 1406925000000
  },
  {
    "propertyid": 2147483854,
    "name": "CrowdsaleTest",
    "issuer": "1471EHpnJ62MDxLw96dKcNT8sWPEbHrAUe",
    "propertyiddesired": 2147483853,
    "tokensperunit": "100",
    "earlybonus": 255,
    "percenttoissuer": 255,
    "starttime": 1453572496,
    "deadline": 7731414000
  },
  {
    "propertyid": 2147483679,
    "name": "OmpaLoompa",
    "issuer": "18eVnuXEixXuVt248a5i18eLnkKbfmpUWk",
    "propertyiddesired": 2,
    "tokensperunit": "0.00000100",
    "earlybonus": 25,
    "percenttoissuer": 10,
    "starttime": 1403303662,
    "deadline": 22453142409904
  },
  {
    "propertyid": 2147483699,
    "name": "1",
    "issuer": "1CTmPpXF89LMNHwdizPXxSLd34uRok133V",
    "propertyiddesired": 2147483692,
    "tokensperunit": "3.00000000",
    "earlybonus": 1,
    "percenttoissuer": 1,
    "starttime": 1404417063,
    "deadline": 1407076800000
  },
  {
    "propertyid": 30,
    "name": "SymChain",
    "issuer": "1CXnRrBm3NezYeAcu555Ubu7swwKsn26dT",
    "propertyiddesired": 24,
    "tokensperunit": "1000.00000000",
    "earlybonus": 0,
    "percenttoissuer": 0,
    "starttime": 1409343479,
    "deadline": 4567622400
  },
  {
    "propertyid": 2147483657,
    "name": "Fundraiser 3 Div",
    "issuer": "1DYb5Njvcgovt9gUMdMgYkpaQjAEdUooon",
    "propertyiddesired": 2,
    "tokensperunit": "0.00001000",
    "earlybonus": 0,
    "percenttoissuer": 0,
    "starttime": 1397243096,
    "deadline": 1649030400
  },
  {
    "propertyid": 759,
    "name": "JOE",
    "issuer": "1FwADyEvdvaLNxjN1v3q6tNJCgHEBuABrS",
    "propertyiddesired": 68,
    "tokensperunit": "1.00000000",
    "earlybonus": 10,
    "percenttoissuer": 10,
    "starttime": 1572580398,
    "deadline": 1604396040
  },
  {
    "propertyid": 2147483744,
    "name": "NeverEndingFunTokens",
    "issuer": "1K6JtSvrHtyFmxdtGZyZEF7ydytTGqasNc",
    "propertyiddesired": 2,
    "tokensperunit": "1",
    "earlybonus": 255,
    "percenttoissuer": 2,
    "starttime": 1411899962,
    "deadline": 8314026105600
  },
  {
    "propertyid": 2147483703,
    "name": "WeeCoin",
    "issuer": "1KVhsbJ4pBgZVSUYUVZUJ2xAMMbt8eY8vU",
    "propertyiddesired": 2,
    "tokensperunit": "25.00000000",
    "earlybonus": 2,
    "percenttoissuer": 10,
    "starttime": 1405016346,
    "deadline": 1406987700000
  },
  {
    "propertyid": 2147483710,
    "name": "SpaceLite Life Sciences R&D",
    "issuer": "1MatrixoUT68b6mWwyRSpL6uVPpfwWhB9R",
    "propertyiddesired": 2147483707,
    "tokensperunit": "7.00000000",
    "earlybonus": 5,
    "percenttoissuer": 100,
    "starttime": 1405500631,
    "deadline": 1409940240000
  },
  {
    "propertyid": 28,
    "name": "ProzCoin",
    "issuer": "1PRozi3UhpXtC4kZtPD1nfCFXJkXrV27Wp",
    "propertyiddesired": 24,
    "tokensperunit": "100000000.00000000",
    "earlybonus": 0,
    "percenttoissuer": 100,
    "starttime": 1406925999,
    "deadline": 1406967060000
  },
  {
    "propertyid": 2147483693,
    "name": "a",
    "issuer": "1PVWtK1ATnvbRaRceLRH5xj8XV1LxUBu7n",
    "propertyiddesired": 2147483671,
    "tokensperunit": "5.00000000",
    "earlybonus": 1,
    "percenttoissuer": 1,
    "starttime": 1404169502,
    "deadline": 1406696400000
  },
  {
    "propertyid": 2147483708,
    "name": "mithradites",
    "issuer": "1PfREWL44zJun1MLXkH64s88DSkPZXVxot",
    "propertyiddesired": 2,
    "tokensperunit": "21000000.00000000",
    "earlybonus": 6,
    "percenttoissuer": 20,
    "starttime": 1405228233,
    "deadline": 1407888180000
  },
  {
    "propertyid": 2147483725,
    "name": "InternCoin",
    "issuer": "1f2dj45pxYb8BCW5sSbCgJ5YvXBfSapeX",
    "propertyiddesired": 2,
    "tokensperunit": "598.00000000",
    "earlybonus": 34,
    "percenttoissuer": 12,
    "starttime": 1407272092,
    "deadline": 1407873600000
  }
]
```

```plaintext
{
  "reply": [
	{
	  "propertyid": 2147483723,
	  "name": "green coin",
	  "issuer": "12UPLX4sk2U85QCKxkJ71RCtczUmMLXvAK",
	  "propertyiddesired": 2147483720,
	  "tokensperunit": "11.00000000",
	  "earlybonus": 6,
	  "percenttoissuer": 10,
	  "starttime": 1406699615,
	  "deadline": 1409356140000
	},
	{
	  "propertyid": 2147483704,
	  "name": "ShoePhone",
	  "issuer": "12vPM3chMgXBoyi5tWSjCcUBQvdPxd4QxH",
	  "propertyiddesired": 2,
	  "tokensperunit": "8686",
	  "earlybonus": 28,
	  "percenttoissuer": 68,
	  "starttime": 1405022172,
	  "deadline": 1406925000000
	},
	{
	  "propertyid": 2147483854,
	  "name": "CrowdsaleTest",
	  "issuer": "1471EHpnJ62MDxLw96dKcNT8sWPEbHrAUe",
	  "propertyiddesired": 2147483853,
	  "tokensperunit": "100",
	  "earlybonus": 255,
	  "percenttoissuer": 255,
	  "starttime": 1453572496,
	  "deadline": 7731414000
	},
	{
	  "propertyid": 2147483679,
	  "name": "OmpaLoompa",
	  "issuer": "18eVnuXEixXuVt248a5i18eLnkKbfmpUWk",
	  "propertyiddesired": 2,
	  "tokensperunit": "0.00000100",
	  "earlybonus": 25,
	  "percenttoissuer": 10,
	  "starttime": 1403303662,
	  "deadline": 22453142409904
	},
	{
	  "propertyid": 2147483699,
	  "name": "1",
	  "issuer": "1CTmPpXF89LMNHwdizPXxSLd34uRok133V",
	  "propertyiddesired": 2147483692,
	  "tokensperunit": "3.00000000",
	  "earlybonus": 1,
	  "percenttoissuer": 1,
	  "starttime": 1404417063,
	  "deadline": 1407076800000
	},
	{
	  "propertyid": 30,
	  "name": "SymChain",
	  "issuer": "1CXnRrBm3NezYeAcu555Ubu7swwKsn26dT",
	  "propertyiddesired": 24,
	  "tokensperunit": "1000.00000000",
	  "earlybonus": 0,
	  "percenttoissuer": 0,
	  "starttime": 1409343479,
	  "deadline": 4567622400
	},
	{
	  "propertyid": 2147483657,
	  "name": "Fundraiser 3 Div",
	  "issuer": "1DYb5Njvcgovt9gUMdMgYkpaQjAEdUooon",
	  "propertyiddesired": 2,
	  "tokensperunit": "0.00001000",
	  "earlybonus": 0,
	  "percenttoissuer": 0,
	  "starttime": 1397243096,
	  "deadline": 1649030400
	},
	{
	  "propertyid": 759,
	  "name": "JOE",
	  "issuer": "1FwADyEvdvaLNxjN1v3q6tNJCgHEBuABrS",
	  "propertyiddesired": 68,
	  "tokensperunit": "1.00000000",
	  "earlybonus": 10,
	  "percenttoissuer": 10,
	  "starttime": 1572580398,
	  "deadline": 1604396040
	},
	{
	  "propertyid": 2147483744,
	  "name": "NeverEndingFunTokens",
	  "issuer": "1K6JtSvrHtyFmxdtGZyZEF7ydytTGqasNc",
	  "propertyiddesired": 2,
	  "tokensperunit": "1",
	  "earlybonus": 255,
	  "percenttoissuer": 2,
	  "starttime": 1411899962,
	  "deadline": 8314026105600
	},
	{
	  "propertyid": 2147483703,
	  "name": "WeeCoin",
	  "issuer": "1KVhsbJ4pBgZVSUYUVZUJ2xAMMbt8eY8vU",
	  "propertyiddesired": 2,
	  "tokensperunit": "25.00000000",
	  "earlybonus": 2,
	  "percenttoissuer": 10,
	  "starttime": 1405016346,
	  "deadline": 1406987700000
	},
	{
	  "propertyid": 2147483710,
	  "name": "SpaceLite Life Sciences R&D",
	  "issuer": "1MatrixoUT68b6mWwyRSpL6uVPpfwWhB9R",
	  "propertyiddesired": 2147483707,
	  "tokensperunit": "7.00000000",
	  "earlybonus": 5,
	  "percenttoissuer": 100,
	  "starttime": 1405500631,
	  "deadline": 1409940240000
	},
	{
	  "propertyid": 28,
	  "name": "ProzCoin",
	  "issuer": "1PRozi3UhpXtC4kZtPD1nfCFXJkXrV27Wp",
	  "propertyiddesired": 24,
	  "tokensperunit": "100000000.00000000",
	  "earlybonus": 0,
	  "percenttoissuer": 100,
	  "starttime": 1406925999,
	  "deadline": 1406967060000
	},
	{
	  "propertyid": 2147483693,
	  "name": "a",
	  "issuer": "1PVWtK1ATnvbRaRceLRH5xj8XV1LxUBu7n",
	  "propertyiddesired": 2147483671,
	  "tokensperunit": "5.00000000",
	  "earlybonus": 1,
	  "percenttoissuer": 1,
	  "starttime": 1404169502,
	  "deadline": 1406696400000
	},
	{
	  "propertyid": 2147483708,
	  "name": "mithradites",
	  "issuer": "1PfREWL44zJun1MLXkH64s88DSkPZXVxot",
	  "propertyiddesired": 2,
	  "tokensperunit": "21000000.00000000",
	  "earlybonus": 6,
	  "percenttoissuer": 20,
	  "starttime": 1405228233,
	  "deadline": 1407888180000
	},
	{
	  "propertyid": 2147483817,
	  "name": "Test_Crowdsale",
	  "issuer": "1Pv6N8X9ofPa27PpWB63A4T4R61kUFqQEK",
	  "propertyiddesired": 2147483707,
	  "tokensperunit": "1.00000000",
	  "earlybonus": 100,
	  "percenttoissuer": 99,
	  "starttime": 1436326452,
	  "deadline": 1577753340
	},
	{
	  "propertyid": 2147483725,
	  "name": "InternCoin",
	  "issuer": "1f2dj45pxYb8BCW5sSbCgJ5YvXBfSapeX",
	  "propertyiddesired": 2,
	  "tokensperunit": "598.00000000",
	  "earlybonus": 34,
	  "percenttoissuer": 12,
	  "starttime": 1407272092,
	  "deadline": 1407873600000
	}
  ],
  "error": null,
  "id": 1,
  "uuid": "66F5922C-6CA2-4FEF-992E-9A64DE806783"
}
```

Parameter            | Type          | Description
---------------------|---------------|-------------
propertyid           | int           | The identifier of the crowdsale.
name                 | string        | The name of the tokens issued via the crowdsale.
issuer               | string        | The Bitcoin address of the issuer on record.
propertyiddesired    | int           | The identifier of the tokens eligible to participate in the crowdsale.
tokensperunit        | string        | The amount of tokens granted per unit invested in the crowdsale.
earlybonus           | int           | An early bird bonus for participants in percent per week.
percenttoissuer      | int           | A percentage of tokens that will be granted to the issuer.
starttime            | int           | The start time of the of the crowdsale as Unix timestamp
deadline             | int           | The deadline of the crowdsale as Unix timestamp
error                | string        | API error code.
id                   | int           | ID number.
uuid                 | string        | The response ID, which can be used to view this response again with [xrGetReply](https://api.blocknet.co/#xrgetreply).





## omni_getactivedexsells

Returns currently active offers on the distributed exchange.

### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '[]' https://api.oracleminer.com/xrs/omni_getactivedexsells
```

```plaintext
blocknet-cli xrService omni_getactivedexsells
```
<code class="api-call">omni_getactivedexsells</code>

This call does not take parameters.


### Response

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
[
  {
    "txid": "fb8573d6f7cd4b57e98625f4df0a818de36e76d7ea4bc500b55d9a60c5095228",
    "propertyid": 1,
    "seller": "1255GUS55xvs6rkiuEzgfT35jq4Kkk9gQL",
    "amountavailable": "1.00000000",
    "bitcoindesired": "1.00000000",
    "unitprice": "1.00000000",
    "timelimit": 100,
    "minimumfee": "0.00010000",
    "amountaccepted": "0.00000000",
    "accepts": []
  },
  {
    "txid": "b962a0658f37a00c69b3232ee3794cedd2c33eb1a15bb6158a9c5907bf0154f9",
    "propertyid": 1,
    "seller": "12t6EZateWSVh9xCaQx5NAf2J5X66Lk6rs",
    "amountavailable": "0.25000000",
    "bitcoindesired": "0.10000000",
    "unitprice": "0.40000000",
    "timelimit": 10,
    "minimumfee": "0.00010000",
    "amountaccepted": "0.00000000",
    "accepts": []
  },
  {
    "txid": "3159d26055ebe16e84da72ba331ecc8312162fc0a0a7837a7b461763a5ca796b",
    "propertyid": 1,
    "seller": "12wv6qoWxEvuoVDspyNgAvEQD7xhQfWPLy",
    "amountavailable": "63.02246436",
    "bitcoindesired": "2.52089798",
    "unitprice": "0.03999999",
    "timelimit": 100,
    "minimumfee": "0.00020000",
    "amountaccepted": "0.00000000",
    "accepts": []
  },
  {
    "txid": "d2ba6328c8cb5b0671bcc1ec2a59fd10f3019fafe5c0e10328213c788f332311",
    "propertyid": 1,
    "seller": "133tYepX5YAmugWbwuEErxoNe8yJXkNqqL",
    "amountavailable": "10.00000000",
    "bitcoindesired": "0.00650000",
    "unitprice": "0.00065000",
    "timelimit": 100,
    "minimumfee": "0.00020000",
    "amountaccepted": "0.00000000",
    "accepts": []
  },
  {
    "txid": "85209c3f7572e1867a5d868c2ef1ecef433e4f8b2d212187f6331e21a2757119",
    "propertyid": 1,
    "seller": "13CsP5SArN7fPXcXkcH331PPEuzCXdo5i4",
    "amountavailable": "1.00000000",
    "bitcoindesired": "0.32000000",
    "unitprice": "0.32000000",
    "timelimit": 3,
    "minimumfee": "0.00010000",
    "amountaccepted": "0.00000000",
    "accepts": []
  },
  {
    "txid": "7e51d9b9e7c0f57d688bf77ea31a315284533391bef2c81beaf12a965c2e0ece",
    "propertyid": 1,
    "seller": "13FrZaxxAWuFUqsmRVatp88h6EKTwmUrtj",
    "amountavailable": "9.00000000",
    "bitcoindesired": "0.83700000",
    "unitprice": "0.09300000",
    "timelimit": 6,
    "minimumfee": "0.00010000",
    "amountaccepted": "0.00000000",
    "accepts": []
  },
  {
    "txid": "f8e53b52fa18e478fca931946bdf388ffcbecd9b053db3672f5289696e552739",
    "propertyid": 2,
    "seller": "13NRX88EZbS5q81x6XFrTECzrciPREo821",
    "amountavailable": "5.00000000",
    "bitcoindesired": "0.00500000",
    "unitprice": "0.00100000",
    "timelimit": 15,
    "minimumfee": "0.00010000",
    "amountaccepted": "0.00000000",
    "accepts": []
  },
  {
    "txid": "ee0bd6e6614f1fbf7866cb61bede9dfc04565ac98a20b2b730f067f5a3a67b45",
    "propertyid": 2,
    "seller": "143jwThfaFtBYxyTfRtjBZrt3i1fuF1udo",
    "amountavailable": "1.00000000",
    "bitcoindesired": "0.10000000",
    "unitprice": "0.10000000",
    "timelimit": 20,
    "minimumfee": "0.00010000",
    "amountaccepted": "0.00000000",
    "accepts": []
  },
  {
    "txid": "b09fc81170ea65f823a675f6d3c6e87f1fc6aeb75898cb6922f9ad183c9952c1",
    "propertyid": 1,
    "seller": "14AET2c8EPCroZRDBNDbbZ1tFA5VUE5mwM",
    "amountavailable": "0.19779250",
    "bitcoindesired": "0.00128708",
    "unitprice": "0.00650718",
    "timelimit": 100,
    "minimumfee": "0.00020000",
    "amountaccepted": "0.00000000",
    "accepts": []
  },
  {
    "txid": "e2376208f5afd1beb3ced966746df9aa918f265c5cfa9725d32ada428bf3df2b",
    "propertyid": 1,
    "seller": "14GD4PY1JfbwR1imWfHXz7hYiG332h83pB",
    "amountavailable": "0.00008268",
    "bitcoindesired": "0.00000125",
    "unitprice": "0.01500608",
    "timelimit": 15,
    "minimumfee": "0.00010000",
    "amountaccepted": "0.00000000",
    "accepts": []
  },
  {
    "txid": "b0f65c56b13806cca4e5cc3d14a062455befefe546b257abe2a8a3ba597c664c",
    "propertyid": 1,
    "seller": "14cn7BiyzUeMcddC3RUFk77Z2k8NcP66yf",
    "amountavailable": "24.85060000",
    "bitcoindesired": "3.72759000",
    "unitprice": "0.15000000",
    "timelimit": 20,
    "minimumfee": "0.00010000",
    "amountaccepted": "0.00000000",
    "accepts": []
  }
]
```

```plaintext
{
  "reply": [
	{
	  "txid": "fb8573d6f7cd4b57e98625f4df0a818de36e76d7ea4bc500b55d9a60c5095228",
	  "propertyid": 1,
	  "seller": "1255GUS55xvs6rkiuEzgfT35jq4Kkk9gQL",
	  "amountavailable": "1.00000000",
	  "bitcoindesired": "1.00000000",
	  "unitprice": "1.00000000",
	  "timelimit": 100,
	  "minimumfee": "0.00010000",
	  "amountaccepted": "0.00000000",
	  "accepts": [
	  ]
	},
	{
	  "txid": "b962a0658f37a00c69b3232ee3794cedd2c33eb1a15bb6158a9c5907bf0154f9",
	  "propertyid": 1,
	  "seller": "12t6EZateWSVh9xCaQx5NAf2J5X66Lk6rs",
	  "amountavailable": "0.25000000",
	  "bitcoindesired": "0.10000000",
	  "unitprice": "0.40000000",
	  "timelimit": 10,
	  "minimumfee": "0.00010000",
	  "amountaccepted": "0.00000000",
	  "accepts": [
	  ]
	},
	{
	  "txid": "3159d26055ebe16e84da72ba331ecc8312162fc0a0a7837a7b461763a5ca796b",
	  "propertyid": 1,
	  "seller": "12wv6qoWxEvuoVDspyNgAvEQD7xhQfWPLy",
	  "amountavailable": "63.02246436",
	  "bitcoindesired": "2.52089798",
	  "unitprice": "0.03999999",
	  "timelimit": 100,
	  "minimumfee": "0.00020000",
	  "amountaccepted": "0.00000000",
	  "accepts": [
	  ]
	},
	{
	  "txid": "d2ba6328c8cb5b0671bcc1ec2a59fd10f3019fafe5c0e10328213c788f332311",
	  "propertyid": 1,
	  "seller": "133tYepX5YAmugWbwuEErxoNe8yJXkNqqL",
	  "amountavailable": "10.00000000",
	  "bitcoindesired": "0.00650000",
	  "unitprice": "0.00065000",
	  "timelimit": 100,
	  "minimumfee": "0.00020000",
	  "amountaccepted": "0.00000000",
	  "accepts": [
	  ]
	},
	{
	  "txid": "85209c3f7572e1867a5d868c2ef1ecef433e4f8b2d212187f6331e21a2757119",
	  "propertyid": 1,
	  "seller": "13CsP5SArN7fPXcXkcH331PPEuzCXdo5i4",
	  "amountavailable": "1.00000000",
	  "bitcoindesired": "0.32000000",
	  "unitprice": "0.32000000",
	  "timelimit": 3,
	  "minimumfee": "0.00010000",
	  "amountaccepted": "0.00000000",
	  "accepts": [
	  ]
	},
	{
	  "txid": "7e51d9b9e7c0f57d688bf77ea31a315284533391bef2c81beaf12a965c2e0ece",
	  "propertyid": 1,
	  "seller": "13FrZaxxAWuFUqsmRVatp88h6EKTwmUrtj",
	  "amountavailable": "9.00000000",
	  "bitcoindesired": "0.83700000",
	  "unitprice": "0.09300000",
	  "timelimit": 6,
	  "minimumfee": "0.00010000",
	  "amountaccepted": "0.00000000",
	  "accepts": [
	  ]
	},
	{
	  "txid": "f8e53b52fa18e478fca931946bdf388ffcbecd9b053db3672f5289696e552739",
	  "propertyid": 2,
	  "seller": "13NRX88EZbS5q81x6XFrTECzrciPREo821",
	  "amountavailable": "5.00000000",
	  "bitcoindesired": "0.00500000",
	  "unitprice": "0.00100000",
	  "timelimit": 15,
	  "minimumfee": "0.00010000",
	  "amountaccepted": "0.00000000",
	  "accepts": [
	  ]
	},
	{
	  "txid": "ee0bd6e6614f1fbf7866cb61bede9dfc04565ac98a20b2b730f067f5a3a67b45",
	  "propertyid": 2,
	  "seller": "143jwThfaFtBYxyTfRtjBZrt3i1fuF1udo",
	  "amountavailable": "1.00000000",
	  "bitcoindesired": "0.10000000",
	  "unitprice": "0.10000000",
	  "timelimit": 20,
	  "minimumfee": "0.00010000",
	  "amountaccepted": "0.00000000",
	  "accepts": [
	  ]
	},
	{
	  "txid": "b09fc81170ea65f823a675f6d3c6e87f1fc6aeb75898cb6922f9ad183c9952c1",
	  "propertyid": 1,
	  "seller": "14AET2c8EPCroZRDBNDbbZ1tFA5VUE5mwM",
	  "amountavailable": "0.19779250",
	  "bitcoindesired": "0.00128708",
	  "unitprice": "0.00650718",
	  "timelimit": 100,
	  "minimumfee": "0.00020000",
	  "amountaccepted": "0.00000000",
	  "accepts": [
	  ]
	},
	{
	  "txid": "e2376208f5afd1beb3ced966746df9aa918f265c5cfa9725d32ada428bf3df2b",
	  "propertyid": 1,
	  "seller": "14GD4PY1JfbwR1imWfHXz7hYiG332h83pB",
	  "amountavailable": "0.00008268",
	  "bitcoindesired": "0.00000125",
	  "unitprice": "0.01500608",
	  "timelimit": 15,
	  "minimumfee": "0.00010000",
	  "amountaccepted": "0.00000000",
	  "accepts": [
	  ]
	},
	{
	  "txid": "b0f65c56b13806cca4e5cc3d14a062455befefe546b257abe2a8a3ba597c664c",
	  "propertyid": 1,
	  "seller": "14cn7BiyzUeMcddC3RUFk77Z2k8NcP66yf",
	  "amountavailable": "24.85060000",
	  "bitcoindesired": "3.72759000",
	  "unitprice": "0.15000000",
	  "timelimit": 20,
	  "minimumfee": "0.00010000",
	  "amountaccepted": "0.00000000",
	  "accepts": [
	  ]
	},
	{
	  "txid": "b2067e0447b645d389c4e2c57cf15671f29d187688679b51a2be2c2eee35f197",
	  "propertyid": 1,
	  "seller": "14fgdCAyhngfNNzHPGRY91QAMCBq2W8UW1",
	  "amountavailable": "5.00000000",
	  "bitcoindesired": "0.23500000",
	  "unitprice": "0.04700000",
	  "timelimit": 10,
	  "minimumfee": "0.00010000",
	  "amountaccepted": "0.00000000",
	  "accepts": [
	  ]
	},
	{
	  "txid": "ad3df801f8d662b47abfd71b27792016e9f210a613bb7de9d5494a16b8b0d8e6",
	  "propertyid": 1,
	  "seller": "14hzzakvvAVdvcQAL38bRhbCb92godUWe8",
	  "amountavailable": "10.00000000",
	  "bitcoindesired": "0.51000000",
	  "unitprice": "0.05100000",
	  "timelimit": 15,
	  "minimumfee": "0.00010000",
	  "amountaccepted": "0.00000000",
	  "accepts": [
	  ]
	},
	{
	  "txid": "86cebb87153c52d61f0e62ce37787def7b3c039c4e14939f28f3fa58ec3afe51",
	  "propertyid": 1,
	  "seller": "14k4GmbeTAwidUUMi99L4f1UDdMD7QjwGd",
	  "amountavailable": "0.00000105",
	  "bitcoindesired": "0.00000001",
	  "unitprice": "0.00796460",
	  "timelimit": 100,
	  "minimumfee": "0.00020000",
	  "amountaccepted": "0.00000000",
	  "accepts": [
	  ]
	},
	{
	  "txid": "67f3a61b1024e71140b9d8244cb32f6b1bd439a1e9eb105bfa025c868237368a",
	  "propertyid": 1,
	  "seller": "14kLL6tk2dgiuaj1PGS52QC6Sec7sqS7SD",
	  "amountavailable": "0.00000023",
	  "bitcoindesired": "0.00000001",
	  "unitprice": "0.00944539",
	  "timelimit": 100,
	  "minimumfee": "0.00010000",
	  "amountaccepted": "0.00000000",
	  "accepts": [
	  ]
	},
	{
	  "txid": "a37a51731c50d3b749f741fb3579f075823e1f277101f78f2e076a60f8cbe1ce",
	  "propertyid": 2,
	  "seller": "15QBPtyFR76ak2NvdfKbgYNp7HtB3tbtRd",
	  "amountavailable": "150.00000000",
	  "bitcoindesired": "5.00000000",
	  "unitprice": "0.03333333",
	  "timelimit": 12,
	  "minimumfee": "0.00000000",
	  "amountaccepted": "0.00000000",
	  "accepts": [
	  ]
	},
	{
	  "txid": "4e3c41d09bf98ac0345dc31b3c9dd98897b5451a82752801b7c937aea4d7553f",
	  "propertyid": 2,
	  "seller": "168F7az8ACWxntNqL1FathoKTbgK17GVft",
	  "amountavailable": "1.00000000",
	  "bitcoindesired": "1000000.00000000",
	  "unitprice": "1000000.00000000",
	  "timelimit": 12,
	  "minimumfee": "0.00010000",
	  "amountaccepted": "0.00000000",
	  "accepts": [
	  ]
	},
	{
	...	
	}
  ],
  "error": null,
  "id": 1,
  "uuid": "52A70ABE-90BE-47B1-8C8D-4A49B533ADD8"
}
```

Parameter            | Type          | Description
---------------------|---------------|-------------
txid                 | string        | The hash of the transaction of this offer.
propertyid           | int           | The identifier of the tokens for sale.
seller               | string        | The Bitcoin address of the seller.
amountavailable      | string        | The number of tokens still listed for sale and currently available.
bitcoindesired       | string        | The number of bitcoins desired in exchange.
unitprice            | string        | The unit price (BTC/token).
timelimit            | int           | The time limit in blocks a buyer has to pay following a successful accept.
minimumfee           | string        | The minimum mining fee a buyer has to pay to accept this offer.
amountaccepted       | string        | The number of tokens currently reserved for pending "accept" orders.
accepts              | Array         | A list of pending "accept" orders.
error                | string        | API error code.
id                   | int           | ID number.
uuid                 | string        | The response ID, which can be used to view this response again with [xrGetReply](https://api.blocknet.co/#xrgetreply).





## omni_getallbalancesforaddress

> Sample Data

```cli
{
  "address": "168F7az8ACWxntNqL1FathoKTbgK17GVft"
}
```
Returns a list of all token balances for a given address.


### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '["168F7az8ACWxntNqL1FathoKTbgK17GVft"]' https://api.oracleminer.com/xrs/omni_getallbalancesforaddress
```

```plaintext
blocknet-cli xrService omni_getallbalancesforaddress 168F7az8ACWxntNqL1FathoKTbgK17GVft
```
<code class="api-call">omni_getallbalancesforaddress [address]</code>

Parameter       | Type       | Description
----------------|------------|-------------
address         | string     | The address.


### Response Parameters

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
[
  {
    "propertyid": 1,
    "name": "Omni tokens",
    "balance": "0.00025000",
    "reserved": "0.00000000",
    "frozen": "0.00000000"
  },
  {
    "propertyid": 2,
    "name": "Test Omni tokens",
    "balance": "0.02382256",
    "reserved": "1.00000000",
    "frozen": "0.00000000"
  },
  {
    "propertyid": 2147483653,
    "name": "Mastercoin Faucet Promo Coupon",
    "balance": "1",
    "reserved": "0",
    "frozen": "0"
  },
  {
    "propertyid": 2147483743,
    "name": "TimeStampTestToken",
    "balance": "5",
    "reserved": "0",
    "frozen": "0"
  }
]
```

```plaintext
{
  "reply": [
	{
	  "propertyid": 1,
	  "name": "Omni tokens",
	  "balance": "0.00025000",
	  "reserved": "0.00000000",
	  "frozen": "0.00000000"
	},
	{
	  "propertyid": 2,
	  "name": "Test Omni tokens",
	  "balance": "0.02382256",
	  "reserved": "1.00000000",
	  "frozen": "0.00000000"
	},
	{
	  "propertyid": 2147483653,
	  "name": "Mastercoin Faucet Promo Coupon",
	  "balance": "1",
	  "reserved": "0",
	  "frozen": "0"
	},
	{
	  "propertyid": 2147483743,
	  "name": "TimeStampTestToken",
	  "balance": "5",
	  "reserved": "0",
	  "frozen": "0"
	}
  ],
  "error": null,
  "id": 1,
  "uuid": "0073255B-7246-4EE0-8389-E9D2969D9409"
}
```

Parameter            | Type          | Description
---------------------|---------------|-------------
propertyid           | int           | The property identifier.
name                 | string        | The name of the property.
balance              | string        | The available balance of the address.
reserved             | string        | The amount reserved by sell offers and accepts.
frozen               | string        | The amount frozen by the issuer (applies to managed properties only).
error                | string        | API error code.
id                   | int           | ID number.
uuid                 | string        | The response ID, which can be used to view this response again with [xrGetReply](https://api.blocknet.co/#xrgetreply).





## omni_getallbalancesforid

> Sample Data

```cli
{
  "propertyid": 2147483743
}
```
Returns a list of all token balances for a given address.


### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '[2147483743]' https://api.oracleminer.com/xrs/omni_getallbalancesforid
```

```plaintext
blocknet-cli xrService omni_getallbalancesforid 2147483743
```
<code class="api-call">omni_getallbalancesforid [propertyid]</code>

Parameter       | Type       | Description
----------------|------------|-------------
propertyid      | int        | The property identifier.


### Response Parameters

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
[
  {
    "address": "168F7az8ACWxntNqL1FathoKTbgK17GVft",
    "balance": "5",
    "reserved": "0",
    "frozen": "0"
  },
  {
    "address": "1CE8bBr1dYZRMnpmyYsFEoexa1YoPz2mfB",
    "balance": "6",
    "reserved": "0",
    "frozen": "0"
  },
  {
    "address": "1xC6gPa4QTM18cPKKPutcEkfmZvabY38j",
    "balance": "131",
    "reserved": "0",
    "frozen": "0"
  }
]
```

```plaintext
{
  "reply": [
	{
	  "address": "1xC6gPa4QTM18cPKKPutcEkfmZvabY38j",
	  "balance": "131",
	  "reserved": "0",
	  "frozen": "0"
	},
	{
	  "address": "1CE8bBr1dYZRMnpmyYsFEoexa1YoPz2mfB",
	  "balance": "6",
	  "reserved": "0",
	  "frozen": "0"
	},
	{
	  "address": "168F7az8ACWxntNqL1FathoKTbgK17GVft",
	  "balance": "5",
	  "reserved": "0",
	  "frozen": "0"
	}
  ],
  "error": null,
  "id": 1,
  "uuid": "D8377788-E46E-424C-A061-0EFF99E00C66"
}
```

Parameter            | Type          | Description
---------------------|---------------|-------------
address              | string        | The address.
balance              | string        | The available balance of the address.
reserved             | string        | The amount reserved by sell offers and accepts.
frozen               | string        | The amount frozen by the issuer (applies to managed properties only).
error                | string        | API error code.
id                   | int           | ID number.
uuid                 | string        | The response ID, which can be used to view this response again with [xrGetReply](https://api.blocknet.co/#xrgetreply).





## omni_getbalance

> Sample Data

```cli
{
  "address": "168F7az8ACWxntNqL1FathoKTbgK17GVft",
  "propertyid": 2147483743
}
```
Returns the token balance for a given address and property.


### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '["168F7az8ACWxntNqL1FathoKTbgK17GVft",2147483743]' https://api.oracleminer.com/xrs/omni_getbalance
```

```plaintext
blocknet-cli xrService omni_getbalance 168F7az8ACWxntNqL1FathoKTbgK17GVft 2147483743
```
<code class="api-call">omni_getbalance [address] [propertyid]</code>

Parameter       | Type       | Description
----------------|------------|-------------
address         | string     | The address.
propertyid      | int        | The property identifier.


### Response Parameters

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
{
  "balance": "5",
  "reserved": "0",
  "frozen": "0"
}
```

```plaintext
{
  "reply": {
	"balance": "5",
	"reserved": "0",
	"frozen": "0"
  },
  "error": null,
  "id": 1,
  "uuid": "330A8FC6-2917-48CA-8581-39558778D56E"
}
```

Parameter            | Type          | Description
---------------------|---------------|-------------
balance              | string        | The available balance of the address.
reserved             | string        | The amount reserved by sell offers and accepts.
frozen               | string        | The amount frozen by the issuer (applies to managed properties only).
error                | string        | API error code.
id                   | int           | ID number.
uuid                 | string        | The response ID, which can be used to view this response again with [xrGetReply](https://api.blocknet.co/#xrgetreply).





## omni_getcrowdsale

> Sample Data

```cli
{
  "propertyid": 2147483743,
  "verbose": false
}
```
Returns information about a crowdsale.


### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '[2147483743,false]' https://api.oracleminer.com/xrs/omni_getcrowdsale
```

```plaintext
blocknet-cli xrService omni_getcrowdsale 2147483743 false
```
<code class="api-call">omni_getcrowdsale [propertyid] [verbose]</code>

Parameter       | Type       | Description
----------------|------------|-------------
propertyid      | int        | The identifier of the crowdsale.
verbose         | bool       | List crowdsale participants.

### Response Parameters

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
{
  "propertyid": 2147483743,
  "name": "TimeStampTestToken",
  "active": false,
  "issuer": "1CE8bBr1dYZRMnpmyYsFEoexa1YoPz2mfB",
  "propertyiddesired": 2,
  "tokensperunit": "10",
  "earlybonus": 10,
  "percenttoissuer": 5,
  "starttime": 1411891018,
  "deadline": 1422475200,
  "amountraised": "5.20000000",
  "tokensissued": "142",
  "issuerbonustokens": "6",
  "addedissuertokens": "0",
  "closedearly": false,
  "maxtokens": false
}
```

```plaintext
{
  "reply": {
	"propertyid": 2147483743,
	"name": "TimeStampTestToken",
	"active": false,
	"issuer": "1CE8bBr1dYZRMnpmyYsFEoexa1YoPz2mfB",
	"propertyiddesired": 2,
	"tokensperunit": "10",
	"earlybonus": 10,
	"percenttoissuer": 5,
	"starttime": 1411891018,
	"deadline": 1422475200,
	"amountraised": "5.20000000",
	"tokensissued": "142",
	"issuerbonustokens": "6",
	"addedissuertokens": "0",
	"closedearly": false,
	"maxtokens": false
  },
  "error": null,
  "id": 1,
  "uuid": "1447AA70-3D3E-4F1F-B99C-E2F4E7EFDFC9"
}
```

Parameter               | Type          | Description
------------------------|---------------|-------------
propertyid              | string        | The identifier of the crowdsale.
name                    | string        | The name of the tokens issued via the crowdsale.
active                  | bool          | Whether the crowdsale is still active.
issuer                  | string        | The Bitcoin address of the issuer on record.
propertyiddesired       | int           | The identifier of the tokens eligible to participate in the crowdsale.
tokensperunit           | string        | The amount of tokens granted per unit invested in the crowdsale.
earlybonus              | int           | An early bird bonus for participants in percent per week.
percenttoissuer         | int           | A percentage of tokens that will be granted to the issuer.
starttime               | int           | The start time of the of the crowdsale as Unix timestamp.
deadline                | int           | The deadline of the crowdsale as Unix timestamp.
amountraised            | string        | The amount of tokens invested by participants.
tokensissued            | string        | The total number of tokens issued via the crowdsale.
issuerbonustokens       | string        | The amount of tokens granted to the issuer as bonus.
addedissuertokens       | string        | The amount of issuer bonus tokens not yet emitted.
closedearly             | bool          | Whether the crowdsale ended early (if not active).
maxtokens               | bool          | Whether the crowdsale ended early due to reaching the limit of max. issuable tokens (if not active).
endedtime               | int           | The time when the crowdsale ended (if closed early).
closetx                 | string        | The hex-encoded hash of the transaction that closed the crowdsale (if closed manually).
participanttransactions | Array         | A list of crowdsale participations (if verbose=true).
error                   | string        | API error code.
id                      | int           | ID number.
uuid                    | string        | The response ID, which can be used to view this response again with [xrGetReply](https://api.blocknet.co/#xrgetreply).





## omni_getcurrentconsensushash

Returns the consensus hash covering the state of the current block.

### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '[]' https://api.oracleminer.com/xrs/omni_getcurrentconsensushash
```

```plaintext
blocknet-cli xrService omni_getcurrentconsensushash
```
<code class="api-call">omni_getcurrentconsensushash</code>

This call does not take parameters.


### Response

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
{
  "block": 616294,
  "blockhash": "00000000000000000000fd73fbeff54e24b5db3a7a693e6a4e62c70f16e845ce",
  "consensushash": "3bb0844047f61d9cac0b853676f83a62dfa142a32acc76534393746b54ce2413"
}
```

```plaintext
{
  "reply": {
	"block": 609339,
	"blockhash": "000000000000000000044486d5daa0f93d371efdfe4bdfb6cd90503c0779bd5f",
	"consensushash": "857612d573af7ac82cb913f1573886e6f29212ee9135256f9224aea3d1f5e9ad"
  },
  "error": null,
  "id": 1,
  "uuid": "7570CF5D-3C1F-4A09-8860-2B5B2C96E0D0"
}
```

Parameter            | Type          | Description
---------------------|---------------|-------------
block                | int           | The index of the block this consensus hash applies to.
blockhash            | string        | The hash of the corresponding block.
consensushash        | string        | The consensus hash for the block.
error                | string        | API error code.
id                   | int           | ID number.
uuid                 | string        | The response ID, which can be used to view this response again with [xrGetReply](https://api.blocknet.co/#xrgetreply).





## omni_getgrants

> Sample Data

```cli
{
  "propertyid": 31
}
```
Returns information about granted and revoked units of managed tokens.


### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '[31]' https://api.oracleminer.com/xrs/omni_getgrants
```

```plaintext
blocknet-cli xrService omni_getgrants 31
```
<code class="api-call">omni_getgrants [propertyid]</code>

Parameter       | Type       | Description
----------------|------------|-------------
propertyid      | int        | The identifier of the managed tokens to lookup.

### Response Parameters

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
{
  "propertyid": 31,
  "name": "TetherUS",
  "issuer": "32TLn1WLcu8LtfvweLzYUYU6ubc2YV9eZs",
  "creationtxid": "5ed3694e8a4fa8d3ec5c75eb6789492c69e65511522b220e94ab51da2b6dd53f",
  "totaltokens": "1555000000.00000000",
  "issuances": [
    {
      "txid": "f307bdf50d90c92278265cd92819c787070d6652ae3c8af46fa6a96278589b03",
      "grant": "25000000.00000000"
    },
    {
      "txid": "d48069d2f2d2360929948e61771ed46f6f31aaf9c75be36bdf3ebc4ec3cded04",
      "grant": "20000000.00000000"
    },
    {
      "txid": "49448e97bfc1ac4f3136035e76eb5dc1f5c1362aef7cf90546d39f406347ce09",
      "revoke": "400000000.00000000"
    },
    {
      "txid": "e30f5ce14c47406f2fd6a2a27b25f6d0a90a1317b7f92b893a93e7529d281d0c",
      "grant": "25000000.00000000"
    },
    {
      "txid": "a992d336afbca58178801dae30cd71308a6a9e1f8b3b9da9f87b81bde402110d",
      "grant": "20000000.00000000"
    },
    {
      "txid": "ce36efda15bc6cf99ba6a010e71b47b00a5ea2071a392839effe7ed392cf690f",
      "grant": "100.00000000"
    },
    {
      "txid": "d97b583356e5ca63d77240b637e203fdf219528133c2700234314a2c99d57410",
      "grant": "500000.00000000"
    },
    {
      "txid": "361ce637741ab91b5e040a572a0ff5163dc1e151d8117ff0865b619cf765981c",
      "revoke": "275000000.00000000"
    },
    {
      "txid": "69a4b3027895da33952d661512d67071b351e11793ca286df24b8b8df63b781d",
      "grant": "25000000.00000000"
    },
    {
      "txid": "ed212c3ae5319ad6b7e3a1d7461e613d44fb2ad7ac0a61fe95195d82f6fe9521",
      "grant": "25048400.00000000"
    },
    {
      "txid": "b8e6d591a4f61b52f7b62ab80ae37b9b4396e00c695190da44211adfabee4424",
      "grant": "24999000.00000000"
    },
    {
      "txid": "b33aeae5fb64ee50229f1a04ea68e0975ba053dcec07cb162c7d2d93a635ed29",
      "grant": "30000000.00000000"
    },
    {
      "txid": "99d41439c1bbae042af6a6b6ef14a6ef408bbadaaa42b0a2949d87345b3fb82c",
      "grant": "25000000.00000000"
    },
    {
      "txid": "b182888725cff4486d4080cf04736ab0d2250a78a02948cfc348d8e1672ef52c",
      "grant": "100000000.00000000"
    },
    {
      "txid": "aec3630a38235e9e9013816b1aa165f1744298fd01c0f7f5710f67ced3392534",
      "grant": "10000000.00000000"
    },
    {
      "txid": "0fbf16c7b937a8a5601ade7897c69bc33f1836b9cb02b1814425dcf4a98d3436",
      "grant": "100000000.00000000"
    },
    {
      "txid": "44613540307e23fac0ab1105c057416a62d839f2a87b441ccd23a09f94780539",
      "grant": "20000000.00000000"
    },
    {
      "txid": "86530a24562c47ed236d11595133ac0b18c5eb5784d4bd44268affbceddb023a",
      "grant": "25000000.00000000"
    },
    {
      "txid": "d20feccaa3cb2ca70f046e4b52e4c0e4f4dd9aab2384b1171aad4ff77920683c",
      "grant": "2000000.00000000"
    },
    {
      "txid": "1fb018be89426bd12a8360cc63b0fb97ab99fa91dc0c878a5b4a409590c7163e",
      "grant": "30000000.00000000"
    },
    {
      "txid": "1e066cb56f44abec2f58879906fa767212d7d66cad0ffb4417ca4df41efa1242",
      "grant": "10000000.00000000"
    },
    {
      "txid": "c399c59e62ab91c00274136f51129a6dc507c1a3a5d60a378f7d7b3df5cf2042",
      "grant": "1000000.00000000"
    },
    {
      "txid": "5f5f34a84f352c79152fb681fbe6daf005fb5976cd553355295d58488ef7f44b",
      "grant": "10000000.00000000"
    },
    {
      "txid": "bd9520b9aea701e9606ad8a8f4d6852d70f2013b12df19b6d58147038392354e",
      "grant": "250000000.00000000"
    },
    {
      "txid": "7bae50bd80ada63deba4a8f774caabba607d4cd6bdadfbb169e71deee74dcc4f",
      "grant": "10000000.00000000"
    },
    {
      "txid": "80041e14c5f1565effb01a107697764d94670a578dc53367ca925556b38e1b51",
      "grant": "30000000.00000000"
    },
    {
      "txid": "0dca5f9d949bea9f528bf8edb3d1e0bb5365e80170a993577c0f46430a595354",
      "grant": "20000000.00000000"
    },
    {
      "txid": "76cc7c991e61749d7f4bf6cc7fec63c2d0286c891e386d9c96b66aa939683859",
      "revoke": "500000000.00000000"
    },
    {
      "txid": "23407cc132443fe5eff94d19ca016705623ca490c74d1a215a1026d801972263",
      "grant": "250000000.00000000"
    },
    {
      "txid": "7d23cb9e256ff614569b1a0269c84a97d0c5a4db0ba6155aca6637ac07caf463",
      "grant": "20000000.00000000"
    },
    {
      "txid": "dbde10653dd7f459260c11e2a80ae887f7c72e5bfd22f5d908b489dd430be764",
      "grant": "30000000.00000000"
    },
    {
      "txid": "d269f8aaaa625f35aad1dcf80ba55023317fdc881aa7f5cad1dff491bd89ff65",
      "grant": "50000000.00000000"
    },
    {
      "txid": "b71949385da682b203403009c26e41acf7f8577844e3c6a6a57236149e53b767",
      "grant": "10000000.00000000"
    },
    {
      "txid": "34dce9425949e2057d324061d82fd16ecfa98ab1177ff7cfe5f883abd5ac3e68",
      "grant": "10000000.00000000"
    },
    {
      "txid": "7e81d1c6dc1f3e82a63afc243a844dcd8b8086df7db3f799443c70a4b308216b",
      "grant": "25000000.00000000"
    },
    {
      "txid": "ace39edbe5211fdf0e3c07fc40255ba3da96258b25b864be2ed97d1ce785e36e",
      "grant": "25000000.00000000"
    },
    {
      "txid": "9560299a436998d24fbe44eca3adc6cbb0ad053438fd8d2cbb92b9209c42556f",
      "grant": "10000000.00000000"
    },
    {
      "txid": "0a390cc7273386a6c96ee6d6329c747dd43b4c899680ba41d897a42bdc707d70",
      "grant": "25000000.00000000"
    },
    {
      "txid": "32f8d7302d34a3d07d1eaa3f8a332097ac036c5ed1b214929ef741dac52c5172",
      "grant": "100000000.00000000"
    },
    {
      "txid": "4543c62de3c535087fe10d6798fc3f77bb9904637b287bc774d481a4f0954674",
      "grant": "100000000.00000000"
    },
    {
      "txid": "6f8b5ae18cc2203d35b0c2cca90b58c774f15ecead93be600232262c21518376",
      "grant": "50000000.00000000"
    },
    {
      "txid": "fcd19f0435f51f21fc4e326b1dfd61fbe6e1d19a03abca5db3fa6bc2f5cd5177",
      "grant": "20000000.00000000"
    },
    {
      "txid": "4719ba0875fb852ad01c5cfa0b6a206283f5a7241f3bca73a5f223bc34dd7b77",
      "revoke": "370000000.00000000"
    },
    {
      "txid": "bb2d78d00f529ae25f94f83ab6144239df30f2669853421815b5b1a12811cf78",
      "grant": "30000000.00000000"
    },
    {
      "txid": "b09d4fb8930bb396126644d01d7d20c961e002ef87f99b9a1fa4b016fa7a1a7a",
      "grant": "25000000.00000000"
    },
    {
      "txid": "0c8c22ee5cd69649ff36c0396bb9ce951425614a32129d8d54c0144895ef4e7a",
      "grant": "300000000.00000000"
    },
    {
      "txid": "0a3614e8770c954f7f6fbe0e0827bee0f26b286ee64f20c74e6fc0508ae32c7b",
      "grant": "10000000.00000000"
    },
    {
      "txid": "a217c29dbea8f07e46f72368ce52e518488a53872b3be5f014a663dfc765aa7c",
      "grant": "1000000.00000000"
    },
    {
      "txid": "fef813aa2c741a7babdd726a1678d3432c6ccc6256fe4676006dedd8b09b407f",
      "grant": "20000000.00000000"
    },
    {
      "txid": "91f2df37258d00f8873d7b3b52b381fe0a428e1a80f8cdeab64c82da5569a388",
      "grant": "25000000.00000000"
    },
    {
      "txid": "056f85a9c6035f94832468977ff4eceb33ebde00198ce9173f968937af59698b",
      "grant": "30000000.00000000"
    },
    {
      "txid": "dd1f01b435ee25137be0ddbfa3a8ffcab29e8076a8c0d9e1d7d7e4206378dc8e",
      "grant": "25000000.00000000"
    },
    {
      "txid": "9df555099b7a0a7d57969a80dc2557672814629d0194c2f1d7ecae279b107b8f",
      "grant": "10000000.00000000"
    },
    {
      "txid": "9a707dfffb734322a5ec1eee808dd0ba0365a84a204e500d23820e7827a1d390",
      "grant": "200000.00000000"
    },
    {
      "txid": "d68a4c0e40496c024cb675c79966522cb55863adf475ada6f87c1a3b775d7695",
      "grant": "25000000.00000000"
    },
    {
      "txid": "7b7f6b4ea3bef50f0652068975caea27c8f822ad484cab04a19a5dd06c3ef198",
      "grant": "25000000.00000000"
    },
    {
      "txid": "3691adbbe8342f6fde7bc549fcb0991decbe3bd040d01d87ee7970c0e47f3e9a",
      "grant": "100000000.00000000"
    },
    {
      "txid": "7830c14932edbed4d907fe856a57f87b6414dfc44402acd4fed4c87fb140749e",
      "grant": "1000000.00000000"
    },
    {
      "txid": "4981d4ffeb18cd4df56806b7414366fa62bf32f77fbe7efaeb8edd04fe90f09f",
      "revoke": "220000000.00000000"
    },
    {
      "txid": "8aaa758ee898258a779a9db34fee0fec1a808ffa33217ed8c46599d2d00677a1",
      "grant": "10000000.00000000"
    },
    {
      "txid": "03be725a88b8444294733ecc2ce6f7823c3a025ff79b612f8d615130a7e420b1",
      "grant": "200000.00000000"
    },
    {
      "txid": "ddfa527bb04d7a75bd2d790554d634bc48f72925f157fb0649abd95cb98ab7bc",
      "grant": "100000000.00000000"
    },
    {
      "txid": "1d2e9bb7e11d923912b5d45c3c0a31e7717ae9f0788ae10112daf9e6f5bdbac3",
      "grant": "10000000.00000000"
    },
    {
      "txid": "f117304418428c1e8d35cded9f0c34d6a8d533071b8761818b373d75930b4ec4",
      "grant": "25000000.00000000"
    },
    {
      "txid": "e4062783d935886392c29396d15aab470fff9732b0b8e80ad56573adcbea79c4",
      "grant": "100000000.00000000"
    },
    {
      "txid": "a48d435d6951a8c76b9a12747114e9bec2cb8f4d3c83141e4762bfdd384964c5",
      "grant": "25000000.00000000"
    },
    {
      "txid": "af28be44c59de9b680fcf374b5d126653659241eec0508fa455a021c2e836fc7",
      "grant": "500000.00000000"
    },
    {
      "txid": "65d0ba4c43787adb28d5a39c1f97c24176946fec241e000f8eb21970a6b298c7",
      "grant": "5000000.00000000"
    },
    {
      "txid": "394a072ed46088e218ac335cb4106050463960f916d420ca86a13ef1d393d2cb",
      "grant": "50000000.00000000"
    },
    {
      "txid": "a4a43812ae92c754783241d17b27ead8c8fcd6bbe8ad1661755872f3d23729cd",
      "grant": "500000.00000000"
    },
    {
      "txid": "0c83e7856c6b565341b85332b1f821a402a84aaf236b54ab6ee30c68901576cd",
      "grant": "100000000.00000000"
    },
    {
      "txid": "62dafaa813446c0ac9bbb14a313de8c6aaef73d44c6cdfadaa7b76a467df2dcf",
      "grant": "20000000.00000000"
    },
    {
      "txid": "c75b3e1d341d350e735e6a56e40c0d320c8d20c85174012df41c6f3ba9967cd0",
      "grant": "55000000.00000000"
    },
    {
      "txid": "080021ae9fd4c4f20bdc12e5b0ec2142e222667f6ceda806be58c988d59666d2",
      "grant": "25000000.00000000"
    },
    {
      "txid": "ede8df626c5d52562a391ec4cf2396e39cbc8b3beb35e44b7a4b23588ed711d4",
      "grant": "1000.00000000"
    },
    {
      "txid": "3490381674b237fa8585001aa6b19f2eed0fb46ac66e43309a0e276f98f398d4",
      "grant": "3000000.00000000"
    },
    {
      "txid": "7fd82ae1d2801572068ea103543c3cf1beb8a6917ba3610d400fb3fc03931fd7",
      "grant": "1500.00000000"
    },
    {
      "txid": "32b9245f23292be8730417f3ee84ff04f911963a33a4c2fdf060a1d7b07599d7",
      "grant": "10000000.00000000"
    },
    {
      "txid": "6aa73824bdae9f685ac657a534b801a7b077d1f0fab64406fb95f27a753c7ada",
      "grant": "50000000.00000000"
    },
    {
      "txid": "e4f40ee093ff38fbcca2597c7316d50ba98bed997a5984e43f0ecc9e51b20ee4",
      "grant": "50000000.00000000"
    },
    {
      "txid": "c9fca1a9ce81e58505f07c2230170524d3f3fa5f185a05a4762e6abfda538de4",
      "grant": "100000000.00000000"
    },
    {
      "txid": "46e4851175dd9f54c63e472173c112fe612895aeccd2a8035e4df708963db0e4",
      "grant": "20000000.00000000"
    },
    {
      "txid": "d63325a8f63a3bf593506cfbe6853f52b7129a875b9382b81da4cfae4134cbe4",
      "grant": "30000000.00000000"
    },
    {
      "txid": "bafbcb0a1700f7bbcb610fdf11111f3918d00af8d0bcede0928ffd50910d9ce7",
      "grant": "50000000.00000000"
    },
    {
      "txid": "24db40680654b8b505fda3e96be722ca10f341a129c99260509eb5d84655f1f0",
      "revoke": "30000000.00000000"
    },
    {
      "txid": "f3efac4b6203248fc06e2788b61e732319a6e596768f5240680f944780ff84f4",
      "grant": "300000000.00000000"
    },
    {
      "txid": "9f7466af946f2de32cb768dde41a8d27975a3d56aac7884329cd7b0b92d229f9",
      "grant": "10000000.00000000"
    },
    {
      "txid": "3983d64150efb63c64820debcd880d1ae579bd8b6fde04f4066d2202eb1548f9",
      "grant": "10000000.00000000"
    },
    {
      "txid": "ad148e88eb594d3c0bafcce1fa7214fd02e7d0af9c55779b03361a9501117ef9",
      "grant": "50000.00000000"
    }
  ]
}
```

```plaintext
{
  "reply": {
	"propertyid": 31,
	"name": "TetherUS",
	"issuer": "32TLn1WLcu8LtfvweLzYUYU6ubc2YV9eZs",
	"creationtxid": "5ed3694e8a4fa8d3ec5c75eb6789492c69e65511522b220e94ab51da2b6dd53f",
	"totaltokens": "1555000000.00000000",
	"issuances": [
	  {
		"txid": "f307bdf50d90c92278265cd92819c787070d6652ae3c8af46fa6a96278589b03",
		"grant": "25000000.00000000"
	  },
	  {
		"txid": "d48069d2f2d2360929948e61771ed46f6f31aaf9c75be36bdf3ebc4ec3cded04",
		"grant": "20000000.00000000"
	  },
	  {
		"txid": "49448e97bfc1ac4f3136035e76eb5dc1f5c1362aef7cf90546d39f406347ce09",
		"revoke": "400000000.00000000"
	  },
	  {
		"txid": "e30f5ce14c47406f2fd6a2a27b25f6d0a90a1317b7f92b893a93e7529d281d0c",
		"grant": "25000000.00000000"
	  },
	  {
		"txid": "a992d336afbca58178801dae30cd71308a6a9e1f8b3b9da9f87b81bde402110d",
		"grant": "20000000.00000000"
	  },
	  {
		"txid": "ce36efda15bc6cf99ba6a010e71b47b00a5ea2071a392839effe7ed392cf690f",
		"grant": "100.00000000"
	  },
	  {
		"txid": "d97b583356e5ca63d77240b637e203fdf219528133c2700234314a2c99d57410",
		"grant": "500000.00000000"
	  },
	  {
		"txid": "361ce637741ab91b5e040a572a0ff5163dc1e151d8117ff0865b619cf765981c",
		"revoke": "275000000.00000000"
	  },
	  {
		"txid": "69a4b3027895da33952d661512d67071b351e11793ca286df24b8b8df63b781d",
		"grant": "25000000.00000000"
	  },
	  {
		"txid": "ed212c3ae5319ad6b7e3a1d7461e613d44fb2ad7ac0a61fe95195d82f6fe9521",
		"grant": "25048400.00000000"
	  },
	  {
		"txid": "b8e6d591a4f61b52f7b62ab80ae37b9b4396e00c695190da44211adfabee4424",
		"grant": "24999000.00000000"
	  },
	  {
		"txid": "b33aeae5fb64ee50229f1a04ea68e0975ba053dcec07cb162c7d2d93a635ed29",
		"grant": "30000000.00000000"
	  },
	  {
		"txid": "99d41439c1bbae042af6a6b6ef14a6ef408bbadaaa42b0a2949d87345b3fb82c",
		"grant": "25000000.00000000"
	  },
	  {
		"txid": "b182888725cff4486d4080cf04736ab0d2250a78a02948cfc348d8e1672ef52c",
		"grant": "100000000.00000000"
	  },
	  {
		"txid": "aec3630a38235e9e9013816b1aa165f1744298fd01c0f7f5710f67ced3392534",
		"grant": "10000000.00000000"
	  },
	  ...      
	]
  },
  "error": null,
  "id": 1,
  "uuid": "1DE2BDB4-F02E-4B02-9C5A-E080B16DEE57"
}
```

Parameter            | Type          | Description
---------------------|---------------|-------------
propertyid           | int           | The identifier of the managed tokens.
name                 | string        | The name of the tokens.
issuer               | string        | The Bitcoin address of the issuer on record.
creationtxid         | string        | The hex-encoded creation transaction hash.
totaltokens          | string        | The total number of tokens in existence.
issuances            | Array         | A list of the granted and revoked tokens.
- txid               | string        | The hash of the transaction that granted tokens.
- grant              | string        | The number of tokens granted by this transaction.
error                | string        | API error code.
id                   | int           | ID number.
uuid                 | string        | The response ID, which can be used to view this response again with [xrGetReply](https://api.blocknet.co/#xrgetreply).





## omni_getinfo

Returns various state information of the client and protocol.

### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '[]' https://api.oracleminer.com/xrs/omni_getinfo
```

```plaintext
blocknet-cli xrService omni_getinfo
```
<code class="api-call">omni_getinfo</code>

This call does not take parameters.


### Response

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
{
  "omnicoreversion_int": 70000000,
  "omnicoreversion": "0.7.0",
  "mastercoreversion": "0.7.0",
  "bitcoincoreversion": "0.18.1",
  "block": 609727,
  "blocktime": 1577290162,
  "blocktransactions": 87,
  "totaltrades": 1867,
  "totaltransactions": 15908554,
  "alerts": [
  ]
}
```

```plaintext
{
  "reply": {
	"omnicoreversion_int": 70000000,
	"omnicoreversion": "0.7.0",
	"mastercoreversion": "0.7.0",
	"bitcoincoreversion": "0.18.1",
	"block": 609727,
	"blocktime": 1577290162,
	"blocktransactions": 87,
	"totaltrades": 1867,
	"totaltransactions": 15908554,
	"alerts": [
	]
  },
  "error": null,
  "id": 1,
  "uuid": "F7A5008B-93D5-4959-AAEB-CF9AAC3C4A4F"
}
```

Parameter              | Type          | Description
-----------------------|---------------|-------------
omnicoreversion_int    | int           | Client version as integer.
omnicoreversion        | string        | Client version.
mastercoreversion      | string        | Client version (DEPRECATED).
bitcoincoreversion     | string        | Bitcoin Core version.
commitinfo             | string        | Build commit identifier.
block                  | int           | Index of the last processed block.
blocktime              | int           | Timestamp of the last processed block.
blocktransactions      | int           | Omni transactions found in the last processed block.
totaltransactions      | int           | Omni transactions processed in total.
alerts                 | Array         | Active protocol alert (if any).
error                  | string        | API error code.
id                     | int           | ID number.
uuid                   | string        | The response ID, which can be used to view this response again with [xrGetReply](https://api.blocknet.co/#xrgetreply).





## omni_getorderbook

> Sample Data

```cli
{
  "propertyid": 1
}
```
List active offers on the distributed token exchange.


### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '[1]' https://api.oracleminer.com/xrs/omni_getorderbook
```

```plaintext
blocknet-cli xrService omni_getorderbook 1
```
<code class="api-call">omni_getorderbook [propertyid]</code>

Parameter       | Type       | Description
----------------|------------|-------------
propertyid      | int        | Filter orders by `propertyid` for sale.


### Response Parameters

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
[
  {
    "address": "1NDD5vvTaienYySNTgP1qsdYa9aHGhtaNz",
    "txid": "933020a835bfb38ea1c81c66d9cfa7d55c0ffab91e1b1083011a285064729309",
    "propertyidforsale": 1,
    "propertyidforsaleisdivisible": true,
    "amountforsale": "0.01400000",
    "amountremaining": "0.01400000",
    "propertyiddesired": 31,
    "propertyiddesiredisdivisible": true,
    "amountdesired": "5.00000000",
    "amounttofill": "5.00000000",
    "action": 1,
    "block": 403142,
    "blocktime": 1458261243
  },
  {
    "address": "1AmQiMqSk5uhkK1J9gKMD4J1dLfuSQWAR1",
    "txid": "f3f176e35025acc2eef8ba01ec6b92413da0a283e5a6918bb347033e5e76b77d",
    "propertyidforsale": 1,
    "propertyidforsaleisdivisible": true,
    "amountforsale": "5.00000000",
    "amountremaining": "5.00000000",
    "propertyiddesired": 41,
    "propertyiddesiredisdivisible": true,
    "amountdesired": "25.00000000",
    "amounttofill": "25.00000000",
    "action": 1,
    "block": 419930,
    "blocktime": 1468042929
  },
  {
    "address": "15jiVUZLqg9ExtyDdfHsjA1J5efujTBqJL",
    "txid": "cac795dfcfd92e7d3ba19c10a923fcf1153259c5e17e23a24fec57959dd3f6ec",
    "propertyidforsale": 1,
    "propertyidforsaleisdivisible": true,
    "amountforsale": "0.50000000",
    "amountremaining": "0.50000000",
    "propertyiddesired": 35,
    "propertyiddesiredisdivisible": true,
    "amountdesired": "25.00000000",
    "amounttofill": "25.00000000",
    "action": 1,
    "block": 431708,
    "blocktime": 1474945812
  },
  {
    "address": "15jiVUZLqg9ExtyDdfHsjA1J5efujTBqJL",
    "txid": "2962373721bd0fbe2085dc1f98d32546dfdc62f0bb97515747bd4a96b12f36c3",
    "propertyidforsale": 1,
    "propertyidforsaleisdivisible": true,
    "amountforsale": "0.10000000",
    "amountremaining": "0.10000000",
    "propertyiddesired": 64,
    "propertyiddesiredisdivisible": true,
    "amountdesired": "1.00000000",
    "amounttofill": "1.00000000",
    "action": 1,
    "block": 438453,
    "blocktime": 1478900035
  },
  {
    "address": "1FcfAR3qtvr13wPZr4zk2U6ZPKDMBp9ony",
    "txid": "9675e7268c863b382ce9c06081c392ed3d9a67f263fc2dd7862e72c21cce6bfc",
    "propertyidforsale": 1,
    "propertyidforsaleisdivisible": true,
    "amountforsale": "1.00000000",
    "amountremaining": "1.00000000",
    "propertyiddesired": 3,
    "propertyiddesiredisdivisible": false,
    "amountdesired": "10000",
    "amounttofill": "10000",
    "action": 1,
    "block": 441455,
    "blocktime": 1480612731
  },
  {
    "address": "1MSCjpdYe1FjMFPnUXXrpnhzYr5SCmBuAx",
    "txid": "a9ac57fd1a9a8b08109fcff96379fbc485befa802d1e23c4b0d3566e7f49e771",
    "propertyidforsale": 1,
    "propertyidforsaleisdivisible": true,
    "amountforsale": "1.00000000",
    "amountremaining": "1.00000000",
    "propertyiddesired": 102,
    "propertyiddesiredisdivisible": false,
    "amountdesired": "20",
    "amounttofill": "20",
    "action": 1,
    "block": 442844,
    "blocktime": 1481413200
  },
  {
    "address": "1MSCjpdYe1FjMFPnUXXrpnhzYr5SCmBuAx",
    "txid": "f8463a6c9c4c8ae3d5cbb77d34051e69838c47089bd57754ad07bb67ab78280a",
    "propertyidforsale": 1,
    "propertyidforsaleisdivisible": true,
    "amountforsale": "5.00000000",
    "amountremaining": "5.00000000",
    "propertyiddesired": 102,
    "propertyiddesiredisdivisible": false,
    "amountdesired": "1",
    "amounttofill": "1",
    "action": 1,
    "block": 447541,
    "blocktime": 1484081325
  },
  {
    "address": "177F3XXXE95vQS1fySD3UCJxGB2Fx6w181",
    "txid": "1f037747ec47caaabab53882a3bd1d5722e34c4ea8e9bac2d7d113a7d8b5590a",
    "propertyidforsale": 1,
    "propertyidforsaleisdivisible": true,
    "amountforsale": "24.97313600",
    "amountremaining": "24.97313600",
    "propertyiddesired": 97,
    "propertyiddesiredisdivisible": false,
    "amountdesired": "1",
    "amounttofill": "1",
    "action": 1,
    "block": 450661,
    "blocktime": 1485737495
  },
  {
    "address": "16gaSeQ1nGmoXAh1NFWUvNZC72pfzVdge2",
    "txid": "44815cbc363ae81507cfb024dd3e2f07925d88a81c5281a457ab691b1a19f620",
    "propertyidforsale": 1,
    "propertyidforsaleisdivisible": true,
    "amountforsale": "1.00000000",
    "amountremaining": "1.00000000",
    "propertyiddesired": 66,
    "propertyiddesiredisdivisible": true,
    "amountdesired": "50000.00000000",
    "amounttofill": "50000.00000000",
    "action": 1,
    "block": 472321,
    "blocktime": 1498089451
  },
  {
    "address": "13piDMgYmHJiZmoDELQJcYc5WWDQZB8w9s",
    "txid": "2cd316cbd96a65f788142e3b4d5b6d90d3c15d73444b2c9a9b1adf417546c16a",
    "propertyidforsale": 1,
    "propertyidforsaleisdivisible": true,
    "amountforsale": "1.97625510",
    "amountremaining": "0.97625510",
    "propertyiddesired": 191,
    "propertyiddesiredisdivisible": true,
    "amountdesired": "333.00000000",
    "amounttofill": "164.49948608",
    "action": 1,
    "block": 478144,
    "blocktime": 1501349314
  },
  {
    "address": "16gaSeQ1nGmoXAh1NFWUvNZC72pfzVdge2",
    "txid": "8a35bcb9245e976d1129bd64238b428a491227d65aa57af6d9c10169461bd96e",
    "propertyidforsale": 1,
    "propertyidforsaleisdivisible": true,
    "amountforsale": "8.77459945",
    "amountremaining": "0.00000001",
    "propertyiddesired": 191,
    "propertyiddesiredisdivisible": true,
    "amountdesired": "877.45994411",
    "amounttofill": "0.00000100",
    "action": 1,
    "block": 480828,
    "blocktime": 1502920692
  },
  {
    "address": "1QJLQbAUbNm5XCYr5Hci8iu8K7YC7Prubo",
    "txid": "0a74cd059b7d7aa5748e7e671de42b5594c2f70e7a718a2534b988aadf4de721",
    "propertyidforsale": 1,
    "propertyidforsaleisdivisible": true,
    "amountforsale": "0.00006000",
    "amountremaining": "0.00006000",
    "propertyiddesired": 66,
    "propertyiddesiredisdivisible": true,
    "amountdesired": "3.00000000",
    "amounttofill": "3.00000000",
    "action": 1,
    "block": 482273,
    "blocktime": 1503877324
  },
  {
    "address": "1FQsEBNQmwVNFPTkg6wZAotm6iDpwne6sZ",
    "txid": "0f5a96f9a08f94754a02e322e9f9aa3207e2e3a4b241cfa1be5e778b92831dcf",
    "propertyidforsale": 1,
    "propertyidforsaleisdivisible": true,
    "amountforsale": "5.07387299",
    "amountremaining": "0.00000299",
    "propertyiddesired": 3,
    "propertyiddesiredisdivisible": false,
    "amountdesired": "300",
    "amounttofill": "1",
    "action": 1,
    "block": 487102,
    "blocktime": 1506468536
  },
  {
    "address": "1NkyK1fAQ3aGjTGuzLHoW6HVkTRXj1xM61",
    "txid": "b35b250f349ebda82a3315217a3e5fe9812be20e59ee49d826d673b991fb46fc",
    "propertyidforsale": 1,
    "propertyidforsaleisdivisible": true,
    "amountforsale": "11.41621425",
    "amountremaining": "0.00000675",
    "propertyiddesired": 3,
    "propertyiddesiredisdivisible": false,
    "amountdesired": "675",
    "amounttofill": "1",
    "action": 1,
    "block": 488580,
    "blocktime": 1507308474
  }
]
```

```plaintext
{
  "reply": [
	{
	  "address": "1NDD5vvTaienYySNTgP1qsdYa9aHGhtaNz",
	  "txid": "933020a835bfb38ea1c81c66d9cfa7d55c0ffab91e1b1083011a285064729309",
	  "propertyidforsale": 1,
	  "propertyidforsaleisdivisible": true,
	  "amountforsale": "0.01400000",
	  "amountremaining": "0.01400000",
	  "propertyiddesired": 31,
	  "propertyiddesiredisdivisible": true,
	  "amountdesired": "5.00000000",
	  "amounttofill": "5.00000000",
	  "action": 1,
	  "block": 403142,
	  "blocktime": 1458261243
	},
	{
	  "address": "1AmQiMqSk5uhkK1J9gKMD4J1dLfuSQWAR1",
	  "txid": "f3f176e35025acc2eef8ba01ec6b92413da0a283e5a6918bb347033e5e76b77d",
	  "propertyidforsale": 1,
	  "propertyidforsaleisdivisible": true,
	  "amountforsale": "5.00000000",
	  "amountremaining": "5.00000000",
	  "propertyiddesired": 41,
	  "propertyiddesiredisdivisible": true,
	  "amountdesired": "25.00000000",
	  "amounttofill": "25.00000000",
	  "action": 1,
	  "block": 419930,
	  "blocktime": 1468042929
	},
	{
	  "address": "15jiVUZLqg9ExtyDdfHsjA1J5efujTBqJL",
	  "txid": "cac795dfcfd92e7d3ba19c10a923fcf1153259c5e17e23a24fec57959dd3f6ec",
	  "propertyidforsale": 1,
	  "propertyidforsaleisdivisible": true,
	  "amountforsale": "0.50000000",
	  "amountremaining": "0.50000000",
	  "propertyiddesired": 35,
	  "propertyiddesiredisdivisible": true,
	  "amountdesired": "25.00000000",
	  "amounttofill": "25.00000000",
	  "action": 1,
	  "block": 431708,
	  "blocktime": 1474945812
	},
	{
	  "address": "15jiVUZLqg9ExtyDdfHsjA1J5efujTBqJL",
	  "txid": "2962373721bd0fbe2085dc1f98d32546dfdc62f0bb97515747bd4a96b12f36c3",
	  "propertyidforsale": 1,
	  "propertyidforsaleisdivisible": true,
	  "amountforsale": "0.10000000",
	  "amountremaining": "0.10000000",
	  "propertyiddesired": 64,
	  "propertyiddesiredisdivisible": true,
	  "amountdesired": "1.00000000",
	  "amounttofill": "1.00000000",
	  "action": 1,
	  "block": 438453,
	  "blocktime": 1478900035
	},
	{
	  "address": "1FcfAR3qtvr13wPZr4zk2U6ZPKDMBp9ony",
	  "txid": "9675e7268c863b382ce9c06081c392ed3d9a67f263fc2dd7862e72c21cce6bfc",
	  "propertyidforsale": 1,
	  "propertyidforsaleisdivisible": true,
	  "amountforsale": "1.00000000",
	  "amountremaining": "1.00000000",
	  "propertyiddesired": 3,
	  "propertyiddesiredisdivisible": false,
	  "amountdesired": "10000",
	  "amounttofill": "10000",
	  "action": 1,
	  "block": 441455,
	  "blocktime": 1480612731
	},
	{
	  "address": "1MSCjpdYe1FjMFPnUXXrpnhzYr5SCmBuAx",
	  "txid": "a9ac57fd1a9a8b08109fcff96379fbc485befa802d1e23c4b0d3566e7f49e771",
	  "propertyidforsale": 1,
	  "propertyidforsaleisdivisible": true,
	  "amountforsale": "1.00000000",
	  "amountremaining": "1.00000000",
	  "propertyiddesired": 102,
	  "propertyiddesiredisdivisible": false,
	  "amountdesired": "20",
	  "amounttofill": "20",
	  "action": 1,
	  "block": 442844,
	  "blocktime": 1481413200
	},
	{
	  "address": "1MSCjpdYe1FjMFPnUXXrpnhzYr5SCmBuAx",
	  "txid": "f8463a6c9c4c8ae3d5cbb77d34051e69838c47089bd57754ad07bb67ab78280a",
	  "propertyidforsale": 1,
	  "propertyidforsaleisdivisible": true,
	  "amountforsale": "5.00000000",
	  "amountremaining": "5.00000000",
	  "propertyiddesired": 102,
	  "propertyiddesiredisdivisible": false,
	  "amountdesired": "1",
	  "amounttofill": "1",
	  "action": 1,
	  "block": 447541,
	  "blocktime": 1484081325
	},
	{
	  "address": "177F3XXXE95vQS1fySD3UCJxGB2Fx6w181",
	  "txid": "1f037747ec47caaabab53882a3bd1d5722e34c4ea8e9bac2d7d113a7d8b5590a",
	  "propertyidforsale": 1,
	  "propertyidforsaleisdivisible": true,
	  "amountforsale": "24.97313600",
	  "amountremaining": "24.97313600",
	  "propertyiddesired": 97,
	  "propertyiddesiredisdivisible": false,
	  "amountdesired": "1",
	  "amounttofill": "1",
	  "action": 1,
	  "block": 450661,
	  "blocktime": 1485737495
	},
	{
	...
	}
  ],
  "error": null,
  "id": 1,
  "uuid": "0FB125C4-4408-4B5C-8900-D9CCB0077288"
}
```

Parameter                     | Type          | Description
------------------------------|---------------|-------------
address                       | string        | The Bitcoin address of the trader.
txid                          | string        | The hex-encoded hash of the transaction of the order.
ecosystem                     | string        | The ecosytem in which the order was made (if "cancel-ecosystem").
propertyidforsale             | int           | The identifier of the tokens put up for sale.
propertyidforsaleisdivisible  | boolean       | Whether the tokens for sale are divisible.
amountforsale                 | string        | The amount of tokens initially offered.
amountremaining               | string        | The amount of tokens still up for sale.
propertydesired               | int           | The identifier of the tokens desired in exchange.
propertyiddesiredisdivisible  | boolean       | Whether the desired tokens are divisible.
amountdesired                 | string        | The amount of tokens initially desired.
amounttofill                  | string        | The amount of tokens still needed to fill the offer completely.
action                        | int           | The action of the transaction: (1) "trade", (2) "cancel-price", (3) "cancel-pair", (4) "cancel-ecosystem".
block                         | int           | The index of the block that contains the transaction.
blocktime                     | int           | The timestamp of the block that contains the transaction.
error                         | string        | API error code.
id                            | int           | ID number.
uuid                          | string        | The response ID, which can be used to view this response again with [xrGetReply](https://api.blocknet.co/#xrgetreply).





## omni_getpayload

> Sample Data

```cli
{
  "txid": "2a9aa70ed7aa84d7976271e464592fb055f51d5e59c8d544d44e6a9115f4061d"
}
```
Get the payload for an Omni transaction.


### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '["2a9aa70ed7aa84d7976271e464592fb055f51d5e59c8d544d44e6a9115f4061d"]' https://api.oracleminer.com/xrs/omni_getpayload
```

```plaintext
blocknet-cli xrService omni_getpayload 2a9aa70ed7aa84d7976271e464592fb055f51d5e59c8d544d44e6a9115f4061d
```
<code class="api-call">omni_getpayload [txid]</code>

Parameter       | Type       | Description
----------------|------------|-------------
txid            | string     | The hash of the transaction to retrieve payload.

### Response Parameters

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
{
  "payload": "000000000000001f00000011a5db9c20",
  "payloadsize": 16
}
```

```plaintext
{
  "reply": {
	"payload": "000000000000001f00000011a5db9c20",
	"payloadsize": 16
  },
  "error": null,
  "id": 1,
  "uuid": "000332B3-5910-4FB8-A3B4-9BF4CB40A516"
}
```

Parameter               | Type          | Description
------------------------|---------------|-------------
payload                 | string        | The decoded Omni payload message.
payloadsize             | int           | The size of the payload.
error                   | string        | API error code.
id                      | int           | ID number.
uuid                    | string        | The response ID, which can be used to view this response again with [xrGetReply](https://api.blocknet.co/#xrgetreply).





## omni_getproperty

> Sample Data

```cli
{
  "propertyid": 1
}
```
Returns details about the tokens or smart property to lookup.


### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '[1]' https://api.oracleminer.com/xrs/omni_getproperty
```

```plaintext
blocknet-cli xrService omni_getproperty 1
```
<code class="api-call">omni_getproperty [propertyid]</code>

Parameter       | Type       | Description
----------------|------------|-------------
propertyid      | int        | The identifier of the tokens or property.


### Response Parameters

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
{
  "propertyid": 1,
  "name": "Omni tokens",
  "category": "N/A",
  "subcategory": "N/A",
  "data": "Omni tokens serve as the binding between Bitcoin, smart properties and contracts created on the Omni Layer.",
  "url": "http://www.omnilayer.org",
  "divisible": true,
  "issuer": "1EXoDusjGwvnjZUyKkxZ4UHEf77z6A5S4P",
  "creationtxid": "0000000000000000000000000000000000000000000000000000000000000000",
  "fixedissuance": false,
  "managedissuance": false,
  "totaltokens": "618827.28474172"
}
```

```plaintext
{
  "reply": {
	"propertyid": 1,
	"name": "Omni tokens",
	"category": "N/A",
	"subcategory": "N/A",
	"data": "Omni tokens serve as the binding between Bitcoin, smart properties and contracts created on the Omni Layer.",
	"url": "http://www.omnilayer.org",
	"divisible": true,
	"issuer": "1EXoDusjGwvnjZUyKkxZ4UHEf77z6A5S4P",
	"creationtxid": "0000000000000000000000000000000000000000000000000000000000000000",
	"fixedissuance": false,
	"managedissuance": false,
	"totaltokens": "618774.78134507"
  },
  "error": null,
  "id": 1,
  "uuid": "71B5128A-202E-4654-9E7F-9BE73BAE333F"
}
```

Parameter               | Type          | Description
------------------------|---------------|-------------
propertyid              | int           | The identifier.
name                    | string        | The name of the tokens.
category                | string        | The category used for the tokens.
subcategory             | string        | The subcategory used for the tokens.
data                    | string        | Additional information or a description.
url                     | string        | An URI, for example pointing to a website.
divisible               | boolean       | Whether the tokens are divisible
issuer                  | string        | The Bitcoin address of the issuer on record.
creationtxid            | string        | The hex-encoded creation transaction hash.
fixedissuance           | boolean       | Whether the token supply is fixed.
managedissuance         | boolean       | Whether the token supply is managed by the issuer
freezingenabled         | boolean       | Whether freezing is enabled for the property (managed properties only).
totaltokens             | string        | The total number of tokens in existence.
error                   | string        | API error code.
id                      | int           | ID number.
uuid                    | string        | The response ID, which can be used to view this response again with [xrGetReply](https://api.blocknet.co/#xrgetreply).





## omni_getseedblocks

> Sample Data

```cli
{
  "startblock": 310001,
  "endblock": 310010
}
```
Returns a list of blocks containing Omni transactions for use in seed block filtering.


### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '[310001,310010]' https://api.oracleminer.com/xrs/omni_getseedblocks
```

```plaintext
blocknet-cli xrService omni_getseedblocks 310001 310010
```
<code class="api-call">omni_getseedblocks [startblock] [endblock]</code>

Parameter       | Type       | Description
----------------|------------|-------------
startblock      | int        | The first block to look for Omni transactions (inclusive).
endblock        | int        | The last block to look for Omni transactions (inclusive).

### Response Parameters

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
[
  310001,
  310003,
  310004,
  310006,
  310007
]
```

```plaintext
{
  "reply": [
	310001,
	310003,
	310004,
	310006,
	310007
  ],
  "error": null,
  "id": 1,
  "uuid": "0B71423F-0025-4A14-B3DA-059DCB1E79F2"
}
```

Parameter            | Type          | Description
---------------------|---------------|-------------
[]                   | Array         | A list of seed blocks.
- block              | int           | The block height of the seed block.
error                | string        | API error code.
id                   | int           | ID number.
uuid                 | string        | The response ID, which can be used to view this response again with [xrGetReply](https://api.blocknet.co/#xrgetreply).





## omni_getsto

> Sample Data

```cli
{
  "txid": "2a9aa70ed7aa84d7976271e464592fb055f51d5e59c8d544d44e6a9115f4061d",
  "recipientfilter": "*"
}
```
Get information and recipients of a send-to-owners transaction.


### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '["2a9aa70ed7aa84d7976271e464592fb055f51d5e59c8d544d44e6a9115f4061d","*"]' https://api.oracleminer.com/xrs/omni_getsto
```

```plaintext
blocknet-cli xrService omni_getsto 2a9aa70ed7aa84d7976271e464592fb055f51d5e59c8d544d44e6a9115f4061d *
```
<code class="api-call">omni_getsto [txid] [recipientfilter]</code>

Parameter       | Type       | Description
----------------|------------|-------------
txid            | string     | The hash of the transaction to lookup.
recipientfilter | string     | A filter for recipients (wallet by default, "*" for all).

### Response Parameters

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
{
  "txid": "2a9aa70ed7aa84d7976271e464592fb055f51d5e59c8d544d44e6a9115f4061d",
  "fee": "0.00089100",
  "sendingaddress": "12qcBeVQXA3MQfedQr2zwRFXMT8FtExk87",
  "referenceaddress": "19gs72noReqnYw2YU1hAPW5izgKqHoJMXe",
  "ismine": false,
  "version": 0,
  "type_int": 0,
  "type": "Simple Send",
  "propertyid": 31,
  "divisible": true,
  "amount": "757.97077024",
  "valid": true,
  "blockhash": "00000000000000000011c1dab569f6de00fdc2d298d5aa700e329316385d0890",
  "blocktime": 1577503605,
  "positioninblock": 5,
  "block": 610086,
  "confirmations": 6210
}
```

```plaintext
{
  "reply": {
	"txid": "2a9aa70ed7aa84d7976271e464592fb055f51d5e59c8d544d44e6a9115f4061d",
	"fee": "0.00089100",
	"sendingaddress": "12qcBeVQXA3MQfedQr2zwRFXMT8FtExk87",
	"referenceaddress": "19gs72noReqnYw2YU1hAPW5izgKqHoJMXe",
	"ismine": false,
	"version": 0,
	"type_int": 0,
	"type": "Simple Send",
	"propertyid": 31,
	"divisible": true,
	"amount": "757.97077024",
	"valid": true,
	"blockhash": "00000000000000000011c1dab569f6de00fdc2d298d5aa700e329316385d0890",
	"blocktime": 1577503605,
	"positioninblock": 5,
	"block": 610086,
	"confirmations": 3
  },
  "error": null,
  "id": 1,
  "uuid": "BBFC37C9-7103-4204-8612-9D5EB6A079C2"
}
```

Parameter            | Type          | Description
---------------------|---------------|-------------
txid                 | string        | The hex-encoded hash of the transaction.
fee                  | string        | The transaction fee in bitcoins.
sendingaddress       | string        | The Bitcoin address of the sender.
referenceaddress     | string        | A Bitcoin address used as reference (if any).
ismine               | boolean       | Whether the transaction involes an address in the wallet.
version              | int           | The transaction version.
type_int             | int           | The transaction type as number.
type                 | string        | The transaction type as string.
propertyid           | int           | The identifier of sent tokens.
divisble             | boolean       | Whether the sent tokens are divisible.
amount               | string        | The number of tokens sent to owners.
valid                | boolean       | Whether the transaction is valid.
blockhash            | string        | The hash of the corresponding block.
blocktime            | int           | The timestamp of the block that contains the transaction.
positioninblock      | int           | The position (index) of the transaction within the block.
block                | int           | The index of the block this consensus hash applies to.
confirmations        | int           | The number of transaction confirmations.
error                | string        | API error code.
id                   | int           | ID number.
uuid                 | string        | The response ID, which can be used to view this response again with [xrGetReply](https://api.blocknet.co/#xrgetreply).





## omni_gettrade

> Sample Data

```cli
{
  "txid": "2a9aa70ed7aa84d7976271e464592fb055f51d5e59c8d544d44e6a9115f4061d"
}
```
Get detailed information and trade matches for orders on the distributed token exchange.


### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '["2a9aa70ed7aa84d7976271e464592fb055f51d5e59c8d544d44e6a9115f4061d"]' https://api.oracleminer.com/xrs/omni_gettrade
```

```plaintext
blocknet-cli xrService omni_gettrade 2a9aa70ed7aa84d7976271e464592fb055f51d5e59c8d544d44e6a9115f4061d
```
<code class="api-call">omni_gettrade [txid]</code>

Parameter       | Type       | Description
----------------|------------|-------------
txid            | string     | The hash of the order to lookup.

### Response Parameters

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
{
  "txid": "2a9aa70ed7aa84d7976271e464592fb055f51d5e59c8d544d44e6a9115f4061d",
  "fee": "0.00089100",
  "sendingaddress": "12qcBeVQXA3MQfedQr2zwRFXMT8FtExk87",
  "referenceaddress": "19gs72noReqnYw2YU1hAPW5izgKqHoJMXe",
  "ismine": false,
  "version": 0,
  "type_int": 0,
  "type": "Simple Send",
  "propertyid": 31,
  "divisible": true,
  "amount": "757.97077024",
  "valid": true,
  "blockhash": "00000000000000000011c1dab569f6de00fdc2d298d5aa700e329316385d0890",
  "blocktime": 1577503605,
  "positioninblock": 5,
  "block": 610086,
  "confirmations": 6210
}
```

```plaintext
{
  "reply": {
	"txid": "2a9aa70ed7aa84d7976271e464592fb055f51d5e59c8d544d44e6a9115f4061d",
	"fee": "0.00089100",
	"sendingaddress": "12qcBeVQXA3MQfedQr2zwRFXMT8FtExk87",
	"referenceaddress": "19gs72noReqnYw2YU1hAPW5izgKqHoJMXe",
	"ismine": false,
	"version": 0,
	"type_int": 0,
	"type": "Simple Send",
	"propertyid": 31,
	"divisible": true,
	"amount": "757.97077024",
	"valid": true,
	"blockhash": "00000000000000000011c1dab569f6de00fdc2d298d5aa700e329316385d0890",
	"blocktime": 1577503605,
	"positioninblock": 5,
	"block": 610086,
	"confirmations": 6
  },
  "error": null,
  "id": 1,
  "uuid": "FC5A8C16-5E04-4E04-9CFB-9F7E7F7ABBF4"
}
```

Parameter            | Type          | Description
---------------------|---------------|-------------
txid                 | string        | The hex-encoded hash of the transaction.
fee                  | string        | The transaction fee in bitcoins.
sendingaddress       | string        | The Bitcoin address of the sender.
referenceaddress     | string        | A Bitcoin address used as reference (if any).
ismine               | boolean       | Whether the transaction involes an address in the wallet.
version              | int           | The transaction version.
type_int             | int           | The transaction type as number.
type                 | string        | The transaction type as string.
propertyid           | int           | The identifier of sent tokens.
divisble             | boolean       | Whether the sent tokens are divisible.
amount               | string        | The number of tokens sent to owners.
valid                | boolean       | Whether the transaction is valid.
blockhash            | string        | The hash of the corresponding block.
blocktime            | int           | The timestamp of the block that contains the transaction.
positioninblock      | int           | The position (index) of the transaction within the block.
block                | int           | The index of the block this consensus hash applies to.
confirmations        | int           | The number of transaction confirmations.
error                | string        | API error code.
id                   | int           | ID number.
uuid                 | string        | The response ID, which can be used to view this response again with [xrGetReply](https://api.blocknet.co/#xrgetreply).





## omni_gettradehistoryforaddress

> Sample Data

```cli
{
  "address": "1NDD5vvTaienYySNTgP1qsdYa9aHGhtaNz",
  "count": 10
}
```
Retrieves the history of orders on the distributed exchange for the supplied address.


### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '["1NDD5vvTaienYySNTgP1qsdYa9aHGhtaNz",10]' https://api.oracleminer.com/xrs/omni_gettradehistoryforaddress
```

```plaintext
blocknet-cli xrService omni_gettradehistoryforaddress 1NDD5vvTaienYySNTgP1qsdYa9aHGhtaNz 10
```
<code class="api-call">omni_gettradehistoryforaddress [address] [count]</code>

Parameter       | Type       | Description
----------------|------------|-------------
address         | string     | Address to retrieve history for.
count           | int        | Number of orders to retrieve (default: `10`).

### Response Parameters

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
[
  {
    "txid": "3403498e043ee6236dcaf80a4e5173ede53d275915d6c9ae91455d10c4c5c86d",
    "fee": "0.00002344",
    "sendingaddress": "1NDD5vvTaienYySNTgP1qsdYa9aHGhtaNz",
    "ismine": false,
    "version": 0,
    "type_int": 25,
    "type": "MetaDEx trade",
    "propertyidforsale": 31,
    "propertyidforsaleisdivisible": true,
    "amountforsale": "4.00000000",
    "propertyiddesired": 1,
    "propertyiddesiredisdivisible": true,
    "amountdesired": "12.00000000",
    "unitprice": "3.00000000000000000000000000000000000000000000000000",
    "amountremaining": "4.00000000",
    "amounttofill": "12.00000000",
    "status": "open",
    "matches": [],
    "valid": true,
    "blockhash": "000000000000000002db8b2b491d4fb6a56e498787b9c8174fcb190294e01560",
    "blocktime": 1458275616,
    "positioninblock": 1543,
    "block": 403167,
    "confirmations": 213129
  },
  {
    "txid": "933020a835bfb38ea1c81c66d9cfa7d55c0ffab91e1b1083011a285064729309",
    "fee": "0.00002427",
    "sendingaddress": "1NDD5vvTaienYySNTgP1qsdYa9aHGhtaNz",
    "ismine": false,
    "version": 0,
    "type_int": 25,
    "type": "MetaDEx trade",
    "propertyidforsale": 1,
    "propertyidforsaleisdivisible": true,
    "amountforsale": "0.01400000",
    "propertyiddesired": 31,
    "propertyiddesiredisdivisible": true,
    "amountdesired": "5.00000000",
    "unitprice": "357.14285714285714285714285714285714285714285714285714",
    "amountremaining": "0.01400000",
    "amounttofill": "5.00000000",
    "status": "open",
    "matches": [],
    "valid": true,
    "blockhash": "000000000000000005db86b40b868beac74995dd4367c6fc16ccace31bac3be6",
    "blocktime": 1458261243,
    "positioninblock": 648,
    "block": 403142,
    "confirmations": 213154
  },
  {
    "txid": "e361b8ffb8ebb9fbe81a3098db16b2c09e3c6be966cea2864def4d7da53814df",
    "fee": "0.00002360",
    "sendingaddress": "1NDD5vvTaienYySNTgP1qsdYa9aHGhtaNz",
    "ismine": false,
    "version": 0,
    "type_int": 25,
    "type": "MetaDEx trade",
    "propertyidforsale": 31,
    "propertyidforsaleisdivisible": true,
    "amountforsale": "5.00000000",
    "propertyiddesired": 1,
    "propertyiddesiredisdivisible": true,
    "amountdesired": "14.00000000",
    "unitprice": "2.80000000000000000000000000000000000000000000000000",
    "status": "filled",
    "matches": [
      {
        "txid": "901243a35ee2d3823af280ab356bfe0a6285dae9d7acb986159a40029d050be3",
        "block": 403140,
        "address": "11NiSNoGYomEA3ZHEN4R9ne4kwDjECsAy",
        "amountsold": "5.00000000",
        "amountreceived": "14.00000000",
        "tradingfee": "0.00000000"
      }
    ],
    "valid": true,
    "blockhash": "0000000000000000006450845df439ea4baddf884d87d91c088df0b33693e80d",
    "blocktime": 1458259438,
    "positioninblock": 925,
    "block": 403140,
    "confirmations": 213156
  }
]
```

```plaintext
{
  "reply": [
	{
	  "txid": "3403498e043ee6236dcaf80a4e5173ede53d275915d6c9ae91455d10c4c5c86d",
	  "fee": "0.00002344",
	  "sendingaddress": "1NDD5vvTaienYySNTgP1qsdYa9aHGhtaNz",
	  "ismine": false,
	  "version": 0,
	  "type_int": 25,
	  "type": "MetaDEx trade",
	  "propertyidforsale": 31,
	  "propertyidforsaleisdivisible": true,
	  "amountforsale": "4.00000000",
	  "propertyiddesired": 1,
	  "propertyiddesiredisdivisible": true,
	  "amountdesired": "12.00000000",
	  "unitprice": "3.00000000000000000000000000000000000000000000000000",
	  "amountremaining": "4.00000000",
	  "amounttofill": "12.00000000",
	  "status": "open",
	  "matches": [
	  ],
	  "valid": true,
	  "blockhash": "000000000000000002db8b2b491d4fb6a56e498787b9c8174fcb190294e01560",
	  "blocktime": 1458275616,
	  "positioninblock": 1543,
	  "block": 403167,
	  "confirmations": 206927
	},
	{
	  "txid": "933020a835bfb38ea1c81c66d9cfa7d55c0ffab91e1b1083011a285064729309",
	  "fee": "0.00002427",
	  "sendingaddress": "1NDD5vvTaienYySNTgP1qsdYa9aHGhtaNz",
	  "ismine": false,
	  "version": 0,
	  "type_int": 25,
	  "type": "MetaDEx trade",
	  "propertyidforsale": 1,
	  "propertyidforsaleisdivisible": true,
	  "amountforsale": "0.01400000",
	  "propertyiddesired": 31,
	  "propertyiddesiredisdivisible": true,
	  "amountdesired": "5.00000000",
	  "unitprice": "357.14285714285714285714285714285714285714285714285714",
	  "amountremaining": "0.01400000",
	  "amounttofill": "5.00000000",
	  "status": "open",
	  "matches": [
	  ],
	  "valid": true,
	  "blockhash": "000000000000000005db86b40b868beac74995dd4367c6fc16ccace31bac3be6",
	  "blocktime": 1458261243,
	  "positioninblock": 648,
	  "block": 403142,
	  "confirmations": 206952
	},
	{
	  "txid": "e361b8ffb8ebb9fbe81a3098db16b2c09e3c6be966cea2864def4d7da53814df",
	  "fee": "0.00002360",
	  "sendingaddress": "1NDD5vvTaienYySNTgP1qsdYa9aHGhtaNz",
	  "ismine": false,
	  "version": 0,
	  "type_int": 25,
	  "type": "MetaDEx trade",
	  "propertyidforsale": 31,
	  "propertyidforsaleisdivisible": true,
	  "amountforsale": "5.00000000",
	  "propertyiddesired": 1,
	  "propertyiddesiredisdivisible": true,
	  "amountdesired": "14.00000000",
	  "unitprice": "2.80000000000000000000000000000000000000000000000000",
	  "status": "filled",
	  "matches": [
		{
		  "txid": "901243a35ee2d3823af280ab356bfe0a6285dae9d7acb986159a40029d050be3",
		  "block": 403140,
		  "address": "11NiSNoGYomEA3ZHEN4R9ne4kwDjECsAy",
		  "amountsold": "5.00000000",
		  "amountreceived": "14.00000000",
		  "tradingfee": "0.00000000"
		}
	  ],
	  "valid": true,
	  "blockhash": "0000000000000000006450845df439ea4baddf884d87d91c088df0b33693e80d",
	  "blocktime": 1458259438,
	  "positioninblock": 925,
	  "block": 403140,
	  "confirmations": 206954
	}
  ],
  "error": null,
  "id": 1,
  "uuid": "F4B26E93-9032-433A-97A7-EFE96E9ACEA4"
}
```

Parameter                     | Type          | Description
------------------------------|---------------|-------------
txid                          | string        | The hex-encoded hash of the transaction.
fee                           | string        | The transaction fee in bitcoins.
sendingaddress                | string        | The Bitcoin address of the sender.
ismine                        | boolean       | Whether the transaction involes an address in the wallet.
version                       | int           | The transaction version.
type_int                      | int           | The transaction type as number.
type                          | string        | The transaction type as string.
propertyidforsale             | int           | The identifier of the tokens put up for sale.
propertyidforsaleisdivisible  | boolean       | Whether the tokens for sale are divisible.
amountforsale                 | string        | The amount of tokens initially offered.
propertyiddesired             | int           | The identifier of the tokens desired in exchange.
propertyiddesiredisdivisible  | boolean       | Whether the desired tokens are divisible.
amountdesired                 | string        | The amount of tokens initially desired.
unitprice                     | string        | The unit price (shown in the property desired).
status                        | string        | The status of the order ("open", "cancelled", "filled", ...).
matches                       | Array         | A list of matched orders and executed trades.
valid                         | boolean       | Whether the transaction is valid.
blockhash                     | string        | The hash of the corresponding block.
blocktime                     | int           | The timestamp of the block that contains the transaction.
positioninblock               | int           | The position (index) of the transaction within the block.
block                         | int           | The index of the block this consensus hash applies to.
confirmations                 | int           | The number of transaction confirmations.
error                         | string        | API error code.
id                            | int           | ID number.
uuid                          | string        | The response ID, which can be used to view this response again with [xrGetReply](https://api.blocknet.co/#xrgetreply).





## omni_gettradehistoryforpair

> Sample Data

```cli
{
  "propertyid": 1,
  "propertyidsecond": 2,
  "count": 10
}
```
Retrieves the history of trades on the distributed token exchange for the specified market.


### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '[1,2,10]' https://api.oracleminer.com/xrs/omni_gettradehistoryforpair
```

```plaintext
blocknet-cli xrService omni_gettradehistoryforpair 1 2 10
```
<code class="api-call">omni_gettradehistoryforpair [propertyid] [propertyidsecond] [count]</code>

Parameter        | Type       | Description
-----------------|------------|-------------
propertyid       | int        | The first side of the traded pair.
propertyidsecond | int        | The second side of the traded pair.
count            | int        | Number of trades to retrieve (default: `10`).


### Response Parameters

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
{
  "result": null,
  "error": null,
  "id": 1
}
```

```plaintext
{
  "reply": {
    "result": null,
    "error": null,
    "id": 1
  },
  "uuid": "B798BAF3-F1BB-4072-AE98-814455EF251C"
}
```

Parameter                     | Type          | Description
------------------------------|---------------|-------------
block                         | int           | The index of the block that contains the trade match.
unitprice                     | string        | The unit price used to execute this trade (received/sold).
inverseprice                  | string        | The inverse unit price (sold/received).
sellertxid                    | string        | The hash of the transaction of the seller.
address                       | string        | The Bitcoin address of the seller.
amountsold                    | string        | The number of tokens sold in this trade.
amountreceived                | string        | The number of tokens traded in exchange.
matchingtxid                  | string        | The hash of the transaction that was matched against.
matchingaddress               | string        | The Bitcoin address of the other party of this trade.
error                         | string        | API error code.
id                            | int           | ID number.
uuid                          | string        | The response ID, which can be used to view this response again with [xrGetReply](https://api.blocknet.co/#xrgetreply).





## omni_gettransaction

> Sample Data

```cli
{
  "txid": "2a9aa70ed7aa84d7976271e464592fb055f51d5e59c8d544d44e6a9115f4061d"
}
```
Get detailed information about an Omni transaction.


### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '["2a9aa70ed7aa84d7976271e464592fb055f51d5e59c8d544d44e6a9115f4061d"]' https://api.oracleminer.com/xrs/omni_gettransaction
```

```plaintext
blocknet-cli xrService omni_gettransaction 2a9aa70ed7aa84d7976271e464592fb055f51d5e59c8d544d44e6a9115f4061d
```
<code class="api-call">omni_gettransaction [txid]</code>

Parameter       | Type       | Description
----------------|------------|-------------
txid            | string     | The hash of the transaction to lookup.

### Response Parameters

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
{
  "txid": "2a9aa70ed7aa84d7976271e464592fb055f51d5e59c8d544d44e6a9115f4061d",
  "fee": "0.00089100",
  "sendingaddress": "12qcBeVQXA3MQfedQr2zwRFXMT8FtExk87",
  "referenceaddress": "19gs72noReqnYw2YU1hAPW5izgKqHoJMXe",
  "ismine": false,
  "version": 0,
  "type_int": 0,
  "type": "Simple Send",
  "propertyid": 31,
  "divisible": true,
  "amount": "757.97077024",
  "valid": true,
  "blockhash": "00000000000000000011c1dab569f6de00fdc2d298d5aa700e329316385d0890",
  "blocktime": 1577503605,
  "positioninblock": 5,
  "block": 610086,
  "confirmations": 6210
}
```

```plaintext
{
  "reply": {
	"txid": "2a9aa70ed7aa84d7976271e464592fb055f51d5e59c8d544d44e6a9115f4061d",
	"fee": "0.00089100",
	"sendingaddress": "12qcBeVQXA3MQfedQr2zwRFXMT8FtExk87",
	"referenceaddress": "19gs72noReqnYw2YU1hAPW5izgKqHoJMXe",
	"ismine": false,
	"version": 0,
	"type_int": 0,
	"type": "Simple Send",
	"propertyid": 31,
	"divisible": true,
	"amount": "757.97077024",
	"valid": true,
	"blockhash": "00000000000000000011c1dab569f6de00fdc2d298d5aa700e329316385d0890",
	"blocktime": 1577503605,
	"positioninblock": 5,
	"block": 610086,
	"confirmations": 12
  },
  "error": null,
  "id": 1,
  "uuid": "8230D9E7-1EAF-4908-AA62-EBD1FB066B72"
}
```

Parameter            | Type          | Description
---------------------|---------------|-------------
txid                 | string        | The hex-encoded hash of the transaction.
fee                  | string        | The transaction fee in bitcoins.
sendingaddress       | string        | The Bitcoin address of the sender.
referenceaddress     | string        | A Bitcoin address used as reference (if any).
ismine               | boolean       | Whether the transaction involes an address in the wallet.
version              | int           | The transaction version.
type_int             | int           | The transaction type as number.
type                 | string        | The transaction type as string.
propertyid           | int           | The identifier of sent tokens.
divisble             | boolean       | Whether the sent tokens are divisible.
amount               | string        | The number of tokens sent to owners.
valid                | boolean       | Whether the transaction is valid.
blockhash            | string        | The hash of the corresponding block.
blocktime            | int           | The timestamp of the block that contains the transaction.
positioninblock      | int           | The position (index) of the transaction within the block.
block                | int           | The index of the block this consensus hash applies to.
confirmations        | int           | The number of transaction confirmations.
error                | string        | API error code.
id                   | int           | ID number.
uuid                 | string        | The response ID, which can be used to view this response again with [xrGetReply](https://api.blocknet.co/#xrgetreply).





## omni_listblocktransactions

> Sample Data

```cli
{
  "index": 610097
}
```
Lists all Omni transactions in a block.


### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '[610097]' https://api.oracleminer.com/xrs/omni_listblocktransactions
```

```plaintext
blocknet-cli xrService omni_listblocktransactions 610097
```
<code class="api-call">omni_listblocktransactions [index]</code>

Parameter       | Type       | Description
----------------|------------|-------------
index           | int        | The block height or block index.

### Response Parameters

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
[
  "1966bd3242231015eb62f8f9095469580a9cfff494441fcb6263ed9788d30dd1",
  "fd68069e742112113cdbef9607f9f95708989148746d00c4813404fc7052fe9e",
  "6b0e75084d1671579151042413118d12dcd89dae5259b2fa51a3c7d72d1c07cc",
  "feaf3f0c1116923f797c870b10965192e08e2354ecb410fc2c5345aafbf925b9",
  "a5555a23ad42589f66b6fb07deb262e7538624be90a1665ac57bc0984ca919d6",
  "aee381ac13327ffd6930e077ca09f8608c8511bdb7ce17deec50397ba1d9231c",
  "2cc37bb6073a6b6e7f3d57873368c45ce587da63c833f2b756fbc9004d9146d8",
  "fb1d1b85413d31f0e5b472b2d2536b258be79b82d7b47f40f885b8cbe20f7019",
  "450770aed3887a7f956ae43d5b8233359315c236100020010e8c388eb5cc6c0f",
  "f417c80b60c636771575da2ffe6caff423a08030c6e4737a98fb01aa6ba83901",
  "7ae0253b5fed011c1b0af15f5e4c3d2548f2bb86de917d76eb343ef87d6f14c3",
  "d3b8e35f692bb2cd8d2dd8e2d3994346f57f68b3d8bf2b553a0eb073b66c3a24",
  "c34181520a3d6d8a4bb7777d6fcba02b223de869cd3d538b99d61b40bdd28a57",
  "35506d57b70a55dc86a58884af217136d14b53bcef7a66d0d02fd586b85832dd",
  "ff2c473041b9e8022a949a46210ed42cfa1a3c696e4f6edc696b5e80731c5a33",
  "58c2fe03b1e81466dfee724d551f744715e1f6da981b5e4283d4e046c570f812",
  "7900cf55c420bc074ff25beebd3d1acd58a6bb7c6ba379f748ed4916a7a56517",
  "c05371f089d002302f757937779e3a91784704d10f40b186e23147d811b3b349",
  "7a4abc1b812083954521065bdd813158ca3cc8ddad513be52a82197115c03520",
  "00b725a3c0cbf59df22f450bcc0be91539cd58d38c6c343f053f7661b906939a",
  "0b7c8b590b6eeeda79ae6a524c9557b79449d413c5f98e8131e13817fe0fb7a5",
  "b11cccc82dd643ced2ff2e3f6fe0e699cc572ffff7ca1a3812f9e68a2c7d14c6",
  "6f89977bf6aa2598015ded10a57dbbb6c2a1a92d611144d41814eb6c4b661b57",
  "406bfcca5ef96007fceca0300f4140f294d26777ea8cc547a955a062cfdb7ddb",
  "c4b47710b30f88d852ef43a41491d9b04e7717ab7416e4481417b30a69c65104",
  "114f378f6a38f0d5b1b9f46349b14bfc7b605b7b588a348882e05a4f44b64224",
  "f4b8c4faba2a9d3e096791d98de26ba8c84174506dc8d6cf895ec7177da1b52b",
  "861821aa307e8aee76009f4c588f9a294d15c15ed064a80149f374c551b73935",
  "fd8052e1fc8cdf95193c54bebf3ce460552a839cca56015381f320bdbb268d6d",
  "3c448e30fc1682bb3ff6936d4d8256b8dc428d8308791bc5ea9f8fd744cd5477",
  "05e0db50b0c5b922719967bfe44700ebd2414c99ed5305dc2d61b98f21091f88",
  "bcce7c1c1a4fbea67f6d31e91e10c90b5190f09a80a8639c379a18469fd9c2c3",
  "ee804bd62b06f1825b30e09cfe24c2c36f50c426f31125e61e560b8ce27978c5",
  "f641b95e99eb392e682272bfa526601f3ba032cd92bfa700e07ac127f6dc34c6",
  "e70d2a1c01a7ea914d65a8f96e31941e4f30e223efb835c923602878a4d915d1",
  "df4a692046ce50b592f28e932c68ae068adf620960d8c879f901546ec9296bda",
  "dc1f4871487838010b10e8d9122a7157ffaecdde7a7e3be4ce4f4125cb9bf7eb",
  "30424259769fa1d01983f8681cf4479f739468249503546c59b6d6dc1b3ea6f5",
  "7c0354babb2c21a9ae8dcc675c2995721f0de3b36876f7b4d40bdf2cd9f7df15",
  "96e6073a6ae1eb98d6fe6d07e2f83058a37d98f2dad339a706c685b02cd1aa1d",
  "e97f3423eaab1869331122e1b9c554a84efb46c053170e4ea20e793c13e69329",
  "8aae08ead4130b4259e31c70d0019c404364a055dea9b0711919e6ab6da31746",
  "2c790078c694cfdb82e2f5d04c27e4cfd599ac220cd8d4a75e4ea2180f53354f",
  "713411e7526df524d63aaf3da46c9c46f2e037ee53f7a0e17f003e9e1881b34f",
  "590ad46265bff1fdfa1fb17feb160c234f6101ec27118062f5c7b2e6b0ef8060",
  "761645501fb8451bb0320176517d4ec9019e4646cfaa278171a75999d55ef588",
  "1a1da8c9492f21f8f9353198bd8cce9bd281fc51d89f13a769ace5a6af43c58b",
  "914145a9687d5d7e358d0919ce5d66afaca87c80dff63df3166ff84b3155ac94",
  "c9abbdc64ff48496f64b2528d3ce105ec69d73479f41346bfdee88e679c5e7d6",
  "c701dcd1fce2283c5a2edd3d405ea6bc3bc1c12536bce0f5524d84138652a3f4",
  "0ac547e5567d25da5493f0d1a562dfef8c221f7842c2849507836f97ac0d9a0a",
  "05feff9afecf64ca2e9a6968f9c160456618fb65491f813c2d98f27673ffa61b",
  "f32ca1337729d11fbff45490cf410011ace77454d9b9ae8228bab2b2874da207",
  "07463be5e8d9b53cd8669191b57359d14a2e41880bafdab7967e52296581e534",
  "79c895ac5f8c9d6e11b872b362dcfb939a7c0baeb1532e1f6c4152a91379cb70",
  "7e73d249164af428e8fac011f6ac6e0c181f4f8717f275b2543f07e429169153",
  "da690750885b735231e52b9110cf46421cddfff449e62ccf86b66144bb11329b",
  "94175e9e5e7f841ccc87658eecedc212ed18a872aaa9c5d1486616e990d5be39",
  "91770f35dad9be25f5d3d1ab9f54e4a966e258a3cb70d8f81e2bef6f99a5b43f",
  "ba64837aa5e7faa5f71c1888591cc84da48ecd5263a0f780538849a17849f067",
  "ba404123af39af826a9885a3ec53494f8173d562ef1e021ff841aa70d1aeb8a5",
  "51dc6a9c4183fdc764e5fb91b62d92b304569dfd9858693ff8e8f630a6ce46ee",
  "f1663295633d54589ce1af47ea5bc4a986d7ac101461adc126f47c03ed9c6f01",
  "dc523305c04227b6f0a4fb1d0e90b7d69b35388b50195d472b6fffc4ce8719d8",
  "389c144c1bb528aa58d659a9ff4d1bd29fecba7bf7a8b0dfc69ce425b85205d4",
  "d8945e5f46984abf0095bdc580f30c8b3929c109c246f3b2c97918ff5a687016",
  "7a42ebb266df836bbd75e2f87d650dcbd075c8d73435dc1b69ee56c634f7822a",
  "c94667e61ba7cdf2fd565643419db44081a6881235fa19bcdc126313a1a5ab54",
  "6035e2f603ac28e8881760cb511f0206b5f3233047237d9eecbfd9d2f9862f53",
  "15a73dbde1979730f3e0c0f694e0b16489e430183eadb52b120d2c3be7c06f3c",
  "047da1bdb51c0c4b723c2293386d6f81c4e61051cb088244759f864ded1f4486",
  "74185cbb8504fb55467e6ca776f8f30d171fd16e6c6c3399a33f00f1a479ecbe",
  "5bbff7293c29fa19440996268982ff36e9b0dd9a8a1ce23239a7f724ad7da4e3",
  "bf52fe2752375f305cb790e5e13c531393ee4babebf0f23dabcde7bfbe00c08f",
  "4da4f8b71495966604da421db71b1a64356ed95776d8e95a93eaadffd70765b9",
  "047b20361710d345f4182842816379084c8e34f6f86f29eb57cacfb46fe7c629",
  "772a6e88e906a42be7eb66ede81cfb8dd7b25973ac2ff4a32c0186e14674457d",
  "c3c6916a32b71e16ec6525f6b4be30e589a5ecd86afc3b04e7b934132aba9dc7",
  "4e523fe5b08642821b3d12a4442067301b2f9ff1b824acc4f5faf3cb393d02ee",
  "1cc2d177d8418787ca7812ea8efad8fcbb680b3c0d4559ae12743143a3952f36",
  "ec78b05ab4688241f5ff2a73ae38f8685c2e92514bba44340b2fe0e5a7ebd79a",
  "f7a475cd178de12059dd05a0d3e72d6de56f50077170a1c3e9f582be20afd0ec",
  "12410b72b41cd861bfe082adbe412e71976d8759a53ef56dfdc8e17ad1d4cba6",
  "375aff99de485bcf20c141d7a8003537f99fea44696dc1b8ab66f6b75f347541",
  "b68d373cc4a185d1b02dba04baf521bfa263f33e976740ec9bf9970d9a2ba149",
  "fbeb800bac8e2a5c872cb4b6200a1765092122b9bb421042354a63a624044b29",
  "4d38a3641763c6922963234f64e49944d98557f79f5fdf2bf69f018a03ea6a74",
  "2d971cac99c36cb854202831b1d447e1fe88fb69a56f9d9ae2eba844e8db300f",
  "a0fc3f202408485506b16540295f9911f771dd3433663cc6f2c45685b60d2e51",
  "f8e9a251c4bfca48173948980b1297a8b758e648e4868eadc61e4b48cec3899a",
  "84e06cc868166a33bea4220f9563d37aed775cc12a92e6d6f92431e0db409ec7",
  "773f163b24b69a5f39e782e39e6cc4b798c1f7e2ea04660dbce60546f6f808a8",
  "65365ac222ec331f67a7bfc250c44385589bb93985373b25c4b2545e53b5bf7f",
  "d1cb356b2af7cef848e10684c1badba8864cea2ebcab54ea3480a90f715696fc",
  "0af0718b231c74a2400acc594bfa7ef7f4c66fbd0e903a2ca8952189054fb4fe",
  "1be3519cd7ea24607d5d07b82f7d31e3231db36ed564f0b31a77e4f5bce50b2f",
  "dc98d353718a0e63636b848ad1e4d5927f18fe016abfac86648e70d6d81a22fb",
  "b4c934639d61c8b67c1faf6acb7c3503c905909f937dd4da49b987d74d129b57",
  "46f45a88d87e1b8c9f0b6b29864daa8d744fa7a79ceb3dc00666b7b9b0f27e36",
  "41e8d5979944dbc067544cbd20283065e036c4df3d3c0a57bd2d818efb61e998",
  "54ba7d31b147851f48ca3b54bc7018e3cea1847edc2b6978d1bdadf898784dab",
  "e337091c3c47fd798291d1df1378f5221fa1dd156f180e79caa9dd9e361f4577",
  "4e3b517685152062698c1c6c2e7daba41d71b4c6a5ecb3a54ec7ef00dfc6f058",
  "3bc13c5733e6bf72e1c988589150d7aeb03fbb6b1459c60ab6715d22d94ae7f1",
  "8c523611dc059ec15167b1dd7a228bc5d008bf9b6efffd2b7e843c37a9feae04",
  "ddb256d8e2391fb54767918e45aeee719bbf3c6623fb42edc11403c77e9d7d7a",
  "84ac6a6f0f16ed34c878f79c2ec1b7c00892393b86022277ad924613071619b6",
  "b2937fa0d38e8edc72a44092860c66d510d527cf45bb9baea2db8f638aae9cdf",
  "db498454c811db810a2ddfe116b5e53d50534a48a7c43c688c97a56acf48241b",
  "e16bde89672294b6a6fb89ba09c8a29b7636a2ad4cf484ab4a45cdc826a79e72",
  "747a655c433a153ca7afcd722692672aa564f2d58786abc5354cd317fb14f007",
  "abf47265b4ffbc693cf79dd63db87e8a9e73571e3f116cfad7f15b3696ac34ea",
  "5528f11093b95b96f4657e549ccc28972864e997ec7e2e6f0d2ed22faefcb9b5",
  "935d040a9d8109de477f970f276da90592f9485ad9070e64cb4d4b250ca63816",
  "0ddf46f394c5936c10368ccd92a0fb0dfa2bb5a720b97f4e4bf87923b190be03",
  "af64df5cade7c405357df436085eca2b4d8a716618c8985e12995c8be01e4a72",
  "992afec06dcb8c0587d5e4ffe84080c2882a91f264c521e6f43f1e37ce9459a4",
  "1f49729c33cf455a63d817073257b69eac5c24761992c2df1a350ee9cfc55cb3",
  "e4f5659d92d9b43bfe92d6d140edf345a4ae5b8e6e950c70d6d9c2962e21e902",
  "ff20645da772124104f5e893523e7780d903f3a016d9fe2fd3d30ad3096f7997",
  "6f89fdee356c702166b1db4764f6be0d8158dd787e47590c286b700da559dfc5",
  "fec32377bf14011b6e4b0db29133cc558caec3f0a2762fcf73a82d899b03701e",
  "658db14181231665c847b84eee98319900603d0fc9306b60784dda0448a7010b",
  "d1e0255c9771cf5144fa570e670de51efd63a0f8b279d78a795a9ccb52152539",
  "02fe1b532116b82998cd2c32420e913de2df0a4e7b151e27ce02ce25dd73591b",
  "b98c4ced94f6b6b8ebfc0a9e6f81cce1bdb46671622e8bd0ec3817b553afa5d0",
  "9af44ac9d693a749c4868b6d95d6da356a83d3d1824cc746e9ef8d224c5f4bde",
  "c67234441cc2e92f83a57320e8ecad5ae06ee6b3a39b2fb16081861a5c65d065",
  "e76c0e644f8d16fc412595cf14305c262e0610d3cce9ec2cbdf0277f31ef3491",
  "ea974954fd149ee50611f9796e74ea3813ee0ed34e63de94c3bdb786e41053d4",
  "c0c784b1703fad821c8a10a0ebb2512d8ac941d97eca8f26d847284b8c0c5ee7",
  "2c1aeac8c5755dc94e1a307aec6a9819a64f2218e751600c925ebbc6f44bb6f6",
  "6583bd01edbea5e5d5badef63205a19c313de41e9b371b2da4ed951bb6785a2a",
  "a9b0f242a1a2ad1e5908fff1525c29982826a6c3dd944b5b0f7951a9b9f32977",
  "7e52684a8f0cca6755d7fab93eef848967296cdb622de543111ad9857da1e358",
  "cff5701b0571020b2b3e809e1d8d5fb380f10478728e8c12de4559d88c5c0612",
  "99851a666d1ff6c2009bbbc6b249c70498f0b08bc9e5c8534b5ceaba47e72144",
  "791dd5ab80adef9171d72f5cd6736d96221e87fd627895afd892fefc748255b8",
  "056683cf82964b780ea4de5a0681ea77278bc770875363b64f06fb5cda2d3eb8",
  "d7123395c1f5d1614d8ac8089a2d5045e77d273a6f61282e0f570061b834ed6f",
  "8d2e5a977d895267a612bd3a2bce43cfc6bad3fbb85f508f18a761ec1ab14f6e",
  "04677d169be115c0193fe0eaba3f11cb9471631c6d863255e444055427fa540a",
  "0e6ffa419a178b8da5e8f668e1bccddf2e50ac97c9dce466c4cb8a0f6ce4601e",
  "be47497840580e7559fb543a3a5bddb53f11817fd137f71541b0c1d0cd5789e0",
  "85a9bcfc730a3dbfd092cf6ded00e544aeea707e077dc7d1ddc8aa706fc17984",
  "8a634684c633211a391894773c880af457bc517ce6db2aba4dce6b3be9912846",
  "cf1d41ec1d33f0f754694d2c2d96ddbdd7bb397fb6d9b239c11e7e7a26dac760",
  "8cfd584e6415448750465516737526d017867118fd0a1b412170bbb64fb45ee2"
]
```

```plaintext
{
  "reply": [
    "1966bd3242231015eb62f8f9095469580a9cfff494441fcb6263ed9788d30dd1",
    "fd68069e742112113cdbef9607f9f95708989148746d00c4813404fc7052fe9e",
    "6b0e75084d1671579151042413118d12dcd89dae5259b2fa51a3c7d72d1c07cc",
    "feaf3f0c1116923f797c870b10965192e08e2354ecb410fc2c5345aafbf925b9",
    "a5555a23ad42589f66b6fb07deb262e7538624be90a1665ac57bc0984ca919d6",
    "aee381ac13327ffd6930e077ca09f8608c8511bdb7ce17deec50397ba1d9231c",
    "2cc37bb6073a6b6e7f3d57873368c45ce587da63c833f2b756fbc9004d9146d8",
    "fb1d1b85413d31f0e5b472b2d2536b258be79b82d7b47f40f885b8cbe20f7019",
    "450770aed3887a7f956ae43d5b8233359315c236100020010e8c388eb5cc6c0f",
    "f417c80b60c636771575da2ffe6caff423a08030c6e4737a98fb01aa6ba83901",
    "7ae0253b5fed011c1b0af15f5e4c3d2548f2bb86de917d76eb343ef87d6f14c3",
    "d3b8e35f692bb2cd8d2dd8e2d3994346f57f68b3d8bf2b553a0eb073b66c3a24",
    "c34181520a3d6d8a4bb7777d6fcba02b223de869cd3d538b99d61b40bdd28a57",
    "35506d57b70a55dc86a58884af217136d14b53bcef7a66d0d02fd586b85832dd",
    "ff2c473041b9e8022a949a46210ed42cfa1a3c696e4f6edc696b5e80731c5a33",
    "58c2fe03b1e81466dfee724d551f744715e1f6da981b5e4283d4e046c570f812",
    "7900cf55c420bc074ff25beebd3d1acd58a6bb7c6ba379f748ed4916a7a56517",
    "c05371f089d002302f757937779e3a91784704d10f40b186e23147d811b3b349",
    "7a4abc1b812083954521065bdd813158ca3cc8ddad513be52a82197115c03520",
    "00b725a3c0cbf59df22f450bcc0be91539cd58d38c6c343f053f7661b906939a",
    "0b7c8b590b6eeeda79ae6a524c9557b79449d413c5f98e8131e13817fe0fb7a5",
    "b11cccc82dd643ced2ff2e3f6fe0e699cc572ffff7ca1a3812f9e68a2c7d14c6",
    "6f89977bf6aa2598015ded10a57dbbb6c2a1a92d611144d41814eb6c4b661b57",
    "406bfcca5ef96007fceca0300f4140f294d26777ea8cc547a955a062cfdb7ddb",
    "c4b47710b30f88d852ef43a41491d9b04e7717ab7416e4481417b30a69c65104",
    "114f378f6a38f0d5b1b9f46349b14bfc7b605b7b588a348882e05a4f44b64224",
    "f4b8c4faba2a9d3e096791d98de26ba8c84174506dc8d6cf895ec7177da1b52b",
    "861821aa307e8aee76009f4c588f9a294d15c15ed064a80149f374c551b73935",
    "fd8052e1fc8cdf95193c54bebf3ce460552a839cca56015381f320bdbb268d6d",
    "3c448e30fc1682bb3ff6936d4d8256b8dc428d8308791bc5ea9f8fd744cd5477",
    "05e0db50b0c5b922719967bfe44700ebd2414c99ed5305dc2d61b98f21091f88",
    "bcce7c1c1a4fbea67f6d31e91e10c90b5190f09a80a8639c379a18469fd9c2c3",
    "ee804bd62b06f1825b30e09cfe24c2c36f50c426f31125e61e560b8ce27978c5",
    "f641b95e99eb392e682272bfa526601f3ba032cd92bfa700e07ac127f6dc34c6",
    "e70d2a1c01a7ea914d65a8f96e31941e4f30e223efb835c923602878a4d915d1",
    "df4a692046ce50b592f28e932c68ae068adf620960d8c879f901546ec9296bda",
    "dc1f4871487838010b10e8d9122a7157ffaecdde7a7e3be4ce4f4125cb9bf7eb",
    "30424259769fa1d01983f8681cf4479f739468249503546c59b6d6dc1b3ea6f5",
    "7c0354babb2c21a9ae8dcc675c2995721f0de3b36876f7b4d40bdf2cd9f7df15",
    "96e6073a6ae1eb98d6fe6d07e2f83058a37d98f2dad339a706c685b02cd1aa1d",
    "e97f3423eaab1869331122e1b9c554a84efb46c053170e4ea20e793c13e69329",
    "8aae08ead4130b4259e31c70d0019c404364a055dea9b0711919e6ab6da31746",
    "2c790078c694cfdb82e2f5d04c27e4cfd599ac220cd8d4a75e4ea2180f53354f",
    "713411e7526df524d63aaf3da46c9c46f2e037ee53f7a0e17f003e9e1881b34f",
    "590ad46265bff1fdfa1fb17feb160c234f6101ec27118062f5c7b2e6b0ef8060",
    "761645501fb8451bb0320176517d4ec9019e4646cfaa278171a75999d55ef588",
    "1a1da8c9492f21f8f9353198bd8cce9bd281fc51d89f13a769ace5a6af43c58b",
    "914145a9687d5d7e358d0919ce5d66afaca87c80dff63df3166ff84b3155ac94",
    "c9abbdc64ff48496f64b2528d3ce105ec69d73479f41346bfdee88e679c5e7d6",
    "c701dcd1fce2283c5a2edd3d405ea6bc3bc1c12536bce0f5524d84138652a3f4",
    "0ac547e5567d25da5493f0d1a562dfef8c221f7842c2849507836f97ac0d9a0a",
    "05feff9afecf64ca2e9a6968f9c160456618fb65491f813c2d98f27673ffa61b",
    "f32ca1337729d11fbff45490cf410011ace77454d9b9ae8228bab2b2874da207",
    "07463be5e8d9b53cd8669191b57359d14a2e41880bafdab7967e52296581e534",
    "79c895ac5f8c9d6e11b872b362dcfb939a7c0baeb1532e1f6c4152a91379cb70",
    "7e73d249164af428e8fac011f6ac6e0c181f4f8717f275b2543f07e429169153",
    "da690750885b735231e52b9110cf46421cddfff449e62ccf86b66144bb11329b",
    "94175e9e5e7f841ccc87658eecedc212ed18a872aaa9c5d1486616e990d5be39",
    "91770f35dad9be25f5d3d1ab9f54e4a966e258a3cb70d8f81e2bef6f99a5b43f",
    "ba64837aa5e7faa5f71c1888591cc84da48ecd5263a0f780538849a17849f067",
    "ba404123af39af826a9885a3ec53494f8173d562ef1e021ff841aa70d1aeb8a5",
    "51dc6a9c4183fdc764e5fb91b62d92b304569dfd9858693ff8e8f630a6ce46ee",
    "f1663295633d54589ce1af47ea5bc4a986d7ac101461adc126f47c03ed9c6f01",
    "dc523305c04227b6f0a4fb1d0e90b7d69b35388b50195d472b6fffc4ce8719d8",
    "389c144c1bb528aa58d659a9ff4d1bd29fecba7bf7a8b0dfc69ce425b85205d4",
    "d8945e5f46984abf0095bdc580f30c8b3929c109c246f3b2c97918ff5a687016",
    "7a42ebb266df836bbd75e2f87d650dcbd075c8d73435dc1b69ee56c634f7822a",
    "c94667e61ba7cdf2fd565643419db44081a6881235fa19bcdc126313a1a5ab54",
    "6035e2f603ac28e8881760cb511f0206b5f3233047237d9eecbfd9d2f9862f53",
    "15a73dbde1979730f3e0c0f694e0b16489e430183eadb52b120d2c3be7c06f3c",
    "047da1bdb51c0c4b723c2293386d6f81c4e61051cb088244759f864ded1f4486",
    "74185cbb8504fb55467e6ca776f8f30d171fd16e6c6c3399a33f00f1a479ecbe",
    "5bbff7293c29fa19440996268982ff36e9b0dd9a8a1ce23239a7f724ad7da4e3",
    "bf52fe2752375f305cb790e5e13c531393ee4babebf0f23dabcde7bfbe00c08f",
    "4da4f8b71495966604da421db71b1a64356ed95776d8e95a93eaadffd70765b9",
    "047b20361710d345f4182842816379084c8e34f6f86f29eb57cacfb46fe7c629",
    "772a6e88e906a42be7eb66ede81cfb8dd7b25973ac2ff4a32c0186e14674457d",
    "c3c6916a32b71e16ec6525f6b4be30e589a5ecd86afc3b04e7b934132aba9dc7",
    "4e523fe5b08642821b3d12a4442067301b2f9ff1b824acc4f5faf3cb393d02ee",
    "1cc2d177d8418787ca7812ea8efad8fcbb680b3c0d4559ae12743143a3952f36",
    "ec78b05ab4688241f5ff2a73ae38f8685c2e92514bba44340b2fe0e5a7ebd79a",
    "f7a475cd178de12059dd05a0d3e72d6de56f50077170a1c3e9f582be20afd0ec",
    "12410b72b41cd861bfe082adbe412e71976d8759a53ef56dfdc8e17ad1d4cba6",
    "375aff99de485bcf20c141d7a8003537f99fea44696dc1b8ab66f6b75f347541",
    "b68d373cc4a185d1b02dba04baf521bfa263f33e976740ec9bf9970d9a2ba149",
    "fbeb800bac8e2a5c872cb4b6200a1765092122b9bb421042354a63a624044b29",
    "4d38a3641763c6922963234f64e49944d98557f79f5fdf2bf69f018a03ea6a74",
    "2d971cac99c36cb854202831b1d447e1fe88fb69a56f9d9ae2eba844e8db300f",
    "a0fc3f202408485506b16540295f9911f771dd3433663cc6f2c45685b60d2e51",
    "f8e9a251c4bfca48173948980b1297a8b758e648e4868eadc61e4b48cec3899a",
    "84e06cc868166a33bea4220f9563d37aed775cc12a92e6d6f92431e0db409ec7",
    "773f163b24b69a5f39e782e39e6cc4b798c1f7e2ea04660dbce60546f6f808a8",
    "65365ac222ec331f67a7bfc250c44385589bb93985373b25c4b2545e53b5bf7f",
    "d1cb356b2af7cef848e10684c1badba8864cea2ebcab54ea3480a90f715696fc",
    "0af0718b231c74a2400acc594bfa7ef7f4c66fbd0e903a2ca8952189054fb4fe",
    "1be3519cd7ea24607d5d07b82f7d31e3231db36ed564f0b31a77e4f5bce50b2f",
    "dc98d353718a0e63636b848ad1e4d5927f18fe016abfac86648e70d6d81a22fb",
    "b4c934639d61c8b67c1faf6acb7c3503c905909f937dd4da49b987d74d129b57",
    "46f45a88d87e1b8c9f0b6b29864daa8d744fa7a79ceb3dc00666b7b9b0f27e36",
    "41e8d5979944dbc067544cbd20283065e036c4df3d3c0a57bd2d818efb61e998",
    "54ba7d31b147851f48ca3b54bc7018e3cea1847edc2b6978d1bdadf898784dab",
    "e337091c3c47fd798291d1df1378f5221fa1dd156f180e79caa9dd9e361f4577",
    "4e3b517685152062698c1c6c2e7daba41d71b4c6a5ecb3a54ec7ef00dfc6f058",
    "3bc13c5733e6bf72e1c988589150d7aeb03fbb6b1459c60ab6715d22d94ae7f1",
    "8c523611dc059ec15167b1dd7a228bc5d008bf9b6efffd2b7e843c37a9feae04",
    "ddb256d8e2391fb54767918e45aeee719bbf3c6623fb42edc11403c77e9d7d7a",
    "84ac6a6f0f16ed34c878f79c2ec1b7c00892393b86022277ad924613071619b6",
    "b2937fa0d38e8edc72a44092860c66d510d527cf45bb9baea2db8f638aae9cdf",
    "db498454c811db810a2ddfe116b5e53d50534a48a7c43c688c97a56acf48241b",
    "e16bde89672294b6a6fb89ba09c8a29b7636a2ad4cf484ab4a45cdc826a79e72",
    "747a655c433a153ca7afcd722692672aa564f2d58786abc5354cd317fb14f007",
    "abf47265b4ffbc693cf79dd63db87e8a9e73571e3f116cfad7f15b3696ac34ea",
    "5528f11093b95b96f4657e549ccc28972864e997ec7e2e6f0d2ed22faefcb9b5",
    "935d040a9d8109de477f970f276da90592f9485ad9070e64cb4d4b250ca63816",
    "0ddf46f394c5936c10368ccd92a0fb0dfa2bb5a720b97f4e4bf87923b190be03",
    "af64df5cade7c405357df436085eca2b4d8a716618c8985e12995c8be01e4a72",
    "992afec06dcb8c0587d5e4ffe84080c2882a91f264c521e6f43f1e37ce9459a4",
    "1f49729c33cf455a63d817073257b69eac5c24761992c2df1a350ee9cfc55cb3",
    "e4f5659d92d9b43bfe92d6d140edf345a4ae5b8e6e950c70d6d9c2962e21e902",
    "ff20645da772124104f5e893523e7780d903f3a016d9fe2fd3d30ad3096f7997",
    "6f89fdee356c702166b1db4764f6be0d8158dd787e47590c286b700da559dfc5",
    "fec32377bf14011b6e4b0db29133cc558caec3f0a2762fcf73a82d899b03701e",
    "658db14181231665c847b84eee98319900603d0fc9306b60784dda0448a7010b",
    "d1e0255c9771cf5144fa570e670de51efd63a0f8b279d78a795a9ccb52152539",
    "02fe1b532116b82998cd2c32420e913de2df0a4e7b151e27ce02ce25dd73591b",
    "b98c4ced94f6b6b8ebfc0a9e6f81cce1bdb46671622e8bd0ec3817b553afa5d0",
    "9af44ac9d693a749c4868b6d95d6da356a83d3d1824cc746e9ef8d224c5f4bde",
    "c67234441cc2e92f83a57320e8ecad5ae06ee6b3a39b2fb16081861a5c65d065",
    "e76c0e644f8d16fc412595cf14305c262e0610d3cce9ec2cbdf0277f31ef3491",
    "ea974954fd149ee50611f9796e74ea3813ee0ed34e63de94c3bdb786e41053d4",
    "c0c784b1703fad821c8a10a0ebb2512d8ac941d97eca8f26d847284b8c0c5ee7",
    "2c1aeac8c5755dc94e1a307aec6a9819a64f2218e751600c925ebbc6f44bb6f6",
    "6583bd01edbea5e5d5badef63205a19c313de41e9b371b2da4ed951bb6785a2a",
    "a9b0f242a1a2ad1e5908fff1525c29982826a6c3dd944b5b0f7951a9b9f32977",
    "7e52684a8f0cca6755d7fab93eef848967296cdb622de543111ad9857da1e358",
    "cff5701b0571020b2b3e809e1d8d5fb380f10478728e8c12de4559d88c5c0612",
    "99851a666d1ff6c2009bbbc6b249c70498f0b08bc9e5c8534b5ceaba47e72144",
    "791dd5ab80adef9171d72f5cd6736d96221e87fd627895afd892fefc748255b8",
    "056683cf82964b780ea4de5a0681ea77278bc770875363b64f06fb5cda2d3eb8",
    "d7123395c1f5d1614d8ac8089a2d5045e77d273a6f61282e0f570061b834ed6f",
    "8d2e5a977d895267a612bd3a2bce43cfc6bad3fbb85f508f18a761ec1ab14f6e",
    "04677d169be115c0193fe0eaba3f11cb9471631c6d863255e444055427fa540a",
    "0e6ffa419a178b8da5e8f668e1bccddf2e50ac97c9dce466c4cb8a0f6ce4601e",
    "be47497840580e7559fb543a3a5bddb53f11817fd137f71541b0c1d0cd5789e0",
    "85a9bcfc730a3dbfd092cf6ded00e544aeea707e077dc7d1ddc8aa706fc17984",
    "8a634684c633211a391894773c880af457bc517ce6db2aba4dce6b3be9912846",
    "cf1d41ec1d33f0f754694d2c2d96ddbdd7bb397fb6d9b239c11e7e7a26dac760",
    "8cfd584e6415448750465516737526d017867118fd0a1b412170bbb64fb45ee2"
  ],
  "error": null,
  "id": 1,
  "uuid": "9CD0F9FE-2857-49E5-B487-79F81FC9303D"
}
```

Parameter            | Type          | Description
---------------------|---------------|-------------
[]                   | Array         | A list of transactions.
- hash               | string        | The hash of the transaction.
error                | string        | API error code.
id                   | int           | ID number.
uuid                 | string        | The response ID, which can be used to view this response again with [xrGetReply](https://api.blocknet.co/#xrgetreply).





## omni_listblockstransactions

> Sample Data

```cli
{
  "firstblock": 610096,
  "lastblock": 610097
}
```
Lists all Omni transactions in a given range of blocks.


### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '[610096,610097]' https://api.oracleminer.com/xrs/omni_listblockstransactions
```

```plaintext
blocknet-cli xrService omni_listblockstransactions 610096 610097
```
<code class="api-call">omni_listblockstransactions [firstblock] [lastblock]</code>

Parameter       | Type       | Description
----------------|------------|-------------
firstblock      | int        | The index of the first block to consider.
lastblock       | int        | The index of the last block to consider.

### Response Parameters

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
[
  "f417c80b60c636771575da2ffe6caff423a08030c6e4737a98fb01aa6ba83901",
  "f1663295633d54589ce1af47ea5bc4a986d7ac101461adc126f47c03ed9c6f01",
  "e4f5659d92d9b43bfe92d6d140edf345a4ae5b8e6e950c70d6d9c2962e21e902",
  "0ddf46f394c5936c10368ccd92a0fb0dfa2bb5a720b97f4e4bf87923b190be03",
  "c4b47710b30f88d852ef43a41491d9b04e7717ab7416e4481417b30a69c65104",
  "8c523611dc059ec15167b1dd7a228bc5d008bf9b6efffd2b7e843c37a9feae04",
  "f32ca1337729d11fbff45490cf410011ace77454d9b9ae8228bab2b2874da207",
  "747a655c433a153ca7afcd722692672aa564f2d58786abc5354cd317fb14f007",
  "04677d169be115c0193fe0eaba3f11cb9471631c6d863255e444055427fa540a",
  "0ac547e5567d25da5493f0d1a562dfef8c221f7842c2849507836f97ac0d9a0a",
  "658db14181231665c847b84eee98319900603d0fc9306b60784dda0448a7010b",
  "2d971cac99c36cb854202831b1d447e1fe88fb69a56f9d9ae2eba844e8db300f",
  "450770aed3887a7f956ae43d5b8233359315c236100020010e8c388eb5cc6c0f",
  "cff5701b0571020b2b3e809e1d8d5fb380f10478728e8c12de4559d88c5c0612",
  "58c2fe03b1e81466dfee724d551f744715e1f6da981b5e4283d4e046c570f812",
  "3453f6ec7829df031bee50293236a952d22ee202f0d7372b261af36fdc918214",
  "7c0354babb2c21a9ae8dcc675c2995721f0de3b36876f7b4d40bdf2cd9f7df15",
  "935d040a9d8109de477f970f276da90592f9485ad9070e64cb4d4b250ca63816",
  "d8945e5f46984abf0095bdc580f30c8b3929c109c246f3b2c97918ff5a687016",
  "7900cf55c420bc074ff25beebd3d1acd58a6bb7c6ba379f748ed4916a7a56517",
  "82b7b86c086102a1f42c0dd55c0a3bec40d715eb38b1d4075c265870be120c19",
  "fb1d1b85413d31f0e5b472b2d2536b258be79b82d7b47f40f885b8cbe20f7019",
  "db498454c811db810a2ddfe116b5e53d50534a48a7c43c688c97a56acf48241b",
  "02fe1b532116b82998cd2c32420e913de2df0a4e7b151e27ce02ce25dd73591b",
  "05feff9afecf64ca2e9a6968f9c160456618fb65491f813c2d98f27673ffa61b",
  "aee381ac13327ffd6930e077ca09f8608c8511bdb7ce17deec50397ba1d9231c",
  "96e6073a6ae1eb98d6fe6d07e2f83058a37d98f2dad339a706c685b02cd1aa1d",
  "0e6ffa419a178b8da5e8f668e1bccddf2e50ac97c9dce466c4cb8a0f6ce4601e",
  "fec32377bf14011b6e4b0db29133cc558caec3f0a2762fcf73a82d899b03701e",
  "7a4abc1b812083954521065bdd813158ca3cc8ddad513be52a82197115c03520",
  "d3b8e35f692bb2cd8d2dd8e2d3994346f57f68b3d8bf2b553a0eb073b66c3a24",
  "114f378f6a38f0d5b1b9f46349b14bfc7b605b7b588a348882e05a4f44b64224",
  "77027bbf65a49cbfe4978a0e4611942ff29121dcda6c305ca68acb71c1461a27",
  "d1438713318f3973fcf33320e2b6372f091587b2d1f0847c3c6a42101a59fb27",
  "fbeb800bac8e2a5c872cb4b6200a1765092122b9bb421042354a63a624044b29",
  "e97f3423eaab1869331122e1b9c554a84efb46c053170e4ea20e793c13e69329",
  "047b20361710d345f4182842816379084c8e34f6f86f29eb57cacfb46fe7c629",
  "6583bd01edbea5e5d5badef63205a19c313de41e9b371b2da4ed951bb6785a2a",
  "7a42ebb266df836bbd75e2f87d650dcbd075c8d73435dc1b69ee56c634f7822a",
  "f4b8c4faba2a9d3e096791d98de26ba8c84174506dc8d6cf895ec7177da1b52b",
  "eac4efd228f63982d7b4bfc2a593f28882f24f59e9956fae22d1090778e1452c",
  "1be3519cd7ea24607d5d07b82f7d31e3231db36ed564f0b31a77e4f5bce50b2f",
  "ff2c473041b9e8022a949a46210ed42cfa1a3c696e4f6edc696b5e80731c5a33",
  "07463be5e8d9b53cd8669191b57359d14a2e41880bafdab7967e52296581e534",
  "861821aa307e8aee76009f4c588f9a294d15c15ed064a80149f374c551b73935",
  "8a937bf8fc495e0c0bdf9364dfae7510e2a2785848ec976d61ae0c3b36356b35",
  "1cc2d177d8418787ca7812ea8efad8fcbb680b3c0d4559ae12743143a3952f36",
  "46f45a88d87e1b8c9f0b6b29864daa8d744fa7a79ceb3dc00666b7b9b0f27e36",
  "d1e0255c9771cf5144fa570e670de51efd63a0f8b279d78a795a9ccb52152539",
  "94175e9e5e7f841ccc87658eecedc212ed18a872aaa9c5d1486616e990d5be39",
  "15a73dbde1979730f3e0c0f694e0b16489e430183eadb52b120d2c3be7c06f3c",
  "6dab3bb72fce0f7af56dd04afd3da248b66f60fa713190a20ea78acec0943c3f",
  "91770f35dad9be25f5d3d1ab9f54e4a966e258a3cb70d8f81e2bef6f99a5b43f",
  "375aff99de485bcf20c141d7a8003537f99fea44696dc1b8ab66f6b75f347541",
  "99851a666d1ff6c2009bbbc6b249c70498f0b08bc9e5c8534b5ceaba47e72144",
  "8aae08ead4130b4259e31c70d0019c404364a055dea9b0711919e6ab6da31746",
  "8a634684c633211a391894773c880af457bc517ce6db2aba4dce6b3be9912846",
  "b68d373cc4a185d1b02dba04baf521bfa263f33e976740ec9bf9970d9a2ba149",
  "c05371f089d002302f757937779e3a91784704d10f40b186e23147d811b3b349",
  "2c790078c694cfdb82e2f5d04c27e4cfd599ac220cd8d4a75e4ea2180f53354f",
  "713411e7526df524d63aaf3da46c9c46f2e037ee53f7a0e17f003e9e1881b34f",
  "85f2b8e7adb7b0fe6b92a0128572bca061a7efe7686301eec378d853b5a40f50",
  "a0fc3f202408485506b16540295f9911f771dd3433663cc6f2c45685b60d2e51",
  "6035e2f603ac28e8881760cb511f0206b5f3233047237d9eecbfd9d2f9862f53",
  "7e73d249164af428e8fac011f6ac6e0c181f4f8717f275b2543f07e429169153",
  "c94667e61ba7cdf2fd565643419db44081a6881235fa19bcdc126313a1a5ab54",
  "8dcdcb7e9e2f161e2e77062e5313d4d3b06a5df288638ad198c3efed0501f656",
  "6f89977bf6aa2598015ded10a57dbbb6c2a1a92d611144d41814eb6c4b661b57",
  "c34181520a3d6d8a4bb7777d6fcba02b223de869cd3d538b99d61b40bdd28a57",
  "b4c934639d61c8b67c1faf6acb7c3503c905909f937dd4da49b987d74d129b57",
  "7e52684a8f0cca6755d7fab93eef848967296cdb622de543111ad9857da1e358",
  "4e3b517685152062698c1c6c2e7daba41d71b4c6a5ecb3a54ec7ef00dfc6f058",
  "050f26dcc5611c779fac8556563feef31b90a150d4f7e98b910ce8d009651d5a",
  "8e020686db747d3105e81785970019435ca852fd909fac9a7582efa89a5f605b",
  "9597877615a02656e9c0e9d8c98795435f997f190da261f69f120698733d0360",
  "590ad46265bff1fdfa1fb17feb160c234f6101ec27118062f5c7b2e6b0ef8060",
  "cf1d41ec1d33f0f754694d2c2d96ddbdd7bb397fb6d9b239c11e7e7a26dac760",
  "c67234441cc2e92f83a57320e8ecad5ae06ee6b3a39b2fb16081861a5c65d065",
  "81058bfc6f2fa86d5083a0710f206865201e82021ab5ae04b01e84674e14c967",
  "ba64837aa5e7faa5f71c1888591cc84da48ecd5263a0f780538849a17849f067",
  "be24812c14bbbdbe6fe07666fdb2a9000a222b7a562f1da04e70268ad22f406b",
  "fd8052e1fc8cdf95193c54bebf3ce460552a839cca56015381f320bdbb268d6d",
  "8d2e5a977d895267a612bd3a2bce43cfc6bad3fbb85f508f18a761ec1ab14f6e",
  "d7123395c1f5d1614d8ac8089a2d5045e77d273a6f61282e0f570061b834ed6f",
  "79c895ac5f8c9d6e11b872b362dcfb939a7c0baeb1532e1f6c4152a91379cb70",
  "af64df5cade7c405357df436085eca2b4d8a716618c8985e12995c8be01e4a72",
  "e16bde89672294b6a6fb89ba09c8a29b7636a2ad4cf484ab4a45cdc826a79e72",
  "4d38a3641763c6922963234f64e49944d98557f79f5fdf2bf69f018a03ea6a74",
  "650451e8261b44942f5b4a30d4b3167824d739850ad28c696d826887da325276",
  "a9b0f242a1a2ad1e5908fff1525c29982826a6c3dd944b5b0f7951a9b9f32977",
  "e337091c3c47fd798291d1df1378f5221fa1dd156f180e79caa9dd9e361f4577",
  "3c448e30fc1682bb3ff6936d4d8256b8dc428d8308791bc5ea9f8fd744cd5477",
  "ddb256d8e2391fb54767918e45aeee719bbf3c6623fb42edc11403c77e9d7d7a",
  "772a6e88e906a42be7eb66ede81cfb8dd7b25973ac2ff4a32c0186e14674457d",
  "bef1190f72d5fb91b037f20ea4b1abdeaab367084acdf19df2c496f05bee937e",
  "65365ac222ec331f67a7bfc250c44385589bb93985373b25c4b2545e53b5bf7f",
  "85a9bcfc730a3dbfd092cf6ded00e544aeea707e077dc7d1ddc8aa706fc17984",
  "047da1bdb51c0c4b723c2293386d6f81c4e61051cb088244759f864ded1f4486",
  "95b882fbb221324ec85e0312afda4338ec0322fc56f1fca0489e8ac5f0640988",
  "05e0db50b0c5b922719967bfe44700ebd2414c99ed5305dc2d61b98f21091f88",
  "761645501fb8451bb0320176517d4ec9019e4646cfaa278171a75999d55ef588",
  "fc525774b18198dcf35b7af6e89680f6c9bfbad0833bd73847f70021e703378b",
  "1a1da8c9492f21f8f9353198bd8cce9bd281fc51d89f13a769ace5a6af43c58b",
  "b1520b461f31147563413d85029adb63af658a10ce1f7d57f876bc651fd13b8f",
  "bf52fe2752375f305cb790e5e13c531393ee4babebf0f23dabcde7bfbe00c08f",
  "69b83f02ff6f39745d74c2859cd476f09e03a7ebe35d7c98017a0612d7fa2c91",
  "e76c0e644f8d16fc412595cf14305c262e0610d3cce9ec2cbdf0277f31ef3491",
  "914145a9687d5d7e358d0919ce5d66afaca87c80dff63df3166ff84b3155ac94",
  "ff20645da772124104f5e893523e7780d903f3a016d9fe2fd3d30ad3096f7997",
  "41e8d5979944dbc067544cbd20283065e036c4df3d3c0a57bd2d818efb61e998",
  "f8e9a251c4bfca48173948980b1297a8b758e648e4868eadc61e4b48cec3899a",
  "00b725a3c0cbf59df22f450bcc0be91539cd58d38c6c343f053f7661b906939a",
  "ec78b05ab4688241f5ff2a73ae38f8685c2e92514bba44340b2fe0e5a7ebd79a",
  "da690750885b735231e52b9110cf46421cddfff449e62ccf86b66144bb11329b",
  "fd68069e742112113cdbef9607f9f95708989148746d00c4813404fc7052fe9e",
  "97cf49f5ac437db8073c26be8416288cf75b94f8b97a1caf6616cda992b7239f",
  "85d1e96d6e9a7e3cf373d63f3c520ace3aacf69ab40fb26c59b079ed4b4319a1",
  "992afec06dcb8c0587d5e4ffe84080c2882a91f264c521e6f43f1e37ce9459a4",
  "0b7c8b590b6eeeda79ae6a524c9557b79449d413c5f98e8131e13817fe0fb7a5",
  "ba404123af39af826a9885a3ec53494f8173d562ef1e021ff841aa70d1aeb8a5",
  "12410b72b41cd861bfe082adbe412e71976d8759a53ef56dfdc8e17ad1d4cba6",
  "773f163b24b69a5f39e782e39e6cc4b798c1f7e2ea04660dbce60546f6f808a8",
  "abdeeb0c30eef7296ff97c7abf3ab4377f39edd4c33274fd22265a8df44be9a8",
  "54ba7d31b147851f48ca3b54bc7018e3cea1847edc2b6978d1bdadf898784dab",
  "8d7085272ebb7760c8e7ef668307dc8f4efb83c0c387977165df06b31db360b1",
  "1f49729c33cf455a63d817073257b69eac5c24761992c2df1a350ee9cfc55cb3",
  "5528f11093b95b96f4657e549ccc28972864e997ec7e2e6f0d2ed22faefcb9b5",
  "84ac6a6f0f16ed34c878f79c2ec1b7c00892393b86022277ad924613071619b6",
  "056683cf82964b780ea4de5a0681ea77278bc770875363b64f06fb5cda2d3eb8",
  "791dd5ab80adef9171d72f5cd6736d96221e87fd627895afd892fefc748255b8",
  "feaf3f0c1116923f797c870b10965192e08e2354ecb410fc2c5345aafbf925b9",
  "4da4f8b71495966604da421db71b1a64356ed95776d8e95a93eaadffd70765b9",
  "550ddf96775c871d98ad6363eb1512a35bd506e9f59bcd4bfa7e173bd55601bb",
  "fc0c1d1fdae045e7be88e67280837cfbdd90f0e5171d13409a4794ab0d2f46bc",
  "74185cbb8504fb55467e6ca776f8f30d171fd16e6c6c3399a33f00f1a479ecbe",
  "19b13d699afef1a52e945b711ce07c0c65b9c5a38c970d6e294f6ad89e835bc2",
  "7ae0253b5fed011c1b0af15f5e4c3d2548f2bb86de917d76eb343ef87d6f14c3",
  "45754f8446ae1b96ff5ffa03b06c9a8421e0166387d955736fb9746c1266a4c3",
  "bcce7c1c1a4fbea67f6d31e91e10c90b5190f09a80a8639c379a18469fd9c2c3",
  "ee804bd62b06f1825b30e09cfe24c2c36f50c426f31125e61e560b8ce27978c5",
  "6f89fdee356c702166b1db4764f6be0d8158dd787e47590c286b700da559dfc5",
  "b11cccc82dd643ced2ff2e3f6fe0e699cc572ffff7ca1a3812f9e68a2c7d14c6",
  "f641b95e99eb392e682272bfa526601f3ba032cd92bfa700e07ac127f6dc34c6",
  "c3c6916a32b71e16ec6525f6b4be30e589a5ecd86afc3b04e7b934132aba9dc7",
  "84e06cc868166a33bea4220f9563d37aed775cc12a92e6d6f92431e0db409ec7",
  "6b0e75084d1671579151042413118d12dcd89dae5259b2fa51a3c7d72d1c07cc",
  "b98c4ced94f6b6b8ebfc0a9e6f81cce1bdb46671622e8bd0ec3817b553afa5d0",
  "1966bd3242231015eb62f8f9095469580a9cfff494441fcb6263ed9788d30dd1",
  "e70d2a1c01a7ea914d65a8f96e31941e4f30e223efb835c923602878a4d915d1",
  "389c144c1bb528aa58d659a9ff4d1bd29fecba7bf7a8b0dfc69ce425b85205d4",
  "0758dca870bfa301fbeb12b5017e1438d6c8fc287d44c8921c9aa7a895c40ad4",
  "ea974954fd149ee50611f9796e74ea3813ee0ed34e63de94c3bdb786e41053d4",
  "a5555a23ad42589f66b6fb07deb262e7538624be90a1665ac57bc0984ca919d6",
  "c9abbdc64ff48496f64b2528d3ce105ec69d73479f41346bfdee88e679c5e7d6",
  "dc523305c04227b6f0a4fb1d0e90b7d69b35388b50195d472b6fffc4ce8719d8",
  "2cc37bb6073a6b6e7f3d57873368c45ce587da63c833f2b756fbc9004d9146d8",
  "df4a692046ce50b592f28e932c68ae068adf620960d8c879f901546ec9296bda",
  "406bfcca5ef96007fceca0300f4140f294d26777ea8cc547a955a062cfdb7ddb",
  "35506d57b70a55dc86a58884af217136d14b53bcef7a66d0d02fd586b85832dd",
  "9af44ac9d693a749c4868b6d95d6da356a83d3d1824cc746e9ef8d224c5f4bde",
  "b2937fa0d38e8edc72a44092860c66d510d527cf45bb9baea2db8f638aae9cdf",
  "be47497840580e7559fb543a3a5bddb53f11817fd137f71541b0c1d0cd5789e0",
  "8cfd584e6415448750465516737526d017867118fd0a1b412170bbb64fb45ee2",
  "5bbff7293c29fa19440996268982ff36e9b0dd9a8a1ce23239a7f724ad7da4e3",
  "20a980b2ee5176dc1f273927e3dc05e1d679328663827eeec6b66a06827239e4",
  "c0c784b1703fad821c8a10a0ebb2512d8ac941d97eca8f26d847284b8c0c5ee7",
  "abf47265b4ffbc693cf79dd63db87e8a9e73571e3f116cfad7f15b3696ac34ea",
  "dc1f4871487838010b10e8d9122a7157ffaecdde7a7e3be4ce4f4125cb9bf7eb",
  "f7a475cd178de12059dd05a0d3e72d6de56f50077170a1c3e9f582be20afd0ec",
  "70bfbb2a3d113733af55ab0f0f6d42284f1a9aad99c45a21e1b0fe778b9ba8ed",
  "4e523fe5b08642821b3d12a4442067301b2f9ff1b824acc4f5faf3cb393d02ee",
  "51dc6a9c4183fdc764e5fb91b62d92b304569dfd9858693ff8e8f630a6ce46ee",
  "3bc13c5733e6bf72e1c988589150d7aeb03fbb6b1459c60ab6715d22d94ae7f1",
  "c701dcd1fce2283c5a2edd3d405ea6bc3bc1c12536bce0f5524d84138652a3f4",
  "30424259769fa1d01983f8681cf4479f739468249503546c59b6d6dc1b3ea6f5",
  "d80a28fdce4cc00bb0ede2d1a277ee196a7a37fba8a965dd994a3405f4b288f6",
  "2c1aeac8c5755dc94e1a307aec6a9819a64f2218e751600c925ebbc6f44bb6f6",
  "0dae4dd4760ef7c74139743f43d3acb1af17a24c7bcd37ae6de0f680b10a48f8",
  "5aa30535c7df544fa66a1173bc2522567cb9c973f7b85fa634652b8fdafd29f9",
  "dc98d353718a0e63636b848ad1e4d5927f18fe016abfac86648e70d6d81a22fb",
  "d1cb356b2af7cef848e10684c1badba8864cea2ebcab54ea3480a90f715696fc",
  "0af0718b231c74a2400acc594bfa7ef7f4c66fbd0e903a2ca8952189054fb4fe"
]
```

```plaintext
{
  "reply": [
    "f417c80b60c636771575da2ffe6caff423a08030c6e4737a98fb01aa6ba83901",
    "f1663295633d54589ce1af47ea5bc4a986d7ac101461adc126f47c03ed9c6f01",
    "e4f5659d92d9b43bfe92d6d140edf345a4ae5b8e6e950c70d6d9c2962e21e902",
    "0ddf46f394c5936c10368ccd92a0fb0dfa2bb5a720b97f4e4bf87923b190be03",
    "c4b47710b30f88d852ef43a41491d9b04e7717ab7416e4481417b30a69c65104",
    "8c523611dc059ec15167b1dd7a228bc5d008bf9b6efffd2b7e843c37a9feae04",
    "f32ca1337729d11fbff45490cf410011ace77454d9b9ae8228bab2b2874da207",
    "747a655c433a153ca7afcd722692672aa564f2d58786abc5354cd317fb14f007",
    "04677d169be115c0193fe0eaba3f11cb9471631c6d863255e444055427fa540a",
    "0ac547e5567d25da5493f0d1a562dfef8c221f7842c2849507836f97ac0d9a0a",
    "658db14181231665c847b84eee98319900603d0fc9306b60784dda0448a7010b",
    "2d971cac99c36cb854202831b1d447e1fe88fb69a56f9d9ae2eba844e8db300f",
    "450770aed3887a7f956ae43d5b8233359315c236100020010e8c388eb5cc6c0f",
    "cff5701b0571020b2b3e809e1d8d5fb380f10478728e8c12de4559d88c5c0612",
    "58c2fe03b1e81466dfee724d551f744715e1f6da981b5e4283d4e046c570f812",
    "3453f6ec7829df031bee50293236a952d22ee202f0d7372b261af36fdc918214",
    "7c0354babb2c21a9ae8dcc675c2995721f0de3b36876f7b4d40bdf2cd9f7df15",
    "935d040a9d8109de477f970f276da90592f9485ad9070e64cb4d4b250ca63816",
    "d8945e5f46984abf0095bdc580f30c8b3929c109c246f3b2c97918ff5a687016",
    "7900cf55c420bc074ff25beebd3d1acd58a6bb7c6ba379f748ed4916a7a56517",
    "82b7b86c086102a1f42c0dd55c0a3bec40d715eb38b1d4075c265870be120c19",
    "fb1d1b85413d31f0e5b472b2d2536b258be79b82d7b47f40f885b8cbe20f7019",
    "db498454c811db810a2ddfe116b5e53d50534a48a7c43c688c97a56acf48241b",
    "02fe1b532116b82998cd2c32420e913de2df0a4e7b151e27ce02ce25dd73591b",
    "05feff9afecf64ca2e9a6968f9c160456618fb65491f813c2d98f27673ffa61b",
    "aee381ac13327ffd6930e077ca09f8608c8511bdb7ce17deec50397ba1d9231c",
    "96e6073a6ae1eb98d6fe6d07e2f83058a37d98f2dad339a706c685b02cd1aa1d",
    "0e6ffa419a178b8da5e8f668e1bccddf2e50ac97c9dce466c4cb8a0f6ce4601e",
    "fec32377bf14011b6e4b0db29133cc558caec3f0a2762fcf73a82d899b03701e",
    "7a4abc1b812083954521065bdd813158ca3cc8ddad513be52a82197115c03520",
    "d3b8e35f692bb2cd8d2dd8e2d3994346f57f68b3d8bf2b553a0eb073b66c3a24",
    "114f378f6a38f0d5b1b9f46349b14bfc7b605b7b588a348882e05a4f44b64224",
    "77027bbf65a49cbfe4978a0e4611942ff29121dcda6c305ca68acb71c1461a27",
    "d1438713318f3973fcf33320e2b6372f091587b2d1f0847c3c6a42101a59fb27",
    "fbeb800bac8e2a5c872cb4b6200a1765092122b9bb421042354a63a624044b29",
    "e97f3423eaab1869331122e1b9c554a84efb46c053170e4ea20e793c13e69329",
    "047b20361710d345f4182842816379084c8e34f6f86f29eb57cacfb46fe7c629",
    "6583bd01edbea5e5d5badef63205a19c313de41e9b371b2da4ed951bb6785a2a",
    "7a42ebb266df836bbd75e2f87d650dcbd075c8d73435dc1b69ee56c634f7822a",
    "f4b8c4faba2a9d3e096791d98de26ba8c84174506dc8d6cf895ec7177da1b52b",
    "eac4efd228f63982d7b4bfc2a593f28882f24f59e9956fae22d1090778e1452c",
    "1be3519cd7ea24607d5d07b82f7d31e3231db36ed564f0b31a77e4f5bce50b2f",
    "ff2c473041b9e8022a949a46210ed42cfa1a3c696e4f6edc696b5e80731c5a33",
    "07463be5e8d9b53cd8669191b57359d14a2e41880bafdab7967e52296581e534",
    "861821aa307e8aee76009f4c588f9a294d15c15ed064a80149f374c551b73935",
    "8a937bf8fc495e0c0bdf9364dfae7510e2a2785848ec976d61ae0c3b36356b35",
    "1cc2d177d8418787ca7812ea8efad8fcbb680b3c0d4559ae12743143a3952f36",
    "46f45a88d87e1b8c9f0b6b29864daa8d744fa7a79ceb3dc00666b7b9b0f27e36",
    "d1e0255c9771cf5144fa570e670de51efd63a0f8b279d78a795a9ccb52152539",
    "94175e9e5e7f841ccc87658eecedc212ed18a872aaa9c5d1486616e990d5be39",
    "15a73dbde1979730f3e0c0f694e0b16489e430183eadb52b120d2c3be7c06f3c",
    "6dab3bb72fce0f7af56dd04afd3da248b66f60fa713190a20ea78acec0943c3f",
    "91770f35dad9be25f5d3d1ab9f54e4a966e258a3cb70d8f81e2bef6f99a5b43f",
    "375aff99de485bcf20c141d7a8003537f99fea44696dc1b8ab66f6b75f347541",
    "99851a666d1ff6c2009bbbc6b249c70498f0b08bc9e5c8534b5ceaba47e72144",
    "8aae08ead4130b4259e31c70d0019c404364a055dea9b0711919e6ab6da31746",
    "8a634684c633211a391894773c880af457bc517ce6db2aba4dce6b3be9912846",
    "b68d373cc4a185d1b02dba04baf521bfa263f33e976740ec9bf9970d9a2ba149",
    "c05371f089d002302f757937779e3a91784704d10f40b186e23147d811b3b349",
    "2c790078c694cfdb82e2f5d04c27e4cfd599ac220cd8d4a75e4ea2180f53354f",
    "713411e7526df524d63aaf3da46c9c46f2e037ee53f7a0e17f003e9e1881b34f",
    "85f2b8e7adb7b0fe6b92a0128572bca061a7efe7686301eec378d853b5a40f50",
    "a0fc3f202408485506b16540295f9911f771dd3433663cc6f2c45685b60d2e51",
    "6035e2f603ac28e8881760cb511f0206b5f3233047237d9eecbfd9d2f9862f53",
    "7e73d249164af428e8fac011f6ac6e0c181f4f8717f275b2543f07e429169153",
    "c94667e61ba7cdf2fd565643419db44081a6881235fa19bcdc126313a1a5ab54",
    "8dcdcb7e9e2f161e2e77062e5313d4d3b06a5df288638ad198c3efed0501f656",
    "6f89977bf6aa2598015ded10a57dbbb6c2a1a92d611144d41814eb6c4b661b57",
    "c34181520a3d6d8a4bb7777d6fcba02b223de869cd3d538b99d61b40bdd28a57",
    "b4c934639d61c8b67c1faf6acb7c3503c905909f937dd4da49b987d74d129b57",
    "7e52684a8f0cca6755d7fab93eef848967296cdb622de543111ad9857da1e358",
    "4e3b517685152062698c1c6c2e7daba41d71b4c6a5ecb3a54ec7ef00dfc6f058",
    "050f26dcc5611c779fac8556563feef31b90a150d4f7e98b910ce8d009651d5a",
    "8e020686db747d3105e81785970019435ca852fd909fac9a7582efa89a5f605b",
    "9597877615a02656e9c0e9d8c98795435f997f190da261f69f120698733d0360",
    "590ad46265bff1fdfa1fb17feb160c234f6101ec27118062f5c7b2e6b0ef8060",
    "cf1d41ec1d33f0f754694d2c2d96ddbdd7bb397fb6d9b239c11e7e7a26dac760",
    "c67234441cc2e92f83a57320e8ecad5ae06ee6b3a39b2fb16081861a5c65d065",
    "81058bfc6f2fa86d5083a0710f206865201e82021ab5ae04b01e84674e14c967",
    "ba64837aa5e7faa5f71c1888591cc84da48ecd5263a0f780538849a17849f067",
    "be24812c14bbbdbe6fe07666fdb2a9000a222b7a562f1da04e70268ad22f406b",
    "fd8052e1fc8cdf95193c54bebf3ce460552a839cca56015381f320bdbb268d6d",
    "8d2e5a977d895267a612bd3a2bce43cfc6bad3fbb85f508f18a761ec1ab14f6e",
    "d7123395c1f5d1614d8ac8089a2d5045e77d273a6f61282e0f570061b834ed6f",
    "79c895ac5f8c9d6e11b872b362dcfb939a7c0baeb1532e1f6c4152a91379cb70",
    "af64df5cade7c405357df436085eca2b4d8a716618c8985e12995c8be01e4a72",
    "e16bde89672294b6a6fb89ba09c8a29b7636a2ad4cf484ab4a45cdc826a79e72",
    "4d38a3641763c6922963234f64e49944d98557f79f5fdf2bf69f018a03ea6a74",
    "650451e8261b44942f5b4a30d4b3167824d739850ad28c696d826887da325276",
    "a9b0f242a1a2ad1e5908fff1525c29982826a6c3dd944b5b0f7951a9b9f32977",
    "e337091c3c47fd798291d1df1378f5221fa1dd156f180e79caa9dd9e361f4577",
    "3c448e30fc1682bb3ff6936d4d8256b8dc428d8308791bc5ea9f8fd744cd5477",
    "ddb256d8e2391fb54767918e45aeee719bbf3c6623fb42edc11403c77e9d7d7a",
    "772a6e88e906a42be7eb66ede81cfb8dd7b25973ac2ff4a32c0186e14674457d",
    "bef1190f72d5fb91b037f20ea4b1abdeaab367084acdf19df2c496f05bee937e",
    "65365ac222ec331f67a7bfc250c44385589bb93985373b25c4b2545e53b5bf7f",
    "85a9bcfc730a3dbfd092cf6ded00e544aeea707e077dc7d1ddc8aa706fc17984",
    "047da1bdb51c0c4b723c2293386d6f81c4e61051cb088244759f864ded1f4486",
    "95b882fbb221324ec85e0312afda4338ec0322fc56f1fca0489e8ac5f0640988",
    "05e0db50b0c5b922719967bfe44700ebd2414c99ed5305dc2d61b98f21091f88",
    "761645501fb8451bb0320176517d4ec9019e4646cfaa278171a75999d55ef588",
    "fc525774b18198dcf35b7af6e89680f6c9bfbad0833bd73847f70021e703378b",
    "1a1da8c9492f21f8f9353198bd8cce9bd281fc51d89f13a769ace5a6af43c58b",
    "b1520b461f31147563413d85029adb63af658a10ce1f7d57f876bc651fd13b8f",
    "bf52fe2752375f305cb790e5e13c531393ee4babebf0f23dabcde7bfbe00c08f",
    "69b83f02ff6f39745d74c2859cd476f09e03a7ebe35d7c98017a0612d7fa2c91",
    "e76c0e644f8d16fc412595cf14305c262e0610d3cce9ec2cbdf0277f31ef3491",
    "914145a9687d5d7e358d0919ce5d66afaca87c80dff63df3166ff84b3155ac94",
    "ff20645da772124104f5e893523e7780d903f3a016d9fe2fd3d30ad3096f7997",
    "41e8d5979944dbc067544cbd20283065e036c4df3d3c0a57bd2d818efb61e998",
    "f8e9a251c4bfca48173948980b1297a8b758e648e4868eadc61e4b48cec3899a",
    "00b725a3c0cbf59df22f450bcc0be91539cd58d38c6c343f053f7661b906939a",
    "ec78b05ab4688241f5ff2a73ae38f8685c2e92514bba44340b2fe0e5a7ebd79a",
    "da690750885b735231e52b9110cf46421cddfff449e62ccf86b66144bb11329b",
    "fd68069e742112113cdbef9607f9f95708989148746d00c4813404fc7052fe9e",
    "97cf49f5ac437db8073c26be8416288cf75b94f8b97a1caf6616cda992b7239f",
    "85d1e96d6e9a7e3cf373d63f3c520ace3aacf69ab40fb26c59b079ed4b4319a1",
    "992afec06dcb8c0587d5e4ffe84080c2882a91f264c521e6f43f1e37ce9459a4",
    "0b7c8b590b6eeeda79ae6a524c9557b79449d413c5f98e8131e13817fe0fb7a5",
    "ba404123af39af826a9885a3ec53494f8173d562ef1e021ff841aa70d1aeb8a5",
    "12410b72b41cd861bfe082adbe412e71976d8759a53ef56dfdc8e17ad1d4cba6",
    "773f163b24b69a5f39e782e39e6cc4b798c1f7e2ea04660dbce60546f6f808a8",
    "abdeeb0c30eef7296ff97c7abf3ab4377f39edd4c33274fd22265a8df44be9a8",
    "54ba7d31b147851f48ca3b54bc7018e3cea1847edc2b6978d1bdadf898784dab",
    "8d7085272ebb7760c8e7ef668307dc8f4efb83c0c387977165df06b31db360b1",
    "1f49729c33cf455a63d817073257b69eac5c24761992c2df1a350ee9cfc55cb3",
    "5528f11093b95b96f4657e549ccc28972864e997ec7e2e6f0d2ed22faefcb9b5",
    "84ac6a6f0f16ed34c878f79c2ec1b7c00892393b86022277ad924613071619b6",
    "056683cf82964b780ea4de5a0681ea77278bc770875363b64f06fb5cda2d3eb8",
    "791dd5ab80adef9171d72f5cd6736d96221e87fd627895afd892fefc748255b8",
    "feaf3f0c1116923f797c870b10965192e08e2354ecb410fc2c5345aafbf925b9",
    "4da4f8b71495966604da421db71b1a64356ed95776d8e95a93eaadffd70765b9",
    "550ddf96775c871d98ad6363eb1512a35bd506e9f59bcd4bfa7e173bd55601bb",
    "fc0c1d1fdae045e7be88e67280837cfbdd90f0e5171d13409a4794ab0d2f46bc",
    "74185cbb8504fb55467e6ca776f8f30d171fd16e6c6c3399a33f00f1a479ecbe",
    "19b13d699afef1a52e945b711ce07c0c65b9c5a38c970d6e294f6ad89e835bc2",
    "7ae0253b5fed011c1b0af15f5e4c3d2548f2bb86de917d76eb343ef87d6f14c3",
    "45754f8446ae1b96ff5ffa03b06c9a8421e0166387d955736fb9746c1266a4c3",
    "bcce7c1c1a4fbea67f6d31e91e10c90b5190f09a80a8639c379a18469fd9c2c3",
    "ee804bd62b06f1825b30e09cfe24c2c36f50c426f31125e61e560b8ce27978c5",
    "6f89fdee356c702166b1db4764f6be0d8158dd787e47590c286b700da559dfc5",
    "b11cccc82dd643ced2ff2e3f6fe0e699cc572ffff7ca1a3812f9e68a2c7d14c6",
    "f641b95e99eb392e682272bfa526601f3ba032cd92bfa700e07ac127f6dc34c6",
    "c3c6916a32b71e16ec6525f6b4be30e589a5ecd86afc3b04e7b934132aba9dc7",
    "84e06cc868166a33bea4220f9563d37aed775cc12a92e6d6f92431e0db409ec7",
    "6b0e75084d1671579151042413118d12dcd89dae5259b2fa51a3c7d72d1c07cc",
    "b98c4ced94f6b6b8ebfc0a9e6f81cce1bdb46671622e8bd0ec3817b553afa5d0",
    "1966bd3242231015eb62f8f9095469580a9cfff494441fcb6263ed9788d30dd1",
    "e70d2a1c01a7ea914d65a8f96e31941e4f30e223efb835c923602878a4d915d1",
    "389c144c1bb528aa58d659a9ff4d1bd29fecba7bf7a8b0dfc69ce425b85205d4",
    "0758dca870bfa301fbeb12b5017e1438d6c8fc287d44c8921c9aa7a895c40ad4",
    "ea974954fd149ee50611f9796e74ea3813ee0ed34e63de94c3bdb786e41053d4",
    "a5555a23ad42589f66b6fb07deb262e7538624be90a1665ac57bc0984ca919d6",
    "c9abbdc64ff48496f64b2528d3ce105ec69d73479f41346bfdee88e679c5e7d6",
    "dc523305c04227b6f0a4fb1d0e90b7d69b35388b50195d472b6fffc4ce8719d8",
    "2cc37bb6073a6b6e7f3d57873368c45ce587da63c833f2b756fbc9004d9146d8",
    "df4a692046ce50b592f28e932c68ae068adf620960d8c879f901546ec9296bda",
    "406bfcca5ef96007fceca0300f4140f294d26777ea8cc547a955a062cfdb7ddb",
    "35506d57b70a55dc86a58884af217136d14b53bcef7a66d0d02fd586b85832dd",
    "9af44ac9d693a749c4868b6d95d6da356a83d3d1824cc746e9ef8d224c5f4bde",
    "b2937fa0d38e8edc72a44092860c66d510d527cf45bb9baea2db8f638aae9cdf",
    "be47497840580e7559fb543a3a5bddb53f11817fd137f71541b0c1d0cd5789e0",
    "8cfd584e6415448750465516737526d017867118fd0a1b412170bbb64fb45ee2",
    "5bbff7293c29fa19440996268982ff36e9b0dd9a8a1ce23239a7f724ad7da4e3",
    "20a980b2ee5176dc1f273927e3dc05e1d679328663827eeec6b66a06827239e4",
    "c0c784b1703fad821c8a10a0ebb2512d8ac941d97eca8f26d847284b8c0c5ee7",
    "abf47265b4ffbc693cf79dd63db87e8a9e73571e3f116cfad7f15b3696ac34ea",
    "dc1f4871487838010b10e8d9122a7157ffaecdde7a7e3be4ce4f4125cb9bf7eb",
    "f7a475cd178de12059dd05a0d3e72d6de56f50077170a1c3e9f582be20afd0ec",
    "70bfbb2a3d113733af55ab0f0f6d42284f1a9aad99c45a21e1b0fe778b9ba8ed",
    "4e523fe5b08642821b3d12a4442067301b2f9ff1b824acc4f5faf3cb393d02ee",
    "51dc6a9c4183fdc764e5fb91b62d92b304569dfd9858693ff8e8f630a6ce46ee",
    "3bc13c5733e6bf72e1c988589150d7aeb03fbb6b1459c60ab6715d22d94ae7f1",
    "c701dcd1fce2283c5a2edd3d405ea6bc3bc1c12536bce0f5524d84138652a3f4",
    "30424259769fa1d01983f8681cf4479f739468249503546c59b6d6dc1b3ea6f5",
    "d80a28fdce4cc00bb0ede2d1a277ee196a7a37fba8a965dd994a3405f4b288f6",
    "2c1aeac8c5755dc94e1a307aec6a9819a64f2218e751600c925ebbc6f44bb6f6",
    "0dae4dd4760ef7c74139743f43d3acb1af17a24c7bcd37ae6de0f680b10a48f8",
    "5aa30535c7df544fa66a1173bc2522567cb9c973f7b85fa634652b8fdafd29f9",
    "dc98d353718a0e63636b848ad1e4d5927f18fe016abfac86648e70d6d81a22fb",
    "d1cb356b2af7cef848e10684c1badba8864cea2ebcab54ea3480a90f715696fc",
    "0af0718b231c74a2400acc594bfa7ef7f4c66fbd0e903a2ca8952189054fb4fe"
  ],
  "error": null,
  "id": 1,
  "uuid": "472C3734-25F1-4D74-8BC7-681B7BF20AAC"
}
```

Parameter            | Type          | Description
---------------------|---------------|-------------
[]                   | Array         | A list of transactions.
- hash               | string        | The hash of the transaction.
error                | string        | API error code.
id                   | int           | ID number.
uuid                 | string        | The response ID, which can be used to view this response again with [xrGetReply](https://api.blocknet.co/#xrgetreply).





## omni_listpendingtransactions

Returns a list of unconfirmed Omni transactions, pending in the memory pool.

### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '[]' https://api.oracleminer.com/xrs/omni_listpendingtransactions
```

```plaintext
blocknet-cli xrService omni_listpendingtransactions
```
<code class="api-call">omni_listpendingtransactions</code>

This call does not take parameters.


### Response

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
[
  {
    "txid": "32f7358f83ba864401e56d64f3b3b2c91bf812eb03bfacf98c6dd1dd631bc2fa",
    "fee": "0.00018180",
    "sendingaddress": "1HckjUpRGcrrRAtFaaCAUaGjsPx9oYmLaZ",
    "referenceaddress": "3NiWtMPSTvbVBccT7p6PXiJTQMy4xC76o1",
    "ismine": false,
    "version": 0,
    "type_int": 0,
    "type": "Simple Send",
    "propertyid": 31,
    "divisible": true,
    "amount": "152007.00000000",
    "confirmations": 0
  },
  {
    "txid": "c25758085d3be7f57aa1f39f7328e5c5b7a02929929a8a1212693be6cf3c0f38",
    "fee": "0.00018180",
    "sendingaddress": "1HckjUpRGcrrRAtFaaCAUaGjsPx9oYmLaZ",
    "referenceaddress": "13A1BwihND8JuoEoufAVC2w9de7M3tKNmy",
    "ismine": false,
    "version": 0,
    "type_int": 0,
    "type": "Simple Send",
    "propertyid": 31,
    "divisible": true,
    "amount": "605.00000000",
    "confirmations": 0
  },
  {
    "txid": "e556f7866e319780443381cbadd3ac0cf790c68db94476c4ba0bec1044a0020c",
    "fee": "0.00018180",
    "sendingaddress": "1HckjUpRGcrrRAtFaaCAUaGjsPx9oYmLaZ",
    "referenceaddress": "19FoFcff1sTrCnkkryqRn8rxj25XwwaZ2H",
    "ismine": false,
    "version": 0,
    "type_int": 0,
    "type": "Simple Send",
    "propertyid": 31,
    "divisible": true,
    "amount": "7004.00550000",
    "confirmations": 0
  },
  {
    "txid": "465d31d45dd137caa37be80f59fc9fde54d7fca7e1cfda7e97cc9c89b9862974",
    "fee": "0.00018180",
    "sendingaddress": "1HckjUpRGcrrRAtFaaCAUaGjsPx9oYmLaZ",
    "referenceaddress": "1H8mZLCrfkfgMJdJF6LtdexGYaX6kfkV3c",
    "ismine": false,
    "version": 0,
    "type_int": 0,
    "type": "Simple Send",
    "propertyid": 31,
    "divisible": true,
    "amount": "253.76740000",
    "confirmations": 0
  },
  {
    "txid": "0c65a1f5f03614863ef3bf320483f03bfb62da57aab3eab94dcda3ed08290e99",
    "fee": "0.00013100",
    "sendingaddress": "1Fi9J5TeaWPHdU5cTJ4e9jr3V58SrWtUuT",
    "referenceaddress": "1JB9aH45hELMdhoBb6z3cLiaZ5sVDowGQu",
    "ismine": false,
    "version": 0,
    "type_int": 0,
    "type": "Simple Send",
    "propertyid": 31,
    "divisible": true,
    "amount": "4995.00000000",
    "confirmations": 0
  },
  {
    "txid": "c4f036f792bf4291ad49d3d6b467ecdebb4f0b4124ef3d19ef17b20dd9700142",
    "fee": "0.00013100",
    "sendingaddress": "1Fi9J5TeaWPHdU5cTJ4e9jr3V58SrWtUuT",
    "referenceaddress": "1HgPFyDu6SHTqgEMDC5CcxYKzoScaWTBsk",
    "ismine": false,
    "version": 0,
    "type_int": 0,
    "type": "Simple Send",
    "propertyid": 31,
    "divisible": true,
    "amount": "3572.48530000",
    "confirmations": 0
  },
  {
    "txid": "3ff882d7c58b17589ec7386871eb7d2d41691a34947c033826696ffc3d39250c",
    "fee": "0.00011150",
    "sendingaddress": "1LJ4obqYuiUfBLgsddQpQsfcsP1MgoYRZM",
    "referenceaddress": "1JaFz7ogfxX2ts3vguThwhHgubC7zidPmM",
    "ismine": false,
    "version": 0,
    "type_int": 0,
    "type": "Simple Send",
    "propertyid": 31,
    "divisible": true,
    "amount": "1419.50140000",
    "confirmations": 0
  },
  {
    "txid": "a73307c788411f65b7b3190610379977b1f53939481ed592bf89cc486dd54340",
    "fee": "0.00012850",
    "sendingaddress": "17m5SEXEY8oB9nsyJVRKhGoafhRJ3ukJau",
    "referenceaddress": "1JuEtiEQEcZZxocwqUA5SsD8K3ynrRKspw",
    "ismine": false,
    "version": 0,
    "type_int": 0,
    "type": "Simple Send",
    "propertyid": 31,
    "divisible": true,
    "amount": "24.17923000",
    "confirmations": 0
  },
  {
    "txid": "99840419d75ef62da061ce1ce95ae5df6d6db92e43ba5fa1a79b2aada07754a0",
    "fee": "0.00011150",
    "sendingaddress": "13uWVgb74U8J6YKUrUSNMPCawVsMP6LbRJ",
    "referenceaddress": "1JaFz7ogfxX2ts3vguThwhHgubC7zidPmM",
    "ismine": false,
    "version": 0,
    "type_int": 0,
    "type": "Simple Send",
    "propertyid": 31,
    "divisible": true,
    "amount": "5700.00000000",
    "confirmations": 0
  },
  {
    "txid": "484db0c16d2951b3be3e7a29ee1a51631f28d3886fafba116b26fc8f5df2f72f",
    "fee": "0.00011150",
    "sendingaddress": "1Bjo5pt32CE7zj91X85MBSFtfMrueH3kn3",
    "referenceaddress": "1JaFz7ogfxX2ts3vguThwhHgubC7zidPmM",
    "ismine": false,
    "version": 0,
    "type_int": 0,
    "type": "Simple Send",
    "propertyid": 31,
    "divisible": true,
    "amount": "287.94130000",
    "confirmations": 0
  },
  {
    "txid": "d7bde4b7eba15e0d86f4070902f6db34b7c1d679ca5a632d0103398e15b6e7a5",
    "fee": "0.00015000",
    "sendingaddress": "17jCC6JLKUYYRrjW9LwkSFtiFLSwgNbHhX",
    "referenceaddress": "1E8GV6xVcLM6RyMecddH9f8vFeJcfu7ZWM",
    "ismine": false,
    "version": 0,
    "type_int": 0,
    "type": "Simple Send",
    "propertyid": 31,
    "divisible": true,
    "amount": "7820.76192759",
    "confirmations": 0
  },
  {
    "txid": "e78388c53f5bd5592aedf327f367e6e8905c0916992f304b529e5c811ac30010",
    "fee": "0.00013554",
    "sendingaddress": "1KePmi1wR1cwodaCCPhddVmLCuWsoURaDD",
    "referenceaddress": "18UDKhLCaz7ELVwBgejpYheqnymLiVVmsK",
    "ismine": false,
    "version": 0,
    "type_int": 0,
    "type": "Simple Send",
    "propertyid": 31,
    "divisible": true,
    "amount": "64.84524700",
    "confirmations": 0
  },
  {
    "txid": "e037a21a237f3134dc8e868691facacb00e7d5dc1ce3f55a166ab1cd4b4bc448",
    "fee": "0.00010539",
    "sendingaddress": "1PVxKZUw1paYUVDqquKbVcLipfh4ppcNz9",
    "referenceaddress": "1NYSY9zwSBEZDbCZmhuapyXTWNCQosfqRG",
    "ismine": false,
    "version": 0,
    "type_int": 4,
    "type": "Send All",
    "ecosystem": "main",
    "confirmations": 0
  },
  {
    "txid": "f901710876289850ffff95da8aef1416ca609b18c0fa2d80eec73b346f4877e0",
    "fee": "0.00007524",
    "sendingaddress": "1K2p4fYSU5PMmSZUEkdxKZLjxSHATaw2kD",
    "referenceaddress": "1Dd15VjJhq6eu2QHPenLfoYDCJv5ZxmHKy",
    "ismine": false,
    "version": 0,
    "type_int": 0,
    "type": "Simple Send",
    "propertyid": 31,
    "divisible": true,
    "amount": "258.30690000",
    "confirmations": 0
  },
  {
    "txid": "39650ce1afab4864aaf3c1e3c3d083b70daa142bc027561b35bda52bba2249d0",
    "fee": "0.00011857",
    "sendingaddress": "1CTDxDwS2VV4PRE4xK5tzijf7o2FgDnyez",
    "referenceaddress": "1HBQudUbkJiyXcqNPZ1GkYUimkswdaD5Se",
    "ismine": false,
    "version": 0,
    "type_int": 0,
    "type": "Simple Send",
    "propertyid": 31,
    "divisible": true,
    "amount": "500.00000000",
    "confirmations": 0
  },
  {
    "txid": "dbc6323e3574555b69cddb8c981ba5e9a5125c2f7511161048a3256834d64b81",
    "fee": "0.00007368",
    "sendingaddress": "1EL2ePgVmxdBSTduXTAN1TczJZwLTMJfxx",
    "referenceaddress": "1P9a6j8y9THMe5vjLWbZfRmbiL9UutjjLK",
    "ismine": false,
    "version": 0,
    "type_int": 0,
    "type": "Simple Send",
    "propertyid": 31,
    "divisible": true,
    "amount": "88.37758897",
    "confirmations": 0
  },
  {
    "txid": "8abcc1ada5a3feca0c9e9eddf68e697aac1e34c32e51a645180bb9ca586f28e8",
    "fee": "0.00008169",
    "sendingaddress": "1Ldquqk821KecY8TtnPRx8YDpQW7aFyqUd",
    "referenceaddress": "37pfyiaeRe5kSMcVFpLMdxiqgyCASGQNpo",
    "ismine": false,
    "version": 0,
    "type_int": 0,
    "type": "Simple Send",
    "propertyid": 31,
    "divisible": true,
    "amount": "4309.00000000",
    "confirmations": 0
  },
  {
    "txid": "170d432618737ec1456fe7d50d360aa31662314e910974c1528d5e9941f05ce9",
    "fee": "0.00007196",
    "sendingaddress": "1FoWyxwPXuj4C6abqwhjDWdz6D4PZgYRjA",
    "referenceaddress": "3DTZ5dsbTVeCnueQsd7HdATefPkH7pZkBa",
    "ismine": false,
    "version": 0,
    "type_int": 0,
    "type": "Simple Send",
    "propertyid": 31,
    "divisible": true,
    "amount": "1001.22000000",
    "confirmations": 0
  },
  {
    "txid": "1a0501555afab2a9440a494c7839eff5c5ce7d40e9f9e75a2855e2363ed39c1c",
    "fee": "0.00008169",
    "sendingaddress": "1FxRjC8ocZ6JF1hnpzLSydG8DxAMaTdfn4",
    "referenceaddress": "1GV9rCq1BA4Tid3zHBdVMUNXecka5vATju",
    "ismine": false,
    "version": 0,
    "type_int": 0,
    "type": "Simple Send",
    "propertyid": 31,
    "divisible": true,
    "amount": "5.00000000",
    "confirmations": 0
  },
  {
    "txid": "1aa78918dd9b0fc2f57ab463dfaad496e41746f7edd51d7b627ed319e934d54e",
    "fee": "0.00010724",
    "sendingaddress": "1NXkq2StVjywfuCVq2MF5kLTEwbCXCffEF",
    "referenceaddress": "1DR5XnVdym8VD5eWLJrApdfpPKs8fgQNo9",
    "ismine": false,
    "version": 0,
    "type_int": 0,
    "type": "Simple Send",
    "propertyid": 31,
    "divisible": true,
    "amount": "2.35812499",
    "confirmations": 0
  },
  {
    "txid": "2d04966ec5d488d6a0ee24f42bc28de5b391e56051acbca6e0ffbed243f15042",
    "fee": "0.00010724",
    "sendingaddress": "1CNCjJezsDuk8ioZN98SQX86bQ9cXsaDPZ",
    "referenceaddress": "1DR5XnVdym8VD5eWLJrApdfpPKs8fgQNo9",
    "ismine": false,
    "version": 0,
    "type_int": 0,
    "type": "Simple Send",
    "propertyid": 31,
    "divisible": true,
    "amount": "2.38625406",
    "confirmations": 0
  }
]
```

```plaintext
{
  "reply": [
    {
      "txid": "e17b4abb83c1fc257e28da22eb27ca477ba19936144320f6002a6f520f858c73",
      "fee": "0.00050000",
      "sendingaddress": "115md8GZ5S8CmvUj8a8cW58YcKvv2SekYf",
      "referenceaddress": "35Kx9CxRFdVjfiDmN1yPRtAx5SgM5oU9BS",
      "ismine": false,
      "version": 0,
      "type_int": 0,
      "type": "Simple Send",
      "propertyid": 31,
      "divisible": true,
      "amount": "895.00000000",
      "confirmations": 0
    },
    {
      "txid": "dc9ed9264e7f863719f585bd238a7b538e950335d339db67904a8ad4c18680b0",
      "fee": "0.00054784",
      "sendingaddress": "39ZEaLMDxWi5EWx9cQ2W3ixDP8rWHhz8GY",
      "referenceaddress": "18j5zmf2hmJqokyk23C9gpgjW52svKR374",
      "ismine": false,
      "version": 0,
      "type_int": 0,
      "type": "Simple Send",
      "propertyid": 31,
      "divisible": true,
      "amount": "261.53400000",
      "confirmations": 0
    },
    {
      "txid": "f7d8a67cc8108d456d129ff0d3eeb644bc97d0d6dfb2f229c5a1cf4992165b8f",
      "fee": "0.00037343",
      "sendingaddress": "16CocFaPZAc8FLzzUTSbBgAEUUF93CnpEE",
      "referenceaddress": "18i2S8UkktAberzi3Mm7A3eN6eVqtC3yxM",
      "ismine": false,
      "version": 0,
      "type_int": 0,
      "type": "Simple Send",
      "propertyid": 31,
      "divisible": true,
      "amount": "3000.00000000",
      "confirmations": 0
    },
    {
      "txid": "e207c54f302ccf9c8373faf51317c21e550607dc917f07bb84069a2326ff58ae",
      "fee": "0.00037343",
      "sendingaddress": "17qwNuv11GeaJ9xmzDn3qqyoivyznrMRNY",
      "referenceaddress": "18i2S8UkktAberzi3Mm7A3eN6eVqtC3yxM",
      "ismine": false,
      "version": 0,
      "type_int": 0,
      "type": "Simple Send",
      "propertyid": 31,
      "divisible": true,
      "amount": "2005.00000000",
      "confirmations": 0
    },
    {
      "txid": "0ef8665adb70b1cec73ecf34136cc30e21eaff92fadc80303867a5c46815a83f",
      "fee": "0.00037343",
      "sendingaddress": "158nJnE1cDa43iSFmTGe8Ppx6at3Nv8bCh",
      "referenceaddress": "18i2S8UkktAberzi3Mm7A3eN6eVqtC3yxM",
      "ismine": false,
      "version": 0,
      "type_int": 0,
      "type": "Simple Send",
      "propertyid": 31,
      "divisible": true,
      "amount": "10771.97740000",
      "confirmations": 0
    },
    {
      "txid": "fe110a83ded359e15c9e490ce38690ad1f14a475b2eb639b61c80717cd5902bd",
      "fee": "0.00022300",
      "sendingaddress": "1KiiBhJb2aQRzPm3nutJxgWk2zcVyf6PJQ",
      "referenceaddress": "1JaFz7ogfxX2ts3vguThwhHgubC7zidPmM",
      "ismine": false,
      "version": 0,
      "type_int": 0,
      "type": "Simple Send",
      "propertyid": 31,
      "divisible": true,
      "amount": "781.10310000",
      "confirmations": 0
    },
    {
      "txid": "0cebb7252569beaa33370a19dafcfe7abfc33a0a78111fdcbe2724a0892dd20e",
      "fee": "0.00022300",
      "sendingaddress": "1DwzXk5P2JGUBeECRrMZAB3UbKTWtQXUQT",
      "referenceaddress": "1JaFz7ogfxX2ts3vguThwhHgubC7zidPmM",
      "ismine": false,
      "version": 0,
      "type_int": 0,
      "type": "Simple Send",
      "propertyid": 31,
      "divisible": true,
      "amount": "1435.92220000",
      "confirmations": 0
    },
    {
      "txid": "c67fd3ff8d1df732492c26d99126ccf0c6f1ee208ae0adc83fb49f97e2aff4d4",
      "fee": "0.00040000",
      "sendingaddress": "1Nz8FiDEftLGWTepJrGoANLppN7RaY1u1W",
      "referenceaddress": "1M2DoF2J7RLCDLDTzbGFLrex5tAu4jTHND",
      "ismine": false,
      "version": 0,
      "type_int": 0,
      "type": "Simple Send",
      "propertyid": 31,
      "divisible": true,
      "amount": "720.00000000",
      "confirmations": 0
    },
    {
      "txid": "882ac8684d2930c2c1d14d12e55ebe6ba30d0d2ada77aefbce5a8b95cb93b75c",
      "fee": "0.00020000",
      "sendingaddress": "12PMymX5srLMaExVUxU2S5Qpg6QXm7w63m",
      "referenceaddress": "1HsADXCiAphKJW92MvbCitkNUbNN38u4hb",
      "ismine": false,
      "version": 0,
      "type_int": 0,
      "type": "Simple Send",
      "propertyid": 31,
      "divisible": true,
      "amount": "55.83408800",
      "confirmations": 0
    },
    {
      "txid": "f0710b2d6bf4f23c2bcbfcf6cc1bf0a1a8ce9c182a1dca5d98f599dab851f7e2",
      "fee": "0.00018180",
      "sendingaddress": "1HckjUpRGcrrRAtFaaCAUaGjsPx9oYmLaZ",
      "referenceaddress": "1B3ik8zjoNYq1gR8pjcFeUkgwkq8zb2AdT",
      "ismine": false,
      "version": 0,
      "type_int": 0,
      "type": "Simple Send",
      "propertyid": 31,
      "divisible": true,
      "amount": "6695.14340000",
      "confirmations": 0
    },
    {
      "txid": "a1d5aced8f235a64ef4a573abc3f4883466453e22ed5cf5de4a06d83554046d1",
      "fee": "0.00018180",
      "sendingaddress": "1HckjUpRGcrrRAtFaaCAUaGjsPx9oYmLaZ",
      "referenceaddress": "1FFdXvmThuTFbDnf71pouWsvQTbmwfnZbr",
      "ismine": false,
      "version": 0,
      "type_int": 0,
      "type": "Simple Send",
      "propertyid": 31,
      "divisible": true,
      "amount": "398.45820000",
      "confirmations": 0
    },
    {
      "txid": "3181df09125157ed1f33cca1a527c7d8baf19ecb2e33864b011535340144b7b0",
      "fee": "0.00018180",
      "sendingaddress": "1HckjUpRGcrrRAtFaaCAUaGjsPx9oYmLaZ",
      "referenceaddress": "1MQTSzDWNSHxUSksWEpr68jEGxxjNGdCpG",
      "ismine": false,
      "version": 0,
      "type_int": 0,
      "type": "Simple Send",
      "propertyid": 31,
      "divisible": true,
      "amount": "500.00000000",
      "confirmations": 0
    },
    {
      "txid": "8a75381cd7d71dfa905e9cc1693a4a95369cb8950718191ca9169ffe6a64172e",
      "fee": "0.00018180",
      "sendingaddress": "1HckjUpRGcrrRAtFaaCAUaGjsPx9oYmLaZ",
      "referenceaddress": "1PmnoNBpXoahHNiskdiVih717TcSjEKCn9",
      "ismine": false,
      "version": 0,
      "type_int": 0,
      "type": "Simple Send",
      "propertyid": 31,
      "divisible": true,
      "amount": "550.02410000",
      "confirmations": 0
    },
    {
    ...
    }
  ],
  "error": null,
  "id": 1,
  "uuid": "61136E65-870C-4DC8-9D33-0DD20F972BB3"
}
```

Parameter            | Type          | Description
---------------------|---------------|-------------
txid                 | string        | The hex-encoded hash of the transaction.
fee                  | string        | The transaction fee in bitcoins.
sendingaddress       | string        | The Bitcoin address of the sender.
referenceaddress     | string        | A Bitcoin address used as reference (if any).
ismine               | boolean       | Whether the transaction involes an address in the wallet.
version              | int           | The transaction version.
type_int             | int           | The transaction type as number.
type                 | string        | The transaction type as string.
propertyid           | int           | The identifier of sent tokens.
divisble             | boolean       | Whether the sent tokens are divisible.
amount               | string        | The number of tokens sent to owners.
confirmations        | int           | The number of transaction confirmations.
error                | string        | API error code.
id                   | int           | ID number.
uuid                 | string        | The response ID, which can be used to view this response again with [xrGetReply](https://api.blocknet.co/#xrgetreply).





## omni_listproperties

Lists all tokens or smart properties.

### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '[]' https://api.oracleminer.com/xrs/omni_listproperties
```

```plaintext
blocknet-cli xrService omni_listproperties
```
<code class="api-call">omni_listproperties</code>

This call does not take parameters.


### Response

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
[
  {
    "propertyid": 2147484131,
    "name": "Blockchain Universal Patents",
    "category": "Public administration and defence; compulsory social security",
    "subcategory": "Other",
    "data": "Blockchain Universal Patents is Blockchain Patent No. 01. Blockchain Universal Patents provides a methodology for universal search and registration of intellectual property rights on the Bitcoin Blockchain. This includes all different types...",
    "url": "https://www.blockchainuniversalpatents.com",
    "divisible": false
  },
  {
    "propertyid": 2147484132,
    "name": "Tetoncoin",
    "category": "Other service activities",
    "subcategory": "Other",
    "data": "Stablecoin For Exchange",
    "url": "http://araguaneybits.com",
    "divisible": true
  },
  {
    "propertyid": 2147484133,
    "name": "USDC",
    "category": "Financial and insurance activities",
    "subcategory": "Other",
    "data": "USDT eq",
    "url": "",
    "divisible": true
  },
  {
    "propertyid": 2147484134,
    "name": "FirstStar",
    "category": "",
    "subcategory": "",
    "data": "",
    "url": "",
    "divisible": false
  },
  {
    "propertyid": 2147484135,
    "name": "nazcacoin",
    "category": "Administrative and support service activities",
    "subcategory": "Employment activities",
    "data": "Criptomoneda social para proyecto Perú",
    "url": "",
    "divisible": true
  },
  {
    "propertyid": 2147484136,
    "name": "SYBPAY",
    "category": "Real estate activities",
    "subcategory": "",
    "data": "We allow consumers to make real estate transactions quickly and easily with syb pay coins",
    "url": "https://www.sybcrowdfunding.com",
    "divisible": true
  }
]
```

```plaintext
{
  "reply": [
    {
      "propertyid": 1,
      "name": "Omni tokens",
      "category": "N/A",
      "subcategory": "N/A",
      "data": "Omni tokens serve as the binding between Bitcoin, smart properties and contracts created on the Omni Layer.",
      "url": "http://www.omnilayer.org",
      "divisible": true
    },
    {
       "propertyid": 2,
       "name": "Test Omni tokens",
       "category": "N/A",
       "subcategory": "N/A",
       "data": "Test Omni tokens serve as the binding between Bitcoin, smart properties and contracts created on the Omni Layer.",
       "url": "http://www.omnilayer.org",
       "divisible": true
    },
    {
       "propertyid": 3,
       "name": "MaidSafeCoin",
       "category": "Crowdsale",
       "subcategory": "MaidSafe",
       "data": "SAFE Network Crowdsale (MSAFE)",
       "url": "www.buysafecoins.com",
       "divisible": false
    },
    {
       "propertyid": 4,
       "name": "Craig",
       "category": "Personal",
       "subcategory": "Name",
       "data": "Be.",
       "url": "udecker.com",
       "divisible": true
    },
    {
       "propertyid": 5,
       "name": "UpbeatOctoProp",
       "category": "Goodwill",
       "subcategory": "Thank You",
       "data": "The Upbeat Octopus Appreciates You!",
       "url": "http://upbeatoctopus.com",
       "divisible": false
    },
    {
       "propertyid": 6,
       "name": "GENERcoin",
       "category": "Tangible Property",
       "subcategory": "Renewable Biofuel",
       "data": "Arterran Renewables Biofuel (10kbtu)",
       "url": "www.arterranrenewables.com",
       "divisible": false
    },
    {
       "propertyid": 7,
       "name": "GENERcoin",
       "category": "Tangible Property",
       "subcategory": "Renewable Biofuel",
       "data": "Arterran Renewables Biofuel (10kbtu)",
       "url": "www.genercoin.org",
       "divisible": false
    },
    {
       ...
    }
  ],
  "error": null,
  "id": 1,
  "uuid": "2AD9C843-CDDF-4CEA-BB81-C2B0E888ECC6"
}
```

Parameter            | Type          | Description
---------------------|---------------|-------------
propertyid           | int           | The identifier of the tokens.
name                 | string        | The name of the tokens.
category             | string        | The category used for the tokens.
subcategory          | string        | The subcategory used for the tokens.
data                 | string        | Additional information or a description.
url                  | string        | An URI, for example pointing to a website.
divisible            | boolean       | Whether the tokens are divisible.
error                | string        | API error code.
id                   | int           | ID number.
uuid                 | string        | The response ID, which can be used to view this response again with [xrGetReply](https://api.blocknet.co/#xrgetreply).





## omni_listtransactions

List wallet transactions, optionally filtered by an address and block boundaries.

### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '[]' https://api.oracleminer.com/xrs/omni_listtransactions
```

```plaintext
blocknet-cli xrService omni_listtransactions
```
<code class="api-call">omni_listtransactions</code>

This call does not take parameters.


### Response

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
{
  "result": [],
  "error": null,
  "id": 1
}
```

```plaintext
{
  "reply": [
  ],
  "error": null,
  "id": 1,
  "uuid": "2AD9C843-CDDF-4CEA-BB81-C2B0E888ECC6"
}
```

Parameter            | Type          | Description
---------------------|---------------|-------------
reply                | Array         | List of wallet transactions. 
error                | string        | API error code.
id                   | int           | ID number.
uuid                 | string        | The response ID, which can be used to view this response again with [xrGetReply](https://api.blocknet.co/#xrgetreply).

**Note:** This call will not return any wallet transactions.
