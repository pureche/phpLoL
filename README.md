phpLoL
========================
phpLoL is a library to access League of Legends statistics via php

Requirements
------------------------
* [composer](https://github.com/composer/composer)

Installation
------------------------

###Standalone use:
1. `git clone https://github.com/zlokomatic/phpLoL.git`
2. composer install 

###As dependency:
1. create a composer.json and define this dependencies.

    ```json
    {
        "repositories": [
            {
                "type": "git",
                "url": "https://github.com/zlokomatic/phpLoL.git"
            },
            {
                "type": "git",
                "url": "https://github.com/zlokomatic/SabreAMF.git"
            }
        ],
        "require": {
            "zlokomatic/phpLoL": "*"
        },
        "minimum-stability": "dev"
    }
    ```
2. composer install


Getting started
------------------------

### LoLConfig.php
change

        private $clientVersion = ""
    
to current client Version (e.g. 3.11.13_09_13_11_54)
 

### Functions
Avaiable functions are:

* getSummonerByName($name)
* getAllPublicSummonerDataByAccount($accountid)
* getSummonerNames(array $accountIds)
* getRecentGames($accountId)
* getPlayerStatsByAccountId($accountId)
* getAggregatedStats($accountId, $gameMode, $season)
    * Available gameModes
        * CLASSIC
        * ODIN
        * ARAM
        * TUTORIAL
    * Available timelines
      * 1 
      * 2 
      * 3
* getAllLeaguesForPlayer($summonerId)
 
 News
------------------------

   1. Made project composer compliant
   2. Small example to show how a way how to stay connected: https://github.com/zlokomatic/phpLoL-tcp


Credit
------------------------
* lolrtmpsclient
* SabreAMF
