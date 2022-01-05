# REST Endpoints

The endpoints for the player activity tracking library are:

--------------

* GET `/api/PingActivity/{accountID}/{ticket}`

 - This will ping the api to know the player is still online, this should be called every 60s or less from the client.

Possible Results:

`Not Found` (404) - User is not in the redis database, reauthenticate them.

`Unauthorized` (401) - The ticket does not match the one in the redis database, reauthenticate or close game.

`Ok` (200) - Success.

--------------

* GET `/api/QueueCasual/{accountID}/{ticket}`

 - This will ping the api to know the player is wanting to enter the casual matchmaking queue.

Possible Results:

`Unauthorized` (401) - The ticket does not match the one in the redis database, reauthenticate or close game.

`Ok` (200) - Success.

--------------

* GET `/api/DequeueCasual/{accountID}/{ticket}`

 - This will ping the api to know the player is wanting to leave the casual matchmaking queue.

Possible Results:

`Unauthorized` (401) - The ticket does not match the one in the redis database, reauthenticate or close game.

`Ok` (200) - Success.

--------------

* GET `/api/AuthenticatePlayer/{accountID}/{token}`

 - This will attempt to authenticate a player and mark them as online.

Possible Results:

`Unauthorized` (401) - The token is not accepted, try again.

`Ok` (200) - Success, also returns their ticket for use with pinging as a string.

--------------

* GET `/api/ValidateTicket/{accountID}/{ticket}/{authkey}`

 - This is used by dedicated servers to validate that a user is who they say they are.

Possible Results:

`Unauthorized` (401) - The token is not accepted or auth key doesnt match, remove the user.

`NotFound` (404) - User account not found as online.

`Ok` (200) - Success, also returns "OK".

--------------

* GET `/api/MatchEnded/{serverName}/{authkey}`

 - This is used by dedicated servers to let the backend know that this server has ended its match.

Possible Results:

`Unauthorized` (401) - The token is not accepted or auth key doesnt match.

`NotFound` (404) - Server not found as online.

`Ok` (200) - Success, also returns "OK".