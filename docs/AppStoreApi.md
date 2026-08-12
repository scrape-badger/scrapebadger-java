# AppStoreApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**appStoreGetAppDetail**](AppStoreApi.md#appStoreGetAppDetail) | **GET** /v1/app-store/apps/{app_id} | Get app detail |
| [**appStoreGetAppReviews**](AppStoreApi.md#appStoreGetAppReviews) | **GET** /v1/app-store/apps/{app_id}/reviews | Get app reviews |
| [**appStoreGetDeveloperApps**](AppStoreApi.md#appStoreGetDeveloperApps) | **GET** /v1/app-store/developers/{artist_id} | Get developer apps |
| [**appStoreListGenres**](AppStoreApi.md#appStoreListGenres) | **GET** /v1/app-store/genres | List genres |
| [**appStoreListMarkets**](AppStoreApi.md#appStoreListMarkets) | **GET** /v1/app-store/markets | List markets |
| [**appStoreSearchApps**](AppStoreApi.md#appStoreSearchApps) | **GET** /v1/app-store/search | Search apps |
| [**appStoreTopCharts**](AppStoreApi.md#appStoreTopCharts) | **GET** /v1/app-store/charts | Top charts |


<a id="appStoreGetAppDetail"></a>
# **appStoreGetAppDetail**
> Object appStoreGetAppDetail(appId, country, lang, includeExtras)

Get app detail

App detail: bundle id, version, pricing, ratings, genres, min OS, size, languages, screenshots, in-app purchases and version history.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.AppStoreApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    AppStoreApi apiInstance = new AppStoreApi(defaultClient);
    String appId = "appId_example"; // String | Numeric trackId (e.g. '310633997') or bundle id (e.g. 'net.whatsapp.WhatsApp').
    String country = "us"; // String | 
    String lang = "lang_example"; // String | Result language, e.g. 'en_us'
    Boolean includeExtras = true; // Boolean | Fetch the storefront page for rating histogram, IAP list, full-res screenshots and App Privacy. Set false to skip the 2nd fetch.
    try {
      Object result = apiInstance.appStoreGetAppDetail(appId, country, lang, includeExtras);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AppStoreApi#appStoreGetAppDetail");
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
| **appId** | **String**| Numeric trackId (e.g. &#39;310633997&#39;) or bundle id (e.g. &#39;net.whatsapp.WhatsApp&#39;). | |
| **country** | **String**|  | [optional] [default to us] |
| **lang** | **String**| Result language, e.g. &#39;en_us&#39; | [optional] |
| **includeExtras** | **Boolean**| Fetch the storefront page for rating histogram, IAP list, full-res screenshots and App Privacy. Set false to skip the 2nd fetch. | [optional] [default to true] |

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

<a id="appStoreGetAppReviews"></a>
# **appStoreGetAppReviews**
> Object appStoreGetAppReviews(appId, country, page, sort)

Get app reviews

Paginated customer reviews (50 per page, up to 10 pages).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.AppStoreApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    AppStoreApi apiInstance = new AppStoreApi(defaultClient);
    String appId = "appId_example"; // String | Numeric trackId, e.g. '310633997'
    String country = "us"; // String | 
    Integer page = 1; // Integer | Apple caps reviews at 10 pages
    String sort = "mostRecent"; // String | mostRecent | mostHelpful
    try {
      Object result = apiInstance.appStoreGetAppReviews(appId, country, page, sort);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AppStoreApi#appStoreGetAppReviews");
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
| **appId** | **String**| Numeric trackId, e.g. &#39;310633997&#39; | |
| **country** | **String**|  | [optional] [default to us] |
| **page** | **Integer**| Apple caps reviews at 10 pages | [optional] [default to 1] |
| **sort** | **String**| mostRecent | mostHelpful | [optional] [default to mostRecent] |

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

<a id="appStoreGetDeveloperApps"></a>
# **appStoreGetDeveloperApps**
> Object appStoreGetDeveloperApps(artistId, country)

Get developer apps

Developer info and their published apps.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.AppStoreApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    AppStoreApi apiInstance = new AppStoreApi(defaultClient);
    String artistId = "artistId_example"; // String | Numeric artistId (developer id)
    String country = "us"; // String | 
    try {
      Object result = apiInstance.appStoreGetDeveloperApps(artistId, country);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AppStoreApi#appStoreGetDeveloperApps");
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
| **artistId** | **String**| Numeric artistId (developer id) | |
| **country** | **String**|  | [optional] [default to us] |

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

<a id="appStoreListGenres"></a>
# **appStoreListGenres**
> Object appStoreListGenres()

List genres

The Apple App Store genre/category ids.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.AppStoreApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    AppStoreApi apiInstance = new AppStoreApi(defaultClient);
    try {
      Object result = apiInstance.appStoreListGenres();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AppStoreApi#appStoreListGenres");
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

<a id="appStoreListMarkets"></a>
# **appStoreListMarkets**
> Object appStoreListMarkets()

List markets

Supported App Store country codes.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.AppStoreApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    AppStoreApi apiInstance = new AppStoreApi(defaultClient);
    try {
      Object result = apiInstance.appStoreListMarkets();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AppStoreApi#appStoreListMarkets");
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

<a id="appStoreSearchApps"></a>
# **appStoreSearchApps**
> Object appStoreSearchApps(query, country, entity, limit, offset, lang)

Search apps

Search the Apple App Store.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.AppStoreApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    AppStoreApi apiInstance = new AppStoreApi(defaultClient);
    String query = "query_example"; // String | Search term, e.g. 'chat'
    String country = "us"; // String | App Store country code
    String entity = "software"; // String | software | iPadSoftware | macSoftware
    Integer limit = 25; // Integer | 
    Integer offset = 0; // Integer | 
    String lang = "lang_example"; // String | Language, e.g. 'en_us'
    try {
      Object result = apiInstance.appStoreSearchApps(query, country, entity, limit, offset, lang);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AppStoreApi#appStoreSearchApps");
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
| **query** | **String**| Search term, e.g. &#39;chat&#39; | |
| **country** | **String**| App Store country code | [optional] [default to us] |
| **entity** | **String**| software | iPadSoftware | macSoftware | [optional] [default to software] |
| **limit** | **Integer**|  | [optional] [default to 25] |
| **offset** | **Integer**|  | [optional] [default to 0] |
| **lang** | **String**| Language, e.g. &#39;en_us&#39; | [optional] |

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

<a id="appStoreTopCharts"></a>
# **appStoreTopCharts**
> Object appStoreTopCharts(country, type, genre, limit, entity)

Top charts

Top charts, optionally scoped to a genre.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.AppStoreApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    AppStoreApi apiInstance = new AppStoreApi(defaultClient);
    String country = "us"; // String | 
    String type = "top-free"; // String | top-free | top-paid | top-grossing
    Integer genre = 56; // Integer | Apple genre id (optional), e.g. 6014
    Integer limit = 50; // Integer | 
    String entity = "apps"; // String | apps (iPhone) | ipad
    try {
      Object result = apiInstance.appStoreTopCharts(country, type, genre, limit, entity);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AppStoreApi#appStoreTopCharts");
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
| **country** | **String**|  | [optional] [default to us] |
| **type** | **String**| top-free | top-paid | top-grossing | [optional] [default to top-free] |
| **genre** | **Integer**| Apple genre id (optional), e.g. 6014 | [optional] |
| **limit** | **Integer**|  | [optional] [default to 50] |
| **entity** | **String**| apps (iPhone) | ipad | [optional] [default to apps] |

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

