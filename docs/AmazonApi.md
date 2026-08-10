# AmazonApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**amazonAmazonScraperHealthCheck**](AmazonApi.md#amazonAmazonScraperHealthCheck) | **GET** /v1/amazon/health | Amazon scraper health check |
| [**amazonAmazonScraperHealthCheckHead**](AmazonApi.md#amazonAmazonScraperHealthCheckHead) | **HEAD** /v1/amazon/health | Amazon scraper health check |
| [**amazonBestsellersByCategory**](AmazonApi.md#amazonBestsellersByCategory) | **GET** /v1/amazon/bestsellers | Bestsellers by category |
| [**amazonBrowseNodeCategoryListing**](AmazonApi.md#amazonBrowseNodeCategoryListing) | **GET** /v1/amazon/category | Browse-node category listing |
| [**amazonGetAllSellerOffersBuybox**](AmazonApi.md#amazonGetAllSellerOffersBuybox) | **GET** /v1/amazon/products/{asin}/offers | Get all seller offers (buybox) |
| [**amazonGetProductDetail**](AmazonApi.md#amazonGetProductDetail) | **GET** /v1/amazon/products/{asin} | Get product detail |
| [**amazonGetProductReviews**](AmazonApi.md#amazonGetProductReviews) | **GET** /v1/amazon/products/{asin}/reviews | Get product reviews |
| [**amazonGetSellerFeedback**](AmazonApi.md#amazonGetSellerFeedback) | **GET** /v1/amazon/sellers/{seller_id}/feedback | Get seller feedback |
| [**amazonGetSellerProfile**](AmazonApi.md#amazonGetSellerProfile) | **GET** /v1/amazon/sellers/{seller_id} | Get seller profile |
| [**amazonGetSellerStorefrontProducts**](AmazonApi.md#amazonGetSellerStorefrontProducts) | **GET** /v1/amazon/sellers/{seller_id}/products | Get seller storefront products |
| [**amazonKeywordSuggestions**](AmazonApi.md#amazonKeywordSuggestions) | **GET** /v1/amazon/autocomplete | Keyword suggestions |
| [**amazonListCategoryAliases**](AmazonApi.md#amazonListCategoryAliases) | **GET** /v1/amazon/categories | List category aliases |
| [**amazonListMarketplaces**](AmazonApi.md#amazonListMarketplaces) | **GET** /v1/amazon/markets | List marketplaces |
| [**amazonNewReleasesByCategory**](AmazonApi.md#amazonNewReleasesByCategory) | **GET** /v1/amazon/new-releases | New releases by category |
| [**amazonSearchAmazonProducts**](AmazonApi.md#amazonSearchAmazonProducts) | **GET** /v1/amazon/search | Search Amazon products |
| [**amazonTodaySDeals**](AmazonApi.md#amazonTodaySDeals) | **GET** /v1/amazon/deals | Today&#39;s deals |


<a id="amazonAmazonScraperHealthCheck"></a>
# **amazonAmazonScraperHealthCheck**
> Object amazonAmazonScraperHealthCheck()

Amazon scraper health check

Check health of the Amazon scraper service (accepts HEAD for UptimeRobot).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.AmazonApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    AmazonApi apiInstance = new AmazonApi(defaultClient);
    try {
      Object result = apiInstance.amazonAmazonScraperHealthCheck();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AmazonApi#amazonAmazonScraperHealthCheck");
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

<a id="amazonAmazonScraperHealthCheckHead"></a>
# **amazonAmazonScraperHealthCheckHead**
> Object amazonAmazonScraperHealthCheckHead()

Amazon scraper health check

Check health of the Amazon scraper service (accepts HEAD for UptimeRobot).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.AmazonApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    AmazonApi apiInstance = new AmazonApi(defaultClient);
    try {
      Object result = apiInstance.amazonAmazonScraperHealthCheckHead();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AmazonApi#amazonAmazonScraperHealthCheckHead");
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

<a id="amazonBestsellersByCategory"></a>
# **amazonBestsellersByCategory**
> Object amazonBestsellersByCategory(domain, category, page)

Bestsellers by category

Top-selling products for a category (browse node).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.AmazonApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    AmazonApi apiInstance = new AmazonApi(defaultClient);
    String domain = "com"; // String | 
    String category = "category_example"; // String | Bestsellers node id or slug
    Integer page = 1; // Integer | 
    try {
      Object result = apiInstance.amazonBestsellersByCategory(domain, category, page);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AmazonApi#amazonBestsellersByCategory");
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
| **domain** | **String**|  | [optional] [default to com] |
| **category** | **String**| Bestsellers node id or slug | [optional] |
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

<a id="amazonBrowseNodeCategoryListing"></a>
# **amazonBrowseNodeCategoryListing**
> Object amazonBrowseNodeCategoryListing(node, domain, page, sortBy)

Browse-node category listing

List products within an Amazon browse-node category.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.AmazonApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    AmazonApi apiInstance = new AmazonApi(defaultClient);
    String node = "node_example"; // String | Amazon browse-node id
    String domain = "com"; // String | 
    Integer page = 1; // Integer | 
    String sortBy = "sortBy_example"; // String | 
    try {
      Object result = apiInstance.amazonBrowseNodeCategoryListing(node, domain, page, sortBy);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AmazonApi#amazonBrowseNodeCategoryListing");
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
| **node** | **String**| Amazon browse-node id | |
| **domain** | **String**|  | [optional] [default to com] |
| **page** | **Integer**|  | [optional] [default to 1] |
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

<a id="amazonGetAllSellerOffersBuybox"></a>
# **amazonGetAllSellerOffersBuybox**
> Object amazonGetAllSellerOffersBuybox(asin, domain, zip)

Get all seller offers (buybox)

All third-party offers for an ASIN, including the Buy Box winner.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.AmazonApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    AmazonApi apiInstance = new AmazonApi(defaultClient);
    String asin = "asin_example"; // String | 
    String domain = "com"; // String | 
    String zip = "zip_example"; // String | 
    try {
      Object result = apiInstance.amazonGetAllSellerOffersBuybox(asin, domain, zip);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AmazonApi#amazonGetAllSellerOffersBuybox");
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
| **asin** | **String**|  | |
| **domain** | **String**|  | [optional] [default to com] |
| **zip** | **String**|  | [optional] |

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

<a id="amazonGetProductDetail"></a>
# **amazonGetProductDetail**
> Object amazonGetProductDetail(asin, domain, zip, language)

Get product detail

Full product detail by ASIN (price, variants, badges, buybox, ranks…).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.AmazonApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    AmazonApi apiInstance = new AmazonApi(defaultClient);
    String asin = "asin_example"; // String | 
    String domain = "com"; // String | 
    String zip = "zip_example"; // String | Delivery postal/zip for localized buybox
    String language = "language_example"; // String | 
    try {
      Object result = apiInstance.amazonGetProductDetail(asin, domain, zip, language);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AmazonApi#amazonGetProductDetail");
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
| **asin** | **String**|  | |
| **domain** | **String**|  | [optional] [default to com] |
| **zip** | **String**| Delivery postal/zip for localized buybox | [optional] |
| **language** | **String**|  | [optional] |

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

<a id="amazonGetProductReviews"></a>
# **amazonGetProductReviews**
> Object amazonGetProductReviews(asin, domain, page, sortBy, star, verifiedOnly, mediaOnly)

Get product reviews

Customer reviews for an ASIN (featured + paginated, with filters).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.AmazonApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    AmazonApi apiInstance = new AmazonApi(defaultClient);
    String asin = "asin_example"; // String | 
    String domain = "com"; // String | 
    Integer page = 1; // Integer | Review page (1-100, ~10 reviews/page)
    String sortBy = "helpful"; // String | helpful | recent
    String star = "star_example"; // String | one_star..five_star | positive | critical
    Boolean verifiedOnly = false; // Boolean | 
    Boolean mediaOnly = false; // Boolean | 
    try {
      Object result = apiInstance.amazonGetProductReviews(asin, domain, page, sortBy, star, verifiedOnly, mediaOnly);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AmazonApi#amazonGetProductReviews");
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
| **asin** | **String**|  | |
| **domain** | **String**|  | [optional] [default to com] |
| **page** | **Integer**| Review page (1-100, ~10 reviews/page) | [optional] [default to 1] |
| **sortBy** | **String**| helpful | recent | [optional] [default to helpful] |
| **star** | **String**| one_star..five_star | positive | critical | [optional] |
| **verifiedOnly** | **Boolean**|  | [optional] [default to false] |
| **mediaOnly** | **Boolean**|  | [optional] [default to false] |

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

<a id="amazonGetSellerFeedback"></a>
# **amazonGetSellerFeedback**
> Object amazonGetSellerFeedback(sellerId, domain, page)

Get seller feedback

Buyer feedback entries for a seller.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.AmazonApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    AmazonApi apiInstance = new AmazonApi(defaultClient);
    String sellerId = "sellerId_example"; // String | 
    String domain = "com"; // String | 
    Integer page = 1; // Integer | 
    try {
      Object result = apiInstance.amazonGetSellerFeedback(sellerId, domain, page);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AmazonApi#amazonGetSellerFeedback");
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
| **sellerId** | **String**|  | |
| **domain** | **String**|  | [optional] [default to com] |
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

<a id="amazonGetSellerProfile"></a>
# **amazonGetSellerProfile**
> Object amazonGetSellerProfile(sellerId, domain)

Get seller profile

Seller profile, ratings and feedback summary.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.AmazonApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    AmazonApi apiInstance = new AmazonApi(defaultClient);
    String sellerId = "sellerId_example"; // String | 
    String domain = "com"; // String | 
    try {
      Object result = apiInstance.amazonGetSellerProfile(sellerId, domain);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AmazonApi#amazonGetSellerProfile");
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
| **sellerId** | **String**|  | |
| **domain** | **String**|  | [optional] [default to com] |

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

<a id="amazonGetSellerStorefrontProducts"></a>
# **amazonGetSellerStorefrontProducts**
> Object amazonGetSellerStorefrontProducts(sellerId, domain, page)

Get seller storefront products

Products listed in a seller&#39;s storefront.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.AmazonApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    AmazonApi apiInstance = new AmazonApi(defaultClient);
    String sellerId = "sellerId_example"; // String | 
    String domain = "com"; // String | 
    Integer page = 1; // Integer | 
    try {
      Object result = apiInstance.amazonGetSellerStorefrontProducts(sellerId, domain, page);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AmazonApi#amazonGetSellerStorefrontProducts");
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
| **sellerId** | **String**|  | |
| **domain** | **String**|  | [optional] [default to com] |
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

<a id="amazonKeywordSuggestions"></a>
# **amazonKeywordSuggestions**
> Object amazonKeywordSuggestions(query, domain)

Keyword suggestions

Get Amazon search autocomplete suggestions for keyword research.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.AmazonApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    AmazonApi apiInstance = new AmazonApi(defaultClient);
    String query = "query_example"; // String | Partial search term
    String domain = "com"; // String | 
    try {
      Object result = apiInstance.amazonKeywordSuggestions(query, domain);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AmazonApi#amazonKeywordSuggestions");
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
| **domain** | **String**|  | [optional] [default to com] |

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

<a id="amazonListCategoryAliases"></a>
# **amazonListCategoryAliases**
> Object amazonListCategoryAliases(domain)

List category aliases

List common Amazon department/category aliases and bestseller nodes.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.AmazonApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    AmazonApi apiInstance = new AmazonApi(defaultClient);
    String domain = "com"; // String | 
    try {
      Object result = apiInstance.amazonListCategoryAliases(domain);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AmazonApi#amazonListCategoryAliases");
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
| **domain** | **String**|  | [optional] [default to com] |

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

<a id="amazonListMarketplaces"></a>
# **amazonListMarketplaces**
> Object amazonListMarketplaces()

List marketplaces

List all supported Amazon marketplaces.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.AmazonApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    AmazonApi apiInstance = new AmazonApi(defaultClient);
    try {
      Object result = apiInstance.amazonListMarketplaces();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AmazonApi#amazonListMarketplaces");
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

<a id="amazonNewReleasesByCategory"></a>
# **amazonNewReleasesByCategory**
> Object amazonNewReleasesByCategory(domain, category, page)

New releases by category

Newly released products for a category (browse node).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.AmazonApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    AmazonApi apiInstance = new AmazonApi(defaultClient);
    String domain = "com"; // String | 
    String category = "category_example"; // String | 
    Integer page = 1; // Integer | 
    try {
      Object result = apiInstance.amazonNewReleasesByCategory(domain, category, page);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AmazonApi#amazonNewReleasesByCategory");
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
| **domain** | **String**|  | [optional] [default to com] |
| **category** | **String**|  | [optional] |
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

<a id="amazonSearchAmazonProducts"></a>
# **amazonSearchAmazonProducts**
> Object amazonSearchAmazonProducts(query, domain, page, sortBy, category, minPrice, maxPrice, zip, language)

Search Amazon products

Search the Amazon catalog with filters and sorting.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.AmazonApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    AmazonApi apiInstance = new AmazonApi(defaultClient);
    String query = "query_example"; // String | Search keywords
    String domain = "com"; // String | Amazon marketplace TLD or code (com, co.uk, de…)
    Integer page = 1; // Integer | 
    String sortBy = "sortBy_example"; // String | relevance | price_low_to_high | price_high_to_low | avg_review | newest
    String category = "category_example"; // String | Department/category alias (i= param)
    BigDecimal minPrice = new BigDecimal(78); // BigDecimal | 
    BigDecimal maxPrice = new BigDecimal(78); // BigDecimal | 
    String zip = "zip_example"; // String | Delivery postal/zip code for localized pricing
    String language = "language_example"; // String | Locale for results, e.g. en_US, fr_FR
    try {
      Object result = apiInstance.amazonSearchAmazonProducts(query, domain, page, sortBy, category, minPrice, maxPrice, zip, language);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AmazonApi#amazonSearchAmazonProducts");
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
| **query** | **String**| Search keywords | |
| **domain** | **String**| Amazon marketplace TLD or code (com, co.uk, de…) | [optional] [default to com] |
| **page** | **Integer**|  | [optional] [default to 1] |
| **sortBy** | **String**| relevance | price_low_to_high | price_high_to_low | avg_review | newest | [optional] |
| **category** | **String**| Department/category alias (i&#x3D; param) | [optional] |
| **minPrice** | **BigDecimal**|  | [optional] |
| **maxPrice** | **BigDecimal**|  | [optional] |
| **zip** | **String**| Delivery postal/zip code for localized pricing | [optional] |
| **language** | **String**| Locale for results, e.g. en_US, fr_FR | [optional] |

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

<a id="amazonTodaySDeals"></a>
# **amazonTodaySDeals**
> Object amazonTodaySDeals(domain, category, page)

Today&#39;s deals

Current Amazon deals (lightning deals, best deals).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.AmazonApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    AmazonApi apiInstance = new AmazonApi(defaultClient);
    String domain = "com"; // String | 
    String category = "category_example"; // String | 
    Integer page = 1; // Integer | 
    try {
      Object result = apiInstance.amazonTodaySDeals(domain, category, page);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AmazonApi#amazonTodaySDeals");
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
| **domain** | **String**|  | [optional] [default to com] |
| **category** | **String**|  | [optional] |
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

