# RequestsApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**requestsPollAnAsyncRequest**](RequestsApi.md#requestsPollAnAsyncRequest) | **GET** /v1/requests/{request_id} | Poll an async request |


<a id="requestsPollAnAsyncRequest"></a>
# **requestsPollAnAsyncRequest**
> Object requestsPollAnAsyncRequest(requestId)

Poll an async request

Status or final response of a call made with &#x60;&#x60;Prefer: respond-async&#x60;&#x60;. While it runs: 202. When done: the original status, headers and body.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.RequestsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    RequestsApi apiInstance = new RequestsApi(defaultClient);
    String requestId = "requestId_example"; // String | 
    try {
      Object result = apiInstance.requestsPollAnAsyncRequest(requestId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling RequestsApi#requestsPollAnAsyncRequest");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **requestId** | **String**|  | |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |

