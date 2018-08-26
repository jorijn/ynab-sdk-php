# ScheduledTransactionSummary

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** |  | 
**dateFirst** | [**\DateTime**](\DateTime.md) | The first date for which the Scheduled Transaction was scheduled. | 
**dateNext** | [**\DateTime**](\DateTime.md) | The next date for which the Scheduled Transaction is scheduled. | 
**frequency** | **string** |  | 
**amount** | **int** | The scheduled transaction amount in milliunits format | 
**accountId** | **string** |  | 
**deleted** | **bool** | Whether or not the scheduled transaction has been deleted.  Deleted scheduled transactions will only be included in delta requests. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


