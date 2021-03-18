# User Accounts

User accounts are whats stored in the BDAPI, they contain all the variables for what consists of a user.

!!! warning "Special Exceptions"
    Anything that starts with a question mark, such as `?string`, has the possibility of being null. Make sure your system is capable of handling those cases.


| Variable                               | Data Type   | Description                                                  |
| -------------------------------------- | ----------- | ------------------------------------------------------------ |
| `BDID`                                 | string      | The backend identifier for the user.                         |
| `Username`                             | string      | The cached username for the user.                            |
| `Unlocked Species`                     | int[]       | An array of unlocked species for the user. (More info soon.) |
| `SID`                                  | ?uint64     | The steamID of the user.                                     |
| `Creation Date`                        | int64       | C# DateTime binary format of the account creation date.      |
| `Active Boosts`                        | int         | Combination of the currently active boosts.                  |
| `Saved Boosts`                         | int[]       | Array of saved boosts. (More info soon.)                     |
| `Wins`                                 | uint64      | The users all time wins.                                     |
| `Loses`                                | uint64      | The users all time loses.                                    |
| `Kills`                                | uint64      | The users all time kills.                                    |
| `Deaths`                               | uint64      | The users all time deaths.                                   |
| `TotalDamage`                          | uint64      | The users all time damage dealt.                             |
| `Last Write Time`                      | int64       | C# DateTime binary format of the last SAT write to account.  |
