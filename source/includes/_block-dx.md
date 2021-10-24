# Block DX

Call                                               | Description
---------------------------------------------------|---------------------------------
[dxGet24hrTradeHistory](#dxget24hrtradehistory)    | View the XBridge trade history for the past 24 hours.
[dxGet24hrTradeSummary](#dxget24hrtradesummary)    | View the XBridge trade summary for the past 24 hours.
[dxGetOrders](#dxgetorders)                        | View the live Block DX order book of a chosen maker/taker.

## dxGet24hrTradeHistory

> Sample Data

```cli
{
  "ticker": "BLOCK"
}
```
This call is used to view the XBridge trade history of a given asset for the past 24 hours.

### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '["BLOCK"]' https://api.oracleminer.com/xrs/dxGet24hrTradeHistory
```

```plaintext
blocknet-cli xrService dxGet24hrTradeHistory BLOCK
```
<code class="api-call">dxGet24hrTradeHistory [ticker]</code>

Parameter       | Type       | Description
----------------|------------|-------------
ticker          | string     | Ticker of the asset 


### Response Parameters

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
[
  {
    "timestamp": 1588606000,
    "txid": "3964ce96e7c1be2e9f0601baa1724150929d11dc37c88267e276ae65daac732c",
    "to": "BLOCK",
    "xid": "f7dc0cd6d893e595ea1927cbcdd1ecabda2dda9295ac5f3655c695c4abb802bd",
    "from": "LTC",
    "fromAmount": 0.7875,
    "toAmount": 35
  },
  {
    "timestamp": 1588603991,
    "txid": "1067885720569d12ac1658235fd2bfe3cd73f45361a086df61e4ff49f5a9c881",
    "to": "BLOCK",
    "xid": "7626c6559bb07547abd3560bbf44dfe534f7918da8e086bfdcb0a5178f999a9e",
    "from": "LTC",
    "fromAmount": 1.13,
    "toAmount": 50
  },
  {
    "timestamp": 1588603991,
    "txid": "2e0bd44e5a53483cc9bc498a633c40a6d6d7fe0bacf8b66d394b380f1296759e",
    "to": "BLOCK",
    "xid": "19d6786d03db2abff382034c6bb3e9b1b59114ee9051d5db0a33437caf1a0aae",
    "from": "LTC",
    "fromAmount": 1.13,
    "toAmount": 50
  },
  {
    "timestamp": 1588576091,
    "txid": "8f8462c134d749adab91be90c6bf2f94ccfbe7d08eb0f9460d14a13bdc04bc71",
    "to": "BLOCK",
    "xid": "dbf32d50b7a9ee8d236ab90a86fa9b9fecf5411c8ffda3a78b59dcc9851cd060",
    "from": "LTC",
    "fromAmount": 1.1285,
    "toAmount": 50
  },
  {
    "timestamp": 1588576088,
    "txid": "67a3febdda51d2244ce3825605942bd6aafc75a6a5305ddf57a9f4016e70b672",
    "to": "BLOCK",
    "xid": "392b0375a2f88dbeaf2ca933c51249410b943440ab27b48a55253119fd889e44",
    "from": "LTC",
    "fromAmount": 1.128,
    "toAmount": 50
  },
  {
    "timestamp": 1588576088,
    "txid": "c258ddaaa387789e0e7df4edef3f18f38a6d1f8809b5f59abf1013a477d38995",
    "to": "BLOCK",
    "xid": "a5389fd8962ddf4fed1b5f4d0a3c19303f3b627965ffc2fd70bd2446b982e24b",
    "from": "LTC",
    "fromAmount": 1.1275,
    "toAmount": 50
  },
  {
    "timestamp": 1588576002,
    "txid": "3bd02de2f1702256cdff9cccc94a98a4578fe4db61028027f7b5dd6e9a16b2a8",
    "to": "BLOCK",
    "xid": "5b7c5ffca803d0b5c4d952f21a037a3a3494b82decabfeccb9baa58faa9f62d8",
    "from": "LTC",
    "fromAmount": 1.127,
    "toAmount": 50
  },
  {
    "timestamp": 1588576002,
    "txid": "8d7a18d4efc365071677fa6697478aa7e3f373f7897b125efa1c809ad5aaa1bd",
    "to": "BLOCK",
    "xid": "c85f1dcd374eafa6a7a4570c7500d8fdf67a964e10d2a18eeecaf9ef3adabed4",
    "from": "LTC",
    "fromAmount": 1.1265,
    "toAmount": 50
  },
  {
    "timestamp": 1588575808,
    "txid": "6d0d74037095a6d3e3d1f4cdc15b2b61a8d81645c0ff6f1dee936e9b4e0082ee",
    "to": "BLOCK",
    "xid": "058e20f390b2373fafbb59959161d8922bd7900cd2c8819fc27c0fe01540b541",
    "from": "LTC",
    "fromAmount": 0.675,
    "toAmount": 30
  },
  {
    "timestamp": 1588575808,
    "txid": "14fdf79efdff927ecad9ef13914444d630cad390d6f3194bb7d11e6ed72b3cb7",
    "to": "BLOCK",
    "xid": "c90f83df0a160183bfda1515575b0a39ef32d2243b8215416f5a3146bd8715db",
    "from": "LTC",
    "fromAmount": 1.126,
    "toAmount": 50
  },
  {
    "timestamp": 1588575808,
    "txid": "bac8dc2e32e4fb1f453b9d25fe85cde006b068e346c63f0f02f080a1411b10c7",
    "to": "BLOCK",
    "xid": "2cd0039cffb6fa6d759da5d0e408af731f2f06f74a14cdbb1a2fbde091fa0bc1",
    "from": "LTC",
    "fromAmount": 1.125,
    "toAmount": 50
  },
  {
    "timestamp": 1588575808,
    "txid": "2eec4d685ab72b12e80f960e684df5424622ea218c4e140baeb2f34577a2b6db",
    "to": "BLOCK",
    "xid": "345f6c1fa54733fd6b826f962b18f5a11ec37ed24d532702fcf99af276f88526",
    "from": "LTC",
    "fromAmount": 1.1255,
    "toAmount": 50
  }
]
```

```plaintext
{
  "reply": [
    {
      "timestamp": 1576194576,
      "txid": "539f14c7fa042bfda87489166fe4ea511ab823e8eee8d8ed98d9c36af52dcc79",
      "to": "BLOCK",
      "xid": "67468e22e7a28454e3bca9222de6665f007f4dd7f7a5f141477a07833a4cc8fc",
      "from": "LTC",
      "fromAmount": 1.68000000,
      "toAmount": 125
    },
    {
      "timestamp": 1576194403,
      "txid": "5c8658dca40913bfa0f1d945b2d04f3f2a9f78aa1112d1cdc5628962bc19fee9",
      "to": "BLOCK",
      "xid": "4c65c61a987b8bc34f0a7ff3e6ac834b538033fad2bef24dcce1788bc462b477",
      "from": "LTC",
      "fromAmount": 1.68000000,
      "toAmount": 125
    },
    {
      "timestamp": 1576193215,
      "txid": "af36ca4a8a3d7b8ed03d3ac0fcf0318b71e63d5eabb3c26afe751eef1dcb65ff",
      "to": "BLOCK",
      "xid": "5316c9b871434516a71fcbc5738f89401fb2a9193caebe7c12f8f9178de68371",
      "from": "LTC",
      "fromAmount": 1.68000000,
      "toAmount": 125
    },
    {
      "timestamp": 1576192777,
      "txid": "4a5dd8aa6a0e39c525e26168c1ca1143fbb4b0a97ccc01a4f1d830db71e081d8",
      "to": "BLOCK",
      "xid": "122d6de73ed7a51d5ad14e63f71c5c7cefab941d89540fd4a768ac77e816e2a3",
      "from": "LTC",
      "fromAmount": 1.68000000,
      "toAmount": 125
    },
    {
      "timestamp": 1576158216,
      "txid": "cf29b123654c90e5df74e3a5026f4d4ba0613ab3b6e6411249cfd59773906fe8",
      "to": "BLOCK",
      "xid": "b59ddb80e0e57467e1bdadae37c9065029eb9774d10513c68b84e05d4523e5f5",
      "from": "LTC",
      "fromAmount": 5.04000000,
      "toAmount": 375
    },
    {
      "timestamp": 1576151196,
      "txid": "a27606dbf53523d9d18053a61dda6a008d932cc036af23e154f8a64419236a27",
      "to": "BLOCK",
      "xid": "73fae96efa727faa818c944d0ae37505be262abe5e94e3a83ac8c792ae015682",
      "from": "LTC",
      "fromAmount": 0.32716400,
      "toAmount": 24.62211400
    }
  ],
  "uuid": "08AFB2D1-663E-4BEE-B84A-013A03B0095B"
}
```

Parameter     | Type          | Description
--------------|---------------|-------------
timestamp     | int           | Unix epoch timestamp of when the trade took place.
txid          | string        | Blocknet trade fee transaction ID.
to            | string        | Service Node that received the trade fee.
xid           | string        | XBridge transaction ID.
from          | string        | Taker trading asset; the ticker of the asset being sold by the taker.
fromAmount    | int           | Taker trading size.
to            | string        | Maker trading asset; the ticker of the asset being sold by the maker.
toAmount      | int           | Maker trading size.
uuid          | string        | The response ID, which can be used to view this response again with [xrGetReply](https://api.blocknet.co/#xrgetreply).




## dxGet24hrTradeSummary

> Sample Data

```cli
{
  "ticker": "BLOCK"
}
```
This call is used to view the XBridge trade summary for a given asset for the past 24 hours and does *not* include values of the inverse market. Only markets that have had trades in the past 24 hours will be included.


### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '["BLOCK"]' https://api.oracleminer.com/xrs/dxGet24hrTradeSummary
```

```plaintext
blocknet-cli xrService dxGet24hrTradeSummary BLOCK
```
<code class="api-call">dxGet24hrTradeSummary [ticker]</code>

Parameter       | Type       | Description
----------------|------------|-------------
ticker          | string     | Ticker of the asset 


### Response Parameters

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
[
  {
    "BLOCK-LTC": {
      "volume": 565,
      "price": "44.42470013",
      "open": "44.42470013",
      "high": "44.44444444",
      "low": "44.24778761",
      "close": "44.44444444",
      "timestamp": 1588606000
    }
  },
  {
    "LTC-BLOCK": {
      "volume": 6.715133,
      "price": "0.02250423",
      "open": "0.02250423",
      "high": "0.02253621",
      "low": "0.02209578",
      "close": "0.02215513",
      "timestamp": 1588605738
    }
  },
  {
    "BTC-BLOCK": {
      "volume": 0.00126,
      "price": "0.00012600",
      "open": "0.00012600",
      "high": "0.00012600",
      "low": "0.00012600",
      "close": "0.00012600",
      "timestamp": 1588587160
    }
  }
]
```

```plaintext
{
  "reply": [
    {
      "BLOCK-LTC": {
        "volume": 1024.52211400,
        "price": 75.25924001,
        "open": 75.25924001,
        "high": 75.25924001,
        "low": 74.34523810,
        "close": 74.34523810,
        "timestamp": 1576195152
      }
    }
  ],
  "uuid": "A84F94D2-31FA-412E-824B-6E5F4C3B941A"
}
```

Parameter     | Type          | Description
--------------|---------------|-------------
Object        | object        | The market in maker-taker format and associated data.
volume        | string        | Rolling 24hr trade volume denominated in the maker (first asset in the market pair).
price         | string        | The last trade price.
open          | string        | Rolling 24hr opning trade price.
high          | string        | Highest trade price in the past 24hrs.
low           | string        | Lowest trade price in the past 24hrs.
close         | string        | Rolling 24hr closing trade price.
timestamp     | int           | The Unix epoch timestamp of when the last trade took place.
uuid          | string        | The response ID, which can be used to view this response again with [xrGetReply](https://api.blocknet.co/#xrgetreply).




## dxGetOrders

> Sample Data

```cli
{
  "maker": "LTC",
  "taker": "BLOCK"
}
```

View the live Block DX order book based on a chosen maker and taker asset.


### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '["LTC","BLOCK"]' https://api.oracleminer.com/xrs/dxGetOrders
```

```plaintext
blocknet-cli xrService dxGetOrders LTC BLOCK
```
<code class="api-call">dxGetOrders [maker] [taker]</code>

Parameter       | Type       | Description
----------------|------------|-------------
maker           | string     | Maker trading asset; the ticker of the asset being sold by the maker.
taker           | string     | Taker trading asset; the ticker of the asset being sold by the taker.

### Response Parameters

<aside class="success">
200 OK
</aside>

> Sample 200 Response \(Detail 1)

```shell
[
  {
    "id": "5ac469616ba587f20ceef0e7e091ac7eb9816be3eefa6624c3de4f459d94e309",
    "maker": "LTC",
    "maker_size": "0.066011",
    "taker": "BLOCK",
    "taker_size": "3.006562",
    "updated_at": "2020-05-04T15:40:57.238Z",
    "created_at": "2020-05-04T15:24:04.979Z",
    "status": "open"
  },
  {
    "id": "4f42254e1db0c784e06967282ff0fa4fa90d654c7e83120feabf1ae2e80b540d",
    "maker": "LTC",
    "maker_size": "1.000755",
    "taker": "BLOCK",
    "taker_size": "52.950000",
    "updated_at": "2020-05-04T15:43:54.366Z",
    "created_at": "2020-05-03T10:28:42.989Z",
    "status": "open"
  },
  {
    "id": "bb40cbf13e29d6b89f0d8ba342496c84ca34a925c3c5181d21a23a7b59f3591a",
    "maker": "LTC",
    "maker_size": "0.387345",
    "taker": "BLOCK",
    "taker_size": "19.103415",
    "updated_at": "2020-05-04T15:45:57.212Z",
    "created_at": "2020-05-04T15:24:53.221Z",
    "status": "open"
  },
  {
    "id": "df8fb6d051a2fe866efaeb2e051e08288a209ddc788bef6add2110f0235a5720",
    "maker": "LTC",
    "maker_size": "0.279195",
    "taker": "BLOCK",
    "taker_size": "12.844200",
    "updated_at": "2020-05-04T15:44:39.851Z",
    "created_at": "2020-05-04T15:44:39.720Z",
    "status": "open"
  },
  {
    "id": "c4af9e12a9a6e9f8635e5c7f7ec4439de961da7b57d4269b4bc8268b5f1b0e27",
    "maker": "LTC",
    "maker_size": "0.066011",
    "taker": "BLOCK",
    "taker_size": "3.129169",
    "updated_at": "2020-05-04T15:45:12.576Z",
    "created_at": "2020-05-04T15:24:10.356Z",
    "status": "open"
  },
  {
    "id": "d9c418608436b58a119e8bf3ea893cb52fab817f9e34e16ca396a21726864d29",
    "maker": "LTC",
    "maker_size": "0.298756",
    "taker": "BLOCK",
    "taker_size": "13.460827",
    "updated_at": "2020-05-04T15:40:55.808Z",
    "created_at": "2020-05-04T15:24:02.634Z",
    "status": "open"
  },
  {
    "id": "ef0ec8a6b2e92763b41c50d51556a01521b2f809387d4961d92ab407cb217e33",
    "maker": "LTC",
    "maker_size": "0.251747",
    "taker": "BLOCK",
    "taker_size": "11.414431",
    "updated_at": "2020-05-04T15:44:45.019Z",
    "created_at": "2020-05-04T15:44:44.914Z",
    "status": "open"
  },
  {
    "id": "7d6e519729e67e8fef882f52f65b22af8e1143212490d3093ec1565f6b342a42",
    "maker": "LTC",
    "maker_size": "2.132987",
    "taker": "BLOCK",
    "taker_size": "96.933093",
    "updated_at": "2020-05-04T15:41:46.403Z",
    "created_at": "2020-05-04T15:37:45.212Z",
    "status": "open"
  },
  {
    "id": "ddacc7645c5978df6b8cfe3094f3495b7a2328d8f09071a7d33b97f68c0c1d45",
    "maker": "LTC",
    "maker_size": "0.083772",
    "taker": "BLOCK",
    "taker_size": "3.893242",
    "updated_at": "2020-05-04T15:40:42.534Z",
    "created_at": "2020-05-04T15:23:48.507Z",
    "status": "open"
  },
  {
    "id": "989dde11007bfdb8baf9496f69a083d2d8a731e2d85e2ce370e80de9d9a37149",
    "maker": "LTC",
    "maker_size": "0.149011",
    "taker": "BLOCK",
    "taker_size": "6.855176",
    "updated_at": "2020-05-04T15:45:13.101Z",
    "created_at": "2020-05-04T15:45:12.929Z",
    "status": "open"
  },
  {
    "id": "fe9277e57b3ca8475c7d6d2c51fd9ee2db7c7e97c8f4ccf4be05478149983465",
    "maker": "LTC",
    "maker_size": "0.406337",
    "taker": "BLOCK",
    "taker_size": "18.423713",
    "updated_at": "2020-05-04T15:45:15.242Z",
    "created_at": "2020-05-04T15:45:15.139Z",
    "status": "open"
  },
  {
    "id": "140bca3b75e1602853831581c0c51ee3345d1ad4bd12832abfa233028e4d4d70",
    "maker": "LTC",
    "maker_size": "15.053574",
    "taker": "BLOCK",
    "taker_size": "687.283882",
    "updated_at": "2020-05-04T15:45:16.907Z",
    "created_at": "2020-05-04T15:24:05.023Z",
    "status": "open"
  },
  {
    "id": "67428db662cfabfe984fcea34f520e06043db2ab57d222cbe5e5055cf3c3d783",
    "maker": "LTC",
    "maker_size": "4.948291",
    "taker": "BLOCK",
    "taker_size": "232.786828",
    "updated_at": "2020-05-04T15:44:46.429Z",
    "created_at": "2020-05-04T15:23:40.913Z",
    "status": "open"
  },
  {
    "id": "7b65fe5555f61b4b3d5b9d7a3b9b5d01028d830a5cecb858b61b0d7c818db689",
    "maker": "LTC",
    "maker_size": "0.135029",
    "taker": "BLOCK",
    "taker_size": "6.122466",
    "updated_at": "2020-05-04T15:45:35.526Z",
    "created_at": "2020-05-04T15:45:35.401Z",
    "status": "open"
  },
  {
    "id": "9188627478b2f377eefbb0a6f8652913ffd5105cf0cae244b39652f04cf6af8c",
    "maker": "LTC",
    "maker_size": "0.081273",
    "taker": "BLOCK",
    "taker_size": "3.814831",
    "updated_at": "2020-05-04T15:44:25.939Z",
    "created_at": "2020-05-04T15:27:27.331Z",
    "status": "open"
  },
  {
    "id": "5aba4f4c883abe972c1c6859bf888d45dd59a5777845cd17ee2562f4fb3eef91",
    "maker": "LTC",
    "maker_size": "0.347352",
    "taker": "BLOCK",
    "taker_size": "15.979723",
    "updated_at": "2020-05-04T15:44:56.537Z",
    "created_at": "2020-05-04T15:44:56.353Z",
    "status": "open"
  },
  {
    "id": "56b4fb5f32baefbe7ea9cd102b9d7150720e915231269a51e142f0876e723ec5",
    "maker": "LTC",
    "maker_size": "0.149011",
    "taker": "BLOCK",
    "taker_size": "7.954851",
    "updated_at": "2020-05-04T15:45:23.762Z",
    "created_at": "2020-05-04T15:45:23.595Z",
    "status": "open"
  },
  {
    "id": "5f1bac389d8e9ca86dce78f6af07f8f406cba727b305860785e91c427bd9a4ca",
    "maker": "LTC",
    "maker_size": "0.226611",
    "taker": "BLOCK",
    "taker_size": "10.428212",
    "updated_at": "2020-05-04T15:43:25.840Z",
    "created_at": "2020-05-04T15:22:37.444Z",
    "status": "open"
  },
  {
    "id": "192e18c375d7cc8b0518c03c4ddddf07ff6ea54a1eeb799cfc441e2b5aef07cf",
    "maker": "LTC",
    "maker_size": "0.098907",
    "taker": "BLOCK",
    "taker_size": "5.075051",
    "updated_at": "2020-05-04T15:42:27.258Z",
    "created_at": "2020-05-04T15:25:36.209Z",
    "status": "open"
  },
  {
    "id": "5241220bc66429915c39fb170f7c1630817a5a3be1eda66a4c685603ea0bf9d4",
    "maker": "LTC",
    "maker_size": "0.050220",
    "taker": "BLOCK",
    "taker_size": "2.310417",
    "updated_at": "2020-05-04T15:45:56.108Z",
    "created_at": "2020-05-04T15:45:55.935Z",
    "status": "open"
  },
  {
    "id": "3259ec76aecb713f1be68b4446967a3dd43b54b51063957f8a163d8485ca34d5",
    "maker": "LTC",
    "maker_size": "0.421840",
    "taker": "BLOCK",
    "taker_size": "19.127223",
    "updated_at": "2020-05-04T15:45:55.377Z",
    "created_at": "2020-05-04T15:45:55.252Z",
    "status": "open"
  },
  {
    "id": "e97eafc4385b862bdf02cfcb7a6d957966044e9766136c29d35e6db389c9b7dc",
    "maker": "LTC",
    "maker_size": "0.309805",
    "taker": "BLOCK",
    "taker_size": "15.584815",
    "updated_at": "2020-05-04T15:42:12.638Z",
    "created_at": "2020-05-04T15:25:14.578Z",
    "status": "open"
  },
  {
    "id": "7c9c507a1dfea893ccfecfa752a2cf33cc991d86907db9d196b383d9bc5dcfe6",
    "maker": "LTC",
    "maker_size": "0.435468",
    "taker": "BLOCK",
    "taker_size": "22.791337",
    "updated_at": "2020-05-04T15:42:57.246Z",
    "created_at": "2020-05-04T15:25:58.517Z",
    "status": "open"
  },
  {
    "id": "d464efee9750a60551477ebf7e321ab196a3f791a6e7c773cf3c4c1baa4113e9",
    "maker": "LTC",
    "maker_size": "0.284726",
    "taker": "BLOCK",
    "taker_size": "13.767022",
    "updated_at": "2020-05-04T15:45:42.598Z",
    "created_at": "2020-05-04T15:24:31.812Z",
    "status": "open"
  },
  {
    "id": "31b3fdc34966a1c564ed308532c7264b437f3171b8ca453c21a69794a7a068ed",
    "maker": "LTC",
    "maker_size": "0.072787",
    "taker": "BLOCK",
    "taker_size": "3.348595",
    "updated_at": "2020-05-04T15:45:37.252Z",
    "created_at": "2020-05-04T15:45:37.025Z",
    "status": "open"
  },
  {
    "id": "735dd28656f19bdf99234aeb5f07c263dc09f0daa5245f5abd2ca03954a50afb",
    "maker": "LTC",
    "maker_size": "0.200041",
    "taker": "BLOCK",
    "taker_size": "9.070019",
    "updated_at": "2020-05-04T15:44:27.468Z",
    "created_at": "2020-05-04T15:44:27.365Z",
    "status": "open"
  }
]
```

```plaintext
{
    "reply": [
        {
            "id": "21aaf5f3faf84e4304ebcb409e4291c3868b2351e31948caf38469fc88c83b01",
            "maker": "LTC",
            "maker_size": "0.220891",
            "taker": "BLOCK",
            "taker_size": "12.268518",
            "updated_at": "2020-05-04T15:51:27.248Z",
            "created_at": "2020-05-04T15:47:16.626Z",
            "status": "open"
        },
        {
            "id": "7f4581e5aaba4d3e63a024e4c9a453f45c85bf23734396b657172161133ae704",
            "maker": "LTC",
            "maker_size": "0.050220",
            "taker": "BLOCK",
            "taker_size": "2.734580",
            "updated_at": "2020-05-04T15:50:12.555Z",
            "created_at": "2020-05-04T15:46:06.757Z",
            "status": "open"
        },
        {
            "id": "4f42254e1db0c784e06967282ff0fa4fa90d654c7e83120feabf1ae2e80b540d",
            "maker": "LTC",
            "maker_size": "1.000755",
            "taker": "BLOCK",
            "taker_size": "52.950000",
            "updated_at": "2020-05-04T15:48:09.345Z",
            "created_at": "2020-05-03T10:28:42.989Z",
            "status": "open"
        },
        {
            "id": "bb40cbf13e29d6b89f0d8ba342496c84ca34a925c3c5181d21a23a7b59f3591a",
            "maker": "LTC",
            "maker_size": "0.387345",
            "taker": "BLOCK",
            "taker_size": "19.103415",
            "updated_at": "2020-05-04T15:45:57.212Z",
            "created_at": "2020-05-04T15:24:53.221Z",
            "status": "open"
        },
        {
            "id": "67647c4d6417b8e5ca56cd0a9ce4751c3565888c9c3904be6ef03e568abbff1e",
            "maker": "LTC",
            "maker_size": "0.392765",
            "taker": "BLOCK",
            "taker_size": "18.049067",
            "updated_at": "2020-05-04T15:47:39.321Z",
            "created_at": "2020-05-04T15:47:39.153Z",
            "status": "open"
        },
        {
            "id": "39afe532a992f628ef5907d94b15fd81af49acdb00d3239e209c3781a482801f",
            "maker": "LTC",
            "maker_size": "0.061159",
            "taker": "BLOCK",
            "taker_size": "2.769477",
            "updated_at": "2020-05-04T15:47:50.418Z",
            "created_at": "2020-05-04T15:47:50.289Z",
            "status": "open"
        },
        {
            "id": "7577ce8ed9b0d162990156433562e070cc51411fad774cffb25c461c3254ee22",
            "maker": "LTC",
            "maker_size": "0.262233",
            "taker": "BLOCK",
            "taker_size": "12.043697",
            "updated_at": "2020-05-04T15:48:13.192Z",
            "created_at": "2020-05-04T15:48:13.037Z",
            "status": "open"
        },
        {
            "id": "6c25765dffabc8bc85263d29af75f6ea4153659652e9de22889a515961133c2c",
            "maker": "LTC",
            "maker_size": "0.133985",
            "taker": "BLOCK",
            "taker_size": "7.897157",
            "updated_at": "2020-05-04T15:49:15.259Z",
            "created_at": "2020-05-04T15:49:15.098Z",
            "status": "open"
        },
        {
            "id": "bfdc451d9955158e39eab9edcc00e84f42ec156112b52a00c051d000b898782f",
            "maker": "LTC",
            "maker_size": "0.313030",
            "taker": "BLOCK",
            "taker_size": "14.159970",
            "updated_at": "2020-05-04T15:51:48.524Z",
            "created_at": "2020-05-04T15:51:48.323Z",
            "status": "open"
        },
        {
            "id": "be522dfea5a0163f23202f404191ce3e41886fb7d03b0516db2f8bde3afb5931",
            "maker": "LTC",
            "maker_size": "0.153750",
            "taker": "BLOCK",
            "taker_size": "8.710225",
            "updated_at": "2020-05-04T15:48:29.966Z",
            "created_at": "2020-05-04T15:48:29.807Z",
            "status": "open"
        },
        {
            "id": "726534966e0ef056d2df6836a5e9f72bf8dde3fb1e6274187079c44ca11f2232",
            "maker": "LTC",
            "maker_size": "0.218013",
            "taker": "BLOCK",
            "taker_size": "13.106814",
            "updated_at": "2020-05-04T15:51:23.465Z",
            "created_at": "2020-05-04T15:51:23.294Z",
            "status": "open"
        },
        {
            "id": "99a2a8a2a1cee58b3c16c0579f420a9e833fb2c389bc20ae2b4036cbacd8ec33",
            "maker": "LTC",
            "maker_size": "0.474693",
            "taker": "BLOCK",
            "taker_size": "21.787041",
            "updated_at": "2020-05-04T15:51:51.211Z",
            "created_at": "2020-05-04T15:51:51.062Z",
            "status": "open"
        },
        {
            "id": "91d4997f60905d37e75b2a029b774d4e5d33e8bc00f8aa5f651bf0fb0116073b",
            "maker": "LTC",
            "maker_size": "0.389390",
            "taker": "BLOCK",
            "taker_size": "17.895948",
            "updated_at": "2020-05-04T15:47:27.880Z",
            "created_at": "2020-05-04T15:47:27.716Z",
            "status": "open"
        },
        {
            "id": "2c4a218aebc2bb5327e7a671cd4b0a50aa7ae10ad6d08c49aad45b69e5e5783c",
            "maker": "LTC",
            "maker_size": "0.068173",
            "taker": "BLOCK",
            "taker_size": "3.128912",
            "updated_at": "2020-05-04T15:51:34.514Z",
            "created_at": "2020-05-04T15:51:34.350Z",
            "status": "open"
        },
        {
            "id": "4349b825cfc072c8cdcd6caa8b4e7e9d563c1f33b4f51de2126a7ea94df0dc41",
            "maker": "LTC",
            "maker_size": "0.352476",
            "taker": "BLOCK",
            "taker_size": "15.953575",
            "updated_at": "2020-05-04T15:48:52.093Z",
            "created_at": "2020-05-04T15:48:51.949Z",
            "status": "open"
        },
        {
            "id": "7d6e519729e67e8fef882f52f65b22af8e1143212490d3093ec1565f6b342a42",
            "maker": "LTC",
            "maker_size": "2.132987",
            "taker": "BLOCK",
            "taker_size": "96.933093",
            "updated_at": "2020-05-04T15:50:16.433Z",
            "created_at": "2020-05-04T15:37:45.212Z",
            "status": "open"
        },
        {
            "id": "d35971f3ed4b24d6124046b35138bd2f500cbd715c89343c27ccd3be5d02514b",
            "maker": "LTC",
            "maker_size": "0.170343",
            "taker": "BLOCK",
            "taker_size": "10.040119",
            "updated_at": "2020-05-04T15:50:24.939Z",
            "created_at": "2020-05-04T15:50:24.753Z",
            "status": "open"
        },
        {
            "id": "3d2b9486fb587eeb7b707aa437dd49b7808d73997dc3e5b35d4e83a0e39e774b",
            "maker": "LTC",
            "maker_size": "0.153427",
            "taker": "BLOCK",
            "taker_size": "6.956529",
            "updated_at": "2020-05-04T15:46:32.873Z",
            "created_at": "2020-05-04T15:46:32.669Z",
            "status": "open"
        },
        {
            "id": "d9a82eb0d7135049266919b3179a97410ff09eb67b382a44ae07205874a68750",
            "maker": "LTC",
            "maker_size": "0.195742",
            "taker": "BLOCK",
            "taker_size": "8.857527",
            "updated_at": "2020-05-04T15:49:16.228Z",
            "created_at": "2020-05-04T15:49:16.085Z",
            "status": "open"
        },
        {
            "id": "1769fa1eee484e79c7707d81fa30df57efe3f5fc329878fbf9a5ed2d0fcba25a",
            "maker": "LTC",
            "maker_size": "0.116339",
            "taker": "BLOCK",
            "taker_size": "6.722638",
            "updated_at": "2020-05-04T15:48:52.642Z",
            "created_at": "2020-05-04T15:48:52.480Z",
            "status": "open"
        },
        {
            "id": "88fb8ac00a3859f2c33b2537e3e0f5d28740c5e06656ab2a6208bb681d45e45f",
            "maker": "LTC",
            "maker_size": "0.080857",
            "taker": "BLOCK",
            "taker_size": "3.657448",
            "updated_at": "2020-05-04T15:51:11.157Z",
            "created_at": "2020-05-04T15:51:11.000Z",
            "status": "open"
        },
        {
            "id": "0c53e981276ea47468bbaa44beed0114cf0a3d68a179ca16c1ce2d9598c99f60",
            "maker": "LTC",
            "maker_size": "0.171180",
            "taker": "BLOCK",
            "taker_size": "7.744759",
            "updated_at": "2020-05-04T15:49:27.857Z",
            "created_at": "2020-05-04T15:49:27.716Z",
            "status": "open"
        },
        {
            "id": "a38704212ba996780a06b947aff8462b2a9c210e1a27711e9904c2ef25f1cd61",
            "maker": "LTC",
            "maker_size": "0.116339",
            "taker": "BLOCK",
            "taker_size": "5.342740",
            "updated_at": "2020-05-04T15:48:47.263Z",
            "created_at": "2020-05-04T15:48:47.135Z",
            "status": "open"
        },
        {
            "id": "97a7e232d0c030540e443786685a71d6c621ecf49018c70c138182ebc8205768",
            "maker": "LTC",
            "maker_size": "0.456676",
            "taker": "BLOCK",
            "taker_size": "20.687307",
            "updated_at": "2020-05-04T15:47:25.598Z",
            "created_at": "2020-05-04T15:47:25.365Z",
            "status": "open"
        },
        {
            "id": "140bca3b75e1602853831581c0c51ee3345d1ad4bd12832abfa233028e4d4d70",
            "maker": "LTC",
            "maker_size": "15.053574",
            "taker": "BLOCK",
            "taker_size": "687.283882",
            "updated_at": "2020-05-04T15:49:32.214Z",
            "created_at": "2020-05-04T15:24:05.023Z",
            "status": "open"
        },
        {
            "id": "3a3ac19bb685c046850468fffb1edb1db5f088d70e8047a3c9e17b4fd841c37a",
            "maker": "LTC",
            "maker_size": "0.333108",
            "taker": "BLOCK",
            "taker_size": "15.081029",
            "updated_at": "2020-05-04T15:48:02.953Z",
            "created_at": "2020-05-04T15:48:02.767Z",
            "status": "open"
        },
        {
            "id": "2f27d82013715cc56509c91858806b66ab4791b5f0091914a21fd92011dffe7a",
            "maker": "LTC",
            "maker_size": "0.068173",
            "taker": "BLOCK",
            "taker_size": "4.180491",
            "updated_at": "2020-05-04T15:51:39.796Z",
            "created_at": "2020-05-04T15:51:39.610Z",
            "status": "open"
        },
        {
            "id": "ed3d2930e31e5a9d01da4b32e670d5a1492cbfe26d0691cc2ef0a4ccd1e1e47d",
            "maker": "LTC",
            "maker_size": "0.222040",
            "taker": "BLOCK",
            "taker_size": "10.049965",
            "updated_at": "2020-05-04T15:48:40.042Z",
            "created_at": "2020-05-04T15:48:39.935Z",
            "status": "open"
        },
        {
            "id": "675baeb11e730b47eb022db8a7f38d3aae9a3fc4fded1dc671119c1c0ed8f27e",
            "maker": "LTC",
            "maker_size": "0.279635",
            "taker": "BLOCK",
            "taker_size": "12.678921",
            "updated_at": "2020-05-04T15:46:50.395Z",
            "created_at": "2020-05-04T15:46:50.160Z",
            "status": "open"
        },
        {
            "id": "67428db662cfabfe984fcea34f520e06043db2ab57d222cbe5e5055cf3c3d783",
            "maker": "LTC",
            "maker_size": "4.948291",
            "taker": "BLOCK",
            "taker_size": "232.786828",
            "updated_at": "2020-05-04T15:49:01.153Z",
            "created_at": "2020-05-04T15:23:40.913Z",
            "status": "open"
        },
        {
            "id": "4c54c2b0d920ce804df48d3fac1187ecf7ed9528cfd2bb68ff294930cd18398c",
            "maker": "LTC",
            "maker_size": "0.133985",
            "taker": "BLOCK",
            "taker_size": "6.151777",
            "updated_at": "2020-05-04T15:49:09.953Z",
            "created_at": "2020-05-04T15:49:09.775Z",
            "status": "open"
        },
        {
            "id": "9188627478b2f377eefbb0a6f8652913ffd5105cf0cae244b39652f04cf6af8c",
            "maker": "LTC",
            "maker_size": "0.081273",
            "taker": "BLOCK",
            "taker_size": "3.814831",
            "updated_at": "2020-05-04T15:48:41.070Z",
            "created_at": "2020-05-04T15:27:27.331Z",
            "status": "open"
        },
        {
            "id": "a7a5754b39f155c895db3b32a053beb90bde9762fa15f70797e71095fc5dc79c",
            "maker": "LTC",
            "maker_size": "0.262558",
            "taker": "BLOCK",
            "taker_size": "11.904244",
            "updated_at": "2020-05-04T15:47:07.924Z",
            "created_at": "2020-05-04T15:47:07.783Z",
            "status": "open"
        },
        {
            "id": "af1852f9014d3ed6319cfaf12cd91795001d8a022bf4ca88b561583f7648aa9d",
            "maker": "LTC",
            "maker_size": "0.422751",
            "taker": "BLOCK",
            "taker_size": "19.148705",
            "updated_at": "2020-05-04T15:47:37.946Z",
            "created_at": "2020-05-04T15:47:37.840Z",
            "status": "open"
        },
        {
            "id": "476deb7c6d4c1bf5afbb6c16ee26e85bed64bccced0655e9f33cee19fa98daa9",
            "maker": "LTC",
            "maker_size": "0.457708",
            "taker": "BLOCK",
            "taker_size": "20.753621",
            "updated_at": "2020-05-04T15:46:15.401Z",
            "created_at": "2020-05-04T15:46:15.126Z",
            "status": "open"
        },
        {
            "id": "66ebc451336358770c3860d905ffbe52758402c9b47733b6d9915c0fb84256b3",
            "maker": "LTC",
            "maker_size": "0.458761",
            "taker": "BLOCK",
            "taker_size": "21.062079",
            "updated_at": "2020-05-04T15:49:32.621Z",
            "created_at": "2020-05-04T15:49:32.421Z",
            "status": "open"
        },
        {
            "id": "18f129f53e0e412fcce338de496601a29d1065141c4a6677c3e8fee87233f3b7",
            "maker": "LTC",
            "maker_size": "0.348467",
            "taker": "BLOCK",
            "taker_size": "16.031048",
            "updated_at": "2020-05-04T15:46:32.033Z",
            "created_at": "2020-05-04T15:46:31.861Z",
            "status": "open"
        },
        {
            "id": "15e0d9c68ada3fecc42602addfc24d292d8d36075b924dc4398bef5d02fe58bc",
            "maker": "LTC",
            "maker_size": "0.355121",
            "taker": "BLOCK",
            "taker_size": "16.312952",
            "updated_at": "2020-05-04T15:48:01.902Z",
            "created_at": "2020-05-04T15:48:01.742Z",
            "status": "open"
        },
        {
            "id": "5347f0d20827719978781fd76a39e831b0bcc23cfe345f6b8238770f23e93cbd",
            "maker": "LTC",
            "maker_size": "0.463113",
            "taker": "BLOCK",
            "taker_size": "20.948413",
            "updated_at": "2020-05-04T15:51:23.817Z",
            "created_at": "2020-05-04T15:51:23.697Z",
            "status": "open"
        },
        {
            "id": "02f3eff7bbb4fffe4e3a05fada0f03a493c3c1948f0e85e74462ba96adf82bc3",
            "maker": "LTC",
            "maker_size": "0.259116",
            "taker": "BLOCK",
            "taker_size": "11.728416",
            "updated_at": "2020-05-04T15:48:27.623Z",
            "created_at": "2020-05-04T15:48:27.489Z",
            "status": "open"
        },
        {
            "id": "56b4fb5f32baefbe7ea9cd102b9d7150720e915231269a51e142f0876e723ec5",
            "maker": "LTC",
            "maker_size": "0.149011",
            "taker": "BLOCK",
            "taker_size": "7.954851",
            "updated_at": "2020-05-04T15:49:27.265Z",
            "created_at": "2020-05-04T15:45:23.595Z",
            "status": "open"
        },
        {
            "id": "ca90b8c54c983f0ffbf1aa1a9e90fd719984dfc91a6a244c9b48f2f7372c95c6",
            "maker": "LTC",
            "maker_size": "0.360464",
            "taker": "BLOCK",
            "taker_size": "16.561845",
            "updated_at": "2020-05-04T15:47:50.625Z",
            "created_at": "2020-05-04T15:47:50.465Z",
            "status": "open"
        },
        {
            "id": "5f1bac389d8e9ca86dce78f6af07f8f406cba727b305860785e91c427bd9a4ca",
            "maker": "LTC",
            "maker_size": "0.226611",
            "taker": "BLOCK",
            "taker_size": "10.428212",
            "updated_at": "2020-05-04T15:51:55.839Z",
            "created_at": "2020-05-04T15:22:37.444Z",
            "status": "open"
        },
        {
            "id": "192e18c375d7cc8b0518c03c4ddddf07ff6ea54a1eeb799cfc441e2b5aef07cf",
            "maker": "LTC",
            "maker_size": "0.098907",
            "taker": "BLOCK",
            "taker_size": "5.075051",
            "updated_at": "2020-05-04T15:46:42.605Z",
            "created_at": "2020-05-04T15:25:36.209Z",
            "status": "open"
        },
        {
            "id": "5241220bc66429915c39fb170f7c1630817a5a3be1eda66a4c685603ea0bf9d4",
            "maker": "LTC",
            "maker_size": "0.050220",
            "taker": "BLOCK",
            "taker_size": "2.310417",
            "updated_at": "2020-05-04T15:45:56.107Z",
            "created_at": "2020-05-04T15:45:55.935Z",
            "status": "open"
        },
        {
            "id": "3259ec76aecb713f1be68b4446967a3dd43b54b51063957f8a163d8485ca34d5",
            "maker": "LTC",
            "maker_size": "0.421840",
            "taker": "BLOCK",
            "taker_size": "19.127223",
            "updated_at": "2020-05-04T15:45:55.391Z",
            "created_at": "2020-05-04T15:45:55.252Z",
            "status": "open"
        },
        {
            "id": "4e231e93e7b2bc9d37bc39623850332167c858095a7f14540f89251c0c8dcad6",
            "maker": "LTC",
            "maker_size": "0.337366",
            "taker": "BLOCK",
            "taker_size": "15.486375",
            "updated_at": "2020-05-04T15:49:43.806Z",
            "created_at": "2020-05-04T15:49:43.640Z",
            "status": "open"
        },
        {
            "id": "6d3c5d848b75843fe00c9cd27de4abedcd2f0d8a377ae97bf61a2cb3872851d8",
            "maker": "LTC",
            "maker_size": "0.153750",
            "taker": "BLOCK",
            "taker_size": "7.061084",
            "updated_at": "2020-05-04T15:48:24.657Z",
            "created_at": "2020-05-04T15:48:24.495Z",
            "status": "open"
        },
        {
            "id": "e97eafc4385b862bdf02cfcb7a6d957966044e9766136c29d35e6db389c9b7dc",
            "maker": "LTC",
            "maker_size": "0.309805",
            "taker": "BLOCK",
            "taker_size": "15.584815",
            "updated_at": "2020-05-04T15:46:27.304Z",
            "created_at": "2020-05-04T15:25:14.578Z",
            "status": "open"
        },
        {
            "id": "54b8844550f6312441ee06ccac64e740b9ca06046d281da6c8ec7720dab777dd",
            "maker": "LTC",
            "maker_size": "0.495970",
            "taker": "BLOCK",
            "taker_size": "22.443509",
            "updated_at": "2020-05-04T15:49:03.916Z",
            "created_at": "2020-05-04T15:49:03.746Z",
            "status": "open"
        },
        {
            "id": "8b32cdd927fd4e0aca092bb3650c9ec72e05a51d129812d634158ca4f54e39de",
            "maker": "LTC",
            "maker_size": "0.441358",
            "taker": "BLOCK",
            "taker_size": "19.968014",
            "updated_at": "2020-05-04T15:49:40.250Z",
            "created_at": "2020-05-04T15:49:40.095Z",
            "status": "open"
        },
        {
            "id": "76d17779c2c2d9336edc5760894a7274f39a2c1233df43139107909581b937e0",
            "maker": "LTC",
            "maker_size": "0.242196",
            "taker": "BLOCK",
            "taker_size": "10.955678",
            "updated_at": "2020-05-04T15:51:36.229Z",
            "created_at": "2020-05-04T15:51:36.124Z",
            "status": "open"
        },
        {
            "id": "7c9c507a1dfea893ccfecfa752a2cf33cc991d86907db9d196b383d9bc5dcfe6",
            "maker": "LTC",
            "maker_size": "0.435468",
            "taker": "BLOCK",
            "taker_size": "22.791337",
            "updated_at": "2020-05-04T15:47:12.559Z",
            "created_at": "2020-05-04T15:25:58.517Z",
            "status": "open"
        },
        {
            "id": "e7821678cae7ada3d199314f9d360dee180cf86513da509778c10ab37ab016f0",
            "maker": "LTC",
            "maker_size": "0.218013",
            "taker": "BLOCK",
            "taker_size": "10.005822",
            "updated_at": "2020-05-04T15:51:18.310Z",
            "created_at": "2020-05-04T15:51:17.975Z",
            "status": "open"
        },
        {
            "id": "0c69b1df4e83141b1888306caaeb8f51de98217228647bb3d5e87666881130f6",
            "maker": "LTC",
            "maker_size": "0.269176",
            "taker": "BLOCK",
            "taker_size": "12.184265",
            "updated_at": "2020-05-04T15:48:15.151Z",
            "created_at": "2020-05-04T15:48:15.052Z",
            "status": "open"
        }
    ],
    "uuid": "582c52c4-f2e4-4f15-8d5d-412da0b52c98"
}
```

Parameter     | Type          | Description
--------------|---------------|-------------
id            | string        | Order ID.
maker         | string        | Maker trading asset; the ticker of the asset being sold by the maker.
maker_size    | int           | Total maker amount.
taker         | string        | Taker trading asset; the ticker of the asset being sold by the taker.
taker_size    | int           | Total taker amount.
updated_at    | string        | Last updated time stamp.
created_at    | string        | Order creation time stamp.
status        | string        | Order status.
uuid          | string        | The response ID, which can be used to view this response again with [xrGetReply](https://api.blocknet.co/#xrgetreply).
