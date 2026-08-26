# KuziumOrbitClient\SalesInvoiceApi



All URIs are relative to https://orbit.kuzium.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getSalesInvoice()**](SalesInvoiceApi.md#getSalesInvoice) | **GET** /api/v1/accounts/{accountId}/sales/invoices/{invoiceId} |  |
| [**listSalesInvoicePayments()**](SalesInvoiceApi.md#listSalesInvoicePayments) | **GET** /api/v1/accounts/{accountId}/sales/invoices/{invoiceId}/payments |  |
| [**listSalesInvoices()**](SalesInvoiceApi.md#listSalesInvoices) | **GET** /api/v1/accounts/{accountId}/sales/invoices |  |
| [**recordSalesInvoicePayment()**](SalesInvoiceApi.md#recordSalesInvoicePayment) | **POST** /api/v1/accounts/{accountId}/sales/invoices/{invoiceId}/payments |  |


## `getSalesInvoice()`

```php
getSalesInvoice($account_id, $invoice_id): \KuziumOrbitClient\Model\SalesInvoiceDetailDto
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKey
$config = KuziumOrbitClient\Configuration::getDefaultConfiguration()->setApiKey('X-Api-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = KuziumOrbitClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Api-Key', 'Bearer');


$apiInstance = new KuziumOrbitClient\Api\SalesInvoiceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string
$invoice_id = 'invoice_id_example'; // string

try {
    $result = $apiInstance->getSalesInvoice($account_id, $invoice_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SalesInvoiceApi->getSalesInvoice: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**|  | |
| **invoice_id** | **string**|  | |

### Return type

[**\KuziumOrbitClient\Model\SalesInvoiceDetailDto**](../Model/SalesInvoiceDetailDto.md)

### Authorization

[ApiKey](../../README.md#ApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `text/plain`, `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listSalesInvoicePayments()`

```php
listSalesInvoicePayments($account_id, $invoice_id): \KuziumOrbitClient\Model\SalesInvoicePaymentDto[]
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKey
$config = KuziumOrbitClient\Configuration::getDefaultConfiguration()->setApiKey('X-Api-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = KuziumOrbitClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Api-Key', 'Bearer');


$apiInstance = new KuziumOrbitClient\Api\SalesInvoiceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string
$invoice_id = 'invoice_id_example'; // string

try {
    $result = $apiInstance->listSalesInvoicePayments($account_id, $invoice_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SalesInvoiceApi->listSalesInvoicePayments: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**|  | |
| **invoice_id** | **string**|  | |

### Return type

[**\KuziumOrbitClient\Model\SalesInvoicePaymentDto[]**](../Model/SalesInvoicePaymentDto.md)

### Authorization

[ApiKey](../../README.md#ApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `text/plain`, `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listSalesInvoices()`

```php
listSalesInvoices($account_id, $customer_id, $status, $search, $filter, $page, $page_size, $sort_by, $sort_order): \KuziumOrbitClient\Model\PagedResultOfSalesInvoiceDto
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKey
$config = KuziumOrbitClient\Configuration::getDefaultConfiguration()->setApiKey('X-Api-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = KuziumOrbitClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Api-Key', 'Bearer');


$apiInstance = new KuziumOrbitClient\Api\SalesInvoiceApi(
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
$sort_by = 'invoicedate'; // string
$sort_order = 'desc'; // string

try {
    $result = $apiInstance->listSalesInvoices($account_id, $customer_id, $status, $search, $filter, $page, $page_size, $sort_by, $sort_order);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SalesInvoiceApi->listSalesInvoices: ', $e->getMessage(), PHP_EOL;
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
| **sort_by** | **string**|  | [optional] [default to &#39;invoicedate&#39;] |
| **sort_order** | **string**|  | [optional] [default to &#39;desc&#39;] |

### Return type

[**\KuziumOrbitClient\Model\PagedResultOfSalesInvoiceDto**](../Model/PagedResultOfSalesInvoiceDto.md)

### Authorization

[ApiKey](../../README.md#ApiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `text/plain`, `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `recordSalesInvoicePayment()`

```php
recordSalesInvoicePayment($account_id, $invoice_id, $record_invoice_payment_request): \KuziumOrbitClient\Model\SalesInvoicePaymentDto
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKey
$config = KuziumOrbitClient\Configuration::getDefaultConfiguration()->setApiKey('X-Api-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = KuziumOrbitClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Api-Key', 'Bearer');


$apiInstance = new KuziumOrbitClient\Api\SalesInvoiceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_id = 'account_id_example'; // string
$invoice_id = 'invoice_id_example'; // string
$record_invoice_payment_request = new \KuziumOrbitClient\Model\RecordInvoicePaymentRequest(); // \KuziumOrbitClient\Model\RecordInvoicePaymentRequest

try {
    $result = $apiInstance->recordSalesInvoicePayment($account_id, $invoice_id, $record_invoice_payment_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SalesInvoiceApi->recordSalesInvoicePayment: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_id** | **string**|  | |
| **invoice_id** | **string**|  | |
| **record_invoice_payment_request** | [**\KuziumOrbitClient\Model\RecordInvoicePaymentRequest**](../Model/RecordInvoicePaymentRequest.md)|  | |

### Return type

[**\KuziumOrbitClient\Model\SalesInvoicePaymentDto**](../Model/SalesInvoicePaymentDto.md)

### Authorization

[ApiKey](../../README.md#ApiKey)

### HTTP request headers

- **Content-Type**: `application/json`, `text/json`, `application/*+json`
- **Accept**: `text/plain`, `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
