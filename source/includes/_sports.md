# Sport Services

Call                                                      | Description
----------------------------------------------------------|---------------------------------
[LiveSportsOdds](#livesportsodds)                         | Displays live sports odds data from bookmakers located in the United States, United Kingdom and Australia. Currently only head-to-head (moneyline) data is available.
[LiveSportsOddsList](#livesportsoddslist)                 | Displays a list of sports available to view head-to-head (moneyline) odds.




## LiveSportsOdds

> Sample Data

```cli
{
  "id_key": "americanfootball_nfl",
  "region": "us"
}
```
Displays live sports odds data from bookmakers located in the United States, United Kingdom and Australia. Currently only head-to-head (moneyline) data is available.

**Notes:**

* To view all live games and the next 8 games set [id_key] = upcoming.

* To view an individual sport, retrieve the [id_key] from [LiveSportsOddsList](#livesportsoddslist).

* 3 region bookmakers to choose from:

   * US bookmakers: GTBets, Bovada, Bookmaker, MyBookie.ag, Interops

   * UK bookmakers: Unibet, William Hill, Ladbrokes, Betfair, Bet Victor, Paddy Power, Nordic Bet

   * AU bookmakers: Sportsbet, TAB, BetEasy, Neds, Ladbrokes, Betfair, Unibet

### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '["americanfootball_nfl","us"]' https://api.maplenodes.com/xrs/LiveSportsOdds
```

<code class="api-call">LiveSportsOdds [id_key] [region]</code>

Parameter       | Type       | Description
----------------|------------|-------------
id_key          | string     | ID key of league.
region          | string     | Bookmakers region: `us`, `uk` and `au`.

### Response Parameters

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
[
  {
    "league": "NFL",
    "teams": [
      "Cincinnati Bengals",
      "New York Giants"
    ],
    "home_team": "Cincinnati Bengals",
    "source_site": []
  },
  {
    "league": "NFL",
    "teams": [
      "Baltimore Ravens",
      "New York Giants"
    ],
    "home_team": "Baltimore Ravens",
    "source_site": []
  },
  {
    "league": "NFL",
    "teams": [
      "Cleveland Browns",
      "New York Giants"
    ],
    "home_team": "New York Giants",
    "source_site": []
  },
  {
    "league": "NFL",
    "teams": [
      "New York Giants",
      "Tampa Bay Buccaneers"
    ],
    "home_team": "New York Giants",
    "source_site": []
  },
  {
    "league": "NFL",
    "teams": [
      "Dallas Cowboys",
      "New York Giants"
    ],
    "home_team": "Dallas Cowboys",
    "source_site": []
  },
  {
    "league": "NFL",
    "teams": [
      "New York Giants",
      "Pittsburgh Steelers"
    ],
    "home_team": "New York Giants",
    "source_site": []
  },
  {
    "league": "NFL",
    "teams": [
      "Los Angeles Rams",
      "New York Giants"
    ],
    "home_team": "Los Angeles Rams",
    "source_site": []
  },
  {
    "league": "NFL",
    "teams": [
      "New York Giants",
      "Washington Redskins"
    ],
    "home_team": "Washington Redskins",
    "source_site": []
  },
  {
    "league": "NFL",
    "teams": [
      "Chicago Bears",
      "New York Giants"
    ],
    "home_team": "Chicago Bears",
    "source_site": []
  },
  {
    "league": "NFL",
    "teams": [
      "New York Giants",
      "Seattle Seahawks"
    ],
    "home_team": "Seattle Seahawks",
    "source_site": []
  },
  {
    "league": "NFL",
    "teams": [
      "New York Giants",
      "Philadelphia Eagles"
    ],
    "home_team": "New York Giants",
    "source_site": []
  },
  {
    "league": "NFL",
    "teams": [
      "New York Giants",
      "San Francisco 49ers"
    ],
    "home_team": "New York Giants",
    "source_site": []
  },
  {
    "league": "NFL",
    "teams": [
      "Arizona Cardinals",
      "New York Giants"
    ],
    "home_team": "New York Giants",
    "source_site": []
  },
  {
    "league": "NFL",
    "teams": [
      "Philadelphia Eagles",
      "Pittsburgh Steelers"
    ],
    "home_team": "Pittsburgh Steelers",
    "source_site": []
  },
  {
    "league": "NFL",
    "teams": [
      "Cleveland Browns",
      "Philadelphia Eagles"
    ],
    "home_team": "Cleveland Browns",
    "source_site": []
  },
  {
    "league": "NFL",
    "teams": [
      "Baltimore Ravens",
      "Philadelphia Eagles"
    ],
    "home_team": "Philadelphia Eagles",
    "source_site": []
  },
  {
    "league": "NFL",
    "teams": [
      "New Orleans Saints",
      "Philadelphia Eagles"
    ],
    "home_team": "Philadelphia Eagles",
    "source_site": []
  },
  {
    "league": "NFL",
    "teams": [
      "Dallas Cowboys",
      "Philadelphia Eagles"
    ],
    "home_team": "Dallas Cowboys",
    "source_site": []
  },
  {
    "league": "NFL",
    "teams": [
      "Cincinnati Bengals",
      "Philadelphia Eagles"
    ],
    "home_team": "Philadelphia Eagles",
    "source_site": []
  },
  {
    "league": "NFL",
    "teams": [
      "Arizona Cardinals",
      "Philadelphia Eagles"
    ],
    "home_team": "Arizona Cardinals",
    "source_site": []
  },
  {
    "league": "NFL",
    "teams": [
      "Philadelphia Eagles",
      "Washington Redskins"
    ],
    "home_team": "Washington Redskins",
    "source_site": []
  },
  {
    "league": "NFL",
    "teams": [
      "Green Bay Packers",
      "Philadelphia Eagles"
    ],
    "home_team": "Green Bay Packers",
    "source_site": []
  },
  {
    "league": "NFL",
    "teams": [
      "Philadelphia Eagles",
      "San Francisco 49ers"
    ],
    "home_team": "San Francisco 49ers",
    "source_site": []
  },
  {
    "league": "NFL",
    "teams": [
      "Los Angeles Chargers",
      "New York Jets"
    ],
    "home_team": "Los Angeles Chargers",
    "source_site": []
  },
  {
    "league": "NFL",
    "teams": [
      "Kansas City Chiefs",
      "New York Jets"
    ],
    "home_team": "Kansas City Chiefs",
    "source_site": []
  },
  {
    "league": "NFL",
    "teams": [
      "New York Jets",
      "Seattle Seahawks"
    ],
    "home_team": "Seattle Seahawks",
    "source_site": []
  },
  {
    "league": "NFL",
    "teams": [
      "Philadelphia Eagles",
      "Seattle Seahawks"
    ],
    "home_team": "Philadelphia Eagles",
    "source_site": []
  },
  {
    "league": "NFL",
    "teams": [
      "Los Angeles Rams",
      "Philadelphia Eagles"
    ],
    "home_team": "Philadelphia Eagles",
    "source_site": []
  },
  {
    "league": "NFL",
    "teams": [
      "Denver Broncos",
      "New York Jets"
    ],
    "home_team": "New York Jets",
    "source_site": []
  },
  {
    "league": "NFL",
    "teams": [
      "Arizona Cardinals",
      "New York Jets"
    ],
    "home_team": "New York Jets",
    "source_site": []
  },
  {
    "league": "NFL",
    "teams": [
      "Cleveland Browns",
      "New York Jets"
    ],
    "home_team": "New York Jets",
    "source_site": []
  },
  {
    "league": "NFL",
    "teams": [
      "New England Patriots",
      "New York Jets"
    ],
    "home_team": "New England Patriots",
    "source_site": []
  },
  {
    "league": "NFL",
    "teams": [
      "New York Jets",
      "San Francisco 49ers"
    ],
    "home_team": "New York Jets",
    "source_site": []
  },
  {
    "league": "NFL",
    "teams": [
      "Miami Dolphins",
      "New York Jets"
    ],
    "home_team": "Miami Dolphins",
    "source_site": []
  },
  {
    "league": "NFL",
    "teams": [
      "Buffalo Bills",
      "New York Jets"
    ],
    "home_team": "Buffalo Bills",
    "source_site": []
  },
  {
    "league": "NFL",
    "teams": [
      "Indianapolis Colts",
      "New York Jets"
    ],
    "home_team": "Indianapolis Colts",
    "source_site": []
  },
  {
    "league": "NFL",
    "teams": [
      "Los Angeles Rams",
      "New York Jets"
    ],
    "home_team": "Los Angeles Rams",
    "source_site": []
  },
  {
    "league": "NFL",
    "teams": [
      "Kansas City Chiefs",
      "Tampa Bay Buccaneers"
    ],
    "home_team": "Tampa Bay Buccaneers",
    "source_site": []
  },
  {
    "league": "NFL",
    "teams": [
      "Carolina Panthers",
      "Tampa Bay Buccaneers"
    ],
    "home_team": "Tampa Bay Buccaneers",
    "source_site": []
  },
  {
    "league": "NFL",
    "teams": [
      "Green Bay Packers",
      "Tampa Bay Buccaneers"
    ],
    "home_team": "Tampa Bay Buccaneers",
    "source_site": []
  },
  {
    "league": "NFL",
    "teams": [
      "Atlanta Falcons",
      "Tampa Bay Buccaneers"
    ],
    "home_team": "Tampa Bay Buccaneers",
    "source_site": []
  },
  {
    "league": "NFL",
    "teams": [
      "Los Angeles Rams",
      "Tampa Bay Buccaneers"
    ],
    "home_team": "Tampa Bay Buccaneers",
    "source_site": []
  },
  {
    "league": "NFL",
    "teams": [
      "Minnesota Vikings",
      "Tampa Bay Buccaneers"
    ],
    "home_team": "Tampa Bay Buccaneers",
    "source_site": []
  },
  {
    "league": "NFL",
    "teams": [
      "Los Angeles Chargers",
      "Tampa Bay Buccaneers"
    ],
    "home_team": "Tampa Bay Buccaneers",
    "source_site": []
  },
  {
    "league": "NFL",
    "teams": [
      "New Orleans Saints",
      "Tampa Bay Buccaneers"
    ],
    "home_team": "Tampa Bay Buccaneers",
    "source_site": []
  },
  {
    "league": "NFL",
    "teams": [
      "San Francisco 49ers",
      "Seattle Seahawks"
    ],
    "home_team": "San Francisco 49ers",
    "source_site": []
  },
  {
    "league": "NFL",
    "teams": [
      "New England Patriots",
      "Seattle Seahawks"
    ],
    "home_team": "Seattle Seahawks",
    "source_site": []
  },
  {
    "league": "NFL",
    "teams": [
      "Chicago Bears",
      "Detroit Lions"
    ],
    "home_team": "Chicago Bears",
    "source_site": []
  },
  {
    "league": "NFL",
    "teams": [
      "Chicago Bears",
      "Minnesota Vikings"
    ],
    "home_team": "Chicago Bears",
    "source_site": []
  },
  {
    "league": "NFL",
    "teams": [
      "Indianapolis Colts",
      "Tennessee Titans"
    ],
    "home_team": "Indianapolis Colts",
    "source_site": []
  },
  {
    "league": "NFL",
    "teams": [
      "Houston Texans",
      "Indianapolis Colts"
    ],
    "home_team": "Indianapolis Colts",
    "source_site": []
  },
  {
    "league": "NFL",
    "teams": [
      "Indianapolis Colts",
      "Jacksonville Jaguars"
    ],
    "home_team": "Indianapolis Colts",
    "source_site": []
  },
  {
    "league": "NFL",
    "teams": [
      "Chicago Bears",
      "Green Bay Packers"
    ],
    "home_team": "Chicago Bears",
    "source_site": []
  },
  {
    "league": "NFL",
    "teams": [
      "Cleveland Browns",
      "Pittsburgh Steelers"
    ],
    "home_team": "Pittsburgh Steelers",
    "source_site": []
  },
  {
    "league": "NFL",
    "teams": [
      "Cincinnati Bengals",
      "Pittsburgh Steelers"
    ],
    "home_team": "Pittsburgh Steelers",
    "source_site": []
  },
  {
    "league": "NFL",
    "teams": [
      "Baltimore Ravens",
      "Pittsburgh Steelers"
    ],
    "home_team": "Pittsburgh Steelers",
    "source_site": []
  }
]
```

Parameter       | Type       | Description
----------------|------------|-------------
league          | string     | Professional league.
teams           | array      | Teams playing against each other.
home_team       | string     | Team playing at home.
source_site     | array      | Bookmakers data.
site_key        | string     | Bookmaker.
site_nice       | string     | Bookmaker.
last_updated    | string     | Timestamp of last updated odds.
odds            | array      | Array of sporting odds data.
h2h             | array      | Array of h2h odds data.
h2h_lay         | array      | Array of h2h_lay odds data.





## LiveSportsOddsList

> Sample Data

```cli
{
  "view_all": 0
}
```
Displays a list of sports available to view head-to-head (moneyline) odds.


### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '["0"]' https://api.maplenodes.com/xrs/LiveSportsOddsList
```

<code class="api-call">LiveSportsOddsList [view_all]</code>

Parameter       | Type       | Description
----------------|------------|-------------
view_all        | int        | `0` = in-season only, `1` = in & off-season


### Response Parameters

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
[
  {
    "league": "NCAAF",
    "in_season": true,
    "id_key": "americanfootball_ncaaf"
  },
  {
    "league": "NFL",
    "in_season": true,
    "id_key": "americanfootball_nfl"
  },
  {
    "league": "AFL",
    "in_season": false,
    "id_key": "aussierules_afl"
  },
  {
    "league": "MLB",
    "in_season": false,
    "id_key": "baseball_mlb"
  },
  {
    "league": "Basketball Euroleague",
    "in_season": false,
    "id_key": "basketball_euroleague"
  },
  {
    "league": "NBA",
    "in_season": false,
    "id_key": "basketball_nba"
  },
  {
    "league": "NCAAB",
    "in_season": false,
    "id_key": "basketball_ncaab"
  },
  {
    "league": "Asia Cup",
    "in_season": false,
    "id_key": "cricket_asia_cup"
  },
  {
    "league": "Big Bash",
    "in_season": false,
    "id_key": "cricket_big_bash"
  },
  {
    "league": "ICC Champions",
    "in_season": false,
    "id_key": "cricket_icc_trophy"
  },
  {
    "league": "ICC World Cup",
    "in_season": false,
    "id_key": "cricket_icc_world_cup"
  },
  {
    "league": "IPL",
    "in_season": false,
    "id_key": "cricket_ipl"
  },
  {
    "league": "IPL T20",
    "in_season": false,
    "id_key": "cricket_ipl_t20"
  },
  {
    "league": "One Day Internationals",
    "in_season": false,
    "id_key": "cricket_odi"
  },
  {
    "league": "Natwest T20 Blast",
    "in_season": false,
    "id_key": "cricket_t20_natwest"
  },
  {
    "league": "Test Matches",
    "in_season": false,
    "id_key": "cricket_test_match"
  },
  {
    "league": "League of Legends",
    "in_season": false,
    "id_key": "esports_lol"
  },
  {
    "league": "NHL",
    "in_season": false,
    "id_key": "icehockey_nhl"
  },
  {
    "league": "MMA",
    "in_season": true,
    "id_key": "mma_mixed_martial_arts"
  },
  {
    "league": "NRL",
    "in_season": false,
    "id_key": "rugbyleague_nrl"
  },
  {
    "league": "State of Origin",
    "in_season": false,
    "id_key": "rugbyleague_nrl_state_of_origin"
  },
  {
    "league": "World Cup",
    "in_season": false,
    "id_key": "rugbyleague_world_cup"
  },
  {
    "league": "Aviva Premiership",
    "in_season": false,
    "id_key": "rugbyunion_aviva_premiership"
  },
  {
    "league": "Premiership Rugby",
    "in_season": false,
    "id_key": "rugbyunion_premiership_rugby"
  },
  {
    "league": "Six Nations",
    "in_season": false,
    "id_key": "rugbyunion_six_nations"
  },
  {
    "league": "Super Rugby",
    "in_season": false,
    "id_key": "rugbyunion_super_rugby"
  },
  {
    "league": "Sydney 7s",
    "in_season": false,
    "id_key": "rugbyunion_sydney_7s"
  },
  {
    "league": "Primera División - Argentina",
    "in_season": false,
    "id_key": "soccer_argentina_primera_division"
  },
  {
    "league": "A-League",
    "in_season": false,
    "id_key": "soccer_australia_aleague"
  },
  {
    "league": "Belgium First Div",
    "in_season": false,
    "id_key": "soccer_belgium_first_div"
  },
  {
    "league": "Brazil Série A",
    "in_season": false,
    "id_key": "soccer_brazil_campeonato"
  },
  {
    "league": "Super League - China",
    "in_season": false,
    "id_key": "soccer_china_superleague"
  },
  {
    "league": "Denmark Superliga",
    "in_season": false,
    "id_key": "soccer_denmark_superliga"
  },
  {
    "league": "Championship",
    "in_season": false,
    "id_key": "soccer_efl_champ"
  },
  {
    "league": "League 1",
    "in_season": false,
    "id_key": "soccer_england_league1"
  },
  {
    "league": "League 2",
    "in_season": false,
    "id_key": "soccer_england_league2"
  },
  {
    "league": "EPL",
    "in_season": false,
    "id_key": "soccer_epl"
  },
  {
    "league": "FA Cup",
    "in_season": false,
    "id_key": "soccer_fa_cup"
  },
  {
    "league": "World Cup",
    "in_season": false,
    "id_key": "soccer_fifa_world_cup"
  },
  {
    "league": "Veikkausliiga - Finland",
    "in_season": false,
    "id_key": "soccer_finland_veikkausliiga"
  },
  {
    "league": "Ligue 1 - France",
    "in_season": false,
    "id_key": "soccer_france_ligue_one"
  },
  {
    "league": "Ligue 2 - France",
    "in_season": false,
    "id_key": "soccer_france_ligue_two"
  },
  {
    "league": "Bundesliga - Germany",
    "in_season": false,
    "id_key": "soccer_germany_bundesliga"
  },
  {
    "league": "Bundesliga 2 - Germany",
    "in_season": false,
    "id_key": "soccer_germany_bundesliga2"
  },
  {
    "league": "Int. Friendlies",
    "in_season": false,
    "id_key": "soccer_int_friendlies"
  },
  {
    "league": "Inter. Champs Cup",
    "in_season": false,
    "id_key": "soccer_inter_champs_cup"
  },
  {
    "league": "Serie A - Italy",
    "in_season": false,
    "id_key": "soccer_italy_serie_a"
  },
  {
    "league": "Serie B - Italy",
    "in_season": false,
    "id_key": "soccer_italy_serie_b"
  },
  {
    "league": "J League",
    "in_season": false,
    "id_key": "soccer_japan_j_league"
  },
  {
    "league": "K League 1",
    "in_season": true,
    "id_key": "soccer_korea_kleague1"
  },
  {
    "league": "League of Ireland",
    "in_season": false,
    "id_key": "soccer_league_of_ireland"
  },
  {
    "league": "Liga MX",
    "in_season": false,
    "id_key": "soccer_mexico_ligamx"
  },
  {
    "league": "Dutch Eredivisie",
    "in_season": false,
    "id_key": "soccer_netherlands_eredivisie"
  },
  {
    "league": "Eliteserien - Norway",
    "in_season": false,
    "id_key": "soccer_norway_eliteserien"
  },
  {
    "league": "Primeira Liga - Portugal",
    "in_season": false,
    "id_key": "soccer_portugal_primeira_liga"
  },
  {
    "league": "Premier League - Russia",
    "in_season": false,
    "id_key": "soccer_russia_premier_league"
  },
  {
    "league": "La Liga - Spain",
    "in_season": false,
    "id_key": "soccer_spain_la_liga"
  },
  {
    "league": "La Liga 2 - Spain",
    "in_season": false,
    "id_key": "soccer_spain_segunda_division"
  },
  {
    "league": "SPL",
    "in_season": false,
    "id_key": "soccer_spl"
  },
  {
    "league": "Allsvenskan - Sweden",
    "in_season": false,
    "id_key": "soccer_sweden_allsvenskan"
  },
  {
    "league": "Superettan - Sweden",
    "in_season": false,
    "id_key": "soccer_sweden_superettan"
  },
  {
    "league": "Swiss Superleague",
    "in_season": false,
    "id_key": "soccer_switzerland_superleague"
  },
  {
    "league": "Turkey Super League",
    "in_season": false,
    "id_key": "soccer_turkey_super_league"
  },
  {
    "league": "UEFA Champions",
    "in_season": false,
    "id_key": "soccer_uefa_champs_league"
  },
  {
    "league": "UEFA Europa",
    "in_season": false,
    "id_key": "soccer_uefa_europa_league"
  },
  {
    "league": "MLS",
    "in_season": false,
    "id_key": "soccer_usa_mls"
  }
]
```

Parameter       | Type       | Description
----------------|------------|-------------
league          | string     | Professional league.
in_season       | bool       | `true` if in season, other `false`.
id_key          | string     | ID key for league.
