# KuziumOrbitClient\PaymentReceiptApi



All URIs are relative to https://orbit.kuzium.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createPaymentReceipt()**](PaymentReceiptApi.md#createPaymentReceipt) | **POST** /api/v1/accounts/{accountId}/payment-receipts |  |
| [**getPaymentReceipt()**](PaymentReceiptApi.md#getPaymentReceipt) | **GET** /api/v1/accounts/{accountId}/payment-receipts/{id} |  |
| [**getPaymentReceiptsSummary()**](PaymentReceiptApi.md#getPaymentReceiptsSummary) | **GET** /api/v1/accounts/{accountId}/payment-receipts/summary |  |
| [**listPaymentReceipts()**](PaymentReceiptApi.md#listPaymentReceipts) | **GET** /api/v1/accounts/{accountId}/payment-receipts |  |
| [**voidPaymentReceipt()**](PaymentReceiptApi.md#voidPaymentReceipt) | **POST** /api/v1/accounts/{accountId}/payment-receipts/{id}/void |  |


## `createPaymentReceipt()`

```php
createPaymentReceipt($account_id, $create_payment_receipt_request): \KuziumOrbitClient\Model\PaymentReceiptResponse
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKey
$config = KuziumOrbitClient\Configuration::getDefaultConfiguration()->setApiKey('X-Api-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = KuziumOrbitClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Api-Key', 'Bearer');


$apiInstance = new KuziumOrbitClient\Api\PaymentReceiptApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string
$create_payment_receipt_request = new \KuziumOrbitClient\Model\CreatePaymentReceiptRequest(); // \KuziumOrbitClient\Model\CreatePaymentReceiptRequest

try {
    $result = $apiInstance->createPaymentReceipt($account_id, $create_payment_receipt_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PaymentReceiptApi->createPaymentReceipt: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**|  | |
| **create_payment_receipt_request** | [**\KuziumOrbitClient\Model\CreatePaymentReceiptRequest**](../Model/CreatePaymentReceiptRequest.md)|  | |

### Return type

[**\KuziumOrbitClient\Model\PaymentReceiptResponse**](../Model/PaymentReceiptResponse.md)

### Authorization

[ApiKey](../../README.md#ApiKey)

### HTTP request headers

- **Content-Type**: `application/json`, `text/json`, `application/*+json`
- **Accept**: `text/plain`, `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getPaymentReceipt()`

```php
getPaymentReceipt($account_id, $id): \KuziumOrbitClient\Model\PaymentReceiptDetailResponse
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKey
$config = KuziumOrbitClient\Configuration::getDefaultConfiguration()->setApiKey('X-Api-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = KuziumOrbitClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Api-Key', 'Bearer');


$apiInstance = new KuziumOrbitClient\Api\PaymentReceiptApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string
$id = 'id_example'; // string

try {
    $result = $apiInstance->getPaymentReceipt($account_id, $id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PaymentReceiptApi->getPaymentReceipt: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**|  | |
| **id** | **string**|  | |

### Return type

[**\KuziumOrbitClient\Model\PaymentReceiptDetailResponse**](../Model/PaymentReceiptDetailResponse.md)

### Authorization

[ApiKey](../../README.md#ApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `text/plain`, `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getPaymentReceiptsSummary()`

```php
getPaymentReceiptsSummary($account_id, $search, $filter): \KuziumOrbitClient\Model\PaymentReceiptSummaryResponse
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKey
$config = KuziumOrbitClient\Configuration::getDefaultConfiguration()->setApiKey('X-Api-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = KuziumOrbitClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Api-Key', 'Bearer');


$apiInstance = new KuziumOrbitClient\Api\PaymentReceiptApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string
$search = 'search_example'; // string
$filter = 'filter_example'; // string

try {
    $result = $apiInstance->getPaymentReceiptsSummary($account_id, $search, $filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PaymentReceiptApi->getPaymentReceiptsSummary: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**|  | |
| **search** | **string**|  | [optional] |
| **filter** | **string**|  | [optional] |

### Return type

[**\KuziumOrbitClient\Model\PaymentReceiptSummaryResponse**](../Model/PaymentReceiptSummaryResponse.md)

### Authorization

[ApiKey](../../README.md#ApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `text/plain`, `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listPaymentReceipts()`

```php
listPaymentReceipts($account_id, $search, $type, $filter, $page, $page_size, $sort_by, $sort_order): \KuziumOrbitClient\Model\PagedResultOfPaymentReceiptResponse
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKey
$config = KuziumOrbitClient\Configuration::getDefaultConfiguration()->setApiKey('X-Api-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = KuziumOrbitClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Api-Key', 'Bearer');


$apiInstance = new KuziumOrbitClient\Api\PaymentReceiptApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string
$search = 'search_example'; // string
$type = 'type_example'; // string
$filter = 'filter_example'; // string
$page = 1; // int
$page_size = 0; // int
$sort_by = 'postingdate'; // string
$sort_order = 'desc'; // string

try {
    $result = $apiInstance->listPaymentReceipts($account_id, $search, $type, $filter, $page, $page_size, $sort_by, $sort_order);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PaymentReceiptApi->listPaymentReceipts: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**|  | |
| **search** | **string**|  | [optional] |
| **type** | **string**|  | [optional] |
| **filter** | **string**|  | [optional] |
| **page** | **int**|  | [optional] [default to 1] |
| **page_size** | **int**|  | [optional] [default to 0] |
| **sort_by** | **string**|  | [optional] [default to &#39;postingdate&#39;] |
| **sort_order** | **string**|  | [optional] [default to &#39;desc&#39;] |

### Return type

[**\KuziumOrbitClient\Model\PagedResultOfPaymentReceiptResponse**](../Model/PagedResultOfPaymentReceiptResponse.md)

### Authorization

[ApiKey](../../README.md#ApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `text/plain`, `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `voidPaymentReceipt()`

```php
voidPaymentReceipt($account_id, $id, $void_payment_receipt_request): \KuziumOrbitClient\Model\PaymentReceiptResponse
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKey
$config = KuziumOrbitClient\Configuration::getDefaultConfiguration()->setApiKey('X-Api-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = KuziumOrbitClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Api-Key', 'Bearer');


$apiInstance = new KuziumOrbitClient\Api\PaymentReceiptApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string
$id = 'id_example'; // string
$void_payment_receipt_request = new \KuziumOrbitClient\Model\VoidPaymentReceiptRequest(); // \KuziumOrbitClient\Model\VoidPaymentReceiptRequest

try {
    $result = $apiInstance->voidPaymentReceipt($account_id, $id, $void_payment_receipt_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PaymentReceiptApi->voidPaymentReceipt: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**|  | |
| **id** | **string**|  | |
| **void_payment_receipt_request** | [**\KuziumOrbitClient\Model\VoidPaymentReceiptRequest**](../Model/VoidPaymentReceiptRequest.md)|  | |

### Return type

[**\KuziumOrbitClient\Model\PaymentReceiptResponse**](../Model/PaymentReceiptResponse.md)

### Authorization

[ApiKey](../../README.md#ApiKey)

### HTTP request headers

- **Content-Type**: `application/json`, `text/json`, `application/*+json`
- **Accept**: `text/plain`, `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
