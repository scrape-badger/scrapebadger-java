# FacebookApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**facebookBrowseAMarketplaceCategory**](FacebookApi.md#facebookBrowseAMarketplaceCategory) | **GET** /v1/facebook/marketplace/category/{category} | Browse a Marketplace category |
| [**facebookGetAMarketplaceItem**](FacebookApi.md#facebookGetAMarketplaceItem) | **GET** /v1/facebook/marketplace/item/{item_id} | Get a Marketplace item |
| [**facebookGetAnAd**](FacebookApi.md#facebookGetAnAd) | **GET** /v1/facebook/ads/{ad_archive_id} | Get an ad |
| [**facebookGetGroupDetail**](FacebookApi.md#facebookGetGroupDetail) | **GET** /v1/facebook/groups/{group_id} | Get group detail |
| [**facebookGetGroupPosts**](FacebookApi.md#facebookGetGroupPosts) | **GET** /v1/facebook/groups/{group_id}/posts | Get group posts |
| [**facebookGetPageDetail**](FacebookApi.md#facebookGetPageDetail) | **GET** /v1/facebook/pages/{identifier} | Get page detail |
| [**facebookGetPagePosts**](FacebookApi.md#facebookGetPagePosts) | **GET** /v1/facebook/pages/{identifier}/posts | Get page posts |
| [**facebookGetPostComments**](FacebookApi.md#facebookGetPostComments) | **GET** /v1/facebook/posts/{post_id}/comments | Get post comments |
| [**facebookGetPostDetail**](FacebookApi.md#facebookGetPostDetail) | **GET** /v1/facebook/posts/{post_id} | Get post detail |
| [**facebookGetProfileDetail**](FacebookApi.md#facebookGetProfileDetail) | **GET** /v1/facebook/profiles/{identifier} | Get profile detail |
| [**facebookGetProfilePosts**](FacebookApi.md#facebookGetProfilePosts) | **GET** /v1/facebook/profiles/{identifier}/posts | Get profile posts |
| [**facebookListCategories**](FacebookApi.md#facebookListCategories) | **GET** /v1/facebook/marketplace/categories | List categories |
| [**facebookListLocations**](FacebookApi.md#facebookListLocations) | **GET** /v1/facebook/marketplace/locations | List locations |
| [**facebookSearchEvents**](FacebookApi.md#facebookSearchEvents) | **GET** /v1/facebook/search/events | Search events |
| [**facebookSearchEverything**](FacebookApi.md#facebookSearchEverything) | **GET** /v1/facebook/search | Search everything |
| [**facebookSearchGroups**](FacebookApi.md#facebookSearchGroups) | **GET** /v1/facebook/search/groups | Search groups |
| [**facebookSearchMarketplace**](FacebookApi.md#facebookSearchMarketplace) | **GET** /v1/facebook/marketplace/search | Search Marketplace |
| [**facebookSearchPages**](FacebookApi.md#facebookSearchPages) | **GET** /v1/facebook/search/pages | Search Pages |
| [**facebookSearchPeople**](FacebookApi.md#facebookSearchPeople) | **GET** /v1/facebook/search/people | Search people |
| [**facebookSearchPlaces**](FacebookApi.md#facebookSearchPlaces) | **GET** /v1/facebook/search/places | Search places |
| [**facebookSearchPosts**](FacebookApi.md#facebookSearchPosts) | **GET** /v1/facebook/search/posts | Search posts |
| [**facebookSearchTheAdLibrary**](FacebookApi.md#facebookSearchTheAdLibrary) | **GET** /v1/facebook/ads/search | Search the Ad Library |


<a id="facebookBrowseAMarketplaceCategory"></a>
# **facebookBrowseAMarketplaceCategory**
> Object facebookBrowseAMarketplaceCategory(category, location, minPrice, maxPrice, sortBy, after)

Browse a Marketplace category

Browse Marketplace listings in a category (vehicles, electronics, ...).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.FacebookApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    FacebookApi apiInstance = new FacebookApi(defaultClient);
    String category = "category_example"; // String | 
    String location = "nyc"; // String | 
    Integer minPrice = 56; // Integer | 
    Integer maxPrice = 56; // Integer | 
    String sortBy = "sortBy_example"; // String | 
    String after = "after_example"; // String | 
    try {
      Object result = apiInstance.facebookBrowseAMarketplaceCategory(category, location, minPrice, maxPrice, sortBy, after);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FacebookApi#facebookBrowseAMarketplaceCategory");
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
| **category** | **String**|  | |
| **location** | **String**|  | [optional] [default to nyc] |
| **minPrice** | **Integer**|  | [optional] |
| **maxPrice** | **Integer**|  | [optional] |
| **sortBy** | **String**|  | [optional] |
| **after** | **String**|  | [optional] |

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

<a id="facebookGetAMarketplaceItem"></a>
# **facebookGetAMarketplaceItem**
> Object facebookGetAMarketplaceItem(itemId)

Get a Marketplace item

Get full detail for a single Marketplace listing.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.FacebookApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    FacebookApi apiInstance = new FacebookApi(defaultClient);
    String itemId = "itemId_example"; // String | 
    try {
      Object result = apiInstance.facebookGetAMarketplaceItem(itemId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FacebookApi#facebookGetAMarketplaceItem");
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
| **itemId** | **String**|  | |

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

<a id="facebookGetAnAd"></a>
# **facebookGetAnAd**
> Object facebookGetAnAd(adArchiveId)

Get an ad

Get a single Ad Library ad by its archive id.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.FacebookApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    FacebookApi apiInstance = new FacebookApi(defaultClient);
    String adArchiveId = "adArchiveId_example"; // String | 
    try {
      Object result = apiInstance.facebookGetAnAd(adArchiveId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FacebookApi#facebookGetAnAd");
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
| **adArchiveId** | **String**|  | |

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

<a id="facebookGetGroupDetail"></a>
# **facebookGetGroupDetail**
> Object facebookGetGroupDetail(groupId)

Get group detail

Get a Facebook group&#39;s details.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.FacebookApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    FacebookApi apiInstance = new FacebookApi(defaultClient);
    String groupId = "groupId_example"; // String | 
    try {
      Object result = apiInstance.facebookGetGroupDetail(groupId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FacebookApi#facebookGetGroupDetail");
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
| **groupId** | **String**|  | |

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

<a id="facebookGetGroupPosts"></a>
# **facebookGetGroupPosts**
> Object facebookGetGroupPosts(groupId, after)

Get group posts

Get a Facebook group&#39;s post feed.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.FacebookApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    FacebookApi apiInstance = new FacebookApi(defaultClient);
    String groupId = "groupId_example"; // String | 
    String after = "after_example"; // String | 
    try {
      Object result = apiInstance.facebookGetGroupPosts(groupId, after);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FacebookApi#facebookGetGroupPosts");
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
| **groupId** | **String**|  | |
| **after** | **String**|  | [optional] |

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

<a id="facebookGetPageDetail"></a>
# **facebookGetPageDetail**
> Object facebookGetPageDetail(identifier)

Get page detail

Get a Facebook Page&#39;s profile (name, category, followers, about).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.FacebookApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    FacebookApi apiInstance = new FacebookApi(defaultClient);
    String identifier = "identifier_example"; // String | 
    try {
      Object result = apiInstance.facebookGetPageDetail(identifier);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FacebookApi#facebookGetPageDetail");
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
| **identifier** | **String**|  | |

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

<a id="facebookGetPagePosts"></a>
# **facebookGetPagePosts**
> Object facebookGetPagePosts(identifier, after)

Get page posts

Get a Facebook Page&#39;s timeline posts.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.FacebookApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    FacebookApi apiInstance = new FacebookApi(defaultClient);
    String identifier = "identifier_example"; // String | 
    String after = "after_example"; // String | 
    try {
      Object result = apiInstance.facebookGetPagePosts(identifier, after);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FacebookApi#facebookGetPagePosts");
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
| **identifier** | **String**|  | |
| **after** | **String**|  | [optional] |

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

<a id="facebookGetPostComments"></a>
# **facebookGetPostComments**
> Object facebookGetPostComments(postId, after, sort)

Get post comments

Get a Facebook post&#39;s comment thread (paginated).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.FacebookApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    FacebookApi apiInstance = new FacebookApi(defaultClient);
    String postId = "postId_example"; // String | 
    String after = "after_example"; // String | 
    String sort = "relevance"; // String | 
    try {
      Object result = apiInstance.facebookGetPostComments(postId, after, sort);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FacebookApi#facebookGetPostComments");
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
| **postId** | **String**|  | |
| **after** | **String**|  | [optional] |
| **sort** | **String**|  | [optional] [default to relevance] |

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

<a id="facebookGetPostDetail"></a>
# **facebookGetPostDetail**
> Object facebookGetPostDetail(postId)

Get post detail

Get a Facebook post&#39;s detail plus its top comments.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.FacebookApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    FacebookApi apiInstance = new FacebookApi(defaultClient);
    String postId = "postId_example"; // String | 
    try {
      Object result = apiInstance.facebookGetPostDetail(postId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FacebookApi#facebookGetPostDetail");
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
| **postId** | **String**|  | |

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

<a id="facebookGetProfileDetail"></a>
# **facebookGetProfileDetail**
> Object facebookGetProfileDetail(identifier)

Get profile detail

Get a Facebook profile&#39;s details.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.FacebookApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    FacebookApi apiInstance = new FacebookApi(defaultClient);
    String identifier = "identifier_example"; // String | 
    try {
      Object result = apiInstance.facebookGetProfileDetail(identifier);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FacebookApi#facebookGetProfileDetail");
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
| **identifier** | **String**|  | |

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

<a id="facebookGetProfilePosts"></a>
# **facebookGetProfilePosts**
> Object facebookGetProfilePosts(identifier, after)

Get profile posts

Get a Facebook profile&#39;s timeline posts.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.FacebookApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    FacebookApi apiInstance = new FacebookApi(defaultClient);
    String identifier = "identifier_example"; // String | 
    String after = "after_example"; // String | 
    try {
      Object result = apiInstance.facebookGetProfilePosts(identifier, after);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FacebookApi#facebookGetProfilePosts");
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
| **identifier** | **String**|  | |
| **after** | **String**|  | [optional] |

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

<a id="facebookListCategories"></a>
# **facebookListCategories**
> Object facebookListCategories()

List categories

List Marketplace category slugs (free).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.FacebookApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    FacebookApi apiInstance = new FacebookApi(defaultClient);
    try {
      Object result = apiInstance.facebookListCategories();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FacebookApi#facebookListCategories");
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

<a id="facebookListLocations"></a>
# **facebookListLocations**
> Object facebookListLocations()

List locations

List common Marketplace location slugs (free).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.FacebookApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    FacebookApi apiInstance = new FacebookApi(defaultClient);
    try {
      Object result = apiInstance.facebookListLocations();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FacebookApi#facebookListLocations");
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

<a id="facebookSearchEvents"></a>
# **facebookSearchEvents**
> Object facebookSearchEvents(q, after)

Search events

Search Facebook events.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.FacebookApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    FacebookApi apiInstance = new FacebookApi(defaultClient);
    String q = "q_example"; // String | 
    String after = "after_example"; // String | 
    try {
      Object result = apiInstance.facebookSearchEvents(q, after);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FacebookApi#facebookSearchEvents");
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
| **q** | **String**|  | |
| **after** | **String**|  | [optional] |

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

<a id="facebookSearchEverything"></a>
# **facebookSearchEverything**
> Object facebookSearchEverything(q, after)

Search everything

Global Facebook search (top results across pages, people, groups, posts).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.FacebookApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    FacebookApi apiInstance = new FacebookApi(defaultClient);
    String q = "q_example"; // String | Search query
    String after = "after_example"; // String | 
    try {
      Object result = apiInstance.facebookSearchEverything(q, after);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FacebookApi#facebookSearchEverything");
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
| **after** | **String**|  | [optional] |

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

<a id="facebookSearchGroups"></a>
# **facebookSearchGroups**
> Object facebookSearchGroups(q, after)

Search groups

Search Facebook groups.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.FacebookApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    FacebookApi apiInstance = new FacebookApi(defaultClient);
    String q = "q_example"; // String | 
    String after = "after_example"; // String | 
    try {
      Object result = apiInstance.facebookSearchGroups(q, after);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FacebookApi#facebookSearchGroups");
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
| **q** | **String**|  | |
| **after** | **String**|  | [optional] |

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

<a id="facebookSearchMarketplace"></a>
# **facebookSearchMarketplace**
> Object facebookSearchMarketplace(query, location, minPrice, maxPrice, daysSinceListed, sortBy, itemCondition, deliveryMethod, after)

Search Marketplace

Search Facebook Marketplace listings by keyword and location.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.FacebookApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    FacebookApi apiInstance = new FacebookApi(defaultClient);
    String query = "query_example"; // String | Search keywords
    String location = "nyc"; // String | Marketplace location slug
    Integer minPrice = 56; // Integer | 
    Integer maxPrice = 56; // Integer | 
    Integer daysSinceListed = 56; // Integer | 
    String sortBy = "sortBy_example"; // String | 
    String itemCondition = "itemCondition_example"; // String | 
    String deliveryMethod = "deliveryMethod_example"; // String | 
    String after = "after_example"; // String | 
    try {
      Object result = apiInstance.facebookSearchMarketplace(query, location, minPrice, maxPrice, daysSinceListed, sortBy, itemCondition, deliveryMethod, after);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FacebookApi#facebookSearchMarketplace");
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
| **location** | **String**| Marketplace location slug | [optional] [default to nyc] |
| **minPrice** | **Integer**|  | [optional] |
| **maxPrice** | **Integer**|  | [optional] |
| **daysSinceListed** | **Integer**|  | [optional] |
| **sortBy** | **String**|  | [optional] |
| **itemCondition** | **String**|  | [optional] |
| **deliveryMethod** | **String**|  | [optional] |
| **after** | **String**|  | [optional] |

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

<a id="facebookSearchPages"></a>
# **facebookSearchPages**
> Object facebookSearchPages(q, after)

Search Pages

Search Facebook Pages.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.FacebookApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    FacebookApi apiInstance = new FacebookApi(defaultClient);
    String q = "q_example"; // String | 
    String after = "after_example"; // String | 
    try {
      Object result = apiInstance.facebookSearchPages(q, after);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FacebookApi#facebookSearchPages");
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
| **q** | **String**|  | |
| **after** | **String**|  | [optional] |

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

<a id="facebookSearchPeople"></a>
# **facebookSearchPeople**
> Object facebookSearchPeople(q, after)

Search people

Search Facebook profiles.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.FacebookApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    FacebookApi apiInstance = new FacebookApi(defaultClient);
    String q = "q_example"; // String | 
    String after = "after_example"; // String | 
    try {
      Object result = apiInstance.facebookSearchPeople(q, after);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FacebookApi#facebookSearchPeople");
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
| **q** | **String**|  | |
| **after** | **String**|  | [optional] |

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

<a id="facebookSearchPlaces"></a>
# **facebookSearchPlaces**
> Object facebookSearchPlaces(q, after)

Search places

Search Facebook places.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.FacebookApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    FacebookApi apiInstance = new FacebookApi(defaultClient);
    String q = "q_example"; // String | 
    String after = "after_example"; // String | 
    try {
      Object result = apiInstance.facebookSearchPlaces(q, after);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FacebookApi#facebookSearchPlaces");
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
| **q** | **String**|  | |
| **after** | **String**|  | [optional] |

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

<a id="facebookSearchPosts"></a>
# **facebookSearchPosts**
> Object facebookSearchPosts(q, after)

Search posts

Search public Facebook posts.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.FacebookApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    FacebookApi apiInstance = new FacebookApi(defaultClient);
    String q = "q_example"; // String | 
    String after = "after_example"; // String | 
    try {
      Object result = apiInstance.facebookSearchPosts(q, after);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FacebookApi#facebookSearchPosts");
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
| **q** | **String**|  | |
| **after** | **String**|  | [optional] |

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

<a id="facebookSearchTheAdLibrary"></a>
# **facebookSearchTheAdLibrary**
> Object facebookSearchTheAdLibrary(query, country, adType, activeStatus, after)

Search the Ad Library

Search the Facebook Ad Library.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.FacebookApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    FacebookApi apiInstance = new FacebookApi(defaultClient);
    String query = "query_example"; // String | Advertiser or keyword
    String country = "US"; // String | 
    String adType = "all"; // String | 
    String activeStatus = "active"; // String | 
    String after = "after_example"; // String | 
    try {
      Object result = apiInstance.facebookSearchTheAdLibrary(query, country, adType, activeStatus, after);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling FacebookApi#facebookSearchTheAdLibrary");
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
| **query** | **String**| Advertiser or keyword | |
| **country** | **String**|  | [optional] [default to US] |
| **adType** | **String**|  | [optional] [default to all] |
| **activeStatus** | **String**|  | [optional] [default to active] |
| **after** | **String**|  | [optional] |

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

