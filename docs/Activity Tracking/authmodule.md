# Authentication Modules

An authentication module is how a user will be authenticated from your main backend/account service (such as steam).

The default authentication module is steam, the usage is simple, just send a user ticket through as the token for the authenticate player api call.

You can make your own authentication modules and switch them with the environment variables `AUTH_MODULE` and set the value to the class name (including name spaces).

The default steam authentication module is `BOFA.ActivityTracking.AuthenticationModules.SteamAuthentication.SteamAuthentication`

To use the steam authentication module, you need to add the following environment variables:

`STEAM_APIKEY` - Your publisher api key.

`STEAM_APPID` - Your games appid.