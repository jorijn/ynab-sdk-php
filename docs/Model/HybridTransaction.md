# HybridTransaction

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** |  | 
**date** | [**\DateTime**](\DateTime.md) |  | 
**amount** | **float** | The transaction amount in milliunits format | 
**cleared** | **string** | The cleared status of the transaction | 
**approved** | **bool** | Whether or not the transaction is approved | 
**flagColor** | **string** | The transaction flag | 
**accountId** | **string** |  | 
**payeeId** | **string** |  | 
**categoryId** | **string** |  | 
**transferAccountId** | **string** |  | 
**importId** | **string** | If the Transaction was imported, this field is a unique (by account) import identifier.  If this transaction was imported through File Based Import or Direct Import and not through the API, the import_id will have the format: &#39;YNAB:[milliunit_amount]:[iso_date]:[occurrence]&#39;.  For example, a transaction dated 2015-12-30 in the amount of -$294.23 USD would have an import_id of &#39;YNAB:-294230:2015-12-30:1&#39;.  If a second transaction on the same account was imported and had the same date and same amount, its import_id would be &#39;YNAB:-294230:2015-12-30:2&#39;. | 
**type** | **string** | Whether the hybrid transaction represents a regular transaction or a subtransaction | 
**parentTransactionId** | **string** | For subtransaction types, this is the id of the pararent transaction.  For transaction types, this id will be always be null. | 
**accountName** | **string** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


