# GoogleApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**googleGetAuthorCitationsPerYearChart**](GoogleApi.md#googleGetAuthorCitationsPerYearChart) | **GET** /v1/google/scholar/author/citation | Get author citations-per-year chart |
| [**googleGetBusinessPosts**](GoogleApi.md#googleGetBusinessPosts) | **GET** /v1/google/maps/posts | Get business posts |
| [**googleGetCitationFormatsForAScholarPaper**](GoogleApi.md#googleGetCitationFormatsForAScholarPaper) | **GET** /v1/google/scholar/cite | Get citation formats for a Scholar paper |
| [**googleGetPlaceDetails**](GoogleApi.md#googleGetPlaceDetails) | **GET** /v1/google/maps/place | Get place details |
| [**googleGetPlacePhotos**](GoogleApi.md#googleGetPlacePhotos) | **GET** /v1/google/maps/photos | Get place photos |
| [**googleGetPlaceReviews**](GoogleApi.md#googleGetPlaceReviews) | **GET** /v1/google/maps/reviews | Get place reviews |
| [**googleGetScholarAuthorProfile**](GoogleApi.md#googleGetScholarAuthorProfile) | **GET** /v1/google/scholar/author | Get Scholar author profile |
| [**googleGetStockIndexQuote**](GoogleApi.md#googleGetStockIndexQuote) | **GET** /v1/google/finance/quote | Get stock/index quote |
| [**googleGoogleAiModeSearch**](GoogleApi.md#googleGoogleAiModeSearch) | **GET** /v1/google/ai-mode/search | Google AI Mode search |
| [**googleGoogleAiOverviewInlineSerpBlock**](GoogleApi.md#googleGoogleAiOverviewInlineSerpBlock) | **GET** /v1/google/ai-overview | Google AI Overview (inline SERP block) |
| [**googleGoogleFlightsCalendarCheapestFarePerDate**](GoogleApi.md#googleGoogleFlightsCalendarCheapestFarePerDate) | **GET** /v1/google/flights/calendar | Google Flights calendar — cheapest fare per date |
| [**googleGoogleFlightsSearch**](GoogleApi.md#googleGoogleFlightsSearch) | **GET** /v1/google/flights/search | Google Flights search |
| [**googleGoogleLensVisualSearch**](GoogleApi.md#googleGoogleLensVisualSearch) | **GET** /v1/google/lens/search | Google Lens visual search |
| [**googleGoogleScraperHealthCheck**](GoogleApi.md#googleGoogleScraperHealthCheck) | **GET** /v1/google/health | Google scraper health check |
| [**googleGoogleScraperHealthCheckHead**](GoogleApi.md#googleGoogleScraperHealthCheckHead) | **HEAD** /v1/google/health | Google scraper health check |
| [**googleGoogleSearchSuggestions**](GoogleApi.md#googleGoogleSearchSuggestions) | **GET** /v1/google/autocomplete | Google search suggestions |
| [**googleGoogleShortsSearch**](GoogleApi.md#googleGoogleShortsSearch) | **GET** /v1/google/shorts/search | Google Shorts search |
| [**googleGoogleWebSearch**](GoogleApi.md#googleGoogleWebSearch) | **GET** /v1/google/search | Google web search |
| [**googleHotelDetails**](GoogleApi.md#googleHotelDetails) | **GET** /v1/google/hotels/details | Hotel details |
| [**googleImmersiveProductDetail**](GoogleApi.md#googleImmersiveProductDetail) | **GET** /v1/google/products/detail | Immersive product detail |
| [**googleInterestByRegion**](GoogleApi.md#googleInterestByRegion) | **GET** /v1/google/trends/regions | Interest by region |
| [**googleInterestOverTime**](GoogleApi.md#googleInterestOverTime) | **GET** /v1/google/trends/interest | Interest over time |
| [**googleMultiSellerOffersByBarcode**](GoogleApi.md#googleMultiSellerOffersByBarcode) | **GET** /v1/google/shopping/offers | Multi-seller offers by barcode |
| [**googleNewsByTopic**](GoogleApi.md#googleNewsByTopic) | **GET** /v1/google/news/topics | News by topic |
| [**googlePatentDetails**](GoogleApi.md#googlePatentDetails) | **GET** /v1/google/patents/detail | Patent details |
| [**googleRelatedTopicsQueries**](GoogleApi.md#googleRelatedTopicsQueries) | **GET** /v1/google/trends/related | Related topics &amp; queries |
| [**googleSearchGoogleImages**](GoogleApi.md#googleSearchGoogleImages) | **GET** /v1/google/images/search | Search Google Images |
| [**googleSearchGoogleJobs**](GoogleApi.md#googleSearchGoogleJobs) | **GET** /v1/google/jobs/search | Search Google Jobs |
| [**googleSearchGoogleMapsPlaces**](GoogleApi.md#googleSearchGoogleMapsPlaces) | **GET** /v1/google/maps/search | Search Google Maps places |
| [**googleSearchGoogleNews**](GoogleApi.md#googleSearchGoogleNews) | **GET** /v1/google/news/search | Search Google News |
| [**googleSearchGoogleScholar**](GoogleApi.md#googleSearchGoogleScholar) | **GET** /v1/google/scholar/search | Search Google Scholar |
| [**googleSearchGoogleVideos**](GoogleApi.md#googleSearchGoogleVideos) | **GET** /v1/google/videos/search | Search Google Videos |
| [**googleSearchHotels**](GoogleApi.md#googleSearchHotels) | **GET** /v1/google/hotels/search | Search hotels |
| [**googleSearchPatents**](GoogleApi.md#googleSearchPatents) | **GET** /v1/google/patents/search | Search patents |
| [**googleSearchProducts**](GoogleApi.md#googleSearchProducts) | **GET** /v1/google/shopping/search | Search products |
| [**googleSearchScholarAuthorProfiles**](GoogleApi.md#googleSearchScholarAuthorProfiles) | **GET** /v1/google/scholar/profiles | Search Scholar author profiles |
| [**googleTrendingNews**](GoogleApi.md#googleTrendingNews) | **GET** /v1/google/news/trending | Trending news |
| [**googleTrendingSearches**](GoogleApi.md#googleTrendingSearches) | **GET** /v1/google/trends/trending | Trending searches |
| [**googleTrendsTopicAutocomplete**](GoogleApi.md#googleTrendsTopicAutocomplete) | **GET** /v1/google/trends/autocomplete | Trends topic autocomplete |


<a id="googleGetAuthorCitationsPerYearChart"></a>
# **googleGetAuthorCitationsPerYearChart**
> Object googleGetAuthorCitationsPerYearChart(authorId, hl)

Get author citations-per-year chart

Return the citations-per-year chart for a Google Scholar author.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.GoogleApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    GoogleApi apiInstance = new GoogleApi(defaultClient);
    String authorId = "authorId_example"; // String | Scholar user ID
    String hl = "en"; // String | Language code
    try {
      Object result = apiInstance.googleGetAuthorCitationsPerYearChart(authorId, hl);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GoogleApi#googleGetAuthorCitationsPerYearChart");
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
| **authorId** | **String**| Scholar user ID | |
| **hl** | **String**| Language code | [optional] [default to en] |

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

<a id="googleGetBusinessPosts"></a>
# **googleGetBusinessPosts**
> Object googleGetBusinessPosts(dataId, nextPageToken)

Get business posts

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.GoogleApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    GoogleApi apiInstance = new GoogleApi(defaultClient);
    String dataId = "dataId_example"; // String | Maps data ID
    String nextPageToken = "nextPageToken_example"; // String | 
    try {
      Object result = apiInstance.googleGetBusinessPosts(dataId, nextPageToken);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GoogleApi#googleGetBusinessPosts");
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
| **dataId** | **String**| Maps data ID | |
| **nextPageToken** | **String**|  | [optional] |

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

<a id="googleGetCitationFormatsForAScholarPaper"></a>
# **googleGetCitationFormatsForAScholarPaper**
> Object googleGetCitationFormatsForAScholarPaper(q, hl)

Get citation formats for a Scholar paper

Return MLA, APA, Chicago, Harvard, and Vancouver citation formats for a paper.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.GoogleApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    GoogleApi apiInstance = new GoogleApi(defaultClient);
    String q = "q_example"; // String | Cluster ID from a search result
    String hl = "en"; // String | Language code
    try {
      Object result = apiInstance.googleGetCitationFormatsForAScholarPaper(q, hl);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GoogleApi#googleGetCitationFormatsForAScholarPaper");
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
| **q** | **String**| Cluster ID from a search result | |
| **hl** | **String**| Language code | [optional] [default to en] |

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

<a id="googleGetPlaceDetails"></a>
# **googleGetPlaceDetails**
> Object googleGetPlaceDetails(placeId, dataId, hl, gl)

Get place details

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.GoogleApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    GoogleApi apiInstance = new GoogleApi(defaultClient);
    String placeId = "placeId_example"; // String | 
    String dataId = "dataId_example"; // String | 
    String hl = "en"; // String | 
    String gl = "us"; // String | 
    try {
      Object result = apiInstance.googleGetPlaceDetails(placeId, dataId, hl, gl);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GoogleApi#googleGetPlaceDetails");
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
| **placeId** | **String**|  | [optional] |
| **dataId** | **String**|  | [optional] |
| **hl** | **String**|  | [optional] [default to en] |
| **gl** | **String**|  | [optional] [default to us] |

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

<a id="googleGetPlacePhotos"></a>
# **googleGetPlacePhotos**
> Object googleGetPlacePhotos(dataId, hl, nextPageToken)

Get place photos

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.GoogleApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    GoogleApi apiInstance = new GoogleApi(defaultClient);
    String dataId = "dataId_example"; // String | Maps data ID
    String hl = "en"; // String | 
    String nextPageToken = "nextPageToken_example"; // String | 
    try {
      Object result = apiInstance.googleGetPlacePhotos(dataId, hl, nextPageToken);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GoogleApi#googleGetPlacePhotos");
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
| **dataId** | **String**| Maps data ID | |
| **hl** | **String**|  | [optional] [default to en] |
| **nextPageToken** | **String**|  | [optional] |

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

<a id="googleGetPlaceReviews"></a>
# **googleGetPlaceReviews**
> Object googleGetPlaceReviews(dataId, sortBy, hl, nextPageToken, results)

Get place reviews

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.GoogleApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    GoogleApi apiInstance = new GoogleApi(defaultClient);
    String dataId = "dataId_example"; // String | Maps data ID
    String sortBy = "qualityScore"; // String | qualityScore | newestFirst | ratingHigh | ratingLow
    String hl = "en"; // String | 
    String nextPageToken = "nextPageToken_example"; // String | Cursor from the previous response's pagination.next; omit for page 1.
    Integer results = 10; // Integer | 
    try {
      Object result = apiInstance.googleGetPlaceReviews(dataId, sortBy, hl, nextPageToken, results);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GoogleApi#googleGetPlaceReviews");
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
| **dataId** | **String**| Maps data ID | |
| **sortBy** | **String**| qualityScore | newestFirst | ratingHigh | ratingLow | [optional] [default to qualityScore] |
| **hl** | **String**|  | [optional] [default to en] |
| **nextPageToken** | **String**| Cursor from the previous response&#39;s pagination.next; omit for page 1. | [optional] |
| **results** | **Integer**|  | [optional] [default to 10] |

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

<a id="googleGetScholarAuthorProfile"></a>
# **googleGetScholarAuthorProfile**
> Object googleGetScholarAuthorProfile(authorId, hl, cstart, pagesize)

Get Scholar author profile

Get detailed Google Scholar author profile including articles, stats, co-authors.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.GoogleApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    GoogleApi apiInstance = new GoogleApi(defaultClient);
    String authorId = "authorId_example"; // String | Scholar user ID (the `user` query parameter)
    String hl = "en"; // String | Language code
    Integer cstart = 0; // Integer | Articles pagination offset
    Integer pagesize = 20; // Integer | Articles per page
    try {
      Object result = apiInstance.googleGetScholarAuthorProfile(authorId, hl, cstart, pagesize);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GoogleApi#googleGetScholarAuthorProfile");
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
| **authorId** | **String**| Scholar user ID (the &#x60;user&#x60; query parameter) | |
| **hl** | **String**| Language code | [optional] [default to en] |
| **cstart** | **Integer**| Articles pagination offset | [optional] [default to 0] |
| **pagesize** | **Integer**| Articles per page | [optional] [default to 20] |

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

<a id="googleGetStockIndexQuote"></a>
# **googleGetStockIndexQuote**
> Object googleGetStockIndexQuote(q, hl)

Get stock/index quote

Get a stock or index quote from Google Finance.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.GoogleApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    GoogleApi apiInstance = new GoogleApi(defaultClient);
    String q = "q_example"; // String | Ticker and exchange (e.g. \"AAPL:NASDAQ\", \"BTC-USD\")
    String hl = "en"; // String | Language code
    try {
      Object result = apiInstance.googleGetStockIndexQuote(q, hl);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GoogleApi#googleGetStockIndexQuote");
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
| **q** | **String**| Ticker and exchange (e.g. \&quot;AAPL:NASDAQ\&quot;, \&quot;BTC-USD\&quot;) | |
| **hl** | **String**| Language code | [optional] [default to en] |

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

<a id="googleGoogleAiModeSearch"></a>
# **googleGoogleAiModeSearch**
> Object googleGoogleAiModeSearch(q, gl, hl, includeHtml)

Google AI Mode search

Get AI-generated search results from Google AI Mode.  Returns the structured &#x60;text_blocks&#x60; (paragraphs, headings, comparison &#x60;table&#x60; blocks and lists), a flat &#x60;references&#x60; source list, a compact &#x60;markdown&#x60; rendering of the whole answer and — unless &#x60;include_html&#x60; is false — the raw &#x60;answer_html&#x60; body.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.GoogleApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    GoogleApi apiInstance = new GoogleApi(defaultClient);
    String q = "q_example"; // String | Search query for AI-generated response
    String gl = "us"; // String | Country code
    String hl = "en"; // String | Language code
    Boolean includeHtml = true; // Boolean | Include the raw `answer_html` (full answer body HTML) in the response for maximum parity. It can be 100s of KB — set false when you only need the structured `text_blocks` + `markdown`.
    try {
      Object result = apiInstance.googleGoogleAiModeSearch(q, gl, hl, includeHtml);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GoogleApi#googleGoogleAiModeSearch");
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
| **q** | **String**| Search query for AI-generated response | |
| **gl** | **String**| Country code | [optional] [default to us] |
| **hl** | **String**| Language code | [optional] [default to en] |
| **includeHtml** | **Boolean**| Include the raw &#x60;answer_html&#x60; (full answer body HTML) in the response for maximum parity. It can be 100s of KB — set false when you only need the structured &#x60;text_blocks&#x60; + &#x60;markdown&#x60;. | [optional] [default to true] |

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

<a id="googleGoogleAiOverviewInlineSerpBlock"></a>
# **googleGoogleAiOverviewInlineSerpBlock**
> Object googleGoogleAiOverviewInlineSerpBlock(q, gl, hl)

Google AI Overview (inline SERP block)

Get the AI Overview block Google renders inline at the top of a SERP.  Deferred overviews (where Google lazy-loads the block via a follow-up &#x60;&#x60;page_token&#x60;&#x60;) are chased automatically.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.GoogleApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    GoogleApi apiInstance = new GoogleApi(defaultClient);
    String q = "q_example"; // String | Search query — same shape as a Google Search query
    String gl = "us"; // String | Country code
    String hl = "en"; // String | Language code
    try {
      Object result = apiInstance.googleGoogleAiOverviewInlineSerpBlock(q, gl, hl);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GoogleApi#googleGoogleAiOverviewInlineSerpBlock");
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
| **q** | **String**| Search query — same shape as a Google Search query | |
| **gl** | **String**| Country code | [optional] [default to us] |
| **hl** | **String**| Language code | [optional] [default to en] |

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

<a id="googleGoogleFlightsCalendarCheapestFarePerDate"></a>
# **googleGoogleFlightsCalendarCheapestFarePerDate**
> Object googleGoogleFlightsCalendarCheapestFarePerDate(departureId, arrivalId, outboundDateFrom, outboundDateTo, tripType, tripLengthDays, returnDateFrom, returnDateTo, adults, children, infantsInSeat, infantsOnLap, travelClass, currency, gl, hl)

Google Flights calendar — cheapest fare per date

Price a whole range of dates in one call — up to 200 dates per request.  Google Flights&#39; own price graph / date grid: the cheapest fare per departure date instead of one search per date. Prices match &#x60;/flights/search&#x60; exactly.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.GoogleApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    GoogleApi apiInstance = new GoogleApi(defaultClient);
    String departureId = "departureId_example"; // String | Departure airport IATA code or location ID
    String arrivalId = "arrivalId_example"; // String | Arrival airport IATA code or location ID
    String outboundDateFrom = "outboundDateFrom_example"; // String | First outbound date to price (YYYY-MM-DD)
    String outboundDateTo = "outboundDateTo_example"; // String | Last outbound date to price (YYYY-MM-DD). At most 200 days from outbound_date_from, or 14 in date-grid mode.
    String tripType = "one_way"; // String | one_way | round_trip
    Integer tripLengthDays = 56; // Integer | Round-trip stay length in nights (price-graph mode). Defaults to 7.
    String returnDateFrom = "returnDateFrom_example"; // String | Date-grid mode: first return date. With return_date_to, returns the full outbound x return matrix (each range at most 14 days). Round-trip only.
    String returnDateTo = "returnDateTo_example"; // String | Date-grid mode: last return date
    Integer adults = 1; // Integer | 
    Integer children = 0; // Integer | 
    Integer infantsInSeat = 0; // Integer | 
    Integer infantsOnLap = 0; // Integer | 
    String travelClass = "economy"; // String | 
    String currency = "USD"; // String | ISO-4217 currency
    String gl = "us"; // String | 
    String hl = "en"; // String | 
    try {
      Object result = apiInstance.googleGoogleFlightsCalendarCheapestFarePerDate(departureId, arrivalId, outboundDateFrom, outboundDateTo, tripType, tripLengthDays, returnDateFrom, returnDateTo, adults, children, infantsInSeat, infantsOnLap, travelClass, currency, gl, hl);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GoogleApi#googleGoogleFlightsCalendarCheapestFarePerDate");
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
| **departureId** | **String**| Departure airport IATA code or location ID | |
| **arrivalId** | **String**| Arrival airport IATA code or location ID | |
| **outboundDateFrom** | **String**| First outbound date to price (YYYY-MM-DD) | |
| **outboundDateTo** | **String**| Last outbound date to price (YYYY-MM-DD). At most 200 days from outbound_date_from, or 14 in date-grid mode. | |
| **tripType** | **String**| one_way | round_trip | [optional] [default to one_way] |
| **tripLengthDays** | **Integer**| Round-trip stay length in nights (price-graph mode). Defaults to 7. | [optional] |
| **returnDateFrom** | **String**| Date-grid mode: first return date. With return_date_to, returns the full outbound x return matrix (each range at most 14 days). Round-trip only. | [optional] |
| **returnDateTo** | **String**| Date-grid mode: last return date | [optional] |
| **adults** | **Integer**|  | [optional] [default to 1] |
| **children** | **Integer**|  | [optional] [default to 0] |
| **infantsInSeat** | **Integer**|  | [optional] [default to 0] |
| **infantsOnLap** | **Integer**|  | [optional] [default to 0] |
| **travelClass** | **String**|  | [optional] [default to economy] |
| **currency** | **String**| ISO-4217 currency | [optional] [default to USD] |
| **gl** | **String**|  | [optional] [default to us] |
| **hl** | **String**|  | [optional] [default to en] |

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

<a id="googleGoogleFlightsSearch"></a>
# **googleGoogleFlightsSearch**
> Object googleGoogleFlightsSearch(departureId, arrivalId, outboundDate, returnDate, tripType, adults, children, infantsInSeat, infantsOnLap, travelClass, currency, gl, hl, stops, maxPrice, departureToken)

Google Flights search

Search Google Flights for available itineraries.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.GoogleApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    GoogleApi apiInstance = new GoogleApi(defaultClient);
    String departureId = "departureId_example"; // String | Departure airport IATA code or location ID
    String arrivalId = "arrivalId_example"; // String | Arrival airport IATA code or location ID
    String outboundDate = "outboundDate_example"; // String | Outbound date (YYYY-MM-DD)
    String returnDate = "returnDate_example"; // String | Return date (round-trip only)
    String tripType = "round_trip"; // String | round_trip | one_way | multi_city
    Integer adults = 1; // Integer | 
    Integer children = 0; // Integer | 
    Integer infantsInSeat = 0; // Integer | 
    Integer infantsOnLap = 0; // Integer | 
    String travelClass = "economy"; // String | 
    String currency = "USD"; // String | ISO-4217 currency
    String gl = "us"; // String | 
    String hl = "en"; // String | 
    String stops = "any"; // String | 
    Integer maxPrice = 56; // Integer | 
    String departureToken = "departureToken_example"; // String | A round-trip offer's departure_token; returns the return-leg flights for that selected outbound (round-trip only).
    try {
      Object result = apiInstance.googleGoogleFlightsSearch(departureId, arrivalId, outboundDate, returnDate, tripType, adults, children, infantsInSeat, infantsOnLap, travelClass, currency, gl, hl, stops, maxPrice, departureToken);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GoogleApi#googleGoogleFlightsSearch");
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
| **departureId** | **String**| Departure airport IATA code or location ID | |
| **arrivalId** | **String**| Arrival airport IATA code or location ID | |
| **outboundDate** | **String**| Outbound date (YYYY-MM-DD) | |
| **returnDate** | **String**| Return date (round-trip only) | [optional] |
| **tripType** | **String**| round_trip | one_way | multi_city | [optional] [default to round_trip] |
| **adults** | **Integer**|  | [optional] [default to 1] |
| **children** | **Integer**|  | [optional] [default to 0] |
| **infantsInSeat** | **Integer**|  | [optional] [default to 0] |
| **infantsOnLap** | **Integer**|  | [optional] [default to 0] |
| **travelClass** | **String**|  | [optional] [default to economy] |
| **currency** | **String**| ISO-4217 currency | [optional] [default to USD] |
| **gl** | **String**|  | [optional] [default to us] |
| **hl** | **String**|  | [optional] [default to en] |
| **stops** | **String**|  | [optional] [default to any] |
| **maxPrice** | **Integer**|  | [optional] |
| **departureToken** | **String**| A round-trip offer&#39;s departure_token; returns the return-leg flights for that selected outbound (round-trip only). | [optional] |

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

<a id="googleGoogleLensVisualSearch"></a>
# **googleGoogleLensVisualSearch**
> Object googleGoogleLensVisualSearch(url, query, country, language, gl, hl, product, visualMatches, exactMatches)

Google Lens visual search

Google Lens visual search.  Response carries &#x60;&#x60;lens_results&#x60;&#x60; (Scrapingdog parity alias) with &#x60;&#x60;title&#x60;&#x60; / &#x60;&#x60;source&#x60;&#x60; / &#x60;&#x60;source_favicon&#x60;&#x60; / &#x60;&#x60;thumbnail&#x60;&#x60; / &#x60;&#x60;original_thumbnail&#x60;&#x60; / &#x60;&#x60;rating&#x60;&#x60; / &#x60;&#x60;reviews&#x60;&#x60; / &#x60;&#x60;in_stock&#x60;&#x60;, plus &#x60;&#x60;price&#x60;&#x60; (&#x60;&#x60;{value, currency, extracted}&#x60;&#x60;) and the raw &#x60;&#x60;tag&#x60;&#x60; chip it is parsed from, on shoppable matches. &#x60;&#x60;related_searches&#x60;&#x60; chips come alongside. Legacy &#x60;&#x60;results&#x60;&#x60; alias kept for backwards compat.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.GoogleApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    GoogleApi apiInstance = new GoogleApi(defaultClient);
    String url = "url_example"; // String | Public URL of the image to search visually
    String query = "query_example"; // String | Optional text refinement (e.g. 'pizza')
    String country = "country_example"; // String | ISO country code (alias for gl)
    String language = "language_example"; // String | Language code (alias for hl)
    String gl = "us"; // String | Country code
    String hl = "en"; // String | Language code
    Boolean product = false; // Boolean | Bias towards shoppable product matches
    Boolean visualMatches = true; // Boolean | Include the visual-matches carousel
    Boolean exactMatches = false; // Boolean | Restrict to exact-match results
    try {
      Object result = apiInstance.googleGoogleLensVisualSearch(url, query, country, language, gl, hl, product, visualMatches, exactMatches);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GoogleApi#googleGoogleLensVisualSearch");
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
| **url** | **String**| Public URL of the image to search visually | |
| **query** | **String**| Optional text refinement (e.g. &#39;pizza&#39;) | [optional] |
| **country** | **String**| ISO country code (alias for gl) | [optional] |
| **language** | **String**| Language code (alias for hl) | [optional] |
| **gl** | **String**| Country code | [optional] [default to us] |
| **hl** | **String**| Language code | [optional] [default to en] |
| **product** | **Boolean**| Bias towards shoppable product matches | [optional] [default to false] |
| **visualMatches** | **Boolean**| Include the visual-matches carousel | [optional] [default to true] |
| **exactMatches** | **Boolean**| Restrict to exact-match results | [optional] [default to false] |

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

<a id="googleGoogleScraperHealthCheck"></a>
# **googleGoogleScraperHealthCheck**
> Object googleGoogleScraperHealthCheck()

Google scraper health check

Check health of the Google scraper service.  Accepts &#x60;&#x60;HEAD&#x60;&#x60; so external uptime checkers (UptimeRobot uses HEAD by default for HTTP monitors) don&#39;t get a 405 Method Not Allowed.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.GoogleApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    GoogleApi apiInstance = new GoogleApi(defaultClient);
    try {
      Object result = apiInstance.googleGoogleScraperHealthCheck();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GoogleApi#googleGoogleScraperHealthCheck");
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

<a id="googleGoogleScraperHealthCheckHead"></a>
# **googleGoogleScraperHealthCheckHead**
> Object googleGoogleScraperHealthCheckHead()

Google scraper health check

Check health of the Google scraper service.  Accepts &#x60;&#x60;HEAD&#x60;&#x60; so external uptime checkers (UptimeRobot uses HEAD by default for HTTP monitors) don&#39;t get a 405 Method Not Allowed.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.GoogleApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    GoogleApi apiInstance = new GoogleApi(defaultClient);
    try {
      Object result = apiInstance.googleGoogleScraperHealthCheckHead();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GoogleApi#googleGoogleScraperHealthCheckHead");
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

<a id="googleGoogleSearchSuggestions"></a>
# **googleGoogleSearchSuggestions**
> Object googleGoogleSearchSuggestions(q, hl, gl)

Google search suggestions

Get Google search autocomplete suggestions.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.GoogleApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    GoogleApi apiInstance = new GoogleApi(defaultClient);
    String q = "q_example"; // String | Search query to get suggestions for
    String hl = "en"; // String | Language code
    String gl = "us"; // String | Country code
    try {
      Object result = apiInstance.googleGoogleSearchSuggestions(q, hl, gl);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GoogleApi#googleGoogleSearchSuggestions");
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
| **q** | **String**| Search query to get suggestions for | |
| **hl** | **String**| Language code | [optional] [default to en] |
| **gl** | **String**| Country code | [optional] [default to us] |

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

<a id="googleGoogleShortsSearch"></a>
# **googleGoogleShortsSearch**
> Object googleGoogleShortsSearch(q, gl, hl, domain, num, start)

Google Shorts search

Return short-form video results (YouTube Shorts, TikToks) from Google Shorts mode.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.GoogleApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    GoogleApi apiInstance = new GoogleApi(defaultClient);
    String q = "q_example"; // String | Search query
    String gl = "us"; // String | Country code
    String hl = "en"; // String | Language code
    String domain = "google.com"; // String | Google domain
    Integer num = 20; // Integer | Results per page
    Integer start = 0; // Integer | Pagination offset
    try {
      Object result = apiInstance.googleGoogleShortsSearch(q, gl, hl, domain, num, start);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GoogleApi#googleGoogleShortsSearch");
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
| **q** | **String**| Search query | |
| **gl** | **String**| Country code | [optional] [default to us] |
| **hl** | **String**| Language code | [optional] [default to en] |
| **domain** | **String**| Google domain | [optional] [default to google.com] |
| **num** | **Integer**| Results per page | [optional] [default to 20] |
| **start** | **Integer**| Pagination offset | [optional] [default to 0] |

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

<a id="googleGoogleWebSearch"></a>
# **googleGoogleWebSearch**
> Object googleGoogleWebSearch(q, gl, hl, num, start, domain, device, userAgent, output, location, lr, tbs, safe, uule, filter, nfpr, cr, ludocid, lsig, kgmid, si, ibp, uds, aiOverview)

Google web search

Search Google and get structured results (organic, ads, KG, AI overview, PAA).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.GoogleApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    GoogleApi apiInstance = new GoogleApi(defaultClient);
    String q = "q_example"; // String | Search query (supports Google operators)
    String gl = "us"; // String | Country code
    String hl = "en"; // String | Language code
    Integer num = 10; // Integer | 
    Integer start = 0; // Integer | Page offset (0, 10, 20...)
    String domain = "google.com"; // String | Google domain
    String device = "desktop"; // String | Device target: desktop, mobile, iphone, android, tablet
    String userAgent = "userAgent_example"; // String | Custom User-Agent (overrides device)
    String output = "json"; // String | Response format: json (parsed) or html (raw SERP)
    String location = "location_example"; // String | City-level geo-targeting
    String lr = "lr_example"; // String | Language restrict (e.g. lang_en)
    String tbs = "tbs_example"; // String | Time filter (e.g. qdr:d)
    String safe = "off"; // String | 
    String uule = "uule_example"; // String | UULE encoded location
    Integer filter = 56; // Integer | Show omitted results
    Integer nfpr = 0; // Integer | Disable auto-correction
    String cr = "cr_example"; // String | Country restrict
    String ludocid = "ludocid_example"; // String | Google Place CID
    String lsig = "lsig_example"; // String | Knowledge Graph map ID
    String kgmid = "kgmid_example"; // String | Knowledge Graph entity ID
    String si = "si_example"; // String | Cached search params
    String ibp = "ibp_example"; // String | Layout control
    String uds = "uds_example"; // String | Google filter string
    Boolean aiOverview = false; // Boolean | Chase deferred AI Overview page_token with a follow-up fetch and merge the result. Adds ~1s and 1 credit when the SERP defers the overview.
    try {
      Object result = apiInstance.googleGoogleWebSearch(q, gl, hl, num, start, domain, device, userAgent, output, location, lr, tbs, safe, uule, filter, nfpr, cr, ludocid, lsig, kgmid, si, ibp, uds, aiOverview);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GoogleApi#googleGoogleWebSearch");
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
| **q** | **String**| Search query (supports Google operators) | |
| **gl** | **String**| Country code | [optional] [default to us] |
| **hl** | **String**| Language code | [optional] [default to en] |
| **num** | **Integer**|  | [optional] [default to 10] |
| **start** | **Integer**| Page offset (0, 10, 20...) | [optional] [default to 0] |
| **domain** | **String**| Google domain | [optional] [default to google.com] |
| **device** | **String**| Device target: desktop, mobile, iphone, android, tablet | [optional] [default to desktop] [enum: desktop, mobile, iphone, android, tablet] |
| **userAgent** | **String**| Custom User-Agent (overrides device) | [optional] |
| **output** | **String**| Response format: json (parsed) or html (raw SERP) | [optional] [default to json] [enum: json, html] |
| **location** | **String**| City-level geo-targeting | [optional] |
| **lr** | **String**| Language restrict (e.g. lang_en) | [optional] |
| **tbs** | **String**| Time filter (e.g. qdr:d) | [optional] |
| **safe** | **String**|  | [optional] [default to off] |
| **uule** | **String**| UULE encoded location | [optional] |
| **filter** | **Integer**| Show omitted results | [optional] |
| **nfpr** | **Integer**| Disable auto-correction | [optional] [default to 0] |
| **cr** | **String**| Country restrict | [optional] |
| **ludocid** | **String**| Google Place CID | [optional] |
| **lsig** | **String**| Knowledge Graph map ID | [optional] |
| **kgmid** | **String**| Knowledge Graph entity ID | [optional] |
| **si** | **String**| Cached search params | [optional] |
| **ibp** | **String**| Layout control | [optional] |
| **uds** | **String**| Google filter string | [optional] |
| **aiOverview** | **Boolean**| Chase deferred AI Overview page_token with a follow-up fetch and merge the result. Adds ~1s and 1 credit when the SERP defers the overview. | [optional] [default to false] |

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

<a id="googleHotelDetails"></a>
# **googleHotelDetails**
> Object googleHotelDetails(propertyToken, checkIn, checkOut)

Hotel details

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.GoogleApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    GoogleApi apiInstance = new GoogleApi(defaultClient);
    String propertyToken = "propertyToken_example"; // String | Property token
    String checkIn = "checkIn_example"; // String | YYYY-MM-DD
    String checkOut = "checkOut_example"; // String | YYYY-MM-DD
    try {
      Object result = apiInstance.googleHotelDetails(propertyToken, checkIn, checkOut);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GoogleApi#googleHotelDetails");
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
| **propertyToken** | **String**| Property token | |
| **checkIn** | **String**| YYYY-MM-DD | |
| **checkOut** | **String**| YYYY-MM-DD | |

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

<a id="googleImmersiveProductDetail"></a>
# **googleImmersiveProductDetail**
> Object googleImmersiveProductDetail(productId, q, gl, hl, catalogId, imageDocid, headlineOfferDocid, mid, includeOffers, includeVariants)

Immersive product detail

Get deep product details from Google&#39;s immersive product page.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.GoogleApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    GoogleApi apiInstance = new GoogleApi(defaultClient);
    String productId = "productId_example"; // String | Google Shopping ``gpcid`` — the product_id returned on ``/shopping/search`` tiles. Scrapingdog-compatible.
    String q = "q_example"; // String | Original search query that surfaced the product. Required by Google's ``/async/oapv`` RPC.
    String gl = "us"; // String | Country code (ISO 3166 alpha-2)
    String hl = "en"; // String | Language code
    String catalogId = "catalogId_example"; // String | Optional ``catalogid`` from the Shopping tile (improves parity).
    String imageDocid = "imageDocid_example"; // String | Optional ``imageDocid`` for higher-fidelity images.
    String headlineOfferDocid = "headlineOfferDocid_example"; // String | Optional ``headlineOfferDocid`` to pin the featured seller.
    String mid = "mid_example"; // String | Optional Google Knowledge-Graph ``mid``.
    Boolean includeOffers = false; // Boolean | When true, fetch the full merchant-offer list via a secondary RPC (``/async/piu_ps``). Adds ~1 s.
    Boolean includeVariants = false; // Boolean | When true, fetch size/colour variants via a secondary RPC (``/async/toy_v``). Adds ~1 s.
    try {
      Object result = apiInstance.googleImmersiveProductDetail(productId, q, gl, hl, catalogId, imageDocid, headlineOfferDocid, mid, includeOffers, includeVariants);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GoogleApi#googleImmersiveProductDetail");
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
| **productId** | **String**| Google Shopping &#x60;&#x60;gpcid&#x60;&#x60; — the product_id returned on &#x60;&#x60;/shopping/search&#x60;&#x60; tiles. Scrapingdog-compatible. | |
| **q** | **String**| Original search query that surfaced the product. Required by Google&#39;s &#x60;&#x60;/async/oapv&#x60;&#x60; RPC. | |
| **gl** | **String**| Country code (ISO 3166 alpha-2) | [optional] [default to us] |
| **hl** | **String**| Language code | [optional] [default to en] |
| **catalogId** | **String**| Optional &#x60;&#x60;catalogid&#x60;&#x60; from the Shopping tile (improves parity). | [optional] |
| **imageDocid** | **String**| Optional &#x60;&#x60;imageDocid&#x60;&#x60; for higher-fidelity images. | [optional] |
| **headlineOfferDocid** | **String**| Optional &#x60;&#x60;headlineOfferDocid&#x60;&#x60; to pin the featured seller. | [optional] |
| **mid** | **String**| Optional Google Knowledge-Graph &#x60;&#x60;mid&#x60;&#x60;. | [optional] |
| **includeOffers** | **Boolean**| When true, fetch the full merchant-offer list via a secondary RPC (&#x60;&#x60;/async/piu_ps&#x60;&#x60;). Adds ~1 s. | [optional] [default to false] |
| **includeVariants** | **Boolean**| When true, fetch size/colour variants via a secondary RPC (&#x60;&#x60;/async/toy_v&#x60;&#x60;). Adds ~1 s. | [optional] [default to false] |

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

<a id="googleInterestByRegion"></a>
# **googleInterestByRegion**
> Object googleInterestByRegion(q, geo)

Interest by region

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.GoogleApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    GoogleApi apiInstance = new GoogleApi(defaultClient);
    String q = "q_example"; // String | Search term
    String geo = ""; // String | 
    try {
      Object result = apiInstance.googleInterestByRegion(q, geo);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GoogleApi#googleInterestByRegion");
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
| **q** | **String**| Search term | |
| **geo** | **String**|  | [optional] [default to ] |

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

<a id="googleInterestOverTime"></a>
# **googleInterestOverTime**
> Object googleInterestOverTime(q, geo, date)

Interest over time

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.GoogleApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    GoogleApi apiInstance = new GoogleApi(defaultClient);
    String q = "q_example"; // String | Search terms
    String geo = ""; // String | 
    String date = "today 12-m"; // String | 
    try {
      Object result = apiInstance.googleInterestOverTime(q, geo, date);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GoogleApi#googleInterestOverTime");
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
| **q** | **String**| Search terms | |
| **geo** | **String**|  | [optional] [default to ] |
| **date** | **String**|  | [optional] [default to today 12-m] |

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

<a id="googleMultiSellerOffersByBarcode"></a>
# **googleMultiSellerOffersByBarcode**
> Object googleMultiSellerOffersByBarcode(barcode, gl, hl)

Multi-seller offers by barcode

Resolve a barcode to a product via Google web search, then return its Google Shopping seller offers (source + price per merchant).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.GoogleApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    GoogleApi apiInstance = new GoogleApi(defaultClient);
    String barcode = "barcode_example"; // String | Product barcode — GTIN-8 / UPC-A / EAN-13 / GTIN-14
    String gl = "gl_example"; // String | Country code (ISO 3166 alpha-2)
    String hl = "en"; // String | Language code
    try {
      Object result = apiInstance.googleMultiSellerOffersByBarcode(barcode, gl, hl);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GoogleApi#googleMultiSellerOffersByBarcode");
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
| **barcode** | **String**| Product barcode — GTIN-8 / UPC-A / EAN-13 / GTIN-14 | |
| **gl** | **String**| Country code (ISO 3166 alpha-2) | [optional] |
| **hl** | **String**| Language code | [optional] [default to en] |

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

<a id="googleNewsByTopic"></a>
# **googleNewsByTopic**
> Object googleNewsByTopic(topic, hl, gl, maxResults)

News by topic

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.GoogleApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    GoogleApi apiInstance = new GoogleApi(defaultClient);
    String topic = "topic_example"; // String | Topic name
    String hl = "en"; // String | 
    String gl = "US"; // String | 
    Integer maxResults = 10; // Integer | 
    try {
      Object result = apiInstance.googleNewsByTopic(topic, hl, gl, maxResults);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GoogleApi#googleNewsByTopic");
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
| **topic** | **String**| Topic name | |
| **hl** | **String**|  | [optional] [default to en] |
| **gl** | **String**|  | [optional] [default to US] |
| **maxResults** | **Integer**|  | [optional] [default to 10] |

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

<a id="googlePatentDetails"></a>
# **googlePatentDetails**
> Object googlePatentDetails(patentId)

Patent details

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.GoogleApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    GoogleApi apiInstance = new GoogleApi(defaultClient);
    String patentId = "patentId_example"; // String | Patent number
    try {
      Object result = apiInstance.googlePatentDetails(patentId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GoogleApi#googlePatentDetails");
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
| **patentId** | **String**| Patent number | |

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

<a id="googleRelatedTopicsQueries"></a>
# **googleRelatedTopicsQueries**
> Object googleRelatedTopicsQueries(q, geo)

Related topics &amp; queries

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.GoogleApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    GoogleApi apiInstance = new GoogleApi(defaultClient);
    String q = "q_example"; // String | Search term
    String geo = ""; // String | 
    try {
      Object result = apiInstance.googleRelatedTopicsQueries(q, geo);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GoogleApi#googleRelatedTopicsQueries");
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
| **q** | **String**| Search term | |
| **geo** | **String**|  | [optional] [default to ] |

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

<a id="googleSearchGoogleImages"></a>
# **googleSearchGoogleImages**
> Object googleSearchGoogleImages(q, gl, hl, tbs, imgsz, imgcolor, imgtype, safe, page)

Search Google Images

Search Google Images for visual content.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.GoogleApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    GoogleApi apiInstance = new GoogleApi(defaultClient);
    String q = "q_example"; // String | Image search query
    String gl = "us"; // String | Country code
    String hl = "en"; // String | Language code
    String tbs = "tbs_example"; // String | Time/filter string (e.g. qdr:d)
    String imgsz = "imgsz_example"; // String | Image size: l, m, i, xXl
    String imgcolor = "imgcolor_example"; // String | Image color filter
    String imgtype = "imgtype_example"; // String | Image type: face, photo, clipart
    String safe = "off"; // String | Safe search
    Integer page = 0; // Integer | Page number
    try {
      Object result = apiInstance.googleSearchGoogleImages(q, gl, hl, tbs, imgsz, imgcolor, imgtype, safe, page);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GoogleApi#googleSearchGoogleImages");
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
| **q** | **String**| Image search query | |
| **gl** | **String**| Country code | [optional] [default to us] |
| **hl** | **String**| Language code | [optional] [default to en] |
| **tbs** | **String**| Time/filter string (e.g. qdr:d) | [optional] |
| **imgsz** | **String**| Image size: l, m, i, xXl | [optional] |
| **imgcolor** | **String**| Image color filter | [optional] |
| **imgtype** | **String**| Image type: face, photo, clipart | [optional] |
| **safe** | **String**| Safe search | [optional] [default to off] |
| **page** | **Integer**| Page number | [optional] [default to 0] |

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

<a id="googleSearchGoogleJobs"></a>
# **googleSearchGoogleJobs**
> Object googleSearchGoogleJobs(q, location, gl, jobType, datePosted)

Search Google Jobs

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.GoogleApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    GoogleApi apiInstance = new GoogleApi(defaultClient);
    String q = "q_example"; // String | Job title, keywords
    String location = "location_example"; // String | 
    String gl = "us"; // String | 
    String jobType = "jobType_example"; // String | 
    String datePosted = "datePosted_example"; // String | 
    try {
      Object result = apiInstance.googleSearchGoogleJobs(q, location, gl, jobType, datePosted);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GoogleApi#googleSearchGoogleJobs");
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
| **q** | **String**| Job title, keywords | |
| **location** | **String**|  | [optional] |
| **gl** | **String**|  | [optional] [default to us] |
| **jobType** | **String**|  | [optional] |
| **datePosted** | **String**|  | [optional] |

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

<a id="googleSearchGoogleMapsPlaces"></a>
# **googleSearchGoogleMapsPlaces**
> Object googleSearchGoogleMapsPlaces(q, ll, gl, hl, start)

Search Google Maps places

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.GoogleApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    GoogleApi apiInstance = new GoogleApi(defaultClient);
    String q = "q_example"; // String | Search query
    String ll = "ll_example"; // String | 
    String gl = "us"; // String | 
    String hl = "en"; // String | 
    Integer start = 0; // Integer | 
    try {
      Object result = apiInstance.googleSearchGoogleMapsPlaces(q, ll, gl, hl, start);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GoogleApi#googleSearchGoogleMapsPlaces");
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
| **q** | **String**| Search query | |
| **ll** | **String**|  | [optional] |
| **gl** | **String**|  | [optional] [default to us] |
| **hl** | **String**|  | [optional] [default to en] |
| **start** | **Integer**|  | [optional] [default to 0] |

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

<a id="googleSearchGoogleNews"></a>
# **googleSearchGoogleNews**
> Object googleSearchGoogleNews(q, hl, gl, maxResults)

Search Google News

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.GoogleApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    GoogleApi apiInstance = new GoogleApi(defaultClient);
    String q = "q_example"; // String | Search query
    String hl = "en"; // String | 
    String gl = "US"; // String | 
    Integer maxResults = 10; // Integer | 
    try {
      Object result = apiInstance.googleSearchGoogleNews(q, hl, gl, maxResults);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GoogleApi#googleSearchGoogleNews");
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
| **q** | **String**| Search query | |
| **hl** | **String**|  | [optional] [default to en] |
| **gl** | **String**|  | [optional] [default to US] |
| **maxResults** | **Integer**|  | [optional] [default to 10] |

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

<a id="googleSearchGoogleScholar"></a>
# **googleSearchGoogleScholar**
> Object googleSearchGoogleScholar(q, hl, asYlo, asYhi, asSdt, page, num)

Search Google Scholar

Search Google Scholar for scholarly articles.  Each result ships with its doc &#x60;&#x60;id&#x60;&#x60;, &#x60;&#x60;type&#x60;&#x60; badge ([BOOK]/[PDF]/...), wrapped &#x60;&#x60;inline_links&#x60;&#x60; (versions + cited_by + related), PDF &#x60;&#x60;resources&#x60;&#x60; list, and structured &#x60;&#x60;authors&#x60;&#x60; (with &#x60;&#x60;author_id&#x60;&#x60; for profiled authors — pipe straight into &#x60;&#x60;/scholar/author&#x60;&#x60;). Envelope carries &#x60;&#x60;scholar_results&#x60;&#x60; alias (Scrapingdog parity), &#x60;&#x60;related_searches&#x60;&#x60;, and matched &#x60;&#x60;profiles&#x60;&#x60; cards.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.GoogleApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    GoogleApi apiInstance = new GoogleApi(defaultClient);
    String q = "q_example"; // String | Search query for scholarly articles
    String hl = "en"; // String | Language code
    Integer asYlo = 56; // Integer | Year from (e.g. 2020)
    Integer asYhi = 56; // Integer | Year to (e.g. 2024)
    String asSdt = "0"; // String | Search type: 0=exclude patents, 7=include
    Integer page = 0; // Integer | Page number (0-based)
    Integer num = 10; // Integer | Results per page (max 20)
    try {
      Object result = apiInstance.googleSearchGoogleScholar(q, hl, asYlo, asYhi, asSdt, page, num);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GoogleApi#googleSearchGoogleScholar");
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
| **q** | **String**| Search query for scholarly articles | |
| **hl** | **String**| Language code | [optional] [default to en] |
| **asYlo** | **Integer**| Year from (e.g. 2020) | [optional] |
| **asYhi** | **Integer**| Year to (e.g. 2024) | [optional] |
| **asSdt** | **String**| Search type: 0&#x3D;exclude patents, 7&#x3D;include | [optional] [default to 0] |
| **page** | **Integer**| Page number (0-based) | [optional] [default to 0] |
| **num** | **Integer**| Results per page (max 20) | [optional] [default to 10] |

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

<a id="googleSearchGoogleVideos"></a>
# **googleSearchGoogleVideos**
> Object googleSearchGoogleVideos(q, gl, hl, tbs, safe, page)

Search Google Videos

Search Google for video results.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.GoogleApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    GoogleApi apiInstance = new GoogleApi(defaultClient);
    String q = "q_example"; // String | Video search query
    String gl = "us"; // String | Country code
    String hl = "en"; // String | Language code
    String tbs = "tbs_example"; // String | Time filter (e.g. qdr:d)
    String safe = "off"; // String | Safe search
    Integer page = 0; // Integer | Page number
    try {
      Object result = apiInstance.googleSearchGoogleVideos(q, gl, hl, tbs, safe, page);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GoogleApi#googleSearchGoogleVideos");
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
| **q** | **String**| Video search query | |
| **gl** | **String**| Country code | [optional] [default to us] |
| **hl** | **String**| Language code | [optional] [default to en] |
| **tbs** | **String**| Time filter (e.g. qdr:d) | [optional] |
| **safe** | **String**| Safe search | [optional] [default to off] |
| **page** | **Integer**| Page number | [optional] [default to 0] |

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

<a id="googleSearchHotels"></a>
# **googleSearchHotels**
> Object googleSearchHotels(q, checkIn, checkOut, adults, currency, gl)

Search hotels

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.GoogleApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    GoogleApi apiInstance = new GoogleApi(defaultClient);
    String q = "q_example"; // String | Location or hotel name
    String checkIn = "checkIn_example"; // String | YYYY-MM-DD
    String checkOut = "checkOut_example"; // String | YYYY-MM-DD
    Integer adults = 2; // Integer | 
    String currency = "USD"; // String | 
    String gl = "us"; // String | 
    try {
      Object result = apiInstance.googleSearchHotels(q, checkIn, checkOut, adults, currency, gl);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GoogleApi#googleSearchHotels");
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
| **q** | **String**| Location or hotel name | |
| **checkIn** | **String**| YYYY-MM-DD | |
| **checkOut** | **String**| YYYY-MM-DD | |
| **adults** | **Integer**|  | [optional] [default to 2] |
| **currency** | **String**|  | [optional] [default to USD] |
| **gl** | **String**|  | [optional] [default to us] |

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

<a id="googleSearchPatents"></a>
# **googleSearchPatents**
> Object googleSearchPatents(q, page, num, sort, inventor, assignee, country, language, status, patentType, before, after)

Search patents

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.GoogleApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    GoogleApi apiInstance = new GoogleApi(defaultClient);
    String q = "q_example"; // String | Search query (Boolean logic supported)
    Integer page = 0; // Integer | 
    Integer num = 10; // Integer | 
    String sort = "sort_example"; // String | 'new' or 'old'
    String inventor = "inventor_example"; // String | Inventor name(s)
    String assignee = "assignee_example"; // String | Assignee / company name(s)
    String country = "country_example"; // String | Country code (US, EP, WO, …)
    String language = "language_example"; // String | Patent language: ENGLISH, GERMAN, CHINESE, FRENCH, JAPANESE, KOREAN, SPANISH
    String status = "status_example"; // String | GRANT or APPLICATION
    String patentType = "patentType_example"; // String | PATENT or DESIGN
    String before = "before_example"; // String | Before date YYYYMMDD
    String after = "after_example"; // String | After date YYYYMMDD
    try {
      Object result = apiInstance.googleSearchPatents(q, page, num, sort, inventor, assignee, country, language, status, patentType, before, after);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GoogleApi#googleSearchPatents");
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
| **q** | **String**| Search query (Boolean logic supported) | |
| **page** | **Integer**|  | [optional] [default to 0] |
| **num** | **Integer**|  | [optional] [default to 10] |
| **sort** | **String**| &#39;new&#39; or &#39;old&#39; | [optional] |
| **inventor** | **String**| Inventor name(s) | [optional] |
| **assignee** | **String**| Assignee / company name(s) | [optional] |
| **country** | **String**| Country code (US, EP, WO, …) | [optional] |
| **language** | **String**| Patent language: ENGLISH, GERMAN, CHINESE, FRENCH, JAPANESE, KOREAN, SPANISH | [optional] |
| **status** | **String**| GRANT or APPLICATION | [optional] |
| **patentType** | **String**| PATENT or DESIGN | [optional] |
| **before** | **String**| Before date YYYYMMDD | [optional] |
| **after** | **String**| After date YYYYMMDD | [optional] |

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

<a id="googleSearchProducts"></a>
# **googleSearchProducts**
> Object googleSearchProducts(q, gl, minPrice, maxPrice, sortBy)

Search products

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.GoogleApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    GoogleApi apiInstance = new GoogleApi(defaultClient);
    String q = "q_example"; // String | Product search query
    String gl = "us"; // String | 
    Integer minPrice = 56; // Integer | 
    Integer maxPrice = 56; // Integer | 
    String sortBy = "sortBy_example"; // String | 
    try {
      Object result = apiInstance.googleSearchProducts(q, gl, minPrice, maxPrice, sortBy);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GoogleApi#googleSearchProducts");
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
| **q** | **String**| Product search query | |
| **gl** | **String**|  | [optional] [default to us] |
| **minPrice** | **Integer**|  | [optional] |
| **maxPrice** | **Integer**|  | [optional] |
| **sortBy** | **String**|  | [optional] |

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

<a id="googleSearchScholarAuthorProfiles"></a>
# **googleSearchScholarAuthorProfiles**
> Object googleSearchScholarAuthorProfiles(mauthors, hl, afterAuthor, beforeAuthor)

Search Scholar author profiles

Search Google Scholar for author profiles by name.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.GoogleApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    GoogleApi apiInstance = new GoogleApi(defaultClient);
    String mauthors = "mauthors_example"; // String | Author name query (e.g. 'Geoffrey Hinton')
    String hl = "en"; // String | Language code
    String afterAuthor = "afterAuthor_example"; // String | Pagination token (next page)
    String beforeAuthor = "beforeAuthor_example"; // String | Pagination token (previous page)
    try {
      Object result = apiInstance.googleSearchScholarAuthorProfiles(mauthors, hl, afterAuthor, beforeAuthor);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GoogleApi#googleSearchScholarAuthorProfiles");
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
| **mauthors** | **String**| Author name query (e.g. &#39;Geoffrey Hinton&#39;) | |
| **hl** | **String**| Language code | [optional] [default to en] |
| **afterAuthor** | **String**| Pagination token (next page) | [optional] |
| **beforeAuthor** | **String**| Pagination token (previous page) | [optional] |

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

<a id="googleTrendingNews"></a>
# **googleTrendingNews**
> Object googleTrendingNews(hl, gl, maxResults)

Trending news

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.GoogleApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    GoogleApi apiInstance = new GoogleApi(defaultClient);
    String hl = "en"; // String | 
    String gl = "US"; // String | 
    Integer maxResults = 10; // Integer | 
    try {
      Object result = apiInstance.googleTrendingNews(hl, gl, maxResults);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GoogleApi#googleTrendingNews");
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
| **hl** | **String**|  | [optional] [default to en] |
| **gl** | **String**|  | [optional] [default to US] |
| **maxResults** | **Integer**|  | [optional] [default to 10] |

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

<a id="googleTrendingSearches"></a>
# **googleTrendingSearches**
> Object googleTrendingSearches(geo)

Trending searches

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.GoogleApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    GoogleApi apiInstance = new GoogleApi(defaultClient);
    String geo = "US"; // String | 
    try {
      Object result = apiInstance.googleTrendingSearches(geo);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GoogleApi#googleTrendingSearches");
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
| **geo** | **String**|  | [optional] [default to US] |

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

<a id="googleTrendsTopicAutocomplete"></a>
# **googleTrendsTopicAutocomplete**
> Object googleTrendsTopicAutocomplete(q, hl, tz)

Trends topic autocomplete

Return categorized Knowledge Graph topic entities (mid, type) for a query.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.GoogleApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    GoogleApi apiInstance = new GoogleApi(defaultClient);
    String q = "q_example"; // String | Query prefix to resolve into Trends topics
    String hl = "en-US"; // String | Language code
    String tz = "0"; // String | Timezone offset in minutes
    try {
      Object result = apiInstance.googleTrendsTopicAutocomplete(q, hl, tz);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GoogleApi#googleTrendsTopicAutocomplete");
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
| **q** | **String**| Query prefix to resolve into Trends topics | |
| **hl** | **String**| Language code | [optional] [default to en-US] |
| **tz** | **String**| Timezone offset in minutes | [optional] [default to 0] |

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

