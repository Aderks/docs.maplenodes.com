# The Graph

Call                                                      | Description
----------------------------------------------------------|---------------------------------
[ENS](#ens)                                               | View ENS name of The Graph Indexers.
[indexer](#indexer)                                       | View The Graph Indexer metrics.
[indexers](#indexers)                                     | View list of indexers on The Graph network.
[IPFS](#ipfs)                                             | Converts subgraph ID to IPFS hash.
[network](#network)                                       | View The Graph network information.


## ENS

> Sample Data

```shell
{
  "indexer_address": "0xbfe2a198cb0cdfb50fb03cd932c7387ddb0d25aa"
}
```

View ENS name of The Graph Indexers.



### Request Parameters

> Sample Request

```shell
curl -X GET https://api.maplenodes.com/graph/ens/0xbfe2a198cb0cdfb50fb03cd932c7387ddb0d25aa
```


<code class="api-call">/graph/ens/[indexer_address]</code>

Parameter          | Type       | Description
-------------------|------------|-------------
indexer_address    | string     | The Graph Indexer address.


### Response Parameters

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
{
  "indexer": "0xbfe2a198cb0cdfb50fb03cd932c7387ddb0d25aa",
  "indexer_ens": "maplenodes",
  "beneficiary_address": "0xebc391ba182f6d8654a516a44e382cf9c9196831"
}
```


Parameter            | Type          | Description
---------------------|---------------|-------------
indexer              | string        | Address of Indexer.
indexer_ens          | string        | ENS name of Indexer, empty if not set.
beneficiary_address  | string        | Beneficiary address of Indexer.





## Indexer

> Sample Data

```shell
{
  "indexer_address": "0xbfe2a198cb0cdfb50fb03cd932c7387ddb0d25aa"
}
```
View The Graph Indexer metrics.



### Request Parameters

> Sample Request

```shell
curl -X GET https://api.maplenodes.com/graph/indexer/0xbfe2a198cb0cdfb50fb03cd932c7387ddb0d25aa
```

<code class="api-call">/graph/indexer/[indexer_address]</code>

Parameter          | Type       | Description
-------------------|------------|-------------
indexer_address    | string     | The Graph Indexer address.


### Response Parameters

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
{
  "indexer": "0xbfe2a198cb0cdfb50fb03cd932c7387ddb0d25aa",
  "indexer_name": "maplenodes",
  "total_allowable_stake": 3097775.1,
  "total_allowable_stake_usd": 6350438.95,
  "total_allocated_stake": 3098227.38,
  "total_allocated_stake_usd": 6351366.13,
  "allocation_difference": -452.28,
  "allocation_difference_usd": -927.17,
  "allocation_percent": 100.01,
  "time_last_allocation": "Wed Mar 31 05:04:38 UTC 2021",
  "time_lapsed_last_allocation": "15d 22h 4m 9s ago",
  "time_lapsed_last_allocation_raw": 1617167078,
  "time_last_parameter_change": "Tue Dec 22 19:12:15 UTC 2020",
  "time_lapsed_last_parameter_change": "114d 7h 56m 32s ago",
  "time_cooldown_remaining": "0d 0h 0m 0s",
  "pending_rewards": 14692.1,
  "pending_rewards_usd": 30118.8,
  "pending_rewards_hourly": 38.45,
  "pending_rewards_hourly_usd": 78.82,
  "pending_rewards_indexer": 13222.89,
  "pending_rewards_indexer_usd": 27106.92,
  "pending_rewards_indexer_hourly": 34.61,
  "pending_rewards_indexer_hourly_usd": 70.95,
  "pending_rewards_delegator": 1469.21,
  "pending_rewards_delegator_usd": 3011.88,
  "pending_rewards_delegator_hourly": 3.85,
  "pending_rewards_delegator_hourly_usd": 7.89,
  "total_query_rebates": 69.55,
  "total_query_rebates_usd": 142.58,
  "indexer_stake": 2080659.78,
  "indexer_stake_usd": 4265352.55,
  "indexer_reward_cut": 90,
  "indexer_rewards": 212042.01,
  "indexer_rewards_usd": 434686.12,
  "indexer_reward_effective_cut": 69.54,
  "indexer_query_cut": 80,
  "indexer_query_fees": 244.33,
  "indexer_query_fees_usd": 500.88,
  "indexer_query_rebates": 55.64,
  "indexer_query_rebates_usd": 114.06,
  "total_delegated": 1017115.32,
  "total_delegated_usd": 2085086.41,
  "delegator_reward_cut": 10,
  "delegator_rewards": 23560.22,
  "delegator_rewards_usd": 48298.45,
  "delegator_query_cut": 20,
  "delegator_query_fees": 13.91,
  "delegator_query_fees_usd": 28.52,
  "total_rewards": 235602.24,
  "total_rewards_usd": 482984.59,
  "grt_usd": 2.05
}
```


Parameter                              | Type          | Description
---------------------------------------|---------------|-------------
indexer                                | string        | Address of Indexer.
indexer_name                           | string        | ENS name of Indexer, empty if not set.
total_allowable_stake                  | int           | Total GRT allowed to be allocated.
total_allowable_stake_usd              | int           | Value ($USD) of total GRT allowed to be allocated.
total_allocated_stake                  | int           | Total GRT currently in allocation.
total_allocated_stake_usd              | int           | Value ($USD) of the total GRT currently in allocation.
allocation_difference                  | int           | Difference of total allowable GRT vs allocated GRT.
allocation_difference_usd              | int           | Value ($USD) of the allocation difference.
allocation_percent                     | int           | Allocated GRT vs Allowable GRT (%).  
time_last_allocation                   | string        | Timestamp (UTC) of last allocation.
time_lapsed_last_allocation            | string        | Time that has elapsed since last allocation.
time_lapsed_last_allocation_raw        | int           | Unix time (seconds) since last allocation.
time_last_parameter_change             | string        | Timestamp (UTC) of last parameter change.
time_lapsed_last_parameter_change      | string        | The time that has elapsed since last parameter change.
time_cooldown_remaining                | string        | Time remaining before Indexer is allowed to change parameters again.
pending_rewards                        | int           | Total GRT the Indexer has accrued in their current open allocation.
pending_rewards_usd                    | int           | Value ($USD) of the total pending rewards.
pending_rewards_hourly                 | int           | Total pending reward rate (GRT/hr).
pending_rewards_hourly_usd             | int           | Total pending reward rate ($USD/hr).
pending_rewards_indexer                | int           | Amount of accrued GRT that is awarded to the Indexer.
pending_rewards_indexer_usd            | int           | Value ($USD) of Indexer's pending rewards.
pending_rewards_indexer_hourly         | int           | Indexer pending reward rate (GRT/hr).
pending_rewards_indexer_hourly_usd     | int           | Indexer pending reward rate ($USD/hr).
pending_rewards_delegator              | int           | Amount of accrued GRT that is awarded to the Delegator.
pending_rewards_delegator_usd          | int           | Value ($USD) of Delegator's pending rewards.
pending_rewards_delegator_hourly       | int           | Delegator pending reward rate (GRT/hr).
pending_rewards_delegator_hourly_usd   | int           | Delegator pending reward rate ($USD/hr).
total_query_rebates                    | int           | Total GRT query fees rewarded to Indexer & Delegator. 
total_query_rebates_usd                | int           | Value ($USD) total GRT query fees.
indexer_stake                          | int           | Total GRT the Indexer is staking.
indexer_stake_usd                      | int           | Value ($USD) of Indexer's total stake.
indexer_reward_cut                     | int           | Indexer's reward cut (%).
indexer_rewards                        | int           | Total amount of GRT the Indexer has been rewarded.
indexer_rewards_usd                    | int           | Value ($USD) of Indexer's total rewards.
indexer_reward_effective_cut           | int           | Indexer's rewards effective cut (%).
indexer_query_cut                      | int           | Indexer's query fees cut (%).
indexer_query_fees                     | int           | Total GRT query fees. 
indexer_query_fees_usd                 | int           | Value ($USD) of total query fees.
indexer_query_rebates                  | int           | Total GRT query fee rebates rewarded to the Indexer.
indexer_query_rebates_usd              | int           | Value ($USD) of Indexer query fee rebates.
total_delegated"                       | int           | Total GRT delegated to the Indexer.
total_delegated_usd                    | int           | Value ($USD) of total delegations.
delegator_reward_cut                   | int           | Delegator's reward cut (%).
delegator_rewards                      | int           | Total amount of GRT Delegator's have been rewarded.
delegator_rewards_usd                  | int           | Value ($USD) of Delegator's total rewards.
delegator_query_cut                    | int           | Delegator's query fees cut (%).
delegator_query_fees                   | int           | Total GRT query fee rebates rewarded to Delegator's.
delegator_query_fees_usd               | int           | Value ($USD) of Delegator query fee rebates.
total_rewards                          | int           | Total GRT rewards for this Indexer.
total_rewards_usd                      | int           | Value ($USD) of total rewards for this Indexer.
grt_usd                                | int           | $USD value of 1 GRT.





## Indexers

View list of indexers on The Graph network.

### Request Parameters

> Sample Request

```shell
curl -X GET https://api.maplenodes.com/graph/indexers/
```

<code class="api-call">/graph/indexers/</code>

This call does not take parameters.


### Response

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
[
  {
    "indexer": "0x011bdfea664ece919d895d174f57331460056236",
    "indexer_name": "stakingcapital2"
  },
  {
    "indexer": "0x025fe57b265ed74d3ef915297ba5b9b4f2a8474e",
    "indexer_name": "glad"
  },
  {
    "indexer": "0x0280464494b1c4ffd18a89ec3b3703fbc28b7b6d",
    "indexer_name": ""
  },
  {
    "indexer": "0x039b47ea916783f78d943d94de700a17f40ae6d4",
    "indexer_name": "dokiacapital"
  },
  {
    "indexer": "0x03db85e86779febdd96d96ba43ac48382fb1a88d",
    "indexer_name": "chainlayer"
  },
  {
    "indexer": "0x040a8ae130b5fbac973074aa1bd2c69773c5fbc2",
    "indexer_name": "inflex"
  },
  {
    "indexer": "0x06590a641dc3eb43f2cebe435576389f209116da",
    "indexer_name": ""
  },
  {
    "indexer": "0x07051463ca2414f716d37da8cdbcdb5abe4cc239",
    "indexer_name": "allyoucanstake"
  },
  {
    "indexer": "0x0b751463e07d90f465573d3b5dd45e1afafd4cd0",
    "indexer_name": "index-africa"
  },
  {
    "indexer": "0x0ceb7aa784616f4cd5d581ed5d1182bc4340b460",
    "indexer_name": ""
  },
  {
    "indexer": "0x0da2b8ead0975f707aa3bad4c1ae4e705e4b3b53",
    "indexer_name": ""
  },
  {
    "indexer": "0x147e0980483f71a235521335a3ef79338ca11d28",
    "indexer_name": ""
  },
  {
    "indexer": "0x15184aed586140527593b32db21bfbb5b53a02c6",
    "indexer_name": ""
  },
  {
    "indexer": "0x163a2ebf98ef202da5834a33f7ce98098a0b7874",
    "indexer_name": "lexprime"
  },
  {
    "indexer": "0x1692a8710dcf0dce24bd34c028479176b97ee9ef",
    "indexer_name": "stake-machine"
  },
  {
    "indexer": "0x17d7dca770ef183355b202435e1ce80a11b53886",
    "indexer_name": ""
  },
  {
    "indexer": "0x1873a56a404b21df3c69c0c105dd65b4e43d88e6",
    "indexer_name": ""
  },
  {
    "indexer": "0x19755b22a68bb72e649f8faafdbb549ed3ea75d2",
    "indexer_name": ""
  },
  {
    "indexer": "0x19fbac0891042be71ce60321a17720358575f580",
    "indexer_name": "stakeservice"
  },
  {
    "indexer": "0x1a6a74648ff8146f9b7df3a7e322506612e13e6a",
    "indexer_name": "easy2stake-com"
  },
  {
    "indexer": "0x1a99dd7d916117a523f3ce6510dcfd6bceab11e7",
    "indexer_name": "p-ops"
  },
  {
    "indexer": "0x1b536a13d1a18eb51bb216cf69aa89fcd0b1badc",
    "indexer_name": ""
  },
  {
    "indexer": "0x1c96a40b413fe428cb86729ebe8c38f559ee7202",
    "indexer_name": ""
  },
  {
    "indexer": "0x24a17f3ce0b06d8da3d058dec91e36bb867cbe65",
    "indexer_name": "stakingcapital3"
  },
  {
    "indexer": "0x27ac40b9198659ce99eef1890d853a40560c9425",
    "indexer_name": ""
  },
  {
    "indexer": "0x27ca9cf008a217e828b4b39945034ff8450730d1",
    "indexer_name": "alphavirtual"
  },
  {
    "indexer": "0x2890d1b13894258ab3d477729d62d52b43754f9b",
    "indexer_name": ""
  },
  {
    "indexer": "0x289d2026a6a09c20261303775b9fca9494e7ab1f",
    "indexer_name": ""
  },
  {
    "indexer": "0x293d739d1a683b3943f14ef55b1b0efc06b9be54",
    "indexer_name": ""
  },
  {
    "indexer": "0x2c313e9fd1794685d2052af79457c858813b108f",
    "indexer_name": ""
  },
  {
    "indexer": "0x2d042d8a78cdaaa674b0aec5538e66a620eef75f",
    "indexer_name": ""
  },
  {
    "indexer": "0x31ebc9f2fff890d84133cb86491942dc8fa70c5e",
    "indexer_name": ""
  },
  {
    "indexer": "0x3217b1a2129941669ffb1aa9f962dc8a686ffd47",
    "indexer_name": ""
  },
  {
    "indexer": "0x34cadf09dbf50a39d1a68b87d7763db3961ef483",
    "indexer_name": ""
  },
  {
    "indexer": "0x34f38671e9ffb8464a268752680444feb8139feb",
    "indexer_name": "rampdefi"
  },
  {
    "indexer": "0x3622522a5eb9bba3417ec3d2a437f9d3c5caacee",
    "indexer_name": ""
  },
  {
    "indexer": "0x362717d3fa1bfe457535b9b716f450b95a858217",
    "indexer_name": ""
  },
  {
    "indexer": "0x365507a4eef5341cf00340f702f7f6e74217d96e",
    "indexer_name": "graphops"
  },
  {
    "indexer": "0x371be11579c15a0a81b50e06087f363b27e14c36",
    "indexer_name": "rampdefi3"
  },
  {
    "indexer": "0x371bff423d9cd52abc79959a52dd8a5ee7216112",
    "indexer_name": ""
  },
  {
    "indexer": "0x38e6b1dc04087f69e69f10d7318643accc9854f5",
    "indexer_name": ""
  },
  {
    "indexer": "0x39839abed87475422c5353256d17e08395c3af6b",
    "indexer_name": "liray-indexer"
  },
  {
    "indexer": "0x399235a909238c4e7915e7ce8a5f2898456fd313",
    "indexer_name": ""
  },
  {
    "indexer": "0x3eb3297b0e34a7897aa004b66a354053425f7894",
    "indexer_name": "chainodetech"
  },
  {
    "indexer": "0x4140d3d0086fce37ebadd965dff88e12cf78b1fb",
    "indexer_name": ""
  },
  {
    "indexer": "0x4167eb613d784c910f5dc0f3f0515d61ec6ec8df",
    "indexer_name": "suntzu-indexer"
  },
  {
    "indexer": "0x41cf9718b66761d121b407f2a139b4f5b22fc9cd",
    "indexer_name": ""
  },
  {
    "indexer": "0x427f071e335bfa32241bbfa7f240f24a8a46f292",
    "indexer_name": "mind-heart-soul"
  },
  {
    "indexer": "0x43d1f66f18ea1c5ad98dc4a059502663987be19b",
    "indexer_name": ""
  },
  {
    "indexer": "0x43eb454e8715164bd41deddaec3d3e2a7fbcd7b4",
    "indexer_name": ""
  },
  {
    "indexer": "0x4437e367cc68d87675148a9e4a1f052f0359c880",
    "indexer_name": "mind-heart-soul"
  },
  {
    "indexer": "0x453b5e165cf98ff60167ccd3560ebf8d436ca86c",
    "indexer_name": ""
  },
  {
    "indexer": "0x45874192929530cd4e3dd0624df05bee3c13974f",
    "indexer_name": "grassets-tech-1"
  },
  {
    "indexer": "0x4595855ed2d498fc2cbd7f415e7f262e2328d950",
    "indexer_name": ""
  },
  {
    "indexer": "0x45ac0ac13cb89e285282b1034e6eedcffb42cc2d",
    "indexer_name": ""
  },
  {
    "indexer": "0x474e571ab6dd77489ec3c7ddf9cbc893fcba684c",
    "indexer_name": ""
  },
  {
    "indexer": "0x48b5687f0595e2a4d581dc72305fbae214345d07",
    "indexer_name": ""
  },
  {
    "indexer": "0x48eecbc147a4b97e30fd03ef738b9305812e0287",
    "indexer_name": ""
  },
  {
    "indexer": "0x4955ec78868e90572c7d315a3c22238451fb7923",
    "indexer_name": "rampdefi4"
  },
  {
    "indexer": "0x49bc9eccd93cbfa6b76dcf33b3ba9a36aab05b36",
    "indexer_name": ""
  },
  {
    "indexer": "0x4ac761592d1f948058843121133d048dc7dfc7c0",
    "indexer_name": ""
  },
  {
    "indexer": "0x4b1c684dc4ad3c77cbaae5f16051c269b79116d2",
    "indexer_name": ""
  },
  {
    "indexer": "0x4bbae81dc703e33cb290c069afac427d96aba895",
    "indexer_name": "rampdefi2"
  },
  {
    "indexer": "0x4bbfbd1320093858d877ab0c8cd91ef0ce065318",
    "indexer_name": "alphavirtual"
  },
  {
    "indexer": "0x4bc2e066fb0857493a1fbe48462bb34ff6ea731f",
    "indexer_name": "dappquery"
  },
  {
    "indexer": "0x4bd07ae84869eaf4413c1a9873a534109f40cc3a",
    "indexer_name": ""
  },
  {
    "indexer": "0x4c059ccb00e504b4472f8fbb0d2556f165bdbb3b",
    "indexer_name": ""
  },
  {
    "indexer": "0x4d6a8776a164776c93618233a0003e8894e7e6c2",
    "indexer_name": "stakedus"
  },
  {
    "indexer": "0x4d7fdee1f02b7864658d7bc8c650b8901d033b9f",
    "indexer_name": ""
  },
  {
    "indexer": "0x4dc44f5906f593da2ac28be1d22c4ee9cd556420",
    "indexer_name": ""
  },
  {
    "indexer": "0x4fedde33607cfda2c82a999accb427d1170987d9",
    "indexer_name": "oraclegen"
  },
  {
    "indexer": "0x50a786a68320fcfb276ef196dee6f4cdae53440e",
    "indexer_name": "stakesystems"
  },
  {
    "indexer": "0x50fda0a43d6770a927ebe2909fce1cdcba417801",
    "indexer_name": "masternode24-de"
  },
  {
    "indexer": "0x532433d8f9ead9a35b10929d024b4cccb8c12321",
    "indexer_name": "lowfeevalidation"
  },
  {
    "indexer": "0x55f3dcdaf0b73f7f0c761a9070d8865f37986e2c",
    "indexer_name": "makingcash-hosted-by-ryabina"
  },
  {
    "indexer": "0x57c6ca1effe6c676d93225a122f41eb24708edd9",
    "indexer_name": ""
  },
  {
    "indexer": "0x5a8904be09625965d9aec4bffd30d853438a053e",
    "indexer_name": "p2p-org"
  },
  {
    "indexer": "0x5ea935a6164629dd9c0f7f1e3b79c2d041108e26",
    "indexer_name": ""
  },
  {
    "indexer": "0x60165e465b242d051de4ebadfe0cf55b13f04dc5",
    "indexer_name": ""
  },
  {
    "indexer": "0x6125ea331851367716bee301ecde7f38a7e429e7",
    "indexer_name": "figment-prime-2"
  },
  {
    "indexer": "0x61590afb7e2c612ef8c441356ee82db8cd90a5d6",
    "indexer_name": ""
  },
  {
    "indexer": "0x62a0bd1d110ff4e5b793119e95fc07c9d1fc8c4a",
    "indexer_name": "nuviba"
  },
  {
    "indexer": "0x632484e0411a40ca7f2552defb70605ec3e58676",
    "indexer_name": ""
  },
  {
    "indexer": "0x63c560997b8338f2b033f3ffdcc0f7c680feec45",
    "indexer_name": "inflex"
  },
  {
    "indexer": "0x643c5f5223ba68e06766b194b274c4d90dd42dc8",
    "indexer_name": ""
  },
  {
    "indexer": "0x66578a314303c4547f6b72ecf21ccb449879be32",
    "indexer_name": ""
  },
  {
    "indexer": "0x671bc7a0ffa02b0ee90ee03bcd11915df011503a",
    "indexer_name": "nodehodler-com"
  },
  {
    "indexer": "0x6879bbfcff0e54e62b899681ea52e74bd9b29fe4",
    "indexer_name": ""
  },
  {
    "indexer": "0x696569606ed7e07a3a5f0720f2ece96a79135762",
    "indexer_name": "stakesquid-3"
  },
  {
    "indexer": "0x6980fd6c85a98df8180123951e46d673b456699c",
    "indexer_name": ""
  },
  {
    "indexer": "0x6ac85b9d834b51b14a7b0ed849bb5199e04c05c5",
    "indexer_name": "figment-prime"
  },
  {
    "indexer": "0x6dae84e4aed2c8708707b358e278408c2deb0397",
    "indexer_name": "agenetwork"
  },
  {
    "indexer": "0x7030613f84334149c3d1324497c96062c01e8459",
    "indexer_name": "kytzu"
  },
  {
    "indexer": "0x720a98087160bfdb282f695abe6f9ac966b03d43",
    "indexer_name": "grassets-tech-2"
  },
  {
    "indexer": "0x72acbecf3013d7b27421185d3bf369520bf552c8",
    "indexer_name": ""
  },
  {
    "indexer": "0x75555d4115fe3b00a90811822ff77b9f97121be2",
    "indexer_name": ""
  },
  {
    "indexer": "0x75a77853c1bf2490bc39c737581c18ca1dd13231",
    "indexer_name": ""
  },
  {
    "indexer": "0x7697a886fc3b71a8a88487019337a6bbe5838f1a",
    "indexer_name": ""
  },
  {
    "indexer": "0x76e84025978a0c16fc7ba483718b667388f2973c",
    "indexer_name": "minatofund"
  },
  {
    "indexer": "0x79c813f6b6a84b4ab7258db617612f06bde25498",
    "indexer_name": "01node-indexer"
  },
  {
    "indexer": "0x7a1247bb8d8d139c0859b439eb44f8480c8ffdc5",
    "indexer_name": ""
  },
  {
    "indexer": "0x7ab4cf25330ed7277ac7ab59380b68eea68abb0e",
    "indexer_name": "stakingfacilities"
  },
  {
    "indexer": "0x7b8f93130b7c610fb102f1e82e23ad978ed81702",
    "indexer_name": ""
  },
  {
    "indexer": "0x7ca0ee4a792f4da7b6aaf4c082b234259de61112",
    "indexer_name": "chainflow-indexer"
  },
  {
    "indexer": "0x7ddf0c8cb0167870bf7cc5368792c93aeeb15430",
    "indexer_name": ""
  },
  {
    "indexer": "0x7ed9d36539f349808c42187ed4e1753d5947db7a",
    "indexer_name": "kukis-global"
  },
  {
    "indexer": "0x7fa7d0212ac64b48efaf62055b9d2d274d14403f",
    "indexer_name": ""
  },
  {
    "indexer": "0x7fd833cf8775e9c3524b8be925723345164964be",
    "indexer_name": "lunanova"
  },
  {
    "indexer": "0x7fd9cada29b91bad49e49481c0288ba045cf8713",
    "indexer_name": ""
  },
  {
    "indexer": "0x81dd719fd7efb19d12740b8057c0e363bee35b4a",
    "indexer_name": "bestake"
  },
  {
    "indexer": "0x8211c6b4c8dc1c252fccab001ec78af87cad87ed",
    "indexer_name": ""
  },
  {
    "indexer": "0x83e1a1853079524443742089d8a4e02470e76250",
    "indexer_name": ""
  },
  {
    "indexer": "0x85fe868adf7f5950b052469075556fb207e5372d",
    "indexer_name": "framework-labs"
  },
  {
    "indexer": "0x88b2e385e95ffcd7ae07629a18d95b7711f4166a",
    "indexer_name": ""
  },
  {
    "indexer": "0x8a1729fe84c53c231c7ae53a5bec3f6e9953cb4b",
    "indexer_name": "graph-node-1-cp0x-hosted-by-ryabina"
  },
  {
    "indexer": "0x8b7663dd451c951f39e541188d9f7d9419e94421",
    "indexer_name": "iukni"
  },
  {
    "indexer": "0x8d632dfc2454d624910fe982e85a5b15d2ae93c5",
    "indexer_name": ""
  },
  {
    "indexer": "0x8e297141f9dc76f4d71741da1a1e47294cf0fde2",
    "indexer_name": "fattox"
  },
  {
    "indexer": "0x8ed9245a00d1f1edc664f32c33c3115f5b2c9a90",
    "indexer_name": ""
  },
  {
    "indexer": "0x8f9793029b66325b70fffbfdf2b04d8491682466",
    "indexer_name": ""
  },
  {
    "indexer": "0x901073d364f6af645648dc81d7f90e7aab47142d",
    "indexer_name": ""
  },
  {
    "indexer": "0x914cefe3b3e68cdf813c4b947ce2db76c28c2287",
    "indexer_name": ""
  },
  {
    "indexer": "0x9154937dc144c87020a7974fbe9b0aa17b69cdfd",
    "indexer_name": ""
  },
  {
    "indexer": "0x9238584c74e5fa445a8f72a4d4ef4699dd783852",
    "indexer_name": "ryabina"
  },
  {
    "indexer": "0x9498abb64b27d1aac5206c09c0eacb445d992e4c",
    "indexer_name": ""
  },
  {
    "indexer": "0x978cd3207d0cf5a89003d85c2913bc9be120c31f",
    "indexer_name": ""
  },
  {
    "indexer": "0x97a13b2969dc8268a24b7997ed64ab8339631cf4",
    "indexer_name": ""
  },
  {
    "indexer": "0x9b1da82ee4d269eeeb4977e092b9ad2d7970c096",
    "indexer_name": ""
  },
  {
    "indexer": "0x9b7d53ac71f04867b80a97dcd919e1235dc6f398",
    "indexer_name": ""
  },
  {
    "indexer": "0x9f491ce41ffa24a074176106ed9c59b0ae504427",
    "indexer_name": ""
  },
  {
    "indexer": "0xa2c46e4fa487f954632e34d479c6047a8214f49d",
    "indexer_name": ""
  },
  {
    "indexer": "0xa3276e7ab0a162f6a3b5aa6b3089accbaa65d12e",
    "indexer_name": ""
  },
  {
    "indexer": "0xa3eb195c91c428d48c7ce24301f0dfbaf972b5d7",
    "indexer_name": ""
  },
  {
    "indexer": "0xa543abe0ea61b4bbbca3f402442bda4bf7d45992",
    "indexer_name": "swiftstaking"
  },
  {
    "indexer": "0xa92bd8c16ae3266cf3b80ba0152735e9a8460ce7",
    "indexer_name": ""
  },
  {
    "indexer": "0xa959b5afe73c6faa803541b5c4edc0492dfda294",
    "indexer_name": ""
  },
  {
    "indexer": "0xaa3b07b1251d7961baf3ce05b101b82bd0ebf8d5",
    "indexer_name": "nebulas-nova"
  },
  {
    "indexer": "0xab55c2d923549317bf7ed7b9f74271e4a1b9ed8f",
    "indexer_name": ""
  },
  {
    "indexer": "0xac104dba73822c575713e1ecb06da67af01c54b3",
    "indexer_name": ""
  },
  {
    "indexer": "0xac8c69428414206b220a5ed20b351e385605b9ff",
    "indexer_name": "intrepido"
  },
  {
    "indexer": "0xaf96dd8fbc94d207bb91181e1e92f34d14f8aea5",
    "indexer_name": ""
  },
  {
    "indexer": "0xb06071394531b63b0bac78f27e12dc2beaa913e4",
    "indexer_name": "protofire"
  },
  {
    "indexer": "0xb393ff3cd1f70fecf9cf8b67f27780fbea0d084f",
    "indexer_name": "joystick"
  },
  {
    "indexer": "0xb3e2fe4e6673709613c22c63d3d7326f3bfa15cc",
    "indexer_name": "stakesystems"
  },
  {
    "indexer": "0xb438830f11820a5e9cdde1363bc49bde2da67f1f",
    "indexer_name": "gunray"
  },
  {
    "indexer": "0xb8f0f81df338338a2672f58e90c2f4b5e45ffacc",
    "indexer_name": ""
  },
  {
    "indexer": "0xbaf3c5958f0c073feb9312816edca59fe070a2d7",
    "indexer_name": ""
  },
  {
    "indexer": "0xbb784d9b398271b7a64f975bebde869409691915",
    "indexer_name": "graph-node-1-cp0x-hosted-by-ryabina"
  },
  {
    "indexer": "0xbbf36ec9311d60513c09f952d7530c2ff37e86b4",
    "indexer_name": ""
  },
  {
    "indexer": "0xbd1a939b4e4125254013a0c4573252be2fd9d207",
    "indexer_name": ""
  },
  {
    "indexer": "0xbe013243e22a9a9752a53f232b2fc7907a5d35ae",
    "indexer_name": ""
  },
  {
    "indexer": "0xbe9d7c691792937ca7e2535652886ff390cc5b86",
    "indexer_name": "lexprime"
  },
  {
    "indexer": "0xbf4af02f7855c7ead52d037349b7a76e48ed47a9",
    "indexer_name": "waynewayner"
  },
  {
    "indexer": "0xbfe2a198cb0cdfb50fb03cd932c7387ddb0d25aa",
    "indexer_name": "maplenodes"
  },
  {
    "indexer": "0xc36157756ea4838cf882edab9dd94325c38f2edc",
    "indexer_name": ""
  },
  {
    "indexer": "0xc430be492ddeb6e761dbbd0e08bafe99f5064d90",
    "indexer_name": "wavefive"
  },
  {
    "indexer": "0xc60d0c8c74b5d3a33ed51c007ebae682490de261",
    "indexer_name": "figment-lemniscap"
  },
  {
    "indexer": "0xc9348dcaef652791033a22f79a2024363e23d32b",
    "indexer_name": ""
  },
  {
    "indexer": "0xc94a2669f719f792f166800fb6ef00fb3a7f5bec",
    "indexer_name": ""
  },
  {
    "indexer": "0xc9899dfdca2b2ef3972ce25e3f1ba0b05cb457b6",
    "indexer_name": ""
  },
  {
    "indexer": "0xcb22a8ce581d04fef99b81ec5a60725070a3e8c4",
    "indexer_name": "legiojuve"
  },
  {
    "indexer": "0xcba3cbd284108e1ad5942e0a6b2c75a030a9d379",
    "indexer_name": ""
  },
  {
    "indexer": "0xcc49c102b09addf780816b9989d95c873032cf88",
    "indexer_name": ""
  },
  {
    "indexer": "0xcd09fc5fc328dfeb2792248b03fee9a0c0b216aa",
    "indexer_name": ""
  },
  {
    "indexer": "0xce9df315e4780fed7894bcbcbfe2e34f0f804df1",
    "indexer_name": ""
  },
  {
    "indexer": "0xd11e05240a50e2eedb03e72d4c9c6465bc05f2a4",
    "indexer_name": "bitnordic"
  },
  {
    "indexer": "0xd11eb5db7cfbb9ecae4b62e71ec0a461f6baf669",
    "indexer_name": ""
  },
  {
    "indexer": "0xd133fd8e0607f5d82c91626140495ea0a31d0398",
    "indexer_name": ""
  },
  {
    "indexer": "0xd22c1c1a1fc452e3312489f1e89676e93c3323f0",
    "indexer_name": "stakesquid-3"
  },
  {
    "indexer": "0xd3a3fa4b73e5007a8adef6ccdfc8d05c06a76035",
    "indexer_name": ""
  },
  {
    "indexer": "0xd7205e8054a6778e383d9afde80fd702db41c7fd",
    "indexer_name": "inotel"
  },
  {
    "indexer": "0xd8410a44041e0a8e758e496113dfb42bef4ed3bc",
    "indexer_name": "hashquark-indexer"
  },
  {
    "indexer": "0xd8f20ebdc2568bc404c66e3745b2050c392022fc",
    "indexer_name": ""
  },
  {
    "indexer": "0xd93456bf656436e66a8e0a8835c43a6f59afbb37",
    "indexer_name": ""
  },
  {
    "indexer": "0xd9c7cdf09d868467d9f94f885dd68e850e278118",
    "indexer_name": "cryptosniffers"
  },
  {
    "indexer": "0xdc81f90ccdd72ce4239d741a7ed9c16006dce73b",
    "indexer_name": ""
  },
  {
    "indexer": "0xddc39dceb6d8fb94d8a9b59cf3bf9a1e7ae19034",
    "indexer_name": "moonlime"
  },
  {
    "indexer": "0xe06899d681922247973437540323d384ae4b3928",
    "indexer_name": ""
  },
  {
    "indexer": "0xe0c1af3235ecee2c085ead8e918cd394986d2303",
    "indexer_name": ""
  },
  {
    "indexer": "0xe183718f4a2a8cfc7fde85dc0a36cf64e5657a14",
    "indexer_name": ""
  },
  {
    "indexer": "0xe2571c87f1433ea06be389e427af2a17bfd37fc0",
    "indexer_name": ""
  },
  {
    "indexer": "0xe6368e677871b288294536c8fe6cb1bbeb19f7a2",
    "indexer_name": ""
  },
  {
    "indexer": "0xe758697c5fc77f6b64bcf54191c08ad051bbdc4b",
    "indexer_name": ""
  },
  {
    "indexer": "0xe7738d5679b54781a5482baa48dadfde624ed7d5",
    "indexer_name": ""
  },
  {
    "indexer": "0xe7a694696a4d11ac0b7ab2dcb99a7fcf200eb00b",
    "indexer_name": "4block-team"
  },
  {
    "indexer": "0xe8832ba6aaf83d80d9e7578415e97576093f4d9f",
    "indexer_name": ""
  },
  {
    "indexer": "0xe995eff16391a874ebe815e4f017b034e673d930",
    "indexer_name": ""
  },
  {
    "indexer": "0xeb8ca82006e0c0fb16cf9fc42e15bf3e9cdf73f9",
    "indexer_name": ""
  },
  {
    "indexer": "0xed093fca388c1fc8ccc77c512ed167b2684e7966",
    "indexer_name": ""
  },
  {
    "indexer": "0xefd8cd2688e270ba60719762d2cc1e6c2e616a2c",
    "indexer_name": "syncnode-indexer"
  },
  {
    "indexer": "0xf304928be241aaa4d3bc6b95328300b5691aab9e",
    "indexer_name": "glad"
  },
  {
    "indexer": "0xf3f182e859f789af8d6c2223d15c691471c79a2b",
    "indexer_name": "blocksteady"
  },
  {
    "indexer": "0xf44964c13b8345302d4a9dfa329c6a002cfc0daf",
    "indexer_name": ""
  },
  {
    "indexer": "0xf4a097ce3a4efbd1748b2ef2076813961e4e6fa7",
    "indexer_name": ""
  },
  {
    "indexer": "0xf4e5f4e0f8ec4d6235bd2fb0443058584ebffbff",
    "indexer_name": "stakingcapital"
  },
  {
    "indexer": "0xf62de2a9d8b8033a5b66f497dca1bd91080316fb",
    "indexer_name": "elerium115"
  },
  {
    "indexer": "0xf7a36339f75ffaf058be67fd2a1764fb84eb5d87",
    "indexer_name": "delegatorsclub"
  },
  {
    "indexer": "0xf8ea1030a4fbc2c55bee9b297492888633947b4d",
    "indexer_name": ""
  },
  {
    "indexer": "0xfb5b40098cdfec1564ae5b94d4deed116b887d08",
    "indexer_name": ""
  },
  {
    "indexer": "0xfc34b8b6ae8fc85a11fcac84fe0713407e23ac0d",
    "indexer_name": ""
  },
  {
    "indexer": "0xfd12a5a7bc7f2eb4904a8177418dbb0bf094ba16",
    "indexer_name": "chorusone"
  },
  {
    "indexer": "0xfd4b9c44ee7afb7f98df3dda40aead6acd9f41f4",
    "indexer_name": ""
  }
]
```


Parameter     | Type          | Description
--------------|---------------|-------------
indexers      | Array         | List of all indexers on the mainnet network.
indexer       | string        | Address of Indexer.
indexer_name  | string        | ENS name of Indexer.





## IPFS

> Sample Data

```shell
{
  "subgraph_id": "0x4a008334f8e7ea21be223d15462084f51abcc0e6625f61de806b8456e67e603e"
}
```

Converts subgraph ID to IPFS hash.



### Request Parameters

> Sample Request

```shell
curl -X GET https://api.maplenodes.com/graph/IPFS/0x4a008334f8e7ea21be223d15462084f51abcc0e6625f61de806b8456e67e603e
```


<code class="api-call">/graph/IPFS/[subgraph_id]</code>

Parameter          | Type       | Description
-------------------|------------|-------------
subgraph_id        | string     | Subgraph ID to convert to a IPFS hash.


### Response Parameters

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
{
  "ipfs_hash":"QmTKXLEdMD6Vq7Nwxo8XAfnHpG6H1TzL1AGwiqLpoae3Pb"
}
```


Parameter            | Type          | Description
---------------------|---------------|-------------
ipfs_hash            | string        | IPFS hash of subgraph ID.






## Network

View The Graph network information.

### Request Parameters

> Sample Request

```shell
curl -X GET https://api.maplenodes.com/graph/network
```

<code class="api-call">/graph/network</code>

This call does not take parameters.


### Response

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
{
  "total_supply": 10077060371.81,
  "indexer_stake": 693995498.73,
  "allocated_stake": 2690702861.08
}
```


Parameter       | Type          | Description
----------------|---------------|-------------
total_supply    | int           | Graph token supply.
indexer_stake   | int           | Total amount of GRT staked in the staking contract.
allocated_stake | int           | Total GRT currently in allocation.