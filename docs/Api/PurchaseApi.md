# KuziumOrbitClient\PurchaseApi



All URIs are relative to https://orbit.kuzium.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createPurchaseOrder()**](PurchaseApi.md#createPurchaseOrder) | **POST** /api/v1/accounts/{accountId}/purchase/orders |  |
| [**deletePurchaseOrder()**](PurchaseApi.md#deletePurchaseOrder) | **DELETE** /api/v1/accounts/{accountId}/purchase/orders/{orderId} |  |
| [**getPurchaseOrder()**](PurchaseApi.md#getPurchaseOrder) | **GET** /api/v1/accounts/{accountId}/purchase/orders/{orderId} |  |
| [**listPurchaseOrders()**](PurchaseApi.md#listPurchaseOrders) | **GET** /api/v1/accounts/{accountId}/purchase/orders |  |
| [**updatePurchaseOrder()**](PurchaseApi.md#updatePurchaseOrder) | **PUT** /api/v1/accounts/{accountId}/purchase/orders/{orderId} |  |
| [**updatePurchaseOrderStatus()**](PurchaseApi.md#updatePurchaseOrderStatus) | **PATCH** /api/v1/accounts/{accountId}/purchase/orders/{orderId}/status |  |


## `createPurchaseOrder()`

```php
createPurchaseOrder($account_id, $create_purchase_order_request): \KuziumOrbitClient\Model\PurchaseOrderResponse
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKey
$config = KuziumOrbitClient\Configuration::getDefaultConfiguration()->setApiKey('X-Api-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = KuziumOrbitClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Api-Key', 'Bearer');


$apiInstance = new KuziumOrbitClient\Api\PurchaseApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string
$create_purchase_order_request = new \KuziumOrbitClient\Model\CreatePurchaseOrderRequest(); // \KuziumOrbitClient\Model\CreatePurchaseOrderRequest

try {
    $result = $apiInstance->createPurchaseOrder($account_id, $create_purchase_order_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PurchaseApi->createPurchaseOrder: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**|  | |
| **create_purchase_order_request** | [**\KuziumOrbitClient\Model\CreatePurchaseOrderRequest**](../Model/CreatePurchaseOrderRequest.md)|  | |

### Return type

[**\KuziumOrbitClient\Model\PurchaseOrderResponse**](../Model/PurchaseOrderResponse.md)

### Authorization

[ApiKey](../../README.md#ApiKey)

### HTTP request headers

- **Content-Type**: `application/json`, `text/json`, `application/*+json`
- **Accept**: `text/plain`, `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deletePurchaseOrder()`

```php
deletePurchaseOrder($account_id, $order_id)
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKey
$config = KuziumOrbitClient\Configuration::getDefaultConfiguration()->setApiKey('X-Api-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = KuziumOrbitClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Api-Key', 'Bearer');


$apiInstance = new KuziumOrbitClient\Api\PurchaseApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string
$order_id = 'order_id_example'; // string

try {
    $apiInstance->deletePurchaseOrder($account_id, $order_id);
} catch (Exception $e) {
    echo 'Exception when calling PurchaseApi->deletePurchaseOrder: ', $e->getMessage(), PHP_EOL;
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

## `getPurchaseOrder()`

```php
getPurchaseOrder($account_id, $order_id): \KuziumOrbitClient\Model\PurchaseOrderResponse
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKey
$config = KuziumOrbitClient\Configuration::getDefaultConfiguration()->setApiKey('X-Api-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = KuziumOrbitClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Api-Key', 'Bearer');


$apiInstance = new KuziumOrbitClient\Api\PurchaseApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string
$order_id = 'order_id_example'; // string

try {
    $result = $apiInstance->getPurchaseOrder($account_id, $order_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PurchaseApi->getPurchaseOrder: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**|  | |
| **order_id** | **string**|  | |

### Return type

[**\KuziumOrbitClient\Model\PurchaseOrderResponse**](../Model/PurchaseOrderResponse.md)

### Authorization

[ApiKey](../../README.md#ApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `text/plain`, `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listPurchaseOrders()`

```php
listPurchaseOrders($account_id, $search, $status, $supplier_id, $filter, $page, $page_size): \KuziumOrbitClient\Model\PagedResultOfPurchaseOrderResponse
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKey
$config = KuziumOrbitClient\Configuration::getDefaultConfiguration()->setApiKey('X-Api-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = KuziumOrbitClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Api-Key', 'Bearer');


$apiInstance = new KuziumOrbitClient\Api\PurchaseApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string
$search = 'search_example'; // string
$status = 'status_example'; // string
$supplier_id = 'supplier_id_example'; // string
$filter = 'filter_example'; // string
$page = 1; // int
$page_size = 0; // int

try {
    $result = $apiInstance->listPurchaseOrders($account_id, $search, $status, $supplier_id, $filter, $page, $page_size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PurchaseApi->listPurchaseOrders: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**|  | |
| **search** | **string**|  | [optional] |
| **status** | **string**|  | [optional] |
| **supplier_id** | **string**|  | [optional] |
| **filter** | **string**|  | [optional] |
| **page** | **int**|  | [optional] [default to 1] |
| **page_size** | **int**|  | [optional] [default to 0] |

### Return type

[**\KuziumOrbitClient\Model\PagedResultOfPurchaseOrderResponse**](../Model/PagedResultOfPurchaseOrderResponse.md)

### Authorization

[ApiKey](../../README.md#ApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `text/plain`, `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updatePurchaseOrder()`

```php
updatePurchaseOrder($account_id, $order_id, $update_purchase_order_request): \KuziumOrbitClient\Model\PurchaseOrderResponse
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKey
$config = KuziumOrbitClient\Configuration::getDefaultConfiguration()->setApiKey('X-Api-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = KuziumOrbitClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Api-Key', 'Bearer');


$apiInstance = new KuziumOrbitClient\Api\PurchaseApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string
$order_id = 'order_id_example'; // string
$update_purchase_order_request = new \KuziumOrbitClient\Model\UpdatePurchaseOrderRequest(); // \KuziumOrbitClient\Model\UpdatePurchaseOrderRequest

try {
    $result = $apiInstance->updatePurchaseOrder($account_id, $order_id, $update_purchase_order_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PurchaseApi->updatePurchaseOrder: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**|  | |
| **order_id** | **string**|  | |
| **update_purchase_order_request** | [**\KuziumOrbitClient\Model\UpdatePurchaseOrderRequest**](../Model/UpdatePurchaseOrderRequest.md)|  | |

### Return type

[**\KuziumOrbitClient\Model\PurchaseOrderResponse**](../Model/PurchaseOrderResponse.md)

### Authorization

[ApiKey](../../README.md#ApiKey)

### HTTP request headers

- **Content-Type**: `application/json`, `text/json`, `application/*+json`
- **Accept**: `text/plain`, `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updatePurchaseOrderStatus()`

```php
updatePurchaseOrderStatus($account_id, $order_id, $update_purchase_order_status_request): \KuziumOrbitClient\Model\PurchaseOrderResponse
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKey
$config = KuziumOrbitClient\Configuration::getDefaultConfiguration()->setApiKey('X-Api-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = KuziumOrbitClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Api-Key', 'Bearer');


$apiInstance = new KuziumOrbitClient\Api\PurchaseApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string
$order_id = 'order_id_example'; // string
$update_purchase_order_status_request = new \KuziumOrbitClient\Model\UpdatePurchaseOrderStatusRequest(); // \KuziumOrbitClient\Model\UpdatePurchaseOrderStatusRequest

try {
    $result = $apiInstance->updatePurchaseOrderStatus($account_id, $order_id, $update_purchase_order_status_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PurchaseApi->updatePurchaseOrderStatus: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**|  | |
| **order_id** | **string**|  | |
| **update_purchase_order_status_request** | [**\KuziumOrbitClient\Model\UpdatePurchaseOrderStatusRequest**](../Model/UpdatePurchaseOrderStatusRequest.md)|  | |

### Return type

[**\KuziumOrbitClient\Model\PurchaseOrderResponse**](../Model/PurchaseOrderResponse.md)

### Authorization

[ApiKey](../../README.md#ApiKey)

### HTTP request headers

- **Content-Type**: `application/json`, `text/json`, `application/*+json`
- **Accept**: `text/plain`, `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
