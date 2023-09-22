# SpaceTradersApi.FleetApi

All URIs are relative to *https://api.spacetraders.io/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createChart**](FleetApi.md#createChart) | **POST** /my/ships/{shipSymbol}/chart | Create Chart
[**createShipShipScan**](FleetApi.md#createShipShipScan) | **POST** /my/ships/{shipSymbol}/scan/ships | Scan Ships
[**createShipSystemScan**](FleetApi.md#createShipSystemScan) | **POST** /my/ships/{shipSymbol}/scan/systems | Scan Systems
[**createShipWaypointScan**](FleetApi.md#createShipWaypointScan) | **POST** /my/ships/{shipSymbol}/scan/waypoints | Scan Waypoints
[**createSurvey**](FleetApi.md#createSurvey) | **POST** /my/ships/{shipSymbol}/survey | Create Survey
[**dockShip**](FleetApi.md#dockShip) | **POST** /my/ships/{shipSymbol}/dock | Dock Ship
[**extractResources**](FleetApi.md#extractResources) | **POST** /my/ships/{shipSymbol}/extract | Extract Resources
[**extractResourcesWithSurvey**](FleetApi.md#extractResourcesWithSurvey) | **POST** /my/ships/{shipSymbol}/extract/survey | Extract Resources with Survey
[**getMounts**](FleetApi.md#getMounts) | **GET** /my/ships/{shipSymbol}/mounts | Get Mounts
[**getMyShip**](FleetApi.md#getMyShip) | **GET** /my/ships/{shipSymbol} | Get Ship
[**getMyShipCargo**](FleetApi.md#getMyShipCargo) | **GET** /my/ships/{shipSymbol}/cargo | Get Ship Cargo
[**getMyShips**](FleetApi.md#getMyShips) | **GET** /my/ships | List Ships
[**getShipCooldown**](FleetApi.md#getShipCooldown) | **GET** /my/ships/{shipSymbol}/cooldown | Get Ship Cooldown
[**getShipNav**](FleetApi.md#getShipNav) | **GET** /my/ships/{shipSymbol}/nav | Get Ship Nav
[**installMount**](FleetApi.md#installMount) | **POST** /my/ships/{shipSymbol}/mounts/install | Install Mount
[**jettison**](FleetApi.md#jettison) | **POST** /my/ships/{shipSymbol}/jettison | Jettison Cargo
[**jumpShip**](FleetApi.md#jumpShip) | **POST** /my/ships/{shipSymbol}/jump | Jump Ship
[**navigateShip**](FleetApi.md#navigateShip) | **POST** /my/ships/{shipSymbol}/navigate | Navigate Ship
[**negotiateContract**](FleetApi.md#negotiateContract) | **POST** /my/ships/{shipSymbol}/negotiate/contract | Negotiate Contract
[**orbitShip**](FleetApi.md#orbitShip) | **POST** /my/ships/{shipSymbol}/orbit | Orbit Ship
[**patchShipNav**](FleetApi.md#patchShipNav) | **PATCH** /my/ships/{shipSymbol}/nav | Patch Ship Nav
[**purchaseCargo**](FleetApi.md#purchaseCargo) | **POST** /my/ships/{shipSymbol}/purchase | Purchase Cargo
[**purchaseShip**](FleetApi.md#purchaseShip) | **POST** /my/ships | Purchase Ship
[**refuelShip**](FleetApi.md#refuelShip) | **POST** /my/ships/{shipSymbol}/refuel | Refuel Ship
[**removeMount**](FleetApi.md#removeMount) | **POST** /my/ships/{shipSymbol}/mounts/remove | Remove Mount
[**sellCargo**](FleetApi.md#sellCargo) | **POST** /my/ships/{shipSymbol}/sell | Sell Cargo
[**shipRefine**](FleetApi.md#shipRefine) | **POST** /my/ships/{shipSymbol}/refine | Ship Refine
[**transferCargo**](FleetApi.md#transferCargo) | **POST** /my/ships/{shipSymbol}/transfer | Transfer Cargo
[**warpShip**](FleetApi.md#warpShip) | **POST** /my/ships/{shipSymbol}/warp | Warp Ship

<a name="createChart"></a>
# **createChart**
> Object createChart()

Create Chart

Command a ship to chart the waypoint at its current location.  Most waypoints in the universe are uncharted by default. These waypoints have their traits hidden until they have been charted by a ship.  Charting a waypoint will record your agent as the one who created the chart, and all other agents would also be able to see the waypoint&#x27;s traits.

### Example
```javascript
import {SpaceTradersApi} from 'space_traders_api';
let defaultClient = SpaceTradersApi.ApiClient.instance;


let apiInstance = new SpaceTradersApi.FleetApi();
apiInstance.createChart((error, data, response) => {
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

<a name="createShipShipScan"></a>
# **createShipShipScan**
> Object createShipShipScan()

Scan Ships

Scan for nearby ships, retrieving information for all ships in range.  Requires a ship to have the &#x60;Sensor Array&#x60; mount installed to use.  The ship will enter a cooldown after using this function, during which it cannot execute certain actions.

### Example
```javascript
import {SpaceTradersApi} from 'space_traders_api';
let defaultClient = SpaceTradersApi.ApiClient.instance;


let apiInstance = new SpaceTradersApi.FleetApi();
apiInstance.createShipShipScan((error, data, response) => {
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

<a name="createShipSystemScan"></a>
# **createShipSystemScan**
> Object createShipSystemScan()

Scan Systems

Scan for nearby systems, retrieving information on the systems&#x27; distance from the ship and their waypoints. Requires a ship to have the &#x60;Sensor Array&#x60; mount installed to use.  The ship will enter a cooldown after using this function, during which it cannot execute certain actions.

### Example
```javascript
import {SpaceTradersApi} from 'space_traders_api';
let defaultClient = SpaceTradersApi.ApiClient.instance;


let apiInstance = new SpaceTradersApi.FleetApi();
apiInstance.createShipSystemScan((error, data, response) => {
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

<a name="createShipWaypointScan"></a>
# **createShipWaypointScan**
> Object createShipWaypointScan()

Scan Waypoints

Scan for nearby waypoints, retrieving detailed information on each waypoint in range. Scanning uncharted waypoints will allow you to ignore their uncharted state and will list the waypoints&#x27; traits.  Requires a ship to have the &#x60;Sensor Array&#x60; mount installed to use.  The ship will enter a cooldown after using this function, during which it cannot execute certain actions.

### Example
```javascript
import {SpaceTradersApi} from 'space_traders_api';
let defaultClient = SpaceTradersApi.ApiClient.instance;


let apiInstance = new SpaceTradersApi.FleetApi();
apiInstance.createShipWaypointScan((error, data, response) => {
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

<a name="createSurvey"></a>
# **createSurvey**
> Object createSurvey()

Create Survey

Create surveys on a waypoint that can be extracted such as asteroid fields. A survey focuses on specific types of deposits from the extracted location. When ships extract using this survey, they are guaranteed to procure a high amount of one of the goods in the survey.  In order to use a survey, send the entire survey details in the body of the extract request.  Each survey may have multiple deposits, and if a symbol shows up more than once, that indicates a higher chance of extracting that resource.  Your ship will enter a cooldown after surveying in which it is unable to perform certain actions. Surveys will eventually expire after a period of time or will be exhausted after being extracted several times based on the survey&#x27;s size. Multiple ships can use the same survey for extraction.  A ship must have the &#x60;Surveyor&#x60; mount installed in order to use this function.

### Example
```javascript
import {SpaceTradersApi} from 'space_traders_api';
let defaultClient = SpaceTradersApi.ApiClient.instance;


let apiInstance = new SpaceTradersApi.FleetApi();
apiInstance.createSurvey((error, data, response) => {
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

<a name="dockShip"></a>
# **dockShip**
> Object dockShip()

Dock Ship

Attempt to dock your ship at its current location. Docking will only succeed if your ship is capable of docking at the time of the request.  Docked ships can access elements in their current location, such as the market or a shipyard, but cannot do actions that require the ship to be above surface such as navigating or extracting.  The endpoint is idempotent - successive calls will succeed even if the ship is already docked.

### Example
```javascript
import {SpaceTradersApi} from 'space_traders_api';
let defaultClient = SpaceTradersApi.ApiClient.instance;


let apiInstance = new SpaceTradersApi.FleetApi();
apiInstance.dockShip((error, data, response) => {
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

<a name="extractResources"></a>
# **extractResources**
> Object extractResources(opts)

Extract Resources

Extract resources from a waypoint that can be extracted, such as asteroid fields, into your ship. Send an optional survey as the payload to target specific yields.  The ship must be in orbit to be able to extract and must have mining equipments installed that can extract goods, such as the &#x60;Gas Siphon&#x60; mount for gas-based goods or &#x60;Mining Laser&#x60; mount for ore-based goods.  The survey property is now deprecated. See the &#x60;extract/survey&#x60; endpoint for more details.

### Example
```javascript
import {SpaceTradersApi} from 'space_traders_api';
let defaultClient = SpaceTradersApi.ApiClient.instance;


let apiInstance = new SpaceTradersApi.FleetApi();
let opts = { 
  'body': null // Object | 
};
apiInstance.extractResources(opts, (error, data, response) => {
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

<a name="extractResourcesWithSurvey"></a>
# **extractResourcesWithSurvey**
> Object extractResourcesWithSurvey()

Extract Resources with Survey

Use a survey when extracting resources from a waypoint. This endpoint requires a survey as the payload, which allows your ship to extract specific yields.  Send the full survey object as the payload which will be validated according to the signature. If the signature is invalid, or any properties of the survey are changed, the request will fail.

### Example
```javascript
import {SpaceTradersApi} from 'space_traders_api';
let defaultClient = SpaceTradersApi.ApiClient.instance;


let apiInstance = new SpaceTradersApi.FleetApi();
apiInstance.extractResourcesWithSurvey((error, data, response) => {
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

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="getMounts"></a>
# **getMounts**
> Object getMounts()

Get Mounts

Get the mounts installed on a ship.

### Example
```javascript
import {SpaceTradersApi} from 'space_traders_api';
let defaultClient = SpaceTradersApi.ApiClient.instance;


let apiInstance = new SpaceTradersApi.FleetApi();
apiInstance.getMounts((error, data, response) => {
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

<a name="getMyShip"></a>
# **getMyShip**
> Object getMyShip()

Get Ship

Retrieve the details of a ship under your agent&#x27;s ownership.

### Example
```javascript
import {SpaceTradersApi} from 'space_traders_api';
let defaultClient = SpaceTradersApi.ApiClient.instance;


let apiInstance = new SpaceTradersApi.FleetApi();
apiInstance.getMyShip((error, data, response) => {
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

<a name="getMyShipCargo"></a>
# **getMyShipCargo**
> Object getMyShipCargo()

Get Ship Cargo

Retrieve the cargo of a ship under your agent&#x27;s ownership.

### Example
```javascript
import {SpaceTradersApi} from 'space_traders_api';
let defaultClient = SpaceTradersApi.ApiClient.instance;


let apiInstance = new SpaceTradersApi.FleetApi();
apiInstance.getMyShipCargo((error, data, response) => {
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

<a name="getMyShips"></a>
# **getMyShips**
> Object getMyShips(opts)

List Ships

Return a paginated list of all of ships under your agent&#x27;s ownership.

### Example
```javascript
import {SpaceTradersApi} from 'space_traders_api';
let defaultClient = SpaceTradersApi.ApiClient.instance;


let apiInstance = new SpaceTradersApi.FleetApi();
let opts = { 
  'page': 1, // Number | What entry offset to request
  'limit': 10 // Number | How many entries to return per page
};
apiInstance.getMyShips(opts, (error, data, response) => {
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

<a name="getShipCooldown"></a>
# **getShipCooldown**
> Object getShipCooldown()

Get Ship Cooldown

Retrieve the details of your ship&#x27;s reactor cooldown. Some actions such as activating your jump drive, scanning, or extracting resources taxes your reactor and results in a cooldown.  Your ship cannot perform additional actions until your cooldown has expired. The duration of your cooldown is relative to the power consumption of the related modules or mounts for the action taken.  Response returns a 204 status code (no-content) when the ship has no cooldown.

### Example
```javascript
import {SpaceTradersApi} from 'space_traders_api';
let defaultClient = SpaceTradersApi.ApiClient.instance;


let apiInstance = new SpaceTradersApi.FleetApi();
apiInstance.getShipCooldown((error, data, response) => {
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

<a name="getShipNav"></a>
# **getShipNav**
> Object getShipNav()

Get Ship Nav

Get the current nav status of a ship.

### Example
```javascript
import {SpaceTradersApi} from 'space_traders_api';
let defaultClient = SpaceTradersApi.ApiClient.instance;


let apiInstance = new SpaceTradersApi.FleetApi();
apiInstance.getShipNav((error, data, response) => {
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

<a name="installMount"></a>
# **installMount**
> Object installMount(opts)

Install Mount

Install a mount on a ship.  In order to install a mount, the ship must be docked and located in a waypoint that has a &#x60;Shipyard&#x60; trait. The ship also must have the mount to install in its cargo hold.  An installation fee will be deduced by the Shipyard for installing the mount on the ship. 

### Example
```javascript
import {SpaceTradersApi} from 'space_traders_api';
let defaultClient = SpaceTradersApi.ApiClient.instance;


let apiInstance = new SpaceTradersApi.FleetApi();
let opts = { 
  'body': null // Object | 
};
apiInstance.installMount(opts, (error, data, response) => {
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

<a name="jettison"></a>
# **jettison**
> Object jettison(opts)

Jettison Cargo

Jettison cargo from your ship&#x27;s cargo hold.

### Example
```javascript
import {SpaceTradersApi} from 'space_traders_api';
let defaultClient = SpaceTradersApi.ApiClient.instance;


let apiInstance = new SpaceTradersApi.FleetApi();
let opts = { 
  'body': null // Object | 
};
apiInstance.jettison(opts, (error, data, response) => {
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

<a name="jumpShip"></a>
# **jumpShip**
> Object jumpShip(opts)

Jump Ship

Jump your ship instantly to a target system. The ship must be in orbit to use this function. When used while in orbit of a Jump Gate waypoint, any ship can use this command, jumping to the target system&#x27;s Jump Gate waypoint.  When used elsewhere, jumping requires the ship to have a &#x60;Jump Drive&#x60; module installed and consumes a unit of antimatter from the ship&#x27;s cargo. The command will fail if there is no antimatter to consume. When jumping via the &#x60;Jump Drive&#x60; module, the ship ends up at its largest source of energy in the system, such as a gas planet or a jump gate.

### Example
```javascript
import {SpaceTradersApi} from 'space_traders_api';
let defaultClient = SpaceTradersApi.ApiClient.instance;


let apiInstance = new SpaceTradersApi.FleetApi();
let opts = { 
  'body': null // Object | 
};
apiInstance.jumpShip(opts, (error, data, response) => {
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

<a name="navigateShip"></a>
# **navigateShip**
> Object navigateShip(opts)

Navigate Ship

Navigate to a target destination. The ship must be in orbit to use this function. The destination waypoint must be within the same system as the ship&#x27;s current location. Navigating will consume the necessary fuel from the ship&#x27;s manifest based on the distance to the target waypoint.  The returned response will detail the route information including the expected time of arrival. Most ship actions are unavailable until the ship has arrived at it&#x27;s destination.  To travel between systems, see the ship&#x27;s Warp or Jump actions.

### Example
```javascript
import {SpaceTradersApi} from 'space_traders_api';
let defaultClient = SpaceTradersApi.ApiClient.instance;


let apiInstance = new SpaceTradersApi.FleetApi();
let opts = { 
  'body': null // Object | 
};
apiInstance.navigateShip(opts, (error, data, response) => {
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

<a name="negotiateContract"></a>
# **negotiateContract**
> Object negotiateContract()

Negotiate Contract

Negotiate a new contract with the HQ.  In order to negotiate a new contract, an agent must not have ongoing or offered contracts over the allowed maximum amount. Currently the maximum contracts an agent can have at a time is 1.  Once a contract is negotiated, it is added to the list of contracts offered to the agent, which the agent can then accept.   The ship must be present at a faction&#x27;s HQ waypoint to negotiate a contract with that faction.

### Example
```javascript
import {SpaceTradersApi} from 'space_traders_api';
let defaultClient = SpaceTradersApi.ApiClient.instance;


let apiInstance = new SpaceTradersApi.FleetApi();
apiInstance.negotiateContract((error, data, response) => {
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

<a name="orbitShip"></a>
# **orbitShip**
> Object orbitShip()

Orbit Ship

Attempt to move your ship into orbit at its current location. The request will only succeed if your ship is capable of moving into orbit at the time of the request.  Orbiting ships are able to do actions that require the ship to be above surface such as navigating or extracting, but cannot access elements in their current waypoint, such as the market or a shipyard.  The endpoint is idempotent - successive calls will succeed even if the ship is already in orbit.

### Example
```javascript
import {SpaceTradersApi} from 'space_traders_api';
let defaultClient = SpaceTradersApi.ApiClient.instance;


let apiInstance = new SpaceTradersApi.FleetApi();
apiInstance.orbitShip((error, data, response) => {
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

<a name="patchShipNav"></a>
# **patchShipNav**
> Object patchShipNav(opts)

Patch Ship Nav

Update the nav configuration of a ship.  Currently only supports configuring the Flight Mode of the ship, which affects its speed and fuel consumption.

### Example
```javascript
import {SpaceTradersApi} from 'space_traders_api';
let defaultClient = SpaceTradersApi.ApiClient.instance;


let apiInstance = new SpaceTradersApi.FleetApi();
let opts = { 
  'body': null // Object | 
};
apiInstance.patchShipNav(opts, (error, data, response) => {
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

<a name="purchaseCargo"></a>
# **purchaseCargo**
> Object purchaseCargo(opts)

Purchase Cargo

Purchase cargo from a market.  The ship must be docked in a waypoint that has &#x60;Marketplace&#x60; trait, and the market must be selling a good to be able to purchase it.  The maximum amount of units of a good that can be purchased in each transaction are denoted by the &#x60;tradeVolume&#x60; value of the good, which can be viewed by using the Get Market action.  Purchased goods are added to the ship&#x27;s cargo hold.

### Example
```javascript
import {SpaceTradersApi} from 'space_traders_api';
let defaultClient = SpaceTradersApi.ApiClient.instance;


let apiInstance = new SpaceTradersApi.FleetApi();
let opts = { 
  'body': null // Object | 
};
apiInstance.purchaseCargo(opts, (error, data, response) => {
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

<a name="purchaseShip"></a>
# **purchaseShip**
> Object purchaseShip(opts)

Purchase Ship

Purchase a ship from a Shipyard. In order to use this function, a ship under your agent&#x27;s ownership must be in a waypoint that has the &#x60;Shipyard&#x60; trait, and the Shipyard must sell the type of the desired ship.  Shipyards typically offer ship types, which are predefined templates of ships that have dedicated roles. A template comes with a preset of an engine, a reactor, and a frame. It may also include a few modules and mounts.

### Example
```javascript
import {SpaceTradersApi} from 'space_traders_api';
let defaultClient = SpaceTradersApi.ApiClient.instance;


let apiInstance = new SpaceTradersApi.FleetApi();
let opts = { 
  'body': null // Object | 
};
apiInstance.purchaseShip(opts, (error, data, response) => {
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

<a name="refuelShip"></a>
# **refuelShip**
> Object refuelShip(opts)

Refuel Ship

Refuel your ship by buying fuel from the local market.  Requires the ship to be docked in a waypoint that has the &#x60;Marketplace&#x60; trait, and the market must be selling fuel in order to refuel.  Each fuel bought from the market replenishes 100 units in your ship&#x27;s fuel.  Ships will always be refuel to their frame&#x27;s maximum fuel capacity when using this action.

### Example
```javascript
import {SpaceTradersApi} from 'space_traders_api';
let defaultClient = SpaceTradersApi.ApiClient.instance;


let apiInstance = new SpaceTradersApi.FleetApi();
let opts = { 
  'body': null // Object | 
};
apiInstance.refuelShip(opts, (error, data, response) => {
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

<a name="removeMount"></a>
# **removeMount**
> Object removeMount(opts)

Remove Mount

Remove a mount from a ship.  The ship must be docked in a waypoint that has the &#x60;Shipyard&#x60; trait, and must have the desired mount that it wish to remove installed.  A removal fee will be deduced from the agent by the Shipyard.

### Example
```javascript
import {SpaceTradersApi} from 'space_traders_api';
let defaultClient = SpaceTradersApi.ApiClient.instance;


let apiInstance = new SpaceTradersApi.FleetApi();
let opts = { 
  'body': null // Object | 
};
apiInstance.removeMount(opts, (error, data, response) => {
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

<a name="sellCargo"></a>
# **sellCargo**
> Object sellCargo(opts)

Sell Cargo

Sell cargo in your ship to a market that trades this cargo. The ship must be docked in a waypoint that has the &#x60;Marketplace&#x60; trait in order to use this function.

### Example
```javascript
import {SpaceTradersApi} from 'space_traders_api';
let defaultClient = SpaceTradersApi.ApiClient.instance;


let apiInstance = new SpaceTradersApi.FleetApi();
let opts = { 
  'body': null // Object | 
};
apiInstance.sellCargo(opts, (error, data, response) => {
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

<a name="shipRefine"></a>
# **shipRefine**
> Object shipRefine(opts)

Ship Refine

Attempt to refine the raw materials on your ship. The request will only succeed if your ship is capable of refining at the time of the request. In order to be able to refine, a ship must have goods that can be refined and have installed a &#x60;Refinery&#x60; module that can refine it.  When refining, 30 basic goods will be converted into 10 processed goods.

### Example
```javascript
import {SpaceTradersApi} from 'space_traders_api';
let defaultClient = SpaceTradersApi.ApiClient.instance;


let apiInstance = new SpaceTradersApi.FleetApi();
let opts = { 
  'body': null // Object | 
};
apiInstance.shipRefine(opts, (error, data, response) => {
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

<a name="transferCargo"></a>
# **transferCargo**
> Object transferCargo(opts)

Transfer Cargo

Transfer cargo between ships.  The receiving ship must be in the same waypoint as the transferring ship, and it must able to hold the additional cargo after the transfer is complete. Both ships also must be in the same state, either both are docked or both are orbiting.  The response body&#x27;s cargo shows the cargo of the transferring ship after the transfer is complete.

### Example
```javascript
import {SpaceTradersApi} from 'space_traders_api';
let defaultClient = SpaceTradersApi.ApiClient.instance;


let apiInstance = new SpaceTradersApi.FleetApi();
let opts = { 
  'body': null // Object | 
};
apiInstance.transferCargo(opts, (error, data, response) => {
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

<a name="warpShip"></a>
# **warpShip**
> Object warpShip(opts)

Warp Ship

Warp your ship to a target destination in another system. The ship must be in orbit to use this function and must have the &#x60;Warp Drive&#x60; module installed. Warping will consume the necessary fuel from the ship&#x27;s manifest.  The returned response will detail the route information including the expected time of arrival. Most ship actions are unavailable until the ship has arrived at its destination.

### Example
```javascript
import {SpaceTradersApi} from 'space_traders_api';
let defaultClient = SpaceTradersApi.ApiClient.instance;


let apiInstance = new SpaceTradersApi.FleetApi();
let opts = { 
  'body': null // Object | 
};
apiInstance.warpShip(opts, (error, data, response) => {
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

