# SpaceTradersApi.SystemsApi

All URIs are relative to *https://api.spacetraders.io/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getJumpGate**](SystemsApi.md#getJumpGate) | **GET** /systems/{systemSymbol}/waypoints/{waypointSymbol}/jump-gate | Get Jump Gate
[**getMarket**](SystemsApi.md#getMarket) | **GET** /systems/{systemSymbol}/waypoints/{waypointSymbol}/market | Get Market
[**getShipyard**](SystemsApi.md#getShipyard) | **GET** /systems/{systemSymbol}/waypoints/{waypointSymbol}/shipyard | Get Shipyard
[**getSystem**](SystemsApi.md#getSystem) | **GET** /systems/{systemSymbol} | Get System
[**getSystemWaypoints**](SystemsApi.md#getSystemWaypoints) | **GET** /systems/{systemSymbol}/waypoints | List Waypoints in System
[**getSystems**](SystemsApi.md#getSystems) | **GET** /systems | List Systems
[**getWaypoint**](SystemsApi.md#getWaypoint) | **GET** /systems/{systemSymbol}/waypoints/{waypointSymbol} | Get Waypoint

<a name="getJumpGate"></a>
# **getJumpGate**
> Object getJumpGate()

Get Jump Gate

Get jump gate details for a waypoint. Requires a waypoint of type &#x60;JUMP_GATE&#x60; to use.  The response will return all systems that are have a Jump Gate in range of this Jump Gate. Those systems can be jumped to from this Jump Gate.

### Example
```javascript
import {SpaceTradersApi} from 'space_traders_api';
let defaultClient = SpaceTradersApi.ApiClient.instance;


let apiInstance = new SpaceTradersApi.SystemsApi();
apiInstance.getJumpGate((error, data, response) => {
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

<a name="getMarket"></a>
# **getMarket**
> Object getMarket()

Get Market

Retrieve imports, exports and exchange data from a marketplace. Requires a waypoint that has the &#x60;Marketplace&#x60; trait to use.  Send a ship to the waypoint to access trade good prices and recent transactions. Refer to the [Market Overview page](https://docs.spacetraders.io/game-concepts/markets) to gain better a understanding of the market in the game.

### Example
```javascript
import {SpaceTradersApi} from 'space_traders_api';
let defaultClient = SpaceTradersApi.ApiClient.instance;


let apiInstance = new SpaceTradersApi.SystemsApi();
apiInstance.getMarket((error, data, response) => {
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

<a name="getShipyard"></a>
# **getShipyard**
> Object getShipyard()

Get Shipyard

Get the shipyard for a waypoint. Requires a waypoint that has the &#x60;Shipyard&#x60; trait to use. Send a ship to the waypoint to access data on ships that are currently available for purchase and recent transactions.

### Example
```javascript
import {SpaceTradersApi} from 'space_traders_api';
let defaultClient = SpaceTradersApi.ApiClient.instance;


let apiInstance = new SpaceTradersApi.SystemsApi();
apiInstance.getShipyard((error, data, response) => {
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

<a name="getSystem"></a>
# **getSystem**
> Object getSystem()

Get System

Get the details of a system.

### Example
```javascript
import {SpaceTradersApi} from 'space_traders_api';
let defaultClient = SpaceTradersApi.ApiClient.instance;


let apiInstance = new SpaceTradersApi.SystemsApi();
apiInstance.getSystem((error, data, response) => {
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

<a name="getSystemWaypoints"></a>
# **getSystemWaypoints**
> Object getSystemWaypoints(systemSymbol, opts)

List Waypoints in System

Return a paginated list of all of the waypoints for a given system.  If a waypoint is uncharted, it will return the &#x60;Uncharted&#x60; trait instead of its actual traits.

### Example
```javascript
import {SpaceTradersApi} from 'space_traders_api';
let defaultClient = SpaceTradersApi.ApiClient.instance;


let apiInstance = new SpaceTradersApi.SystemsApi();
let systemSymbol = "systemSymbol_example"; // String | The system symbol
let opts = { 
  'page': 1, // Number | What entry offset to request
  'limit': 10 // Number | How many entries to return per page
};
apiInstance.getSystemWaypoints(systemSymbol, opts, (error, data, response) => {
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
 **systemSymbol** | **String**| The system symbol | 
 **page** | **Number**| What entry offset to request | [optional] [default to 1]
 **limit** | **Number**| How many entries to return per page | [optional] [default to 10]

### Return type

**Object**

### Authorization

[AgentToken](../README.md#AgentToken)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a name="getSystems"></a>
# **getSystems**
> Object getSystems(opts)

List Systems

Return a paginated list of all systems.

### Example
```javascript
import {SpaceTradersApi} from 'space_traders_api';
let defaultClient = SpaceTradersApi.ApiClient.instance;


let apiInstance = new SpaceTradersApi.SystemsApi();
let opts = { 
  'page': 1, // Number | What entry offset to request
  'limit': 10 // Number | How many entries to return per page
};
apiInstance.getSystems(opts, (error, data, response) => {
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

<a name="getWaypoint"></a>
# **getWaypoint**
> Object getWaypoint()

Get Waypoint

View the details of a waypoint.  If the waypoint is uncharted, it will return the &#x27;Uncharted&#x27; trait instead of its actual traits.

### Example
```javascript
import {SpaceTradersApi} from 'space_traders_api';
let defaultClient = SpaceTradersApi.ApiClient.instance;


let apiInstance = new SpaceTradersApi.SystemsApi();
apiInstance.getWaypoint((error, data, response) => {
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

