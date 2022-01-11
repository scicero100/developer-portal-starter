## Logging Key Value Pair Definitions

This section describes the key value pair definitions required when logging

| Key            |Name |Value                          |Description                  
|----------------|------------|-------------------------------|-----------------------------|
|DTS			 |Date and Time Stamp|`[2021-10-27T08:51:02.8264455Z]`         |This is the date and time stamp in UTC of when the event took place.  ISO 8601 format 'yyyy-MM-ddTHH:mm:ss.fffffffZ'.            |
|CID|Correlation ID |`[a88c40e2-b677-4fa9-b883-02b51cb55961]`            |This is the Correlation ID, a unique value used to capture all logs associated with a transaction or series of events            |
|LLE|Log Level|`TRACE`<br>`DEBUG`<br>`INFO`<br>`WARNING`<br>`ERROR`<br>`CRITIAL`|Trace - Contain the most detailed messages. These messages may contain sensitive app data. These messages are disabled by default and should not be enabled in production.<br><br>Debug - For debugging and development. Use with caution in production due to the high volume.<br><br>Info - Tracks the general flow of the app. May have long-term value.<br><br>Warning - For abnormal or unexpected events. Typically includes errors or conditions that don't cause the app to fail.<br><br>Error - For errors and exceptions that cannot be handled. These messages indicate a failure in the current operation or request, not an app-wide failure.<br><br>Critial - For failures that require immediate attention. Examples: data loss scenarios, out of disk space.|STC|HTTP Status Code|`[200]`|If a Http response is returned, this specifies the HTTP Status Code
|SVC|Service Name|`RiskManagement`<br>`Cage`<br>`Identity`<br>`Reporting`<br>`SystemSetup`<br>`MerchantSetup`<br>`ServiceRepository`<br>`MerchantNotification`<br>`PSMerchantNotification`|Log entry related to which service
|VER|Version of Service|[1.1.0]|The unique version of the service
|MTI|Merchant Transaction ID|[This_is_my_merchant_transaction_id]|The unique Merchant Transaction  Identifier
|itm.{property}|Merchant Transaction ID|[itm.merchant=ACME<br>&itm.site=SITE-0001<br>&itm.merchantTransactionId=This_is_my_transaction_id<br>&itm.voucherNumber=1234567890<br>&itm.shopper.id=Shopper_01&]|Key Value pairs for each property in the item
|ECO|Error Code|`[INVALID_REQUEST]`|The Error Code if a handled error has occurred
|ERS|Error Reason|`[One or more validation errors occurred]`|The Error Reason if a handled error has occurred
|EXC|Exception|`[Index was outside the bounds of the array ...]`|The Exception Message and Inner Exception if an Unhandled error has occurred