# GooglePlayApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**googlePlayBrowseACategory**](GooglePlayApi.md#googlePlayBrowseACategory) | **GET** /v1/google-play/categories/{category_id} | Browse a category |
| [**googlePlayGetAppDetail**](GooglePlayApi.md#googlePlayGetAppDetail) | **GET** /v1/google-play/apps/{app_id} | Get app detail |
| [**googlePlayGetAppPermissions**](GooglePlayApi.md#googlePlayGetAppPermissions) | **GET** /v1/google-play/apps/{app_id}/permissions | Get app permissions |
| [**googlePlayGetAppReviews**](GooglePlayApi.md#googlePlayGetAppReviews) | **GET** /v1/google-play/apps/{app_id}/reviews | Get app reviews |
| [**googlePlayGetDeveloperApps**](GooglePlayApi.md#googlePlayGetDeveloperApps) | **GET** /v1/google-play/developers/{developer} | Get developer apps |
| [**googlePlayGetSimilarApps**](GooglePlayApi.md#googlePlayGetSimilarApps) | **GET** /v1/google-play/apps/{app_id}/similar | Get similar apps |
| [**googlePlayListCategories**](GooglePlayApi.md#googlePlayListCategories) | **GET** /v1/google-play/categories | List categories |
| [**googlePlayListMarkets**](GooglePlayApi.md#googlePlayListMarkets) | **GET** /v1/google-play/markets | List markets |
| [**googlePlaySearchApps**](GooglePlayApi.md#googlePlaySearchApps) | **GET** /v1/google-play/search | Search apps |
| [**googlePlayTopCharts**](GooglePlayApi.md#googlePlayTopCharts) | **GET** /v1/google-play/collections/{collection} | Top charts |


<a id="googlePlayBrowseACategory"></a>
# **googlePlayBrowseACategory**
> Object googlePlayBrowseACategory(categoryId, country, lang, num)

Browse a category

The top apps within a Play category.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.GooglePlayApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    GooglePlayApi apiInstance = new GooglePlayApi(defaultClient);
    String categoryId = "categoryId_example"; // String | Play category id, e.g. 'GAME_PUZZLE' or 'SOCIAL'
    String country = "US"; // String | Play storefront country (gl), ISO 3166-1 alpha-2, e.g. 'US'
    String lang = "en"; // String | Play content language (hl), e.g. 'en' or 'pt-BR'
    Integer num = 100; // Integer | Max apps; follows each rail's 'see more' continuation above the ~40-120 the page renders directly
    try {
      Object result = apiInstance.googlePlayBrowseACategory(categoryId, country, lang, num);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GooglePlayApi#googlePlayBrowseACategory");
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
| **categoryId** | **String**| Play category id, e.g. &#39;GAME_PUZZLE&#39; or &#39;SOCIAL&#39; | |
| **country** | **String**| Play storefront country (gl), ISO 3166-1 alpha-2, e.g. &#39;US&#39; | [optional] [default to US] |
| **lang** | **String**| Play content language (hl), e.g. &#39;en&#39; or &#39;pt-BR&#39; | [optional] [default to en] |
| **num** | **Integer**| Max apps; follows each rail&#39;s &#39;see more&#39; continuation above the ~40-120 the page renders directly | [optional] [default to 100] |

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

<a id="googlePlayGetAppDetail"></a>
# **googlePlayGetAppDetail**
> Object googlePlayGetAppDetail(appId, country, lang)

Get app detail

Full app detail: ratings histogram, installs, pricing, IAP, developer, screenshots, version metadata and what&#39;s-new.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.GooglePlayApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    GooglePlayApi apiInstance = new GooglePlayApi(defaultClient);
    String appId = "appId_example"; // String | Android package id, e.g. 'com.whatsapp'.
    String country = "US"; // String | Play storefront country (gl), ISO 3166-1 alpha-2, e.g. 'US'
    String lang = "en"; // String | Play content language (hl), e.g. 'en' or 'pt-BR'
    try {
      Object result = apiInstance.googlePlayGetAppDetail(appId, country, lang);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GooglePlayApi#googlePlayGetAppDetail");
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
| **appId** | **String**| Android package id, e.g. &#39;com.whatsapp&#39;. | |
| **country** | **String**| Play storefront country (gl), ISO 3166-1 alpha-2, e.g. &#39;US&#39; | [optional] [default to US] |
| **lang** | **String**| Play content language (hl), e.g. &#39;en&#39; or &#39;pt-BR&#39; | [optional] [default to en] |

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

<a id="googlePlayGetAppPermissions"></a>
# **googlePlayGetAppPermissions**
> Object googlePlayGetAppPermissions(appId, lang)

Get app permissions

The app&#39;s requested Android permissions, grouped.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.GooglePlayApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    GooglePlayApi apiInstance = new GooglePlayApi(defaultClient);
    String appId = "appId_example"; // String | Android package id, e.g. 'com.whatsapp'.
    String lang = "en"; // String | Play content language (hl), e.g. 'en' or 'pt-BR'
    try {
      Object result = apiInstance.googlePlayGetAppPermissions(appId, lang);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GooglePlayApi#googlePlayGetAppPermissions");
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
| **appId** | **String**| Android package id, e.g. &#39;com.whatsapp&#39;. | |
| **lang** | **String**| Play content language (hl), e.g. &#39;en&#39; or &#39;pt-BR&#39; | [optional] [default to en] |

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

<a id="googlePlayGetAppReviews"></a>
# **googlePlayGetAppReviews**
> Object googlePlayGetAppReviews(appId, country, lang, sort, count, pageToken)

Get app reviews

Paginated app reviews via the Play batchexecute RPC.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.GooglePlayApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    GooglePlayApi apiInstance = new GooglePlayApi(defaultClient);
    String appId = "appId_example"; // String | Android package id, e.g. 'com.whatsapp'.
    String country = "US"; // String | Play storefront country (gl), ISO 3166-1 alpha-2, e.g. 'US'
    String lang = "en"; // String | Play content language (hl), e.g. 'en' or 'pt-BR'
    String sort = "newest"; // String | newest | rating | helpfulness
    Integer count = 40; // Integer | 
    String pageToken = "pageToken_example"; // String | Pagination token
    try {
      Object result = apiInstance.googlePlayGetAppReviews(appId, country, lang, sort, count, pageToken);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GooglePlayApi#googlePlayGetAppReviews");
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
| **appId** | **String**| Android package id, e.g. &#39;com.whatsapp&#39;. | |
| **country** | **String**| Play storefront country (gl), ISO 3166-1 alpha-2, e.g. &#39;US&#39; | [optional] [default to US] |
| **lang** | **String**| Play content language (hl), e.g. &#39;en&#39; or &#39;pt-BR&#39; | [optional] [default to en] |
| **sort** | **String**| newest | rating | helpfulness | [optional] [default to newest] |
| **count** | **Integer**|  | [optional] [default to 40] |
| **pageToken** | **String**| Pagination token | [optional] |

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

<a id="googlePlayGetDeveloperApps"></a>
# **googlePlayGetDeveloperApps**
> Object googlePlayGetDeveloperApps(developer, country, lang, num)

Get developer apps

A developer&#39;s published apps.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.GooglePlayApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    GooglePlayApi apiInstance = new GooglePlayApi(defaultClient);
    String developer = "developer_example"; // String | Developer name or numeric id
    String country = "US"; // String | Play storefront country (gl), ISO 3166-1 alpha-2, e.g. 'US'
    String lang = "en"; // String | Play content language (hl), e.g. 'en' or 'pt-BR'
    Integer num = 100; // Integer | Max apps; follows rail continuations above the page's directly-rendered slice
    try {
      Object result = apiInstance.googlePlayGetDeveloperApps(developer, country, lang, num);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GooglePlayApi#googlePlayGetDeveloperApps");
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
| **developer** | **String**| Developer name or numeric id | |
| **country** | **String**| Play storefront country (gl), ISO 3166-1 alpha-2, e.g. &#39;US&#39; | [optional] [default to US] |
| **lang** | **String**| Play content language (hl), e.g. &#39;en&#39; or &#39;pt-BR&#39; | [optional] [default to en] |
| **num** | **Integer**| Max apps; follows rail continuations above the page&#39;s directly-rendered slice | [optional] [default to 100] |

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

<a id="googlePlayGetSimilarApps"></a>
# **googlePlayGetSimilarApps**
> Object googlePlayGetSimilarApps(appId, country, lang)

Get similar apps

Apps Google Play lists as similar to this one.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.GooglePlayApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    GooglePlayApi apiInstance = new GooglePlayApi(defaultClient);
    String appId = "appId_example"; // String | Android package id, e.g. 'com.whatsapp'.
    String country = "US"; // String | Play storefront country (gl), ISO 3166-1 alpha-2, e.g. 'US'
    String lang = "en"; // String | Play content language (hl), e.g. 'en' or 'pt-BR'
    try {
      Object result = apiInstance.googlePlayGetSimilarApps(appId, country, lang);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GooglePlayApi#googlePlayGetSimilarApps");
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
| **appId** | **String**| Android package id, e.g. &#39;com.whatsapp&#39;. | |
| **country** | **String**| Play storefront country (gl), ISO 3166-1 alpha-2, e.g. &#39;US&#39; | [optional] [default to US] |
| **lang** | **String**| Play content language (hl), e.g. &#39;en&#39; or &#39;pt-BR&#39; | [optional] [default to en] |

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

<a id="googlePlayListCategories"></a>
# **googlePlayListCategories**
> Object googlePlayListCategories()

List categories

The Google Play app/game category ids.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.GooglePlayApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    GooglePlayApi apiInstance = new GooglePlayApi(defaultClient);
    try {
      Object result = apiInstance.googlePlayListCategories();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GooglePlayApi#googlePlayListCategories");
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

<a id="googlePlayListMarkets"></a>
# **googlePlayListMarkets**
> Object googlePlayListMarkets()

List markets

Supported Google Play store countries and languages.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.GooglePlayApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    GooglePlayApi apiInstance = new GooglePlayApi(defaultClient);
    try {
      Object result = apiInstance.googlePlayListMarkets();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GooglePlayApi#googlePlayListMarkets");
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

<a id="googlePlaySearchApps"></a>
# **googlePlaySearchApps**
> Object googlePlaySearchApps(query, country, lang, price)

Search apps

Search Google Play for apps and games (the ~30 server-rendered results; Play exposes no page parameter).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.GooglePlayApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    GooglePlayApi apiInstance = new GooglePlayApi(defaultClient);
    String query = "query_example"; // String | Search keywords, e.g. 'puzzle'
    String country = "US"; // String | Play storefront country (gl), ISO 3166-1 alpha-2, e.g. 'US'
    String lang = "en"; // String | Play content language (hl), e.g. 'en' or 'pt-BR'
    String price = "price_example"; // String | free | paid | all
    try {
      Object result = apiInstance.googlePlaySearchApps(query, country, lang, price);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GooglePlayApi#googlePlaySearchApps");
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
| **query** | **String**| Search keywords, e.g. &#39;puzzle&#39; | |
| **country** | **String**| Play storefront country (gl), ISO 3166-1 alpha-2, e.g. &#39;US&#39; | [optional] [default to US] |
| **lang** | **String**| Play content language (hl), e.g. &#39;en&#39; or &#39;pt-BR&#39; | [optional] [default to en] |
| **price** | **String**| free | paid | all | [optional] |

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

<a id="googlePlayTopCharts"></a>
# **googlePlayTopCharts**
> Object googlePlayTopCharts(collection, category, country, lang)

Top charts

Top charts for a collection, optionally scoped to a category.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.GooglePlayApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    GooglePlayApi apiInstance = new GooglePlayApi(defaultClient);
    String collection = "collection_example"; // String | topselling_free | topselling_paid | topgrossing
    String category = "APPLICATION"; // String | Play category, e.g. 'GAME'
    String country = "US"; // String | Play storefront country (gl), ISO 3166-1 alpha-2, e.g. 'US'
    String lang = "en"; // String | Play content language (hl), e.g. 'en' or 'pt-BR'
    try {
      Object result = apiInstance.googlePlayTopCharts(collection, category, country, lang);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GooglePlayApi#googlePlayTopCharts");
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
| **collection** | **String**| topselling_free | topselling_paid | topgrossing | |
| **category** | **String**| Play category, e.g. &#39;GAME&#39; | [optional] [default to APPLICATION] |
| **country** | **String**| Play storefront country (gl), ISO 3166-1 alpha-2, e.g. &#39;US&#39; | [optional] [default to US] |
| **lang** | **String**| Play content language (hl), e.g. &#39;en&#39; or &#39;pt-BR&#39; | [optional] [default to en] |

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

