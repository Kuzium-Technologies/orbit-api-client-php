# KuziumOrbitClient\SalesApi



All URIs are relative to http://localhost:5221, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createSalesOrder()**](SalesApi.md#createSalesOrder) | **POST** /api/v1/accounts/{accountId}/sales/orders |  |
| [**deleteSalesOrder()**](SalesApi.md#deleteSalesOrder) | **DELETE** /api/v1/accounts/{accountId}/sales/orders/{orderId} |  |
| [**getSalesOrder()**](SalesApi.md#getSalesOrder) | **GET** /api/v1/accounts/{accountId}/sales/orders/{orderId} |  |
| [**listSalesOrders()**](SalesApi.md#listSalesOrders) | **GET** /api/v1/accounts/{accountId}/sales/orders |  |
| [**updateSalesOrder()**](SalesApi.md#updateSalesOrder) | **PUT** /api/v1/accounts/{accountId}/sales/orders/{orderId} |  |
| [**updateSalesOrderStatus()**](SalesApi.md#updateSalesOrderStatus) | **PUT** /api/v1/accounts/{accountId}/sales/orders/{orderId}/status |  |


## `createSalesOrder()`

```php
createSalesOrder($account_id, $create_sales_order_request): \KuziumOrbitClient\Model\SalesOrder
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKey
$config = KuziumOrbitClient\Configuration::getDefaultConfiguration()->setApiKey('X-Api-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = KuziumOrbitClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Api-Key', 'Bearer');


$apiInstance = new KuziumOrbitClient\Api\SalesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string
$create_sales_order_request = new \KuziumOrbitClient\Model\CreateSalesOrderRequest(); // \KuziumOrbitClient\Model\CreateSalesOrderRequest

try {
    $result = $apiInstance->createSalesOrder($account_id, $create_sales_order_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SalesApi->createSalesOrder: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**|  | |
| **create_sales_order_request** | [**\KuziumOrbitClient\Model\CreateSalesOrderRequest**](../Model/CreateSalesOrderRequest.md)|  | |

### Return type

[**\KuziumOrbitClient\Model\SalesOrder**](../Model/SalesOrder.md)

### Authorization

[ApiKey](../../README.md#ApiKey)

### HTTP request headers

- **Content-Type**: `application/json`, `text/json`, `application/*+json`
- **Accept**: `text/plain`, `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteSalesOrder()`

```php
deleteSalesOrder($account_id, $order_id)
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKey
$config = KuziumOrbitClient\Configuration::getDefaultConfiguration()->setApiKey('X-Api-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = KuziumOrbitClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Api-Key', 'Bearer');


$apiInstance = new KuziumOrbitClient\Api\SalesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string
$order_id = 'order_id_example'; // string

try {
    $apiInstance->deleteSalesOrder($account_id, $order_id);
} catch (Exception $e) {
    echo 'Exception when calling SalesApi->deleteSalesOrder: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**|  | |
| **order_id** | **string**|  | |

### Return type

void (empty response body)

### Authorization

[ApiKey](../../README.md#ApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getSalesOrder()`

```php
getSalesOrder($account_id, $order_id): \KuziumOrbitClient\Model\SalesOrderDetailDto
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKey
$config = KuziumOrbitClient\Configuration::getDefaultConfiguration()->setApiKey('X-Api-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = KuziumOrbitClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Api-Key', 'Bearer');


$apiInstance = new KuziumOrbitClient\Api\SalesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string
$order_id = 'order_id_example'; // string

try {
    $result = $apiInstance->getSalesOrder($account_id, $order_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SalesApi->getSalesOrder: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**|  | |
| **order_id** | **string**|  | |

### Return type

[**\KuziumOrbitClient\Model\SalesOrderDetailDto**](../Model/SalesOrderDetailDto.md)

### Authorization

[ApiKey](../../README.md#ApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `text/plain`, `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listSalesOrders()`

```php
listSalesOrders($account_id, $customer_id, $status, $search, $filter, $page, $page_size, $sort_by, $sort_order): \KuziumOrbitClient\Model\PagedResultOfSalesOrderDto
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKey
$config = KuziumOrbitClient\Configuration::getDefaultConfiguration()->setApiKey('X-Api-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = KuziumOrbitClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Api-Key', 'Bearer');


$apiInstance = new KuziumOrbitClient\Api\SalesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string
$customer_id = 'customer_id_example'; // string
$status = 'status_example'; // string
$search = 'search_example'; // string
$filter = 'filter_example'; // string
$page = 1; // int
$page_size = 0; // int
$sort_by = 'orderdate'; // string
$sort_order = 'desc'; // string

try {
    $result = $apiInstance->listSalesOrders($account_id, $customer_id, $status, $search, $filter, $page, $page_size, $sort_by, $sort_order);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SalesApi->listSalesOrders: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**|  | |
| **customer_id** | **string**|  | [optional] |
| **status** | **string**|  | [optional] |
| **search** | **string**|  | [optional] |
| **filter** | **string**|  | [optional] |
| **page** | **int**|  | [optional] [default to 1] |
| **page_size** | **int**|  | [optional] [default to 0] |
| **sort_by** | **string**|  | [optional] [default to &#39;orderdate&#39;] |
| **sort_order** | **string**|  | [optional] [default to &#39;desc&#39;] |

### Return type

[**\KuziumOrbitClient\Model\PagedResultOfSalesOrderDto**](../Model/PagedResultOfSalesOrderDto.md)

### Authorization

[ApiKey](../../README.md#ApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `text/plain`, `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateSalesOrder()`

```php
updateSalesOrder($account_id, $order_id, $update_sales_order_request): \KuziumOrbitClient\Model\SalesOrder
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKey
$config = KuziumOrbitClient\Configuration::getDefaultConfiguration()->setApiKey('X-Api-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = KuziumOrbitClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Api-Key', 'Bearer');


$apiInstance = new KuziumOrbitClient\Api\SalesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string
$order_id = 'order_id_example'; // string
$update_sales_order_request = new \KuziumOrbitClient\Model\UpdateSalesOrderRequest(); // \KuziumOrbitClient\Model\UpdateSalesOrderRequest

try {
    $result = $apiInstance->updateSalesOrder($account_id, $order_id, $update_sales_order_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SalesApi->updateSalesOrder: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**|  | |
| **order_id** | **string**|  | |
| **update_sales_order_request** | [**\KuziumOrbitClient\Model\UpdateSalesOrderRequest**](../Model/UpdateSalesOrderRequest.md)|  | |

### Return type

[**\KuziumOrbitClient\Model\SalesOrder**](../Model/SalesOrder.md)

### Authorization

[ApiKey](../../README.md#ApiKey)

### HTTP request headers

- **Content-Type**: `application/json`, `text/json`, `application/*+json`
- **Accept**: `text/plain`, `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateSalesOrderStatus()`

```php
updateSalesOrderStatus($account_id, $order_id, $update_order_status_request)
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKey
$config = KuziumOrbitClient\Configuration::getDefaultConfiguration()->setApiKey('X-Api-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = KuziumOrbitClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Api-Key', 'Bearer');


$apiInstance = new KuziumOrbitClient\Api\SalesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string
$order_id = 'order_id_example'; // string
$update_order_status_request = new \KuziumOrbitClient\Model\UpdateOrderStatusRequest(); // \KuziumOrbitClient\Model\UpdateOrderStatusRequest

try {
    $apiInstance->updateSalesOrderStatus($account_id, $order_id, $update_order_status_request);
} catch (Exception $e) {
    echo 'Exception when calling SalesApi->updateSalesOrderStatus: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**|  | |
| **order_id** | **string**|  | |
| **update_order_status_request** | [**\KuziumOrbitClient\Model\UpdateOrderStatusRequest**](../Model/UpdateOrderStatusRequest.md)|  | |

### Return type

void (empty response body)

### Authorization

[ApiKey](../../README.md#ApiKey)

### HTTP request headers

- **Content-Type**: `application/json`, `text/json`, `application/*+json`
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
