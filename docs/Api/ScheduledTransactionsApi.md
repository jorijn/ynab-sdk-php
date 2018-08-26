# YNAB\ScheduledTransactionsApi

All URIs are relative to *https://api.youneedabudget.com/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getScheduledTransactionById**](ScheduledTransactionsApi.md#getScheduledTransactionById) | **GET** /budgets/{budget_id}/scheduled_transactions/{scheduled_transaction_id} | Single scheduled transaction
[**getScheduledTransactions**](ScheduledTransactionsApi.md#getScheduledTransactions) | **GET** /budgets/{budget_id}/scheduled_transactions | List scheduled transactions


# **getScheduledTransactionById**
> \YNAB\Model\ScheduledTransactionResponse getScheduledTransactionById($budgetId, $scheduledTransactionId)

Single scheduled transaction

Returns a single scheduled transaction

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: bearer
$config = YNAB\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = YNAB\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new YNAB\Api\ScheduledTransactionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$budgetId = "budgetId_example"; // string | The ID of the Budget.  \"last-used\" can also be used to specify the last used budget.
$scheduledTransactionId = "scheduledTransactionId_example"; // string | The ID of the Scheduled Transaction.

try {
    $result = $apiInstance->getScheduledTransactionById($budgetId, $scheduledTransactionId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ScheduledTransactionsApi->getScheduledTransactionById: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **budgetId** | [**string**](../Model/.md)| The ID of the Budget.  \&quot;last-used\&quot; can also be used to specify the last used budget. |
 **scheduledTransactionId** | [**string**](../Model/.md)| The ID of the Scheduled Transaction. |

### Return type

[**\YNAB\Model\ScheduledTransactionResponse**](../Model/ScheduledTransactionResponse.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getScheduledTransactions**
> \YNAB\Model\ScheduledTransactionsResponse getScheduledTransactions($budgetId)

List scheduled transactions

Returns all scheduled transactions

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: bearer
$config = YNAB\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = YNAB\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new YNAB\Api\ScheduledTransactionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$budgetId = "budgetId_example"; // string | The ID of the Budget.  \"last-used\" can also be used to specify the last used budget.

try {
    $result = $apiInstance->getScheduledTransactions($budgetId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ScheduledTransactionsApi->getScheduledTransactions: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **budgetId** | [**string**](../Model/.md)| The ID of the Budget.  \&quot;last-used\&quot; can also be used to specify the last used budget. |

### Return type

[**\YNAB\Model\ScheduledTransactionsResponse**](../Model/ScheduledTransactionsResponse.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

