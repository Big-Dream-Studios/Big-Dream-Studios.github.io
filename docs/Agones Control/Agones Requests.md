# Agones Requests

There are two methods in the AgonesRequests class, along with initializing.

To create an instance of the AgonesRequests class you will need to pass the endpoint and your token from k8s config.

## ** Ping(Async) **

* `BOFA.AgonesControl.AgonesRequests.Ping()`

- Optionally has an async version.

This will return a bool of wheater or not you are able to ping the k8s cluster.

-----------------

## ** AllocateServer(Async) **

* `BOFA.AgonesControl.AgonesRequests.AllocateServer(string allocationRequest)`

- Optionally has an async version.

Requires a json-format allocation request, typically they are basic and just look like: `{\"apiVersion\":\"allocation.agones.dev/v1\",\"kind\":\"GameServerAllocation\",\"spec\":{\"required\":{\"matchLabels\":{\"agones.dev/fleet\":\"zs-server\"}}}}`

Returns a `GameServerAllocationResult` or null depending on if it was successful.