# Crypto Information

Call                                                      | Description
----------------------------------------------------------|---------------------------------
[CCMultiPrice](#ccmultiprice)                             | Returns the current price of any given crypto currency ticker(s) in the desired currency(s).
[CCSinglePrice](#ccsingleprice)                           | Returns the current price of any given cryptocurrency ticker in the desired currency(s).
[CCTopExchangesVolumeByPair](#cctopexchangesvolumebypair) | Returns the top list exchanges based on volume by pair.
[CCTopListMarketCap](#cctoplistmarketcap)                 | Returns the top list by market cap.
[CCTopListVolume24H](#cctoplistvolume24h)                 | Returns the top list of 24 hour volume.
[CCTopListVolumeByPair](#cctoplistvolumebypair)           | Returns the top list of volume by pair.



## CCMultiPrice

> Sample Data

```cli
{
  "tickers": "BTC,DASH",
  "currencies": "USD,CAD"
}
```
Returns the current price of any given crypto currency ticker(s) in the desired currency(s). Pricing information provided by Crypto Compare.



### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '["BTC,DASH","USD,CAD"]' https://api.maplenodes.com/v1/CCMultiPrice
```

<code class="api-call">CCMultiPrice [tickers] [currencies]</code>

Parameter       | Type       | Description
----------------|------------|-------------
tickers         | string     | Crypto currency tickers joined by commas.
currencies      | string     | World currencies joined by commas.


### Response Parameters

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
{
  "BTC": {
    "USD": 8853.22,
    "CAD": 12599.3
  },
  "DASH": {
    "USD": 79.71,
    "CAD": 112.17
  }
}
```

Parameter      | Type          | Description
---------------|---------------|-------------
crypto_ticker  | string        | Crypto currency ticker.
currencies     | int           | Current pricing of crypto ticker in desired currency.





## CCSinglePrice

> Sample Data

```cli
{
  "ticker": "BTC",
  "currencies": "USD,CAD"
}
```
Returns the current price of any given cryptocurrency ticker in the desired currency(s). Pricing information provided by Crypto Compare.



### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '["BTC","USD,CAD"]' https://api.maplenodes.com/v1/CCSinglePrice
```

<code class="api-call">CCSinglePrice [ticker] [currencies]</code>

Parameter       | Type       | Description
----------------|------------|-------------
ticker          | string     | Crypto currency ticker.
currencies      | string     | World currencies joined by commas.


### Response Parameters

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
{
  "USD": 8857.56,
  "CAD": 12599.3
}
```

Parameter      | Type          | Description
---------------|---------------|-------------
currencies     | int           | Current pricing of crypto ticker in desired currencies.





## CCTopExchangesVolumeByPair

> Sample Data

```cli
{
  "ticker": "BTC",
  "currency": "USD"
}
```
Returns the top list exchanges based on volume by pair. Pricing information provided by Crypto Compare.



### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '["BTC","USD"]' https://api.maplenodes.com/v1/CCTopExchangesVolumeByPair
```

<code class="api-call">CCTopExchangesVolumeByPair [ticker] [currency]</code>

Parameter       | Type       | Description
----------------|------------|-------------
ticker          | string     | Crypto currency ticker.
currency        | string     | World currency.


### Response Parameters

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
{
  "Response": "Success",
  "Data": [
    {
      "exchange": "Coinsbit",
      "fromSymbol": "BTC",
      "toSymbol": "USD",
      "volume24h": 69323.89512443,
      "volume24hTo": 604919028.448395
    },
    {
      "exchange": "P2PB2B",
      "fromSymbol": "BTC",
      "toSymbol": "USD",
      "volume24h": 61164.896717,
      "volume24hTo": 537775810.031167
    },
    {
      "exchange": "bitasset",
      "fromSymbol": "BTC",
      "toSymbol": "USD",
      "volume24h": 18223.9468,
      "volume24hTo": 161003439.435717
    },
    {
      "exchange": "Coinbase",
      "fromSymbol": "BTC",
      "toSymbol": "USD",
      "volume24h": 15626.50845041,
      "volume24hTo": 136869331.37539
    },
    {
      "exchange": "lmax",
      "fromSymbol": "BTC",
      "toSymbol": "USD",
      "volume24h": 9524.03,
      "volume24hTo": 83341039.57487
    }
  ],
  "RateLimit": {},
  "HasWarning": false,
  "Type": 100
}
```

Parameter      | Type          | Description
---------------|---------------|-------------
Response       | string        | Status of call.
Data           | array         | Array of exchanges and corresponding data.
exchange       | string        | Crypto exchange.
fromSymbol     | string        | From asset ticker.
toSymbol       | string        | To asset ticker.
volume24h      | int           | 24 hour volume.
volume24hTo    | int           | 24 hour volume To.
RateLimit      | string        | Rate limit.
HasWarning     | bool          | If no warnings `false`, otherwise `true`.
Type           | int           | Type.





## CCTopListMarketCap

> Sample Data

```cli
{
  "limit": "10",
  "currency": "USD"
}
```
Returns the top list by market cap. Pricing information provided by Crypto Compare.



### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '["10","USD"]' https://api.maplenodes.com/v1/CCTopListMarketCap
```

<code class="api-call">CCTopListMarketCap [limit] [currency]</code>

Parameter       | Type       | Description
----------------|------------|-------------
limit           | int        | Number of assets to return in toplist (10-100)
currency        | string     | World currency.


### Response Parameters

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
{
  "Message": "Success",
  "Type": 100,
  "SponsoredData": [],
  "Data": [
    {
      "CoinInfo": {
        "Id": "1182",
        "Name": "BTC",
        "FullName": "Bitcoin",
        "Internal": "BTC",
        "ImageUrl": "/media/19633/btc.png",
        "Url": "/coins/btc/overview",
        "Algorithm": "SHA-256",
        "ProofType": "PoW",
        "Rating": {
          "Weiss": {
            "Rating": "B+",
            "TechnologyAdoptionRating": "A",
            "MarketPerformanceRating": "D"
          }
        },
        "NetHashesPerSecond": 114238226202.791,
        "BlockNumber": 628908,
        "BlockTime": 600,
        "BlockReward": 12.5,
        "Type": 1,
        "DocumentType": "Webpagecoinp"
      },
      "RAW": {
        "USD": {
          "TYPE": "5",
          "MARKET": "CCCAGG",
          "FROMSYMBOL": "BTC",
          "TOSYMBOL": "USD",
          "FLAGS": "2049",
          "PRICE": 8890.31,
          "LASTUPDATE": 1588608036,
          "MEDIAN": 8874.61,
          "LASTVOLUME": 0.005,
          "LASTVOLUMETO": 44.421499999999995,
          "LASTTRADEID": "442046250",
          "VOLUMEDAY": 45113.805399809666,
          "VOLUMEDAYTO": 393651326.3958163,
          "VOLUME24HOUR": 57064.9968953409,
          "VOLUME24HOURTO": 499651320.06807214,
          "OPENDAY": 8907.07,
          "HIGHDAY": 8946.95,
          "LOWDAY": 8537.49,
          "OPEN24HOUR": 8858.96,
          "HIGH24HOUR": 8967.86,
          "LOW24HOUR": 8512.93,
          "LASTMARKET": "Bitfinex",
          "VOLUMEHOUR": 407.7042508799994,
          "VOLUMEHOURTO": 3618292.537797033,
          "OPENHOUR": 8854.23,
          "HIGHHOUR": 8890.31,
          "LOWHOUR": 8854.2,
          "TOPTIERVOLUME24HOUR": 54791.59841103089,
          "TOPTIERVOLUME24HOURTO": 479711616.8877831,
          "CHANGE24HOUR": 31.350000000000364,
          "CHANGEPCT24HOUR": 0.35387901062879124,
          "CHANGEDAY": -16.76000000000022,
          "CHANGEPCTDAY": -0.18816513174366226,
          "CHANGEHOUR": 36.07999999999993,
          "CHANGEPCTHOUR": 0.40748884996210766,
          "CONVERSIONTYPE": "direct",
          "CONVERSIONSYMBOL": "",
          "SUPPLY": 18361300,
          "MKTCAP": 163237649003,
          "TOTALVOLUME24H": 645096.4287276813,
          "TOTALVOLUME24HTO": 5727433038.801447,
          "TOTALTOPTIERVOLUME24H": 413668.69280135486,
          "TOTALTOPTIERVOLUME24HTO": 3670240237.917024,
          "IMAGEURL": "/media/19633/btc.png"
        }
      },
      "DISPLAY": {
        "USD": {
          "FROMSYMBOL": "Ƀ",
          "TOSYMBOL": "$",
          "MARKET": "CryptoCompare Index",
          "PRICE": "$ 8,890.31",
          "LASTUPDATE": "Just now",
          "LASTVOLUME": "Ƀ 0.005000",
          "LASTVOLUMETO": "$ 44.42",
          "LASTTRADEID": "442046250",
          "VOLUMEDAY": "Ƀ 45,113.8",
          "VOLUMEDAYTO": "$ 393,651,326.4",
          "VOLUME24HOUR": "Ƀ 57,065.0",
          "VOLUME24HOURTO": "$ 499,651,320.1",
          "OPENDAY": "$ 8,907.07",
          "HIGHDAY": "$ 8,946.95",
          "LOWDAY": "$ 8,537.49",
          "OPEN24HOUR": "$ 8,858.96",
          "HIGH24HOUR": "$ 8,967.86",
          "LOW24HOUR": "$ 8,512.93",
          "LASTMARKET": "Bitfinex",
          "VOLUMEHOUR": "Ƀ 407.70",
          "VOLUMEHOURTO": "$ 3,618,292.5",
          "OPENHOUR": "$ 8,854.23",
          "HIGHHOUR": "$ 8,890.31",
          "LOWHOUR": "$ 8,854.20",
          "TOPTIERVOLUME24HOUR": "Ƀ 54,791.6",
          "TOPTIERVOLUME24HOURTO": "$ 479,711,616.9",
          "CHANGE24HOUR": "$ 31.35",
          "CHANGEPCT24HOUR": "0.35",
          "CHANGEDAY": "$ -16.76",
          "CHANGEPCTDAY": "-0.19",
          "CHANGEHOUR": "$ 36.08",
          "CHANGEPCTHOUR": "0.41",
          "CONVERSIONTYPE": "direct",
          "CONVERSIONSYMBOL": "",
          "SUPPLY": "Ƀ 18,361,300.0",
          "MKTCAP": "$ 163.24 B",
          "TOTALVOLUME24H": "Ƀ 645.10 K",
          "TOTALVOLUME24HTO": "$ 5.73 B",
          "TOTALTOPTIERVOLUME24H": "Ƀ 413.67 K",
          "TOTALTOPTIERVOLUME24HTO": "$ 3.67 B",
          "IMAGEURL": "/media/19633/btc.png"
        }
      }
    },
    {
      "CoinInfo": {
        "Id": "7605",
        "Name": "ETH",
        "FullName": "Ethereum",
        "Internal": "ETH",
        "ImageUrl": "/media/20646/eth_logo.png",
        "Url": "/coins/eth/overview",
        "Algorithm": "Ethash",
        "ProofType": "PoW",
        "Rating": {
          "Weiss": {
            "Rating": "B+",
            "TechnologyAdoptionRating": "A",
            "MarketPerformanceRating": "D"
          }
        },
        "NetHashesPerSecond": 179649712318722,
        "BlockNumber": 10000444,
        "BlockTime": 15,
        "BlockReward": 2,
        "Type": 1,
        "DocumentType": "Webpagecoinp"
      },
      "RAW": {
        "USD": {
          "TYPE": "5",
          "MARKET": "CCCAGG",
          "FROMSYMBOL": "ETH",
          "TOSYMBOL": "USD",
          "FLAGS": "2052",
          "PRICE": 206.79,
          "LASTUPDATE": 1588608035,
          "MEDIAN": 206.4,
          "LASTVOLUME": 0.005402,
          "LASTVOLUMETO": 1.1160531999999999,
          "LASTTRADEID": "442045389",
          "VOLUMEDAY": 468509.28080370574,
          "VOLUMEDAYTO": 94706234.8684289,
          "VOLUME24HOUR": 566783.9250802201,
          "VOLUME24HOURTO": 115244919.84331566,
          "OPENDAY": 210.06,
          "HIGHDAY": 210.81,
          "LOWDAY": 195.3,
          "OPEN24HOUR": 208.98,
          "HIGH24HOUR": 211.75,
          "LOW24HOUR": 195.09,
          "LASTMARKET": "Bitfinex",
          "VOLUMEHOUR": 1148.22746665,
          "VOLUMEHOURTO": 237197.15675253866,
          "OPENHOUR": 206.23,
          "HIGHHOUR": 206.79,
          "LOWHOUR": 206.23,
          "TOPTIERVOLUME24HOUR": 553206.20998776,
          "TOPTIERVOLUME24HOURTO": 112488631.35511072,
          "CHANGE24HOUR": -2.1899999999999977,
          "CHANGEPCT24HOUR": -1.0479471719781788,
          "CHANGEDAY": -3.2700000000000102,
          "CHANGEPCTDAY": -1.556698086261073,
          "CHANGEHOUR": 0.5600000000000023,
          "CHANGEPCTHOUR": 0.2715414828104555,
          "CONVERSIONTYPE": "direct",
          "CONVERSIONSYMBOL": "",
          "SUPPLY": 110788681.499,
          "MKTCAP": 22909991447.178207,
          "TOTALVOLUME24H": 11644040.47122921,
          "TOTALVOLUME24HTO": 2405910801.0214653,
          "TOTALTOPTIERVOLUME24H": 6091716.388962934,
          "TOTALTOPTIERVOLUME24HTO": 1257797151.2653868,
          "IMAGEURL": "/media/20646/eth_logo.png"
        }
      },
      "DISPLAY": {
        "USD": {
          "FROMSYMBOL": "Ξ",
          "TOSYMBOL": "$",
          "MARKET": "CryptoCompare Index",
          "PRICE": "$ 206.79",
          "LASTUPDATE": "Just now",
          "LASTVOLUME": "Ξ 0.005402",
          "LASTVOLUMETO": "$ 1.12",
          "LASTTRADEID": "442045389",
          "VOLUMEDAY": "Ξ 468,509.3",
          "VOLUMEDAYTO": "$ 94,706,234.9",
          "VOLUME24HOUR": "Ξ 566,783.9",
          "VOLUME24HOURTO": "$ 115,244,919.8",
          "OPENDAY": "$ 210.06",
          "HIGHDAY": "$ 210.81",
          "LOWDAY": "$ 195.30",
          "OPEN24HOUR": "$ 208.98",
          "HIGH24HOUR": "$ 211.75",
          "LOW24HOUR": "$ 195.09",
          "LASTMARKET": "Bitfinex",
          "VOLUMEHOUR": "Ξ 1,148.23",
          "VOLUMEHOURTO": "$ 237,197.2",
          "OPENHOUR": "$ 206.23",
          "HIGHHOUR": "$ 206.79",
          "LOWHOUR": "$ 206.23",
          "TOPTIERVOLUME24HOUR": "Ξ 553,206.2",
          "TOPTIERVOLUME24HOURTO": "$ 112,488,631.4",
          "CHANGE24HOUR": "$ -2.19",
          "CHANGEPCT24HOUR": "-1.05",
          "CHANGEDAY": "$ -3.27",
          "CHANGEPCTDAY": "-1.56",
          "CHANGEHOUR": "$ 0.56",
          "CHANGEPCTHOUR": "0.27",
          "CONVERSIONTYPE": "direct",
          "CONVERSIONSYMBOL": "",
          "SUPPLY": "Ξ 110,788,681.5",
          "MKTCAP": "$ 22.91 B",
          "TOTALVOLUME24H": "Ξ 11.64 M",
          "TOTALVOLUME24HTO": "$ 2.41 B",
          "TOTALTOPTIERVOLUME24H": "Ξ 6.09 M",
          "TOTALTOPTIERVOLUME24HTO": "$ 1.26 B",
          "IMAGEURL": "/media/20646/eth_logo.png"
        }
      }
    },
    {
      "CoinInfo": {
        "Id": "5031",
        "Name": "XRP",
        "FullName": "XRP",
        "Internal": "XRP",
        "ImageUrl": "/media/34477776/xrp.png",
        "Url": "/coins/xrp/overview",
        "Algorithm": "N/A",
        "ProofType": "N/A",
        "Rating": {
          "Weiss": {
            "Rating": "B-",
            "TechnologyAdoptionRating": "B+",
            "MarketPerformanceRating": "D-"
          }
        },
        "NetHashesPerSecond": 0,
        "BlockNumber": 0,
        "BlockTime": 4,
        "BlockReward": 0,
        "Type": 1,
        "DocumentType": "Webpagecoinp"
      },
      "RAW": {
        "USD": {
          "TYPE": "5",
          "MARKET": "CCCAGG",
          "FROMSYMBOL": "XRP",
          "TOSYMBOL": "USD",
          "FLAGS": "2052",
          "PRICE": 0.2191,
          "LASTUPDATE": 1588608036,
          "MEDIAN": 0.21868,
          "LASTVOLUME": 960.60564602,
          "LASTVOLUMETO": 210.0652426716536,
          "LASTTRADEID": "442042653",
          "VOLUMEDAY": 153186174.47837344,
          "VOLUMEDAYTO": 32694611.765551638,
          "VOLUME24HOUR": 188127155.31923506,
          "VOLUME24HOURTO": 40326306.276131034,
          "OPENDAY": 0.2194,
          "HIGHDAY": 0.2207,
          "LOWDAY": 0.2074,
          "OPEN24HOUR": 0.2189,
          "HIGH24HOUR": 0.2216,
          "LOW24HOUR": 0.2074,
          "LASTMARKET": "Bitfinex",
          "VOLUMEHOUR": 530380.1492834102,
          "VOLUMEHOURTO": 116114.27957505982,
          "OPENHOUR": 0.2186,
          "HIGHHOUR": 0.2191,
          "LOWHOUR": 0.2186,
          "TOPTIERVOLUME24HOUR": 188118357.02014032,
          "TOPTIERVOLUME24HOURTO": 40324447.98795003,
          "CHANGE24HOUR": 0.00019999999999997797,
          "CHANGEPCT24HOUR": 0.0913659205116391,
          "CHANGEDAY": -0.00030000000000002247,
          "CHANGEPCTDAY": -0.13673655423884343,
          "CHANGEHOUR": 0.0005000000000000004,
          "CHANGEPCTHOUR": 0.22872827081427288,
          "CONVERSIONTYPE": "direct",
          "CONVERSIONSYMBOL": "",
          "SUPPLY": 99991850794,
          "MKTCAP": 21908214508.9654,
          "TOTALVOLUME24H": 1664558551.1767914,
          "TOTALVOLUME24HTO": 363812425.10852164,
          "TOTALTOPTIERVOLUME24H": 1234616765.876044,
          "TOTALTOPTIERVOLUME24HTO": 269612249.3682785,
          "IMAGEURL": "/media/34477776/xrp.png"
        }
      },
      "DISPLAY": {
        "USD": {
          "FROMSYMBOL": "XRP",
          "TOSYMBOL": "$",
          "MARKET": "CryptoCompare Index",
          "PRICE": "$ 0.2191",
          "LASTUPDATE": "Just now",
          "LASTVOLUME": "XRP 960.61",
          "LASTVOLUMETO": "$ 210.07",
          "LASTTRADEID": "442042653",
          "VOLUMEDAY": "XRP 153,186,174.5",
          "VOLUMEDAYTO": "$ 32,694,611.8",
          "VOLUME24HOUR": "XRP 188,127,155.3",
          "VOLUME24HOURTO": "$ 40,326,306.3",
          "OPENDAY": "$ 0.2194",
          "HIGHDAY": "$ 0.2207",
          "LOWDAY": "$ 0.2074",
          "OPEN24HOUR": "$ 0.2189",
          "HIGH24HOUR": "$ 0.2216",
          "LOW24HOUR": "$ 0.2074",
          "LASTMARKET": "Bitfinex",
          "VOLUMEHOUR": "XRP 530,380.1",
          "VOLUMEHOURTO": "$ 116,114.3",
          "OPENHOUR": "$ 0.2186",
          "HIGHHOUR": "$ 0.2191",
          "LOWHOUR": "$ 0.2186",
          "TOPTIERVOLUME24HOUR": "XRP 188,118,357.0",
          "TOPTIERVOLUME24HOURTO": "$ 40,324,448.0",
          "CHANGE24HOUR": "$ 0.00020",
          "CHANGEPCT24HOUR": "0.09",
          "CHANGEDAY": "$ -0.00030",
          "CHANGEPCTDAY": "-0.14",
          "CHANGEHOUR": "$ 0.00050",
          "CHANGEPCTHOUR": "0.23",
          "CONVERSIONTYPE": "direct",
          "CONVERSIONSYMBOL": "",
          "SUPPLY": "XRP 99,991,850,794.0",
          "MKTCAP": "$ 21.91 B",
          "TOTALVOLUME24H": "XRP 1.66 B",
          "TOTALVOLUME24HTO": "$ 363.81 M",
          "TOTALTOPTIERVOLUME24H": "XRP 1.23 B",
          "TOTALTOPTIERVOLUME24HTO": "$ 269.61 M",
          "IMAGEURL": "/media/34477776/xrp.png"
        }
      }
    },
    {
      "CoinInfo": {
        "Id": "932313",
        "Name": "GAPS",
        "FullName": "Gaps Chain",
        "Internal": "GAPS",
        "ImageUrl": "/media/35651651/gaps.png",
        "Url": "/coins/gaps/overview",
        "Algorithm": "N/A",
        "ProofType": "N/A",
        "Rating": {
          "Weiss": {
            "Rating": "",
            "TechnologyAdoptionRating": "",
            "MarketPerformanceRating": ""
          }
        },
        "NetHashesPerSecond": 0,
        "BlockNumber": 0,
        "BlockTime": 0,
        "BlockReward": 0,
        "Type": 1,
        "DocumentType": "Webpagecoinp"
      },
      "RAW": {
        "USD": {
          "TYPE": "5",
          "MARKET": "CCCAGG",
          "FROMSYMBOL": "GAPS",
          "TOSYMBOL": "USD",
          "FLAGS": "2052",
          "PRICE": 3.2321277,
          "LASTUPDATE": 1588608035,
          "MEDIAN": 3.2327170515,
          "LASTVOLUME": 5.8128,
          "LASTVOLUMETO": 18.78771189456,
          "LASTTRADEID": "15886079440001",
          "VOLUMEDAY": 1275545.1058000005,
          "VOLUMEDAYTO": 4122724.669055613,
          "VOLUME24HOUR": 1649248.084,
          "VOLUME24HOURTO": 5330580.416468328,
          "OPENDAY": 3.1039179,
          "HIGHDAY": 3.4203066,
          "LOWDAY": 3.10185,
          "OPEN24HOUR": 3.2176524,
          "HIGH24HOUR": 3.4203066,
          "LOW24HOUR": 3.0997821,
          "LASTMARKET": "Bitforex",
          "VOLUMEHOUR": 0,
          "VOLUMEHOURTO": 0,
          "OPENHOUR": 3.2321277,
          "HIGHHOUR": 3.2321277,
          "LOWHOUR": 3.2321277,
          "TOPTIERVOLUME24HOUR": 0,
          "TOPTIERVOLUME24HOURTO": 0,
          "CHANGE24HOUR": 0.014475299999999969,
          "CHANGEPCT24HOUR": 0.4498714652956289,
          "CHANGEDAY": 0.12820980000000004,
          "CHANGEPCTDAY": 4.130579613590941,
          "CHANGEHOUR": 0,
          "CHANGEPCTHOUR": 0,
          "CONVERSIONTYPE": "multiply",
          "CONVERSIONSYMBOL": "ETH",
          "SUPPLY": 2000000000,
          "MKTCAP": 6464255400,
          "TOTALVOLUME24H": 1813480.218600094,
          "TOTALVOLUME24HTO": 5861399.64793942,
          "TOTALTOPTIERVOLUME24H": 0,
          "TOTALTOPTIERVOLUME24HTO": 0,
          "IMAGEURL": "/media/35651651/gaps.png"
        }
      },
      "DISPLAY": {
        "USD": {
          "FROMSYMBOL": "GAPS",
          "TOSYMBOL": "$",
          "MARKET": "CryptoCompare Index",
          "PRICE": "$ 3.23",
          "LASTUPDATE": "Just now",
          "LASTVOLUME": "GAPS 5.81",
          "LASTVOLUMETO": "$ 18.79",
          "LASTTRADEID": "15886079440001",
          "VOLUMEDAY": "GAPS 1,275,545.1",
          "VOLUMEDAYTO": "$ 4,122,724.7",
          "VOLUME24HOUR": "GAPS 1,649,248.1",
          "VOLUME24HOURTO": "$ 5,330,580.4",
          "OPENDAY": "$ 3.10",
          "HIGHDAY": "$ 3.42",
          "LOWDAY": "$ 3.10",
          "OPEN24HOUR": "$ 3.22",
          "HIGH24HOUR": "$ 3.42",
          "LOW24HOUR": "$ 3.10",
          "LASTMARKET": "Bitforex",
          "VOLUMEHOUR": "GAPS 0",
          "VOLUMEHOURTO": "$ 0",
          "OPENHOUR": "$ 3.23",
          "HIGHHOUR": "$ 3.23",
          "LOWHOUR": "$ 3.23",
          "TOPTIERVOLUME24HOUR": "GAPS 0",
          "TOPTIERVOLUME24HOURTO": "$ 0",
          "CHANGE24HOUR": "$ 0.014",
          "CHANGEPCT24HOUR": "0.45",
          "CHANGEDAY": "$ 0.13",
          "CHANGEPCTDAY": "4.13",
          "CHANGEHOUR": "$ 0.0",
          "CHANGEPCTHOUR": "0.00",
          "CONVERSIONTYPE": "multiply",
          "CONVERSIONSYMBOL": "ETH",
          "SUPPLY": "GAPS 2,000,000,000.0",
          "MKTCAP": "$ 6.46 B",
          "TOTALVOLUME24H": "GAPS 1.81 M",
          "TOTALVOLUME24HTO": "$ 5.86 M",
          "TOTALTOPTIERVOLUME24H": "GAPS 0",
          "TOTALTOPTIERVOLUME24HTO": "$ 0",
          "IMAGEURL": "/media/35651651/gaps.png"
        }
      }
    },
    {
      "CoinInfo": {
        "Id": "929418",
        "Name": "CRO",
        "FullName": "Crypto.com Chain Token",
        "Internal": "CRO",
        "ImageUrl": "/media/34478435/mco.png",
        "Url": "/coins/cro/overview",
        "Algorithm": "N/A",
        "ProofType": "N/A",
        "Rating": {
          "Weiss": {
            "Rating": "",
            "TechnologyAdoptionRating": "",
            "MarketPerformanceRating": ""
          }
        },
        "NetHashesPerSecond": 0,
        "BlockNumber": 0,
        "BlockTime": 0,
        "BlockReward": 0,
        "Type": 1,
        "DocumentType": "Webpagecoinp"
      },
      "RAW": {
        "USD": {
          "TYPE": "5",
          "MARKET": "CCCAGG",
          "FROMSYMBOL": "CRO",
          "TOSYMBOL": "USD",
          "FLAGS": "2052",
          "PRICE": 0.06072081729999999,
          "LASTUPDATE": 1588608036,
          "MEDIAN": 0.0608097204,
          "LASTVOLUME": 200,
          "LASTVOLUMETO": 12.14416346,
          "LASTTRADEID": "1.0006283043084477e+22",
          "VOLUMEDAY": 30513414.811183292,
          "VOLUMEDAYTO": 1852799.485948974,
          "VOLUME24HOUR": 43862303.02732922,
          "VOLUME24HOURTO": 2663354.888479694,
          "OPENDAY": 0.06000959249999999,
          "HIGHDAY": 0.06160984829999999,
          "LOWDAY": 0.0596539801,
          "OPEN24HOUR": 0.0600984956,
          "HIGH24HOUR": 0.0618765576,
          "LOW24HOUR": 0.059565077,
          "LASTMARKET": "HuobiPro",
          "VOLUMEHOUR": 7264.02,
          "VOLUMEHOURTO": 441.077231283546,
          "OPENHOUR": 0.06072081729999999,
          "HIGHHOUR": 0.06072081729999999,
          "LOWHOUR": 0.06072081729999999,
          "TOPTIERVOLUME24HOUR": 36812885.18314728,
          "TOPTIERVOLUME24HOURTO": 2235308.475491763,
          "CHANGE24HOUR": 0.0006223216999999906,
          "CHANGEPCT24HOUR": 1.0355029585798659,
          "CHANGEDAY": 0.0007112248000000002,
          "CHANGEPCTDAY": 1.1851851851851856,
          "CHANGEHOUR": 0,
          "CHANGEPCTHOUR": 0,
          "CONVERSIONTYPE": "multiply",
          "CONVERSIONSYMBOL": "BTC",
          "SUPPLY": 100000000000,
          "MKTCAP": 6072081729.999999,
          "TOTALVOLUME24H": 78564084.97568677,
          "TOTALVOLUME24HTO": 4770475.45015035,
          "TOTALTOPTIERVOLUME24H": 62727518.86253818,
          "TOTALTOPTIERVOLUME24HTO": 3808866.2125344845,
          "IMAGEURL": "/media/34478435/mco.png"
        }
      },
      "DISPLAY": {
        "USD": {
          "FROMSYMBOL": "CRO",
          "TOSYMBOL": "$",
          "MARKET": "CryptoCompare Index",
          "PRICE": "$ 0.06072",
          "LASTUPDATE": "Just now",
          "LASTVOLUME": "CRO 200.00",
          "LASTVOLUMETO": "$ 12.14",
          "LASTTRADEID": "1.0006283043084477e+22",
          "VOLUMEDAY": "CRO 30,513,414.8",
          "VOLUMEDAYTO": "$ 1,852,799.5",
          "VOLUME24HOUR": "CRO 43,862,303.0",
          "VOLUME24HOURTO": "$ 2,663,354.9",
          "OPENDAY": "$ 0.06001",
          "HIGHDAY": "$ 0.06161",
          "LOWDAY": "$ 0.05965",
          "OPEN24HOUR": "$ 0.06010",
          "HIGH24HOUR": "$ 0.06188",
          "LOW24HOUR": "$ 0.05957",
          "LASTMARKET": "HuobiPro",
          "VOLUMEHOUR": "CRO 7,264.02",
          "VOLUMEHOURTO": "$ 441.08",
          "OPENHOUR": "$ 0.06072",
          "HIGHHOUR": "$ 0.06072",
          "LOWHOUR": "$ 0.06072",
          "TOPTIERVOLUME24HOUR": "CRO 36,812,885.2",
          "TOPTIERVOLUME24HOURTO": "$ 2,235,308.5",
          "CHANGE24HOUR": "$ 0.00062",
          "CHANGEPCT24HOUR": "1.04",
          "CHANGEDAY": "$ 0.00071",
          "CHANGEPCTDAY": "1.19",
          "CHANGEHOUR": "$ 0.0",
          "CHANGEPCTHOUR": "0.00",
          "CONVERSIONTYPE": "multiply",
          "CONVERSIONSYMBOL": "BTC",
          "SUPPLY": "CRO 100,000,000,000.0",
          "MKTCAP": "$ 6.07 B",
          "TOTALVOLUME24H": "CRO 78.56 M",
          "TOTALVOLUME24HTO": "$ 4.77 M",
          "TOTALTOPTIERVOLUME24H": "CRO 62.73 M",
          "TOTALTOPTIERVOLUME24HTO": "$ 3.81 M",
          "IMAGEURL": "/media/34478435/mco.png"
        }
      }
    },
    {
      "CoinInfo": {
        "Id": "930952",
        "Name": "HYN",
        "FullName": "Hyperion",
        "Internal": "HYN",
        "ImageUrl": "/media/35650877/hyn.png",
        "Url": "/coins/hyn/overview",
        "Algorithm": "N/A",
        "ProofType": "N/A",
        "Rating": {
          "Weiss": {
            "Rating": "",
            "TechnologyAdoptionRating": "",
            "MarketPerformanceRating": ""
          }
        },
        "NetHashesPerSecond": 0,
        "BlockNumber": 0,
        "BlockTime": 0,
        "BlockReward": 0,
        "Type": 1,
        "DocumentType": "Webpagecoinp"
      },
      "RAW": {
        "USD": {
          "TYPE": "5",
          "MARKET": "CCCAGG",
          "FROMSYMBOL": "HYN",
          "TOSYMBOL": "USD",
          "FLAGS": "1026",
          "PRICE": 0.6050675400000001,
          "LASTUPDATE": 1588608035,
          "MEDIAN": 0.6050799473999999,
          "LASTVOLUME": 797.86,
          "LASTVOLUMETO": 482.7591874644,
          "LASTTRADEID": "15886080350001",
          "VOLUMEDAY": 15030464.030900026,
          "VOLUMEDAYTO": 9094445.896235164,
          "VOLUME24HOUR": 17922884.3046,
          "VOLUME24HOURTO": 10844555.51588893,
          "OPENDAY": 0.37098126,
          "HIGHDAY": 0.66152121,
          "LOWDAY": 0.36953373,
          "OPEN24HOUR": 0.37139484,
          "HIGH24HOUR": 0.66152121,
          "LOW24HOUR": 0.36849978,
          "LASTMARKET": "Bibox",
          "VOLUMEHOUR": 1798.1799999999998,
          "VOLUMEHOURTO": 1088.0203490772,
          "OPENHOUR": 0.6058946999999999,
          "HIGHHOUR": 0.60630828,
          "LOWHOUR": 0.6050675400000001,
          "TOPTIERVOLUME24HOUR": 17922884.3046,
          "TOPTIERVOLUME24HOURTO": 10844555.51588893,
          "CHANGE24HOUR": 0.23367270000000007,
          "CHANGEPCT24HOUR": 62.91759465478843,
          "CHANGEDAY": 0.2340862800000001,
          "CHANGEPCTDAY": 63.09921962095878,
          "CHANGEHOUR": -0.0008271599999998269,
          "CHANGEPCTHOUR": -0.1365187713310295,
          "CONVERSIONTYPE": "multiply",
          "CONVERSIONSYMBOL": "ETH",
          "SUPPLY": 10000000000,
          "MKTCAP": 6050675400.000001,
          "TOTALVOLUME24H": 48786590.8286023,
          "TOTALVOLUME24HTO": 29519182.497648954,
          "TOTALTOPTIERVOLUME24H": 48786590.8286023,
          "TOTALTOPTIERVOLUME24HTO": 29519182.497648954,
          "IMAGEURL": "/media/35650877/hyn.png"
        }
      },
      "DISPLAY": {
        "USD": {
          "FROMSYMBOL": "HYN",
          "TOSYMBOL": "$",
          "MARKET": "CryptoCompare Index",
          "PRICE": "$ 0.6051",
          "LASTUPDATE": "Just now",
          "LASTVOLUME": "HYN 797.86",
          "LASTVOLUMETO": "$ 482.76",
          "LASTTRADEID": "15886080350001",
          "VOLUMEDAY": "HYN 15,030,464.0",
          "VOLUMEDAYTO": "$ 9,094,445.9",
          "VOLUME24HOUR": "HYN 17,922,884.3",
          "VOLUME24HOURTO": "$ 10,844,555.5",
          "OPENDAY": "$ 0.3710",
          "HIGHDAY": "$ 0.6615",
          "LOWDAY": "$ 0.3695",
          "OPEN24HOUR": "$ 0.3714",
          "HIGH24HOUR": "$ 0.6615",
          "LOW24HOUR": "$ 0.3685",
          "LASTMARKET": "Bibox",
          "VOLUMEHOUR": "HYN 1,798.18",
          "VOLUMEHOURTO": "$ 1,088.02",
          "OPENHOUR": "$ 0.6059",
          "HIGHHOUR": "$ 0.6063",
          "LOWHOUR": "$ 0.6051",
          "TOPTIERVOLUME24HOUR": "HYN 17,922,884.3",
          "TOPTIERVOLUME24HOURTO": "$ 10,844,555.5",
          "CHANGE24HOUR": "$ 0.23",
          "CHANGEPCT24HOUR": "62.92",
          "CHANGEDAY": "$ 0.23",
          "CHANGEPCTDAY": "63.10",
          "CHANGEHOUR": "$ -0.00083",
          "CHANGEPCTHOUR": "-0.14",
          "CONVERSIONTYPE": "multiply",
          "CONVERSIONSYMBOL": "ETH",
          "SUPPLY": "HYN 10,000,000,000.0",
          "MKTCAP": "$ 6.05 B",
          "TOTALVOLUME24H": "HYN 48.79 M",
          "TOTALVOLUME24HTO": "$ 29.52 M",
          "TOTALTOPTIERVOLUME24H": "HYN 48.79 M",
          "TOTALTOPTIERVOLUME24HTO": "$ 29.52 M",
          "IMAGEURL": "/media/35650877/hyn.png"
        }
      }
    },
    {
      "CoinInfo": {
        "Id": "171986",
        "Name": "USDT",
        "FullName": "Tether",
        "Internal": "USDT",
        "ImageUrl": "/media/1383672/usdt.png",
        "Url": "/coins/usdt/overview",
        "Algorithm": "N/A",
        "ProofType": "N/A",
        "Rating": {
          "Weiss": {
            "Rating": "",
            "TechnologyAdoptionRating": "",
            "MarketPerformanceRating": ""
          }
        },
        "NetHashesPerSecond": 0,
        "BlockNumber": 0,
        "BlockTime": 0,
        "BlockReward": 0,
        "Type": 1,
        "DocumentType": "Webpagecoinp"
      },
      "RAW": {
        "USD": {
          "TYPE": "5",
          "MARKET": "CCCAGG",
          "FROMSYMBOL": "USDT",
          "TOSYMBOL": "USD",
          "FLAGS": "2052",
          "PRICE": 1.001,
          "LASTUPDATE": 1588608031,
          "MEDIAN": 1.001,
          "LASTVOLUME": 173.81273594,
          "LASTVOLUMETO": 174.038692496722,
          "LASTTRADEID": "1588608031.1762",
          "VOLUMEDAY": 15747443.121178651,
          "VOLUMEDAYTO": 15755786.139271814,
          "VOLUME24HOUR": 18144173.5746615,
          "VOLUME24HOURTO": 18153654.859136734,
          "OPENDAY": 1.001,
          "HIGHDAY": 1.001,
          "LOWDAY": 1,
          "OPEN24HOUR": 1.001,
          "HIGH24HOUR": 1.001,
          "LOW24HOUR": 1,
          "LASTMARKET": "Kraken",
          "VOLUMEHOUR": 50565.04257573999,
          "VOLUMEHOURTO": 50596.92155713554,
          "OPENHOUR": 1.001,
          "HIGHHOUR": 1.001,
          "LOWHOUR": 1.001,
          "TOPTIERVOLUME24HOUR": 18136448.759853892,
          "TOPTIERVOLUME24HOURTO": 18145845.67057651,
          "CHANGE24HOUR": 0,
          "CHANGEPCT24HOUR": 0,
          "CHANGEDAY": 0,
          "CHANGEPCTDAY": 0,
          "CHANGEHOUR": 0,
          "CHANGEPCTHOUR": 0,
          "CONVERSIONTYPE": "direct",
          "CONVERSIONSYMBOL": "",
          "SUPPLY": 4642367414,
          "MKTCAP": 4647009781.414,
          "TOTALVOLUME24H": 59767977.22565654,
          "TOTALVOLUME24HTO": 59819082.31378277,
          "TOTALTOPTIERVOLUME24H": 45467163.77118031,
          "TOTALTOPTIERVOLUME24HTO": 45503891.39691425,
          "IMAGEURL": "/media/1383672/usdt.png"
        }
      },
      "DISPLAY": {
        "USD": {
          "FROMSYMBOL": "₮",
          "TOSYMBOL": "$",
          "MARKET": "CryptoCompare Index",
          "PRICE": "$ 1.00",
          "LASTUPDATE": "Just now",
          "LASTVOLUME": "₮ 173.81",
          "LASTVOLUMETO": "$ 174.04",
          "LASTTRADEID": "1588608031.1762",
          "VOLUMEDAY": "₮ 15,747,443.1",
          "VOLUMEDAYTO": "$ 15,755,786.1",
          "VOLUME24HOUR": "₮ 18,144,173.6",
          "VOLUME24HOURTO": "$ 18,153,654.9",
          "OPENDAY": "$ 1.00",
          "HIGHDAY": "$ 1.00",
          "LOWDAY": "$ 1.00",
          "OPEN24HOUR": "$ 1.00",
          "HIGH24HOUR": "$ 1.00",
          "LOW24HOUR": "$ 1.00",
          "LASTMARKET": "Kraken",
          "VOLUMEHOUR": "₮ 50,565.0",
          "VOLUMEHOURTO": "$ 50,596.9",
          "OPENHOUR": "$ 1.00",
          "HIGHHOUR": "$ 1.00",
          "LOWHOUR": "$ 1.00",
          "TOPTIERVOLUME24HOUR": "₮ 18,136,448.8",
          "TOPTIERVOLUME24HOURTO": "$ 18,145,845.7",
          "CHANGE24HOUR": "$ 0.0",
          "CHANGEPCT24HOUR": "0.00",
          "CHANGEDAY": "$ 0.0",
          "CHANGEPCTDAY": "0.00",
          "CHANGEHOUR": "$ 0.0",
          "CHANGEPCTHOUR": "0.00",
          "CONVERSIONTYPE": "direct",
          "CONVERSIONSYMBOL": "",
          "SUPPLY": "₮ 4,642,367,414.0",
          "MKTCAP": "$ 4.65 B",
          "TOTALVOLUME24H": "₮ 59.77 M",
          "TOTALVOLUME24HTO": "$ 59.82 M",
          "TOTALTOPTIERVOLUME24H": "₮ 45.47 M",
          "TOTALTOPTIERVOLUME24HTO": "$ 45.50 M",
          "IMAGEURL": "/media/1383672/usdt.png"
        }
      }
    },
    {
      "CoinInfo": {
        "Id": "202330",
        "Name": "BCH",
        "FullName": "Bitcoin Cash",
        "Internal": "BCH",
        "ImageUrl": "/media/35650680/bch.png",
        "Url": "/coins/bch/overview",
        "Algorithm": "SHA-256",
        "ProofType": "PoW",
        "Rating": {
          "Weiss": {
            "Rating": "C",
            "TechnologyAdoptionRating": "C+",
            "MarketPerformanceRating": "E"
          }
        },
        "NetHashesPerSecond": 1951295829052530000,
        "BlockNumber": 633652,
        "BlockTime": 600,
        "BlockReward": 6.25,
        "Type": 1,
        "DocumentType": "Webpagecoinp"
      },
      "RAW": {
        "USD": {
          "TYPE": "5",
          "MARKET": "CCCAGG",
          "FROMSYMBOL": "BCH",
          "TOSYMBOL": "USD",
          "FLAGS": "2052",
          "PRICE": 247.23,
          "LASTUPDATE": 1588608031,
          "MEDIAN": 247.16,
          "LASTVOLUME": 0.025,
          "LASTVOLUMETO": 6.182500000000001,
          "LASTTRADEID": "442045387",
          "VOLUMEDAY": 50689.19224127965,
          "VOLUMEDAYTO": 12303596.216005474,
          "VOLUME24HOUR": 65314.264226840016,
          "VOLUME24HOURTO": 15952597.266321843,
          "OPENDAY": 251.9,
          "HIGHDAY": 252.72,
          "LOWDAY": 236.46,
          "OPEN24HOUR": 250.37,
          "HIGH24HOUR": 253.78,
          "LOW24HOUR": 235.75,
          "LASTMARKET": "Bitfinex",
          "VOLUMEHOUR": 272.7073217,
          "VOLUMEHOURTO": 67372.63797887608,
          "OPENHOUR": 246.56,
          "HIGHHOUR": 247.23,
          "LOWHOUR": 246.54,
          "TOPTIERVOLUME24HOUR": 64978.393285530015,
          "TOPTIERVOLUME24HOURTO": 15869839.929257937,
          "CHANGE24HOUR": -3.140000000000015,
          "CHANGEPCT24HOUR": -1.2541438670767324,
          "CHANGEDAY": -4.670000000000016,
          "CHANGEPCTDAY": -1.8539102818578863,
          "CHANGEHOUR": 0.6699999999999875,
          "CHANGEPCTHOUR": 0.27173913043477754,
          "CONVERSIONTYPE": "direct",
          "CONVERSIONSYMBOL": "",
          "SUPPLY": 18397814.6467999,
          "MKTCAP": 4548491715.128339,
          "TOTALVOLUME24H": 2116480.834586476,
          "TOTALVOLUME24HTO": 523062508.4563346,
          "TOTALTOPTIERVOLUME24H": 1104368.6006473694,
          "TOTALTOPTIERVOLUME24HTO": 272838280.8953255,
          "IMAGEURL": "/media/35650680/bch.png"
        }
      },
      "DISPLAY": {
        "USD": {
          "FROMSYMBOL": "BCH",
          "TOSYMBOL": "$",
          "MARKET": "CryptoCompare Index",
          "PRICE": "$ 247.23",
          "LASTUPDATE": "Just now",
          "LASTVOLUME": "BCH 0.02500",
          "LASTVOLUMETO": "$ 6.18",
          "LASTTRADEID": "442045387",
          "VOLUMEDAY": "BCH 50,689.2",
          "VOLUMEDAYTO": "$ 12,303,596.2",
          "VOLUME24HOUR": "BCH 65,314.3",
          "VOLUME24HOURTO": "$ 15,952,597.3",
          "OPENDAY": "$ 251.90",
          "HIGHDAY": "$ 252.72",
          "LOWDAY": "$ 236.46",
          "OPEN24HOUR": "$ 250.37",
          "HIGH24HOUR": "$ 253.78",
          "LOW24HOUR": "$ 235.75",
          "LASTMARKET": "Bitfinex",
          "VOLUMEHOUR": "BCH 272.71",
          "VOLUMEHOURTO": "$ 67,372.6",
          "OPENHOUR": "$ 246.56",
          "HIGHHOUR": "$ 247.23",
          "LOWHOUR": "$ 246.54",
          "TOPTIERVOLUME24HOUR": "BCH 64,978.4",
          "TOPTIERVOLUME24HOURTO": "$ 15,869,839.9",
          "CHANGE24HOUR": "$ -3.14",
          "CHANGEPCT24HOUR": "-1.25",
          "CHANGEDAY": "$ -4.67",
          "CHANGEPCTDAY": "-1.85",
          "CHANGEHOUR": "$ 0.67",
          "CHANGEPCTHOUR": "0.27",
          "CONVERSIONTYPE": "direct",
          "CONVERSIONSYMBOL": "",
          "SUPPLY": "BCH 18,397,814.6",
          "MKTCAP": "$ 4.55 B",
          "TOTALVOLUME24H": "BCH 2.12 M",
          "TOTALVOLUME24HTO": "$ 523.06 M",
          "TOTALTOPTIERVOLUME24H": "BCH 1.10 M",
          "TOTALTOPTIERVOLUME24HTO": "$ 272.84 M",
          "IMAGEURL": "/media/35650680/bch.png"
        }
      }
    },
    {
      "CoinInfo": {
        "Id": "933127",
        "Name": "PLF",
        "FullName": "PlayFuel",
        "Internal": "PLF",
        "ImageUrl": "/media/36639916/plf.png",
        "Url": "/coins/plf/overview",
        "Algorithm": "N/A",
        "ProofType": "N/A",
        "Rating": {
          "Weiss": {
            "Rating": "",
            "TechnologyAdoptionRating": "",
            "MarketPerformanceRating": ""
          }
        },
        "NetHashesPerSecond": 0,
        "BlockNumber": 0,
        "BlockTime": 0,
        "BlockReward": 0,
        "Type": 1,
        "DocumentType": "Webpagecoinp"
      },
      "RAW": {
        "USD": {
          "TYPE": "5",
          "MARKET": "CCCAGG",
          "FROMSYMBOL": "PLF",
          "TOSYMBOL": "USD",
          "FLAGS": "2052",
          "PRICE": 0.3965967291,
          "LASTUPDATE": 1588608036,
          "MEDIAN": 0.3968634384,
          "LASTVOLUME": 4989,
          "LASTVOLUMETO": 1978.6210814799,
          "LASTTRADEID": "42096864",
          "VOLUMEDAY": 2965368.687925504,
          "VOLUMEDAYTO": 1176055.522206814,
          "VOLUME24HOUR": 4533224.26882737,
          "VOLUME24HOURTO": 1797861.917293674,
          "OPENDAY": 0.3941074422999999,
          "HIGHDAY": 0.3981080818,
          "LOWDAY": 0.392062671,
          "OPEN24HOUR": 0.3941963454,
          "HIGH24HOUR": 0.3986415004,
          "LOW24HOUR": 0.3905513183,
          "LASTMARKET": "crex24",
          "VOLUMEHOUR": 0,
          "VOLUMEHOURTO": 0,
          "OPENHOUR": 0.3965967291,
          "HIGHHOUR": 0.3965967291,
          "LOWHOUR": 0.3965967291,
          "TOPTIERVOLUME24HOUR": 0,
          "TOPTIERVOLUME24HOURTO": 0,
          "CHANGE24HOUR": 0.0024003837000000083,
          "CHANGEPCT24HOUR": 0.6089309878213824,
          "CHANGEDAY": 0.002489286800000101,
          "CHANGEPCTDAY": 0.6316264380780768,
          "CHANGEHOUR": 0,
          "CHANGEPCTHOUR": 0,
          "CONVERSIONTYPE": "multiply",
          "CONVERSIONSYMBOL": "BTC",
          "SUPPLY": 10000000000,
          "MKTCAP": 3965967291,
          "TOTALVOLUME24H": 12742333.071138393,
          "TOTALVOLUME24HTO": 5053567.6171162445,
          "TOTALTOPTIERVOLUME24H": 0,
          "TOTALTOPTIERVOLUME24HTO": 0,
          "IMAGEURL": "/media/36639916/plf.png"
        }
      },
      "DISPLAY": {
        "USD": {
          "FROMSYMBOL": "PLF",
          "TOSYMBOL": "$",
          "MARKET": "CryptoCompare Index",
          "PRICE": "$ 0.3966",
          "LASTUPDATE": "Just now",
          "LASTVOLUME": "PLF 4,989.00",
          "LASTVOLUMETO": "$ 1,978.62",
          "LASTTRADEID": "42096864",
          "VOLUMEDAY": "PLF 2,965,368.7",
          "VOLUMEDAYTO": "$ 1,176,055.5",
          "VOLUME24HOUR": "PLF 4,533,224.3",
          "VOLUME24HOURTO": "$ 1,797,861.9",
          "OPENDAY": "$ 0.3941",
          "HIGHDAY": "$ 0.3981",
          "LOWDAY": "$ 0.3921",
          "OPEN24HOUR": "$ 0.3942",
          "HIGH24HOUR": "$ 0.3986",
          "LOW24HOUR": "$ 0.3906",
          "LASTMARKET": "crex24",
          "VOLUMEHOUR": "PLF 0",
          "VOLUMEHOURTO": "$ 0",
          "OPENHOUR": "$ 0.3966",
          "HIGHHOUR": "$ 0.3966",
          "LOWHOUR": "$ 0.3966",
          "TOPTIERVOLUME24HOUR": "PLF 0",
          "TOPTIERVOLUME24HOURTO": "$ 0",
          "CHANGE24HOUR": "$ 0.0024",
          "CHANGEPCT24HOUR": "0.61",
          "CHANGEDAY": "$ 0.0025",
          "CHANGEPCTDAY": "0.63",
          "CHANGEHOUR": "$ 0.0",
          "CHANGEPCTHOUR": "0.00",
          "CONVERSIONTYPE": "multiply",
          "CONVERSIONSYMBOL": "BTC",
          "SUPPLY": "PLF 10,000,000,000.0",
          "MKTCAP": "$ 3.97 B",
          "TOTALVOLUME24H": "PLF 12.74 M",
          "TOTALVOLUME24HTO": "$ 5.05 M",
          "TOTALTOPTIERVOLUME24H": "PLF 0",
          "TOTALTOPTIERVOLUME24HTO": "$ 0",
          "IMAGEURL": "/media/36639916/plf.png"
        }
      }
    },
    {
      "CoinInfo": {
        "Id": "934311",
        "Name": "ELAMA",
        "FullName": "Elamachain",
        "Internal": "ELAMA",
        "ImageUrl": "/media/36934886/elama.png",
        "Url": "/coins/elama/overview",
        "Algorithm": "N/A",
        "ProofType": "N/A",
        "Rating": {
          "Weiss": {
            "Rating": "",
            "TechnologyAdoptionRating": "",
            "MarketPerformanceRating": ""
          }
        },
        "NetHashesPerSecond": 0,
        "BlockNumber": 0,
        "BlockTime": 0,
        "BlockReward": 0,
        "Type": 1,
        "DocumentType": "Webpagecoinp"
      },
      "RAW": {
        "USD": {
          "TYPE": "5",
          "MARKET": "CCCAGG",
          "FROMSYMBOL": "ELAMA",
          "TOSYMBOL": "USD",
          "FLAGS": "2052",
          "PRICE": 0.387617516,
          "LASTUPDATE": 1588608036,
          "MEDIAN": 0.387617516,
          "LASTVOLUME": 733.432,
          "LASTVOLUMETO": 284.291089994912,
          "LASTTRADEID": "15886075550001",
          "VOLUMEDAY": 69620.32608695001,
          "VOLUMEDAYTO": 26986.05786093356,
          "VOLUME24HOUR": 110446.44461295,
          "VOLUME24HOURTO": 42810.97651190326,
          "OPENDAY": 0.3879731284,
          "HIGHDAY": 0.3882398377,
          "LOWDAY": 0.3873508066999999,
          "OPEN24HOUR": 0.388506547,
          "HIGH24HOUR": 0.3885954501,
          "LOW24HOUR": 0.3873508066999999,
          "LASTMARKET": "BitTrex",
          "VOLUMEHOUR": 0,
          "VOLUMEHOURTO": 0,
          "OPENHOUR": 0.387617516,
          "HIGHHOUR": 0.387617516,
          "LOWHOUR": 0.387617516,
          "TOPTIERVOLUME24HOUR": 110446.44461295,
          "TOPTIERVOLUME24HOURTO": 42810.97651190326,
          "CHANGE24HOUR": -0.0008890309999999846,
          "CHANGEPCT24HOUR": -0.22883295194507614,
          "CHANGEDAY": -0.00035561239999998273,
          "CHANGEPCTDAY": -0.09165902841429437,
          "CHANGEHOUR": 0,
          "CHANGEPCTHOUR": 0,
          "CONVERSIONTYPE": "multiply",
          "CONVERSIONSYMBOL": "BTC",
          "SUPPLY": 10000000000,
          "MKTCAP": 3876175160,
          "TOTALVOLUME24H": 110446.44461295,
          "TOTALVOLUME24HTO": 42810.97651190326,
          "TOTALTOPTIERVOLUME24H": 110446.44461295,
          "TOTALTOPTIERVOLUME24HTO": 42810.97651190326,
          "IMAGEURL": "/media/36934886/elama.png"
        }
      },
      "DISPLAY": {
        "USD": {
          "FROMSYMBOL": "ELAMA",
          "TOSYMBOL": "$",
          "MARKET": "CryptoCompare Index",
          "PRICE": "$ 0.3876",
          "LASTUPDATE": "Just now",
          "LASTVOLUME": "ELAMA 733.43",
          "LASTVOLUMETO": "$ 284.29",
          "LASTTRADEID": "15886075550001",
          "VOLUMEDAY": "ELAMA 69,620.3",
          "VOLUMEDAYTO": "$ 26,986.1",
          "VOLUME24HOUR": "ELAMA 110,446.4",
          "VOLUME24HOURTO": "$ 42,811.0",
          "OPENDAY": "$ 0.3880",
          "HIGHDAY": "$ 0.3882",
          "LOWDAY": "$ 0.3874",
          "OPEN24HOUR": "$ 0.3885",
          "HIGH24HOUR": "$ 0.3886",
          "LOW24HOUR": "$ 0.3874",
          "LASTMARKET": "BitTrex",
          "VOLUMEHOUR": "ELAMA 0",
          "VOLUMEHOURTO": "$ 0",
          "OPENHOUR": "$ 0.3876",
          "HIGHHOUR": "$ 0.3876",
          "LOWHOUR": "$ 0.3876",
          "TOPTIERVOLUME24HOUR": "ELAMA 110,446.4",
          "TOPTIERVOLUME24HOURTO": "$ 42,811.0",
          "CHANGE24HOUR": "$ -0.00089",
          "CHANGEPCT24HOUR": "-0.23",
          "CHANGEDAY": "$ -0.00036",
          "CHANGEPCTDAY": "-0.09",
          "CHANGEHOUR": "$ 0.0",
          "CHANGEPCTHOUR": "0.00",
          "CONVERSIONTYPE": "multiply",
          "CONVERSIONSYMBOL": "BTC",
          "SUPPLY": "ELAMA 10,000,000,000.0",
          "MKTCAP": "$ 3.88 B",
          "TOTALVOLUME24H": "ELAMA 110.45 K",
          "TOTALVOLUME24HTO": "$ 42.81 K",
          "TOTALTOPTIERVOLUME24H": "ELAMA 110.45 K",
          "TOTALTOPTIERVOLUME24HTO": "$ 42.81 K",
          "IMAGEURL": "/media/36934886/elama.png"
        }
      }
    }
  ],
  "RateLimit": {},
  "HasWarning": false
}
```


Parameter      | Type          | Description
---------------|---------------|-------------
CoinInfo       | Object        | Coin info data.
RAW            | Object        | Raw data.
DISPLAY        | Object        | Display data.





## CCTopListVolume24H


> Sample Data

```cli
{
  "limit": "10",
  "currency": "USD"
}
```
Returns the top list of 24 hour volume. Pricing information provided by Crypto Compare.



### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '["10","USD"]' https://api.maplenodes.com/v1/CCTopListVolume24H
```

<code class="api-call">CCTopListVolume24H [limit] [currency]</code>

Parameter       | Type       | Description
----------------|------------|-------------
limit           | int        | Number of assets to return in toplist (10-100)
currency        | string     | World currency.


### Response Parameters

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
{
  "Message": "Success",
  "Type": 100,
  "SponsoredData": [],
  "Data": [
    {
      "CoinInfo": {
        "Id": "1182",
        "Name": "BTC",
        "FullName": "Bitcoin",
        "Internal": "BTC",
        "ImageUrl": "/media/19633/btc.png",
        "Url": "/coins/btc/overview",
        "Algorithm": "SHA-256",
        "ProofType": "PoW",
        "Rating": {
          "Weiss": {
            "Rating": "B+",
            "TechnologyAdoptionRating": "A",
            "MarketPerformanceRating": "D"
          }
        },
        "NetHashesPerSecond": 114238226202.791,
        "BlockNumber": 628912,
        "BlockTime": 600,
        "BlockReward": 12.5,
        "Type": 1,
        "DocumentType": "Webpagecoinp"
      },
      "RAW": {
        "USD": {
          "TYPE": "5",
          "MARKET": "CCCAGG",
          "FROMSYMBOL": "BTC",
          "TOSYMBOL": "USD",
          "FLAGS": "2052",
          "PRICE": 8884.06,
          "LASTUPDATE": 1588608085,
          "MEDIAN": 8874.98,
          "LASTVOLUME": 0.01,
          "LASTVOLUMETO": 88.875,
          "LASTTRADEID": "1588608085_1",
          "VOLUMEDAY": 45232.47557574955,
          "VOLUMEDAYTO": 394706362.9450392,
          "VOLUME24HOUR": 57183.6670712809,
          "VOLUME24HOURTO": 500706356.6172946,
          "OPENDAY": 8907.07,
          "HIGHDAY": 8946.95,
          "LOWDAY": 8537.49,
          "OPEN24HOUR": 8859,
          "HIGH24HOUR": 8967.86,
          "LOW24HOUR": 8513.06,
          "LASTMARKET": "lmax",
          "VOLUMEHOUR": 526.3744268199976,
          "VOLUMEHOURTO": 4673329.087019654,
          "OPENHOUR": 8854.23,
          "HIGHHOUR": 8891.56,
          "LOWHOUR": 8854.2,
          "TOPTIERVOLUME24HOUR": 54906.51324697089,
          "TOPTIERVOLUME24HOURTO": 480733314.2135993,
          "CHANGE24HOUR": 25.05999999999949,
          "CHANGEPCT24HOUR": 0.2828761711254034,
          "CHANGEDAY": -23.01000000000022,
          "CHANGEPCTDAY": -0.25833410987002703,
          "CHANGEHOUR": 29.829999999999927,
          "CHANGEPCTHOUR": 0.3369011195778733,
          "CONVERSIONTYPE": "direct",
          "CONVERSIONSYMBOL": "",
          "SUPPLY": 18361400,
          "MKTCAP": 163123779284,
          "TOTALVOLUME24H": 646499.5483110677,
          "TOTALVOLUME24HTO": 5736224004.504435,
          "TOTALTOPTIERVOLUME24H": 414822.2748669354,
          "TOTALTOPTIERVOLUME24HTO": 3678246535.391061,
          "IMAGEURL": "/media/19633/btc.png"
        }
      },
      "DISPLAY": {
        "USD": {
          "FROMSYMBOL": "Ƀ",
          "TOSYMBOL": "$",
          "MARKET": "CryptoCompare Index",
          "PRICE": "$ 8,884.06",
          "LASTUPDATE": "Just now",
          "LASTVOLUME": "Ƀ 0.01000",
          "LASTVOLUMETO": "$ 88.88",
          "LASTTRADEID": "1588608085_1",
          "VOLUMEDAY": "Ƀ 45,232.5",
          "VOLUMEDAYTO": "$ 394,706,362.9",
          "VOLUME24HOUR": "Ƀ 57,183.7",
          "VOLUME24HOURTO": "$ 500,706,356.6",
          "OPENDAY": "$ 8,907.07",
          "HIGHDAY": "$ 8,946.95",
          "LOWDAY": "$ 8,537.49",
          "OPEN24HOUR": "$ 8,859.00",
          "HIGH24HOUR": "$ 8,967.86",
          "LOW24HOUR": "$ 8,513.06",
          "LASTMARKET": "lmax",
          "VOLUMEHOUR": "Ƀ 526.37",
          "VOLUMEHOURTO": "$ 4,673,329.1",
          "OPENHOUR": "$ 8,854.23",
          "HIGHHOUR": "$ 8,891.56",
          "LOWHOUR": "$ 8,854.20",
          "TOPTIERVOLUME24HOUR": "Ƀ 54,906.5",
          "TOPTIERVOLUME24HOURTO": "$ 480,733,314.2",
          "CHANGE24HOUR": "$ 25.06",
          "CHANGEPCT24HOUR": "0.28",
          "CHANGEDAY": "$ -23.01",
          "CHANGEPCTDAY": "-0.26",
          "CHANGEHOUR": "$ 29.83",
          "CHANGEPCTHOUR": "0.34",
          "CONVERSIONTYPE": "direct",
          "CONVERSIONSYMBOL": "",
          "SUPPLY": "Ƀ 18,361,400.0",
          "MKTCAP": "$ 163.12 B",
          "TOTALVOLUME24H": "Ƀ 646.50 K",
          "TOTALVOLUME24HTO": "$ 5.74 B",
          "TOTALTOPTIERVOLUME24H": "Ƀ 414.82 K",
          "TOTALTOPTIERVOLUME24HTO": "$ 3.68 B",
          "IMAGEURL": "/media/19633/btc.png"
        }
      }
    },
    {
      "CoinInfo": {
        "Id": "7605",
        "Name": "ETH",
        "FullName": "Ethereum",
        "Internal": "ETH",
        "ImageUrl": "/media/20646/eth_logo.png",
        "Url": "/coins/eth/overview",
        "Algorithm": "Ethash",
        "ProofType": "PoW",
        "Rating": {
          "Weiss": {
            "Rating": "B+",
            "TechnologyAdoptionRating": "A",
            "MarketPerformanceRating": "D"
          }
        },
        "NetHashesPerSecond": 180269998621113,
        "BlockNumber": 10000605,
        "BlockTime": 15,
        "BlockReward": 2,
        "Type": 1,
        "DocumentType": "Webpagecoinp"
      },
      "RAW": {
        "USD": {
          "TYPE": "5",
          "MARKET": "CCCAGG",
          "FROMSYMBOL": "ETH",
          "TOSYMBOL": "USD",
          "FLAGS": "2052",
          "PRICE": 206.77,
          "LASTUPDATE": 1588608084,
          "MEDIAN": 206.75,
          "LASTVOLUME": 2.9116,
          "LASTVOLUMETO": 602.031532,
          "LASTTRADEID": "509515",
          "VOLUMEDAY": 470103.6117200457,
          "VOLUMEDAYTO": 95035992.22237962,
          "VOLUME24HOUR": 568378.2559965601,
          "VOLUME24HOURTO": 115574677.19726644,
          "OPENDAY": 210.06,
          "HIGHDAY": 210.81,
          "LOWDAY": 195.3,
          "OPEN24HOUR": 208.98,
          "HIGH24HOUR": 211.75,
          "LOW24HOUR": 195.09,
          "LASTMARKET": "OKCoin",
          "VOLUMEHOUR": 2742.558382990002,
          "VOLUMEHOURTO": 566954.5107032723,
          "OPENHOUR": 206.23,
          "HIGHHOUR": 206.95,
          "LOWHOUR": 206.23,
          "TOPTIERVOLUME24HOUR": 554794.5518189,
          "TOPTIERVOLUME24HOURTO": 112817150.6273891,
          "CHANGE24HOUR": -2.2099999999999795,
          "CHANGEPCT24HOUR": -1.0575174657861899,
          "CHANGEDAY": -3.289999999999992,
          "CHANGEPCTDAY": -1.5662191754736703,
          "CHANGEHOUR": 0.5400000000000205,
          "CHANGEPCTHOUR": 0.2618435727100909,
          "CONVERSIONTYPE": "direct",
          "CONVERSIONSYMBOL": "",
          "SUPPLY": 110789015.874,
          "MKTCAP": 22907844812.26698,
          "TOTALVOLUME24H": 11661546.354900157,
          "TOTALVOLUME24HTO": 2409309045.007563,
          "TOTALTOPTIERVOLUME24H": 6102021.593037258,
          "TOTALTOPTIERVOLUME24HTO": 1259817285.9401093,
          "IMAGEURL": "/media/20646/eth_logo.png"
        }
      },
      "DISPLAY": {
        "USD": {
          "FROMSYMBOL": "Ξ",
          "TOSYMBOL": "$",
          "MARKET": "CryptoCompare Index",
          "PRICE": "$ 206.77",
          "LASTUPDATE": "Just now",
          "LASTVOLUME": "Ξ 2.91",
          "LASTVOLUMETO": "$ 602.03",
          "LASTTRADEID": "509515",
          "VOLUMEDAY": "Ξ 470,103.6",
          "VOLUMEDAYTO": "$ 95,035,992.2",
          "VOLUME24HOUR": "Ξ 568,378.3",
          "VOLUME24HOURTO": "$ 115,574,677.2",
          "OPENDAY": "$ 210.06",
          "HIGHDAY": "$ 210.81",
          "LOWDAY": "$ 195.30",
          "OPEN24HOUR": "$ 208.98",
          "HIGH24HOUR": "$ 211.75",
          "LOW24HOUR": "$ 195.09",
          "LASTMARKET": "OKCoin",
          "VOLUMEHOUR": "Ξ 2,742.56",
          "VOLUMEHOURTO": "$ 566,954.5",
          "OPENHOUR": "$ 206.23",
          "HIGHHOUR": "$ 206.95",
          "LOWHOUR": "$ 206.23",
          "TOPTIERVOLUME24HOUR": "Ξ 554,794.6",
          "TOPTIERVOLUME24HOURTO": "$ 112,817,150.6",
          "CHANGE24HOUR": "$ -2.21",
          "CHANGEPCT24HOUR": "-1.06",
          "CHANGEDAY": "$ -3.29",
          "CHANGEPCTDAY": "-1.57",
          "CHANGEHOUR": "$ 0.54",
          "CHANGEPCTHOUR": "0.26",
          "CONVERSIONTYPE": "direct",
          "CONVERSIONSYMBOL": "",
          "SUPPLY": "Ξ 110,789,015.9",
          "MKTCAP": "$ 22.91 B",
          "TOTALVOLUME24H": "Ξ 11.66 M",
          "TOTALVOLUME24HTO": "$ 2.41 B",
          "TOTALTOPTIERVOLUME24H": "Ξ 6.10 M",
          "TOTALTOPTIERVOLUME24HTO": "$ 1.26 B",
          "IMAGEURL": "/media/20646/eth_logo.png"
        }
      }
    },
    {
      "CoinInfo": {
        "Id": "166503",
        "Name": "EOS",
        "FullName": "EOS",
        "Internal": "EOS",
        "ImageUrl": "/media/1383652/eos_1.png",
        "Url": "/coins/eos/overview",
        "Algorithm": "DPoS",
        "ProofType": "DPoS",
        "Rating": {
          "Weiss": {
            "Rating": "C+",
            "TechnologyAdoptionRating": "B-",
            "MarketPerformanceRating": "D-"
          }
        },
        "NetHashesPerSecond": 0,
        "BlockNumber": 69480094,
        "BlockTime": 3,
        "BlockReward": 0,
        "Type": 1,
        "DocumentType": "Webpagecoinp"
      },
      "RAW": {
        "USD": {
          "TYPE": "5",
          "MARKET": "CCCAGG",
          "FROMSYMBOL": "EOS",
          "TOSYMBOL": "USD",
          "FLAGS": "516",
          "PRICE": 2.785,
          "LASTUPDATE": 1588608088,
          "MEDIAN": 2.7815,
          "LASTVOLUME": 19.2,
          "LASTVOLUMETO": 53.404799999999994,
          "LASTTRADEID": "442043458",
          "VOLUMEDAY": 1863770.5186698542,
          "VOLUMEDAYTO": 5066036.446964271,
          "VOLUME24HOUR": 2147426.25136197,
          "VOLUME24HOURTO": 5856771.10049991,
          "OPENDAY": 2.839,
          "HIGHDAY": 2.847,
          "LOWDAY": 2.631,
          "OPEN24HOUR": 2.827,
          "HIGH24HOUR": 2.85,
          "LOW24HOUR": 2.63,
          "LASTMARKET": "Bitfinex",
          "VOLUMEHOUR": 13298.799688400013,
          "VOLUMEHOURTO": 37076.34157046786,
          "OPENHOUR": 2.779,
          "HIGHHOUR": 2.79,
          "LOWHOUR": 2.779,
          "TOPTIERVOLUME24HOUR": 2147372.39346232,
          "TOPTIERVOLUME24HOURTO": 5856622.2967562685,
          "CHANGE24HOUR": -0.041999999999999815,
          "CHANGEPCT24HOUR": -1.4856738592147087,
          "CHANGEDAY": -0.053999999999999826,
          "CHANGEPCTDAY": -1.9020781965480742,
          "CHANGEHOUR": 0.006000000000000227,
          "CHANGEPCTHOUR": 0.21590500179921654,
          "CONVERSIONTYPE": "direct",
          "CONVERSIONSYMBOL": "",
          "SUPPLY": 1020544523.0722,
          "MKTCAP": 2842216496.756077,
          "TOTALVOLUME24H": 234133193.5701495,
          "TOTALVOLUME24HTO": 651937133.0833232,
          "TOTALTOPTIERVOLUME24H": 113606363.88563548,
          "TOTALTOPTIERVOLUME24HTO": 316269913.60245854,
          "IMAGEURL": "/media/1383652/eos_1.png"
        }
      },
      "DISPLAY": {
        "USD": {
          "FROMSYMBOL": "EOS",
          "TOSYMBOL": "$",
          "MARKET": "CryptoCompare Index",
          "PRICE": "$ 2.79",
          "LASTUPDATE": "Just now",
          "LASTVOLUME": "EOS 19.20",
          "LASTVOLUMETO": "$ 53.40",
          "LASTTRADEID": "442043458",
          "VOLUMEDAY": "EOS 1,863,770.5",
          "VOLUMEDAYTO": "$ 5,066,036.4",
          "VOLUME24HOUR": "EOS 2,147,426.3",
          "VOLUME24HOURTO": "$ 5,856,771.1",
          "OPENDAY": "$ 2.84",
          "HIGHDAY": "$ 2.85",
          "LOWDAY": "$ 2.63",
          "OPEN24HOUR": "$ 2.83",
          "HIGH24HOUR": "$ 2.85",
          "LOW24HOUR": "$ 2.63",
          "LASTMARKET": "Bitfinex",
          "VOLUMEHOUR": "EOS 13,298.8",
          "VOLUMEHOURTO": "$ 37,076.3",
          "OPENHOUR": "$ 2.78",
          "HIGHHOUR": "$ 2.79",
          "LOWHOUR": "$ 2.78",
          "TOPTIERVOLUME24HOUR": "EOS 2,147,372.4",
          "TOPTIERVOLUME24HOURTO": "$ 5,856,622.3",
          "CHANGE24HOUR": "$ -0.042",
          "CHANGEPCT24HOUR": "-1.49",
          "CHANGEDAY": "$ -0.054",
          "CHANGEPCTDAY": "-1.90",
          "CHANGEHOUR": "$ 0.0060",
          "CHANGEPCTHOUR": "0.22",
          "CONVERSIONTYPE": "direct",
          "CONVERSIONSYMBOL": "",
          "SUPPLY": "EOS 1,020,544,523.1",
          "MKTCAP": "$ 2.84 B",
          "TOTALVOLUME24H": "EOS 234.13 M",
          "TOTALVOLUME24HTO": "$ 651.94 M",
          "TOTALTOPTIERVOLUME24H": "EOS 113.61 M",
          "TOTALTOPTIERVOLUME24HTO": "$ 316.27 M",
          "IMAGEURL": "/media/1383652/eos_1.png"
        }
      }
    },
    {
      "CoinInfo": {
        "Id": "844139",
        "Name": "TUSD",
        "FullName": "True USD",
        "Internal": "TUSD",
        "ImageUrl": "/media/35650578/tusd.png",
        "Url": "/coins/tusd/overview",
        "Algorithm": "N/A",
        "ProofType": "N/A",
        "Rating": {
          "Weiss": {
            "Rating": "",
            "TechnologyAdoptionRating": "",
            "MarketPerformanceRating": ""
          }
        },
        "NetHashesPerSecond": 0,
        "BlockNumber": 0,
        "BlockTime": 0,
        "BlockReward": 0,
        "Type": 1,
        "DocumentType": "Webpagecoinp"
      },
      "RAW": {
        "USD": {
          "TYPE": "5",
          "MARKET": "CCCAGG",
          "FROMSYMBOL": "TUSD",
          "TOSYMBOL": "USD",
          "FLAGS": "2052",
          "PRICE": 0.9970089730807579,
          "LASTUPDATE": 1588606011,
          "MEDIAN": 0.9970089730807579,
          "LASTVOLUME": 65.62629,
          "LASTVOLUMETO": 65.43,
          "LASTTRADEID": "837113828",
          "VOLUMEDAY": 15619.328411970006,
          "VOLUMEDAYTO": 15600.559999999998,
          "VOLUME24HOUR": 20187.20907802,
          "VOLUME24HOURTO": 20172.26,
          "OPENDAY": 0.9990009990009991,
          "HIGHDAY": 1.001001001001001,
          "LOWDAY": 0.9970089730807579,
          "OPEN24HOUR": 1,
          "HIGH24HOUR": 1.002004008016032,
          "LOW24HOUR": 0.9970089730807579,
          "LASTMARKET": "HitBTC",
          "VOLUMEHOUR": 0,
          "VOLUMEHOURTO": 0,
          "OPENHOUR": 0.9970089730807579,
          "HIGHHOUR": 0.9970089730807579,
          "LOWHOUR": 0.9970089730807579,
          "TOPTIERVOLUME24HOUR": 20187.20907802,
          "TOPTIERVOLUME24HOURTO": 20172.26,
          "CHANGE24HOUR": -0.0029910269192421346,
          "CHANGEPCT24HOUR": -0.29910269192421346,
          "CHANGEDAY": -0.0019920259202412804,
          "CHANGEPCTDAY": -0.19940179461615215,
          "CHANGEHOUR": 0,
          "CHANGEPCTHOUR": 0,
          "CONVERSIONTYPE": "invert",
          "CONVERSIONSYMBOL": "",
          "SUPPLY": 137381003.68,
          "MKTCAP": 136970093.39980063,
          "TOTALVOLUME24H": 619121293.4166268,
          "TOTALVOLUME24HTO": 617269530.3931494,
          "TOTALTOPTIERVOLUME24H": 7151110.249568579,
          "TOTALTOPTIERVOLUME24HTO": 7129766.517717407,
          "IMAGEURL": "/media/35650578/tusd.png"
        }
      },
      "DISPLAY": {
        "USD": {
          "FROMSYMBOL": "TUSD",
          "TOSYMBOL": "$",
          "MARKET": "CryptoCompare Index",
          "PRICE": "$ 0.9970",
          "LASTUPDATE": "34 min ago",
          "LASTVOLUME": "TUSD 65.63",
          "LASTVOLUMETO": "$ 65.43",
          "LASTTRADEID": "837113828",
          "VOLUMEDAY": "TUSD 15,619.3",
          "VOLUMEDAYTO": "$ 15,600.6",
          "VOLUME24HOUR": "TUSD 20,187.2",
          "VOLUME24HOURTO": "$ 20,172.3",
          "OPENDAY": "$ 0.9990",
          "HIGHDAY": "$ 1.00",
          "LOWDAY": "$ 0.9970",
          "OPEN24HOUR": "$ 1.00",
          "HIGH24HOUR": "$ 1.00",
          "LOW24HOUR": "$ 0.9970",
          "LASTMARKET": "HitBTC",
          "VOLUMEHOUR": "TUSD 0",
          "VOLUMEHOURTO": "$ 0",
          "OPENHOUR": "$ 0.9970",
          "HIGHHOUR": "$ 0.9970",
          "LOWHOUR": "$ 0.9970",
          "TOPTIERVOLUME24HOUR": "TUSD 20,187.2",
          "TOPTIERVOLUME24HOURTO": "$ 20,172.3",
          "CHANGE24HOUR": "$ -0.0030",
          "CHANGEPCT24HOUR": "-0.30",
          "CHANGEDAY": "$ -0.0020",
          "CHANGEPCTDAY": "-0.20",
          "CHANGEHOUR": "$ 0.0",
          "CHANGEPCTHOUR": "0.00",
          "CONVERSIONTYPE": "invert",
          "CONVERSIONSYMBOL": "",
          "SUPPLY": "TUSD 137,381,003.7",
          "MKTCAP": "$ 136.97 M",
          "TOTALVOLUME24H": "TUSD 619.12 M",
          "TOTALVOLUME24HTO": "$ 617.27 M",
          "TOTALTOPTIERVOLUME24H": "TUSD 7.15 M",
          "TOTALTOPTIERVOLUME24HTO": "$ 7.13 M",
          "IMAGEURL": "/media/35650578/tusd.png"
        }
      }
    },
    {
      "CoinInfo": {
        "Id": "202330",
        "Name": "BCH",
        "FullName": "Bitcoin Cash",
        "Internal": "BCH",
        "ImageUrl": "/media/35650680/bch.png",
        "Url": "/coins/bch/overview",
        "Algorithm": "SHA-256",
        "ProofType": "PoW",
        "Rating": {
          "Weiss": {
            "Rating": "C",
            "TechnologyAdoptionRating": "C+",
            "MarketPerformanceRating": "E"
          }
        },
        "NetHashesPerSecond": 1977960925466640000,
        "BlockNumber": 633654,
        "BlockTime": 600,
        "BlockReward": 6.25,
        "Type": 1,
        "DocumentType": "Webpagecoinp"
      },
      "RAW": {
        "USD": {
          "TYPE": "5",
          "MARKET": "CCCAGG",
          "FROMSYMBOL": "BCH",
          "TOSYMBOL": "USD",
          "FLAGS": "2050",
          "PRICE": 247.2,
          "LASTUPDATE": 1588608077,
          "MEDIAN": 247.2,
          "LASTVOLUME": 3.41,
          "LASTVOLUMETO": 843.3271000000001,
          "LASTTRADEID": "16062485",
          "VOLUMEDAY": 50701.130625349644,
          "VOLUMEDAYTO": 12306550.494803313,
          "VOLUME24HOUR": 65326.20261091001,
          "VOLUME24HOURTO": 15955551.545119682,
          "OPENDAY": 251.9,
          "HIGHDAY": 252.72,
          "LOWDAY": 236.46,
          "OPEN24HOUR": 250.37,
          "HIGH24HOUR": 253.78,
          "LOW24HOUR": 235.75,
          "LASTMARKET": "Coinbase",
          "VOLUMEHOUR": 284.64570577000006,
          "VOLUMEHOURTO": 70326.91677671496,
          "OPENHOUR": 246.56,
          "HIGHHOUR": 247.41,
          "LOWHOUR": 246.54,
          "TOPTIERVOLUME24HOUR": 64990.331669600004,
          "TOPTIERVOLUME24HOURTO": 15872794.208055776,
          "CHANGE24HOUR": -3.170000000000016,
          "CHANGEPCT24HOUR": -1.2661261333226888,
          "CHANGEDAY": -4.700000000000017,
          "CHANGEPCTDAY": -1.8658197697499075,
          "CHANGEHOUR": 0.6399999999999864,
          "CHANGEPCTHOUR": 0.2595717066839659,
          "CONVERSIONTYPE": "direct",
          "CONVERSIONSYMBOL": "",
          "SUPPLY": 18397827.1467999,
          "MKTCAP": 4547942870.688935,
          "TOTALVOLUME24H": 2120226.2980311844,
          "TOTALVOLUME24HTO": 523926855.1330115,
          "TOTALTOPTIERVOLUME24H": 1106841.108242674,
          "TOTALTOPTIERVOLUME24HTO": 273418306.1769197,
          "IMAGEURL": "/media/35650680/bch.png"
        }
      },
      "DISPLAY": {
        "USD": {
          "FROMSYMBOL": "BCH",
          "TOSYMBOL": "$",
          "MARKET": "CryptoCompare Index",
          "PRICE": "$ 247.20",
          "LASTUPDATE": "Just now",
          "LASTVOLUME": "BCH 3.41",
          "LASTVOLUMETO": "$ 843.33",
          "LASTTRADEID": "16062485",
          "VOLUMEDAY": "BCH 50,701.1",
          "VOLUMEDAYTO": "$ 12,306,550.5",
          "VOLUME24HOUR": "BCH 65,326.2",
          "VOLUME24HOURTO": "$ 15,955,551.5",
          "OPENDAY": "$ 251.90",
          "HIGHDAY": "$ 252.72",
          "LOWDAY": "$ 236.46",
          "OPEN24HOUR": "$ 250.37",
          "HIGH24HOUR": "$ 253.78",
          "LOW24HOUR": "$ 235.75",
          "LASTMARKET": "Coinbase",
          "VOLUMEHOUR": "BCH 284.65",
          "VOLUMEHOURTO": "$ 70,326.9",
          "OPENHOUR": "$ 246.56",
          "HIGHHOUR": "$ 247.41",
          "LOWHOUR": "$ 246.54",
          "TOPTIERVOLUME24HOUR": "BCH 64,990.3",
          "TOPTIERVOLUME24HOURTO": "$ 15,872,794.2",
          "CHANGE24HOUR": "$ -3.17",
          "CHANGEPCT24HOUR": "-1.27",
          "CHANGEDAY": "$ -4.70",
          "CHANGEPCTDAY": "-1.87",
          "CHANGEHOUR": "$ 0.64",
          "CHANGEPCTHOUR": "0.26",
          "CONVERSIONTYPE": "direct",
          "CONVERSIONSYMBOL": "",
          "SUPPLY": "BCH 18,397,827.1",
          "MKTCAP": "$ 4.55 B",
          "TOTALVOLUME24H": "BCH 2.12 M",
          "TOTALVOLUME24HTO": "$ 523.93 M",
          "TOTALTOPTIERVOLUME24H": "BCH 1.11 M",
          "TOTALTOPTIERVOLUME24HTO": "$ 273.42 M",
          "IMAGEURL": "/media/35650680/bch.png"
        }
      }
    },
    {
      "CoinInfo": {
        "Id": "5324",
        "Name": "ETC",
        "FullName": "Ethereum Classic",
        "Internal": "ETC",
        "ImageUrl": "/media/33752295/etc_new.png",
        "Url": "/coins/etc/overview",
        "Algorithm": "Ethash",
        "ProofType": "PoW",
        "Rating": {
          "Weiss": {
            "Rating": "C+",
            "TechnologyAdoptionRating": "B-",
            "MarketPerformanceRating": "E+"
          }
        },
        "NetHashesPerSecond": 8510964339720,
        "BlockNumber": 0,
        "BlockTime": 14,
        "BlockReward": 3.2,
        "Type": 1,
        "DocumentType": "Webpagecoinp"
      },
      "RAW": {
        "USD": {
          "TYPE": "5",
          "MARKET": "CCCAGG",
          "FROMSYMBOL": "ETC",
          "TOSYMBOL": "USD",
          "FLAGS": "1026",
          "PRICE": 7.298,
          "LASTUPDATE": 1588608070,
          "MEDIAN": 7.311,
          "LASTVOLUME": 8.2114,
          "LASTVOLUMETO": 60.148505,
          "LASTTRADEID": "1588608070.1827",
          "VOLUMEDAY": 619493.0932036992,
          "VOLUMEDAYTO": 4343489.357684183,
          "VOLUME24HOUR": 905097.60209333,
          "VOLUME24HOURTO": 6405343.7096770555,
          "OPENDAY": 7.219,
          "HIGHDAY": 7.357,
          "LOWDAY": 6.683,
          "OPEN24HOUR": 7.342,
          "HIGH24HOUR": 7.399,
          "LOW24HOUR": 6.68,
          "LASTMARKET": "Kraken",
          "VOLUMEHOUR": 5906.946863309998,
          "VOLUMEHOURTO": 43317.507270999675,
          "OPENHOUR": 7.293,
          "HIGHHOUR": 7.357,
          "LOWHOUR": 7.293,
          "TOPTIERVOLUME24HOUR": 905097.60209333,
          "TOPTIERVOLUME24HOURTO": 6405343.7096770555,
          "CHANGE24HOUR": -0.043999999999999595,
          "CHANGEPCT24HOUR": -0.5992917461182184,
          "CHANGEDAY": 0.07899999999999974,
          "CHANGEPCTDAY": 1.0943343953456122,
          "CHANGEHOUR": 0.004999999999999893,
          "CHANGEPCTHOUR": 0.06855889208830239,
          "CONVERSIONTYPE": "direct",
          "CONVERSIONSYMBOL": "",
          "SUPPLY": 114733314.76127,
          "MKTCAP": 837323731.1277485,
          "TOTALVOLUME24H": 70708441.23581254,
          "TOTALVOLUME24HTO": 515830145.5485599,
          "TOTALTOPTIERVOLUME24H": 36096350.099910006,
          "TOTALTOPTIERVOLUME24HTO": 263231104.43874317,
          "IMAGEURL": "/media/33752295/etc_new.png"
        }
      },
      "DISPLAY": {
        "USD": {
          "FROMSYMBOL": "ETC",
          "TOSYMBOL": "$",
          "MARKET": "CryptoCompare Index",
          "PRICE": "$ 7.30",
          "LASTUPDATE": "Just now",
          "LASTVOLUME": "ETC 8.21",
          "LASTVOLUMETO": "$ 60.15",
          "LASTTRADEID": "1588608070.1827",
          "VOLUMEDAY": "ETC 619,493.1",
          "VOLUMEDAYTO": "$ 4,343,489.4",
          "VOLUME24HOUR": "ETC 905,097.6",
          "VOLUME24HOURTO": "$ 6,405,343.7",
          "OPENDAY": "$ 7.22",
          "HIGHDAY": "$ 7.36",
          "LOWDAY": "$ 6.68",
          "OPEN24HOUR": "$ 7.34",
          "HIGH24HOUR": "$ 7.40",
          "LOW24HOUR": "$ 6.68",
          "LASTMARKET": "Kraken",
          "VOLUMEHOUR": "ETC 5,906.95",
          "VOLUMEHOURTO": "$ 43,317.5",
          "OPENHOUR": "$ 7.29",
          "HIGHHOUR": "$ 7.36",
          "LOWHOUR": "$ 7.29",
          "TOPTIERVOLUME24HOUR": "ETC 905,097.6",
          "TOPTIERVOLUME24HOURTO": "$ 6,405,343.7",
          "CHANGE24HOUR": "$ -0.044",
          "CHANGEPCT24HOUR": "-0.60",
          "CHANGEDAY": "$ 0.079",
          "CHANGEPCTDAY": "1.09",
          "CHANGEHOUR": "$ 0.0050",
          "CHANGEPCTHOUR": "0.07",
          "CONVERSIONTYPE": "direct",
          "CONVERSIONSYMBOL": "",
          "SUPPLY": "ETC 114,733,314.8",
          "MKTCAP": "$ 837.32 M",
          "TOTALVOLUME24H": "ETC 70.71 M",
          "TOTALVOLUME24HTO": "$ 515.83 M",
          "TOTALTOPTIERVOLUME24H": "ETC 36.10 M",
          "TOTALTOPTIERVOLUME24HTO": "$ 263.23 M",
          "IMAGEURL": "/media/33752295/etc_new.png"
        }
      }
    },
    {
      "CoinInfo": {
        "Id": "926591",
        "Name": "BSV",
        "FullName": "Bitcoin SV",
        "Internal": "BSV",
        "ImageUrl": "/media/35309257/bsv1.png",
        "Url": "/coins/bsv/overview",
        "Algorithm": "SHA-256",
        "ProofType": "PoW",
        "Rating": {
          "Weiss": {
            "Rating": "D+",
            "TechnologyAdoptionRating": "C-",
            "MarketPerformanceRating": "D-"
          }
        },
        "NetHashesPerSecond": 1555630723797500000,
        "BlockNumber": 633466,
        "BlockTime": 0,
        "BlockReward": 6.25,
        "Type": 1,
        "DocumentType": "Webpagecoinp"
      },
      "RAW": {
        "USD": {
          "TYPE": "5",
          "MARKET": "CCCAGG",
          "FROMSYMBOL": "BSV",
          "TOSYMBOL": "USD",
          "FLAGS": "1028",
          "PRICE": 204.67,
          "LASTUPDATE": 1588608086,
          "MEDIAN": 204.28,
          "LASTVOLUME": 1.46297246,
          "LASTVOLUMETO": 298.8560141288,
          "LASTTRADEID": "442034004",
          "VOLUMEDAY": 10219.041728539984,
          "VOLUMEDAYTO": 2048248.9053474243,
          "VOLUME24HOUR": 10959.17042628,
          "VOLUME24HOURTO": 2200948.671280569,
          "OPENDAY": 207.91,
          "HIGHDAY": 209.39,
          "LOWDAY": 191.22,
          "OPEN24HOUR": 206.94,
          "HIGH24HOUR": 209.51,
          "LOW24HOUR": 191.35,
          "LASTMARKET": "Bitfinex",
          "VOLUMEHOUR": 32.5819733,
          "VOLUMEHOURTO": 6661.6769360888,
          "OPENHOUR": 203.69,
          "HIGHHOUR": 204.96,
          "LOWHOUR": 203.69,
          "TOPTIERVOLUME24HOUR": 10959.17042628,
          "TOPTIERVOLUME24HOURTO": 2200948.671280569,
          "CHANGE24HOUR": -2.2700000000000102,
          "CHANGEPCT24HOUR": -1.0969363100415628,
          "CHANGEDAY": -3.240000000000009,
          "CHANGEPCTDAY": -1.5583666009331005,
          "CHANGEHOUR": 0.9799999999999898,
          "CHANGEPCTHOUR": 0.48112327556580575,
          "CONVERSIONTYPE": "direct",
          "CONVERSIONSYMBOL": "",
          "SUPPLY": 18396652.0819233,
          "MKTCAP": 3765242781.607241,
          "TOTALVOLUME24H": 1779612.0747343851,
          "TOTALVOLUME24HTO": 364191138.5960204,
          "TOTALTOPTIERVOLUME24H": 1073525.0475900215,
          "TOTALTOPTIERVOLUME24HTO": 219676306.75038353,
          "IMAGEURL": "/media/35309257/bsv1.png"
        }
      },
      "DISPLAY": {
        "USD": {
          "FROMSYMBOL": "BSV",
          "TOSYMBOL": "$",
          "MARKET": "CryptoCompare Index",
          "PRICE": "$ 204.67",
          "LASTUPDATE": "Just now",
          "LASTVOLUME": "BSV 1.46",
          "LASTVOLUMETO": "$ 298.86",
          "LASTTRADEID": "442034004",
          "VOLUMEDAY": "BSV 10,219.0",
          "VOLUMEDAYTO": "$ 2,048,248.9",
          "VOLUME24HOUR": "BSV 10,959.2",
          "VOLUME24HOURTO": "$ 2,200,948.7",
          "OPENDAY": "$ 207.91",
          "HIGHDAY": "$ 209.39",
          "LOWDAY": "$ 191.22",
          "OPEN24HOUR": "$ 206.94",
          "HIGH24HOUR": "$ 209.51",
          "LOW24HOUR": "$ 191.35",
          "LASTMARKET": "Bitfinex",
          "VOLUMEHOUR": "BSV 32.58",
          "VOLUMEHOURTO": "$ 6,661.68",
          "OPENHOUR": "$ 203.69",
          "HIGHHOUR": "$ 204.96",
          "LOWHOUR": "$ 203.69",
          "TOPTIERVOLUME24HOUR": "BSV 10,959.2",
          "TOPTIERVOLUME24HOURTO": "$ 2,200,948.7",
          "CHANGE24HOUR": "$ -2.27",
          "CHANGEPCT24HOUR": "-1.10",
          "CHANGEDAY": "$ -3.24",
          "CHANGEPCTDAY": "-1.56",
          "CHANGEHOUR": "$ 0.98",
          "CHANGEPCTHOUR": "0.48",
          "CONVERSIONTYPE": "direct",
          "CONVERSIONSYMBOL": "",
          "SUPPLY": "BSV 18,396,652.1",
          "MKTCAP": "$ 3.77 B",
          "TOTALVOLUME24H": "BSV 1.78 M",
          "TOTALVOLUME24HTO": "$ 364.19 M",
          "TOTALTOPTIERVOLUME24H": "BSV 1.07 M",
          "TOTALTOPTIERVOLUME24HTO": "$ 219.68 M",
          "IMAGEURL": "/media/35309257/bsv1.png"
        }
      }
    },
    {
      "CoinInfo": {
        "Id": "5031",
        "Name": "XRP",
        "FullName": "XRP",
        "Internal": "XRP",
        "ImageUrl": "/media/34477776/xrp.png",
        "Url": "/coins/xrp/overview",
        "Algorithm": "N/A",
        "ProofType": "N/A",
        "Rating": {
          "Weiss": {
            "Rating": "B-",
            "TechnologyAdoptionRating": "B+",
            "MarketPerformanceRating": "D-"
          }
        },
        "NetHashesPerSecond": 0,
        "BlockNumber": 0,
        "BlockTime": 4,
        "BlockReward": 0,
        "Type": 1,
        "DocumentType": "Webpagecoinp"
      },
      "RAW": {
        "USD": {
          "TYPE": "5",
          "MARKET": "CCCAGG",
          "FROMSYMBOL": "XRP",
          "TOSYMBOL": "USD",
          "FLAGS": "2052",
          "PRICE": 0.219,
          "LASTUPDATE": 1588608089,
          "MEDIAN": 0.2188,
          "LASTVOLUME": 142.148244,
          "LASTVOLUMETO": 31.07502762084,
          "LASTTRADEID": "15886080890002",
          "VOLUMEDAY": 153828300.9552291,
          "VOLUMEDAYTO": 32835240.022716925,
          "VOLUME24HOUR": 188769281.79609063,
          "VOLUME24HOURTO": 40466934.533296354,
          "OPENDAY": 0.2194,
          "HIGHDAY": 0.2207,
          "LOWDAY": 0.2074,
          "OPEN24HOUR": 0.2189,
          "HIGH24HOUR": 0.2216,
          "LOW24HOUR": 0.2074,
          "LASTMARKET": "BitTrex",
          "VOLUMEHOUR": 1172506.6261389903,
          "VOLUMEHOURTO": 256742.53674032018,
          "OPENHOUR": 0.2186,
          "HIGHHOUR": 0.2192,
          "LOWHOUR": 0.2186,
          "TOPTIERVOLUME24HOUR": 188760483.4969959,
          "TOPTIERVOLUME24HOURTO": 40465076.24511535,
          "CHANGE24HOUR": 9.999999999998899e-05,
          "CHANGEPCT24HOUR": 0.04568296025581955,
          "CHANGEDAY": -0.00040000000000001146,
          "CHANGEPCTDAY": -0.1823154056517828,
          "CHANGEHOUR": 0.00040000000000001146,
          "CHANGEPCTHOUR": 0.18298261665142337,
          "CONVERSIONTYPE": "direct",
          "CONVERSIONSYMBOL": "",
          "SUPPLY": 99991850794,
          "MKTCAP": 21898215323.886,
          "TOTALVOLUME24H": 1667666111.4829407,
          "TOTALVOLUME24HTO": 364345340.23471653,
          "TOTALTOPTIERVOLUME24H": 1237082853.5591474,
          "TOTALTOPTIERVOLUME24HTO": 270047675.2887265,
          "IMAGEURL": "/media/34477776/xrp.png"
        }
      },
      "DISPLAY": {
        "USD": {
          "FROMSYMBOL": "XRP",
          "TOSYMBOL": "$",
          "MARKET": "CryptoCompare Index",
          "PRICE": "$ 0.2190",
          "LASTUPDATE": "Just now",
          "LASTVOLUME": "XRP 142.15",
          "LASTVOLUMETO": "$ 31.08",
          "LASTTRADEID": "15886080890002",
          "VOLUMEDAY": "XRP 153,828,301.0",
          "VOLUMEDAYTO": "$ 32,835,240.0",
          "VOLUME24HOUR": "XRP 188,769,281.8",
          "VOLUME24HOURTO": "$ 40,466,934.5",
          "OPENDAY": "$ 0.2194",
          "HIGHDAY": "$ 0.2207",
          "LOWDAY": "$ 0.2074",
          "OPEN24HOUR": "$ 0.2189",
          "HIGH24HOUR": "$ 0.2216",
          "LOW24HOUR": "$ 0.2074",
          "LASTMARKET": "BitTrex",
          "VOLUMEHOUR": "XRP 1,172,506.6",
          "VOLUMEHOURTO": "$ 256,742.5",
          "OPENHOUR": "$ 0.2186",
          "HIGHHOUR": "$ 0.2192",
          "LOWHOUR": "$ 0.2186",
          "TOPTIERVOLUME24HOUR": "XRP 188,760,483.5",
          "TOPTIERVOLUME24HOURTO": "$ 40,465,076.2",
          "CHANGE24HOUR": "$ 0.00010",
          "CHANGEPCT24HOUR": "0.05",
          "CHANGEDAY": "$ -0.00040",
          "CHANGEPCTDAY": "-0.18",
          "CHANGEHOUR": "$ 0.00040",
          "CHANGEPCTHOUR": "0.18",
          "CONVERSIONTYPE": "direct",
          "CONVERSIONSYMBOL": "",
          "SUPPLY": "XRP 99,991,850,794.0",
          "MKTCAP": "$ 21.90 B",
          "TOTALVOLUME24H": "XRP 1.67 B",
          "TOTALVOLUME24HTO": "$ 364.35 M",
          "TOTALTOPTIERVOLUME24H": "XRP 1.24 B",
          "TOTALTOPTIERVOLUME24HTO": "$ 270.05 M",
          "IMAGEURL": "/media/34477776/xrp.png"
        }
      }
    },
    {
      "CoinInfo": {
        "Id": "3808",
        "Name": "LTC",
        "FullName": "Litecoin",
        "Internal": "LTC",
        "ImageUrl": "/media/35309662/ltc.png",
        "Url": "/coins/ltc/overview",
        "Algorithm": "Scrypt",
        "ProofType": "PoW",
        "Rating": {
          "Weiss": {
            "Rating": "B-",
            "TechnologyAdoptionRating": "B+",
            "MarketPerformanceRating": "D-"
          }
        },
        "NetHashesPerSecond": 152498639444493,
        "BlockNumber": 1835255,
        "BlockTime": 150,
        "BlockReward": 12.4999999975165,
        "Type": 1,
        "DocumentType": "Webpagecoinp"
      },
      "RAW": {
        "USD": {
          "TYPE": "5",
          "MARKET": "CCCAGG",
          "FROMSYMBOL": "LTC",
          "TOSYMBOL": "USD",
          "FLAGS": "2052",
          "PRICE": 47.34,
          "LASTUPDATE": 1588608090,
          "MEDIAN": 47.32,
          "LASTVOLUME": 7.79963,
          "LASTVOLUMETO": 368.7665064,
          "LASTTRADEID": "62140258",
          "VOLUMEDAY": 276365.9659365289,
          "VOLUMEDAYTO": 12831088.37199474,
          "VOLUME24HOUR": 351662.52105106995,
          "VOLUME24HOURTO": 16402222.350785641,
          "OPENDAY": 48.12,
          "HIGHDAY": 48.24,
          "LOWDAY": 45.24,
          "OPEN24HOUR": 47.65,
          "HIGH24HOUR": 48.31,
          "LOW24HOUR": 45.22,
          "LASTMARKET": "BTCAlpha",
          "VOLUMEHOUR": 1002.22482775,
          "VOLUMEHOURTO": 47454.90802329166,
          "OPENHOUR": 47.26,
          "HIGHHOUR": 47.37,
          "LOWHOUR": 47.26,
          "TOPTIERVOLUME24HOUR": 317581.39580665,
          "TOPTIERVOLUME24HOURTO": 14813674.752956398,
          "CHANGE24HOUR": -0.30999999999999517,
          "CHANGEPCT24HOUR": -0.6505771248688251,
          "CHANGEDAY": -0.779999999999994,
          "CHANGEPCTDAY": -1.6209476309226807,
          "CHANGEHOUR": 0.0800000000000054,
          "CHANGEPCTHOUR": 0.169276343630989,
          "CONVERSIONTYPE": "direct",
          "CONVERSIONSYMBOL": "",
          "SUPPLY": 64938708.0057612,
          "MKTCAP": 3074198436.9927354,
          "TOTALVOLUME24H": 7028675.2943008095,
          "TOTALVOLUME24HTO": 332492007.03642833,
          "TOTALTOPTIERVOLUME24H": 4283737.374255774,
          "TOTALTOPTIERVOLUME24HTO": 202571498.77273792,
          "IMAGEURL": "/media/35309662/ltc.png"
        }
      },
      "DISPLAY": {
        "USD": {
          "FROMSYMBOL": "Ł",
          "TOSYMBOL": "$",
          "MARKET": "CryptoCompare Index",
          "PRICE": "$ 47.34",
          "LASTUPDATE": "Just now",
          "LASTVOLUME": "Ł 7.80",
          "LASTVOLUMETO": "$ 368.77",
          "LASTTRADEID": "62140258",
          "VOLUMEDAY": "Ł 276,366.0",
          "VOLUMEDAYTO": "$ 12,831,088.4",
          "VOLUME24HOUR": "Ł 351,662.5",
          "VOLUME24HOURTO": "$ 16,402,222.4",
          "OPENDAY": "$ 48.12",
          "HIGHDAY": "$ 48.24",
          "LOWDAY": "$ 45.24",
          "OPEN24HOUR": "$ 47.65",
          "HIGH24HOUR": "$ 48.31",
          "LOW24HOUR": "$ 45.22",
          "LASTMARKET": "BTCAlpha",
          "VOLUMEHOUR": "Ł 1,002.22",
          "VOLUMEHOURTO": "$ 47,454.9",
          "OPENHOUR": "$ 47.26",
          "HIGHHOUR": "$ 47.37",
          "LOWHOUR": "$ 47.26",
          "TOPTIERVOLUME24HOUR": "Ł 317,581.4",
          "TOPTIERVOLUME24HOURTO": "$ 14,813,674.8",
          "CHANGE24HOUR": "$ -0.31",
          "CHANGEPCT24HOUR": "-0.65",
          "CHANGEDAY": "$ -0.78",
          "CHANGEPCTDAY": "-1.62",
          "CHANGEHOUR": "$ 0.080",
          "CHANGEPCTHOUR": "0.17",
          "CONVERSIONTYPE": "direct",
          "CONVERSIONSYMBOL": "",
          "SUPPLY": "Ł 64,938,708.0",
          "MKTCAP": "$ 3.07 B",
          "TOTALVOLUME24H": "Ł 7.03 M",
          "TOTALVOLUME24HTO": "$ 332.49 M",
          "TOTALTOPTIERVOLUME24H": "Ł 4.28 M",
          "TOTALTOPTIERVOLUME24HTO": "$ 202.57 M",
          "IMAGEURL": "/media/35309662/ltc.png"
        }
      }
    },
    {
      "CoinInfo": {
        "Id": "4614",
        "Name": "XLM",
        "FullName": "Stellar",
        "Internal": "XLM",
        "ImageUrl": "/media/35521289/xlm.png",
        "Url": "/coins/xlm/overview",
        "Algorithm": "N/A",
        "ProofType": "N/A",
        "Rating": {
          "Weiss": {
            "Rating": "C+",
            "TechnologyAdoptionRating": "B",
            "MarketPerformanceRating": "D"
          }
        },
        "NetHashesPerSecond": 0,
        "BlockNumber": 0,
        "BlockTime": 0,
        "BlockReward": 0,
        "Type": 1,
        "DocumentType": "Webpagecoinp"
      },
      "RAW": {
        "USD": {
          "TYPE": "5",
          "MARKET": "CCCAGG",
          "FROMSYMBOL": "XLM",
          "TOSYMBOL": "USD",
          "FLAGS": "2049",
          "PRICE": 0.07379,
          "LASTUPDATE": 1588608087,
          "MEDIAN": 0.0735,
          "LASTVOLUME": 671,
          "LASTVOLUMETO": 49.565428,
          "LASTTRADEID": "4105759",
          "VOLUMEDAY": 68236008.23762074,
          "VOLUMEDAYTO": 4796144.216254544,
          "VOLUME24HOUR": 88984556.0258368,
          "VOLUME24HOURTO": 6302979.635320942,
          "OPENDAY": 0.07313,
          "HIGHDAY": 0.07392,
          "LOWDAY": 0.06779,
          "OPEN24HOUR": 0.07285,
          "HIGH24HOUR": 0.07398,
          "LOW24HOUR": 0.06758,
          "LASTMARKET": "Coinbase",
          "VOLUMEHOUR": 152598.77527931,
          "VOLUMEHOURTO": 11281.00577214806,
          "OPENHOUR": 0.07358,
          "HIGHHOUR": 0.07392,
          "LOWHOUR": 0.07358,
          "TOPTIERVOLUME24HOUR": 88984480.88297966,
          "TOPTIERVOLUME24HOURTO": 6302974.375320942,
          "CHANGE24HOUR": 0.0009399999999999964,
          "CHANGEPCT24HOUR": 1.2903225806451564,
          "CHANGEDAY": 0.0006599999999999939,
          "CHANGEPCTDAY": 0.902502392998761,
          "CHANGEHOUR": 0.00020999999999998797,
          "CHANGEPCTHOUR": 0.28540364229408527,
          "CONVERSIONTYPE": "direct",
          "CONVERSIONSYMBOL": "",
          "SUPPLY": 20223415802,
          "MKTCAP": 1492285852.0295799,
          "TOTALVOLUME24H": 3812635899.3051987,
          "TOTALVOLUME24HTO": 281071212.25590503,
          "TOTALTOPTIERVOLUME24H": 609578910.5794994,
          "TOTALTOPTIERVOLUME24HTO": 44717637.34262713,
          "IMAGEURL": "/media/35521289/xlm.png"
        }
      },
      "DISPLAY": {
        "USD": {
          "FROMSYMBOL": "XLM",
          "TOSYMBOL": "$",
          "MARKET": "CryptoCompare Index",
          "PRICE": "$ 0.07379",
          "LASTUPDATE": "Just now",
          "LASTVOLUME": "XLM 671.00",
          "LASTVOLUMETO": "$ 49.57",
          "LASTTRADEID": "4105759",
          "VOLUMEDAY": "XLM 68,236,008.2",
          "VOLUMEDAYTO": "$ 4,796,144.2",
          "VOLUME24HOUR": "XLM 88,984,556.0",
          "VOLUME24HOURTO": "$ 6,302,979.6",
          "OPENDAY": "$ 0.07313",
          "HIGHDAY": "$ 0.07392",
          "LOWDAY": "$ 0.06779",
          "OPEN24HOUR": "$ 0.07285",
          "HIGH24HOUR": "$ 0.07398",
          "LOW24HOUR": "$ 0.06758",
          "LASTMARKET": "Coinbase",
          "VOLUMEHOUR": "XLM 152,598.8",
          "VOLUMEHOURTO": "$ 11,281.0",
          "OPENHOUR": "$ 0.07358",
          "HIGHHOUR": "$ 0.07392",
          "LOWHOUR": "$ 0.07358",
          "TOPTIERVOLUME24HOUR": "XLM 88,984,480.9",
          "TOPTIERVOLUME24HOURTO": "$ 6,302,974.4",
          "CHANGE24HOUR": "$ 0.00094",
          "CHANGEPCT24HOUR": "1.29",
          "CHANGEDAY": "$ 0.00066",
          "CHANGEPCTDAY": "0.90",
          "CHANGEHOUR": "$ 0.00021",
          "CHANGEPCTHOUR": "0.29",
          "CONVERSIONTYPE": "direct",
          "CONVERSIONSYMBOL": "",
          "SUPPLY": "XLM 20,223,415,802.0",
          "MKTCAP": "$ 1.49 B",
          "TOTALVOLUME24H": "XLM 3.81 B",
          "TOTALVOLUME24HTO": "$ 281.07 M",
          "TOTALTOPTIERVOLUME24H": "XLM 609.58 M",
          "TOTALTOPTIERVOLUME24HTO": "$ 44.72 M",
          "IMAGEURL": "/media/35521289/xlm.png"
        }
      }
    }
  ],
  "RateLimit": {},
  "HasWarning": false
}
```


Parameter      | Type          | Description
---------------|---------------|-------------
CoinInfo       | Object        | Coin info data.
RAW            | Object        | Raw data.
DISPLAY        | Object        | Display data.





## CCTopListVolumeByPair

> Sample Data

```cli
{
  "ticker": "BTC"
}
```
Returns the top list of volume by pair. Pricing information provided by Crypto Compare.



### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '["BTC"]' https://api.maplenodes.com/v1/CCTopListVolumeByPair
```

<code class="api-call">CCTopListVolumeByPair [ticker]</code>

Parameter       | Type       | Description
----------------|------------|-------------
ticker          | string     | Crypto currency ticker.


### Response Parameters

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
{
  "Data": [
    {
      "SYMBOL": "LIPS",
      "SUPPLY": 0,
      "FULLNAME": "LipChain (LIPS)",
      "NAME": "LipChain",
      "ID": "928569",
      "VOLUME24HOURTO": 13007294.48231
    },
    {
      "SYMBOL": "ETH",
      "SUPPLY": 110789041.874,
      "FULLNAME": "Ethereum (ETH)",
      "NAME": "Ethereum",
      "ID": "7605",
      "VOLUME24HOURTO": 33544.96071507822
    },
    {
      "SYMBOL": "BCH",
      "SUPPLY": 18397827.1467999,
      "FULLNAME": "Bitcoin Cash (BCH)",
      "NAME": "Bitcoin Cash",
      "ID": "202330",
      "VOLUME24HOURTO": 16496.182256017244
    },
    {
      "SYMBOL": "EOS",
      "SUPPLY": 1020544523.0722,
      "FULLNAME": "EOS (EOS)",
      "NAME": "EOS",
      "ID": "166503",
      "VOLUME24HOURTO": 16395.163909776165
    },
    {
      "SYMBOL": "BSV",
      "SUPPLY": 18396652.0819233,
      "FULLNAME": "Bitcoin SV (BSV)",
      "NAME": "Bitcoin SV",
      "ID": "926591",
      "VOLUME24HOURTO": 13363.373435626554
    },
    {
      "SYMBOL": "ETC",
      "SUPPLY": 114733314.76127,
      "FULLNAME": "Ethereum Classic (ETC)",
      "NAME": "Ethereum Classic",
      "ID": "5324",
      "VOLUME24HOURTO": 9347.157249735406
    },
    {
      "SYMBOL": "QTUM",
      "SUPPLY": 100000000,
      "FULLNAME": "QTUM (QTUM)",
      "NAME": "QTUM",
      "ID": "112392",
      "VOLUME24HOURTO": 7691.881395609399
    },
    {
      "SYMBOL": "DATA",
      "SUPPLY": 987154514,
      "FULLNAME": "Streamr DATAcoin (DATA)",
      "NAME": "Streamr DATAcoin",
      "ID": "369151",
      "VOLUME24HOURTO": 6020.170163852114
    },
    {
      "SYMBOL": "XRP",
      "SUPPLY": 99991850794,
      "FULLNAME": "XRP (XRP)",
      "NAME": "XRP",
      "ID": "5031",
      "VOLUME24HOURTO": 6010.647037081988
    },
    {
      "SYMBOL": "LTC",
      "SUPPLY": 64938708.0057612,
      "FULLNAME": "Litecoin (LTC)",
      "NAME": "Litecoin",
      "ID": "3808",
      "VOLUME24HOURTO": 5978.870334883455
    },
    {
      "SYMBOL": "XLM",
      "SUPPLY": 20223415802,
      "FULLNAME": "Stellar (XLM)",
      "NAME": "Stellar",
      "ID": "4614",
      "VOLUME24HOURTO": 5792.094432763407
    },
    {
      "SYMBOL": "TRX",
      "SUPPLY": 66752027614.8321,
      "FULLNAME": "TRON (TRX)",
      "NAME": "TRON",
      "ID": "310829",
      "VOLUME24HOURTO": 2359.528321651738
    },
    {
      "SYMBOL": "OMG",
      "SUPPLY": 140245398.245133,
      "FULLNAME": "OmiseGo (OMG)",
      "NAME": "OmiseGo",
      "ID": "187440",
      "VOLUME24HOURTO": 2188.2901753036467
    },
    {
      "SYMBOL": "LINK",
      "SUPPLY": 1000000000,
      "FULLNAME": "Chainlink (LINK)",
      "NAME": "Chainlink",
      "ID": "309621",
      "VOLUME24HOURTO": 2146.5044573269765
    },
    {
      "SYMBOL": "BNB",
      "SUPPLY": 155536713,
      "FULLNAME": "Binance Coin (BNB)",
      "NAME": "Binance Coin",
      "ID": "204788",
      "VOLUME24HOURTO": 2143.784016362084
    },
    {
      "SYMBOL": "ZEC",
      "SUPPLY": 9082156.25,
      "FULLNAME": "ZCash (ZEC)",
      "NAME": "ZCash",
      "ID": "24854",
      "VOLUME24HOURTO": 2031.047056008054
    },
    {
      "SYMBOL": "NEO",
      "SUPPLY": 100000000,
      "FULLNAME": "NEO (NEO)",
      "NAME": "NEO",
      "ID": "27368",
      "VOLUME24HOURTO": 1949.7157149607178
    },
    {
      "SYMBOL": "OKB",
      "SUPPLY": 300000000,
      "FULLNAME": "Okex (OKB)",
      "NAME": "Okex",
      "ID": "925144",
      "VOLUME24HOURTO": 1852.7903522970119
    },
    {
      "SYMBOL": "XTZ",
      "SUPPLY": 810904882.005803,
      "FULLNAME": "Tezos (XTZ)",
      "NAME": "Tezos",
      "ID": "166390",
      "VOLUME24HOURTO": 1805.5410264333902
    },
    {
      "SYMBOL": "XMR",
      "SUPPLY": 17547647.7481086,
      "FULLNAME": "Monero (XMR)",
      "NAME": "Monero",
      "ID": "5038",
      "VOLUME24HOURTO": 1689.4258261503492
    },
    {
      "SYMBOL": "TRUE",
      "SUPPLY": 100000000,
      "FULLNAME": "True Chain (TRUE)",
      "NAME": "True Chain",
      "ID": "887527",
      "VOLUME24HOURTO": 1677.3203859323
    }
  ],
  "Type": 100,
  "Response": "Success",
  "VolSymbol": "BTC",
  "Message": "All ok",
  "RateLimit": {},
  "HasWarning": false
}
```


Parameter      | Type          | Description
---------------|---------------|-------------
Data           | array         | Data array containing top list asset by pair.
SYMBOL         | string        | Crypto ticker.
SUPPLY         | int           | Total supply.
FULLNAME       | string        | Crypto name and ticker.
NAME           | string        | Crypto name.
ID             | int           | Crypto ID.
VOLUME24HOURTO | int           | Volume 24 hour to.
Type           | int           | Type.
Response       | string        | Response.
VolSymbol      | string        | Volume ticker.
Message        | string        | Message.
RateLimit      | string        | Rate limit.
HasWarning     | bool          | If no warnings `false`, otherwise `true`.
