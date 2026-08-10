# PerplexityApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**perplexityAskPerplexityAQuestion**](PerplexityApi.md#perplexityAskPerplexityAQuestion) | **GET** /v1/perplexity/ask | Ask Perplexity a question |
| [**perplexityAskPerplexityAQuestionPost**](PerplexityApi.md#perplexityAskPerplexityAQuestionPost) | **POST** /v1/perplexity/ask | Ask Perplexity a question (POST) |
| [**perplexityMeasureABrandSVisibilityInAPerplexityAnswer**](PerplexityApi.md#perplexityMeasureABrandSVisibilityInAPerplexityAnswer) | **GET** /v1/perplexity/brand-visibility | Measure a brand&#39;s visibility in a Perplexity answer |
| [**perplexityMeasureABrandSVisibilityInAPerplexityAnswerPost**](PerplexityApi.md#perplexityMeasureABrandSVisibilityInAPerplexityAnswerPost) | **POST** /v1/perplexity/brand-visibility | Measure a brand&#39;s visibility in a Perplexity answer (POST) |
| [**perplexityPerplexityScraperHealthCheck**](PerplexityApi.md#perplexityPerplexityScraperHealthCheck) | **GET** /v1/perplexity/health | Perplexity scraper health check |
| [**perplexityPerplexityScraperHealthCheckHead**](PerplexityApi.md#perplexityPerplexityScraperHealthCheckHead) | **HEAD** /v1/perplexity/health | Perplexity scraper health check |


<a id="perplexityAskPerplexityAQuestion"></a>
# **perplexityAskPerplexityAQuestion**
> Object perplexityAskPerplexityAQuestion(prompt, country)

Ask Perplexity a question

Send a prompt to Perplexity and get the answer plus the web sources it cited.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.PerplexityApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    PerplexityApi apiInstance = new PerplexityApi(defaultClient);
    String prompt = "prompt_example"; // String | The prompt to send to Perplexity (max 4096 characters).
    String country = "country_example"; // String | ISO-3166 alpha-2 egress country, e.g. 'US', 'GB', 'DE'.
    try {
      Object result = apiInstance.perplexityAskPerplexityAQuestion(prompt, country);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PerplexityApi#perplexityAskPerplexityAQuestion");
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
| **prompt** | **String**| The prompt to send to Perplexity (max 4096 characters). | |
| **country** | **String**| ISO-3166 alpha-2 egress country, e.g. &#39;US&#39;, &#39;GB&#39;, &#39;DE&#39;. | [optional] |

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

<a id="perplexityAskPerplexityAQuestionPost"></a>
# **perplexityAskPerplexityAQuestionPost**
> Object perplexityAskPerplexityAQuestionPost()

Ask Perplexity a question (POST)

POST form of &#x60;/ask&#x60;, for prompts too long for a query string.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.PerplexityApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    PerplexityApi apiInstance = new PerplexityApi(defaultClient);
    try {
      Object result = apiInstance.perplexityAskPerplexityAQuestionPost();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PerplexityApi#perplexityAskPerplexityAQuestionPost");
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

<a id="perplexityMeasureABrandSVisibilityInAPerplexityAnswer"></a>
# **perplexityMeasureABrandSVisibilityInAPerplexityAnswer**
> Object perplexityMeasureABrandSVisibilityInAPerplexityAnswer(prompt, brand, domain, aliases, competitors, country)

Measure a brand&#39;s visibility in a Perplexity answer

Ask Perplexity, then report whether the brand is mentioned, cited and how prominently.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.PerplexityApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    PerplexityApi apiInstance = new PerplexityApi(defaultClient);
    String prompt = "prompt_example"; // String | The prompt to ask Perplexity.
    String brand = "brand_example"; // String | Brand name to look for in the answer.
    String domain = "domain_example"; // String | Brand domain, for citation matching.
    String aliases = "aliases_example"; // String | Comma-separated alternative names.
    String competitors = "competitors_example"; // String | Comma-separated competitor names.
    String country = "country_example"; // String | ISO-3166 alpha-2 egress country.
    try {
      Object result = apiInstance.perplexityMeasureABrandSVisibilityInAPerplexityAnswer(prompt, brand, domain, aliases, competitors, country);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PerplexityApi#perplexityMeasureABrandSVisibilityInAPerplexityAnswer");
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
| **prompt** | **String**| The prompt to ask Perplexity. | |
| **brand** | **String**| Brand name to look for in the answer. | |
| **domain** | **String**| Brand domain, for citation matching. | [optional] |
| **aliases** | **String**| Comma-separated alternative names. | [optional] |
| **competitors** | **String**| Comma-separated competitor names. | [optional] |
| **country** | **String**| ISO-3166 alpha-2 egress country. | [optional] |

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

<a id="perplexityMeasureABrandSVisibilityInAPerplexityAnswerPost"></a>
# **perplexityMeasureABrandSVisibilityInAPerplexityAnswerPost**
> Object perplexityMeasureABrandSVisibilityInAPerplexityAnswerPost()

Measure a brand&#39;s visibility in a Perplexity answer (POST)

POST form, for longer prompts and larger competitor sets.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.PerplexityApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    PerplexityApi apiInstance = new PerplexityApi(defaultClient);
    try {
      Object result = apiInstance.perplexityMeasureABrandSVisibilityInAPerplexityAnswerPost();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PerplexityApi#perplexityMeasureABrandSVisibilityInAPerplexityAnswerPost");
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

<a id="perplexityPerplexityScraperHealthCheck"></a>
# **perplexityPerplexityScraperHealthCheck**
> Object perplexityPerplexityScraperHealthCheck()

Perplexity scraper health check

Check health of the Perplexity scraper service (accepts HEAD).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.PerplexityApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    PerplexityApi apiInstance = new PerplexityApi(defaultClient);
    try {
      Object result = apiInstance.perplexityPerplexityScraperHealthCheck();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PerplexityApi#perplexityPerplexityScraperHealthCheck");
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

<a id="perplexityPerplexityScraperHealthCheckHead"></a>
# **perplexityPerplexityScraperHealthCheckHead**
> Object perplexityPerplexityScraperHealthCheckHead()

Perplexity scraper health check

Check health of the Perplexity scraper service (accepts HEAD).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.PerplexityApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    PerplexityApi apiInstance = new PerplexityApi(defaultClient);
    try {
      Object result = apiInstance.perplexityPerplexityScraperHealthCheckHead();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PerplexityApi#perplexityPerplexityScraperHealthCheckHead");
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

