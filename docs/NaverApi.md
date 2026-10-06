# NaverApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**naverNaverBlogSearch**](NaverApi.md#naverNaverBlogSearch) | **GET** /v1/naver/blog | Naver blog search |
| [**naverNaverDatalabShoppingKeywordInsight**](NaverApi.md#naverNaverDatalabShoppingKeywordInsight) | **GET** /v1/naver/shopping/insight | Naver DataLab shopping keyword insight |
| [**naverNaverNewsSearch**](NaverApi.md#naverNaverNewsSearch) | **GET** /v1/naver/news | Naver news search |
| [**naverNaverPlaceDetail**](NaverApi.md#naverNaverPlaceDetail) | **GET** /v1/naver/place/{place_id} | Naver place detail |
| [**naverNaverPlaceLocalSearch**](NaverApi.md#naverNaverPlaceLocalSearch) | **GET** /v1/naver/local | Naver Place/Local search |
| [**naverNaverPlaceVisitorReviews**](NaverApi.md#naverNaverPlaceVisitorReviews) | **GET** /v1/naver/place/{place_id}/reviews | Naver place visitor reviews |
| [**naverNaverScraperHealthCheck**](NaverApi.md#naverNaverScraperHealthCheck) | **GET** /v1/naver/health | Naver scraper health check |
| [**naverNaverScraperHealthCheckHead**](NaverApi.md#naverNaverScraperHealthCheckHead) | **HEAD** /v1/naver/health | Naver scraper health check |
| [**naverNaverShoppingBestsellerRankings**](NaverApi.md#naverNaverShoppingBestsellerRankings) | **GET** /v1/naver/shopping/bestsellers | Naver Shopping bestseller rankings |
| [**naverNaverShoppingCategoryReference**](NaverApi.md#naverNaverShoppingCategoryReference) | **GET** /v1/naver/shopping/categories | Naver Shopping category reference |
| [**naverNaverShoppingTrendingKeywordRankings**](NaverApi.md#naverNaverShoppingTrendingKeywordRankings) | **GET** /v1/naver/shopping/keywords | Naver Shopping trending keyword rankings |
| [**naverNaverWebSearch**](NaverApi.md#naverNaverWebSearch) | **GET** /v1/naver/search | Naver web search |
| [**naverSearchSuggestions**](NaverApi.md#naverSearchSuggestions) | **GET** /v1/naver/autocomplete | Search suggestions |


<a id="naverNaverBlogSearch"></a>
# **naverNaverBlogSearch**
> Object naverNaverBlogSearch(query, page)

Naver blog search

Naver blog vertical — post title, blog name and real post URLs.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.NaverApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    NaverApi apiInstance = new NaverApi(defaultClient);
    String query = "query_example"; // String | 검색어
    Integer page = 1; // Integer | 
    try {
      Object result = apiInstance.naverNaverBlogSearch(query, page);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling NaverApi#naverNaverBlogSearch");
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
| **query** | **String**| 검색어 | |
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

<a id="naverNaverDatalabShoppingKeywordInsight"></a>
# **naverNaverDatalabShoppingKeywordInsight**
> Object naverNaverDatalabShoppingKeywordInsight(categoryId, startDate, endDate, timeUnit, count)

Naver DataLab shopping keyword insight

DataLab Shopping Insight — top search keywords in a category over a window.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.NaverApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    NaverApi apiInstance = new NaverApi(defaultClient);
    String categoryId = "categoryId_example"; // String | DataLab category id (cid), e.g. 50000000
    String startDate = "startDate_example"; // String | YYYY-MM-DD
    String endDate = "endDate_example"; // String | YYYY-MM-DD
    String timeUnit = "date"; // String | date | week | month
    Integer count = 20; // Integer | Keywords to return
    try {
      Object result = apiInstance.naverNaverDatalabShoppingKeywordInsight(categoryId, startDate, endDate, timeUnit, count);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling NaverApi#naverNaverDatalabShoppingKeywordInsight");
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
| **categoryId** | **String**| DataLab category id (cid), e.g. 50000000 | |
| **startDate** | **String**| YYYY-MM-DD | |
| **endDate** | **String**| YYYY-MM-DD | |
| **timeUnit** | **String**| date | week | month | [optional] [default to date] |
| **count** | **Integer**| Keywords to return | [optional] [default to 20] |

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

<a id="naverNaverNewsSearch"></a>
# **naverNaverNewsSearch**
> Object naverNaverNewsSearch(query, page)

Naver news search

Naver news vertical — publisher, age string and real article URLs.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.NaverApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    NaverApi apiInstance = new NaverApi(defaultClient);
    String query = "query_example"; // String | 검색어
    Integer page = 1; // Integer | 
    try {
      Object result = apiInstance.naverNaverNewsSearch(query, page);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling NaverApi#naverNaverNewsSearch");
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
| **query** | **String**| 검색어 | |
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

<a id="naverNaverPlaceDetail"></a>
# **naverNaverPlaceDetail**
> Object naverNaverPlaceDetail(placeId)

Naver place detail

Naver Place detail by place id.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.NaverApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    NaverApi apiInstance = new NaverApi(defaultClient);
    String placeId = "placeId_example"; // String | 
    try {
      Object result = apiInstance.naverNaverPlaceDetail(placeId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling NaverApi#naverNaverPlaceDetail");
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

<a id="naverNaverPlaceLocalSearch"></a>
# **naverNaverPlaceLocalSearch**
> Object naverNaverPlaceLocalSearch(query)

Naver Place/Local search

Naver Place/Local search — name, category, rating, hours status.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.NaverApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    NaverApi apiInstance = new NaverApi(defaultClient);
    String query = "query_example"; // String | Place query, e.g. '성남 카페'
    try {
      Object result = apiInstance.naverNaverPlaceLocalSearch(query);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling NaverApi#naverNaverPlaceLocalSearch");
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
| **query** | **String**| Place query, e.g. &#39;성남 카페&#39; | |

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

<a id="naverNaverPlaceVisitorReviews"></a>
# **naverNaverPlaceVisitorReviews**
> Object naverNaverPlaceVisitorReviews(placeId)

Naver place visitor reviews

Visitor reviews for a Naver place — rating, body, reviewer, voted keywords, photos.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.NaverApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    NaverApi apiInstance = new NaverApi(defaultClient);
    String placeId = "placeId_example"; // String | 
    try {
      Object result = apiInstance.naverNaverPlaceVisitorReviews(placeId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling NaverApi#naverNaverPlaceVisitorReviews");
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

<a id="naverNaverScraperHealthCheck"></a>
# **naverNaverScraperHealthCheck**
> Object naverNaverScraperHealthCheck()

Naver scraper health check

Check health of the Naver scraper service (accepts HEAD for UptimeRobot).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.NaverApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    NaverApi apiInstance = new NaverApi(defaultClient);
    try {
      Object result = apiInstance.naverNaverScraperHealthCheck();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling NaverApi#naverNaverScraperHealthCheck");
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

<a id="naverNaverScraperHealthCheckHead"></a>
# **naverNaverScraperHealthCheckHead**
> Object naverNaverScraperHealthCheckHead()

Naver scraper health check

Check health of the Naver scraper service (accepts HEAD for UptimeRobot).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.NaverApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    NaverApi apiInstance = new NaverApi(defaultClient);
    try {
      Object result = apiInstance.naverNaverScraperHealthCheckHead();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling NaverApi#naverNaverScraperHealthCheckHead");
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

<a id="naverNaverShoppingBestsellerRankings"></a>
# **naverNaverShoppingBestsellerRankings**
> Object naverNaverShoppingBestsellerRankings(categoryId, ageType, sortType, periodType)

Naver Shopping bestseller rankings

Naver Shopping bestseller rankings — ranked products with price, review score, mall.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.NaverApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    NaverApi apiInstance = new NaverApi(defaultClient);
    String categoryId = "ALL"; // String | Naver shopping category id, or ALL
    String ageType = "ALL"; // String | ALL | MEN_20 | WOMEN_20 | ...
    String sortType = "PRODUCT_CLICK"; // String | PRODUCT_CLICK | PRODUCT_BUY
    String periodType = "DAILY"; // String | DAILY | WEEKLY
    try {
      Object result = apiInstance.naverNaverShoppingBestsellerRankings(categoryId, ageType, sortType, periodType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling NaverApi#naverNaverShoppingBestsellerRankings");
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
| **categoryId** | **String**| Naver shopping category id, or ALL | [optional] [default to ALL] |
| **ageType** | **String**| ALL | MEN_20 | WOMEN_20 | ... | [optional] [default to ALL] |
| **sortType** | **String**| PRODUCT_CLICK | PRODUCT_BUY | [optional] [default to PRODUCT_CLICK] |
| **periodType** | **String**| DAILY | WEEKLY | [optional] [default to DAILY] |

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

<a id="naverNaverShoppingCategoryReference"></a>
# **naverNaverShoppingCategoryReference**
> Object naverNaverShoppingCategoryReference()

Naver Shopping category reference

Naver Shopping top-level category ids (for bestsellers/keywords/insight). Free.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.NaverApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    NaverApi apiInstance = new NaverApi(defaultClient);
    try {
      Object result = apiInstance.naverNaverShoppingCategoryReference();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling NaverApi#naverNaverShoppingCategoryReference");
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

<a id="naverNaverShoppingTrendingKeywordRankings"></a>
# **naverNaverShoppingTrendingKeywordRankings**
> Object naverNaverShoppingTrendingKeywordRankings(categoryId, ageType, sortType, periodType)

Naver Shopping trending keyword rankings

Trending Naver Shopping keywords for a category (snxbest keyword rankings).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.NaverApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    NaverApi apiInstance = new NaverApi(defaultClient);
    String categoryId = "categoryId_example"; // String | Naver shopping category id (see /shopping/categories)
    String ageType = "ALL"; // String | ALL | MEN_20 | WOMEN_20 | ...
    String sortType = "KEYWORD_POPULAR"; // String | 
    String periodType = "WEEKLY"; // String | DAILY | WEEKLY
    try {
      Object result = apiInstance.naverNaverShoppingTrendingKeywordRankings(categoryId, ageType, sortType, periodType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling NaverApi#naverNaverShoppingTrendingKeywordRankings");
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
| **categoryId** | **String**| Naver shopping category id (see /shopping/categories) | |
| **ageType** | **String**| ALL | MEN_20 | WOMEN_20 | ... | [optional] [default to ALL] |
| **sortType** | **String**|  | [optional] [default to KEYWORD_POPULAR] |
| **periodType** | **String**| DAILY | WEEKLY | [optional] [default to WEEKLY] |

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

<a id="naverNaverWebSearch"></a>
# **naverNaverWebSearch**
> Object naverNaverWebSearch(query, page)

Naver web search

Naver integrated SERP — organic results plus the inline Place pack.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.NaverApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    NaverApi apiInstance = new NaverApi(defaultClient);
    String query = "query_example"; // String | 검색어, e.g. '성남 카페'
    Integer page = 1; // Integer | Result page
    try {
      Object result = apiInstance.naverNaverWebSearch(query, page);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling NaverApi#naverNaverWebSearch");
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
| **query** | **String**| 검색어, e.g. &#39;성남 카페&#39; | |
| **page** | **Integer**| Result page | [optional] [default to 1] |

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

<a id="naverSearchSuggestions"></a>
# **naverSearchSuggestions**
> Object naverSearchSuggestions(query)

Search suggestions

Naver search-box suggestions.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.NaverApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    NaverApi apiInstance = new NaverApi(defaultClient);
    String query = "query_example"; // String | Partial search term
    try {
      Object result = apiInstance.naverSearchSuggestions(query);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling NaverApi#naverSearchSuggestions");
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
| **query** | **String**| Partial search term | |

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

