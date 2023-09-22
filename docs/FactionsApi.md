# SpaceTradersApi.FactionsApi

All URIs are relative to *https://api.spacetraders.io/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getFaction**](FactionsApi.md#getFaction) | **GET** /factions/{factionSymbol} | Get Faction
[**getFactions**](FactionsApi.md#getFactions) | **GET** /factions | List Factions

<a name="getFaction"></a>
# **getFaction**
> Object getFaction()

Get Faction

View the details of a faction.

### Example
```javascript
import {SpaceTradersApi} from 'space_traders_api';
let defaultClient = SpaceTradersApi.ApiClient.instance;


let apiInstance = new SpaceTradersApi.FactionsApi();
apiInstance.getFaction((error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters
This endpoint does not need any parameter.

### Return type

**Object**

### Authorization

[AgentToken](../README.md#AgentToken)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a name="getFactions"></a>
# **getFactions**
> Object getFactions(opts)

List Factions

Return a paginated list of all the factions in the game.

### Example
```javascript
import {SpaceTradersApi} from 'space_traders_api';
let defaultClient = SpaceTradersApi.ApiClient.instance;


let apiInstance = new SpaceTradersApi.FactionsApi();
let opts = { 
  'page': 1, // Number | What entry offset to request
  'limit': 10 // Number | How many entries to return per page
};
apiInstance.getFactions(opts, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **Number**| What entry offset to request | [optional] [default to 1]
 **limit** | **Number**| How many entries to return per page | [optional] [default to 10]

### Return type

**Object**

### Authorization

[AgentToken](../README.md#AgentToken)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

