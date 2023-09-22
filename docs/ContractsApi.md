# SpaceTradersApi.ContractsApi

All URIs are relative to *https://api.spacetraders.io/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**acceptContract**](ContractsApi.md#acceptContract) | **POST** /my/contracts/{contractId}/accept | Accept Contract
[**deliverContract**](ContractsApi.md#deliverContract) | **POST** /my/contracts/{contractId}/deliver | Deliver Cargo to Contract
[**fulfillContract**](ContractsApi.md#fulfillContract) | **POST** /my/contracts/{contractId}/fulfill | Fulfill Contract
[**getContract**](ContractsApi.md#getContract) | **GET** /my/contracts/{contractId} | Get Contract
[**getContracts**](ContractsApi.md#getContracts) | **GET** /my/contracts | List Contracts

<a name="acceptContract"></a>
# **acceptContract**
> Object acceptContract()

Accept Contract

Accept a contract by ID.   You can only accept contracts that were offered to you, were not accepted yet, and whose deadlines has not passed yet.

### Example
```javascript
import {SpaceTradersApi} from 'space_traders_api';
let defaultClient = SpaceTradersApi.ApiClient.instance;


let apiInstance = new SpaceTradersApi.ContractsApi();
apiInstance.acceptContract((error, data, response) => {
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

<a name="deliverContract"></a>
# **deliverContract**
> Object deliverContract(opts)

Deliver Cargo to Contract

Deliver cargo to a contract.  In order to use this API, a ship must be at the delivery location (denoted in the delivery terms as &#x60;destinationSymbol&#x60; of a contract) and must have a number of units of a good required by this contract in its cargo.  Cargo that was delivered will be removed from the ship&#x27;s cargo.

### Example
```javascript
import {SpaceTradersApi} from 'space_traders_api';
let defaultClient = SpaceTradersApi.ApiClient.instance;


let apiInstance = new SpaceTradersApi.ContractsApi();
let opts = { 
  'body': null // Object | 
};
apiInstance.deliverContract(opts, (error, data, response) => {
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
 **body** | [**Object**](Object.md)|  | [optional] 

### Return type

**Object**

### Authorization

[AgentToken](../README.md#AgentToken)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="fulfillContract"></a>
# **fulfillContract**
> Object fulfillContract()

Fulfill Contract

Fulfill a contract. Can only be used on contracts that have all of their delivery terms fulfilled.

### Example
```javascript
import {SpaceTradersApi} from 'space_traders_api';
let defaultClient = SpaceTradersApi.ApiClient.instance;


let apiInstance = new SpaceTradersApi.ContractsApi();
apiInstance.fulfillContract((error, data, response) => {
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

<a name="getContract"></a>
# **getContract**
> Object getContract()

Get Contract

Get the details of a contract by ID.

### Example
```javascript
import {SpaceTradersApi} from 'space_traders_api';
let defaultClient = SpaceTradersApi.ApiClient.instance;


let apiInstance = new SpaceTradersApi.ContractsApi();
apiInstance.getContract((error, data, response) => {
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

<a name="getContracts"></a>
# **getContracts**
> Object getContracts(opts)

List Contracts

Return a paginated list of all your contracts.

### Example
```javascript
import {SpaceTradersApi} from 'space_traders_api';
let defaultClient = SpaceTradersApi.ApiClient.instance;


let apiInstance = new SpaceTradersApi.ContractsApi();
let opts = { 
  'page': 1, // Number | What entry offset to request
  'limit': 10 // Number | How many entries to return per page
};
apiInstance.getContracts(opts, (error, data, response) => {
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

