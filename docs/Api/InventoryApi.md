# KuziumOrbitClient\InventoryApi



All URIs are relative to http://localhost:5221, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getInventoryDashboard()**](InventoryApi.md#getInventoryDashboard) | **GET** /api/v1/accounts/{accountId}/inventory/dashboard |  |
| [**getInventoryItem()**](InventoryApi.md#getInventoryItem) | **GET** /api/v1/accounts/{accountId}/inventory/items/{id} |  |
| [**listInventoryItems()**](InventoryApi.md#listInventoryItems) | **GET** /api/v1/accounts/{accountId}/inventory/items |  |


## `getInventoryDashboard()`

```php
getInventoryDashboard($account_id): \KuziumOrbitClient\Model\InventoryDashboardStats
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKey
$config = KuziumOrbitClient\Configuration::getDefaultConfiguration()->setApiKey('X-Api-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = KuziumOrbitClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Api-Key', 'Bearer');


$apiInstance = new KuziumOrbitClient\Api\InventoryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string

try {
    $result = $apiInstance->getInventoryDashboard($account_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InventoryApi->getInventoryDashboard: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**|  | |

### Return type

[**\KuziumOrbitClient\Model\InventoryDashboardStats**](../Model/InventoryDashboardStats.md)

### Authorization

[ApiKey](../../README.md#ApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `text/plain`, `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getInventoryItem()`

```php
getInventoryItem($account_id, $id): \KuziumOrbitClient\Model\InventoryItemResponse
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKey
$config = KuziumOrbitClient\Configuration::getDefaultConfiguration()->setApiKey('X-Api-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = KuziumOrbitClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Api-Key', 'Bearer');


$apiInstance = new KuziumOrbitClient\Api\InventoryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string
$id = 'id_example'; // string

try {
    $result = $apiInstance->getInventoryItem($account_id, $id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InventoryApi->getInventoryItem: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**|  | |
| **id** | **string**|  | |

### Return type

[**\KuziumOrbitClient\Model\InventoryItemResponse**](../Model/InventoryItemResponse.md)

### Authorization

[ApiKey](../../README.md#ApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `text/plain`, `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listInventoryItems()`

```php
listInventoryItems($account_id): \KuziumOrbitClient\Model\InventoryItemResponse[]
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKey
$config = KuziumOrbitClient\Configuration::getDefaultConfiguration()->setApiKey('X-Api-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = KuziumOrbitClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Api-Key', 'Bearer');


$apiInstance = new KuziumOrbitClient\Api\InventoryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string

try {
    $result = $apiInstance->listInventoryItems($account_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InventoryApi->listInventoryItems: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**|  | |

### Return type

[**\KuziumOrbitClient\Model\InventoryItemResponse[]**](../Model/InventoryItemResponse.md)

### Authorization

[ApiKey](../../README.md#ApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `text/plain`, `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
