# ApartmentsApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**apartmentsApartmentsScraperHealthCheck**](ApartmentsApi.md#apartmentsApartmentsScraperHealthCheck) | **GET** /v1/apartments/health | Apartments scraper health check |
| [**apartmentsApartmentsScraperHealthCheckHead**](ApartmentsApi.md#apartmentsApartmentsScraperHealthCheckHead) | **HEAD** /v1/apartments/health | Apartments scraper health check |
| [**apartmentsGetPropertyDetailBySlugId**](ApartmentsApi.md#apartmentsGetPropertyDetailBySlugId) | **GET** /v1/apartments/properties/{slug}/{property_id} | Get property detail by slug + id |
| [**apartmentsGetPropertyDetailByUrl**](ApartmentsApi.md#apartmentsGetPropertyDetailByUrl) | **GET** /v1/apartments/property | Get property detail by URL |
| [**apartmentsSearchRentalListings**](ApartmentsApi.md#apartmentsSearchRentalListings) | **GET** /v1/apartments/search | Search rental listings |


<a id="apartmentsApartmentsScraperHealthCheck"></a>
# **apartmentsApartmentsScraperHealthCheck**
> Object apartmentsApartmentsScraperHealthCheck()

Apartments scraper health check

Check health of the Apartments scraper service (accepts HEAD for UptimeRobot).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.ApartmentsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    ApartmentsApi apiInstance = new ApartmentsApi(defaultClient);
    try {
      Object result = apiInstance.apartmentsApartmentsScraperHealthCheck();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ApartmentsApi#apartmentsApartmentsScraperHealthCheck");
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

<a id="apartmentsApartmentsScraperHealthCheckHead"></a>
# **apartmentsApartmentsScraperHealthCheckHead**
> Object apartmentsApartmentsScraperHealthCheckHead()

Apartments scraper health check

Check health of the Apartments scraper service (accepts HEAD for UptimeRobot).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.ApartmentsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    ApartmentsApi apiInstance = new ApartmentsApi(defaultClient);
    try {
      Object result = apiInstance.apartmentsApartmentsScraperHealthCheckHead();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ApartmentsApi#apartmentsApartmentsScraperHealthCheckHead");
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

<a id="apartmentsGetPropertyDetailBySlugId"></a>
# **apartmentsGetPropertyDetailBySlugId**
> Object apartmentsGetPropertyDetailBySlugId(slug, propertyId)

Get property detail by slug + id

Get a property by its SEO slug and 7-character listing id.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.ApartmentsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    ApartmentsApi apiInstance = new ApartmentsApi(defaultClient);
    String slug = "slug_example"; // String | 
    String propertyId = "propertyId_example"; // String | 
    try {
      Object result = apiInstance.apartmentsGetPropertyDetailBySlugId(slug, propertyId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ApartmentsApi#apartmentsGetPropertyDetailBySlugId");
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
| **slug** | **String**|  | |
| **propertyId** | **String**|  | |

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

<a id="apartmentsGetPropertyDetailByUrl"></a>
# **apartmentsGetPropertyDetailByUrl**
> Object apartmentsGetPropertyDetailByUrl(url)

Get property detail by URL

Get an apartments.com property with full per-unit pricing and availability.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.ApartmentsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    ApartmentsApi apiInstance = new ApartmentsApi(defaultClient);
    String url = "url_example"; // String | Full apartments.com property URL, e.g. https://www.apartments.com/urbane-kansas-city-mo/wcd6e5k/
    try {
      Object result = apiInstance.apartmentsGetPropertyDetailByUrl(url);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ApartmentsApi#apartmentsGetPropertyDetailByUrl");
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
| **url** | **String**| Full apartments.com property URL, e.g. https://www.apartments.com/urbane-kansas-city-mo/wcd6e5k/ | |

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

<a id="apartmentsSearchRentalListings"></a>
# **apartmentsSearchRentalListings**
> Object apartmentsSearchRentalListings(location, page, beds, minPrice, maxPrice)

Search rental listings

Search apartments.com for rental properties. 40 cards per page.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.ApartmentsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    ApartmentsApi apiInstance = new ApartmentsApi(defaultClient);
    String location = "location_example"; // String | apartments.com location slug, e.g. 'kansas-city-mo'
    Integer page = 1; // Integer | 
    Integer beds = 56; // Integer | 0=studio, 1-4 bedrooms
    Integer minPrice = 56; // Integer | 
    Integer maxPrice = 56; // Integer | 
    try {
      Object result = apiInstance.apartmentsSearchRentalListings(location, page, beds, minPrice, maxPrice);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ApartmentsApi#apartmentsSearchRentalListings");
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
| **location** | **String**| apartments.com location slug, e.g. &#39;kansas-city-mo&#39; | |
| **page** | **Integer**|  | [optional] [default to 1] |
| **beds** | **Integer**| 0&#x3D;studio, 1-4 bedrooms | [optional] |
| **minPrice** | **Integer**|  | [optional] |
| **maxPrice** | **Integer**|  | [optional] |

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

