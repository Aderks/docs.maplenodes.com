# Utility Services

Call                                                      | Description
----------------------------------------------------------|---------------------------------
[BitlyURLShortener](#bitlyurlshortener)                   | Shortens user provided URL via Bitly.
[CurrencyExchangeRate](#currencyexchangerate)             | Outputs the exchange rate between two currency pairs.
[WorldCurrencyList](#worldcurrencylist)                   | Outputs a full list of world currency names.



## BitlyURLShortener

> Sample Data

```cli
{
  "long_url": "https://www.google.com/"
}
```
Shortens user provided URL via Bitly.

**Note:** Ensure to include HTTP/HTTPS in the URL link or you will receive a `null` response.


### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '["https://www.google.com/"]' https://api.maplenodes.com/v1/BitlyURLShortener
```

<code class="api-call">BitlyURLShortener [long_url]</code>

Parameter       | Type       | Description
----------------|------------|-------------
long_url        | string     | URL to be shortened.


### Response Parameters

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
[
  {
    "shortened_url": "https://bit.ly/2WWi4R8",
    "long_url": "https://www.google.com/"
  }
]
```

Parameter       | Type       | Description
----------------|------------|-------------
shortened_url   | string     | Shortened URL.
long_url        | string     | URL that was shortened.





## CurrencyExchangeRate

> Sample Data

```cli
{
  "currency_id1": "CAD",
  "currency_id2": "USD"
}
```
Outputs the exchange rate between two currency pairs.


### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '["CAD","USD"]' https://api.maplenodes.com/v1/CurrencyExchangeRate
```

<code class="api-call">CurrencyExchangeRate [currency_id1] [currency_id2]</code>

Parameter       | Type       | Description
----------------|------------|-------------
currency_id1    | string     | Currency to compare exchange rate with.
currency_id2    | string     | Currency to compare exchange rate with.


### Response Parameters

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
{
  "CAD_USD": 0.709675
}
```

Parameter       | Type       | Description
----------------|------------|-------------
exchange_rate   | int        | Exchange rate of currency_id1 and currency_id2.





## WorldCurrencyList

Outputs a full list of world currency names.

### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '[]' https://api.maplenodes.com/v1/WorldCurrencyList
```

<code class="api-call">WorldCurrencyList</code>

This call does not take parameters.


### Response

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
[
  {
    "currencyName": "Albanian Lek",
    "id": "ALL"
  },
  {
    "currencyName": "East Caribbean Dollar",
    "id": "XCD"
  },
  {
    "currencyName": "Euro",
    "id": "EUR"
  },
  {
    "currencyName": "Barbadian Dollar",
    "id": "BBD"
  },
  {
    "currencyName": "Bhutanese Ngultrum",
    "id": "BTN"
  },
  {
    "currencyName": "Brunei Dollar",
    "id": "BND"
  },
  {
    "currencyName": "Central African CFA Franc",
    "id": "XAF"
  },
  {
    "currencyName": "Cuban Peso",
    "id": "CUP"
  },
  {
    "currencyName": "United States Dollar",
    "id": "USD"
  },
  {
    "currencyName": "Falkland Islands Pound",
    "id": "FKP"
  },
  {
    "currencyName": "Gibraltar Pound",
    "id": "GIP"
  },
  {
    "currencyName": "Hungarian Forint",
    "id": "HUF"
  },
  {
    "currencyName": "Iranian Rial",
    "id": "IRR"
  },
  {
    "currencyName": "Jamaican Dollar",
    "id": "JMD"
  },
  {
    "currencyName": "Australian Dollar",
    "id": "AUD"
  },
  {
    "currencyName": "Lao Kip",
    "id": "LAK"
  },
  {
    "currencyName": "Libyan Dinar",
    "id": "LYD"
  },
  {
    "currencyName": "Macedonian Denar",
    "id": "MKD"
  },
  {
    "currencyName": "West African CFA Franc",
    "id": "XOF"
  },
  {
    "currencyName": "New Zealand Dollar",
    "id": "NZD"
  },
  {
    "currencyName": "Omani Rial",
    "id": "OMR"
  },
  {
    "currencyName": "Papua New Guinean Kina",
    "id": "PGK"
  },
  {
    "currencyName": "Rwandan Franc",
    "id": "RWF"
  },
  {
    "currencyName": "Samoan Tala",
    "id": "WST"
  },
  {
    "currencyName": "Serbian Dinar",
    "id": "RSD"
  },
  {
    "currencyName": "Swedish Krona",
    "id": "SEK"
  },
  {
    "currencyName": "Tanzanian Shilling",
    "id": "TZS"
  },
  {
    "currencyName": "Armenian Dram",
    "id": "AMD"
  },
  {
    "currencyName": "Bahamian Dollar",
    "id": "BSD"
  },
  {
    "currencyName": "Bosnia And Herzegovina Konvertibilna Marka",
    "id": "BAM"
  },
  {
    "currencyName": "Cape Verdean Escudo",
    "id": "CVE"
  },
  {
    "currencyName": "Chinese Yuan",
    "id": "CNY"
  },
  {
    "currencyName": "Costa Rican Colon",
    "id": "CRC"
  },
  {
    "currencyName": "Czech Koruna",
    "id": "CZK"
  },
  {
    "currencyName": "Eritrean Nakfa",
    "id": "ERN"
  },
  {
    "currencyName": "Georgian Lari",
    "id": "GEL"
  },
  {
    "currencyName": "Haitian Gourde",
    "id": "HTG"
  },
  {
    "currencyName": "Indian Rupee",
    "id": "INR"
  },
  {
    "currencyName": "Jordanian Dinar",
    "id": "JOD"
  },
  {
    "currencyName": "South Korean Won",
    "id": "KRW"
  },
  {
    "currencyName": "Lebanese Lira",
    "id": "LBP"
  },
  {
    "currencyName": "Malawian Kwacha",
    "id": "MWK"
  },
  {
    "currencyName": "Mauritanian Ouguiya",
    "id": "MRO"
  },
  {
    "currencyName": "Mozambican Metical",
    "id": "MZN"
  },
  {
    "currencyName": "Netherlands Antillean Gulden",
    "id": "ANG"
  },
  {
    "currencyName": "Peruvian Nuevo Sol",
    "id": "PEN"
  },
  {
    "currencyName": "Qatari Riyal",
    "id": "QAR"
  },
  {
    "currencyName": "Sao Tome And Principe Dobra",
    "id": "STD"
  },
  {
    "currencyName": "Sierra Leonean Leone",
    "id": "SLL"
  },
  {
    "currencyName": "Somali Shilling",
    "id": "SOS"
  },
  {
    "currencyName": "Sudanese Pound",
    "id": "SDG"
  },
  {
    "currencyName": "Syrian Pound",
    "id": "SYP"
  },
  {
    "currencyName": "Angolan Kwanza",
    "id": "AOA"
  },
  {
    "currencyName": "Aruban Florin",
    "id": "AWG"
  },
  {
    "currencyName": "Bahraini Dinar",
    "id": "BHD"
  },
  {
    "currencyName": "Belize Dollar",
    "id": "BZD"
  },
  {
    "currencyName": "Botswana Pula",
    "id": "BWP"
  },
  {
    "currencyName": "Burundi Franc",
    "id": "BIF"
  },
  {
    "currencyName": "Cayman Islands Dollar",
    "id": "KYD"
  },
  {
    "currencyName": "Colombian Peso",
    "id": "COP"
  },
  {
    "currencyName": "Danish Krone",
    "id": "DKK"
  },
  {
    "currencyName": "Guatemalan Quetzal",
    "id": "GTQ"
  },
  {
    "currencyName": "Honduran Lempira",
    "id": "HNL"
  },
  {
    "currencyName": "Indonesian Rupiah",
    "id": "IDR"
  },
  {
    "currencyName": "Israeli New Sheqel",
    "id": "ILS"
  },
  {
    "currencyName": "Kazakhstani Tenge",
    "id": "KZT"
  },
  {
    "currencyName": "Kuwaiti Dinar",
    "id": "KWD"
  },
  {
    "currencyName": "Lesotho Loti",
    "id": "LSL"
  },
  {
    "currencyName": "Malaysian Ringgit",
    "id": "MYR"
  },
  {
    "currencyName": "Mauritian Rupee",
    "id": "MUR"
  },
  {
    "currencyName": "Mongolian Tugrik",
    "id": "MNT"
  },
  {
    "currencyName": "Myanma Kyat",
    "id": "MMK"
  },
  {
    "currencyName": "Nigerian Naira",
    "id": "NGN"
  },
  {
    "currencyName": "Panamanian Balboa",
    "id": "PAB"
  },
  {
    "currencyName": "Philippine Peso",
    "id": "PHP"
  },
  {
    "currencyName": "Romanian Leu",
    "id": "RON"
  },
  {
    "currencyName": "Saudi Riyal",
    "id": "SAR"
  },
  {
    "currencyName": "Singapore Dollar",
    "id": "SGD"
  },
  {
    "currencyName": "South African Rand",
    "id": "ZAR"
  },
  {
    "currencyName": "Surinamese Dollar",
    "id": "SRD"
  },
  {
    "currencyName": "New Taiwan Dollar",
    "id": "TWD"
  },
  {
    "currencyName": "Paanga",
    "id": "TOP"
  },
  {
    "currencyName": "Venezuelan Bolivar",
    "id": "VEF"
  },
  {
    "currencyName": "Algerian Dinar",
    "id": "DZD"
  },
  {
    "currencyName": "Argentine Peso",
    "id": "ARS"
  },
  {
    "currencyName": "Azerbaijani Manat",
    "id": "AZN"
  },
  {
    "currencyName": "Belarusian Ruble",
    "id": "BYR"
  },
  {
    "currencyName": "Bolivian Boliviano",
    "id": "BOB"
  },
  {
    "currencyName": "Bulgarian Lev",
    "id": "BGN"
  },
  {
    "currencyName": "Canadian Dollar",
    "id": "CAD"
  },
  {
    "currencyName": "Chilean Peso",
    "id": "CLP"
  },
  {
    "currencyName": "Congolese Franc",
    "id": "CDF"
  },
  {
    "currencyName": "Dominican Peso",
    "id": "DOP"
  },
  {
    "currencyName": "Fijian Dollar",
    "id": "FJD"
  },
  {
    "currencyName": "Gambian Dalasi",
    "id": "GMD"
  },
  {
    "currencyName": "Guyanese Dollar",
    "id": "GYD"
  },
  {
    "currencyName": "Icelandic Króna",
    "id": "ISK"
  },
  {
    "currencyName": "Iraqi Dinar",
    "id": "IQD"
  },
  {
    "currencyName": "Japanese Yen",
    "id": "JPY"
  },
  {
    "currencyName": "North Korean Won",
    "id": "KPW"
  },
  {
    "currencyName": "Latvian Lats",
    "id": "LVL"
  },
  {
    "currencyName": "Swiss Franc",
    "id": "CHF"
  },
  {
    "currencyName": "Malagasy Ariary",
    "id": "MGA"
  },
  {
    "currencyName": "Moldovan Leu",
    "id": "MDL"
  },
  {
    "currencyName": "Moroccan Dirham",
    "id": "MAD"
  },
  {
    "currencyName": "Nepalese Rupee",
    "id": "NPR"
  },
  {
    "currencyName": "Nicaraguan Cordoba",
    "id": "NIO"
  },
  {
    "currencyName": "Pakistani Rupee",
    "id": "PKR"
  },
  {
    "currencyName": "Paraguayan Guarani",
    "id": "PYG"
  },
  {
    "currencyName": "Saint Helena Pound",
    "id": "SHP"
  },
  {
    "currencyName": "Seychellois Rupee",
    "id": "SCR"
  },
  {
    "currencyName": "Solomon Islands Dollar",
    "id": "SBD"
  },
  {
    "currencyName": "Sri Lankan Rupee",
    "id": "LKR"
  },
  {
    "currencyName": "Thai Baht",
    "id": "THB"
  },
  {
    "currencyName": "Turkish New Lira",
    "id": "TRY"
  },
  {
    "currencyName": "UAE Dirham",
    "id": "AED"
  },
  {
    "currencyName": "Vanuatu Vatu",
    "id": "VUV"
  },
  {
    "currencyName": "Yemeni Rial",
    "id": "YER"
  },
  {
    "currencyName": "Afghan Afghani",
    "id": "AFN"
  },
  {
    "currencyName": "Bangladeshi Taka",
    "id": "BDT"
  },
  {
    "currencyName": "Brazilian Real",
    "id": "BRL"
  },
  {
    "currencyName": "Cambodian Riel",
    "id": "KHR"
  },
  {
    "currencyName": "Comorian Franc",
    "id": "KMF"
  },
  {
    "currencyName": "Croatian Kuna",
    "id": "HRK"
  },
  {
    "currencyName": "Djiboutian Franc",
    "id": "DJF"
  },
  {
    "currencyName": "Egyptian Pound",
    "id": "EGP"
  },
  {
    "currencyName": "Ethiopian Birr",
    "id": "ETB"
  },
  {
    "currencyName": "CFP Franc",
    "id": "XPF"
  },
  {
    "currencyName": "Ghanaian Cedi",
    "id": "GHS"
  },
  {
    "currencyName": "Guinean Franc",
    "id": "GNF"
  },
  {
    "currencyName": "Hong Kong Dollar",
    "id": "HKD"
  },
  {
    "currencyName": "Special Drawing Rights",
    "id": "XDR"
  },
  {
    "currencyName": "Kenyan Shilling",
    "id": "KES"
  },
  {
    "currencyName": "Kyrgyzstani Som",
    "id": "KGS"
  },
  {
    "currencyName": "Liberian Dollar",
    "id": "LRD"
  },
  {
    "currencyName": "Macanese Pataca",
    "id": "MOP"
  },
  {
    "currencyName": "Maldivian Rufiyaa",
    "id": "MVR"
  },
  {
    "currencyName": "Mexican Peso",
    "id": "MXN"
  },
  {
    "currencyName": "Namibian Dollar",
    "id": "NAD"
  },
  {
    "currencyName": "Norwegian Krone",
    "id": "NOK"
  },
  {
    "currencyName": "Polish Zloty",
    "id": "PLN"
  },
  {
    "currencyName": "Russian Ruble",
    "id": "RUB"
  },
  {
    "currencyName": "Swazi Lilangeni",
    "id": "SZL"
  },
  {
    "currencyName": "Tajikistani Somoni",
    "id": "TJS"
  },
  {
    "currencyName": "Trinidad and Tobago Dollar",
    "id": "TTD"
  },
  {
    "currencyName": "Ugandan Shilling",
    "id": "UGX"
  },
  {
    "currencyName": "Uruguayan Peso",
    "id": "UYU"
  },
  {
    "currencyName": "Vietnamese Dong",
    "id": "VND"
  },
  {
    "currencyName": "Tunisian Dinar",
    "id": "TND"
  },
  {
    "currencyName": "Ukrainian Hryvnia",
    "id": "UAH"
  },
  {
    "currencyName": "Uzbekistani Som",
    "id": "UZS"
  },
  {
    "currencyName": "Turkmenistan Manat",
    "id": "TMT"
  },
  {
    "currencyName": "British Pound",
    "id": "GBP"
  },
  {
    "currencyName": "Zambian Kwacha",
    "id": "ZMW"
  },
  {
    "currencyName": "Bitcoin",
    "id": "BTC"
  },
  {
    "currencyName": "New Belarusian Ruble",
    "id": "BYN"
  },
  {
    "currencyName": "Bermudan Dollar",
    "id": "BMD"
  },
  {
    "currencyName": "Guernsey Pound",
    "id": "GGP"
  },
  {
    "currencyName": "Chilean Unit Of Account",
    "id": "CLF"
  },
  {
    "currencyName": "Cuban Convertible Peso",
    "id": "CUC"
  },
  {
    "currencyName": "Manx pound",
    "id": "IMP"
  },
  {
    "currencyName": "Jersey Pound",
    "id": "JEP"
  },
  {
    "currencyName": "Salvadoran Colón",
    "id": "SVC"
  },
  {
    "currencyName": "Old Zambian Kwacha",
    "id": "ZMK"
  },
  {
    "currencyName": "Silver (troy ounce)",
    "id": "XAG"
  },
  {
    "currencyName": "Zimbabwean Dollar",
    "id": "ZWL"
  }
]
```

Parameter       | Type       | Description
----------------|------------|-------------
currencyName    | String     | Currency name.
id              | String     | Currency ID.
