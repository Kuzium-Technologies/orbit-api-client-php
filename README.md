# orbit-api-client

The stable, external-integration surface of the Orbit API. Authenticate with an API key (Settings > API Keys) via the X-Api-Key header.


## Installation & Usage

### Requirements

PHP 8.1 and later.

### Composer

To install the bindings via [Composer](https://getcomposer.org/), add the following to `composer.json`:

```json
{
  "repositories": [
    {
      "type": "vcs",
      "url": "https://github.com/GIT_USER_ID/GIT_REPO_ID.git"
    }
  ],
  "require": {
    "GIT_USER_ID/GIT_REPO_ID": "*@dev"
  }
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
<?php
require_once('/path/to/orbit-api-client/vendor/autoload.php');
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



// Configure API key authorization: ApiKey
$config = KuziumOrbitClient\Configuration::getDefaultConfiguration()->setApiKey('X-Api-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = KuziumOrbitClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Api-Key', 'Bearer');


$apiInstance = new KuziumOrbitClient\Api\CrmApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string
$create_customer_request = new \KuziumOrbitClient\Model\CreateCustomerRequest(); // \KuziumOrbitClient\Model\CreateCustomerRequest

try {
    $result = $apiInstance->createCustomer($account_id, $create_customer_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CrmApi->createCustomer: ', $e->getMessage(), PHP_EOL;
}

```

## API Endpoints

All URIs are relative to *http://localhost:5221*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*CrmApi* | [**createCustomer**](docs/Api/CrmApi.md#createcustomer) | **POST** /api/v1/accounts/{accountId}/crm/customers | 
*CrmApi* | [**deleteCustomer**](docs/Api/CrmApi.md#deletecustomer) | **DELETE** /api/v1/accounts/{accountId}/crm/customers/{customerId} | 
*CrmApi* | [**getCustomer**](docs/Api/CrmApi.md#getcustomer) | **GET** /api/v1/accounts/{accountId}/crm/customers/{customerId} | 
*CrmApi* | [**listCustomers**](docs/Api/CrmApi.md#listcustomers) | **GET** /api/v1/accounts/{accountId}/crm/customers | 
*CrmApi* | [**updateCustomer**](docs/Api/CrmApi.md#updatecustomer) | **PATCH** /api/v1/accounts/{accountId}/crm/customers/{customerId} | 
*InventoryApi* | [**getInventoryDashboard**](docs/Api/InventoryApi.md#getinventorydashboard) | **GET** /api/v1/accounts/{accountId}/inventory/dashboard | 
*InventoryApi* | [**getInventoryItem**](docs/Api/InventoryApi.md#getinventoryitem) | **GET** /api/v1/accounts/{accountId}/inventory/items/{id} | 
*InventoryApi* | [**listInventoryItems**](docs/Api/InventoryApi.md#listinventoryitems) | **GET** /api/v1/accounts/{accountId}/inventory/items | 
*MeApi* | [**getCurrentContext**](docs/Api/MeApi.md#getcurrentcontext) | **GET** /api/v1/me | 
*SalesApi* | [**createSalesOrder**](docs/Api/SalesApi.md#createsalesorder) | **POST** /api/v1/accounts/{accountId}/sales/orders | 
*SalesApi* | [**deleteSalesOrder**](docs/Api/SalesApi.md#deletesalesorder) | **DELETE** /api/v1/accounts/{accountId}/sales/orders/{orderId} | 
*SalesApi* | [**getSalesOrder**](docs/Api/SalesApi.md#getsalesorder) | **GET** /api/v1/accounts/{accountId}/sales/orders/{orderId} | 
*SalesApi* | [**listSalesOrders**](docs/Api/SalesApi.md#listsalesorders) | **GET** /api/v1/accounts/{accountId}/sales/orders | 
*SalesApi* | [**updateSalesOrder**](docs/Api/SalesApi.md#updatesalesorder) | **PUT** /api/v1/accounts/{accountId}/sales/orders/{orderId} | 
*SalesApi* | [**updateSalesOrderStatus**](docs/Api/SalesApi.md#updatesalesorderstatus) | **PUT** /api/v1/accounts/{accountId}/sales/orders/{orderId}/status | 

## Models

- [CreateCustomerRequest](docs/Model/CreateCustomerRequest.md)
- [CreateSalesOrderLineRequest](docs/Model/CreateSalesOrderLineRequest.md)
- [CreateSalesOrderRequest](docs/Model/CreateSalesOrderRequest.md)
- [CustomerResponse](docs/Model/CustomerResponse.md)
- [InventoryDashboardStats](docs/Model/InventoryDashboardStats.md)
- [InventoryItemResponse](docs/Model/InventoryItemResponse.md)
- [MeResponse](docs/Model/MeResponse.md)
- [PagedResultOfCustomerResponse](docs/Model/PagedResultOfCustomerResponse.md)
- [PagedResultOfSalesOrderDto](docs/Model/PagedResultOfSalesOrderDto.md)
- [SalesOrder](docs/Model/SalesOrder.md)
- [SalesOrderDetailDto](docs/Model/SalesOrderDetailDto.md)
- [SalesOrderDto](docs/Model/SalesOrderDto.md)
- [SalesOrderLine](docs/Model/SalesOrderLine.md)
- [SalesOrderLineDto](docs/Model/SalesOrderLineDto.md)
- [UpdateCustomerRequest](docs/Model/UpdateCustomerRequest.md)
- [UpdateOrderStatusRequest](docs/Model/UpdateOrderStatusRequest.md)
- [UpdateSalesOrderRequest](docs/Model/UpdateSalesOrderRequest.md)

## Authorization

Authentication schemes defined for the API:
### ApiKey

- **Type**: API key
- **API key parameter name**: X-Api-Key
- **Location**: HTTP header


## Tests

To run the tests, use:

```bash
composer install
vendor/bin/phpunit
```

## Author



## About this package

This PHP package is automatically generated by the [OpenAPI Generator](https://openapi-generator.tech) project:

- API version: `1.0.0`
    - Package version: `0.1.0`
    - Generator version: `7.25.0`
- Build package: `org.openapitools.codegen.languages.PhpClientCodegen`
