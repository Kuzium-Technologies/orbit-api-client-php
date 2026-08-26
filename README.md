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
      "url": "https://github.com/Kuzium-Technologies/orbit-api-client-php.git"
    }
  ],
  "require": {
    "Kuzium-Technologies/orbit-api-client-php": "*@dev"
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

All URIs are relative to *https://orbit.kuzium.com*

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
*ProductsApi* | [**createProduct**](docs/Api/ProductsApi.md#createproduct) | **POST** /api/v1/accounts/{accountId}/products | 
*ProductsApi* | [**deleteProduct**](docs/Api/ProductsApi.md#deleteproduct) | **DELETE** /api/v1/accounts/{accountId}/products/{id} | 
*ProductsApi* | [**getProduct**](docs/Api/ProductsApi.md#getproduct) | **GET** /api/v1/accounts/{accountId}/products/{id} | 
*ProductsApi* | [**listProducts**](docs/Api/ProductsApi.md#listproducts) | **GET** /api/v1/accounts/{accountId}/products | 
*ProductsApi* | [**updateProduct**](docs/Api/ProductsApi.md#updateproduct) | **PUT** /api/v1/accounts/{accountId}/products/{id} | 
*PurchaseApi* | [**createPurchaseOrder**](docs/Api/PurchaseApi.md#createpurchaseorder) | **POST** /api/v1/accounts/{accountId}/purchase/orders | 
*PurchaseApi* | [**deletePurchaseOrder**](docs/Api/PurchaseApi.md#deletepurchaseorder) | **DELETE** /api/v1/accounts/{accountId}/purchase/orders/{orderId} | 
*PurchaseApi* | [**getPurchaseOrder**](docs/Api/PurchaseApi.md#getpurchaseorder) | **GET** /api/v1/accounts/{accountId}/purchase/orders/{orderId} | 
*PurchaseApi* | [**listPurchaseOrders**](docs/Api/PurchaseApi.md#listpurchaseorders) | **GET** /api/v1/accounts/{accountId}/purchase/orders | 
*PurchaseApi* | [**updatePurchaseOrder**](docs/Api/PurchaseApi.md#updatepurchaseorder) | **PUT** /api/v1/accounts/{accountId}/purchase/orders/{orderId} | 
*PurchaseApi* | [**updatePurchaseOrderStatus**](docs/Api/PurchaseApi.md#updatepurchaseorderstatus) | **PATCH** /api/v1/accounts/{accountId}/purchase/orders/{orderId}/status | 
*PurchaseInvoiceApi* | [**getPurchaseInvoice**](docs/Api/PurchaseInvoiceApi.md#getpurchaseinvoice) | **GET** /api/v1/accounts/{accountId}/purchase/invoices/{invoiceId} | 
*PurchaseInvoiceApi* | [**listPurchaseInvoicePayments**](docs/Api/PurchaseInvoiceApi.md#listpurchaseinvoicepayments) | **GET** /api/v1/accounts/{accountId}/purchase/invoices/{invoiceId}/payments | 
*PurchaseInvoiceApi* | [**listPurchaseInvoices**](docs/Api/PurchaseInvoiceApi.md#listpurchaseinvoices) | **GET** /api/v1/accounts/{accountId}/purchase/invoices | 
*PurchaseInvoiceApi* | [**recordPurchaseInvoicePayment**](docs/Api/PurchaseInvoiceApi.md#recordpurchaseinvoicepayment) | **POST** /api/v1/accounts/{accountId}/purchase/invoices/{invoiceId}/payments | 
*SalesApi* | [**createSalesOrder**](docs/Api/SalesApi.md#createsalesorder) | **POST** /api/v1/accounts/{accountId}/sales/orders | 
*SalesApi* | [**deleteSalesOrder**](docs/Api/SalesApi.md#deletesalesorder) | **DELETE** /api/v1/accounts/{accountId}/sales/orders/{orderId} | 
*SalesApi* | [**getSalesOrder**](docs/Api/SalesApi.md#getsalesorder) | **GET** /api/v1/accounts/{accountId}/sales/orders/{orderId} | 
*SalesApi* | [**listSalesOrders**](docs/Api/SalesApi.md#listsalesorders) | **GET** /api/v1/accounts/{accountId}/sales/orders | 
*SalesApi* | [**updateSalesOrder**](docs/Api/SalesApi.md#updatesalesorder) | **PUT** /api/v1/accounts/{accountId}/sales/orders/{orderId} | 
*SalesApi* | [**updateSalesOrderStatus**](docs/Api/SalesApi.md#updatesalesorderstatus) | **PUT** /api/v1/accounts/{accountId}/sales/orders/{orderId}/status | 
*SalesInvoiceApi* | [**getSalesInvoice**](docs/Api/SalesInvoiceApi.md#getsalesinvoice) | **GET** /api/v1/accounts/{accountId}/sales/invoices/{invoiceId} | 
*SalesInvoiceApi* | [**listSalesInvoicePayments**](docs/Api/SalesInvoiceApi.md#listsalesinvoicepayments) | **GET** /api/v1/accounts/{accountId}/sales/invoices/{invoiceId}/payments | 
*SalesInvoiceApi* | [**listSalesInvoices**](docs/Api/SalesInvoiceApi.md#listsalesinvoices) | **GET** /api/v1/accounts/{accountId}/sales/invoices | 
*SalesInvoiceApi* | [**recordSalesInvoicePayment**](docs/Api/SalesInvoiceApi.md#recordsalesinvoicepayment) | **POST** /api/v1/accounts/{accountId}/sales/invoices/{invoiceId}/payments | 

## Models

- [CreateCustomerRequest](docs/Model/CreateCustomerRequest.md)
- [CreateProductRequest](docs/Model/CreateProductRequest.md)
- [CreatePurchaseOrderLineRequest](docs/Model/CreatePurchaseOrderLineRequest.md)
- [CreatePurchaseOrderRequest](docs/Model/CreatePurchaseOrderRequest.md)
- [CreateSalesOrderLineRequest](docs/Model/CreateSalesOrderLineRequest.md)
- [CreateSalesOrderRequest](docs/Model/CreateSalesOrderRequest.md)
- [CustomerResponse](docs/Model/CustomerResponse.md)
- [InventoryDashboardStats](docs/Model/InventoryDashboardStats.md)
- [InventoryItemResponse](docs/Model/InventoryItemResponse.md)
- [MeResponse](docs/Model/MeResponse.md)
- [PagedResultOfCustomerResponse](docs/Model/PagedResultOfCustomerResponse.md)
- [PagedResultOfProductResponse](docs/Model/PagedResultOfProductResponse.md)
- [PagedResultOfPurchaseInvoiceDto](docs/Model/PagedResultOfPurchaseInvoiceDto.md)
- [PagedResultOfPurchaseOrderResponse](docs/Model/PagedResultOfPurchaseOrderResponse.md)
- [PagedResultOfSalesInvoiceDto](docs/Model/PagedResultOfSalesInvoiceDto.md)
- [PagedResultOfSalesOrderDto](docs/Model/PagedResultOfSalesOrderDto.md)
- [ProductResponse](docs/Model/ProductResponse.md)
- [PurchaseInvoiceDetailDto](docs/Model/PurchaseInvoiceDetailDto.md)
- [PurchaseInvoiceDto](docs/Model/PurchaseInvoiceDto.md)
- [PurchaseInvoicePaymentDto](docs/Model/PurchaseInvoicePaymentDto.md)
- [PurchaseOrderLineResponse](docs/Model/PurchaseOrderLineResponse.md)
- [PurchaseOrderResponse](docs/Model/PurchaseOrderResponse.md)
- [RecordInvoicePaymentRequest](docs/Model/RecordInvoicePaymentRequest.md)
- [RecordPurchaseInvoicePaymentRequest](docs/Model/RecordPurchaseInvoicePaymentRequest.md)
- [SalesInvoiceDetailDto](docs/Model/SalesInvoiceDetailDto.md)
- [SalesInvoiceDto](docs/Model/SalesInvoiceDto.md)
- [SalesInvoicePaymentDto](docs/Model/SalesInvoicePaymentDto.md)
- [SalesOrder](docs/Model/SalesOrder.md)
- [SalesOrderDetailDto](docs/Model/SalesOrderDetailDto.md)
- [SalesOrderDto](docs/Model/SalesOrderDto.md)
- [SalesOrderLine](docs/Model/SalesOrderLine.md)
- [SalesOrderLineDto](docs/Model/SalesOrderLineDto.md)
- [UpdateCustomerRequest](docs/Model/UpdateCustomerRequest.md)
- [UpdateOrderStatusRequest](docs/Model/UpdateOrderStatusRequest.md)
- [UpdateProductRequest](docs/Model/UpdateProductRequest.md)
- [UpdatePurchaseOrderRequest](docs/Model/UpdatePurchaseOrderRequest.md)
- [UpdatePurchaseOrderStatusRequest](docs/Model/UpdatePurchaseOrderStatusRequest.md)
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
    - Package version: `0.2.0`
    - Generator version: `7.25.0`
- Build package: `org.openapitools.codegen.languages.PhpClientCodegen`
