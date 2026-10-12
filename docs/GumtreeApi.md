# GumtreeApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**gumtreeGetListing**](GumtreeApi.md#gumtreeGetListing) | **GET** /v1/gumtree/listings/{listing_id} | Get listing |
| [**gumtreeGetSearchFilters**](GumtreeApi.md#gumtreeGetSearchFilters) | **GET** /v1/gumtree/search/filters | Get search filters |
| [**gumtreeGetSellerListings**](GumtreeApi.md#gumtreeGetSellerListings) | **GET** /v1/gumtree/listings/{listing_id}/seller-listings | Get seller listings |
| [**gumtreeGumtreeScraperHealthCheck**](GumtreeApi.md#gumtreeGumtreeScraperHealthCheck) | **GET** /v1/gumtree/health | Gumtree scraper health check |
| [**gumtreeGumtreeScraperHealthCheckHead**](GumtreeApi.md#gumtreeGumtreeScraperHealthCheckHead) | **HEAD** /v1/gumtree/health | Gumtree scraper health check |
| [**gumtreeListCategories**](GumtreeApi.md#gumtreeListCategories) | **GET** /v1/gumtree/categories | List categories |
| [**gumtreeListLocations**](GumtreeApi.md#gumtreeListLocations) | **GET** /v1/gumtree/locations | List locations |
| [**gumtreeListMarkets**](GumtreeApi.md#gumtreeListMarkets) | **GET** /v1/gumtree/markets | List markets |
| [**gumtreeLocationSuggestions**](GumtreeApi.md#gumtreeLocationSuggestions) | **GET** /v1/gumtree/locations/autocomplete | Location suggestions |
| [**gumtreeSearchListings**](GumtreeApi.md#gumtreeSearchListings) | **GET** /v1/gumtree/search | Search listings |
| [**gumtreeSearchSuggestions**](GumtreeApi.md#gumtreeSearchSuggestions) | **GET** /v1/gumtree/autocomplete | Search suggestions |


<a id="gumtreeGetListing"></a>
# **gumtreeGetListing**
> Object gumtreeGetListing(listingId, market)

Get listing

Full listing — description, attributes, images, seller, similar listings.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.GumtreeApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    GumtreeApi apiInstance = new GumtreeApi(defaultClient);
    String listingId = "listingId_example"; // String | Gumtree listing id — the number at the end of the listing URL (uk/au: ~10 digits; za: the full 26-digit ad id, not the short one)
    String market = "uk"; // String | Which Gumtree: 'uk' (gumtree.com, GBP), 'au' (gumtree.com.au, AUD) or 'za' (gumtree.co.za, ZAR). Separate sites — ids from one market mean nothing in another.
    try {
      Object result = apiInstance.gumtreeGetListing(listingId, market);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GumtreeApi#gumtreeGetListing");
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
| **listingId** | **String**| Gumtree listing id — the number at the end of the listing URL (uk/au: ~10 digits; za: the full 26-digit ad id, not the short one) | |
| **market** | **String**| Which Gumtree: &#39;uk&#39; (gumtree.com, GBP), &#39;au&#39; (gumtree.com.au, AUD) or &#39;za&#39; (gumtree.co.za, ZAR). Separate sites — ids from one market mean nothing in another. | [optional] [default to uk] [enum: uk, au, za] |

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

<a id="gumtreeGetSearchFilters"></a>
# **gumtreeGetSearchFilters**
> Object gumtreeGetSearchFilters(category, location, query, filters, market)

Get search filters

Filters, sort orders and radius options for a category, with live counts.  Feed a &#x60;key&#x60; and a &#x60;value&#x60; back into &#x60;/search&#x60; as &#x60;filters&#x3D;key:value&#x60;. au bills 2x (browser render).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.GumtreeApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    GumtreeApi apiInstance = new GumtreeApi(defaultClient);
    String category = "all"; // String | uk: category slug, e.g. 'cars', 'for-sale', 'property-to-rent', 'jobs', 'bicycles'. au/za: numeric category id, e.g. '18320' (au cars) or '9077' (za cars). Use /categories to browse the tree. Default 'all'.
    String location = "location_example"; // String | uk: location slug ('london'), town name or UK postcode ('SW1A 1AA'). au/za: numeric location id, e.g. '3003435' (au Sydney) or '3100003' (za Gauteng). Use /locations/autocomplete to resolve one. Default: the whole country.
    String query = "query_example"; // String | Optional keywords to scope the counts
    String filters = "filters_example"; // String | za only: filters already applied (e.g. 'ma:toyota' to list Toyota models)
    String market = "uk"; // String | Which Gumtree: 'uk' (gumtree.com, GBP), 'au' (gumtree.com.au, AUD) or 'za' (gumtree.co.za, ZAR). Separate sites — ids from one market mean nothing in another.
    try {
      Object result = apiInstance.gumtreeGetSearchFilters(category, location, query, filters, market);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GumtreeApi#gumtreeGetSearchFilters");
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
| **category** | **String**| uk: category slug, e.g. &#39;cars&#39;, &#39;for-sale&#39;, &#39;property-to-rent&#39;, &#39;jobs&#39;, &#39;bicycles&#39;. au/za: numeric category id, e.g. &#39;18320&#39; (au cars) or &#39;9077&#39; (za cars). Use /categories to browse the tree. Default &#39;all&#39;. | [optional] [default to all] |
| **location** | **String**| uk: location slug (&#39;london&#39;), town name or UK postcode (&#39;SW1A 1AA&#39;). au/za: numeric location id, e.g. &#39;3003435&#39; (au Sydney) or &#39;3100003&#39; (za Gauteng). Use /locations/autocomplete to resolve one. Default: the whole country. | [optional] |
| **query** | **String**| Optional keywords to scope the counts | [optional] |
| **filters** | **String**| za only: filters already applied (e.g. &#39;ma:toyota&#39; to list Toyota models) | [optional] |
| **market** | **String**| Which Gumtree: &#39;uk&#39; (gumtree.com, GBP), &#39;au&#39; (gumtree.com.au, AUD) or &#39;za&#39; (gumtree.co.za, ZAR). Separate sites — ids from one market mean nothing in another. | [optional] [default to uk] [enum: uk, au, za] |

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

<a id="gumtreeGetSellerListings"></a>
# **gumtreeGetSellerListings**
> Object gumtreeGetSellerListings(listingId, page, market)

Get seller listings

Every live listing by the seller of the given listing.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.GumtreeApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    GumtreeApi apiInstance = new GumtreeApi(defaultClient);
    String listingId = "listingId_example"; // String | Gumtree listing id — the number at the end of the listing URL (uk/au: ~10 digits; za: the full 26-digit ad id, not the short one)
    Integer page = 1; // Integer | 
    String market = "uk"; // String | Which Gumtree: 'uk' (gumtree.com, GBP), 'au' (gumtree.com.au, AUD) or 'za' (gumtree.co.za, ZAR). Separate sites — ids from one market mean nothing in another.
    try {
      Object result = apiInstance.gumtreeGetSellerListings(listingId, page, market);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GumtreeApi#gumtreeGetSellerListings");
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
| **listingId** | **String**| Gumtree listing id — the number at the end of the listing URL (uk/au: ~10 digits; za: the full 26-digit ad id, not the short one) | |
| **page** | **Integer**|  | [optional] [default to 1] |
| **market** | **String**| Which Gumtree: &#39;uk&#39; (gumtree.com, GBP), &#39;au&#39; (gumtree.com.au, AUD) or &#39;za&#39; (gumtree.co.za, ZAR). Separate sites — ids from one market mean nothing in another. | [optional] [default to uk] [enum: uk, au, za] |

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

<a id="gumtreeGumtreeScraperHealthCheck"></a>
# **gumtreeGumtreeScraperHealthCheck**
> Object gumtreeGumtreeScraperHealthCheck()

Gumtree scraper health check

Check health of the Gumtree scraper service (accepts HEAD for UptimeRobot).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.GumtreeApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    GumtreeApi apiInstance = new GumtreeApi(defaultClient);
    try {
      Object result = apiInstance.gumtreeGumtreeScraperHealthCheck();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GumtreeApi#gumtreeGumtreeScraperHealthCheck");
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

<a id="gumtreeGumtreeScraperHealthCheckHead"></a>
# **gumtreeGumtreeScraperHealthCheckHead**
> Object gumtreeGumtreeScraperHealthCheckHead()

Gumtree scraper health check

Check health of the Gumtree scraper service (accepts HEAD for UptimeRobot).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.GumtreeApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    GumtreeApi apiInstance = new GumtreeApi(defaultClient);
    try {
      Object result = apiInstance.gumtreeGumtreeScraperHealthCheckHead();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GumtreeApi#gumtreeGumtreeScraperHealthCheckHead");
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

<a id="gumtreeListCategories"></a>
# **gumtreeListCategories**
> Object gumtreeListCategories(parentId, market)

List categories

Browse Gumtree&#39;s category tree.  A node&#39;s &#x60;slug&#x60; (uk) or &#x60;id&#x60; (au/za) is the &#x60;/search&#x60; category.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.GumtreeApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    GumtreeApi apiInstance = new GumtreeApi(defaultClient);
    Integer parentId = 56; // Integer | Category id to list the children of (default: all)
    String market = "uk"; // String | Which Gumtree: 'uk' (gumtree.com, GBP), 'au' (gumtree.com.au, AUD) or 'za' (gumtree.co.za, ZAR). Separate sites — ids from one market mean nothing in another.
    try {
      Object result = apiInstance.gumtreeListCategories(parentId, market);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GumtreeApi#gumtreeListCategories");
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
| **parentId** | **Integer**| Category id to list the children of (default: all) | [optional] |
| **market** | **String**| Which Gumtree: &#39;uk&#39; (gumtree.com, GBP), &#39;au&#39; (gumtree.com.au, AUD) or &#39;za&#39; (gumtree.co.za, ZAR). Separate sites — ids from one market mean nothing in another. | [optional] [default to uk] [enum: uk, au, za] |

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

<a id="gumtreeListLocations"></a>
# **gumtreeListLocations**
> Object gumtreeListLocations(parentId, market)

List locations

Browse Gumtree&#39;s location tree.  uk: UK -&gt; nations -&gt; counties -&gt; towns. au: states -&gt; regions -&gt; areas, each with its live ad count (browser render, bills 5x). za: provinces -&gt; towns.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.GumtreeApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    GumtreeApi apiInstance = new GumtreeApi(defaultClient);
    Integer parentId = 56; // Integer | Location id to list the children of (default: the whole country)
    String market = "uk"; // String | Which Gumtree: 'uk' (gumtree.com, GBP), 'au' (gumtree.com.au, AUD) or 'za' (gumtree.co.za, ZAR). Separate sites — ids from one market mean nothing in another.
    try {
      Object result = apiInstance.gumtreeListLocations(parentId, market);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GumtreeApi#gumtreeListLocations");
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
| **parentId** | **Integer**| Location id to list the children of (default: the whole country) | [optional] |
| **market** | **String**| Which Gumtree: &#39;uk&#39; (gumtree.com, GBP), &#39;au&#39; (gumtree.com.au, AUD) or &#39;za&#39; (gumtree.co.za, ZAR). Separate sites — ids from one market mean nothing in another. | [optional] [default to uk] [enum: uk, au, za] |

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

<a id="gumtreeListMarkets"></a>
# **gumtreeListMarkets**
> Object gumtreeListMarkets()

List markets

The Gumtree sites this API covers (uk, au, za) with currency and id formats.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.GumtreeApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    GumtreeApi apiInstance = new GumtreeApi(defaultClient);
    try {
      Object result = apiInstance.gumtreeListMarkets();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GumtreeApi#gumtreeListMarkets");
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

<a id="gumtreeLocationSuggestions"></a>
# **gumtreeLocationSuggestions**
> Object gumtreeLocationSuggestions(query, market)

Location suggestions

Resolve a place name or postcode to Gumtree location ids (uk: with coordinates).  The &#x60;id&#x60; (au/za) or &#x60;name&#x60; (uk) is what &#x60;/search&#x60; takes as &#x60;location&#x60;.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.GumtreeApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    GumtreeApi apiInstance = new GumtreeApi(defaultClient);
    String query = "query_example"; // String | Town, area or postcode prefix, e.g. 'manch' or 'SW1A'
    String market = "uk"; // String | Which Gumtree: 'uk' (gumtree.com, GBP), 'au' (gumtree.com.au, AUD) or 'za' (gumtree.co.za, ZAR). Separate sites — ids from one market mean nothing in another.
    try {
      Object result = apiInstance.gumtreeLocationSuggestions(query, market);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GumtreeApi#gumtreeLocationSuggestions");
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
| **query** | **String**| Town, area or postcode prefix, e.g. &#39;manch&#39; or &#39;SW1A&#39; | |
| **market** | **String**| Which Gumtree: &#39;uk&#39; (gumtree.com, GBP), &#39;au&#39; (gumtree.com.au, AUD) or &#39;za&#39; (gumtree.co.za, ZAR). Separate sites — ids from one market mean nothing in another. | [optional] [default to uk] [enum: uk, au, za] |

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

<a id="gumtreeSearchListings"></a>
# **gumtreeSearchListings**
> Object gumtreeSearchListings(query, category, location, distance, minPrice, maxPrice, sort, sellerType, urgentOnly, withPhotos, filters, page, market)

Search listings

Search Gumtree listings in the UK, Australia or South Africa.  Up to 50 pages. Page size: uk 25, au 24 (plus up to 6 featured top ads), za 20. An au search runs a real browser (~10-20 s) and bills 2x.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.GumtreeApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    GumtreeApi apiInstance = new GumtreeApi(defaultClient);
    String query = "query_example"; // String | Search keywords, e.g. 'mountain bike'
    String category = "all"; // String | uk: category slug, e.g. 'cars', 'for-sale', 'property-to-rent', 'jobs', 'bicycles'. au/za: numeric category id, e.g. '18320' (au cars) or '9077' (za cars). Use /categories to browse the tree. Default 'all'.
    String location = "location_example"; // String | uk: location slug ('london'), town name or UK postcode ('SW1A 1AA'). au/za: numeric location id, e.g. '3003435' (au Sydney) or '3100003' (za Gauteng). Use /locations/autocomplete to resolve one. Default: the whole country.
    BigDecimal distance = new BigDecimal(78); // BigDecimal | Radius around `location`: miles (uk) or km (au). Not offered by za.
    Integer minPrice = 56; // Integer | Minimum price in the market's currency (uk: needs a category, not 'all')
    Integer maxPrice = 56; // Integer | Maximum price in the market's currency (uk: needs a category, not 'all')
    String sort = "relevance"; // String | Result ordering (default relevance). 'distance' needs uk, or au with a location.
    String sellerType = "private"; // String | uk/za: 'trade' covers dealers, agencies and recruiters. au: not supported — use a category filter such as 'cars.forsaleby_s:ownr'.
    Boolean urgentOnly = false; // Boolean | uk only: only ads marked urgent
    Boolean withPhotos = false; // Boolean | uk only: only ads with photos
    String filters = "filters_example"; // String | Category-specific filters as comma-separated key:value pairs, e.g. 'vehicle_make:bmw,vehicle_fuel_type:petrol,min_vehicle_mileage:10000' (uk), 'cars.carmake_s:toyota,cars.forsaleby_s:ownr' (au) or 'ma:toyota,fu:petrol,max_km:100000' (za). Range filters take min_<key>/max_<key>. Discover keys and values with /search/filters for the same market.
    Integer page = 1; // Integer | 
    String market = "uk"; // String | Which Gumtree: 'uk' (gumtree.com, GBP), 'au' (gumtree.com.au, AUD) or 'za' (gumtree.co.za, ZAR). Separate sites — ids from one market mean nothing in another.
    try {
      Object result = apiInstance.gumtreeSearchListings(query, category, location, distance, minPrice, maxPrice, sort, sellerType, urgentOnly, withPhotos, filters, page, market);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GumtreeApi#gumtreeSearchListings");
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
| **query** | **String**| Search keywords, e.g. &#39;mountain bike&#39; | [optional] |
| **category** | **String**| uk: category slug, e.g. &#39;cars&#39;, &#39;for-sale&#39;, &#39;property-to-rent&#39;, &#39;jobs&#39;, &#39;bicycles&#39;. au/za: numeric category id, e.g. &#39;18320&#39; (au cars) or &#39;9077&#39; (za cars). Use /categories to browse the tree. Default &#39;all&#39;. | [optional] [default to all] |
| **location** | **String**| uk: location slug (&#39;london&#39;), town name or UK postcode (&#39;SW1A 1AA&#39;). au/za: numeric location id, e.g. &#39;3003435&#39; (au Sydney) or &#39;3100003&#39; (za Gauteng). Use /locations/autocomplete to resolve one. Default: the whole country. | [optional] |
| **distance** | **BigDecimal**| Radius around &#x60;location&#x60;: miles (uk) or km (au). Not offered by za. | [optional] |
| **minPrice** | **Integer**| Minimum price in the market&#39;s currency (uk: needs a category, not &#39;all&#39;) | [optional] |
| **maxPrice** | **Integer**| Maximum price in the market&#39;s currency (uk: needs a category, not &#39;all&#39;) | [optional] |
| **sort** | **String**| Result ordering (default relevance). &#39;distance&#39; needs uk, or au with a location. | [optional] [enum: relevance, date, price_asc, price_desc, distance] |
| **sellerType** | **String**| uk/za: &#39;trade&#39; covers dealers, agencies and recruiters. au: not supported — use a category filter such as &#39;cars.forsaleby_s:ownr&#39;. | [optional] [enum: private, trade] |
| **urgentOnly** | **Boolean**| uk only: only ads marked urgent | [optional] [default to false] |
| **withPhotos** | **Boolean**| uk only: only ads with photos | [optional] [default to false] |
| **filters** | **String**| Category-specific filters as comma-separated key:value pairs, e.g. &#39;vehicle_make:bmw,vehicle_fuel_type:petrol,min_vehicle_mileage:10000&#39; (uk), &#39;cars.carmake_s:toyota,cars.forsaleby_s:ownr&#39; (au) or &#39;ma:toyota,fu:petrol,max_km:100000&#39; (za). Range filters take min_&lt;key&gt;/max_&lt;key&gt;. Discover keys and values with /search/filters for the same market. | [optional] |
| **page** | **Integer**|  | [optional] [default to 1] |
| **market** | **String**| Which Gumtree: &#39;uk&#39; (gumtree.com, GBP), &#39;au&#39; (gumtree.com.au, AUD) or &#39;za&#39; (gumtree.co.za, ZAR). Separate sites — ids from one market mean nothing in another. | [optional] [default to uk] [enum: uk, au, za] |

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

<a id="gumtreeSearchSuggestions"></a>
# **gumtreeSearchSuggestions**
> Object gumtreeSearchSuggestions(query, market)

Search suggestions

Gumtree search-box keyword suggestions with their categories.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.GumtreeApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    GumtreeApi apiInstance = new GumtreeApi(defaultClient);
    String query = "query_example"; // String | Partial search term, e.g. 'iph'
    String market = "uk"; // String | Which Gumtree: 'uk' (gumtree.com, GBP), 'au' (gumtree.com.au, AUD) or 'za' (gumtree.co.za, ZAR). Separate sites — ids from one market mean nothing in another.
    try {
      Object result = apiInstance.gumtreeSearchSuggestions(query, market);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GumtreeApi#gumtreeSearchSuggestions");
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
| **query** | **String**| Partial search term, e.g. &#39;iph&#39; | |
| **market** | **String**| Which Gumtree: &#39;uk&#39; (gumtree.com, GBP), &#39;au&#39; (gumtree.com.au, AUD) or &#39;za&#39; (gumtree.co.za, ZAR). Separate sites — ids from one market mean nothing in another. | [optional] [default to uk] [enum: uk, au, za] |

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

