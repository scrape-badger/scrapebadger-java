# TwitterApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**twitterAdvancedTweetSearch**](TwitterApi.md#twitterAdvancedTweetSearch) | **GET** /v1/twitter/tweets/advanced_search | Advanced tweet search |
| [**twitterBatchGetUsersByIds**](TwitterApi.md#twitterBatchGetUsersByIds) | **GET** /v1/twitter/users/batch_by_ids | Batch get users by IDs |
| [**twitterBatchGetUsersByUsernames**](TwitterApi.md#twitterBatchGetUsersByUsernames) | **GET** /v1/twitter/users/batch_by_usernames | Batch get users by usernames |
| [**twitterConfigureWebhookOnAMonitor**](TwitterApi.md#twitterConfigureWebhookOnAMonitor) | **POST** /v1/twitter/stream/webhooks | Configure webhook on a monitor |
| [**twitterCreateFilterRule**](TwitterApi.md#twitterCreateFilterRule) | **POST** /v1/twitter/stream/filter-rules | Create filter rule |
| [**twitterCreateStreamMonitor**](TwitterApi.md#twitterCreateStreamMonitor) | **POST** /v1/twitter/stream/monitors | Create stream monitor |
| [**twitterDeleteFilterRule**](TwitterApi.md#twitterDeleteFilterRule) | **DELETE** /v1/twitter/stream/filter-rules/{rule_id} | Delete filter rule |
| [**twitterDeleteStreamMonitor**](TwitterApi.md#twitterDeleteStreamMonitor) | **DELETE** /v1/twitter/stream/monitors/{monitor_id} | Delete stream monitor |
| [**twitterGetArticleById**](TwitterApi.md#twitterGetArticleById) | **GET** /v1/twitter/tweets/article/{article_id} | Get article by ID |
| [**twitterGetBroadcastDetails**](TwitterApi.md#twitterGetBroadcastDetails) | **GET** /v1/twitter/spaces/broadcast/{broadcast_id} | Get broadcast details |
| [**twitterGetCommunityDetails**](TwitterApi.md#twitterGetCommunityDetails) | **GET** /v1/twitter/communities/{community_id} | Get community details |
| [**twitterGetCommunityNotes**](TwitterApi.md#twitterGetCommunityNotes) | **GET** /v1/twitter/tweets/tweet/{tweet_id}/community_notes | Get community notes |
| [**twitterGetCommunityTweets**](TwitterApi.md#twitterGetCommunityTweets) | **GET** /v1/twitter/communities/{community_id}/tweets | Get community tweets |
| [**twitterGetFilterRule**](TwitterApi.md#twitterGetFilterRule) | **GET** /v1/twitter/stream/filter-rules/{rule_id} | Get filter rule |
| [**twitterGetFilterRulePerPollRates**](TwitterApi.md#twitterGetFilterRulePerPollRates) | **GET** /v1/twitter/stream/filter-rules-pricing | Get filter rule per-poll rates |
| [**twitterGetListDetails**](TwitterApi.md#twitterGetListDetails) | **GET** /v1/twitter/lists/{list_id}/detail | Get list details |
| [**twitterGetListTweets**](TwitterApi.md#twitterGetListTweets) | **GET** /v1/twitter/lists/{list_id}/tweets | Get list tweets |
| [**twitterGetPlaceDetails**](TwitterApi.md#twitterGetPlaceDetails) | **GET** /v1/twitter/geo/places/{place_id} | Get place details |
| [**twitterGetSimilarTweets**](TwitterApi.md#twitterGetSimilarTweets) | **GET** /v1/twitter/tweets/tweet/{tweet_id}/similar | Get similar tweets |
| [**twitterGetSpaceDetails**](TwitterApi.md#twitterGetSpaceDetails) | **GET** /v1/twitter/spaces/{space_id} | Get Space details |
| [**twitterGetStreamMonitor**](TwitterApi.md#twitterGetStreamMonitor) | **GET** /v1/twitter/stream/monitors/{monitor_id} | Get stream monitor |
| [**twitterGetTrendingTopics**](TwitterApi.md#twitterGetTrendingTopics) | **GET** /v1/twitter/trends/ | Get trending topics |
| [**twitterGetTrendsByLocation**](TwitterApi.md#twitterGetTrendsByLocation) | **GET** /v1/twitter/trends/place/{woeid} | Get trends by location |
| [**twitterGetTweetDetails**](TwitterApi.md#twitterGetTweetDetails) | **GET** /v1/twitter/tweets/tweet/{tweet_id} | Get tweet details |
| [**twitterGetTweetEditHistory**](TwitterApi.md#twitterGetTweetEditHistory) | **GET** /v1/twitter/tweets/tweet/{tweet_id}/edit_history | Get tweet edit history |
| [**twitterGetTweetFavoriters**](TwitterApi.md#twitterGetTweetFavoriters) | **GET** /v1/twitter/tweets/tweet/{tweet_id}/favoriters | Get tweet favoriters |
| [**twitterGetTweetQuotes**](TwitterApi.md#twitterGetTweetQuotes) | **GET** /v1/twitter/tweets/tweet/{tweet_id}/quotes | Get tweet quotes |
| [**twitterGetTweetReplies**](TwitterApi.md#twitterGetTweetReplies) | **GET** /v1/twitter/tweets/tweet/{tweet_id}/replies | Get tweet replies |
| [**twitterGetTweetRetweeters**](TwitterApi.md#twitterGetTweetRetweeters) | **GET** /v1/twitter/tweets/tweet/{tweet_id}/retweeters | Get tweet retweeters |
| [**twitterGetTweetsByIds**](TwitterApi.md#twitterGetTweetsByIds) | **GET** /v1/twitter/tweets/ | Get tweets by IDs |
| [**twitterGetUserArticles**](TwitterApi.md#twitterGetUserArticles) | **GET** /v1/twitter/users/{user_id}/articles | Get user articles |
| [**twitterGetUserById**](TwitterApi.md#twitterGetUserById) | **GET** /v1/twitter/users/{user_id}/by_id | Get user by ID |
| [**twitterGetUserByUsername**](TwitterApi.md#twitterGetUserByUsername) | **GET** /v1/twitter/users/{username}/by_username | Get user by username |
| [**twitterGetUserFollowers**](TwitterApi.md#twitterGetUserFollowers) | **GET** /v1/twitter/users/{username}/followers | Get user followers |
| [**twitterGetUserFollowing**](TwitterApi.md#twitterGetUserFollowing) | **GET** /v1/twitter/users/{username}/followings | Get user following |
| [**twitterGetUserMentions**](TwitterApi.md#twitterGetUserMentions) | **GET** /v1/twitter/users/{username}/mentions | Get user mentions |
| [**twitterGetUserSubscriptions**](TwitterApi.md#twitterGetUserSubscriptions) | **GET** /v1/twitter/users/{user_id}/subscriptions | Get user subscriptions |
| [**twitterGetUserTweets**](TwitterApi.md#twitterGetUserTweets) | **GET** /v1/twitter/users/{username}/latest_tweets | Get user tweets |
| [**twitterListBillingLogs**](TwitterApi.md#twitterListBillingLogs) | **GET** /v1/twitter/stream/billing-logs | List billing logs |
| [**twitterListDeliveryLogsForAFilterRule**](TwitterApi.md#twitterListDeliveryLogsForAFilterRule) | **GET** /v1/twitter/stream/filter-rules/{rule_id}/logs | List delivery logs for a filter rule |
| [**twitterListFilterRules**](TwitterApi.md#twitterListFilterRules) | **GET** /v1/twitter/stream/filter-rules | List filter rules |
| [**twitterListStreamMonitors**](TwitterApi.md#twitterListStreamMonitors) | **GET** /v1/twitter/stream/monitors | List stream monitors |
| [**twitterListTweetDeliveryLogs**](TwitterApi.md#twitterListTweetDeliveryLogs) | **GET** /v1/twitter/stream/logs | List tweet delivery logs |
| [**twitterListWebhooks**](TwitterApi.md#twitterListWebhooks) | **GET** /v1/twitter/stream/webhooks | List webhooks |
| [**twitterRemoveWebhookFromMonitor**](TwitterApi.md#twitterRemoveWebhookFromMonitor) | **DELETE** /v1/twitter/stream/webhooks/{webhook_id} | Remove webhook from monitor |
| [**twitterSearchCommunities**](TwitterApi.md#twitterSearchCommunities) | **GET** /v1/twitter/communities/search | Search communities |
| [**twitterSearchListTweets**](TwitterApi.md#twitterSearchListTweets) | **GET** /v1/twitter/lists/{list_id}/search_tweets | Search list tweets |
| [**twitterSearchPlaces**](TwitterApi.md#twitterSearchPlaces) | **GET** /v1/twitter/geo/search | Search places |
| [**twitterSearchUsers**](TwitterApi.md#twitterSearchUsers) | **GET** /v1/twitter/users/search_users | Search users |
| [**twitterTestWebhookDelivery**](TwitterApi.md#twitterTestWebhookDelivery) | **POST** /v1/twitter/stream/webhooks/test | Test webhook delivery |
| [**twitterTwitterScraperHealthCheck**](TwitterApi.md#twitterTwitterScraperHealthCheck) | **GET** /v1/twitter/health | Twitter scraper health check |
| [**twitterTwitterScraperHealthCheckHead**](TwitterApi.md#twitterTwitterScraperHealthCheckHead) | **HEAD** /v1/twitter/health | Twitter scraper health check |
| [**twitterUpdateFilterRule**](TwitterApi.md#twitterUpdateFilterRule) | **PATCH** /v1/twitter/stream/filter-rules/{rule_id} | Update filter rule |
| [**twitterUpdateStreamMonitor**](TwitterApi.md#twitterUpdateStreamMonitor) | **PATCH** /v1/twitter/stream/monitors/{monitor_id} | Update stream monitor |
| [**twitterValidateSearchQuery**](TwitterApi.md#twitterValidateSearchQuery) | **POST** /v1/twitter/stream/filter-rules/validate | Validate search query |


<a id="twitterAdvancedTweetSearch"></a>
# **twitterAdvancedTweetSearch**
> Object twitterAdvancedTweetSearch(query, queryType, count, cursor)

Advanced tweet search

Search tweets with advanced options.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TwitterApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TwitterApi apiInstance = new TwitterApi(defaultClient);
    String query = "query_example"; // String | 
    String queryType = "queryType_example"; // String | 
    Integer count = 56; // Integer | 
    String cursor = "cursor_example"; // String | 
    try {
      Object result = apiInstance.twitterAdvancedTweetSearch(query, queryType, count, cursor);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TwitterApi#twitterAdvancedTweetSearch");
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
| **queryType** | **String**|  | [optional] |
| **count** | **Integer**|  | [optional] |
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

<a id="twitterBatchGetUsersByIds"></a>
# **twitterBatchGetUsersByIds**
> Object twitterBatchGetUsersByIds(userIds)

Batch get users by IDs

Get multiple user profiles by their numeric IDs (comma-separated).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TwitterApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TwitterApi apiInstance = new TwitterApi(defaultClient);
    String userIds = "userIds_example"; // String | 
    try {
      Object result = apiInstance.twitterBatchGetUsersByIds(userIds);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TwitterApi#twitterBatchGetUsersByIds");
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
| **userIds** | **String**|  | |

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

<a id="twitterBatchGetUsersByUsernames"></a>
# **twitterBatchGetUsersByUsernames**
> Object twitterBatchGetUsersByUsernames(usernames)

Batch get users by usernames

Get multiple user profiles by their usernames (comma-separated).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TwitterApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TwitterApi apiInstance = new TwitterApi(defaultClient);
    String usernames = "usernames_example"; // String | 
    try {
      Object result = apiInstance.twitterBatchGetUsersByUsernames(usernames);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TwitterApi#twitterBatchGetUsersByUsernames");
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
| **usernames** | **String**|  | |

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

<a id="twitterConfigureWebhookOnAMonitor"></a>
# **twitterConfigureWebhookOnAMonitor**
> WebhookResponse twitterConfigureWebhookOnAMonitor(webhookCreate)

Configure webhook on a monitor

Configure a webhook delivery URL on a stream monitor.  The secret is returned only once on creation. Subsequent calls show secret_set: bool. If monitor already has a webhook, delete it first (409 is returned).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TwitterApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TwitterApi apiInstance = new TwitterApi(defaultClient);
    WebhookCreate webhookCreate = new WebhookCreate(); // WebhookCreate | 
    try {
      WebhookResponse result = apiInstance.twitterConfigureWebhookOnAMonitor(webhookCreate);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TwitterApi#twitterConfigureWebhookOnAMonitor");
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
| **webhookCreate** | [**WebhookCreate**](WebhookCreate.md)|  | |

### Return type

[**WebhookResponse**](WebhookResponse.md)

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

<a id="twitterCreateFilterRule"></a>
# **twitterCreateFilterRule**
> FilterRuleResponse twitterCreateFilterRule(filterRuleCreate)

Create filter rule

Create a new query-based tweet filter rule.  The rule starts in &#39;active&#39; status immediately. Credits must be positive. The (api_key_id, tag) pair must be unique.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TwitterApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TwitterApi apiInstance = new TwitterApi(defaultClient);
    FilterRuleCreate filterRuleCreate = new FilterRuleCreate(); // FilterRuleCreate | 
    try {
      FilterRuleResponse result = apiInstance.twitterCreateFilterRule(filterRuleCreate);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TwitterApi#twitterCreateFilterRule");
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
| **filterRuleCreate** | [**FilterRuleCreate**](FilterRuleCreate.md)|  | |

### Return type

[**FilterRuleResponse**](FilterRuleResponse.md)

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

<a id="twitterCreateStreamMonitor"></a>
# **twitterCreateStreamMonitor**
> StreamMonitorResponse twitterCreateStreamMonitor(streamMonitorCreate)

Create stream monitor

Create a new stream monitor to watch Twitter accounts in real-time.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TwitterApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TwitterApi apiInstance = new TwitterApi(defaultClient);
    StreamMonitorCreate streamMonitorCreate = new StreamMonitorCreate(); // StreamMonitorCreate | 
    try {
      StreamMonitorResponse result = apiInstance.twitterCreateStreamMonitor(streamMonitorCreate);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TwitterApi#twitterCreateStreamMonitor");
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
| **streamMonitorCreate** | [**StreamMonitorCreate**](StreamMonitorCreate.md)|  | |

### Return type

[**StreamMonitorResponse**](StreamMonitorResponse.md)

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

<a id="twitterDeleteFilterRule"></a>
# **twitterDeleteFilterRule**
> twitterDeleteFilterRule(ruleId)

Delete filter rule

Delete a filter rule and all its logs.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TwitterApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TwitterApi apiInstance = new TwitterApi(defaultClient);
    String ruleId = "ruleId_example"; // String | 
    try {
      apiInstance.twitterDeleteFilterRule(ruleId);
    } catch (ApiException e) {
      System.err.println("Exception when calling TwitterApi#twitterDeleteFilterRule");
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
| **ruleId** | **String**|  | |

### Return type

null (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **204** | Successful Response |  -  |
| **422** | Validation Error |  -  |

<a id="twitterDeleteStreamMonitor"></a>
# **twitterDeleteStreamMonitor**
> twitterDeleteStreamMonitor(monitorId)

Delete stream monitor

Delete a stream monitor and all its logs.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TwitterApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TwitterApi apiInstance = new TwitterApi(defaultClient);
    String monitorId = "monitorId_example"; // String | 
    try {
      apiInstance.twitterDeleteStreamMonitor(monitorId);
    } catch (ApiException e) {
      System.err.println("Exception when calling TwitterApi#twitterDeleteStreamMonitor");
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
| **monitorId** | **String**|  | |

### Return type

null (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **204** | Successful Response |  -  |
| **422** | Validation Error |  -  |

<a id="twitterGetArticleById"></a>
# **twitterGetArticleById**
> Object twitterGetArticleById(articleId)

Get article by ID

Get a long-form article by its ID.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TwitterApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TwitterApi apiInstance = new TwitterApi(defaultClient);
    String articleId = "articleId_example"; // String | 
    try {
      Object result = apiInstance.twitterGetArticleById(articleId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TwitterApi#twitterGetArticleById");
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
| **articleId** | **String**|  | |

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

<a id="twitterGetBroadcastDetails"></a>
# **twitterGetBroadcastDetails**
> Object twitterGetBroadcastDetails(broadcastId)

Get broadcast details

Get details of a live video broadcast.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TwitterApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TwitterApi apiInstance = new TwitterApi(defaultClient);
    String broadcastId = "broadcastId_example"; // String | 
    try {
      Object result = apiInstance.twitterGetBroadcastDetails(broadcastId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TwitterApi#twitterGetBroadcastDetails");
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
| **broadcastId** | **String**|  | |

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

<a id="twitterGetCommunityDetails"></a>
# **twitterGetCommunityDetails**
> Object twitterGetCommunityDetails(communityId)

Get community details

Get details of a specific community.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TwitterApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TwitterApi apiInstance = new TwitterApi(defaultClient);
    String communityId = "communityId_example"; // String | 
    try {
      Object result = apiInstance.twitterGetCommunityDetails(communityId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TwitterApi#twitterGetCommunityDetails");
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
| **communityId** | **String**|  | |

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

<a id="twitterGetCommunityNotes"></a>
# **twitterGetCommunityNotes**
> Object twitterGetCommunityNotes(tweetId)

Get community notes

Get community notes (Birdwatch) for a specific tweet.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TwitterApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TwitterApi apiInstance = new TwitterApi(defaultClient);
    String tweetId = "tweetId_example"; // String | 
    try {
      Object result = apiInstance.twitterGetCommunityNotes(tweetId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TwitterApi#twitterGetCommunityNotes");
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
| **tweetId** | **String**|  | |

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

<a id="twitterGetCommunityTweets"></a>
# **twitterGetCommunityTweets**
> Object twitterGetCommunityTweets(communityId, tweetType, cursor)

Get community tweets

Get tweets from a specific community.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TwitterApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TwitterApi apiInstance = new TwitterApi(defaultClient);
    String communityId = "communityId_example"; // String | 
    String tweetType = "tweetType_example"; // String | 
    String cursor = "cursor_example"; // String | 
    try {
      Object result = apiInstance.twitterGetCommunityTweets(communityId, tweetType, cursor);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TwitterApi#twitterGetCommunityTweets");
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
| **communityId** | **String**|  | |
| **tweetType** | **String**|  | [optional] |
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

<a id="twitterGetFilterRule"></a>
# **twitterGetFilterRule**
> FilterRuleResponse twitterGetFilterRule(ruleId)

Get filter rule

Get a single filter rule by ID.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TwitterApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TwitterApi apiInstance = new TwitterApi(defaultClient);
    String ruleId = "ruleId_example"; // String | 
    try {
      FilterRuleResponse result = apiInstance.twitterGetFilterRule(ruleId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TwitterApi#twitterGetFilterRule");
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
| **ruleId** | **String**|  | |

### Return type

[**FilterRuleResponse**](FilterRuleResponse.md)

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

<a id="twitterGetFilterRulePerPollRates"></a>
# **twitterGetFilterRulePerPollRates**
> PortalApiRoutersV1TwitterFilterRulesFilterRulePricingResponse twitterGetFilterRulePerPollRates()

Get filter rule per-poll rates

Current per-poll rates (auth required — used by SDK + dashboard).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TwitterApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TwitterApi apiInstance = new TwitterApi(defaultClient);
    try {
      PortalApiRoutersV1TwitterFilterRulesFilterRulePricingResponse result = apiInstance.twitterGetFilterRulePerPollRates();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TwitterApi#twitterGetFilterRulePerPollRates");
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

[**PortalApiRoutersV1TwitterFilterRulesFilterRulePricingResponse**](PortalApiRoutersV1TwitterFilterRulesFilterRulePricingResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |

<a id="twitterGetListDetails"></a>
# **twitterGetListDetails**
> Object twitterGetListDetails(listId)

Get list details

Get details of a specific list.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TwitterApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TwitterApi apiInstance = new TwitterApi(defaultClient);
    String listId = "listId_example"; // String | 
    try {
      Object result = apiInstance.twitterGetListDetails(listId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TwitterApi#twitterGetListDetails");
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
| **listId** | **String**|  | |

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

<a id="twitterGetListTweets"></a>
# **twitterGetListTweets**
> Object twitterGetListTweets(listId, cursor)

Get list tweets

Get tweets from a specific list.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TwitterApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TwitterApi apiInstance = new TwitterApi(defaultClient);
    String listId = "listId_example"; // String | 
    String cursor = "cursor_example"; // String | 
    try {
      Object result = apiInstance.twitterGetListTweets(listId, cursor);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TwitterApi#twitterGetListTweets");
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
| **listId** | **String**|  | |
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

<a id="twitterGetPlaceDetails"></a>
# **twitterGetPlaceDetails**
> Object twitterGetPlaceDetails(placeId)

Get place details

Get details of a specific place.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TwitterApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TwitterApi apiInstance = new TwitterApi(defaultClient);
    String placeId = "placeId_example"; // String | 
    try {
      Object result = apiInstance.twitterGetPlaceDetails(placeId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TwitterApi#twitterGetPlaceDetails");
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
| **placeId** | **String**|  | |

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

<a id="twitterGetSimilarTweets"></a>
# **twitterGetSimilarTweets**
> Object twitterGetSimilarTweets(tweetId)

Get similar tweets

Get tweets similar to a specific tweet.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TwitterApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TwitterApi apiInstance = new TwitterApi(defaultClient);
    String tweetId = "tweetId_example"; // String | 
    try {
      Object result = apiInstance.twitterGetSimilarTweets(tweetId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TwitterApi#twitterGetSimilarTweets");
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
| **tweetId** | **String**|  | |

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

<a id="twitterGetSpaceDetails"></a>
# **twitterGetSpaceDetails**
> Object twitterGetSpaceDetails(spaceId)

Get Space details

Get details of a Twitter Space.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TwitterApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TwitterApi apiInstance = new TwitterApi(defaultClient);
    String spaceId = "spaceId_example"; // String | 
    try {
      Object result = apiInstance.twitterGetSpaceDetails(spaceId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TwitterApi#twitterGetSpaceDetails");
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
| **spaceId** | **String**|  | |

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

<a id="twitterGetStreamMonitor"></a>
# **twitterGetStreamMonitor**
> StreamMonitorResponse twitterGetStreamMonitor(monitorId)

Get stream monitor

Get a single stream monitor by ID.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TwitterApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TwitterApi apiInstance = new TwitterApi(defaultClient);
    String monitorId = "monitorId_example"; // String | 
    try {
      StreamMonitorResponse result = apiInstance.twitterGetStreamMonitor(monitorId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TwitterApi#twitterGetStreamMonitor");
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
| **monitorId** | **String**|  | |

### Return type

[**StreamMonitorResponse**](StreamMonitorResponse.md)

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

<a id="twitterGetTrendingTopics"></a>
# **twitterGetTrendingTopics**
> Object twitterGetTrendingTopics(category, count)

Get trending topics

Get trending topics.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TwitterApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TwitterApi apiInstance = new TwitterApi(defaultClient);
    String category = "category_example"; // String | 
    Integer count = 56; // Integer | 
    try {
      Object result = apiInstance.twitterGetTrendingTopics(category, count);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TwitterApi#twitterGetTrendingTopics");
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
| **category** | **String**|  | [optional] |
| **count** | **Integer**|  | [optional] |

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

<a id="twitterGetTrendsByLocation"></a>
# **twitterGetTrendsByLocation**
> Object twitterGetTrendsByLocation(woeid)

Get trends by location

Get trending topics for a specific location (WOEID).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TwitterApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TwitterApi apiInstance = new TwitterApi(defaultClient);
    String woeid = "woeid_example"; // String | 
    try {
      Object result = apiInstance.twitterGetTrendsByLocation(woeid);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TwitterApi#twitterGetTrendsByLocation");
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
| **woeid** | **String**|  | |

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

<a id="twitterGetTweetDetails"></a>
# **twitterGetTweetDetails**
> Object twitterGetTweetDetails(tweetId, cursor)

Get tweet details

Get detailed information about a specific tweet.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TwitterApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TwitterApi apiInstance = new TwitterApi(defaultClient);
    String tweetId = "tweetId_example"; // String | 
    String cursor = "cursor_example"; // String | 
    try {
      Object result = apiInstance.twitterGetTweetDetails(tweetId, cursor);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TwitterApi#twitterGetTweetDetails");
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
| **tweetId** | **String**|  | |
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

<a id="twitterGetTweetEditHistory"></a>
# **twitterGetTweetEditHistory**
> Object twitterGetTweetEditHistory(tweetId)

Get tweet edit history

Get the edit history of a tweet.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TwitterApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TwitterApi apiInstance = new TwitterApi(defaultClient);
    String tweetId = "tweetId_example"; // String | 
    try {
      Object result = apiInstance.twitterGetTweetEditHistory(tweetId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TwitterApi#twitterGetTweetEditHistory");
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
| **tweetId** | **String**|  | |

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

<a id="twitterGetTweetFavoriters"></a>
# **twitterGetTweetFavoriters**
> Object twitterGetTweetFavoriters(tweetId, cursor)

Get tweet favoriters

Get users who favorited a specific tweet.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TwitterApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TwitterApi apiInstance = new TwitterApi(defaultClient);
    String tweetId = "tweetId_example"; // String | 
    String cursor = "cursor_example"; // String | 
    try {
      Object result = apiInstance.twitterGetTweetFavoriters(tweetId, cursor);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TwitterApi#twitterGetTweetFavoriters");
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
| **tweetId** | **String**|  | |
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

<a id="twitterGetTweetQuotes"></a>
# **twitterGetTweetQuotes**
> Object twitterGetTweetQuotes(tweetId, cursor)

Get tweet quotes

Get tweets that quote a specific tweet.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TwitterApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TwitterApi apiInstance = new TwitterApi(defaultClient);
    String tweetId = "tweetId_example"; // String | 
    String cursor = "cursor_example"; // String | 
    try {
      Object result = apiInstance.twitterGetTweetQuotes(tweetId, cursor);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TwitterApi#twitterGetTweetQuotes");
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
| **tweetId** | **String**|  | |
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

<a id="twitterGetTweetReplies"></a>
# **twitterGetTweetReplies**
> Object twitterGetTweetReplies(tweetId, cursor)

Get tweet replies

Get replies to a specific tweet.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TwitterApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TwitterApi apiInstance = new TwitterApi(defaultClient);
    String tweetId = "tweetId_example"; // String | 
    String cursor = "cursor_example"; // String | 
    try {
      Object result = apiInstance.twitterGetTweetReplies(tweetId, cursor);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TwitterApi#twitterGetTweetReplies");
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
| **tweetId** | **String**|  | |
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

<a id="twitterGetTweetRetweeters"></a>
# **twitterGetTweetRetweeters**
> Object twitterGetTweetRetweeters(tweetId, cursor)

Get tweet retweeters

Get users who retweeted a specific tweet.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TwitterApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TwitterApi apiInstance = new TwitterApi(defaultClient);
    String tweetId = "tweetId_example"; // String | 
    String cursor = "cursor_example"; // String | 
    try {
      Object result = apiInstance.twitterGetTweetRetweeters(tweetId, cursor);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TwitterApi#twitterGetTweetRetweeters");
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
| **tweetId** | **String**|  | |
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

<a id="twitterGetTweetsByIds"></a>
# **twitterGetTweetsByIds**
> Object twitterGetTweetsByIds(tweets)

Get tweets by IDs

Get multiple tweets by their IDs.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TwitterApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TwitterApi apiInstance = new TwitterApi(defaultClient);
    String tweets = "tweets_example"; // String | 
    try {
      Object result = apiInstance.twitterGetTweetsByIds(tweets);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TwitterApi#twitterGetTweetsByIds");
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
| **tweets** | **String**|  | |

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

<a id="twitterGetUserArticles"></a>
# **twitterGetUserArticles**
> Object twitterGetUserArticles(userId, cursor)

Get user articles

Get long-form articles written by a user.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TwitterApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TwitterApi apiInstance = new TwitterApi(defaultClient);
    String userId = "userId_example"; // String | 
    String cursor = "cursor_example"; // String | 
    try {
      Object result = apiInstance.twitterGetUserArticles(userId, cursor);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TwitterApi#twitterGetUserArticles");
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
| **userId** | **String**|  | |
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

<a id="twitterGetUserById"></a>
# **twitterGetUserById**
> Object twitterGetUserById(userId)

Get user by ID

Get user profile by user ID.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TwitterApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TwitterApi apiInstance = new TwitterApi(defaultClient);
    String userId = "userId_example"; // String | 
    try {
      Object result = apiInstance.twitterGetUserById(userId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TwitterApi#twitterGetUserById");
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
| **userId** | **String**|  | |

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

<a id="twitterGetUserByUsername"></a>
# **twitterGetUserByUsername**
> Object twitterGetUserByUsername(username)

Get user by username

Get user profile by username.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TwitterApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TwitterApi apiInstance = new TwitterApi(defaultClient);
    String username = "username_example"; // String | 
    try {
      Object result = apiInstance.twitterGetUserByUsername(username);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TwitterApi#twitterGetUserByUsername");
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

<a id="twitterGetUserFollowers"></a>
# **twitterGetUserFollowers**
> Object twitterGetUserFollowers(username, cursor)

Get user followers

Get followers of a specific user.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TwitterApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TwitterApi apiInstance = new TwitterApi(defaultClient);
    String username = "username_example"; // String | 
    String cursor = "cursor_example"; // String | 
    try {
      Object result = apiInstance.twitterGetUserFollowers(username, cursor);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TwitterApi#twitterGetUserFollowers");
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

<a id="twitterGetUserFollowing"></a>
# **twitterGetUserFollowing**
> Object twitterGetUserFollowing(username, cursor)

Get user following

Get users that a specific user is following.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TwitterApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TwitterApi apiInstance = new TwitterApi(defaultClient);
    String username = "username_example"; // String | 
    String cursor = "cursor_example"; // String | 
    try {
      Object result = apiInstance.twitterGetUserFollowing(username, cursor);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TwitterApi#twitterGetUserFollowing");
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

<a id="twitterGetUserMentions"></a>
# **twitterGetUserMentions**
> Object twitterGetUserMentions(username, count, cursor)

Get user mentions

Get tweets mentioning a specific user.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TwitterApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TwitterApi apiInstance = new TwitterApi(defaultClient);
    String username = "username_example"; // String | 
    Integer count = 56; // Integer | 
    String cursor = "cursor_example"; // String | 
    try {
      Object result = apiInstance.twitterGetUserMentions(username, count, cursor);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TwitterApi#twitterGetUserMentions");
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
| **count** | **Integer**|  | [optional] |
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

<a id="twitterGetUserSubscriptions"></a>
# **twitterGetUserSubscriptions**
> Object twitterGetUserSubscriptions(userId, cursor)

Get user subscriptions

Get subscriptions of a specific user.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TwitterApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TwitterApi apiInstance = new TwitterApi(defaultClient);
    String userId = "userId_example"; // String | 
    String cursor = "cursor_example"; // String | 
    try {
      Object result = apiInstance.twitterGetUserSubscriptions(userId, cursor);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TwitterApi#twitterGetUserSubscriptions");
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
| **userId** | **String**|  | |
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

<a id="twitterGetUserTweets"></a>
# **twitterGetUserTweets**
> Object twitterGetUserTweets(username, cursor)

Get user tweets

Get latest tweets from a specific user.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TwitterApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TwitterApi apiInstance = new TwitterApi(defaultClient);
    String username = "username_example"; // String | 
    String cursor = "cursor_example"; // String | 
    try {
      Object result = apiInstance.twitterGetUserTweets(username, cursor);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TwitterApi#twitterGetUserTweets");
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

<a id="twitterListBillingLogs"></a>
# **twitterListBillingLogs**
> BillingLogListResponse twitterListBillingLogs(monitorId, page, pageSize)

List billing logs

List billing activity logs for the authenticated API key&#39;s monitors.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TwitterApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TwitterApi apiInstance = new TwitterApi(defaultClient);
    String monitorId = "monitorId_example"; // String | 
    Integer page = 1; // Integer | 
    Integer pageSize = 20; // Integer | 
    try {
      BillingLogListResponse result = apiInstance.twitterListBillingLogs(monitorId, page, pageSize);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TwitterApi#twitterListBillingLogs");
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
| **monitorId** | **String**|  | [optional] |
| **page** | **Integer**|  | [optional] [default to 1] |
| **pageSize** | **Integer**|  | [optional] [default to 20] |

### Return type

[**BillingLogListResponse**](BillingLogListResponse.md)

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

<a id="twitterListDeliveryLogsForAFilterRule"></a>
# **twitterListDeliveryLogsForAFilterRule**
> FilterRuleDeliveryLogListResponse twitterListDeliveryLogsForAFilterRule(ruleId, deliveryStatus, authorUsername, page, pageSize, sort)

List delivery logs for a filter rule

List tweet delivery logs for a specific filter rule.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TwitterApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TwitterApi apiInstance = new TwitterApi(defaultClient);
    String ruleId = "ruleId_example"; // String | 
    String deliveryStatus = "deliveryStatus_example"; // String | 
    String authorUsername = "authorUsername_example"; // String | 
    Integer page = 1; // Integer | 
    Integer pageSize = 20; // Integer | 
    String sort = "asc"; // String | 
    try {
      FilterRuleDeliveryLogListResponse result = apiInstance.twitterListDeliveryLogsForAFilterRule(ruleId, deliveryStatus, authorUsername, page, pageSize, sort);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TwitterApi#twitterListDeliveryLogsForAFilterRule");
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
| **ruleId** | **String**|  | |
| **deliveryStatus** | **String**|  | [optional] |
| **authorUsername** | **String**|  | [optional] |
| **page** | **Integer**|  | [optional] [default to 1] |
| **pageSize** | **Integer**|  | [optional] [default to 20] |
| **sort** | **String**|  | [optional] [default to desc] [enum: asc, desc] |

### Return type

[**FilterRuleDeliveryLogListResponse**](FilterRuleDeliveryLogListResponse.md)

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

<a id="twitterListFilterRules"></a>
# **twitterListFilterRules**
> FilterRuleListResponse twitterListFilterRules(status, page, pageSize)

List filter rules

List all filter rules for the authenticated API key.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TwitterApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TwitterApi apiInstance = new TwitterApi(defaultClient);
    String status = "status_example"; // String | 
    Integer page = 1; // Integer | 
    Integer pageSize = 20; // Integer | 
    try {
      FilterRuleListResponse result = apiInstance.twitterListFilterRules(status, page, pageSize);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TwitterApi#twitterListFilterRules");
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
| **status** | **String**|  | [optional] |
| **page** | **Integer**|  | [optional] [default to 1] |
| **pageSize** | **Integer**|  | [optional] [default to 20] |

### Return type

[**FilterRuleListResponse**](FilterRuleListResponse.md)

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

<a id="twitterListStreamMonitors"></a>
# **twitterListStreamMonitors**
> StreamMonitorListResponse twitterListStreamMonitors(status, page, pageSize)

List stream monitors

List all stream monitors for the authenticated API key.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TwitterApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TwitterApi apiInstance = new TwitterApi(defaultClient);
    String status = "status_example"; // String | 
    Integer page = 1; // Integer | 
    Integer pageSize = 20; // Integer | 
    try {
      StreamMonitorListResponse result = apiInstance.twitterListStreamMonitors(status, page, pageSize);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TwitterApi#twitterListStreamMonitors");
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
| **status** | **String**|  | [optional] |
| **page** | **Integer**|  | [optional] [default to 1] |
| **pageSize** | **Integer**|  | [optional] [default to 20] |

### Return type

[**StreamMonitorListResponse**](StreamMonitorListResponse.md)

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

<a id="twitterListTweetDeliveryLogs"></a>
# **twitterListTweetDeliveryLogs**
> TweetDeliveryLogListResponse twitterListTweetDeliveryLogs(monitorId, authorUsername, deliveryStatus, page, pageSize, sort)

List tweet delivery logs

List tweet delivery logs for the authenticated API key&#39;s monitors.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TwitterApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TwitterApi apiInstance = new TwitterApi(defaultClient);
    String monitorId = "monitorId_example"; // String | 
    String authorUsername = "authorUsername_example"; // String | 
    String deliveryStatus = "deliveryStatus_example"; // String | 
    Integer page = 1; // Integer | 
    Integer pageSize = 20; // Integer | 
    String sort = "asc"; // String | 
    try {
      TweetDeliveryLogListResponse result = apiInstance.twitterListTweetDeliveryLogs(monitorId, authorUsername, deliveryStatus, page, pageSize, sort);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TwitterApi#twitterListTweetDeliveryLogs");
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
| **monitorId** | **String**|  | [optional] |
| **authorUsername** | **String**|  | [optional] |
| **deliveryStatus** | **String**|  | [optional] |
| **page** | **Integer**|  | [optional] [default to 1] |
| **pageSize** | **Integer**|  | [optional] [default to 20] |
| **sort** | **String**|  | [optional] [default to desc] [enum: asc, desc] |

### Return type

[**TweetDeliveryLogListResponse**](TweetDeliveryLogListResponse.md)

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

<a id="twitterListWebhooks"></a>
# **twitterListWebhooks**
> WebhookListResponse twitterListWebhooks(monitorId)

List webhooks

List all webhook-configured monitors for the authenticated API key.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TwitterApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TwitterApi apiInstance = new TwitterApi(defaultClient);
    String monitorId = "monitorId_example"; // String | 
    try {
      WebhookListResponse result = apiInstance.twitterListWebhooks(monitorId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TwitterApi#twitterListWebhooks");
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
| **monitorId** | **String**|  | [optional] |

### Return type

[**WebhookListResponse**](WebhookListResponse.md)

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

<a id="twitterRemoveWebhookFromMonitor"></a>
# **twitterRemoveWebhookFromMonitor**
> twitterRemoveWebhookFromMonitor(webhookId)

Remove webhook from monitor

Remove webhook configuration from a monitor. webhook_id is the monitor_id.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TwitterApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TwitterApi apiInstance = new TwitterApi(defaultClient);
    String webhookId = "webhookId_example"; // String | 
    try {
      apiInstance.twitterRemoveWebhookFromMonitor(webhookId);
    } catch (ApiException e) {
      System.err.println("Exception when calling TwitterApi#twitterRemoveWebhookFromMonitor");
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
| **webhookId** | **String**|  | |

### Return type

null (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **204** | Successful Response |  -  |
| **422** | Validation Error |  -  |

<a id="twitterSearchCommunities"></a>
# **twitterSearchCommunities**
> Object twitterSearchCommunities(query, cursor)

Search communities

Search for communities by query.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TwitterApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TwitterApi apiInstance = new TwitterApi(defaultClient);
    String query = "query_example"; // String | 
    String cursor = "cursor_example"; // String | 
    try {
      Object result = apiInstance.twitterSearchCommunities(query, cursor);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TwitterApi#twitterSearchCommunities");
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

<a id="twitterSearchListTweets"></a>
# **twitterSearchListTweets**
> Object twitterSearchListTweets(listId, query, cursor)

Search list tweets

Search tweets within a specific list.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TwitterApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TwitterApi apiInstance = new TwitterApi(defaultClient);
    String listId = "listId_example"; // String | 
    String query = "query_example"; // String | 
    String cursor = "cursor_example"; // String | 
    try {
      Object result = apiInstance.twitterSearchListTweets(listId, query, cursor);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TwitterApi#twitterSearchListTweets");
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
| **listId** | **String**|  | |
| **query** | **String**|  | |
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

<a id="twitterSearchPlaces"></a>
# **twitterSearchPlaces**
> Object twitterSearchPlaces(query, lat, _long)

Search places

Search for places by query or coordinates.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TwitterApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TwitterApi apiInstance = new TwitterApi(defaultClient);
    String query = "query_example"; // String | 
    BigDecimal lat = new BigDecimal(78); // BigDecimal | 
    BigDecimal _long = new BigDecimal(78); // BigDecimal | 
    try {
      Object result = apiInstance.twitterSearchPlaces(query, lat, _long);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TwitterApi#twitterSearchPlaces");
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
| **query** | **String**|  | [optional] |
| **lat** | **BigDecimal**|  | [optional] |
| **_long** | **BigDecimal**|  | [optional] |

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

<a id="twitterSearchUsers"></a>
# **twitterSearchUsers**
> Object twitterSearchUsers(query, cursor)

Search users

Search for users by query.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TwitterApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TwitterApi apiInstance = new TwitterApi(defaultClient);
    String query = "query_example"; // String | 
    String cursor = "cursor_example"; // String | 
    try {
      Object result = apiInstance.twitterSearchUsers(query, cursor);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TwitterApi#twitterSearchUsers");
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

<a id="twitterTestWebhookDelivery"></a>
# **twitterTestWebhookDelivery**
> WebhookTestResponse twitterTestWebhookDelivery(webhookTestRequest)

Test webhook delivery

Send a test payload to a monitor&#39;s webhook URL.  The test payload has type&#x3D;\&quot;test\&quot; instead of type&#x3D;\&quot;tweet\&quot;. Makes a synchronous HTTP POST and returns the delivery result.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TwitterApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TwitterApi apiInstance = new TwitterApi(defaultClient);
    WebhookTestRequest webhookTestRequest = new WebhookTestRequest(); // WebhookTestRequest | 
    try {
      WebhookTestResponse result = apiInstance.twitterTestWebhookDelivery(webhookTestRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TwitterApi#twitterTestWebhookDelivery");
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
| **webhookTestRequest** | [**WebhookTestRequest**](WebhookTestRequest.md)|  | |

### Return type

[**WebhookTestResponse**](WebhookTestResponse.md)

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

<a id="twitterTwitterScraperHealthCheck"></a>
# **twitterTwitterScraperHealthCheck**
> Object twitterTwitterScraperHealthCheck()

Twitter scraper health check

Check health of the Twitter scraper service.  Accepts &#x60;&#x60;HEAD&#x60;&#x60; so external uptime checkers (UptimeRobot uses HEAD by default for HTTP monitors) don&#39;t get a 405 Method Not Allowed.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TwitterApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TwitterApi apiInstance = new TwitterApi(defaultClient);
    try {
      Object result = apiInstance.twitterTwitterScraperHealthCheck();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TwitterApi#twitterTwitterScraperHealthCheck");
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

<a id="twitterTwitterScraperHealthCheckHead"></a>
# **twitterTwitterScraperHealthCheckHead**
> Object twitterTwitterScraperHealthCheckHead()

Twitter scraper health check

Check health of the Twitter scraper service.  Accepts &#x60;&#x60;HEAD&#x60;&#x60; so external uptime checkers (UptimeRobot uses HEAD by default for HTTP monitors) don&#39;t get a 405 Method Not Allowed.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TwitterApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TwitterApi apiInstance = new TwitterApi(defaultClient);
    try {
      Object result = apiInstance.twitterTwitterScraperHealthCheckHead();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TwitterApi#twitterTwitterScraperHealthCheckHead");
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

<a id="twitterUpdateFilterRule"></a>
# **twitterUpdateFilterRule**
> FilterRuleResponse twitterUpdateFilterRule(ruleId, filterRuleUpdate)

Update filter rule

Partially update a filter rule.  Setting status&#x3D;&#39;active&#39; on a paused rule performs a credit check.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TwitterApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TwitterApi apiInstance = new TwitterApi(defaultClient);
    String ruleId = "ruleId_example"; // String | 
    FilterRuleUpdate filterRuleUpdate = new FilterRuleUpdate(); // FilterRuleUpdate | 
    try {
      FilterRuleResponse result = apiInstance.twitterUpdateFilterRule(ruleId, filterRuleUpdate);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TwitterApi#twitterUpdateFilterRule");
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
| **ruleId** | **String**|  | |
| **filterRuleUpdate** | [**FilterRuleUpdate**](FilterRuleUpdate.md)|  | |

### Return type

[**FilterRuleResponse**](FilterRuleResponse.md)

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

<a id="twitterUpdateStreamMonitor"></a>
# **twitterUpdateStreamMonitor**
> StreamMonitorResponse twitterUpdateStreamMonitor(monitorId, streamMonitorUpdate)

Update stream monitor

Partially update a stream monitor.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TwitterApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TwitterApi apiInstance = new TwitterApi(defaultClient);
    String monitorId = "monitorId_example"; // String | 
    StreamMonitorUpdate streamMonitorUpdate = new StreamMonitorUpdate(); // StreamMonitorUpdate | 
    try {
      StreamMonitorResponse result = apiInstance.twitterUpdateStreamMonitor(monitorId, streamMonitorUpdate);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TwitterApi#twitterUpdateStreamMonitor");
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
| **monitorId** | **String**|  | |
| **streamMonitorUpdate** | [**StreamMonitorUpdate**](StreamMonitorUpdate.md)|  | |

### Return type

[**StreamMonitorResponse**](StreamMonitorResponse.md)

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

<a id="twitterValidateSearchQuery"></a>
# **twitterValidateSearchQuery**
> FilterRuleValidateResponse twitterValidateSearchQuery(filterRuleValidateRequest)

Validate search query

Validate a Twitter search query string.  Performs basic structural validation without making a live Twitter request. Returns valid&#x3D;True if the query passes syntax checks.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.TwitterApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    TwitterApi apiInstance = new TwitterApi(defaultClient);
    FilterRuleValidateRequest filterRuleValidateRequest = new FilterRuleValidateRequest(); // FilterRuleValidateRequest | 
    try {
      FilterRuleValidateResponse result = apiInstance.twitterValidateSearchQuery(filterRuleValidateRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TwitterApi#twitterValidateSearchQuery");
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
| **filterRuleValidateRequest** | [**FilterRuleValidateRequest**](FilterRuleValidateRequest.md)|  | |

### Return type

[**FilterRuleValidateResponse**](FilterRuleValidateResponse.md)

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

