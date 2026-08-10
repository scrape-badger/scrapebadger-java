# YouTubeApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**youtubeBatchVideoDetail**](YouTubeApi.md#youtubeBatchVideoDetail) | **POST** /v1/youtube/videos/batch | Batch video detail |
| [**youtubeChannelAbout**](YouTubeApi.md#youtubeChannelAbout) | **GET** /v1/youtube/channels/{channel_id}/about | Channel about |
| [**youtubeChannelPlaylists**](YouTubeApi.md#youtubeChannelPlaylists) | **GET** /v1/youtube/channels/{channel_id}/playlists | Channel playlists |
| [**youtubeChannelShorts**](YouTubeApi.md#youtubeChannelShorts) | **GET** /v1/youtube/channels/{channel_id}/shorts | Channel shorts |
| [**youtubeChannelStreams**](YouTubeApi.md#youtubeChannelStreams) | **GET** /v1/youtube/channels/{channel_id}/streams | Channel streams |
| [**youtubeChannelVideos**](YouTubeApi.md#youtubeChannelVideos) | **GET** /v1/youtube/channels/{channel_id}/videos | Channel videos |
| [**youtubeCommentReplies**](YouTubeApi.md#youtubeCommentReplies) | **GET** /v1/youtube/videos/{video_id}/comments/{comment_id}/replies | Comment replies |
| [**youtubeCommunityPostComments**](YouTubeApi.md#youtubeCommunityPostComments) | **GET** /v1/youtube/posts/{post_id}/comments | Community post comments |
| [**youtubeCommunityPosts**](YouTubeApi.md#youtubeCommunityPosts) | **GET** /v1/youtube/channels/{channel_id}/community | Community posts |
| [**youtubeContentRegions**](YouTubeApi.md#youtubeContentRegions) | **GET** /v1/youtube/regions | Content regions |
| [**youtubeGetACommunityPost**](YouTubeApi.md#youtubeGetACommunityPost) | **GET** /v1/youtube/posts/{post_id} | Get a community post |
| [**youtubeGetAMixRadioQueue**](YouTubeApi.md#youtubeGetAMixRadioQueue) | **GET** /v1/youtube/mixes/{playlist_id} | Get a mix / radio queue |
| [**youtubeGetAShort**](YouTubeApi.md#youtubeGetAShort) | **GET** /v1/youtube/shorts/{video_id} | Get a Short |
| [**youtubeGetChannelDetail**](YouTubeApi.md#youtubeGetChannelDetail) | **GET** /v1/youtube/channels/{channel_id} | Get channel detail |
| [**youtubeGetPlaylistDetail**](YouTubeApi.md#youtubeGetPlaylistDetail) | **GET** /v1/youtube/playlists/{playlist_id} | Get playlist detail |
| [**youtubeGetVideoDetail**](YouTubeApi.md#youtubeGetVideoDetail) | **GET** /v1/youtube/videos/{video_id} | Get video detail |
| [**youtubeGuestHomeFeed**](YouTubeApi.md#youtubeGuestHomeFeed) | **GET** /v1/youtube/home | Guest home feed |
| [**youtubeKeywordSuggestions**](YouTubeApi.md#youtubeKeywordSuggestions) | **GET** /v1/youtube/autocomplete | Keyword suggestions |
| [**youtubeListCaptionTracks**](YouTubeApi.md#youtubeListCaptionTracks) | **GET** /v1/youtube/videos/{video_id}/captions | List caption tracks |
| [**youtubeLiveChatMessages**](YouTubeApi.md#youtubeLiveChatMessages) | **GET** /v1/youtube/videos/{video_id}/live_chat | Live chat messages |
| [**youtubeOembedMetadata**](YouTubeApi.md#youtubeOembedMetadata) | **GET** /v1/youtube/oembed | oEmbed metadata |
| [**youtubePlaylistItemsPage**](YouTubeApi.md#youtubePlaylistItemsPage) | **GET** /v1/youtube/playlists/{playlist_id}/items | Playlist items page |
| [**youtubeRelatedVideos**](YouTubeApi.md#youtubeRelatedVideos) | **GET** /v1/youtube/videos/{video_id}/related | Related videos |
| [**youtubeResolveHandleUrlToId**](YouTubeApi.md#youtubeResolveHandleUrlToId) | **GET** /v1/youtube/channels/resolve | Resolve handle/URL to id |
| [**youtubeSearchWithinAChannel**](YouTubeApi.md#youtubeSearchWithinAChannel) | **GET** /v1/youtube/channels/{channel_id}/search | Search within a channel |
| [**youtubeSearchYoutube**](YouTubeApi.md#youtubeSearchYoutube) | **GET** /v1/youtube/search | Search YouTube |
| [**youtubeSearchYoutubeMusic**](YouTubeApi.md#youtubeSearchYoutubeMusic) | **GET** /v1/youtube/music/search | Search YouTube Music |
| [**youtubeShortsBySound**](YouTubeApi.md#youtubeShortsBySound) | **GET** /v1/youtube/shorts/by_sound/{sound_id} | Shorts by sound |
| [**youtubeStreamFormats**](YouTubeApi.md#youtubeStreamFormats) | **GET** /v1/youtube/videos/{video_id}/streams | Stream formats |
| [**youtubeSubscriberCountFast**](YouTubeApi.md#youtubeSubscriberCountFast) | **GET** /v1/youtube/channels/{channel_id}/subscriber_count | Subscriber count (fast) |
| [**youtubeSupportedMarkets**](YouTubeApi.md#youtubeSupportedMarkets) | **GET** /v1/youtube/markets | Supported markets |
| [**youtubeTrendingShorts**](YouTubeApi.md#youtubeTrendingShorts) | **GET** /v1/youtube/trending/shorts | Trending shorts |
| [**youtubeTrendingVideos**](YouTubeApi.md#youtubeTrendingVideos) | **GET** /v1/youtube/trending | Trending videos |
| [**youtubeUiLanguages**](YouTubeApi.md#youtubeUiLanguages) | **GET** /v1/youtube/languages | UI languages |
| [**youtubeVideoCategories**](YouTubeApi.md#youtubeVideoCategories) | **GET** /v1/youtube/categories | Video categories |
| [**youtubeVideoComments**](YouTubeApi.md#youtubeVideoComments) | **GET** /v1/youtube/videos/{video_id}/comments | Video comments |
| [**youtubeVideoTranscript**](YouTubeApi.md#youtubeVideoTranscript) | **GET** /v1/youtube/videos/{video_id}/transcript | Video transcript |
| [**youtubeVideosUnderAHashtag**](YouTubeApi.md#youtubeVideosUnderAHashtag) | **GET** /v1/youtube/hashtags/{tag} | Videos under a hashtag |
| [**youtubeYoutubeScraperHealthCheck**](YouTubeApi.md#youtubeYoutubeScraperHealthCheck) | **GET** /v1/youtube/health | YouTube scraper health check |
| [**youtubeYoutubeScraperHealthCheckHead**](YouTubeApi.md#youtubeYoutubeScraperHealthCheckHead) | **HEAD** /v1/youtube/health | YouTube scraper health check |


<a id="youtubeBatchVideoDetail"></a>
# **youtubeBatchVideoDetail**
> Object youtubeBatchVideoDetail(requestBody)

Batch video detail

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.YouTubeApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    YouTubeApi apiInstance = new YouTubeApi(defaultClient);
    Map<String, Object> requestBody = null; // Map<String, Object> | 
    try {
      Object result = apiInstance.youtubeBatchVideoDetail(requestBody);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling YouTubeApi#youtubeBatchVideoDetail");
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
| **requestBody** | [**Map&lt;String, Object&gt;**](Object.md)|  | |

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

<a id="youtubeChannelAbout"></a>
# **youtubeChannelAbout**
> Object youtubeChannelAbout(channelId)

Channel about

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.YouTubeApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    YouTubeApi apiInstance = new YouTubeApi(defaultClient);
    String channelId = "channelId_example"; // String | 
    try {
      Object result = apiInstance.youtubeChannelAbout(channelId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling YouTubeApi#youtubeChannelAbout");
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
| **channelId** | **String**|  | |

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

<a id="youtubeChannelPlaylists"></a>
# **youtubeChannelPlaylists**
> Object youtubeChannelPlaylists(channelId)

Channel playlists

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.YouTubeApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    YouTubeApi apiInstance = new YouTubeApi(defaultClient);
    String channelId = "channelId_example"; // String | 
    try {
      Object result = apiInstance.youtubeChannelPlaylists(channelId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling YouTubeApi#youtubeChannelPlaylists");
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
| **channelId** | **String**|  | |

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

<a id="youtubeChannelShorts"></a>
# **youtubeChannelShorts**
> Object youtubeChannelShorts(channelId)

Channel shorts

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.YouTubeApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    YouTubeApi apiInstance = new YouTubeApi(defaultClient);
    String channelId = "channelId_example"; // String | 
    try {
      Object result = apiInstance.youtubeChannelShorts(channelId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling YouTubeApi#youtubeChannelShorts");
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
| **channelId** | **String**|  | |

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

<a id="youtubeChannelStreams"></a>
# **youtubeChannelStreams**
> Object youtubeChannelStreams(channelId)

Channel streams

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.YouTubeApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    YouTubeApi apiInstance = new YouTubeApi(defaultClient);
    String channelId = "channelId_example"; // String | 
    try {
      Object result = apiInstance.youtubeChannelStreams(channelId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling YouTubeApi#youtubeChannelStreams");
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
| **channelId** | **String**|  | |

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

<a id="youtubeChannelVideos"></a>
# **youtubeChannelVideos**
> Object youtubeChannelVideos(channelId)

Channel videos

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.YouTubeApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    YouTubeApi apiInstance = new YouTubeApi(defaultClient);
    String channelId = "channelId_example"; // String | 
    try {
      Object result = apiInstance.youtubeChannelVideos(channelId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling YouTubeApi#youtubeChannelVideos");
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
| **channelId** | **String**|  | |

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

<a id="youtubeCommentReplies"></a>
# **youtubeCommentReplies**
> Object youtubeCommentReplies(videoId, commentId, continuation)

Comment replies

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.YouTubeApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    YouTubeApi apiInstance = new YouTubeApi(defaultClient);
    String videoId = "videoId_example"; // String | 
    String commentId = "commentId_example"; // String | 
    String continuation = "continuation_example"; // String | Replies continuation token
    try {
      Object result = apiInstance.youtubeCommentReplies(videoId, commentId, continuation);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling YouTubeApi#youtubeCommentReplies");
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
| **commentId** | **String**|  | |
| **continuation** | **String**| Replies continuation token | |

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

<a id="youtubeCommunityPostComments"></a>
# **youtubeCommunityPostComments**
> Object youtubeCommunityPostComments(postId)

Community post comments

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.YouTubeApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    YouTubeApi apiInstance = new YouTubeApi(defaultClient);
    String postId = "postId_example"; // String | 
    try {
      Object result = apiInstance.youtubeCommunityPostComments(postId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling YouTubeApi#youtubeCommunityPostComments");
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

<a id="youtubeCommunityPosts"></a>
# **youtubeCommunityPosts**
> Object youtubeCommunityPosts(channelId)

Community posts

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.YouTubeApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    YouTubeApi apiInstance = new YouTubeApi(defaultClient);
    String channelId = "channelId_example"; // String | 
    try {
      Object result = apiInstance.youtubeCommunityPosts(channelId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling YouTubeApi#youtubeCommunityPosts");
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
| **channelId** | **String**|  | |

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

<a id="youtubeContentRegions"></a>
# **youtubeContentRegions**
> Object youtubeContentRegions()

Content regions

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.YouTubeApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    YouTubeApi apiInstance = new YouTubeApi(defaultClient);
    try {
      Object result = apiInstance.youtubeContentRegions();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling YouTubeApi#youtubeContentRegions");
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

<a id="youtubeGetACommunityPost"></a>
# **youtubeGetACommunityPost**
> Object youtubeGetACommunityPost(postId)

Get a community post

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.YouTubeApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    YouTubeApi apiInstance = new YouTubeApi(defaultClient);
    String postId = "postId_example"; // String | 
    try {
      Object result = apiInstance.youtubeGetACommunityPost(postId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling YouTubeApi#youtubeGetACommunityPost");
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

<a id="youtubeGetAMixRadioQueue"></a>
# **youtubeGetAMixRadioQueue**
> Object youtubeGetAMixRadioQueue(playlistId)

Get a mix / radio queue

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.YouTubeApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    YouTubeApi apiInstance = new YouTubeApi(defaultClient);
    String playlistId = "playlistId_example"; // String | 
    try {
      Object result = apiInstance.youtubeGetAMixRadioQueue(playlistId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling YouTubeApi#youtubeGetAMixRadioQueue");
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
| **playlistId** | **String**|  | |

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

<a id="youtubeGetAShort"></a>
# **youtubeGetAShort**
> Object youtubeGetAShort(videoId)

Get a Short

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.YouTubeApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    YouTubeApi apiInstance = new YouTubeApi(defaultClient);
    String videoId = "videoId_example"; // String | 
    try {
      Object result = apiInstance.youtubeGetAShort(videoId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling YouTubeApi#youtubeGetAShort");
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

<a id="youtubeGetChannelDetail"></a>
# **youtubeGetChannelDetail**
> Object youtubeGetChannelDetail(channelId, gl, hl)

Get channel detail

Channel detail (accepts a UC id, @handle, or custom URL).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.YouTubeApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    YouTubeApi apiInstance = new YouTubeApi(defaultClient);
    String channelId = "channelId_example"; // String | 
    String gl = "gl_example"; // String | 
    String hl = "hl_example"; // String | 
    try {
      Object result = apiInstance.youtubeGetChannelDetail(channelId, gl, hl);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling YouTubeApi#youtubeGetChannelDetail");
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
| **channelId** | **String**|  | |
| **gl** | **String**|  | [optional] |
| **hl** | **String**|  | [optional] |

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

<a id="youtubeGetPlaylistDetail"></a>
# **youtubeGetPlaylistDetail**
> Object youtubeGetPlaylistDetail(playlistId)

Get playlist detail

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.YouTubeApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    YouTubeApi apiInstance = new YouTubeApi(defaultClient);
    String playlistId = "playlistId_example"; // String | 
    try {
      Object result = apiInstance.youtubeGetPlaylistDetail(playlistId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling YouTubeApi#youtubeGetPlaylistDetail");
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
| **playlistId** | **String**|  | |

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

<a id="youtubeGetVideoDetail"></a>
# **youtubeGetVideoDetail**
> Object youtubeGetVideoDetail(videoId, gl, hl)

Get video detail

Full video detail — merged player + next (likes, comments, chapters, related).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.YouTubeApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    YouTubeApi apiInstance = new YouTubeApi(defaultClient);
    String videoId = "videoId_example"; // String | 
    String gl = "gl_example"; // String | 
    String hl = "hl_example"; // String | 
    try {
      Object result = apiInstance.youtubeGetVideoDetail(videoId, gl, hl);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling YouTubeApi#youtubeGetVideoDetail");
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
| **gl** | **String**|  | [optional] |
| **hl** | **String**|  | [optional] |

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

<a id="youtubeGuestHomeFeed"></a>
# **youtubeGuestHomeFeed**
> Object youtubeGuestHomeFeed()

Guest home feed

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.YouTubeApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    YouTubeApi apiInstance = new YouTubeApi(defaultClient);
    try {
      Object result = apiInstance.youtubeGuestHomeFeed();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling YouTubeApi#youtubeGuestHomeFeed");
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

<a id="youtubeKeywordSuggestions"></a>
# **youtubeKeywordSuggestions**
> Object youtubeKeywordSuggestions(query, gl, hl)

Keyword suggestions

Return YouTube keyword autocomplete suggestions.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.YouTubeApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    YouTubeApi apiInstance = new YouTubeApi(defaultClient);
    String query = "query_example"; // String | Partial query prefix
    String gl = "gl_example"; // String | 
    String hl = "hl_example"; // String | 
    try {
      Object result = apiInstance.youtubeKeywordSuggestions(query, gl, hl);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling YouTubeApi#youtubeKeywordSuggestions");
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
| **query** | **String**| Partial query prefix | |
| **gl** | **String**|  | [optional] |
| **hl** | **String**|  | [optional] |

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

<a id="youtubeListCaptionTracks"></a>
# **youtubeListCaptionTracks**
> Object youtubeListCaptionTracks(videoId)

List caption tracks

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.YouTubeApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    YouTubeApi apiInstance = new YouTubeApi(defaultClient);
    String videoId = "videoId_example"; // String | 
    try {
      Object result = apiInstance.youtubeListCaptionTracks(videoId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling YouTubeApi#youtubeListCaptionTracks");
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

<a id="youtubeLiveChatMessages"></a>
# **youtubeLiveChatMessages**
> Object youtubeLiveChatMessages(videoId, continuation, replay)

Live chat messages

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.YouTubeApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    YouTubeApi apiInstance = new YouTubeApi(defaultClient);
    String videoId = "videoId_example"; // String | 
    String continuation = "continuation_example"; // String | 
    Boolean replay = false; // Boolean | 
    try {
      Object result = apiInstance.youtubeLiveChatMessages(videoId, continuation, replay);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling YouTubeApi#youtubeLiveChatMessages");
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
| **continuation** | **String**|  | [optional] |
| **replay** | **Boolean**|  | [optional] [default to false] |

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

<a id="youtubeOembedMetadata"></a>
# **youtubeOembedMetadata**
> Object youtubeOembedMetadata(url)

oEmbed metadata

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.YouTubeApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    YouTubeApi apiInstance = new YouTubeApi(defaultClient);
    String url = "url_example"; // String | A YouTube URL
    try {
      Object result = apiInstance.youtubeOembedMetadata(url);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling YouTubeApi#youtubeOembedMetadata");
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
| **url** | **String**| A YouTube URL | |

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

<a id="youtubePlaylistItemsPage"></a>
# **youtubePlaylistItemsPage**
> Object youtubePlaylistItemsPage(playlistId)

Playlist items page

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.YouTubeApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    YouTubeApi apiInstance = new YouTubeApi(defaultClient);
    String playlistId = "playlistId_example"; // String | 
    try {
      Object result = apiInstance.youtubePlaylistItemsPage(playlistId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling YouTubeApi#youtubePlaylistItemsPage");
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
| **playlistId** | **String**|  | |

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

<a id="youtubeRelatedVideos"></a>
# **youtubeRelatedVideos**
> Object youtubeRelatedVideos(videoId)

Related videos

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.YouTubeApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    YouTubeApi apiInstance = new YouTubeApi(defaultClient);
    String videoId = "videoId_example"; // String | 
    try {
      Object result = apiInstance.youtubeRelatedVideos(videoId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling YouTubeApi#youtubeRelatedVideos");
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

<a id="youtubeResolveHandleUrlToId"></a>
# **youtubeResolveHandleUrlToId**
> Object youtubeResolveHandleUrlToId(handle, url)

Resolve handle/URL to id

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.YouTubeApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    YouTubeApi apiInstance = new YouTubeApi(defaultClient);
    String handle = "handle_example"; // String | 
    String url = "url_example"; // String | 
    try {
      Object result = apiInstance.youtubeResolveHandleUrlToId(handle, url);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling YouTubeApi#youtubeResolveHandleUrlToId");
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
| **handle** | **String**|  | [optional] |
| **url** | **String**|  | [optional] |

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

<a id="youtubeSearchWithinAChannel"></a>
# **youtubeSearchWithinAChannel**
> Object youtubeSearchWithinAChannel(channelId, query)

Search within a channel

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.YouTubeApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    YouTubeApi apiInstance = new YouTubeApi(defaultClient);
    String channelId = "channelId_example"; // String | 
    String query = "query_example"; // String | Search keywords
    try {
      Object result = apiInstance.youtubeSearchWithinAChannel(channelId, query);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling YouTubeApi#youtubeSearchWithinAChannel");
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
| **channelId** | **String**|  | |
| **query** | **String**| Search keywords | |

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

<a id="youtubeSearchYoutube"></a>
# **youtubeSearchYoutube**
> Object youtubeSearchYoutube(query, type, sortBy, uploadDate, duration, features, gl, hl, continuation)

Search YouTube

Search videos / channels / playlists with the full filter matrix.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.YouTubeApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    YouTubeApi apiInstance = new YouTubeApi(defaultClient);
    String query = "query_example"; // String | Search keywords
    String type = "type_example"; // String | video|channel|playlist|movie|all
    String sortBy = "sortBy_example"; // String | relevance|date|views|rating
    String uploadDate = "uploadDate_example"; // String | hour|today|week|month|year
    String duration = "duration_example"; // String | short|medium|long
    String features = "features_example"; // String | hd,4k,360,vr180,3d,hdr,cc,subtitles,live
    String gl = "gl_example"; // String | Content region (US, GB, DE…)
    String hl = "hl_example"; // String | UI language
    String continuation = "continuation_example"; // String | 
    try {
      Object result = apiInstance.youtubeSearchYoutube(query, type, sortBy, uploadDate, duration, features, gl, hl, continuation);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling YouTubeApi#youtubeSearchYoutube");
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
| **query** | **String**| Search keywords | |
| **type** | **String**| video|channel|playlist|movie|all | [optional] |
| **sortBy** | **String**| relevance|date|views|rating | [optional] |
| **uploadDate** | **String**| hour|today|week|month|year | [optional] |
| **duration** | **String**| short|medium|long | [optional] |
| **features** | **String**| hd,4k,360,vr180,3d,hdr,cc,subtitles,live | [optional] |
| **gl** | **String**| Content region (US, GB, DE…) | [optional] |
| **hl** | **String**| UI language | [optional] |
| **continuation** | **String**|  | [optional] |

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

<a id="youtubeSearchYoutubeMusic"></a>
# **youtubeSearchYoutubeMusic**
> Object youtubeSearchYoutubeMusic(query)

Search YouTube Music

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.YouTubeApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    YouTubeApi apiInstance = new YouTubeApi(defaultClient);
    String query = "query_example"; // String | Search keywords
    try {
      Object result = apiInstance.youtubeSearchYoutubeMusic(query);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling YouTubeApi#youtubeSearchYoutubeMusic");
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
| **query** | **String**| Search keywords | |

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

<a id="youtubeShortsBySound"></a>
# **youtubeShortsBySound**
> Object youtubeShortsBySound(soundId)

Shorts by sound

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.YouTubeApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    YouTubeApi apiInstance = new YouTubeApi(defaultClient);
    String soundId = "soundId_example"; // String | 
    try {
      Object result = apiInstance.youtubeShortsBySound(soundId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling YouTubeApi#youtubeShortsBySound");
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
| **soundId** | **String**|  | |

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

<a id="youtubeStreamFormats"></a>
# **youtubeStreamFormats**
> Object youtubeStreamFormats(videoId, client)

Stream formats

Stream/format metadata (best-effort; media URLs may be PO-token gated).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.YouTubeApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    YouTubeApi apiInstance = new YouTubeApi(defaultClient);
    String videoId = "videoId_example"; // String | 
    String client = "IOS"; // String | IOS|ANDROID|WEB
    try {
      Object result = apiInstance.youtubeStreamFormats(videoId, client);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling YouTubeApi#youtubeStreamFormats");
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
| **client** | **String**| IOS|ANDROID|WEB | [optional] [default to IOS] |

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

<a id="youtubeSubscriberCountFast"></a>
# **youtubeSubscriberCountFast**
> Object youtubeSubscriberCountFast(channelId)

Subscriber count (fast)

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.YouTubeApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    YouTubeApi apiInstance = new YouTubeApi(defaultClient);
    String channelId = "channelId_example"; // String | 
    try {
      Object result = apiInstance.youtubeSubscriberCountFast(channelId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling YouTubeApi#youtubeSubscriberCountFast");
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
| **channelId** | **String**|  | |

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

<a id="youtubeSupportedMarkets"></a>
# **youtubeSupportedMarkets**
> Object youtubeSupportedMarkets()

Supported markets

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.YouTubeApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    YouTubeApi apiInstance = new YouTubeApi(defaultClient);
    try {
      Object result = apiInstance.youtubeSupportedMarkets();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling YouTubeApi#youtubeSupportedMarkets");
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

<a id="youtubeTrendingShorts"></a>
# **youtubeTrendingShorts**
> Object youtubeTrendingShorts()

Trending shorts

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.YouTubeApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    YouTubeApi apiInstance = new YouTubeApi(defaultClient);
    try {
      Object result = apiInstance.youtubeTrendingShorts();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling YouTubeApi#youtubeTrendingShorts");
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

<a id="youtubeTrendingVideos"></a>
# **youtubeTrendingVideos**
> Object youtubeTrendingVideos(gl, type)

Trending videos

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.YouTubeApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    YouTubeApi apiInstance = new YouTubeApi(defaultClient);
    String gl = "gl_example"; // String | 
    String type = "now"; // String | now|music|gaming|movies
    try {
      Object result = apiInstance.youtubeTrendingVideos(gl, type);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling YouTubeApi#youtubeTrendingVideos");
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
| **gl** | **String**|  | [optional] |
| **type** | **String**| now|music|gaming|movies | [optional] [default to now] |

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

<a id="youtubeUiLanguages"></a>
# **youtubeUiLanguages**
> Object youtubeUiLanguages()

UI languages

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.YouTubeApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    YouTubeApi apiInstance = new YouTubeApi(defaultClient);
    try {
      Object result = apiInstance.youtubeUiLanguages();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling YouTubeApi#youtubeUiLanguages");
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

<a id="youtubeVideoCategories"></a>
# **youtubeVideoCategories**
> Object youtubeVideoCategories(gl)

Video categories

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.YouTubeApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    YouTubeApi apiInstance = new YouTubeApi(defaultClient);
    String gl = "US"; // String | 
    try {
      Object result = apiInstance.youtubeVideoCategories(gl);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling YouTubeApi#youtubeVideoCategories");
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
| **gl** | **String**|  | [optional] [default to US] |

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

<a id="youtubeVideoComments"></a>
# **youtubeVideoComments**
> Object youtubeVideoComments(videoId, sortBy, continuation)

Video comments

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.YouTubeApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    YouTubeApi apiInstance = new YouTubeApi(defaultClient);
    String videoId = "videoId_example"; // String | 
    String sortBy = "top"; // String | top|newest
    String continuation = "continuation_example"; // String | 
    try {
      Object result = apiInstance.youtubeVideoComments(videoId, sortBy, continuation);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling YouTubeApi#youtubeVideoComments");
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
| **sortBy** | **String**| top|newest | [optional] [default to top] |
| **continuation** | **String**|  | [optional] |

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

<a id="youtubeVideoTranscript"></a>
# **youtubeVideoTranscript**
> Object youtubeVideoTranscript(videoId, language)

Video transcript

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.YouTubeApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    YouTubeApi apiInstance = new YouTubeApi(defaultClient);
    String videoId = "videoId_example"; // String | 
    String language = "language_example"; // String | BCP-47 language code
    try {
      Object result = apiInstance.youtubeVideoTranscript(videoId, language);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling YouTubeApi#youtubeVideoTranscript");
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
| **language** | **String**| BCP-47 language code | [optional] |

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

<a id="youtubeVideosUnderAHashtag"></a>
# **youtubeVideosUnderAHashtag**
> Object youtubeVideosUnderAHashtag(tag)

Videos under a hashtag

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.YouTubeApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    YouTubeApi apiInstance = new YouTubeApi(defaultClient);
    String tag = "tag_example"; // String | 
    try {
      Object result = apiInstance.youtubeVideosUnderAHashtag(tag);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling YouTubeApi#youtubeVideosUnderAHashtag");
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

<a id="youtubeYoutubeScraperHealthCheck"></a>
# **youtubeYoutubeScraperHealthCheck**
> Object youtubeYoutubeScraperHealthCheck()

YouTube scraper health check

Check health of the YouTube scraper service (accepts HEAD for UptimeRobot).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.YouTubeApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    YouTubeApi apiInstance = new YouTubeApi(defaultClient);
    try {
      Object result = apiInstance.youtubeYoutubeScraperHealthCheck();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling YouTubeApi#youtubeYoutubeScraperHealthCheck");
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

<a id="youtubeYoutubeScraperHealthCheckHead"></a>
# **youtubeYoutubeScraperHealthCheckHead**
> Object youtubeYoutubeScraperHealthCheckHead()

YouTube scraper health check

Check health of the YouTube scraper service (accepts HEAD for UptimeRobot).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.YouTubeApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    YouTubeApi apiInstance = new YouTubeApi(defaultClient);
    try {
      Object result = apiInstance.youtubeYoutubeScraperHealthCheckHead();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling YouTubeApi#youtubeYoutubeScraperHealthCheckHead");
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

