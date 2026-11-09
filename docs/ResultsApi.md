# ResultsApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**resultsReReadAResultRemoved**](ResultsApi.md#resultsReReadAResultRemoved) | **GET** /v1/results/{result_id} | Re-read a result (removed) |


<a id="resultsReReadAResultRemoved"></a>
# **resultsReReadAResultRemoved**
> Object resultsReReadAResultRemoved(resultId)

Re-read a result (removed)

Removed (SCR-396): ScrapeBadger no longer stores results, so there is nothing to re-read. Always 410. Narrow a call with _jq / _fields / _max_items instead.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.ResultsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    ResultsApi apiInstance = new ResultsApi(defaultClient);
    String resultId = "resultId_example"; // String | 
    try {
      Object result = apiInstance.resultsReReadAResultRemoved(resultId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ResultsApi#resultsReReadAResultRemoved");
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
| **resultId** | **String**|  | |

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

