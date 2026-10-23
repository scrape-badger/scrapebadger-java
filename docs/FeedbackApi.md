# FeedbackApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**feedbackReportABugOrSendFeedback**](FeedbackApi.md#feedbackReportABugOrSendFeedback) | **POST** /v1/feedback | Report a bug or send feedback |


<a id="feedbackReportABugOrSendFeedback"></a>
# **feedbackReportABugOrSendFeedback**
> Object feedbackReportABugOrSendFeedback(feedbackRequest)

Report a bug or send feedback

File a bug (wrong/empty result for valid input, misleading error, price mismatch) or feedback (an API or field you needed and couldn&#39;t find). Free, never billed. Pass the failing call&#39;s X-Request-ID so we can find it.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.FeedbackApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    FeedbackApi apiInstance = new FeedbackApi(defaultClient);
    FeedbackRequest feedbackRequest = new FeedbackRequest(); // FeedbackRequest | 
    try {
      Object result = apiInstance.feedbackReportABugOrSendFeedback(feedbackRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FeedbackApi#feedbackReportABugOrSendFeedback");
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
| **feedbackRequest** | [**FeedbackRequest**](FeedbackRequest.md)|  | |

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
| **201** | Successful Response |  -  |
| **422** | Validation Error |  -  |

