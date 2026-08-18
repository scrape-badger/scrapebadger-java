# BookingApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**bookingBookingScraperHealthCheck**](BookingApi.md#bookingBookingScraperHealthCheck) | **GET** /v1/booking/health | Booking scraper health check |
| [**bookingBookingScraperHealthCheckHead**](BookingApi.md#bookingBookingScraperHealthCheckHead) | **HEAD** /v1/booking/health | Booking scraper health check |
| [**bookingGetPropertyDetail**](BookingApi.md#bookingGetPropertyDetail) | **GET** /v1/booking/properties/{country_code}/{slug} | Get property detail |
| [**bookingGetPropertyReviews**](BookingApi.md#bookingGetPropertyReviews) | **GET** /v1/booking/properties/{country_code}/{slug}/reviews | Get property reviews |
| [**bookingGetRoomTypesAndLiveRates**](BookingApi.md#bookingGetRoomTypesAndLiveRates) | **GET** /v1/booking/properties/{country_code}/{slug}/rooms | Get room types and live rates |
| [**bookingSearchDestinations**](BookingApi.md#bookingSearchDestinations) | **GET** /v1/booking/destinations | Search destinations |
| [**bookingSearchProperties**](BookingApi.md#bookingSearchProperties) | **GET** /v1/booking/search | Search properties |


<a id="bookingBookingScraperHealthCheck"></a>
# **bookingBookingScraperHealthCheck**
> Object bookingBookingScraperHealthCheck()

Booking scraper health check

Check health of the Booking scraper service (accepts HEAD).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.BookingApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    BookingApi apiInstance = new BookingApi(defaultClient);
    try {
      Object result = apiInstance.bookingBookingScraperHealthCheck();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BookingApi#bookingBookingScraperHealthCheck");
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

<a id="bookingBookingScraperHealthCheckHead"></a>
# **bookingBookingScraperHealthCheckHead**
> Object bookingBookingScraperHealthCheckHead()

Booking scraper health check

Check health of the Booking scraper service (accepts HEAD).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.BookingApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    BookingApi apiInstance = new BookingApi(defaultClient);
    try {
      Object result = apiInstance.bookingBookingScraperHealthCheckHead();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BookingApi#bookingBookingScraperHealthCheckHead");
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

<a id="bookingGetPropertyDetail"></a>
# **bookingGetPropertyDetail**
> Object bookingGetPropertyDetail(countryCode, slug, photos, questions, language)

Get property detail

Full detail for one property: description, address and coordinates, star rating, review score with per-category breakdown, facilities, house rules, room types with occupancy and beds, photos and guest Q&amp;A.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.BookingApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    BookingApi apiInstance = new BookingApi(defaultClient);
    String countryCode = "countryCode_example"; // String | Two-letter country code, e.g. 'it'
    String slug = "slug_example"; // String | Booking page name, e.g. 'hotel-artemide'
    Integer photos = 40; // Integer | Gallery photos to return
    Integer questions = 10; // Integer | Guest Q&A pairs to return
    String language = "language_example"; // String | Locale, e.g. en-us, fr
    try {
      Object result = apiInstance.bookingGetPropertyDetail(countryCode, slug, photos, questions, language);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BookingApi#bookingGetPropertyDetail");
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
| **countryCode** | **String**| Two-letter country code, e.g. &#39;it&#39; | |
| **slug** | **String**| Booking page name, e.g. &#39;hotel-artemide&#39; | |
| **photos** | **Integer**| Gallery photos to return | [optional] [default to 40] |
| **questions** | **Integer**| Guest Q&amp;A pairs to return | [optional] [default to 10] |
| **language** | **String**| Locale, e.g. en-us, fr | [optional] |

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

<a id="bookingGetPropertyReviews"></a>
# **bookingGetPropertyReviews**
> Object bookingGetPropertyReviews(countryCode, slug, limit, offset, sort, reviewLanguage, guestType, language)

Get property reviews

Paginated guest reviews with score, positive and negative text, stay dates, room type, guest country and type, photos and the partner&#39;s reply.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.BookingApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    BookingApi apiInstance = new BookingApi(defaultClient);
    String countryCode = "countryCode_example"; // String | Two-letter country code, e.g. 'it'
    String slug = "slug_example"; // String | Booking page name, e.g. 'hotel-artemide'
    Integer limit = 25; // Integer | 
    Integer offset = 0; // Integer | 
    String sort = "MOST_RELEVANT"; // String | MOST_RELEVANT | NEWEST_FIRST | OLDEST_FIRST | SCORE_DESC | SCORE_ASC
    String reviewLanguage = "reviewLanguage_example"; // String | Only reviews written in this language, e.g. 'fr'
    String guestType = "guestType_example"; // String | FAMILIES | COUPLES | GROUP_OF_FRIENDS | SOLO_TRAVELLERS | BUSINESS_TRAVELLERS
    String language = "language_example"; // String | Locale for labels, e.g. en-us
    try {
      Object result = apiInstance.bookingGetPropertyReviews(countryCode, slug, limit, offset, sort, reviewLanguage, guestType, language);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BookingApi#bookingGetPropertyReviews");
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
| **countryCode** | **String**| Two-letter country code, e.g. &#39;it&#39; | |
| **slug** | **String**| Booking page name, e.g. &#39;hotel-artemide&#39; | |
| **limit** | **Integer**|  | [optional] [default to 25] |
| **offset** | **Integer**|  | [optional] [default to 0] |
| **sort** | **String**| MOST_RELEVANT | NEWEST_FIRST | OLDEST_FIRST | SCORE_DESC | SCORE_ASC | [optional] [default to MOST_RELEVANT] |
| **reviewLanguage** | **String**| Only reviews written in this language, e.g. &#39;fr&#39; | [optional] |
| **guestType** | **String**| FAMILIES | COUPLES | GROUP_OF_FRIENDS | SOLO_TRAVELLERS | BUSINESS_TRAVELLERS | [optional] |
| **language** | **String**| Locale for labels, e.g. en-us | [optional] |

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

<a id="bookingGetRoomTypesAndLiveRates"></a>
# **bookingGetRoomTypesAndLiveRates**
> Object bookingGetRoomTypesAndLiveRates(countryCode, slug, checkin, checkout, adults, children, rooms, currency, language)

Get room types and live rates

Every room type at one property with every rate bookable on it for the given dates — price, price before discount, price per night, discounts and badges — plus per-room facilities, bed layouts, occupancy and photos. /search returns only the cheapest rate per property; this returns the whole table.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.BookingApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    BookingApi apiInstance = new BookingApi(defaultClient);
    String countryCode = "countryCode_example"; // String | Two-letter country code, e.g. 'it'
    String slug = "slug_example"; // String | Booking page name, e.g. 'hotel-artemide'
    String checkin = "checkin_example"; // String | Check-in date YYYY-MM-DD
    String checkout = "checkout_example"; // String | Check-out date YYYY-MM-DD
    Integer adults = 2; // Integer | 
    String children = "children_example"; // String | Comma-separated children ages, e.g. '4,9'
    Integer rooms = 1; // Integer | 
    String currency = "currency_example"; // String | ISO currency, e.g. EUR, USD, GBP
    String language = "language_example"; // String | Locale, e.g. en-us, fr, de
    try {
      Object result = apiInstance.bookingGetRoomTypesAndLiveRates(countryCode, slug, checkin, checkout, adults, children, rooms, currency, language);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BookingApi#bookingGetRoomTypesAndLiveRates");
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
| **countryCode** | **String**| Two-letter country code, e.g. &#39;it&#39; | |
| **slug** | **String**| Booking page name, e.g. &#39;hotel-artemide&#39; | |
| **checkin** | **String**| Check-in date YYYY-MM-DD | |
| **checkout** | **String**| Check-out date YYYY-MM-DD | |
| **adults** | **Integer**|  | [optional] [default to 2] |
| **children** | **String**| Comma-separated children ages, e.g. &#39;4,9&#39; | [optional] |
| **rooms** | **Integer**|  | [optional] [default to 1] |
| **currency** | **String**| ISO currency, e.g. EUR, USD, GBP | [optional] |
| **language** | **String**| Locale, e.g. en-us, fr, de | [optional] |

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

<a id="bookingSearchDestinations"></a>
# **bookingSearchDestinations**
> Object bookingSearchDestinations(query, limit, language)

Search destinations

Resolve a place name to Booking&#39;s &#x60;dest_id&#x60;/&#x60;dest_type&#x60;, with coordinates and country — feed the pair back into /search for an exact match.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.BookingApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    BookingApi apiInstance = new BookingApi(defaultClient);
    String query = "query_example"; // String | Free-text place, e.g. 'amsterd'
    Integer limit = 8; // Integer | 
    String language = "language_example"; // String | Locale, e.g. en-us, fr
    try {
      Object result = apiInstance.bookingSearchDestinations(query, limit, language);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BookingApi#bookingSearchDestinations");
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
| **query** | **String**| Free-text place, e.g. &#39;amsterd&#39; | |
| **limit** | **Integer**|  | [optional] [default to 8] |
| **language** | **String**| Locale, e.g. en-us, fr | [optional] |

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

<a id="bookingSearchProperties"></a>
# **bookingSearchProperties**
> Object bookingSearchProperties(location, destId, destType, checkin, checkout, adults, children, rooms, offset, limit, sort, filters, currency, language)

Search properties

Search Booking.com properties by destination, with dates, occupancy, sorting and filters. Returns prices, review scores, coordinates, room configuration and photos. Paginate with &#x60;offset&#x60;.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.BookingApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    BookingApi apiInstance = new BookingApi(defaultClient);
    String location = "location_example"; // String | Free-text destination, e.g. 'Rome'
    Integer destId = 56; // Integer | Exact destination id (ufi) from /destinations
    String destType = "NO_DEST_TYPE"; // String | Destination type, e.g. CITY
    String checkin = "checkin_example"; // String | Check-in date YYYY-MM-DD
    String checkout = "checkout_example"; // String | Check-out date YYYY-MM-DD
    Integer adults = 2; // Integer | 
    String children = "children_example"; // String | Comma-separated children ages, e.g. '4,9'
    Integer rooms = 1; // Integer | 
    Integer offset = 0; // Integer | Result offset for pagination
    Integer limit = 25; // Integer | 
    String sort = "sort_example"; // String | popularity | price | class_descending | class_ascending | distance_from_search | bayesian_review_score | review_score_and_price | upsort_bh
    String filters = "filters_example"; // String | Semicolon-separated Booking filter ids, e.g. 'class=4'
    String currency = "currency_example"; // String | ISO currency, e.g. EUR, USD, GBP
    String language = "language_example"; // String | Locale, e.g. en-us, fr, de, es
    try {
      Object result = apiInstance.bookingSearchProperties(location, destId, destType, checkin, checkout, adults, children, rooms, offset, limit, sort, filters, currency, language);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BookingApi#bookingSearchProperties");
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
| **location** | **String**| Free-text destination, e.g. &#39;Rome&#39; | [optional] |
| **destId** | **Integer**| Exact destination id (ufi) from /destinations | [optional] |
| **destType** | **String**| Destination type, e.g. CITY | [optional] [default to NO_DEST_TYPE] |
| **checkin** | **String**| Check-in date YYYY-MM-DD | [optional] |
| **checkout** | **String**| Check-out date YYYY-MM-DD | [optional] |
| **adults** | **Integer**|  | [optional] [default to 2] |
| **children** | **String**| Comma-separated children ages, e.g. &#39;4,9&#39; | [optional] |
| **rooms** | **Integer**|  | [optional] [default to 1] |
| **offset** | **Integer**| Result offset for pagination | [optional] [default to 0] |
| **limit** | **Integer**|  | [optional] [default to 25] |
| **sort** | **String**| popularity | price | class_descending | class_ascending | distance_from_search | bayesian_review_score | review_score_and_price | upsort_bh | [optional] |
| **filters** | **String**| Semicolon-separated Booking filter ids, e.g. &#39;class&#x3D;4&#39; | [optional] |
| **currency** | **String**| ISO currency, e.g. EUR, USD, GBP | [optional] |
| **language** | **String**| Locale, e.g. en-us, fr, de, es | [optional] |

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

