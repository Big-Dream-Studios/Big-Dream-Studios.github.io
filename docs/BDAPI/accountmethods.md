# Account Endpoints

The following are the endpoints for accessing account information of a user.


## ** Get Full Profile **

* GET `/GetUserInformation`

Requires SAT: False

Headers:

| Variable                               | Data Type   |
| -------------------------------------- | ----------- |
| `BDID`                                 | ?string     |
| `SID`                                  | ?uint64     |

This method will return a full user object (in json) from either the BDID or SID. Leave one null and use the other.
If account is null, it will return blank JSON object.

-----------------

## ** Authenticate Steam User **

* GET `/AuthenticateSteamUser`

Requires SAT: False

Headers:

| Variable                               | Data Type   |
| -------------------------------------- | ----------- |
| `Ticket`                               | string      |

This method will return a BDID or nothing if it failed/ticket is invalid. 

This method is used by every server (offical, and unoffical) and used to authenticate users.
If the user does not exsist in the backend, it will create a new one and return the BDID of the new user.

-----------------

## ** Give Species **

* GET `/UnlockSpecies`

Requires SAT: true

Headers:

| Variable                               | Data Type   |
| -------------------------------------- | ----------- |
| `SID`                                  | uint64      |
| `Species`                              | int         |

This method will give the user the species passed in by the header.

-----------------

## ** Increment Kills **

* GET `/IncrementKills`

Requires SAT: true

Headers:

| Variable                               | Data Type   |
| -------------------------------------- | ----------- |
| `SID`                                  | uint64      |
| `Kills`                                | int         |

This method will increase the kill amount on the users profile, based on the amount of kills passed in.

-----------------

## ** Increment Deaths **

* GET `/IncrementDeaths`

Requires SAT: true

Headers:

| Variable                               | Data Type   |
| -------------------------------------- | ----------- |
| `SID`                                  | uint64      |
| `Deaths`                               | int         |

This method will increase the death amount on the users profile, based on the amount of deaths passed in.

-----------------

## ** Increment Wins **

* GET `/IncrementWins`

Requires SAT: true

Headers:

| Variable                               | Data Type   |
| -------------------------------------- | ----------- |
| `SID`                                  | uint64      |
| `Wins`                                 | int         |

This method will increase the win amount on the users profile, based on the amount of wins passed in.

-----------------

## ** Increment Loses **

* GET `/IncrementLoses`

Requires SAT: true

Headers:

| Variable                               | Data Type   |
| -------------------------------------- | ----------- |
| `SID`                                  | uint64      |
| `Loses`                                | int         |

This method will increase the loses amount on the users profile, based on the amount of loses passed in.

-----------------

## ** Increment Damage **

* GET `/IncrementDamage`

Requires SAT: true

Headers:

| Variable                               | Data Type   |
| -------------------------------------- | ----------- |
| `SID`                                  | uint64      |
| `Damage`                               | int         |

This method will increase the damage amount on the users profile, based on the amount of damage passed in.
