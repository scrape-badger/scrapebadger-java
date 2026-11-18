# RequestsApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**requestsCallbackStatus**](RequestsApi.md#requestsCallbackStatus) | **GET** /v1/requests/{request_id}/callback | Callback status |
| [**requestsPollAnAsyncRequest**](RequestsApi.md#requestsPollAnAsyncRequest) | **GET** /v1/requests/{request_id} | Poll an async request |


<a id="requestsCallbackStatus"></a>
# **requestsCallbackStatus**
> AsyncCallbackStatus requestsCallbackStatus(requestId)

Callback status

Webhook delivery state of a call submitted with &#x60;X-Callback-URL&#x60; / &#x60;callback_url&#x60;: kept for 24 h. Free. &#x60;404 callback_not_found&#x60; for a request without a callback, of another account, or older than 24 h.

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
      AsyncCallbackStatus result = apiInstance.requestsCallbackStatus(requestId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling RequestsApi#requestsCallbackStatus");
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

[**AsyncCallbackStatus**](AsyncCallbackStatus.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **404** | &#x60;callback_not_found&#x60;. |  -  |

<a id="requestsPollAnAsyncRequest"></a>
# **requestsPollAnAsyncRequest**
> Object requestsPollAnAsyncRequest(requestId)

Poll an async request

Status or final response of a call made with &#x60;&#x60;Prefer: respond-async&#x60;&#x60;. While it runs: 202. When done: the original status, headers and body.  The final response carries &#x60;X-Callback-Status&#x60;, &#x60;X-Callback-Attempts&#x60; and &#x60;X-Callback-Error&#x60; for a call submitted with a callback; while it runs, the &#x60;202&#x60; body has a &#x60;callback&#x60; object. Full delivery state: &#x60;GET /v1/requests/{request_id}/callback&#x60;.

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
| **202** | The call is still running. |  * Location - &#x60;/v1/requests/{request_id}&#x60;. <br>  * Retry-After - Seconds until the next poll. <br>  |
| **404** | &#x60;request_not_found&#x60;: unknown, another account&#39;s, or expired. |  -  |

