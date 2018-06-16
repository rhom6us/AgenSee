# IO.Swagger.Api.DefaultApi

All URIs are relative to *https://upz2qxo7x5.execute-api.us-east-1.amazonaws.com/uat*

Method | HTTP request | Description
------------- | ------------- | -------------
[**EformsMessageIdGet**](DefaultApi.md#eformsmessageidget) | **GET** /eforms/{messageId} | 
[**EformsPost**](DefaultApi.md#eformspost) | **POST** /eforms | 


<a name="eformsmessageidget"></a>
# **EformsMessageIdGet**
> byte[] EformsMessageIdGet (long? messageId)



### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class EformsMessageIdGetExample
    {
        public void main()
        {
            // Configure API key authorization: api_key
            Configuration.Default.AddApiKey("x-api-key", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("x-api-key", "Bearer");
            // Configure API key authorization: sigv4
            Configuration.Default.AddApiKey("Authorization", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Authorization", "Bearer");

            var apiInstance = new DefaultApi();
            var messageId = 789;  // long? | ID of message to fetch

            try
            {
                byte[] result = apiInstance.EformsMessageIdGet(messageId);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling DefaultApi.EformsMessageIdGet: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **messageId** | **long?**| ID of message to fetch | 

### Return type

**byte[]**

### Authorization

[api_key](../README.md#api_key), [sigv4](../README.md#sigv4)

### HTTP request headers

 - **Content-Type**: text/plain
 - **Accept**: application/xml, application/JSON

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="eformspost"></a>
# **EformsPost**
> List<EFormsMessage> EformsPost (string inpFormat, string outFormat, List<EFormsMessage> body, bool? merge = null)



### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class EformsPostExample
    {
        public void main()
        {
            // Configure API key authorization: api_key
            Configuration.Default.AddApiKey("x-api-key", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("x-api-key", "Bearer");
            // Configure API key authorization: sigv4
            Configuration.Default.AddApiKey("Authorization", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Authorization", "Bearer");

            var apiInstance = new DefaultApi();
            var inpFormat = inpFormat_example;  // string | 
            var outFormat = outFormat_example;  // string | 
            var body = new List<EFormsMessage>(); // List<EFormsMessage> | to process
            var merge = true;  // bool? |  (optional) 

            try
            {
                List&lt;EFormsMessage&gt; result = apiInstance.EformsPost(inpFormat, outFormat, body, merge);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling DefaultApi.EformsPost: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inpFormat** | **string**|  | 
 **outFormat** | **string**|  | 
 **body** | [**List&lt;EFormsMessage&gt;**](EFormsMessage.md)| to process | 
 **merge** | **bool?**|  | [optional] 

### Return type

[**List<EFormsMessage>**](EFormsMessage.md)

### Authorization

[api_key](../README.md#api_key), [sigv4](../README.md#sigv4)

### HTTP request headers

 - **Content-Type**: application/json, application/xml
 - **Accept**: application/xml, application/JSON

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

