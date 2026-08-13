# AirbnbApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**airbnbAirbnbScraperHealthCheck**](AirbnbApi.md#airbnbAirbnbScraperHealthCheck) | **GET** /v1/airbnb/health | Airbnb scraper health check |
| [**airbnbAirbnbScraperHealthCheckHead**](AirbnbApi.md#airbnbAirbnbScraperHealthCheckHead) | **HEAD** /v1/airbnb/health | Airbnb scraper health check |
| [**airbnbGetAvailabilityCalendar**](AirbnbApi.md#airbnbGetAvailabilityCalendar) | **GET** /v1/airbnb/listings/{room_id}/calendar | Get availability calendar |
| [**airbnbGetExperienceDetail**](AirbnbApi.md#airbnbGetExperienceDetail) | **GET** /v1/airbnb/experiences/{experience_id} | Get experience detail |
| [**airbnbGetListingDetail**](AirbnbApi.md#airbnbGetListingDetail) | **GET** /v1/airbnb/listings/{room_id} | Get listing detail |
| [**airbnbGetListingReviews**](AirbnbApi.md#airbnbGetListingReviews) | **GET** /v1/airbnb/listings/{room_id}/reviews | Get listing reviews |
| [**airbnbSearchExperiences**](AirbnbApi.md#airbnbSearchExperiences) | **GET** /v1/airbnb/experiences | Search experiences |
| [**airbnbSearchStays**](AirbnbApi.md#airbnbSearchStays) | **GET** /v1/airbnb/search | Search stays |


<a id="airbnbAirbnbScraperHealthCheck"></a>
# **airbnbAirbnbScraperHealthCheck**
> Object airbnbAirbnbScraperHealthCheck()

Airbnb scraper health check

Check health of the Airbnb scraper service (accepts HEAD).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.AirbnbApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    AirbnbApi apiInstance = new AirbnbApi(defaultClient);
    try {
      Object result = apiInstance.airbnbAirbnbScraperHealthCheck();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AirbnbApi#airbnbAirbnbScraperHealthCheck");
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

<a id="airbnbAirbnbScraperHealthCheckHead"></a>
# **airbnbAirbnbScraperHealthCheckHead**
> Object airbnbAirbnbScraperHealthCheckHead()

Airbnb scraper health check

Check health of the Airbnb scraper service (accepts HEAD).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.AirbnbApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    AirbnbApi apiInstance = new AirbnbApi(defaultClient);
    try {
      Object result = apiInstance.airbnbAirbnbScraperHealthCheckHead();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AirbnbApi#airbnbAirbnbScraperHealthCheckHead");
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

<a id="airbnbGetAvailabilityCalendar"></a>
# **airbnbGetAvailabilityCalendar**
> Object airbnbGetAvailabilityCalendar(roomId, month, year, months, currency, locale)

Get availability calendar

Day-by-day availability for up to 12 months: bookable, check-in/out windows and min/max nights per date.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.AirbnbApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    AirbnbApi apiInstance = new AirbnbApi(defaultClient);
    String roomId = "roomId_example"; // String | 
    Integer month = 1; // Integer | Start month (1-12)
    Integer year = 2026; // Integer | Start year
    Integer months = 12; // Integer | Number of months (max 12)
    String currency = "currency_example"; // String | 
    String locale = "locale_example"; // String | 
    try {
      Object result = apiInstance.airbnbGetAvailabilityCalendar(roomId, month, year, months, currency, locale);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AirbnbApi#airbnbGetAvailabilityCalendar");
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
| **roomId** | **String**|  | |
| **month** | **Integer**| Start month (1-12) | [optional] [default to 1] |
| **year** | **Integer**| Start year | [optional] [default to 2026] |
| **months** | **Integer**| Number of months (max 12) | [optional] [default to 12] |
| **currency** | **String**|  | [optional] |
| **locale** | **String**|  | [optional] |

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

<a id="airbnbGetExperienceDetail"></a>
# **airbnbGetExperienceDetail**
> Object airbnbGetExperienceDetail(experienceId, adults, children, infants, currency, locale)

Get experience detail

Full detail for one experience: description, rating, host, location and photos.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.AirbnbApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    AirbnbApi apiInstance = new AirbnbApi(defaultClient);
    String experienceId = "experienceId_example"; // String | 
    Integer adults = 1; // Integer | 
    Integer children = 0; // Integer | 
    Integer infants = 0; // Integer | 
    String currency = "currency_example"; // String | 
    String locale = "locale_example"; // String | 
    try {
      Object result = apiInstance.airbnbGetExperienceDetail(experienceId, adults, children, infants, currency, locale);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AirbnbApi#airbnbGetExperienceDetail");
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
| **experienceId** | **String**|  | |
| **adults** | **Integer**|  | [optional] [default to 1] |
| **children** | **Integer**|  | [optional] [default to 0] |
| **infants** | **Integer**|  | [optional] [default to 0] |
| **currency** | **String**|  | [optional] |
| **locale** | **String**|  | [optional] |

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

<a id="airbnbGetListingDetail"></a>
# **airbnbGetListingDetail**
> Object airbnbGetListingDetail(roomId, adults, currency, locale)

Get listing detail

Full detail for one listing: amenities, house rules, host, ratings, coordinates and photos.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.AirbnbApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    AirbnbApi apiInstance = new AirbnbApi(defaultClient);
    String roomId = "roomId_example"; // String | 
    Integer adults = 1; // Integer | 
    String currency = "currency_example"; // String | 
    String locale = "locale_example"; // String | 
    try {
      Object result = apiInstance.airbnbGetListingDetail(roomId, adults, currency, locale);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AirbnbApi#airbnbGetListingDetail");
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
| **roomId** | **String**|  | |
| **adults** | **Integer**|  | [optional] [default to 1] |
| **currency** | **String**|  | [optional] |
| **locale** | **String**|  | [optional] |

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

<a id="airbnbGetListingReviews"></a>
# **airbnbGetListingReviews**
> Object airbnbGetListingReviews(roomId, limit, offset, sort, currency, locale)

Get listing reviews

Paginated guest reviews with reviewer, rating, date, text and host response.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.AirbnbApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    AirbnbApi apiInstance = new AirbnbApi(defaultClient);
    String roomId = "roomId_example"; // String | 
    Integer limit = 24; // Integer | 
    Integer offset = 0; // Integer | 
    String sort = "MOST_RECENT"; // String | MOST_RECENT | RATING_DESC | RATING_ASC
    String currency = "currency_example"; // String | 
    String locale = "locale_example"; // String | 
    try {
      Object result = apiInstance.airbnbGetListingReviews(roomId, limit, offset, sort, currency, locale);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AirbnbApi#airbnbGetListingReviews");
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
| **roomId** | **String**|  | |
| **limit** | **Integer**|  | [optional] [default to 24] |
| **offset** | **Integer**|  | [optional] [default to 0] |
| **sort** | **String**| MOST_RECENT | RATING_DESC | RATING_ASC | [optional] [default to MOST_RECENT] |
| **currency** | **String**|  | [optional] |
| **locale** | **String**|  | [optional] |

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

<a id="airbnbSearchExperiences"></a>
# **airbnbSearchExperiences**
> Object airbnbSearchExperiences(location, cursor, currency, locale)

Search experiences

Search Airbnb Experiences by location.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.AirbnbApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    AirbnbApi apiInstance = new AirbnbApi(defaultClient);
    String location = "location_example"; // String | Free-text place, e.g. 'Rome, Italy'
    String cursor = "cursor_example"; // String | next_page_cursor from a prior response
    String currency = "currency_example"; // String | 
    String locale = "locale_example"; // String | 
    try {
      Object result = apiInstance.airbnbSearchExperiences(location, cursor, currency, locale);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AirbnbApi#airbnbSearchExperiences");
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
| **location** | **String**| Free-text place, e.g. &#39;Rome, Italy&#39; | |
| **cursor** | **String**| next_page_cursor from a prior response | [optional] |
| **currency** | **String**|  | [optional] |
| **locale** | **String**|  | [optional] |

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

<a id="airbnbSearchStays"></a>
# **airbnbSearchStays**
> Object airbnbSearchStays(location, neLat, neLng, swLat, swLng, checkIn, checkOut, adults, children, infants, pets, priceMin, priceMax, minBedrooms, minBeds, minBathrooms, roomType, cursor, limit, currency, locale)

Search stays

Search Airbnb stays by place name and/or map bounding box, with dates, guests, price and property filters. Paginate with the &#x60;cursor&#x60;.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.AirbnbApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    AirbnbApi apiInstance = new AirbnbApi(defaultClient);
    String location = "location_example"; // String | Free-text place, e.g. 'Paris, France'
    BigDecimal neLat = new BigDecimal(78); // BigDecimal | Map bounding-box NE latitude
    BigDecimal neLng = new BigDecimal(78); // BigDecimal | Map bounding-box NE longitude
    BigDecimal swLat = new BigDecimal(78); // BigDecimal | Map bounding-box SW latitude
    BigDecimal swLng = new BigDecimal(78); // BigDecimal | Map bounding-box SW longitude
    String checkIn = "checkIn_example"; // String | Check-in date YYYY-MM-DD
    String checkOut = "checkOut_example"; // String | Check-out date YYYY-MM-DD
    Integer adults = 1; // Integer | 
    Integer children = 0; // Integer | 
    Integer infants = 0; // Integer | 
    Integer pets = 0; // Integer | 
    Integer priceMin = 56; // Integer | 
    Integer priceMax = 56; // Integer | 
    Integer minBedrooms = 56; // Integer | 
    Integer minBeds = 56; // Integer | 
    Integer minBathrooms = 56; // Integer | 
    String roomType = "roomType_example"; // String | e.g. 'Entire home/apt', 'Private room'
    String cursor = "cursor_example"; // String | next_page_cursor from a prior response
    Integer limit = 18; // Integer | 
    String currency = "currency_example"; // String | ISO currency, e.g. USD, EUR
    String locale = "locale_example"; // String | Locale, e.g. en, fr
    try {
      Object result = apiInstance.airbnbSearchStays(location, neLat, neLng, swLat, swLng, checkIn, checkOut, adults, children, infants, pets, priceMin, priceMax, minBedrooms, minBeds, minBathrooms, roomType, cursor, limit, currency, locale);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AirbnbApi#airbnbSearchStays");
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
| **location** | **String**| Free-text place, e.g. &#39;Paris, France&#39; | [optional] |
| **neLat** | **BigDecimal**| Map bounding-box NE latitude | [optional] |
| **neLng** | **BigDecimal**| Map bounding-box NE longitude | [optional] |
| **swLat** | **BigDecimal**| Map bounding-box SW latitude | [optional] |
| **swLng** | **BigDecimal**| Map bounding-box SW longitude | [optional] |
| **checkIn** | **String**| Check-in date YYYY-MM-DD | [optional] |
| **checkOut** | **String**| Check-out date YYYY-MM-DD | [optional] |
| **adults** | **Integer**|  | [optional] [default to 1] |
| **children** | **Integer**|  | [optional] [default to 0] |
| **infants** | **Integer**|  | [optional] [default to 0] |
| **pets** | **Integer**|  | [optional] [default to 0] |
| **priceMin** | **Integer**|  | [optional] |
| **priceMax** | **Integer**|  | [optional] |
| **minBedrooms** | **Integer**|  | [optional] |
| **minBeds** | **Integer**|  | [optional] |
| **minBathrooms** | **Integer**|  | [optional] |
| **roomType** | **String**| e.g. &#39;Entire home/apt&#39;, &#39;Private room&#39; | [optional] |
| **cursor** | **String**| next_page_cursor from a prior response | [optional] |
| **limit** | **Integer**|  | [optional] [default to 18] |
| **currency** | **String**| ISO currency, e.g. USD, EUR | [optional] |
| **locale** | **String**| Locale, e.g. en, fr | [optional] |

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

