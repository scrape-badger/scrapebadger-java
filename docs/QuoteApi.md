# QuoteApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**quoteQuoteACall**](QuoteApi.md#quoteQuoteACall) | **POST** /v1/quote | Quote a call |


<a id="quoteQuoteACall"></a>
# **quoteQuoteACall**
> Object quoteQuoteACall(quoteRequest)

Quote a call

What a call would cost (credits and USD), whether its parameters are valid, and how long it usually takes. Free: nothing runs and nothing is charged.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.QuoteApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    QuoteApi apiInstance = new QuoteApi(defaultClient);
    QuoteRequest quoteRequest = new QuoteRequest(); // QuoteRequest | 
    try {
      Object result = apiInstance.quoteQuoteACall(quoteRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling QuoteApi#quoteQuoteACall");
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
| **quoteRequest** | [**QuoteRequest**](QuoteRequest.md)|  | |

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
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |

