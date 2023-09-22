# SpaceTradersApi.AgentsApi

All URIs are relative to *https://api.spacetraders.io/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getAgent**](AgentsApi.md#getAgent) | **GET** /agents/{agentSymbol} | Get Public Agent
[**getAgents**](AgentsApi.md#getAgents) | **GET** /agents | List Agents
[**getMyAgent**](AgentsApi.md#getMyAgent) | **GET** /my/agent | Get Agent

<a name="getAgent"></a>
# **getAgent**
> Object getAgent(agentSymbol)

Get Public Agent

Fetch agent details.

### Example
```javascript
import {SpaceTradersApi} from 'space_traders_api';
let defaultClient = SpaceTradersApi.ApiClient.instance;


let apiInstance = new SpaceTradersApi.AgentsApi();
let agentSymbol = "agentSymbol_example"; // String | The agent symbol

apiInstance.getAgent(agentSymbol, (error, data, response) => {
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
 **agentSymbol** | **String**| The agent symbol | 

### Return type

**Object**

### Authorization

[AgentToken](../README.md#AgentToken)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a name="getAgents"></a>
# **getAgents**
> Object getAgents(opts)

List Agents

Fetch agents details.

### Example
```javascript
import {SpaceTradersApi} from 'space_traders_api';
let defaultClient = SpaceTradersApi.ApiClient.instance;


let apiInstance = new SpaceTradersApi.AgentsApi();
let opts = { 
  'page': 1, // Number | What entry offset to request
  'limit': 10 // Number | How many entries to return per page
};
apiInstance.getAgents(opts, (error, data, response) => {
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

<a name="getMyAgent"></a>
# **getMyAgent**
> Object getMyAgent()

Get Agent

Fetch your agent&#x27;s details.

### Example
```javascript
import {SpaceTradersApi} from 'space_traders_api';
let defaultClient = SpaceTradersApi.ApiClient.instance;


let apiInstance = new SpaceTradersApi.AgentsApi();
apiInstance.getMyAgent((error, data, response) => {
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

