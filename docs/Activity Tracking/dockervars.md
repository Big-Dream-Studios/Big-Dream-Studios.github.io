# Docker Environment Variables

To make it easier for auto deployments, BOFA.ActivityTracking uses environment variables for the configuration.

Here are the environment variables for the redis connection:
### Required
`REDIS_HOST` [string] - The remote endpoint for the redis database.

`REDIS_PORT` [int] - The port for the redis database.

`REDIS_PASSWORD` [string] - The password used for the redis database.

`AUTH_KEY` [string] - The key used to validate a user based on their ticket.

### Optional
`REDIS_SSL` [bool] (Default: true) - Enables SSL communication to your redis database.

`REDIS_ALLOWADMIN` [bool] (Default: true) - Enables admin usage of the redis database.

`REDIS_CONNECTTIMEOUT` [int] (Default: 6000) - The time in miliseconds before timing out.

`REDIS_DATABASE` [int] (Default: 0) - The (sub)database to use on the redis database.

`REDIS_CONNECTRETRY` [int] (Default: 2) - The amount of times to attempt to connect.