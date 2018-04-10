# YNAB\Api\PayeeLocationsApi

All URIs are relative to *https://api.youneedabudget.com/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getPayeeLocationById**](PayeeLocationsApi.md#getPayeeLocationById) | **GET** /budgets/{budget_id}/payee_locations/{payee_location_id} | Single payee location
[**getPayeeLocations**](PayeeLocationsApi.md#getPayeeLocations) | **GET** /budgets/{budget_id}/payee_locations | List payee locations
[**getPayeeLocationsByPayee**](PayeeLocationsApi.md#getPayeeLocationsByPayee) | **GET** /budgets/{budget_id}/payees/{payee_id}/payee_locations | List locations for a payee


# **getPayeeLocationById**
> \YNAB\Api\Model\PayeeLocationResponse getPayeeLocationById($budgetId, $payeeLocationId)

Single payee location

Returns a single payee location

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: bearer
$config = YNAB\Api\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = YNAB\Api\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new YNAB\Api\Api\PayeeLocationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$budgetId = "budgetId_example"; // string | The ID of the Budget.
$payeeLocationId = "payeeLocationId_example"; // string | ID of payee location

try {
    $result = $apiInstance->getPayeeLocationById($budgetId, $payeeLocationId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PayeeLocationsApi->getPayeeLocationById: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **budgetId** | [**string**](../Model/.md)| The ID of the Budget. |
 **payeeLocationId** | [**string**](../Model/.md)| ID of payee location |

### Return type

[**\YNAB\Api\Model\PayeeLocationResponse**](../Model/PayeeLocationResponse.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getPayeeLocations**
> \YNAB\Api\Model\PayeeLocationsResponse getPayeeLocations($budgetId)

List payee locations

Returns all payee locations

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: bearer
$config = YNAB\Api\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = YNAB\Api\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new YNAB\Api\Api\PayeeLocationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$budgetId = "budgetId_example"; // string | The ID of the Budget.

try {
    $result = $apiInstance->getPayeeLocations($budgetId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PayeeLocationsApi->getPayeeLocations: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **budgetId** | [**string**](../Model/.md)| The ID of the Budget. |

### Return type

[**\YNAB\Api\Model\PayeeLocationsResponse**](../Model/PayeeLocationsResponse.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getPayeeLocationsByPayee**
> \YNAB\Api\Model\PayeeLocationsResponse getPayeeLocationsByPayee($budgetId, $payeeId)

List locations for a payee

Returns all payee locations for the specified payee

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: bearer
$config = YNAB\Api\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = YNAB\Api\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new YNAB\Api\Api\PayeeLocationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$budgetId = "budgetId_example"; // string | The ID of the Budget.
$payeeId = "payeeId_example"; // string | ID of payee

try {
    $result = $apiInstance->getPayeeLocationsByPayee($budgetId, $payeeId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PayeeLocationsApi->getPayeeLocationsByPayee: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **budgetId** | [**string**](../Model/.md)| The ID of the Budget. |
 **payeeId** | [**string**](../Model/.md)| ID of payee |

### Return type

[**\YNAB\Api\Model\PayeeLocationsResponse**](../Model/PayeeLocationsResponse.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

