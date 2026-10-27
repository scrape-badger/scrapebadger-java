# BatchApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**batchSubmitABatchOfAsyncRequests**](BatchApi.md#batchSubmitABatchOfAsyncRequests) | **POST** /v1/batch | Submit a batch of async requests |


<a id="batchSubmitABatchOfAsyncRequests"></a>
# **batchSubmitABatchOfAsyncRequests**
> Object batchSubmitABatchOfAsyncRequests(batchRequest)

Submit a batch of async requests

Submit up to 100 GET reads in one call. Each item runs as its own &#x60;&#x60;Prefer: respond-async&#x60;&#x60; request under this key, with the same auth, credit check, rate limit and billing as if it were sent alone, and returns a request_id to poll (or a webhook to &#x60;&#x60;callback_url&#x60;&#x60;). At most 10 items of a batch run at the same time. Submitting is free; each item bills as it runs. Items are checked against the spendable balance first, at the endpoint&#39;s base price, so a batch never starts more than the account can pay for.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.BatchApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    BatchApi apiInstance = new BatchApi(defaultClient);
    BatchRequest batchRequest = new BatchRequest(); // BatchRequest | 
    try {
      Object result = apiInstance.batchSubmitABatchOfAsyncRequests(batchRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BatchApi#batchSubmitABatchOfAsyncRequests");
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
| **batchRequest** | [**BatchRequest**](BatchRequest.md)|  | |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **202** | Successful Response |  -  |
| **422** | Validation Error |  -  |

