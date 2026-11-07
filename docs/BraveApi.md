# BraveApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**braveAutocomplete**](BraveApi.md#braveAutocomplete) | **GET** /v1/brave/autocomplete | Autocomplete |
| [**braveImageSearch**](BraveApi.md#braveImageSearch) | **GET** /v1/brave/images | Image search |
| [**braveListSupportedLocales**](BraveApi.md#braveListSupportedLocales) | **GET** /v1/brave/locales | List supported locales |
| [**braveNewsSearch**](BraveApi.md#braveNewsSearch) | **GET** /v1/brave/news | News search |
| [**braveVideoSearch**](BraveApi.md#braveVideoSearch) | **GET** /v1/brave/videos | Video search |
| [**braveWebSearch**](BraveApi.md#braveWebSearch) | **GET** /v1/brave/search | Web search |


<a id="braveAutocomplete"></a>
# **braveAutocomplete**
> BraveAutocompleteResponse braveAutocomplete(query, country)

Autocomplete

Native search-box suggestions with entity descriptions and images. Two credits.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.BraveApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    BraveApi apiInstance = new BraveApi(defaultClient);
    String query = "query_example"; // String | 
    String country = "us"; // String | 
    try {
      BraveAutocompleteResponse result = apiInstance.braveAutocomplete(query, country);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BraveApi#braveAutocomplete");
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
| **country** | **String**|  | [optional] [default to us] [enum: us, all, ar, au, at, be, br, ca, cl, cn, dk, fi, fr, de, gr, hk, in, id, it, jp, kr, my, mx, nl, nz, no, ph, pl, pt, ru, sa, sg, za, es, se, ch, tw, tr, gb] |

### Return type

[**BraveAutocompleteResponse**](BraveAutocompleteResponse.md)

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

<a id="braveImageSearch"></a>
# **braveImageSearch**
> BraveResponse braveImageSearch(query, country, uiLanguage, safeSearch, count)

Image search

Native image batch with original URLs, source pages, thumbnails and dimensions.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.BraveApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    BraveApi apiInstance = new BraveApi(defaultClient);
    String query = "query_example"; // String | Native Brave search query
    String country = "us"; // String | Native result region; see /locales
    String uiLanguage = "en-us"; // String | UI labels/date language; does not restrict result language
    String safeSearch = "off"; // String | 
    Integer count = 50; // Integer | Slice the initial native image batch
    try {
      BraveResponse result = apiInstance.braveImageSearch(query, country, uiLanguage, safeSearch, count);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BraveApi#braveImageSearch");
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
| **query** | **String**| Native Brave search query | |
| **country** | **String**| Native result region; see /locales | [optional] [default to us] [enum: us, all, ar, au, at, be, br, ca, cl, cn, dk, fi, fr, de, gr, hk, in, id, it, jp, kr, my, mx, nl, nz, no, ph, pl, pt, ru, sa, sg, za, es, se, ch, tw, tr, gb] |
| **uiLanguage** | **String**| UI labels/date language; does not restrict result language | [optional] [default to en-us] [enum: en-us, az, id, ms, br, ca, cs, cy, da, de-de, et, en-ca, en-in, en-gb, es, eu, fr-ca, fr-fr, gl, hr, it, sw-ke, lv, lt, hu, nl, nb, pl, pt-br, ro, sq-al, sk, sl, sr-latn, fi-fi, sv, vi, tr, el, bg, ru, sr, uk, ka, th, ko, zh, zh-tw, ja-jp] |
| **safeSearch** | **String**|  | [optional] [default to moderate] [enum: off, moderate, strict] |
| **count** | **Integer**| Slice the initial native image batch | [optional] [default to 50] |

### Return type

[**BraveResponse**](BraveResponse.md)

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

<a id="braveListSupportedLocales"></a>
# **braveListSupportedLocales**
> BraveLocalesResponse braveListSupportedLocales()

List supported locales

Native country and UI-language choices. Free; result language is a separate preference.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.BraveApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    BraveApi apiInstance = new BraveApi(defaultClient);
    try {
      BraveLocalesResponse result = apiInstance.braveListSupportedLocales();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BraveApi#braveListSupportedLocales");
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

[**BraveLocalesResponse**](BraveLocalesResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |

<a id="braveNewsSearch"></a>
# **braveNewsSearch**
> BraveResponse braveNewsSearch(query, country, uiLanguage, safeSearch, count)

News search

Native news batch; relative source dates stay display strings.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.BraveApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    BraveApi apiInstance = new BraveApi(defaultClient);
    String query = "query_example"; // String | Native Brave search query
    String country = "us"; // String | Native result region; see /locales
    String uiLanguage = "en-us"; // String | UI labels/date language; does not restrict result language
    String safeSearch = "off"; // String | 
    Integer count = 35; // Integer | Slice the initial native news batch
    try {
      BraveResponse result = apiInstance.braveNewsSearch(query, country, uiLanguage, safeSearch, count);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BraveApi#braveNewsSearch");
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
| **query** | **String**| Native Brave search query | |
| **country** | **String**| Native result region; see /locales | [optional] [default to us] [enum: us, all, ar, au, at, be, br, ca, cl, cn, dk, fi, fr, de, gr, hk, in, id, it, jp, kr, my, mx, nl, nz, no, ph, pl, pt, ru, sa, sg, za, es, se, ch, tw, tr, gb] |
| **uiLanguage** | **String**| UI labels/date language; does not restrict result language | [optional] [default to en-us] [enum: en-us, az, id, ms, br, ca, cs, cy, da, de-de, et, en-ca, en-in, en-gb, es, eu, fr-ca, fr-fr, gl, hr, it, sw-ke, lv, lt, hu, nl, nb, pl, pt-br, ro, sq-al, sk, sl, sr-latn, fi-fi, sv, vi, tr, el, bg, ru, sr, uk, ka, th, ko, zh, zh-tw, ja-jp] |
| **safeSearch** | **String**|  | [optional] [default to moderate] [enum: off, moderate, strict] |
| **count** | **Integer**| Slice the initial native news batch | [optional] [default to 35] |

### Return type

[**BraveResponse**](BraveResponse.md)

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

<a id="braveVideoSearch"></a>
# **braveVideoSearch**
> BravePagedResponse braveVideoSearch(query, country, uiLanguage, safeSearch, page, count)

Video search

Native video results with duration, creator, publisher and verified page ordinals.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.BraveApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    BraveApi apiInstance = new BraveApi(defaultClient);
    String query = "query_example"; // String | Native Brave search query
    String country = "us"; // String | Native result region; see /locales
    String uiLanguage = "en-us"; // String | UI labels/date language; does not restrict result language
    String safeSearch = "off"; // String | 
    Integer page = 1; // Integer | 1-based native page ordinal
    Integer count = 50; // Integer | 
    try {
      BravePagedResponse result = apiInstance.braveVideoSearch(query, country, uiLanguage, safeSearch, page, count);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BraveApi#braveVideoSearch");
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
| **query** | **String**| Native Brave search query | |
| **country** | **String**| Native result region; see /locales | [optional] [default to us] [enum: us, all, ar, au, at, be, br, ca, cl, cn, dk, fi, fr, de, gr, hk, in, id, it, jp, kr, my, mx, nl, nz, no, ph, pl, pt, ru, sa, sg, za, es, se, ch, tw, tr, gb] |
| **uiLanguage** | **String**| UI labels/date language; does not restrict result language | [optional] [default to en-us] [enum: en-us, az, id, ms, br, ca, cs, cy, da, de-de, et, en-ca, en-in, en-gb, es, eu, fr-ca, fr-fr, gl, hr, it, sw-ke, lv, lt, hu, nl, nb, pl, pt-br, ro, sq-al, sk, sl, sr-latn, fi-fi, sv, vi, tr, el, bg, ru, sr, uk, ka, th, ko, zh, zh-tw, ja-jp] |
| **safeSearch** | **String**|  | [optional] [default to moderate] [enum: off, moderate, strict] |
| **page** | **Integer**| 1-based native page ordinal | [optional] [default to 1] |
| **count** | **Integer**|  | [optional] [default to 50] |

### Return type

[**BravePagedResponse**](BravePagedResponse.md)

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

<a id="braveWebSearch"></a>
# **braveWebSearch**
> BraveSearchResponse braveWebSearch(query, country, uiLanguage, safeSearch, page, count, freshness, spellcheck)

Web search

Native Brave organic results, rich source blocks and page metadata. Seven credits.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.BraveApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    BraveApi apiInstance = new BraveApi(defaultClient);
    String query = "query_example"; // String | Native Brave search query
    String country = "us"; // String | Native result region; see /locales
    String uiLanguage = "en-us"; // String | UI labels/date language; does not restrict result language
    String safeSearch = "off"; // String | 
    Integer page = 1; // Integer | 1-based native page ordinal
    Integer count = 20; // Integer | Slice one native page; does not change native page boundaries
    String freshness = "any"; // String | 
    Boolean spellcheck = false; // Boolean | Allow native spelling correction
    try {
      BraveSearchResponse result = apiInstance.braveWebSearch(query, country, uiLanguage, safeSearch, page, count, freshness, spellcheck);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BraveApi#braveWebSearch");
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
| **query** | **String**| Native Brave search query | |
| **country** | **String**| Native result region; see /locales | [optional] [default to us] [enum: us, all, ar, au, at, be, br, ca, cl, cn, dk, fi, fr, de, gr, hk, in, id, it, jp, kr, my, mx, nl, nz, no, ph, pl, pt, ru, sa, sg, za, es, se, ch, tw, tr, gb] |
| **uiLanguage** | **String**| UI labels/date language; does not restrict result language | [optional] [default to en-us] [enum: en-us, az, id, ms, br, ca, cs, cy, da, de-de, et, en-ca, en-in, en-gb, es, eu, fr-ca, fr-fr, gl, hr, it, sw-ke, lv, lt, hu, nl, nb, pl, pt-br, ro, sq-al, sk, sl, sr-latn, fi-fi, sv, vi, tr, el, bg, ru, sr, uk, ka, th, ko, zh, zh-tw, ja-jp] |
| **safeSearch** | **String**|  | [optional] [default to moderate] [enum: off, moderate, strict] |
| **page** | **Integer**| 1-based native page ordinal | [optional] [default to 1] |
| **count** | **Integer**| Slice one native page; does not change native page boundaries | [optional] [default to 20] |
| **freshness** | **String**|  | [optional] [default to any] [enum: any, day, week, month, year] |
| **spellcheck** | **Boolean**| Allow native spelling correction | [optional] [default to false] |

### Return type

[**BraveSearchResponse**](BraveSearchResponse.md)

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

