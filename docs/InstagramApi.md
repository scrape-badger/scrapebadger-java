# InstagramApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**instagramAboutThisAccount**](InstagramApi.md#instagramAboutThisAccount) | **GET** /v1/instagram/users/{username}/about | About this account |
| [**instagramBlendedTopSearch**](InstagramApi.md#instagramBlendedTopSearch) | **GET** /v1/instagram/search/top | Blended top search |
| [**instagramGetActiveStories**](InstagramApi.md#instagramGetActiveStories) | **GET** /v1/instagram/users/{username}/stories | Get active stories |
| [**instagramGetAudioTrack**](InstagramApi.md#instagramGetAudioTrack) | **GET** /v1/instagram/audio/{audio_id} | Get audio track |
| [**instagramGetComments**](InstagramApi.md#instagramGetComments) | **GET** /v1/instagram/media/{code}/comments | Get comments |
| [**instagramGetFollowers**](InstagramApi.md#instagramGetFollowers) | **GET** /v1/instagram/users/{username}/followers | Get followers |
| [**instagramGetFollowing**](InstagramApi.md#instagramGetFollowing) | **GET** /v1/instagram/users/{username}/following | Get following |
| [**instagramGetHashtagInfo**](InstagramApi.md#instagramGetHashtagInfo) | **GET** /v1/instagram/hashtags/{tag} | Get hashtag info |
| [**instagramGetHighlights**](InstagramApi.md#instagramGetHighlights) | **GET** /v1/instagram/users/{username}/highlights | Get highlights |
| [**instagramGetLikers**](InstagramApi.md#instagramGetLikers) | **GET** /v1/instagram/media/{code}/likers | Get likers |
| [**instagramGetLocation**](InstagramApi.md#instagramGetLocation) | **GET** /v1/instagram/locations/{location_pk} | Get location |
| [**instagramGetPostReelDetail**](InstagramApi.md#instagramGetPostReelDetail) | **GET** /v1/instagram/media/{code} | Get post/reel detail |
| [**instagramGetProfile**](InstagramApi.md#instagramGetProfile) | **GET** /v1/instagram/users/{username} | Get profile |
| [**instagramGetTaggedPosts**](InstagramApi.md#instagramGetTaggedPosts) | **GET** /v1/instagram/users/{username}/tagged | Get tagged posts |
| [**instagramGetUserPosts**](InstagramApi.md#instagramGetUserPosts) | **GET** /v1/instagram/users/{username}/posts | Get user posts |
| [**instagramGetUserReels**](InstagramApi.md#instagramGetUserReels) | **GET** /v1/instagram/users/{username}/reels | Get user reels |
| [**instagramHealth**](InstagramApi.md#instagramHealth) | **GET** /v1/instagram/health | Health |
| [**instagramHealthHead**](InstagramApi.md#instagramHealthHead) | **HEAD** /v1/instagram/health | Health |
| [**instagramRecentHashtagPosts**](InstagramApi.md#instagramRecentHashtagPosts) | **GET** /v1/instagram/hashtags/{tag}/recent | Recent hashtag posts |
| [**instagramRelatedProfiles**](InstagramApi.md#instagramRelatedProfiles) | **GET** /v1/instagram/users/{username}/related | Related profiles |
| [**instagramSearchHashtags**](InstagramApi.md#instagramSearchHashtags) | **GET** /v1/instagram/search/hashtags | Search hashtags |
| [**instagramSearchUsers**](InstagramApi.md#instagramSearchUsers) | **GET** /v1/instagram/search/users | Search users |
| [**instagramTopHashtagPosts**](InstagramApi.md#instagramTopHashtagPosts) | **GET** /v1/instagram/hashtags/{tag}/top | Top hashtag posts |


<a id="instagramAboutThisAccount"></a>
# **instagramAboutThisAccount**
> Object instagramAboutThisAccount(username)

About this account

**Temporarily unavailable.** The authenticated Instagram tier is offline, so this endpoint currently returns &#x60;503 temporarily_unavailable&#x60; (not billed, &#x60;Retry-After&#x60; set) — see https://docs.scrapebadger.com/instagram/overview. Country, join date and former usernames.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.InstagramApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    InstagramApi apiInstance = new InstagramApi(defaultClient);
    String username = "username_example"; // String | 
    try {
      Object result = apiInstance.instagramAboutThisAccount(username);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InstagramApi#instagramAboutThisAccount");
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

<a id="instagramBlendedTopSearch"></a>
# **instagramBlendedTopSearch**
> Object instagramBlendedTopSearch(query)

Blended top search

**Temporarily unavailable.** The authenticated Instagram tier is offline, so this endpoint currently returns &#x60;503 temporarily_unavailable&#x60; (not billed, &#x60;Retry-After&#x60; set) — see https://docs.scrapebadger.com/instagram/overview.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.InstagramApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    InstagramApi apiInstance = new InstagramApi(defaultClient);
    String query = "query_example"; // String | 
    try {
      Object result = apiInstance.instagramBlendedTopSearch(query);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InstagramApi#instagramBlendedTopSearch");
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
| **query** | **String**|  | |

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

<a id="instagramGetActiveStories"></a>
# **instagramGetActiveStories**
> Object instagramGetActiveStories(username)

Get active stories

**Temporarily unavailable.** The authenticated Instagram tier is offline, so this endpoint currently returns &#x60;503 temporarily_unavailable&#x60; (not billed, &#x60;Retry-After&#x60; set) — see https://docs.scrapebadger.com/instagram/overview. Active stories (account pool only).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.InstagramApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    InstagramApi apiInstance = new InstagramApi(defaultClient);
    String username = "username_example"; // String | 
    try {
      Object result = apiInstance.instagramGetActiveStories(username);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InstagramApi#instagramGetActiveStories");
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

<a id="instagramGetAudioTrack"></a>
# **instagramGetAudioTrack**
> Object instagramGetAudioTrack(audioId)

Get audio track

**Temporarily unavailable.** The authenticated Instagram tier is offline, so this endpoint currently returns &#x60;503 temporarily_unavailable&#x60; (not billed, &#x60;Retry-After&#x60; set) — see https://docs.scrapebadger.com/instagram/overview.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.InstagramApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    InstagramApi apiInstance = new InstagramApi(defaultClient);
    String audioId = "audioId_example"; // String | 
    try {
      Object result = apiInstance.instagramGetAudioTrack(audioId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InstagramApi#instagramGetAudioTrack");
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
| **audioId** | **String**|  | |

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

<a id="instagramGetComments"></a>
# **instagramGetComments**
> Object instagramGetComments(code, amount, cursor)

Get comments

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.InstagramApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    InstagramApi apiInstance = new InstagramApi(defaultClient);
    String code = "code_example"; // String | 
    Integer amount = 20; // Integer | 
    String cursor = "cursor_example"; // String | 
    try {
      Object result = apiInstance.instagramGetComments(code, amount, cursor);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InstagramApi#instagramGetComments");
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
| **code** | **String**|  | |
| **amount** | **Integer**|  | [optional] [default to 20] |
| **cursor** | **String**|  | [optional] |

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

<a id="instagramGetFollowers"></a>
# **instagramGetFollowers**
> Object instagramGetFollowers(username, amount, cursor, order)

Get followers

**Temporarily unavailable.** The authenticated Instagram tier is offline, so this endpoint currently returns &#x60;503 temporarily_unavailable&#x60; (not billed, &#x60;Retry-After&#x60; set) — see https://docs.scrapebadger.com/instagram/overview. Followers list, paginated (account pool).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.InstagramApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    InstagramApi apiInstance = new InstagramApi(defaultClient);
    String username = "username_example"; // String | 
    Integer amount = 50; // Integer | 
    String cursor = "cursor_example"; // String | 
    String order = "order_example"; // String | date_followed_latest | date_followed_earliest
    try {
      Object result = apiInstance.instagramGetFollowers(username, amount, cursor, order);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InstagramApi#instagramGetFollowers");
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
| **amount** | **Integer**|  | [optional] [default to 50] |
| **cursor** | **String**|  | [optional] |
| **order** | **String**| date_followed_latest | date_followed_earliest | [optional] |

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

<a id="instagramGetFollowing"></a>
# **instagramGetFollowing**
> Object instagramGetFollowing(username, amount, cursor)

Get following

**Temporarily unavailable.** The authenticated Instagram tier is offline, so this endpoint currently returns &#x60;503 temporarily_unavailable&#x60; (not billed, &#x60;Retry-After&#x60; set) — see https://docs.scrapebadger.com/instagram/overview.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.InstagramApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    InstagramApi apiInstance = new InstagramApi(defaultClient);
    String username = "username_example"; // String | 
    Integer amount = 50; // Integer | 
    String cursor = "cursor_example"; // String | 
    try {
      Object result = apiInstance.instagramGetFollowing(username, amount, cursor);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InstagramApi#instagramGetFollowing");
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
| **amount** | **Integer**|  | [optional] [default to 50] |
| **cursor** | **String**|  | [optional] |

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

<a id="instagramGetHashtagInfo"></a>
# **instagramGetHashtagInfo**
> Object instagramGetHashtagInfo(tag)

Get hashtag info

**Temporarily unavailable.** The authenticated Instagram tier is offline, so this endpoint currently returns &#x60;503 temporarily_unavailable&#x60; (not billed, &#x60;Retry-After&#x60; set) — see https://docs.scrapebadger.com/instagram/overview.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.InstagramApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    InstagramApi apiInstance = new InstagramApi(defaultClient);
    String tag = "tag_example"; // String | 
    try {
      Object result = apiInstance.instagramGetHashtagInfo(tag);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InstagramApi#instagramGetHashtagInfo");
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
| **tag** | **String**|  | |

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

<a id="instagramGetHighlights"></a>
# **instagramGetHighlights**
> Object instagramGetHighlights(username)

Get highlights

**Temporarily unavailable.** The authenticated Instagram tier is offline, so this endpoint currently returns &#x60;503 temporarily_unavailable&#x60; (not billed, &#x60;Retry-After&#x60; set) — see https://docs.scrapebadger.com/instagram/overview.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.InstagramApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    InstagramApi apiInstance = new InstagramApi(defaultClient);
    String username = "username_example"; // String | 
    try {
      Object result = apiInstance.instagramGetHighlights(username);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InstagramApi#instagramGetHighlights");
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

<a id="instagramGetLikers"></a>
# **instagramGetLikers**
> Object instagramGetLikers(code)

Get likers

**Temporarily unavailable.** The authenticated Instagram tier is offline, so this endpoint currently returns &#x60;503 temporarily_unavailable&#x60; (not billed, &#x60;Retry-After&#x60; set) — see https://docs.scrapebadger.com/instagram/overview.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.InstagramApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    InstagramApi apiInstance = new InstagramApi(defaultClient);
    String code = "code_example"; // String | 
    try {
      Object result = apiInstance.instagramGetLikers(code);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InstagramApi#instagramGetLikers");
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
| **code** | **String**|  | |

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

<a id="instagramGetLocation"></a>
# **instagramGetLocation**
> Object instagramGetLocation(locationPk)

Get location

**Temporarily unavailable.** The authenticated Instagram tier is offline, so this endpoint currently returns &#x60;503 temporarily_unavailable&#x60; (not billed, &#x60;Retry-After&#x60; set) — see https://docs.scrapebadger.com/instagram/overview.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.InstagramApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    InstagramApi apiInstance = new InstagramApi(defaultClient);
    Integer locationPk = 56; // Integer | 
    try {
      Object result = apiInstance.instagramGetLocation(locationPk);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InstagramApi#instagramGetLocation");
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
| **locationPk** | **Integer**|  | |

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

<a id="instagramGetPostReelDetail"></a>
# **instagramGetPostReelDetail**
> Object instagramGetPostReelDetail(code)

Get post/reel detail

Single post or reel: caption, media, counts, tags, location, carousel.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.InstagramApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    InstagramApi apiInstance = new InstagramApi(defaultClient);
    String code = "code_example"; // String | 
    try {
      Object result = apiInstance.instagramGetPostReelDetail(code);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InstagramApi#instagramGetPostReelDetail");
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
| **code** | **String**|  | |

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

<a id="instagramGetProfile"></a>
# **instagramGetProfile**
> Object instagramGetProfile(username)

Get profile

Full public profile: bio, counts, verification, business contact, links.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.InstagramApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    InstagramApi apiInstance = new InstagramApi(defaultClient);
    String username = "username_example"; // String | 
    try {
      Object result = apiInstance.instagramGetProfile(username);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InstagramApi#instagramGetProfile");
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

<a id="instagramGetTaggedPosts"></a>
# **instagramGetTaggedPosts**
> Object instagramGetTaggedPosts(username, amount, cursor)

Get tagged posts

**Temporarily unavailable.** The authenticated Instagram tier is offline, so this endpoint currently returns &#x60;503 temporarily_unavailable&#x60; (not billed, &#x60;Retry-After&#x60; set) — see https://docs.scrapebadger.com/instagram/overview.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.InstagramApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    InstagramApi apiInstance = new InstagramApi(defaultClient);
    String username = "username_example"; // String | 
    Integer amount = 20; // Integer | 
    String cursor = "cursor_example"; // String | 
    try {
      Object result = apiInstance.instagramGetTaggedPosts(username, amount, cursor);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InstagramApi#instagramGetTaggedPosts");
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
| **amount** | **Integer**|  | [optional] [default to 20] |
| **cursor** | **String**|  | [optional] |

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

<a id="instagramGetUserPosts"></a>
# **instagramGetUserPosts**
> Object instagramGetUserPosts(username, amount, cursor)

Get user posts

Timeline posts, paginated.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.InstagramApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    InstagramApi apiInstance = new InstagramApi(defaultClient);
    String username = "username_example"; // String | 
    Integer amount = 20; // Integer | 
    String cursor = "cursor_example"; // String | 
    try {
      Object result = apiInstance.instagramGetUserPosts(username, amount, cursor);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InstagramApi#instagramGetUserPosts");
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
| **amount** | **Integer**|  | [optional] [default to 20] |
| **cursor** | **String**|  | [optional] |

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

<a id="instagramGetUserReels"></a>
# **instagramGetUserReels**
> Object instagramGetUserReels(username, amount, cursor)

Get user reels

**Temporarily unavailable.** The authenticated Instagram tier is offline, so this endpoint currently returns &#x60;503 temporarily_unavailable&#x60; (not billed, &#x60;Retry-After&#x60; set) — see https://docs.scrapebadger.com/instagram/overview.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.InstagramApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    InstagramApi apiInstance = new InstagramApi(defaultClient);
    String username = "username_example"; // String | 
    Integer amount = 20; // Integer | 
    String cursor = "cursor_example"; // String | 
    try {
      Object result = apiInstance.instagramGetUserReels(username, amount, cursor);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InstagramApi#instagramGetUserReels");
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
| **amount** | **Integer**|  | [optional] [default to 20] |
| **cursor** | **String**|  | [optional] |

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

<a id="instagramHealth"></a>
# **instagramHealth**
> Object instagramHealth()

Health

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.InstagramApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    InstagramApi apiInstance = new InstagramApi(defaultClient);
    try {
      Object result = apiInstance.instagramHealth();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InstagramApi#instagramHealth");
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

<a id="instagramHealthHead"></a>
# **instagramHealthHead**
> Object instagramHealthHead()

Health

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.InstagramApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    InstagramApi apiInstance = new InstagramApi(defaultClient);
    try {
      Object result = apiInstance.instagramHealthHead();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InstagramApi#instagramHealthHead");
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

<a id="instagramRecentHashtagPosts"></a>
# **instagramRecentHashtagPosts**
> Object instagramRecentHashtagPosts(tag, amount, cursor)

Recent hashtag posts

**Temporarily unavailable.** The authenticated Instagram tier is offline, so this endpoint currently returns &#x60;503 temporarily_unavailable&#x60; (not billed, &#x60;Retry-After&#x60; set) — see https://docs.scrapebadger.com/instagram/overview.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.InstagramApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    InstagramApi apiInstance = new InstagramApi(defaultClient);
    String tag = "tag_example"; // String | 
    Integer amount = 20; // Integer | 
    String cursor = "cursor_example"; // String | 
    try {
      Object result = apiInstance.instagramRecentHashtagPosts(tag, amount, cursor);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InstagramApi#instagramRecentHashtagPosts");
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
| **tag** | **String**|  | |
| **amount** | **Integer**|  | [optional] [default to 20] |
| **cursor** | **String**|  | [optional] |

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

<a id="instagramRelatedProfiles"></a>
# **instagramRelatedProfiles**
> Object instagramRelatedProfiles(username)

Related profiles

**Temporarily unavailable.** The authenticated Instagram tier is offline, so this endpoint currently returns &#x60;503 temporarily_unavailable&#x60; (not billed, &#x60;Retry-After&#x60; set) — see https://docs.scrapebadger.com/instagram/overview.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.InstagramApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    InstagramApi apiInstance = new InstagramApi(defaultClient);
    String username = "username_example"; // String | 
    try {
      Object result = apiInstance.instagramRelatedProfiles(username);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InstagramApi#instagramRelatedProfiles");
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

<a id="instagramSearchHashtags"></a>
# **instagramSearchHashtags**
> Object instagramSearchHashtags(query)

Search hashtags

**Temporarily unavailable.** The authenticated Instagram tier is offline, so this endpoint currently returns &#x60;503 temporarily_unavailable&#x60; (not billed, &#x60;Retry-After&#x60; set) — see https://docs.scrapebadger.com/instagram/overview.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.InstagramApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    InstagramApi apiInstance = new InstagramApi(defaultClient);
    String query = "query_example"; // String | 
    try {
      Object result = apiInstance.instagramSearchHashtags(query);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InstagramApi#instagramSearchHashtags");
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
| **query** | **String**|  | |

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

<a id="instagramSearchUsers"></a>
# **instagramSearchUsers**
> Object instagramSearchUsers(query)

Search users

**Temporarily unavailable.** The authenticated Instagram tier is offline, so this endpoint currently returns &#x60;503 temporarily_unavailable&#x60; (not billed, &#x60;Retry-After&#x60; set) — see https://docs.scrapebadger.com/instagram/overview.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.InstagramApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    InstagramApi apiInstance = new InstagramApi(defaultClient);
    String query = "query_example"; // String | 
    try {
      Object result = apiInstance.instagramSearchUsers(query);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InstagramApi#instagramSearchUsers");
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
| **query** | **String**|  | |

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

<a id="instagramTopHashtagPosts"></a>
# **instagramTopHashtagPosts**
> Object instagramTopHashtagPosts(tag, amount, cursor)

Top hashtag posts

**Temporarily unavailable.** The authenticated Instagram tier is offline, so this endpoint currently returns &#x60;503 temporarily_unavailable&#x60; (not billed, &#x60;Retry-After&#x60; set) — see https://docs.scrapebadger.com/instagram/overview.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.InstagramApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    InstagramApi apiInstance = new InstagramApi(defaultClient);
    String tag = "tag_example"; // String | 
    Integer amount = 20; // Integer | 
    String cursor = "cursor_example"; // String | 
    try {
      Object result = apiInstance.instagramTopHashtagPosts(tag, amount, cursor);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InstagramApi#instagramTopHashtagPosts");
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
| **tag** | **String**|  | |
| **amount** | **Integer**|  | [optional] [default to 20] |
| **cursor** | **String**|  | [optional] |

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

