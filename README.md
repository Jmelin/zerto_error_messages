# zerto_error_messages

Blob updated as of 10/24/2019.


All Zerto error messages in a json blob for an easy search and easy return of more info about the error message. 

Sometimes Zerto error messages need a little help.

## Use case
If you are using the Zerto v1 api and you hit the `/v1/alerts/` endpoint, It will return information and include a Help Identifier like:
```
"HelpIdentifier": "ZVM0003"
```

The given alert description from the api doesn't give you all that much.

So you can parse the json blob to get more info about the error. `Alert Name`, `Severity`, and `AlertDescription` or more information.
```
 "ZVM0003": {
      "Alert Name": "No connection to site",
      "Severity": "Error",
      "Alert Description": "The connection between the local Zerto Virtual Manager and the remote Zerto Virtual Manager is down."
}
```

Very useful when automating alert notifications from the api.
