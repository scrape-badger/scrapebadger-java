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
| [**gumtreeLocationSuggestions**](GumtreeApi.md#gumtreeLocationSuggestions) | **GET** /v1/gumtree/locations/autocomplete | Location suggestions |
| [**gumtreeSearchListings**](GumtreeApi.md#gumtreeSearchListings) | **GET** /v1/gumtree/search | Search listings |
| [**gumtreeSearchSuggestions**](GumtreeApi.md#gumtreeSearchSuggestions) | **GET** /v1/gumtree/autocomplete | Search suggestions |


<a id="gumtreeGetListing"></a>
# **gumtreeGetListing**
> Object gumtreeGetListing(listingId)

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
    String listingId = "listingId_example"; // String | Gumtree listing id — the number at the end of a gumtree.com/p/... URL
    try {
      Object result = apiInstance.gumtreeGetListing(listingId);
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
| **listingId** | **String**| Gumtree listing id — the number at the end of a gumtree.com/p/... URL | |

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
> Object gumtreeGetSearchFilters(category, location, query)

Get search filters

Filters, sort orders and radius options for a category, with live counts.

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
    String category = "all"; // String | Category slug, e.g. 'cars', 'for-sale', 'property-to-rent', 'jobs'. Default 'all'.
    String location = "uk"; // String | Location slug ('london'), town name or UK postcode ('SW1A 1AA'). Default 'uk'.
    String query = "query_example"; // String | 
    try {
      Object result = apiInstance.gumtreeGetSearchFilters(category, location, query);
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
| **category** | **String**| Category slug, e.g. &#39;cars&#39;, &#39;for-sale&#39;, &#39;property-to-rent&#39;, &#39;jobs&#39;. Default &#39;all&#39;. | [optional] [default to all] |
| **location** | **String**| Location slug (&#39;london&#39;), town name or UK postcode (&#39;SW1A 1AA&#39;). Default &#39;uk&#39;. | [optional] [default to uk] |
| **query** | **String**|  | [optional] |

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
> Object gumtreeGetSellerListings(listingId, page)

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
    String listingId = "listingId_example"; // String | Gumtree listing id — the number at the end of a gumtree.com/p/... URL
    Integer page = 1; // Integer | 
    try {
      Object result = apiInstance.gumtreeGetSellerListings(listingId, page);
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
| **listingId** | **String**| Gumtree listing id — the number at the end of a gumtree.com/p/... URL | |
| **page** | **Integer**|  | [optional] [default to 1] |

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
> Object gumtreeListCategories(parentId)

List categories

Browse Gumtree&#39;s category tree. A node&#39;s &#x60;slug&#x60; is the &#x60;/search&#x60; category.

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
    Integer parentId = 1; // Integer | Parent category id (default: all)
    try {
      Object result = apiInstance.gumtreeListCategories(parentId);
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
| **parentId** | **Integer**| Parent category id (default: all) | [optional] [default to 1] |

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
> Object gumtreeListLocations(parentId)

List locations

Browse Gumtree&#39;s location tree.

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
    Integer parentId = 10000392; // Integer | Parent location id (default: UK)
    try {
      Object result = apiInstance.gumtreeListLocations(parentId);
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
| **parentId** | **Integer**| Parent location id (default: UK) | [optional] [default to 10000392] |

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

<a id="gumtreeLocationSuggestions"></a>
# **gumtreeLocationSuggestions**
> Object gumtreeLocationSuggestions(query)

Location suggestions

Resolve a place name or postcode to Gumtree locations with coordinates.

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
    String query = "query_example"; // String | Town or postcode prefix, e.g. 'manch'
    try {
      Object result = apiInstance.gumtreeLocationSuggestions(query);
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
| **query** | **String**| Town or postcode prefix, e.g. &#39;manch&#39; | |

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
> Object gumtreeSearchListings(query, category, location, distance, minPrice, maxPrice, sort, sellerType, urgentOnly, withPhotos, filters, page)

Search listings

Search gumtree.com listings. ~25-30 per page, up to 50 pages.

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
    String category = "all"; // String | Category slug, e.g. 'cars', 'for-sale', 'property-to-rent', 'jobs'. Default 'all'.
    String location = "uk"; // String | Location slug ('london'), town name or UK postcode ('SW1A 1AA'). Default 'uk'.
    BigDecimal distance = new BigDecimal(78); // BigDecimal | Radius in miles
    Integer minPrice = 56; // Integer | GBP; needs a category
    Integer maxPrice = 56; // Integer | GBP; needs a category
    String sort = "relevance"; // String | 
    String sellerType = "private"; // String | 
    Boolean urgentOnly = false; // Boolean | 
    Boolean withPhotos = false; // Boolean | 
    String filters = "filters_example"; // String | Category filters as key:value pairs, e.g. 'vehicle_make:bmw,vehicle_fuel_type:petrol'
    Integer page = 1; // Integer | 
    try {
      Object result = apiInstance.gumtreeSearchListings(query, category, location, distance, minPrice, maxPrice, sort, sellerType, urgentOnly, withPhotos, filters, page);
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
| **category** | **String**| Category slug, e.g. &#39;cars&#39;, &#39;for-sale&#39;, &#39;property-to-rent&#39;, &#39;jobs&#39;. Default &#39;all&#39;. | [optional] [default to all] |
| **location** | **String**| Location slug (&#39;london&#39;), town name or UK postcode (&#39;SW1A 1AA&#39;). Default &#39;uk&#39;. | [optional] [default to uk] |
| **distance** | **BigDecimal**| Radius in miles | [optional] |
| **minPrice** | **Integer**| GBP; needs a category | [optional] |
| **maxPrice** | **Integer**| GBP; needs a category | [optional] |
| **sort** | **String**|  | [optional] [enum: relevance, date, price_asc, price_desc, distance] |
| **sellerType** | **String**|  | [optional] [enum: private, trade] |
| **urgentOnly** | **Boolean**|  | [optional] [default to false] |
| **withPhotos** | **Boolean**|  | [optional] [default to false] |
| **filters** | **String**| Category filters as key:value pairs, e.g. &#39;vehicle_make:bmw,vehicle_fuel_type:petrol&#39; | [optional] |
| **page** | **Integer**|  | [optional] [default to 1] |

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
> Object gumtreeSearchSuggestions(query)

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
    try {
      Object result = apiInstance.gumtreeSearchSuggestions(query);
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

