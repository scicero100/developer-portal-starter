## Logging Key Value Pair Definitions

This section describes the key value pair definitions required when logging

| Key            |Name |Value                          |Description                  
|----------------|------------|-------------------------------|-----------------------------|
|DTS			 |Date and Time Stamp|`[2021-10-27T08:51:02.8264455Z]`         |This is the date and time stamp in UTC of when the event took place.  ISO 8601 format 'yyyy-MM-ddTHH:mm:ss.fffffffZ'.            |
|CID|Correlation ID |`[a88c40e2-b677-4fa9-b883-02b51cb55961]`            |This is the Correlation ID, a unique value used to capture all logs associated with a transaction or series of events            |
|LLE|Log Level|`-- is en-dash, --- is em-dash`|-- is en-dash, --- is em-dash|
|STC|HTTP Status Code|`[200]`|If a Http response is returned, this specifies the HTTP Status Code
|SVC|Service Name|`RiskManagement` `Cage` `Identity` `Reporting` `SystemSetup` `MerchantSetup` `ServiceRepository` `MerchantNotification` `PSMerchantNotification`|Log entry related to which service
|MTI|Merchant Transaction ID|[This_is_my_merchant_transaction_id]|The unique Merchant Transaction  Identifier
|itm.{property}|Merchant Transaction ID|`[itm.merchant=ACME&itm.site=ACME-0000001&itm.merchantTransactionId=This_is_my_transaction_id&itm.voucherId=1232322232&itm.shopper.id=1ed768bb-e88a-4636-91ae-67927ccbb02b&]`|Key Value pairs for each property in the item
|ECO|Error Code|`[INVALID_REQUEST]`|The Error Code if a handled error has occurred
|ERS|Error Reason|`[One or more validation errors occurred]`|The Error Reason if a handled error has occurred
|EXC|Exception|`[Index was outside the bounds of the array ...]`|The Exception Message and Inner Exception if an Unhandled error has occurred