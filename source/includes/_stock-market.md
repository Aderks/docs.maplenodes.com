# Stock Market Information

Call                                                      | Description
----------------------------------------------------------|---------------------------------
[GlobalStockLatestInfo](#globalstocklatestinfo)           | Retrieves the latest pricing and volume information for a given stock.
[GlobalStockSymbolSearch](#globalstocksymbolsearch)       | Information for globally traded assets based on a single keyword search. Any assets relevant to the keyword search will be outputted.




## GlobalStockLatestInfo

> Sample Data

```cli
{
  "ticker_symbol": "AAPL"
}
```
Retrieves the latest pricing and volume information for a given stock.


### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '["AAPL"]' https://api.maplenodes.com/v1/GlobalStockLatestInfo
```

<code class="api-call">GlobalStockLatestInfo [ticker_symbol]</code>

Parameter       | Type       | Description
----------------|------------|-------------
ticker_symbol   | string     | Single ticker symbol.


### Response Parameters

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
{
  "Global Quote": {
    "01. symbol": "AAPL",
    "02. open": "286.2500",
    "03. high": "299.0000",
    "04. low": "285.8500",
    "05. price": "289.0700",
    "06. volume": "60154175",
    "07. latest trading day": "2020-05-01",
    "08. previous close": "293.8000",
    "09. change": "-4.7300",
    "10. change percent": "-1.6099%"
  }
}
```

Parameter               | Type       | Description
------------------------|------------|-------------
01. symbol              | string     | Ticker symbol.
02. open                | int        | Market open price.
03. high                | int        | Market daily high price.
04. low                 | int        | Market daily low price.
05. price               | int        | Current price.
06. volume              | int        | Market volume.
07. latest trading day  | string     | Latest trading day.
08. previous close      | int        | Previous closing price.
09. change              | int        | Change in price from current to previous close.
10. change percent      | sring      | Change in price percentage.




## GlobalStockSymbolSearch

> Sample Data

```cli
{
  "keyword": "google"
}
```
Information for globally traded assets based on a single keyword search. Any assets relevant to the keyword search will be outputted.


### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '["google"]' https://api.maplenodes.com/v1/GlobalStockSymbolSearch
```

<code class="api-call">GlobalStockSymbolSearch [keyword]</code>

Parameter       | Type       | Description
----------------|------------|-------------
keyword         | string     | Search keyword.


### Response Parameters

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
{
  "bestMatches": [
    {
      "1. symbol": "GOOG",
      "2. name": "Alphabet Inc.",
      "3. type": "Equity",
      "4. region": "United States",
      "5. marketOpen": "09:30",
      "6. marketClose": "16:00",
      "7. timezone": "UTC-05",
      "8. currency": "USD",
      "9. matchScore": "0.9091"
    },
    {
      "1. symbol": "GOOGL",
      "2. name": "Alphabet Inc.",
      "3. type": "Equity",
      "4. region": "United States",
      "5. marketOpen": "09:30",
      "6. marketClose": "16:00",
      "7. timezone": "UTC-05",
      "8. currency": "USD",
      "9. matchScore": "0.8000"
    },
    {
      "1. symbol": "GOOGL.MIL",
      "2. name": "ALPHABET CLASSE A",
      "3. type": "Equity",
      "4. region": "Milan",
      "5. marketOpen": "09:00",
      "6. marketClose": "17:30",
      "7. timezone": "UTC+02",
      "8. currency": "EUR",
      "9. matchScore": "0.7143"
    },
    {
      "1. symbol": "GOOGL.ARG",
      "2. name": "Alphabet Inc.",
      "3. type": "Equity",
      "4. region": "Argentina",
      "5. marketOpen": "11:00",
      "6. marketClose": "17:00",
      "7. timezone": "UTC-03",
      "8. currency": "ARS",
      "9. matchScore": "0.7143"
    },
    {
      "1. symbol": "GOOGL.MEX",
      "2. name": "Alphabet Inc.",
      "3. type": "Equity",
      "4. region": "Mexico",
      "5. marketOpen": "08:30",
      "6. marketClose": "15:00",
      "7. timezone": "UTC-05",
      "8. currency": "MXP",
      "9. matchScore": "0.7143"
    },
    {
      "1. symbol": "GOOG.MIL",
      "2. name": "Alphabet Inc.",
      "3. type": "Equity",
      "4. region": "Milan",
      "5. marketOpen": "09:00",
      "6. marketClose": "17:30",
      "7. timezone": "UTC+02",
      "8. currency": "EUR",
      "9. matchScore": "0.6154"
    },
    {
      "1. symbol": "GOOG.MEX",
      "2. name": "Alphabet Inc.",
      "3. type": "Equity",
      "4. region": "Mexico",
      "5. marketOpen": "08:30",
      "6. marketClose": "15:00",
      "7. timezone": "UTC-05",
      "8. currency": "MXP",
      "9. matchScore": "0.6154"
    }
  ]
}
```

Parameter       | Type       | Description
----------------|------------|-------------
1. symbol       | string     | Ticker symbol.
2. name         | string     | Company name.
3. type         | string     | Type of asset.
4. region       | int        | Region of asset.
5. marketOpen   | int        | Time market opens.
6. marketClose  | int        | Time market closes.
7. timezone     | string     | Asset timezone.
8. currency     | int        | Currency asset is traded in.
9. matchScore   | int        | Search match percentage in decimal form. 
