# YNAB\BudgetsApi

All URIs are relative to *https://api.youneedabudget.com/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getBudgetById**](BudgetsApi.md#getBudgetById) | **GET** /budgets/{budget_id} | Single budget
[**getBudgetSettingsById**](BudgetsApi.md#getBudgetSettingsById) | **GET** /budgets/{budget_id}/settings | Budget Settings
[**getBudgets**](BudgetsApi.md#getBudgets) | **GET** /budgets | List budgets


# **getBudgetById**
> \YNAB\Model\BudgetDetailResponse getBudgetById($budgetId, $lastKnowledgeOfServer)

Single budget

Returns a single budget with all related entities.  This resource is effectively a full budget export.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: bearer
$config = YNAB\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = YNAB\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new YNAB\Api\BudgetsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$budgetId = "budgetId_example"; // string | The ID of the Budget.  \"last-used\" can also be used to specify the last used budget.
$lastKnowledgeOfServer = 56; // int | The starting server knowledge.  If provided, only entities that have changed since last_knowledge_of_server will be included.

try {
    $result = $apiInstance->getBudgetById($budgetId, $lastKnowledgeOfServer);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BudgetsApi->getBudgetById: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **budgetId** | [**string**](../Model/.md)| The ID of the Budget.  \&quot;last-used\&quot; can also be used to specify the last used budget. |
 **lastKnowledgeOfServer** | **int**| The starting server knowledge.  If provided, only entities that have changed since last_knowledge_of_server will be included. | [optional]

### Return type

[**\YNAB\Model\BudgetDetailResponse**](../Model/BudgetDetailResponse.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getBudgetSettingsById**
> \YNAB\Model\BudgetSettingsResponse getBudgetSettingsById($budgetId)

Budget Settings

Returns settings for a budget.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: bearer
$config = YNAB\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = YNAB\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new YNAB\Api\BudgetsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$budgetId = "budgetId_example"; // string | The ID of the Budget.  \"last-used\" can also be used to specify the last used budget.

try {
    $result = $apiInstance->getBudgetSettingsById($budgetId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BudgetsApi->getBudgetSettingsById: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **budgetId** | [**string**](../Model/.md)| The ID of the Budget.  \&quot;last-used\&quot; can also be used to specify the last used budget. |

### Return type

[**\YNAB\Model\BudgetSettingsResponse**](../Model/BudgetSettingsResponse.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getBudgets**
> \YNAB\Model\BudgetSummaryResponse getBudgets()

List budgets

Returns budgets list with summary information.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: bearer
$config = YNAB\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = YNAB\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new YNAB\Api\BudgetsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->getBudgets();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BudgetsApi->getBudgets: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\YNAB\Model\BudgetSummaryResponse**](../Model/BudgetSummaryResponse.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

