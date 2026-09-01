# TikTokApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**tiktokGeneralSearch**](TikTokApi.md#tiktokGeneralSearch) | **GET** /v1/tiktok/search | General search |
| [**tiktokGetCommentReplies**](TikTokApi.md#tiktokGetCommentReplies) | **GET** /v1/tiktok/comments/{comment_id}/replies | Get comment replies |
| [**tiktokGetComments**](TikTokApi.md#tiktokGetComments) | **GET** /v1/tiktok/videos/{video_id}/comments | Get comments |
| [**tiktokGetFollowersDeprecated**](TikTokApi.md#tiktokGetFollowersDeprecated) | **GET** /v1/tiktok/users/{username}/followers | Get followers (deprecated) |
| [**tiktokGetFollowingDeprecated**](TikTokApi.md#tiktokGetFollowingDeprecated) | **GET** /v1/tiktok/users/{username}/following | Get following (deprecated) |
| [**tiktokGetHashtagDetail**](TikTokApi.md#tiktokGetHashtagDetail) | **GET** /v1/tiktok/hashtags/{name} | Get hashtag detail |
| [**tiktokGetHashtagVideos**](TikTokApi.md#tiktokGetHashtagVideos) | **GET** /v1/tiktok/hashtags/{name}/videos | Get hashtag videos |
| [**tiktokGetLikedVideosDeprecated**](TikTokApi.md#tiktokGetLikedVideosDeprecated) | **GET** /v1/tiktok/users/{username}/liked | Get liked videos (deprecated) |
| [**tiktokGetMusicSoundDetail**](TikTokApi.md#tiktokGetMusicSoundDetail) | **GET** /v1/tiktok/music/{music_id} | Get music/sound detail |
| [**tiktokGetMusicVideos**](TikTokApi.md#tiktokGetMusicVideos) | **GET** /v1/tiktok/music/{music_id}/videos | Get music videos |
| [**tiktokGetOembedMetadata**](TikTokApi.md#tiktokGetOembedMetadata) | **GET** /v1/tiktok/oembed | Get oEmbed metadata |
| [**tiktokGetRelatedVideos**](TikTokApi.md#tiktokGetRelatedVideos) | **GET** /v1/tiktok/videos/{video_id}/related | Get related videos |
| [**tiktokGetReposts**](TikTokApi.md#tiktokGetReposts) | **GET** /v1/tiktok/users/{username}/reposts | Get reposts |
| [**tiktokGetTiktokAdDetail**](TikTokApi.md#tiktokGetTiktokAdDetail) | **GET** /v1/tiktok/ads/{ad_id} | Get TikTok ad detail |
| [**tiktokGetTranscript**](TikTokApi.md#tiktokGetTranscript) | **GET** /v1/tiktok/videos/{video_id}/transcript | Get transcript |
| [**tiktokGetUserProfile**](TikTokApi.md#tiktokGetUserProfile) | **GET** /v1/tiktok/users/{username} | Get user profile |
| [**tiktokGetUserVideos**](TikTokApi.md#tiktokGetUserVideos) | **GET** /v1/tiktok/users/{username}/videos | Get user videos |
| [**tiktokGetVideoDetail**](TikTokApi.md#tiktokGetVideoDetail) | **GET** /v1/tiktok/videos/{video_id} | Get video detail |
| [**tiktokHealthCheck**](TikTokApi.md#tiktokHealthCheck) | **GET** /v1/tiktok/health | Health check |
| [**tiktokHealthCheckHead**](TikTokApi.md#tiktokHealthCheckHead) | **HEAD** /v1/tiktok/health | Health check |
| [**tiktokListRegions**](TikTokApi.md#tiktokListRegions) | **GET** /v1/tiktok/regions | List regions |
| [**tiktokSearchHashtags**](TikTokApi.md#tiktokSearchHashtags) | **GET** /v1/tiktok/search/hashtags | Search hashtags |
| [**tiktokSearchTheTiktokAdLibrary**](TikTokApi.md#tiktokSearchTheTiktokAdLibrary) | **GET** /v1/tiktok/ads/search | Search the TikTok Ad Library |
| [**tiktokSearchTiktokAdvertisers**](TikTokApi.md#tiktokSearchTiktokAdvertisers) | **GET** /v1/tiktok/ads/advertisers | Search TikTok advertisers |
| [**tiktokSearchTiktokShopProducts**](TikTokApi.md#tiktokSearchTiktokShopProducts) | **GET** /v1/tiktok/shop/search | Search TikTok Shop products |
| [**tiktokSearchUsers**](TikTokApi.md#tiktokSearchUsers) | **GET** /v1/tiktok/search/users | Search users |
| [**tiktokSearchVideos**](TikTokApi.md#tiktokSearchVideos) | **GET** /v1/tiktok/search/videos | Search videos |
| [**tiktokTiktokShopBestSellers**](TikTokApi.md#tiktokTiktokShopBestSellers) | **GET** /v1/tiktok/shop/ranking | TikTok Shop best sellers |
| [**tiktokTiktokShopCategorySubcategoriesTopProducts**](TikTokApi.md#tiktokTiktokShopCategorySubcategoriesTopProducts) | **GET** /v1/tiktok/shop/categories/{category_id} | TikTok Shop category: subcategories + top products |
| [**tiktokTiktokShopProductDetail**](TikTokApi.md#tiktokTiktokShopProductDetail) | **GET** /v1/tiktok/shop/products/{product_id} | TikTok Shop product detail |
| [**tiktokTiktokShopRootCategories**](TikTokApi.md#tiktokTiktokShopRootCategories) | **GET** /v1/tiktok/shop/categories | TikTok Shop root categories |
| [**tiktokTrendingHashtags**](TikTokApi.md#tiktokTrendingHashtags) | **GET** /v1/tiktok/trending/hashtags | Trending hashtags |
| [**tiktokTrendingSongs**](TikTokApi.md#tiktokTrendingSongs) | **GET** /v1/tiktok/trending/songs | Trending songs |
| [**tiktokTrendingVideos**](TikTokApi.md#tiktokTrendingVideos) | **GET** /v1/tiktok/trending/videos | Trending videos |


<a id="tiktokGeneralSearch"></a>
# **tiktokGeneralSearch**
> Object tiktokGeneralSearch(query, region, count, cursor)

General search

General TikTok search — video results from the Top feed.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TikTokApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TikTokApi apiInstance = new TikTokApi(defaultClient);
    String query = "query_example"; // String | Search keyword
    String region = "US"; // String | 
    Integer count = 20; // Integer | 
    String cursor = "cursor_example"; // String | Composite pagination cursor (offset.search_id) from a prior page's pagination.cursor
    try {
      Object result = apiInstance.tiktokGeneralSearch(query, region, count, cursor);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TikTokApi#tiktokGeneralSearch");
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
| **query** | **String**| Search keyword | |
| **region** | **String**|  | [optional] [default to US] |
| **count** | **Integer**|  | [optional] [default to 20] |
| **cursor** | **String**| Composite pagination cursor (offset.search_id) from a prior page&#39;s pagination.cursor | [optional] |

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

<a id="tiktokGetCommentReplies"></a>
# **tiktokGetCommentReplies**
> Object tiktokGetCommentReplies(commentId, videoId, region, count, cursor)

Get comment replies

Get replies to a TikTok comment (best-effort).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TikTokApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TikTokApi apiInstance = new TikTokApi(defaultClient);
    String commentId = "commentId_example"; // String | 
    String videoId = "videoId_example"; // String | Parent video id
    String region = "US"; // String | 
    Integer count = 20; // Integer | 
    String cursor = "cursor_example"; // String | Pagination cursor from a prior page's pagination.cursor
    try {
      Object result = apiInstance.tiktokGetCommentReplies(commentId, videoId, region, count, cursor);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TikTokApi#tiktokGetCommentReplies");
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
| **commentId** | **String**|  | |
| **videoId** | **String**| Parent video id | |
| **region** | **String**|  | [optional] [default to US] |
| **count** | **Integer**|  | [optional] [default to 20] |
| **cursor** | **String**| Pagination cursor from a prior page&#39;s pagination.cursor | [optional] |

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

<a id="tiktokGetComments"></a>
# **tiktokGetComments**
> Object tiktokGetComments(videoId, region, count, cursor)

Get comments

Get top-level comments on a TikTok video.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TikTokApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TikTokApi apiInstance = new TikTokApi(defaultClient);
    String videoId = "videoId_example"; // String | 
    String region = "US"; // String | 
    Integer count = 20; // Integer | 
    String cursor = "cursor_example"; // String | Pagination cursor from a prior page's pagination.cursor
    try {
      Object result = apiInstance.tiktokGetComments(videoId, region, count, cursor);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TikTokApi#tiktokGetComments");
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
| **videoId** | **String**|  | |
| **region** | **String**|  | [optional] [default to US] |
| **count** | **Integer**|  | [optional] [default to 20] |
| **cursor** | **String**| Pagination cursor from a prior page&#39;s pagination.cursor | [optional] |

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

<a id="tiktokGetFollowersDeprecated"></a>
# **tiktokGetFollowersDeprecated**
> Object tiktokGetFollowersDeprecated(username, region, count)

Get followers (deprecated)

DEPRECATED — TikTok followers require an authenticated account session. Returns HTTP 410.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TikTokApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TikTokApi apiInstance = new TikTokApi(defaultClient);
    String username = "username_example"; // String | 
    String region = "US"; // String | 
    Integer count = 30; // Integer | 
    try {
      Object result = apiInstance.tiktokGetFollowersDeprecated(username, region, count);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TikTokApi#tiktokGetFollowersDeprecated");
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
| **region** | **String**|  | [optional] [default to US] |
| **count** | **Integer**|  | [optional] [default to 30] |

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

<a id="tiktokGetFollowingDeprecated"></a>
# **tiktokGetFollowingDeprecated**
> Object tiktokGetFollowingDeprecated(username, region, count)

Get following (deprecated)

DEPRECATED — TikTok following requires an authenticated account session. Returns HTTP 410.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TikTokApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TikTokApi apiInstance = new TikTokApi(defaultClient);
    String username = "username_example"; // String | 
    String region = "US"; // String | 
    Integer count = 30; // Integer | 
    try {
      Object result = apiInstance.tiktokGetFollowingDeprecated(username, region, count);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TikTokApi#tiktokGetFollowingDeprecated");
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
| **region** | **String**|  | [optional] [default to US] |
| **count** | **Integer**|  | [optional] [default to 30] |

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

<a id="tiktokGetHashtagDetail"></a>
# **tiktokGetHashtagDetail**
> Object tiktokGetHashtagDetail(name, region)

Get hashtag detail

Get TikTok hashtag/challenge detail.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TikTokApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TikTokApi apiInstance = new TikTokApi(defaultClient);
    String name = "name_example"; // String | 
    String region = "US"; // String | 
    try {
      Object result = apiInstance.tiktokGetHashtagDetail(name, region);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TikTokApi#tiktokGetHashtagDetail");
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
| **name** | **String**|  | |
| **region** | **String**|  | [optional] [default to US] |

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

<a id="tiktokGetHashtagVideos"></a>
# **tiktokGetHashtagVideos**
> Object tiktokGetHashtagVideos(name, region, count, cursor)

Get hashtag videos

Get videos tagged with a TikTok hashtag.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TikTokApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TikTokApi apiInstance = new TikTokApi(defaultClient);
    String name = "name_example"; // String | 
    String region = "US"; // String | 
    Integer count = 30; // Integer | 
    String cursor = "cursor_example"; // String | Pagination cursor from a prior page's pagination.cursor
    try {
      Object result = apiInstance.tiktokGetHashtagVideos(name, region, count, cursor);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TikTokApi#tiktokGetHashtagVideos");
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
| **name** | **String**|  | |
| **region** | **String**|  | [optional] [default to US] |
| **count** | **Integer**|  | [optional] [default to 30] |
| **cursor** | **String**| Pagination cursor from a prior page&#39;s pagination.cursor | [optional] |

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

<a id="tiktokGetLikedVideosDeprecated"></a>
# **tiktokGetLikedVideosDeprecated**
> Object tiktokGetLikedVideosDeprecated(username, region, count)

Get liked videos (deprecated)

DEPRECATED — TikTok liked videos require an authenticated account session. Returns HTTP 410.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TikTokApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TikTokApi apiInstance = new TikTokApi(defaultClient);
    String username = "username_example"; // String | 
    String region = "US"; // String | 
    Integer count = 30; // Integer | 
    try {
      Object result = apiInstance.tiktokGetLikedVideosDeprecated(username, region, count);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TikTokApi#tiktokGetLikedVideosDeprecated");
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
| **region** | **String**|  | [optional] [default to US] |
| **count** | **Integer**|  | [optional] [default to 30] |

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

<a id="tiktokGetMusicSoundDetail"></a>
# **tiktokGetMusicSoundDetail**
> Object tiktokGetMusicSoundDetail(musicId, region)

Get music/sound detail

Get TikTok sound/music detail.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TikTokApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TikTokApi apiInstance = new TikTokApi(defaultClient);
    String musicId = "musicId_example"; // String | 
    String region = "US"; // String | 
    try {
      Object result = apiInstance.tiktokGetMusicSoundDetail(musicId, region);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TikTokApi#tiktokGetMusicSoundDetail");
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
| **musicId** | **String**|  | |
| **region** | **String**|  | [optional] [default to US] |

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

<a id="tiktokGetMusicVideos"></a>
# **tiktokGetMusicVideos**
> Object tiktokGetMusicVideos(musicId, region, count, cursor)

Get music videos

Get videos using a given TikTok sound.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TikTokApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TikTokApi apiInstance = new TikTokApi(defaultClient);
    String musicId = "musicId_example"; // String | 
    String region = "US"; // String | 
    Integer count = 30; // Integer | 
    String cursor = "cursor_example"; // String | Pagination cursor from a prior page's pagination.cursor
    try {
      Object result = apiInstance.tiktokGetMusicVideos(musicId, region, count, cursor);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TikTokApi#tiktokGetMusicVideos");
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
| **musicId** | **String**|  | |
| **region** | **String**|  | [optional] [default to US] |
| **count** | **Integer**|  | [optional] [default to 30] |
| **cursor** | **String**| Pagination cursor from a prior page&#39;s pagination.cursor | [optional] |

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

<a id="tiktokGetOembedMetadata"></a>
# **tiktokGetOembedMetadata**
> Object tiktokGetOembedMetadata(url, region)

Get oEmbed metadata

Get cheap unauthenticated oEmbed metadata for a TikTok URL.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TikTokApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TikTokApi apiInstance = new TikTokApi(defaultClient);
    String url = "url_example"; // String | Full TikTok video or profile URL
    String region = "US"; // String | 
    try {
      Object result = apiInstance.tiktokGetOembedMetadata(url, region);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TikTokApi#tiktokGetOembedMetadata");
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
| **url** | **String**| Full TikTok video or profile URL | |
| **region** | **String**|  | [optional] [default to US] |

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

<a id="tiktokGetRelatedVideos"></a>
# **tiktokGetRelatedVideos**
> Object tiktokGetRelatedVideos(videoId, region, count)

Get related videos

Get TikTok&#39;s related videos for a given video.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TikTokApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TikTokApi apiInstance = new TikTokApi(defaultClient);
    String videoId = "videoId_example"; // String | 
    String region = "US"; // String | 
    Integer count = 16; // Integer | 
    try {
      Object result = apiInstance.tiktokGetRelatedVideos(videoId, region, count);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TikTokApi#tiktokGetRelatedVideos");
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
| **videoId** | **String**|  | |
| **region** | **String**|  | [optional] [default to US] |
| **count** | **Integer**|  | [optional] [default to 16] |

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

<a id="tiktokGetReposts"></a>
# **tiktokGetReposts**
> Object tiktokGetReposts(username, region, count)

Get reposts

Get videos a TikTok user has reposted.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TikTokApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TikTokApi apiInstance = new TikTokApi(defaultClient);
    String username = "username_example"; // String | 
    String region = "US"; // String | 
    Integer count = 30; // Integer | 
    try {
      Object result = apiInstance.tiktokGetReposts(username, region, count);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TikTokApi#tiktokGetReposts");
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
| **region** | **String**|  | [optional] [default to US] |
| **count** | **Integer**|  | [optional] [default to 30] |

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

<a id="tiktokGetTiktokAdDetail"></a>
# **tiktokGetTiktokAdDetail**
> Object tiktokGetTiktokAdDetail(adId, region)

Get TikTok ad detail

Get a single ad&#39;s advertiser, creatives, and targeting/impression breakdown.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TikTokApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TikTokApi apiInstance = new TikTokApi(defaultClient);
    String adId = "adId_example"; // String | 
    String region = "DE"; // String | EU region code (the Ad Library is EU-only)
    try {
      Object result = apiInstance.tiktokGetTiktokAdDetail(adId, region);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TikTokApi#tiktokGetTiktokAdDetail");
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
| **adId** | **String**|  | |
| **region** | **String**| EU region code (the Ad Library is EU-only) | [optional] [default to DE] |

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

<a id="tiktokGetTranscript"></a>
# **tiktokGetTranscript**
> Object tiktokGetTranscript(videoId, region)

Get transcript

Get subtitle/caption tracks for a TikTok video.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TikTokApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TikTokApi apiInstance = new TikTokApi(defaultClient);
    String videoId = "videoId_example"; // String | 
    String region = "US"; // String | 
    try {
      Object result = apiInstance.tiktokGetTranscript(videoId, region);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TikTokApi#tiktokGetTranscript");
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
| **videoId** | **String**|  | |
| **region** | **String**|  | [optional] [default to US] |

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

<a id="tiktokGetUserProfile"></a>
# **tiktokGetUserProfile**
> Object tiktokGetUserProfile(username, region)

Get user profile

Get a TikTok user&#39;s full profile.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TikTokApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TikTokApi apiInstance = new TikTokApi(defaultClient);
    String username = "username_example"; // String | 
    String region = "US"; // String | Content region (ISO 3166-1 alpha-2)
    try {
      Object result = apiInstance.tiktokGetUserProfile(username, region);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TikTokApi#tiktokGetUserProfile");
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
| **region** | **String**| Content region (ISO 3166-1 alpha-2) | [optional] [default to US] |

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

<a id="tiktokGetUserVideos"></a>
# **tiktokGetUserVideos**
> Object tiktokGetUserVideos(username, region, count, cursor)

Get user videos

Get a TikTok user&#39;s posted videos.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TikTokApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TikTokApi apiInstance = new TikTokApi(defaultClient);
    String username = "username_example"; // String | 
    String region = "US"; // String | 
    Integer count = 30; // Integer | 
    String cursor = "cursor_example"; // String | Pagination cursor from a prior page's `pagination.cursor` (signer path only).
    try {
      Object result = apiInstance.tiktokGetUserVideos(username, region, count, cursor);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TikTokApi#tiktokGetUserVideos");
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
| **region** | **String**|  | [optional] [default to US] |
| **count** | **Integer**|  | [optional] [default to 30] |
| **cursor** | **String**| Pagination cursor from a prior page&#39;s &#x60;pagination.cursor&#x60; (signer path only). | [optional] |

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

<a id="tiktokGetVideoDetail"></a>
# **tiktokGetVideoDetail**
> Object tiktokGetVideoDetail(videoId, region, username)

Get video detail

Get full metadata for a single TikTok video/post.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TikTokApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TikTokApi apiInstance = new TikTokApi(defaultClient);
    String videoId = "videoId_example"; // String | 
    String region = "US"; // String | 
    String username = "username_example"; // String | Author handle (skips oEmbed lookup)
    try {
      Object result = apiInstance.tiktokGetVideoDetail(videoId, region, username);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TikTokApi#tiktokGetVideoDetail");
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
| **videoId** | **String**|  | |
| **region** | **String**|  | [optional] [default to US] |
| **username** | **String**| Author handle (skips oEmbed lookup) | [optional] |

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

<a id="tiktokHealthCheck"></a>
# **tiktokHealthCheck**
> Object tiktokHealthCheck()

Health check

Check health of the TikTok scraper service.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TikTokApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TikTokApi apiInstance = new TikTokApi(defaultClient);
    try {
      Object result = apiInstance.tiktokHealthCheck();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TikTokApi#tiktokHealthCheck");
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

<a id="tiktokHealthCheckHead"></a>
# **tiktokHealthCheckHead**
> Object tiktokHealthCheckHead()

Health check

Check health of the TikTok scraper service.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TikTokApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TikTokApi apiInstance = new TikTokApi(defaultClient);
    try {
      Object result = apiInstance.tiktokHealthCheckHead();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TikTokApi#tiktokHealthCheckHead");
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

<a id="tiktokListRegions"></a>
# **tiktokListRegions**
> Object tiktokListRegions()

List regions

List supported TikTok content regions.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TikTokApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TikTokApi apiInstance = new TikTokApi(defaultClient);
    try {
      Object result = apiInstance.tiktokListRegions();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TikTokApi#tiktokListRegions");
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

<a id="tiktokSearchHashtags"></a>
# **tiktokSearchHashtags**
> Object tiktokSearchHashtags(query, region, count, cursor)

Search hashtags

Search TikTok hashtags by keyword.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TikTokApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TikTokApi apiInstance = new TikTokApi(defaultClient);
    String query = "query_example"; // String | Search keyword
    String region = "US"; // String | 
    Integer count = 20; // Integer | 
    String cursor = "cursor_example"; // String | Composite pagination cursor (offset.search_id) from a prior page's pagination.cursor
    try {
      Object result = apiInstance.tiktokSearchHashtags(query, region, count, cursor);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TikTokApi#tiktokSearchHashtags");
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
| **query** | **String**| Search keyword | |
| **region** | **String**|  | [optional] [default to US] |
| **count** | **Integer**|  | [optional] [default to 20] |
| **cursor** | **String**| Composite pagination cursor (offset.search_id) from a prior page&#39;s pagination.cursor | [optional] |

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

<a id="tiktokSearchTheTiktokAdLibrary"></a>
# **tiktokSearchTheTiktokAdLibrary**
> Object tiktokSearchTheTiktokAdLibrary(query, advertiserId, region, days, sort, offset, searchId, count)

Search the TikTok Ad Library

Search TikTok&#39;s Commercial Content Library (ad transparency) by keyword or advertiser.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TikTokApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TikTokApi apiInstance = new TikTokApi(defaultClient);
    String query = ""; // String | Keyword (ignored when advertiser_id is set)
    String advertiserId = ""; // String | Advertiser business id(s) for advertiser search
    String region = "DE"; // String | EU region code (the Ad Library is EU-only)
    Integer days = 30; // Integer | 
    String sort = "last_shown_date,desc"; // String | 
    Integer offset = 0; // Integer | 
    String searchId = ""; // String | 
    Integer count = 20; // Integer | 
    try {
      Object result = apiInstance.tiktokSearchTheTiktokAdLibrary(query, advertiserId, region, days, sort, offset, searchId, count);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TikTokApi#tiktokSearchTheTiktokAdLibrary");
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
| **query** | **String**| Keyword (ignored when advertiser_id is set) | [optional] [default to ] |
| **advertiserId** | **String**| Advertiser business id(s) for advertiser search | [optional] [default to ] |
| **region** | **String**| EU region code (the Ad Library is EU-only) | [optional] [default to DE] |
| **days** | **Integer**|  | [optional] [default to 30] |
| **sort** | **String**|  | [optional] [default to last_shown_date,desc] |
| **offset** | **Integer**|  | [optional] [default to 0] |
| **searchId** | **String**|  | [optional] [default to ] |
| **count** | **Integer**|  | [optional] [default to 20] |

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

<a id="tiktokSearchTiktokAdvertisers"></a>
# **tiktokSearchTiktokAdvertisers**
> Object tiktokSearchTiktokAdvertisers(query, region, count)

Search TikTok advertisers

Look up TikTok advertiser business ids by name (feeds ads/search?advertiser_id&#x3D;).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TikTokApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TikTokApi apiInstance = new TikTokApi(defaultClient);
    String query = "query_example"; // String | Advertiser name (or partial) to look up
    String region = "DE"; // String | EU region code (the Ad Library is EU-only)
    Integer count = 10; // Integer | 
    try {
      Object result = apiInstance.tiktokSearchTiktokAdvertisers(query, region, count);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TikTokApi#tiktokSearchTiktokAdvertisers");
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
| **query** | **String**| Advertiser name (or partial) to look up | |
| **region** | **String**| EU region code (the Ad Library is EU-only) | [optional] [default to DE] |
| **count** | **Integer**|  | [optional] [default to 10] |

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

<a id="tiktokSearchTiktokShopProducts"></a>
# **tiktokSearchTiktokShopProducts**
> Object tiktokSearchTiktokShopProducts(q)

Search TikTok Shop products

Keyword search over TikTok Shop products (US): products with their bound video, matching shops, related searches and categories.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TikTokApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TikTokApi apiInstance = new TikTokApi(defaultClient);
    String q = "q_example"; // String | Keyword, e.g. 'wireless earbuds'
    try {
      Object result = apiInstance.tiktokSearchTiktokShopProducts(q);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TikTokApi#tiktokSearchTiktokShopProducts");
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
| **q** | **String**| Keyword, e.g. &#39;wireless earbuds&#39; | |

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

<a id="tiktokSearchUsers"></a>
# **tiktokSearchUsers**
> Object tiktokSearchUsers(query, region, count, cursor)

Search users

Search TikTok users by keyword.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TikTokApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TikTokApi apiInstance = new TikTokApi(defaultClient);
    String query = "query_example"; // String | Search keyword
    String region = "US"; // String | 
    Integer count = 20; // Integer | 
    String cursor = "cursor_example"; // String | Composite pagination cursor (offset.search_id) from a prior page's pagination.cursor
    try {
      Object result = apiInstance.tiktokSearchUsers(query, region, count, cursor);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TikTokApi#tiktokSearchUsers");
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
| **query** | **String**| Search keyword | |
| **region** | **String**|  | [optional] [default to US] |
| **count** | **Integer**|  | [optional] [default to 20] |
| **cursor** | **String**| Composite pagination cursor (offset.search_id) from a prior page&#39;s pagination.cursor | [optional] |

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

<a id="tiktokSearchVideos"></a>
# **tiktokSearchVideos**
> Object tiktokSearchVideos(query, region, count, cursor)

Search videos

Search TikTok videos by keyword.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TikTokApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TikTokApi apiInstance = new TikTokApi(defaultClient);
    String query = "query_example"; // String | Search keyword
    String region = "US"; // String | 
    Integer count = 20; // Integer | 
    String cursor = "cursor_example"; // String | Composite pagination cursor (offset.search_id) from a prior page's pagination.cursor
    try {
      Object result = apiInstance.tiktokSearchVideos(query, region, count, cursor);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TikTokApi#tiktokSearchVideos");
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
| **query** | **String**| Search keyword | |
| **region** | **String**|  | [optional] [default to US] |
| **count** | **Integer**|  | [optional] [default to 20] |
| **cursor** | **String**| Composite pagination cursor (offset.search_id) from a prior page&#39;s pagination.cursor | [optional] |

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

<a id="tiktokTiktokShopBestSellers"></a>
# **tiktokTiktokShopBestSellers**
> Object tiktokTiktokShopBestSellers(count)

TikTok Shop best sellers

TikTok Shop&#39;s own ranking of the best-selling products of the past 30 days (US).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TikTokApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TikTokApi apiInstance = new TikTokApi(defaultClient);
    Integer count = 20; // Integer | Max products to return
    try {
      Object result = apiInstance.tiktokTiktokShopBestSellers(count);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TikTokApi#tiktokTiktokShopBestSellers");
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
| **count** | **Integer**| Max products to return | [optional] [default to 20] |

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

<a id="tiktokTiktokShopCategorySubcategoriesTopProducts"></a>
# **tiktokTiktokShopCategorySubcategoriesTopProducts**
> Object tiktokTiktokShopCategorySubcategoriesTopProducts(categoryId)

TikTok Shop category: subcategories + top products

A category&#39;s subcategories and its top products as TikTok Shop ranks them (US).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TikTokApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TikTokApi apiInstance = new TikTokApi(defaultClient);
    String categoryId = "categoryId_example"; // String | 
    try {
      Object result = apiInstance.tiktokTiktokShopCategorySubcategoriesTopProducts(categoryId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TikTokApi#tiktokTiktokShopCategorySubcategoriesTopProducts");
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
| **categoryId** | **String**|  | |

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

<a id="tiktokTiktokShopProductDetail"></a>
# **tiktokTiktokShopProductDetail**
> Object tiktokTiktokShopProductDetail(productId)

TikTok Shop product detail

Full TikTok Shop product page (US): description, images, price, SKUs with stock, reviews, shop and TikTok&#39;s AI summary.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TikTokApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TikTokApi apiInstance = new TikTokApi(defaultClient);
    String productId = "productId_example"; // String | 
    try {
      Object result = apiInstance.tiktokTiktokShopProductDetail(productId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TikTokApi#tiktokTiktokShopProductDetail");
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
| **productId** | **String**|  | |

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

<a id="tiktokTiktokShopRootCategories"></a>
# **tiktokTiktokShopRootCategories**
> Object tiktokTiktokShopRootCategories()

TikTok Shop root categories

Top-level TikTok Shop categories (US). Drill down with /shop/categories/{category_id}.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TikTokApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TikTokApi apiInstance = new TikTokApi(defaultClient);
    try {
      Object result = apiInstance.tiktokTiktokShopRootCategories();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TikTokApi#tiktokTiktokShopRootCategories");
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

<a id="tiktokTrendingHashtags"></a>
# **tiktokTrendingHashtags**
> Object tiktokTrendingHashtags(region, period, count)

Trending hashtags

Get trending hashtags (mobile Discover surface — view_count + creators).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TikTokApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TikTokApi apiInstance = new TikTokApi(defaultClient);
    String region = "US"; // String | 
    Integer period = 7; // Integer | 
    Integer count = 20; // Integer | 
    try {
      Object result = apiInstance.tiktokTrendingHashtags(region, period, count);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TikTokApi#tiktokTrendingHashtags");
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
| **region** | **String**|  | [optional] [default to US] |
| **period** | **Integer**|  | [optional] [default to 7] |
| **count** | **Integer**|  | [optional] [default to 20] |

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

<a id="tiktokTrendingSongs"></a>
# **tiktokTrendingSongs**
> Object tiktokTrendingSongs(region, period, count)

Trending songs

Get trending songs/sounds (mobile hot-music feed — ranked by usage).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TikTokApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TikTokApi apiInstance = new TikTokApi(defaultClient);
    String region = "US"; // String | 
    Integer period = 7; // Integer | 
    Integer count = 20; // Integer | 
    try {
      Object result = apiInstance.tiktokTrendingSongs(region, period, count);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TikTokApi#tiktokTrendingSongs");
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
| **region** | **String**|  | [optional] [default to US] |
| **period** | **Integer**|  | [optional] [default to 7] |
| **count** | **Integer**|  | [optional] [default to 20] |

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

<a id="tiktokTrendingVideos"></a>
# **tiktokTrendingVideos**
> Object tiktokTrendingVideos(region, count)

Trending videos

Get trending videos from the TikTok Explore feed.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TikTokApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TikTokApi apiInstance = new TikTokApi(defaultClient);
    String region = "US"; // String | 
    Integer count = 20; // Integer | 
    try {
      Object result = apiInstance.tiktokTrendingVideos(region, count);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TikTokApi#tiktokTrendingVideos");
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
| **region** | **String**|  | [optional] [default to US] |
| **count** | **Integer**|  | [optional] [default to 20] |

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

