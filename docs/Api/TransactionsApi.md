# YNAB\TransactionsApi

All URIs are relative to *https://api.youneedabudget.com/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**bulkCreateTransactions**](TransactionsApi.md#bulkCreateTransactions) | **POST** /budgets/{budget_id}/transactions/bulk | Bulk create transactions
[**createTransaction**](TransactionsApi.md#createTransaction) | **POST** /budgets/{budget_id}/transactions | Create new transaction
[**getTransactionById**](TransactionsApi.md#getTransactionById) | **GET** /budgets/{budget_id}/transactions/{transaction_id} | Single transaction
[**getTransactions**](TransactionsApi.md#getTransactions) | **GET** /budgets/{budget_id}/transactions | List transactions
[**getTransactionsByAccount**](TransactionsApi.md#getTransactionsByAccount) | **GET** /budgets/{budget_id}/accounts/{account_id}/transactions | List account transactions
[**getTransactionsByCategory**](TransactionsApi.md#getTransactionsByCategory) | **GET** /budgets/{budget_id}/categories/{category_id}/transactions | List category transactions
[**getTransactionsByPayee**](TransactionsApi.md#getTransactionsByPayee) | **GET** /budgets/{budget_id}/payees/{payee_id}/transactions | List payee transactions
[**updateTransaction**](TransactionsApi.md#updateTransaction) | **PUT** /budgets/{budget_id}/transactions/{transaction_id} | Updates an existing transaction


# **bulkCreateTransactions**
> \YNAB\Model\BulkResponse bulkCreateTransactions($budgetId, $transactions)

Bulk create transactions

Creates multiple transactions

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: bearer
$config = YNAB\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = YNAB\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new YNAB\Api\TransactionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$budgetId = "budgetId_example"; // string | The ID of the Budget.  \"last-used\" can also be used to specify the last used budget.
$transactions = new \YNAB\Model\BulkTransactions(); // \YNAB\Model\BulkTransactions | The list of Transactions to create.

try {
    $result = $apiInstance->bulkCreateTransactions($budgetId, $transactions);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TransactionsApi->bulkCreateTransactions: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **budgetId** | [**string**](../Model/.md)| The ID of the Budget.  \&quot;last-used\&quot; can also be used to specify the last used budget. |
 **transactions** | [**\YNAB\Model\BulkTransactions**](../Model/BulkTransactions.md)| The list of Transactions to create. |

### Return type

[**\YNAB\Model\BulkResponse**](../Model/BulkResponse.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **createTransaction**
> \YNAB\Model\TransactionResponse createTransaction($budgetId, $transaction)

Create new transaction

Creates a transaction

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: bearer
$config = YNAB\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = YNAB\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new YNAB\Api\TransactionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$budgetId = "budgetId_example"; // string | The ID of the Budget.  \"last-used\" can also be used to specify the last used budget.
$transaction = new \YNAB\Model\SaveTransactionWrapper(); // \YNAB\Model\SaveTransactionWrapper | The Transaction to create.

try {
    $result = $apiInstance->createTransaction($budgetId, $transaction);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TransactionsApi->createTransaction: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **budgetId** | [**string**](../Model/.md)| The ID of the Budget.  \&quot;last-used\&quot; can also be used to specify the last used budget. |
 **transaction** | [**\YNAB\Model\SaveTransactionWrapper**](../Model/SaveTransactionWrapper.md)| The Transaction to create. |

### Return type

[**\YNAB\Model\TransactionResponse**](../Model/TransactionResponse.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getTransactionById**
> \YNAB\Model\TransactionResponse getTransactionById($budgetId, $transactionId)

Single transaction

Returns a single transaction

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: bearer
$config = YNAB\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = YNAB\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new YNAB\Api\TransactionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$budgetId = "budgetId_example"; // string | The ID of the Budget.  \"last-used\" can also be used to specify the last used budget.
$transactionId = "transactionId_example"; // string | The ID of the Transaction.

try {
    $result = $apiInstance->getTransactionById($budgetId, $transactionId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TransactionsApi->getTransactionById: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **budgetId** | [**string**](../Model/.md)| The ID of the Budget.  \&quot;last-used\&quot; can also be used to specify the last used budget. |
 **transactionId** | [**string**](../Model/.md)| The ID of the Transaction. |

### Return type

[**\YNAB\Model\TransactionResponse**](../Model/TransactionResponse.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getTransactions**
> \YNAB\Model\TransactionsResponse getTransactions($budgetId, $sinceDate, $type)

List transactions

Returns budget transactions

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: bearer
$config = YNAB\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = YNAB\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new YNAB\Api\TransactionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$budgetId = "budgetId_example"; // string | The ID of the Budget.  \"last-used\" can also be used to specify the last used budget.
$sinceDate = new \DateTime("2013-10-20"); // \DateTime | Only return transactions on or after this date.
$type = "type_example"; // string | Only return transactions of a certain type ('uncategorized' and 'unapproved' are currently supported)

try {
    $result = $apiInstance->getTransactions($budgetId, $sinceDate, $type);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TransactionsApi->getTransactions: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **budgetId** | [**string**](../Model/.md)| The ID of the Budget.  \&quot;last-used\&quot; can also be used to specify the last used budget. |
 **sinceDate** | **\DateTime**| Only return transactions on or after this date. | [optional]
 **type** | **string**| Only return transactions of a certain type (&#39;uncategorized&#39; and &#39;unapproved&#39; are currently supported) | [optional]

### Return type

[**\YNAB\Model\TransactionsResponse**](../Model/TransactionsResponse.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getTransactionsByAccount**
> \YNAB\Model\TransactionsResponse getTransactionsByAccount($budgetId, $accountId, $sinceDate, $type)

List account transactions

Returns all transactions for a specified account

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: bearer
$config = YNAB\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = YNAB\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new YNAB\Api\TransactionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$budgetId = "budgetId_example"; // string | The ID of the Budget.  \"last-used\" can also be used to specify the last used budget.
$accountId = "accountId_example"; // string | The ID of the Account.
$sinceDate = new \DateTime("2013-10-20"); // \DateTime | Only return transactions on or after this date.
$type = "type_example"; // string | Only return transactions of a certain type (i.e. 'uncategorized', 'unapproved')

try {
    $result = $apiInstance->getTransactionsByAccount($budgetId, $accountId, $sinceDate, $type);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TransactionsApi->getTransactionsByAccount: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **budgetId** | [**string**](../Model/.md)| The ID of the Budget.  \&quot;last-used\&quot; can also be used to specify the last used budget. |
 **accountId** | [**string**](../Model/.md)| The ID of the Account. |
 **sinceDate** | **\DateTime**| Only return transactions on or after this date. | [optional]
 **type** | **string**| Only return transactions of a certain type (i.e. &#39;uncategorized&#39;, &#39;unapproved&#39;) | [optional]

### Return type

[**\YNAB\Model\TransactionsResponse**](../Model/TransactionsResponse.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getTransactionsByCategory**
> \YNAB\Model\HybridTransactionsResponse getTransactionsByCategory($budgetId, $categoryId, $sinceDate, $type)

List category transactions

Returns all transactions for a specified category

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: bearer
$config = YNAB\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = YNAB\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new YNAB\Api\TransactionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$budgetId = "budgetId_example"; // string | The ID of the Budget.  \"last-used\" can also be used to specify the last used budget.
$categoryId = "categoryId_example"; // string | The ID of the Category.
$sinceDate = new \DateTime("2013-10-20"); // \DateTime | Only return transactions on or after this date.
$type = "type_example"; // string | Only return transactions of a certain type (i.e. 'uncategorized', 'unapproved')

try {
    $result = $apiInstance->getTransactionsByCategory($budgetId, $categoryId, $sinceDate, $type);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TransactionsApi->getTransactionsByCategory: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **budgetId** | [**string**](../Model/.md)| The ID of the Budget.  \&quot;last-used\&quot; can also be used to specify the last used budget. |
 **categoryId** | [**string**](../Model/.md)| The ID of the Category. |
 **sinceDate** | **\DateTime**| Only return transactions on or after this date. | [optional]
 **type** | **string**| Only return transactions of a certain type (i.e. &#39;uncategorized&#39;, &#39;unapproved&#39;) | [optional]

### Return type

[**\YNAB\Model\HybridTransactionsResponse**](../Model/HybridTransactionsResponse.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getTransactionsByPayee**
> \YNAB\Model\HybridTransactionsResponse getTransactionsByPayee($budgetId, $payeeId, $sinceDate, $type)

List payee transactions

Returns all transactions for a specified payee

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: bearer
$config = YNAB\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = YNAB\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new YNAB\Api\TransactionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$budgetId = "budgetId_example"; // string | The ID of the Budget.  \"last-used\" can also be used to specify the last used budget.
$payeeId = "payeeId_example"; // string | The ID of the Payee.
$sinceDate = new \DateTime("2013-10-20"); // \DateTime | Only return transactions on or after this date.
$type = "type_example"; // string | Only return transactions of a certain type (i.e. 'uncategorized', 'unapproved')

try {
    $result = $apiInstance->getTransactionsByPayee($budgetId, $payeeId, $sinceDate, $type);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TransactionsApi->getTransactionsByPayee: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **budgetId** | [**string**](../Model/.md)| The ID of the Budget.  \&quot;last-used\&quot; can also be used to specify the last used budget. |
 **payeeId** | [**string**](../Model/.md)| The ID of the Payee. |
 **sinceDate** | **\DateTime**| Only return transactions on or after this date. | [optional]
 **type** | **string**| Only return transactions of a certain type (i.e. &#39;uncategorized&#39;, &#39;unapproved&#39;) | [optional]

### Return type

[**\YNAB\Model\HybridTransactionsResponse**](../Model/HybridTransactionsResponse.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **updateTransaction**
> \YNAB\Model\TransactionResponse updateTransaction($budgetId, $transactionId, $transaction)

Updates an existing transaction

Updates a transaction

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: bearer
$config = YNAB\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = YNAB\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new YNAB\Api\TransactionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$budgetId = "budgetId_example"; // string | The ID of the Budget.  \"last-used\" can also be used to specify the last used budget.
$transactionId = "transactionId_example"; // string | The ID of the Transaction.
$transaction = new \YNAB\Model\SaveTransactionWrapper(); // \YNAB\Model\SaveTransactionWrapper | The Transaction to update.

try {
    $result = $apiInstance->updateTransaction($budgetId, $transactionId, $transaction);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TransactionsApi->updateTransaction: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **budgetId** | [**string**](../Model/.md)| The ID of the Budget.  \&quot;last-used\&quot; can also be used to specify the last used budget. |
 **transactionId** | [**string**](../Model/.md)| The ID of the Transaction. |
 **transaction** | [**\YNAB\Model\SaveTransactionWrapper**](../Model/SaveTransactionWrapper.md)| The Transaction to update. |

### Return type

[**\YNAB\Model\TransactionResponse**](../Model/TransactionResponse.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

