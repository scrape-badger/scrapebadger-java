# RedditApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**redditGetCrossPosts**](RedditApi.md#redditGetCrossPosts) | **GET** /v1/reddit/posts/{post_id}/duplicates | Get cross-posts |
| [**redditGetPostComments**](RedditApi.md#redditGetPostComments) | **GET** /v1/reddit/posts/{post_id}/comments | Get post comments |
| [**redditGetPostDetail**](RedditApi.md#redditGetPostDetail) | **GET** /v1/reddit/posts/{post_id} | Get post detail |
| [**redditGetPostsByDomain**](RedditApi.md#redditGetPostsByDomain) | **GET** /v1/reddit/domains/{domain}/posts | Get posts by domain |
| [**redditGetSubredditInfo**](RedditApi.md#redditGetSubredditInfo) | **GET** /v1/reddit/subreddits/{subreddit} | Get subreddit info |
| [**redditGetSubredditPosts**](RedditApi.md#redditGetSubredditPosts) | **GET** /v1/reddit/subreddits/{subreddit}/posts | Get subreddit posts |
| [**redditGetSubredditRules**](RedditApi.md#redditGetSubredditRules) | **GET** /v1/reddit/subreddits/{subreddit}/rules | Get subreddit rules |
| [**redditGetTrendingPosts**](RedditApi.md#redditGetTrendingPosts) | **GET** /v1/reddit/posts/trending | Get trending posts |
| [**redditGetUserProfile**](RedditApi.md#redditGetUserProfile) | **GET** /v1/reddit/users/{username} | Get user profile |
| [**redditGetUserSComments**](RedditApi.md#redditGetUserSComments) | **GET** /v1/reddit/users/{username}/comments | Get user&#39;s comments |
| [**redditGetUserSModeratedSubreddits**](RedditApi.md#redditGetUserSModeratedSubreddits) | **GET** /v1/reddit/users/{username}/moderated | Get user&#39;s moderated subreddits |
| [**redditGetUserSPosts**](RedditApi.md#redditGetUserSPosts) | **GET** /v1/reddit/users/{username}/posts | Get user&#39;s posts |
| [**redditGetUserSTrophies**](RedditApi.md#redditGetUserSTrophies) | **GET** /v1/reddit/users/{username}/trophies | Get user&#39;s trophies |
| [**redditGetWikiPageContent**](RedditApi.md#redditGetWikiPageContent) | **GET** /v1/reddit/subreddits/{subreddit}/wiki/{page} | Get wiki page content |
| [**redditListWikiPages**](RedditApi.md#redditListWikiPages) | **GET** /v1/reddit/subreddits/{subreddit}/wiki | List wiki pages |
| [**redditNewSubreddits**](RedditApi.md#redditNewSubreddits) | **GET** /v1/reddit/subreddits/new | New subreddits |
| [**redditPopularSubreddits**](RedditApi.md#redditPopularSubreddits) | **GET** /v1/reddit/subreddits/popular | Popular subreddits |
| [**redditRedditScraperHealthCheck**](RedditApi.md#redditRedditScraperHealthCheck) | **GET** /v1/reddit/health | Reddit scraper health check |
| [**redditRedditScraperHealthCheckHead**](RedditApi.md#redditRedditScraperHealthCheckHead) | **HEAD** /v1/reddit/health | Reddit scraper health check |
| [**redditSearchRedditPosts**](RedditApi.md#redditSearchRedditPosts) | **GET** /v1/reddit/search/posts | Search Reddit posts |
| [**redditSearchSubreddits**](RedditApi.md#redditSearchSubreddits) | **GET** /v1/reddit/search/subreddits | Search subreddits |
| [**redditSearchUsers**](RedditApi.md#redditSearchUsers) | **GET** /v1/reddit/search/users | Search users |


<a id="redditGetCrossPosts"></a>
# **redditGetCrossPosts**
> Object redditGetCrossPosts(postId, limit, after)

Get cross-posts

Get cross-posts and duplicates of a Reddit post.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.RedditApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    RedditApi apiInstance = new RedditApi(defaultClient);
    String postId = "postId_example"; // String | 
    Integer limit = 25; // Integer | 
    String after = "after_example"; // String | 
    try {
      Object result = apiInstance.redditGetCrossPosts(postId, limit, after);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling RedditApi#redditGetCrossPosts");
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
| **postId** | **String**|  | |
| **limit** | **Integer**|  | [optional] [default to 25] |
| **after** | **String**|  | [optional] |

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

<a id="redditGetPostComments"></a>
# **redditGetPostComments**
> Object redditGetPostComments(postId, sort, limit, depth)

Get post comments

Get comment tree for a Reddit post.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.RedditApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    RedditApi apiInstance = new RedditApi(defaultClient);
    String postId = "postId_example"; // String | 
    String sort = "confidence"; // String | Sort: confidence, top, new, controversial, old, qa
    Integer limit = 25; // Integer | 
    Integer depth = 56; // Integer | 
    try {
      Object result = apiInstance.redditGetPostComments(postId, sort, limit, depth);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling RedditApi#redditGetPostComments");
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
| **postId** | **String**|  | |
| **sort** | **String**| Sort: confidence, top, new, controversial, old, qa | [optional] [default to confidence] |
| **limit** | **Integer**|  | [optional] [default to 25] |
| **depth** | **Integer**|  | [optional] |

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

<a id="redditGetPostDetail"></a>
# **redditGetPostDetail**
> Object redditGetPostDetail(postId)

Get post detail

Get detailed information about a Reddit post.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.RedditApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    RedditApi apiInstance = new RedditApi(defaultClient);
    String postId = "postId_example"; // String | 
    try {
      Object result = apiInstance.redditGetPostDetail(postId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling RedditApi#redditGetPostDetail");
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
| **postId** | **String**|  | |

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

<a id="redditGetPostsByDomain"></a>
# **redditGetPostsByDomain**
> Object redditGetPostsByDomain(domain, sort, t, limit, after)

Get posts by domain

Get Reddit posts linking to a specific domain.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.RedditApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    RedditApi apiInstance = new RedditApi(defaultClient);
    String domain = "domain_example"; // String | 
    String sort = "hot"; // String | 
    String t = "all"; // String | 
    Integer limit = 25; // Integer | 
    String after = "after_example"; // String | 
    try {
      Object result = apiInstance.redditGetPostsByDomain(domain, sort, t, limit, after);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling RedditApi#redditGetPostsByDomain");
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
| **domain** | **String**|  | |
| **sort** | **String**|  | [optional] [default to hot] |
| **t** | **String**|  | [optional] [default to all] |
| **limit** | **Integer**|  | [optional] [default to 25] |
| **after** | **String**|  | [optional] |

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

<a id="redditGetSubredditInfo"></a>
# **redditGetSubredditInfo**
> Object redditGetSubredditInfo(subreddit)

Get subreddit info

Get detailed information about a subreddit.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.RedditApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    RedditApi apiInstance = new RedditApi(defaultClient);
    String subreddit = "subreddit_example"; // String | 
    try {
      Object result = apiInstance.redditGetSubredditInfo(subreddit);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling RedditApi#redditGetSubredditInfo");
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
| **subreddit** | **String**|  | |

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

<a id="redditGetSubredditPosts"></a>
# **redditGetSubredditPosts**
> Object redditGetSubredditPosts(subreddit, sort, t, limit, after)

Get subreddit posts

Get posts from a subreddit with sorting options.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.RedditApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    RedditApi apiInstance = new RedditApi(defaultClient);
    String subreddit = "subreddit_example"; // String | 
    String sort = "hot"; // String | Sort: hot, new, top, rising, controversial
    String t = "all"; // String | Time filter
    Integer limit = 25; // Integer | 
    String after = "after_example"; // String | 
    try {
      Object result = apiInstance.redditGetSubredditPosts(subreddit, sort, t, limit, after);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling RedditApi#redditGetSubredditPosts");
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
| **subreddit** | **String**|  | |
| **sort** | **String**| Sort: hot, new, top, rising, controversial | [optional] [default to hot] |
| **t** | **String**| Time filter | [optional] [default to all] |
| **limit** | **Integer**|  | [optional] [default to 25] |
| **after** | **String**|  | [optional] |

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

<a id="redditGetSubredditRules"></a>
# **redditGetSubredditRules**
> Object redditGetSubredditRules(subreddit)

Get subreddit rules

Get the rules of a subreddit.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.RedditApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    RedditApi apiInstance = new RedditApi(defaultClient);
    String subreddit = "subreddit_example"; // String | 
    try {
      Object result = apiInstance.redditGetSubredditRules(subreddit);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling RedditApi#redditGetSubredditRules");
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
| **subreddit** | **String**|  | |

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

<a id="redditGetTrendingPosts"></a>
# **redditGetTrendingPosts**
> Object redditGetTrendingPosts(sort, t, limit, after)

Get trending posts

Get trending posts from Reddit&#39;s front page.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.RedditApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    RedditApi apiInstance = new RedditApi(defaultClient);
    String sort = "hot"; // String | Sort: hot, new, top, rising, controversial, best
    String t = "day"; // String | Time filter
    Integer limit = 25; // Integer | 
    String after = "after_example"; // String | 
    try {
      Object result = apiInstance.redditGetTrendingPosts(sort, t, limit, after);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling RedditApi#redditGetTrendingPosts");
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
| **sort** | **String**| Sort: hot, new, top, rising, controversial, best | [optional] [default to hot] |
| **t** | **String**| Time filter | [optional] [default to day] |
| **limit** | **Integer**|  | [optional] [default to 25] |
| **after** | **String**|  | [optional] |

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

<a id="redditGetUserProfile"></a>
# **redditGetUserProfile**
> Object redditGetUserProfile(username)

Get user profile

Get a Reddit user&#39;s profile.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.RedditApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    RedditApi apiInstance = new RedditApi(defaultClient);
    String username = "username_example"; // String | 
    try {
      Object result = apiInstance.redditGetUserProfile(username);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling RedditApi#redditGetUserProfile");
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

<a id="redditGetUserSComments"></a>
# **redditGetUserSComments**
> Object redditGetUserSComments(username, sort, t, limit, after)

Get user&#39;s comments

Get comments by a Reddit user.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.RedditApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    RedditApi apiInstance = new RedditApi(defaultClient);
    String username = "username_example"; // String | 
    String sort = "new"; // String | 
    String t = "all"; // String | 
    Integer limit = 25; // Integer | 
    String after = "after_example"; // String | 
    try {
      Object result = apiInstance.redditGetUserSComments(username, sort, t, limit, after);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling RedditApi#redditGetUserSComments");
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
| **sort** | **String**|  | [optional] [default to new] |
| **t** | **String**|  | [optional] [default to all] |
| **limit** | **Integer**|  | [optional] [default to 25] |
| **after** | **String**|  | [optional] |

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

<a id="redditGetUserSModeratedSubreddits"></a>
# **redditGetUserSModeratedSubreddits**
> Object redditGetUserSModeratedSubreddits(username)

Get user&#39;s moderated subreddits

Get subreddits moderated by a user.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.RedditApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    RedditApi apiInstance = new RedditApi(defaultClient);
    String username = "username_example"; // String | 
    try {
      Object result = apiInstance.redditGetUserSModeratedSubreddits(username);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling RedditApi#redditGetUserSModeratedSubreddits");
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

<a id="redditGetUserSPosts"></a>
# **redditGetUserSPosts**
> Object redditGetUserSPosts(username, sort, t, limit, after)

Get user&#39;s posts

Get posts submitted by a Reddit user.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.RedditApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    RedditApi apiInstance = new RedditApi(defaultClient);
    String username = "username_example"; // String | 
    String sort = "new"; // String | 
    String t = "all"; // String | 
    Integer limit = 25; // Integer | 
    String after = "after_example"; // String | 
    try {
      Object result = apiInstance.redditGetUserSPosts(username, sort, t, limit, after);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling RedditApi#redditGetUserSPosts");
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
| **sort** | **String**|  | [optional] [default to new] |
| **t** | **String**|  | [optional] [default to all] |
| **limit** | **Integer**|  | [optional] [default to 25] |
| **after** | **String**|  | [optional] |

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

<a id="redditGetUserSTrophies"></a>
# **redditGetUserSTrophies**
> Object redditGetUserSTrophies(username)

Get user&#39;s trophies

Get a user&#39;s trophy case.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.RedditApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    RedditApi apiInstance = new RedditApi(defaultClient);
    String username = "username_example"; // String | 
    try {
      Object result = apiInstance.redditGetUserSTrophies(username);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling RedditApi#redditGetUserSTrophies");
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

<a id="redditGetWikiPageContent"></a>
# **redditGetWikiPageContent**
> Object redditGetWikiPageContent(subreddit, page)

Get wiki page content

Get the content of a specific wiki page.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.RedditApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    RedditApi apiInstance = new RedditApi(defaultClient);
    String subreddit = "subreddit_example"; // String | 
    String page = "page_example"; // String | 
    try {
      Object result = apiInstance.redditGetWikiPageContent(subreddit, page);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling RedditApi#redditGetWikiPageContent");
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
| **subreddit** | **String**|  | |
| **page** | **String**|  | |

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

<a id="redditListWikiPages"></a>
# **redditListWikiPages**
> Object redditListWikiPages(subreddit)

List wiki pages

List all wiki pages in a subreddit.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.RedditApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    RedditApi apiInstance = new RedditApi(defaultClient);
    String subreddit = "subreddit_example"; // String | 
    try {
      Object result = apiInstance.redditListWikiPages(subreddit);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling RedditApi#redditListWikiPages");
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
| **subreddit** | **String**|  | |

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

<a id="redditNewSubreddits"></a>
# **redditNewSubreddits**
> Object redditNewSubreddits(limit, after)

New subreddits

Get recently created subreddits.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.RedditApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    RedditApi apiInstance = new RedditApi(defaultClient);
    Integer limit = 25; // Integer | 
    String after = "after_example"; // String | 
    try {
      Object result = apiInstance.redditNewSubreddits(limit, after);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling RedditApi#redditNewSubreddits");
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
| **limit** | **Integer**|  | [optional] [default to 25] |
| **after** | **String**|  | [optional] |

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

<a id="redditPopularSubreddits"></a>
# **redditPopularSubreddits**
> Object redditPopularSubreddits(limit, after)

Popular subreddits

Get popular subreddits by subscriber count.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.RedditApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    RedditApi apiInstance = new RedditApi(defaultClient);
    Integer limit = 25; // Integer | 
    String after = "after_example"; // String | 
    try {
      Object result = apiInstance.redditPopularSubreddits(limit, after);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling RedditApi#redditPopularSubreddits");
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
| **limit** | **Integer**|  | [optional] [default to 25] |
| **after** | **String**|  | [optional] |

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

<a id="redditRedditScraperHealthCheck"></a>
# **redditRedditScraperHealthCheck**
> Object redditRedditScraperHealthCheck()

Reddit scraper health check

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.RedditApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    RedditApi apiInstance = new RedditApi(defaultClient);
    try {
      Object result = apiInstance.redditRedditScraperHealthCheck();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling RedditApi#redditRedditScraperHealthCheck");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters
This endpoint does not need any parameter.

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

<a id="redditRedditScraperHealthCheckHead"></a>
# **redditRedditScraperHealthCheckHead**
> Object redditRedditScraperHealthCheckHead()

Reddit scraper health check

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.RedditApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    RedditApi apiInstance = new RedditApi(defaultClient);
    try {
      Object result = apiInstance.redditRedditScraperHealthCheckHead();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling RedditApi#redditRedditScraperHealthCheckHead");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters
This endpoint does not need any parameter.

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

<a id="redditSearchRedditPosts"></a>
# **redditSearchRedditPosts**
> Object redditSearchRedditPosts(q, subreddit, sort, t, limit, after)

Search Reddit posts

Search Reddit posts globally or within a subreddit.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.RedditApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    RedditApi apiInstance = new RedditApi(defaultClient);
    String q = "q_example"; // String | Search query
    String subreddit = "subreddit_example"; // String | Restrict to subreddit
    String sort = "relevance"; // String | Sort: relevance, hot, top, new, comments
    String t = "all"; // String | Time: hour, day, week, month, year, all
    Integer limit = 25; // Integer | 
    String after = "after_example"; // String | 
    try {
      Object result = apiInstance.redditSearchRedditPosts(q, subreddit, sort, t, limit, after);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling RedditApi#redditSearchRedditPosts");
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
| **q** | **String**| Search query | |
| **subreddit** | **String**| Restrict to subreddit | [optional] |
| **sort** | **String**| Sort: relevance, hot, top, new, comments | [optional] [default to relevance] |
| **t** | **String**| Time: hour, day, week, month, year, all | [optional] [default to all] |
| **limit** | **Integer**|  | [optional] [default to 25] |
| **after** | **String**|  | [optional] |

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

<a id="redditSearchSubreddits"></a>
# **redditSearchSubreddits**
> Object redditSearchSubreddits(q, limit, after)

Search subreddits

Search for subreddits by keyword.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.RedditApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    RedditApi apiInstance = new RedditApi(defaultClient);
    String q = "q_example"; // String | Search query
    Integer limit = 25; // Integer | 
    String after = "after_example"; // String | 
    try {
      Object result = apiInstance.redditSearchSubreddits(q, limit, after);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling RedditApi#redditSearchSubreddits");
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
| **q** | **String**| Search query | |
| **limit** | **Integer**|  | [optional] [default to 25] |
| **after** | **String**|  | [optional] |

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

<a id="redditSearchUsers"></a>
# **redditSearchUsers**
> Object redditSearchUsers(q, limit, after)

Search users

Search for Reddit users.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.RedditApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    RedditApi apiInstance = new RedditApi(defaultClient);
    String q = "q_example"; // String | Search query
    Integer limit = 25; // Integer | 
    String after = "after_example"; // String | 
    try {
      Object result = apiInstance.redditSearchUsers(q, limit, after);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling RedditApi#redditSearchUsers");
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
| **q** | **String**| Search query | |
| **limit** | **Integer**|  | [optional] [default to 25] |
| **after** | **String**|  | [optional] |

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

