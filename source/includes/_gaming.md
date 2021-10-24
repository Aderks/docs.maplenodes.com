# Gaming Services

Call                                      | Description
------------------------------------------|---------------------------------
[BlackJack](#blackjack)                   | Play a round of BlackJack.
[BlackJackHIT](#blackjackhit)             | Hit on a BlackJack round id.
[BlackJackSTAND](#blackjackstand)         | Stand on a BlackJack round id.





## BlackJack

Play a round of BlackJack. Rounds expire after 30 minutes of no action. Limited to 1000 concurrent rounds. BlackJack splitting is not currently supported.

### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '[]' https://api.maplenodes.com/xrs/BlackJack
```

<code class="api-call">BlackJack</code>

This call does not take parameters.


### Response

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
{
  "dealer": "8,?",
  "player": "10,6 [16]",
  "round_id": "464",
  "action": "HIT or STAND?"
}
```

Parameter       | Type    | Description
----------------|---------|-------------
dealer          | string  | Dealers 1st draw hand.
player          | string  | Players 1st draw hand.
round_id        | int     | The round id.
action          | string  | Action to hit or stand.





## BlackJackHIT

> Sample Data

```cli
{
  "round_id": "298"
}
```
BlackJack hit on the given round id. Hit once or multi-hit until desired player hand.


### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '["464"]' https://api.maplenodes.com/xrs/BlackJackHIT
```

<code class="api-call">BlackJackHIT [round_id]</code>

Parameter       | Type       | Description
----------------|------------|-------------
round_id        | int        | The round id.



### Response Parameters

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
{
  "dealer": "8,3 [11]",
  "player": "10,6,8 [24]",
  "round_id": "464",
  "message": "BUST, you lose!"
}
```

Parameter       | Type    | Description
----------------|---------|-------------
dealer          | string  | Dealers 1st draw hand.
player          | string  | Players current hand.
round_id        | int     | The round id.
action          | string  | Action to HIT or STAND.





## BlackJackSTAND

> Sample Data

```cli
{
  "round_id": "298"
}
```
BlackJack stand on the given round id. Dealer will reveal the hand, and a winner will be declared. Round id is automatically deleted post BlackJack stand.


### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '["256"]' https://api.maplenodes.com/xrs/BlackJackSTAND
```

<code class="api-call">BlackJackSTAND [round_id]</code>

Parameter       | Type       | Description
----------------|------------|-------------
round_id        | int        | The round id.



### Response Parameters

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
{
  "dealer": "A,J [21]",
  "player": "2,5,8 [15]",
  "round_id": "256",
  "message": "You lose!"
}
```

Parameter       | Type    | Description
----------------|---------|-------------
dealer          | string  | Dealers final hand.
player          | string  | Players final hand.
round_id        | int     | The round id.
message         | string  | Winner or loser or tied.
