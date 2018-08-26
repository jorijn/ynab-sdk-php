# HybridTransaction

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** |  | 
**date** | [**\DateTime**](\DateTime.md) |  | 
**amount** | **int** | The transaction amount in milliunits format | 
**cleared** | **string** | The cleared status of the transaction | 
**approved** | **bool** | Whether or not the transaction is approved | 
**accountId** | **string** |  | 
**deleted** | **bool** | Whether or not the transaction has been deleted.  Deleted transactions will only be included in delta requests. | 
**type** | **string** | Whether the hybrid transaction represents a regular transaction or a subtransaction | 
**accountName** | **string** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


