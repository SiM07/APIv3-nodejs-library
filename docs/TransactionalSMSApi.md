# SibApiV3Sdk.TransactionalSMSApi

All URIs are relative to *https://api.sendinblue.com/v3*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getSmsEvents**](TransactionalSMSApi.md#getSmsEvents) | **GET** /transactionalSMS/statistics/events | Get all the SMS activity (unaggregated events)
[**getTransacAggregatedSmsReport**](TransactionalSMSApi.md#getTransacAggregatedSmsReport) | **GET** /transactionalSMS/statistics/aggregatedReport | Get your SMS activity aggregated over a period of time
[**getTransacSmsReport**](TransactionalSMSApi.md#getTransacSmsReport) | **GET** /transactionalSMS/statistics/reports | Get your SMS activity aggregated per day
[**sendTransacSms**](TransactionalSMSApi.md#sendTransacSms) | **POST** /transactionalSMS/sms | Send the SMS campaign to the specified mobile number


<a name="getSmsEvents"></a>
# **getSmsEvents**
> GetSmsEventReport getSmsEvents(opts)

Get all the SMS activity (unaggregated events)

### Example
```javascript
var SibApiV3Sdk = require('sib-api-v3-sdk');
var defaultClient = SibApiV3Sdk.ApiClient.instance;

// Configure API key authorization: api-key
var apiKey = defaultClient.authentications['api-key'];
apiKey.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//apiKey.apiKeyPrefix = 'Token';

var apiInstance = new SibApiV3Sdk.TransactionalSMSApi();

var opts = { 
  'limit': 50, // Number | Number of documents per page
  'startDate': new Date("2013-10-20"), // Date | Mandatory if endDate is used. Starting date (YYYY-MM-DD) of the report
  'endDate': new Date("2013-10-20"), // Date | Mandatory if startDate is used. Ending date (YYYY-MM-DD) of the report
  'offset': 0, // Number | Index of the first document of the page
  'days': 56, // Number | Number of days in the past including today (positive integer). Not compatible with 'startDate' and 'endDate'
  'phoneNumber': "phoneNumber_example", // String | Filter the report for a specific phone number
  'event': "event_example", // String | Filter the report for specific events
  'tags': "tags_example" // String | Filter the report for specific tags passed as a serialized urlencoded array
};
apiInstance.getSmsEvents(opts).then(function(data) {
  console.log('API called successfully. Returned data: ' + data);
}, function(error) {
  console.error(error);
});

```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **limit** | **Number**| Number of documents per page | [optional] [default to 50]
 **startDate** | **Date**| Mandatory if endDate is used. Starting date (YYYY-MM-DD) of the report | [optional] 
 **endDate** | **Date**| Mandatory if startDate is used. Ending date (YYYY-MM-DD) of the report | [optional] 
 **offset** | **Number**| Index of the first document of the page | [optional] [default to 0]
 **days** | **Number**| Number of days in the past including today (positive integer). Not compatible with &#39;startDate&#39; and &#39;endDate&#39; | [optional] 
 **phoneNumber** | **String**| Filter the report for a specific phone number | [optional] 
 **event** | **String**| Filter the report for specific events | [optional] 
 **tags** | **String**| Filter the report for specific tags passed as a serialized urlencoded array | [optional] 

### Return type

[**GetSmsEventReport**](GetSmsEventReport.md)

### Authorization

[api-key](../README.md#api-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="getTransacAggregatedSmsReport"></a>
# **getTransacAggregatedSmsReport**
> GetTransacAggregatedSmsReport getTransacAggregatedSmsReport(opts)

Get your SMS activity aggregated over a period of time

### Example
```javascript
var SibApiV3Sdk = require('sib-api-v3-sdk');
var defaultClient = SibApiV3Sdk.ApiClient.instance;

// Configure API key authorization: api-key
var apiKey = defaultClient.authentications['api-key'];
apiKey.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//apiKey.apiKeyPrefix = 'Token';

var apiInstance = new SibApiV3Sdk.TransactionalSMSApi();

var opts = { 
  'startDate': new Date("2013-10-20"), // Date | Mandatory if endDate is used. Starting date (YYYY-MM-DD) of the report
  'endDate': new Date("2013-10-20"), // Date | Mandatory if startDate is used. Ending date (YYYY-MM-DD) of the report
  'days': 56, // Number | Number of days in the past including today (positive integer). Not compatible with startDate and endDate
  'tag': "tag_example" // String | Filter on a tag
};
apiInstance.getTransacAggregatedSmsReport(opts).then(function(data) {
  console.log('API called successfully. Returned data: ' + data);
}, function(error) {
  console.error(error);
});

```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **startDate** | **Date**| Mandatory if endDate is used. Starting date (YYYY-MM-DD) of the report | [optional] 
 **endDate** | **Date**| Mandatory if startDate is used. Ending date (YYYY-MM-DD) of the report | [optional] 
 **days** | **Number**| Number of days in the past including today (positive integer). Not compatible with startDate and endDate | [optional] 
 **tag** | **String**| Filter on a tag | [optional] 

### Return type

[**GetTransacAggregatedSmsReport**](GetTransacAggregatedSmsReport.md)

### Authorization

[api-key](../README.md#api-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="getTransacSmsReport"></a>
# **getTransacSmsReport**
> GetTransacSmsReport getTransacSmsReport(opts)

Get your SMS activity aggregated per day

### Example
```javascript
var SibApiV3Sdk = require('sib-api-v3-sdk');
var defaultClient = SibApiV3Sdk.ApiClient.instance;

// Configure API key authorization: api-key
var apiKey = defaultClient.authentications['api-key'];
apiKey.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//apiKey.apiKeyPrefix = 'Token';

var apiInstance = new SibApiV3Sdk.TransactionalSMSApi();

var opts = { 
  'startDate': new Date("2013-10-20"), // Date | Mandatory if endDate is used. Starting date (YYYY-MM-DD) of the report
  'endDate': new Date("2013-10-20"), // Date | Mandatory if startDate is used. Ending date (YYYY-MM-DD) of the report
  'days': 56, // Number | Number of days in the past including today (positive integer). Not compatible with 'startDate' and 'endDate'
  'tag': "tag_example" // String | Filter on a tag
};
apiInstance.getTransacSmsReport(opts).then(function(data) {
  console.log('API called successfully. Returned data: ' + data);
}, function(error) {
  console.error(error);
});

```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **startDate** | **Date**| Mandatory if endDate is used. Starting date (YYYY-MM-DD) of the report | [optional] 
 **endDate** | **Date**| Mandatory if startDate is used. Ending date (YYYY-MM-DD) of the report | [optional] 
 **days** | **Number**| Number of days in the past including today (positive integer). Not compatible with &#39;startDate&#39; and &#39;endDate&#39; | [optional] 
 **tag** | **String**| Filter on a tag | [optional] 

### Return type

[**GetTransacSmsReport**](GetTransacSmsReport.md)

### Authorization

[api-key](../README.md#api-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="sendTransacSms"></a>
# **sendTransacSms**
> SendSms sendTransacSms(sendTransacSms)

Send the SMS campaign to the specified mobile number

### Example
```javascript
var SibApiV3Sdk = require('sib-api-v3-sdk');
var defaultClient = SibApiV3Sdk.ApiClient.instance;

// Configure API key authorization: api-key
var apiKey = defaultClient.authentications['api-key'];
apiKey.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//apiKey.apiKeyPrefix = 'Token';

var apiInstance = new SibApiV3Sdk.TransactionalSMSApi();

var sendTransacSms = new SibApiV3Sdk.SendTransacSms(); // SendTransacSms | Values to send a transactional SMS

apiInstance.sendTransacSms(sendTransacSms).then(function(data) {
  console.log('API called successfully. Returned data: ' + data);
}, function(error) {
  console.error(error);
});

```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **sendTransacSms** | [**SendTransacSms**](SendTransacSms.md)| Values to send a transactional SMS | 

### Return type

[**SendSms**](SendSms.md)

### Authorization

[api-key](../README.md#api-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

