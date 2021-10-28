# Models

## ** GameServerAllocationResult **

| Variable         | Data Type                             | Description                                                  |
| ---------------- | ------------------------------------- | ------------------------------------------------------------ |
| `kind`           | string                                | The kind of request                                          |
| `apiVersion`     | string                                | The API version                                              |
| `metadata`       | GameServerAllocationResultMetadata    | Extra Metadata                                               |
| `status`         | GameServerAllocationResultStatus      | The status of the gameserver along with ip/port              |


## ** GameServerAllocationResultMetadata **

| Variable              | Data Type                             | Description                         |
| --------------------- | ------------------------------------- | ----------------------------------- |
| `name`                | string                                | The name of the gameserver pod      |
| `nameSpace`           | string                                | The namespace of the pod            |
| `creationTimestamp`   | DateTime                              | The gameserver creation time        |


## ** GameServerAllocationResultStatus **

| Variable              | Data Type                             | Description                                  |
| --------------------- | ------------------------------------- | -------------------------------------------- |
| `state`               | string                                | The state of the game server                 |
| `gameServerName`      | string                                | The name of the gameserver pod               |
| `ports`               | GameServerAllocationResultPort[]      | The gameserver ports                         |
| `address`             | string                                | The gameserver node IP                       |
| `nodeName`            | string                                | The name of the node the game server is on   |


## ** GameServerAllocationResultPort **

| Variable    | Data Type    | Description                                  |
| ----------- | ------------ | -------------------------- |
| `name`      | string       | The name of the port type  |
| `port`      | ushort       | The port                   |