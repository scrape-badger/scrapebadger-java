# GitHubApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**githubGetProfile**](GitHubApi.md#githubGetProfile) | **GET** /v1/github/profiles/{username} | Get profile |


<a id="githubGetProfile"></a>
# **githubGetProfile**
> GitHubProfileResponse githubGetProfile(username, tab, year, page, nextPageToken)

Get profile

Public user or organization profile, pins/popular repositories, README and contributions.  The overview preserves GitHub&#39;s public website sections, including organization-specific metadata. Compact displayed counts are approximate and marked with *_approximate. Unavailable or blocked data is an unbilled error, never an empty success.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.GitHubApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    GitHubApi apiInstance = new GitHubApi(defaultClient);
    String username = "username_example"; // String | 
    String tab = "overview"; // String | Profile section; stars is available for users only
    Integer year = 56; // Integer | Overview only: 1970 through the current UTC year; activity is December or current month
    Integer page = 56; // Integer | Repositories only: page number, 30 rows per page
    String nextPageToken = "nextPageToken_example"; // String | Stars only: previous pagination.next_page_token
    try {
      GitHubProfileResponse result = apiInstance.githubGetProfile(username, tab, year, page, nextPageToken);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GitHubApi#githubGetProfile");
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
| **username** | **String**|  | |
| **tab** | **String**| Profile section; stars is available for users only | [optional] [default to overview] [enum: overview, repositories, stars] |
| **year** | **Integer**| Overview only: 1970 through the current UTC year; activity is December or current month | [optional] |
| **page** | **Integer**| Repositories only: page number, 30 rows per page | [optional] |
| **nextPageToken** | **String**| Stars only: previous pagination.next_page_token | [optional] |

### Return type

[**GitHubProfileResponse**](GitHubProfileResponse.md)

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

