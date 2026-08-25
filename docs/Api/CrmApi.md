# KuziumOrbitClient\CrmApi



All URIs are relative to http://localhost:5221, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createCustomer()**](CrmApi.md#createCustomer) | **POST** /api/v1/accounts/{accountId}/crm/customers |  |
| [**deleteCustomer()**](CrmApi.md#deleteCustomer) | **DELETE** /api/v1/accounts/{accountId}/crm/customers/{customerId} |  |
| [**getCustomer()**](CrmApi.md#getCustomer) | **GET** /api/v1/accounts/{accountId}/crm/customers/{customerId} |  |
| [**listCustomers()**](CrmApi.md#listCustomers) | **GET** /api/v1/accounts/{accountId}/crm/customers |  |
| [**updateCustomer()**](CrmApi.md#updateCustomer) | **PATCH** /api/v1/accounts/{accountId}/crm/customers/{customerId} |  |


## `createCustomer()`

```php
createCustomer($account_id, $create_customer_request): \KuziumOrbitClient\Model\CustomerResponse
```



### Example

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

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**|  | |
| **create_customer_request** | [**\KuziumOrbitClient\Model\CreateCustomerRequest**](../Model/CreateCustomerRequest.md)|  | |

### Return type

[**\KuziumOrbitClient\Model\CustomerResponse**](../Model/CustomerResponse.md)

### Authorization

[ApiKey](../../README.md#ApiKey)

### HTTP request headers

- **Content-Type**: `application/json`, `text/json`, `application/*+json`
- **Accept**: `text/plain`, `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteCustomer()`

```php
deleteCustomer($account_id, $customer_id)
```



### Example

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
$customer_id = 'customer_id_example'; // string

try {
    $apiInstance->deleteCustomer($account_id, $customer_id);
} catch (Exception $e) {
    echo 'Exception when calling CrmApi->deleteCustomer: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**|  | |
| **customer_id** | **string**|  | |

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

## `getCustomer()`

```php
getCustomer($account_id, $customer_id): \KuziumOrbitClient\Model\CustomerResponse
```



### Example

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
$customer_id = 'customer_id_example'; // string

try {
    $result = $apiInstance->getCustomer($account_id, $customer_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CrmApi->getCustomer: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**|  | |
| **customer_id** | **string**|  | |

### Return type

[**\KuziumOrbitClient\Model\CustomerResponse**](../Model/CustomerResponse.md)

### Authorization

[ApiKey](../../README.md#ApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `text/plain`, `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listCustomers()`

```php
listCustomers($account_id, $status, $search, $filter, $page, $page_size, $sort_by, $sort_order): \KuziumOrbitClient\Model\PagedResultOfCustomerResponse
```



### Example

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
$status = 'status_example'; // string
$search = 'search_example'; // string
$filter = 'filter_example'; // string
$page = 56; // int
$page_size = 56; // int
$sort_by = 'name'; // string
$sort_order = 'asc'; // string

try {
    $result = $apiInstance->listCustomers($account_id, $status, $search, $filter, $page, $page_size, $sort_by, $sort_order);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CrmApi->listCustomers: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**|  | |
| **status** | **string**|  | [optional] |
| **search** | **string**|  | [optional] |
| **filter** | **string**|  | [optional] |
| **page** | **int**|  | [optional] |
| **page_size** | **int**|  | [optional] |
| **sort_by** | **string**|  | [optional] [default to &#39;name&#39;] |
| **sort_order** | **string**|  | [optional] [default to &#39;asc&#39;] |

### Return type

[**\KuziumOrbitClient\Model\PagedResultOfCustomerResponse**](../Model/PagedResultOfCustomerResponse.md)

### Authorization

[ApiKey](../../README.md#ApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `text/plain`, `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateCustomer()`

```php
updateCustomer($account_id, $customer_id, $update_customer_request): \KuziumOrbitClient\Model\CustomerResponse
```



### Example

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
$customer_id = 'customer_id_example'; // string
$update_customer_request = new \KuziumOrbitClient\Model\UpdateCustomerRequest(); // \KuziumOrbitClient\Model\UpdateCustomerRequest

try {
    $result = $apiInstance->updateCustomer($account_id, $customer_id, $update_customer_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CrmApi->updateCustomer: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**|  | |
| **customer_id** | **string**|  | |
| **update_customer_request** | [**\KuziumOrbitClient\Model\UpdateCustomerRequest**](../Model/UpdateCustomerRequest.md)|  | |

### Return type

[**\KuziumOrbitClient\Model\CustomerResponse**](../Model/CustomerResponse.md)

### Authorization

[ApiKey](../../README.md#ApiKey)

### HTTP request headers

- **Content-Type**: `application/json`, `text/json`, `application/*+json`
- **Accept**: `text/plain`, `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
