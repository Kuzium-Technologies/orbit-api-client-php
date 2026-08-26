# KuziumOrbitClient\PurchaseInvoiceApi



All URIs are relative to https://orbit.kuzium.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getPurchaseInvoice()**](PurchaseInvoiceApi.md#getPurchaseInvoice) | **GET** /api/v1/accounts/{accountId}/purchase/invoices/{invoiceId} |  |
| [**listPurchaseInvoicePayments()**](PurchaseInvoiceApi.md#listPurchaseInvoicePayments) | **GET** /api/v1/accounts/{accountId}/purchase/invoices/{invoiceId}/payments |  |
| [**listPurchaseInvoices()**](PurchaseInvoiceApi.md#listPurchaseInvoices) | **GET** /api/v1/accounts/{accountId}/purchase/invoices |  |
| [**recordPurchaseInvoicePayment()**](PurchaseInvoiceApi.md#recordPurchaseInvoicePayment) | **POST** /api/v1/accounts/{accountId}/purchase/invoices/{invoiceId}/payments |  |


## `getPurchaseInvoice()`

```php
getPurchaseInvoice($account_id, $invoice_id): \KuziumOrbitClient\Model\PurchaseInvoiceDetailDto
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKey
$config = KuziumOrbitClient\Configuration::getDefaultConfiguration()->setApiKey('X-Api-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = KuziumOrbitClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Api-Key', 'Bearer');


$apiInstance = new KuziumOrbitClient\Api\PurchaseInvoiceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string
$invoice_id = 'invoice_id_example'; // string

try {
    $result = $apiInstance->getPurchaseInvoice($account_id, $invoice_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PurchaseInvoiceApi->getPurchaseInvoice: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**|  | |
| **invoice_id** | **string**|  | |

### Return type

[**\KuziumOrbitClient\Model\PurchaseInvoiceDetailDto**](../Model/PurchaseInvoiceDetailDto.md)

### Authorization

[ApiKey](../../README.md#ApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `text/plain`, `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listPurchaseInvoicePayments()`

```php
listPurchaseInvoicePayments($account_id, $invoice_id): \KuziumOrbitClient\Model\PurchaseInvoicePaymentDto[]
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKey
$config = KuziumOrbitClient\Configuration::getDefaultConfiguration()->setApiKey('X-Api-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = KuziumOrbitClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Api-Key', 'Bearer');


$apiInstance = new KuziumOrbitClient\Api\PurchaseInvoiceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string
$invoice_id = 'invoice_id_example'; // string

try {
    $result = $apiInstance->listPurchaseInvoicePayments($account_id, $invoice_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PurchaseInvoiceApi->listPurchaseInvoicePayments: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**|  | |
| **invoice_id** | **string**|  | |

### Return type

[**\KuziumOrbitClient\Model\PurchaseInvoicePaymentDto[]**](../Model/PurchaseInvoicePaymentDto.md)

### Authorization

[ApiKey](../../README.md#ApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `text/plain`, `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listPurchaseInvoices()`

```php
listPurchaseInvoices($account_id, $search, $status, $filter, $page, $page_size): \KuziumOrbitClient\Model\PagedResultOfPurchaseInvoiceDto
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKey
$config = KuziumOrbitClient\Configuration::getDefaultConfiguration()->setApiKey('X-Api-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = KuziumOrbitClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Api-Key', 'Bearer');


$apiInstance = new KuziumOrbitClient\Api\PurchaseInvoiceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string
$search = 'search_example'; // string
$status = 'status_example'; // string
$filter = 'filter_example'; // string
$page = 1; // int
$page_size = 0; // int

try {
    $result = $apiInstance->listPurchaseInvoices($account_id, $search, $status, $filter, $page, $page_size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PurchaseInvoiceApi->listPurchaseInvoices: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**|  | |
| **search** | **string**|  | [optional] |
| **status** | **string**|  | [optional] |
| **filter** | **string**|  | [optional] |
| **page** | **int**|  | [optional] [default to 1] |
| **page_size** | **int**|  | [optional] [default to 0] |

### Return type

[**\KuziumOrbitClient\Model\PagedResultOfPurchaseInvoiceDto**](../Model/PagedResultOfPurchaseInvoiceDto.md)

### Authorization

[ApiKey](../../README.md#ApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `text/plain`, `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `recordPurchaseInvoicePayment()`

```php
recordPurchaseInvoicePayment($account_id, $invoice_id, $record_purchase_invoice_payment_request): \KuziumOrbitClient\Model\PurchaseInvoicePaymentDto
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKey
$config = KuziumOrbitClient\Configuration::getDefaultConfiguration()->setApiKey('X-Api-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = KuziumOrbitClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Api-Key', 'Bearer');


$apiInstance = new KuziumOrbitClient\Api\PurchaseInvoiceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string
$invoice_id = 'invoice_id_example'; // string
$record_purchase_invoice_payment_request = new \KuziumOrbitClient\Model\RecordPurchaseInvoicePaymentRequest(); // \KuziumOrbitClient\Model\RecordPurchaseInvoicePaymentRequest

try {
    $result = $apiInstance->recordPurchaseInvoicePayment($account_id, $invoice_id, $record_purchase_invoice_payment_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PurchaseInvoiceApi->recordPurchaseInvoicePayment: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**|  | |
| **invoice_id** | **string**|  | |
| **record_purchase_invoice_payment_request** | [**\KuziumOrbitClient\Model\RecordPurchaseInvoicePaymentRequest**](../Model/RecordPurchaseInvoicePaymentRequest.md)|  | |

### Return type

[**\KuziumOrbitClient\Model\PurchaseInvoicePaymentDto**](../Model/PurchaseInvoicePaymentDto.md)

### Authorization

[ApiKey](../../README.md#ApiKey)

### HTTP request headers

- **Content-Type**: `application/json`, `text/json`, `application/*+json`
- **Accept**: `text/plain`, `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
