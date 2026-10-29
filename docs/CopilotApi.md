# CopilotApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**copilotAskCopilotAQuestion**](CopilotApi.md#copilotAskCopilotAQuestion) | **GET** /v1/copilot/ask | Ask Copilot a question |
| [**copilotAskCopilotAQuestionPost**](CopilotApi.md#copilotAskCopilotAQuestionPost) | **POST** /v1/copilot/ask | Ask Copilot a question (POST) |
| [**copilotCopilotScraperHealthCheck**](CopilotApi.md#copilotCopilotScraperHealthCheck) | **GET** /v1/copilot/health | Copilot scraper health check |
| [**copilotCopilotScraperHealthCheckHead**](CopilotApi.md#copilotCopilotScraperHealthCheckHead) | **HEAD** /v1/copilot/health | Copilot scraper health check |
| [**copilotListCopilotMarkets**](CopilotApi.md#copilotListCopilotMarkets) | **GET** /v1/copilot/markets | List Copilot markets |
| [**copilotMeasureABrandSVisibilityInACopilotAnswer**](CopilotApi.md#copilotMeasureABrandSVisibilityInACopilotAnswer) | **GET** /v1/copilot/brand-visibility | Measure a brand&#39;s visibility in a Copilot answer |
| [**copilotMeasureABrandSVisibilityInACopilotAnswerPost**](CopilotApi.md#copilotMeasureABrandSVisibilityInACopilotAnswerPost) | **POST** /v1/copilot/brand-visibility | Measure a brand&#39;s visibility in a Copilot answer (POST) |


<a id="copilotAskCopilotAQuestion"></a>
# **copilotAskCopilotAQuestion**
> Object copilotAskCopilotAQuestion(prompt, country, market, strictCountry)

Ask Copilot a question

Ask Microsoft Copilot (Copilot Search in Bing) and get the answer plus its cited sources.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.CopilotApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    CopilotApi apiInstance = new CopilotApi(defaultClient);
    String prompt = "prompt_example"; // String | The prompt to send to Copilot (max 2000 characters).
    String country = "country_example"; // String | ISO-3166 alpha-2 country to ask from, e.g. 'JP', 'US', 'GB'. Unless `market` is set, Copilot also answers in that country's market.
    String market = "market_example"; // String | Bing market (language-COUNTRY), e.g. 'ja-JP', 'en-GB'. Defaults to the country's.
    Boolean strictCountry = false; // Boolean | Answer only from an exit in `country`, never another one; 503 `country_unavailable` (not billed) when none answers. Requires `country`.
    try {
      Object result = apiInstance.copilotAskCopilotAQuestion(prompt, country, market, strictCountry);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CopilotApi#copilotAskCopilotAQuestion");
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
| **prompt** | **String**| The prompt to send to Copilot (max 2000 characters). | |
| **country** | **String**| ISO-3166 alpha-2 country to ask from, e.g. &#39;JP&#39;, &#39;US&#39;, &#39;GB&#39;. Unless &#x60;market&#x60; is set, Copilot also answers in that country&#39;s market. | [optional] |
| **market** | **String**| Bing market (language-COUNTRY), e.g. &#39;ja-JP&#39;, &#39;en-GB&#39;. Defaults to the country&#39;s. | [optional] |
| **strictCountry** | **Boolean**| Answer only from an exit in &#x60;country&#x60;, never another one; 503 &#x60;country_unavailable&#x60; (not billed) when none answers. Requires &#x60;country&#x60;. | [optional] [default to false] |

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

<a id="copilotAskCopilotAQuestionPost"></a>
# **copilotAskCopilotAQuestionPost**
> Object copilotAskCopilotAQuestionPost()

Ask Copilot a question (POST)

POST form of &#x60;/ask&#x60;, for prompts too long for a query string.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.CopilotApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    CopilotApi apiInstance = new CopilotApi(defaultClient);
    try {
      Object result = apiInstance.copilotAskCopilotAQuestionPost();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CopilotApi#copilotAskCopilotAQuestionPost");
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

<a id="copilotCopilotScraperHealthCheck"></a>
# **copilotCopilotScraperHealthCheck**
> Object copilotCopilotScraperHealthCheck()

Copilot scraper health check

Check health of the Copilot scraper service (accepts HEAD).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.CopilotApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    CopilotApi apiInstance = new CopilotApi(defaultClient);
    try {
      Object result = apiInstance.copilotCopilotScraperHealthCheck();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CopilotApi#copilotCopilotScraperHealthCheck");
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

<a id="copilotCopilotScraperHealthCheckHead"></a>
# **copilotCopilotScraperHealthCheckHead**
> Object copilotCopilotScraperHealthCheckHead()

Copilot scraper health check

Check health of the Copilot scraper service (accepts HEAD).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.CopilotApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    CopilotApi apiInstance = new CopilotApi(defaultClient);
    try {
      Object result = apiInstance.copilotCopilotScraperHealthCheckHead();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CopilotApi#copilotCopilotScraperHealthCheckHead");
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

<a id="copilotListCopilotMarkets"></a>
# **copilotListCopilotMarkets**
> Object copilotListCopilotMarkets()

List Copilot markets

The Bing markets Copilot can be asked in.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.CopilotApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    CopilotApi apiInstance = new CopilotApi(defaultClient);
    try {
      Object result = apiInstance.copilotListCopilotMarkets();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CopilotApi#copilotListCopilotMarkets");
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

<a id="copilotMeasureABrandSVisibilityInACopilotAnswer"></a>
# **copilotMeasureABrandSVisibilityInACopilotAnswer**
> Object copilotMeasureABrandSVisibilityInACopilotAnswer(prompt, brand, domain, aliases, competitors, country, market, strictCountry)

Measure a brand&#39;s visibility in a Copilot answer

Ask Copilot, then report whether the brand is mentioned, cited and how prominently.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.CopilotApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    CopilotApi apiInstance = new CopilotApi(defaultClient);
    String prompt = "prompt_example"; // String | The prompt to ask Copilot.
    String brand = "brand_example"; // String | Brand name to look for in the answer.
    String domain = "domain_example"; // String | Brand domain, for citation matching.
    String aliases = "aliases_example"; // String | Comma-separated alternative names.
    String competitors = "competitors_example"; // String | Comma-separated competitor names.
    String country = "country_example"; // String | ISO-3166 alpha-2 country to ask from, e.g. 'JP', 'US', 'GB'. Unless `market` is set, Copilot also answers in that country's market.
    String market = "market_example"; // String | Bing market (language-COUNTRY), e.g. 'ja-JP', 'en-GB'. Defaults to the country's.
    Boolean strictCountry = false; // Boolean | Answer only from an exit in `country`, never another one; 503 `country_unavailable` (not billed) when none answers. Requires `country`.
    try {
      Object result = apiInstance.copilotMeasureABrandSVisibilityInACopilotAnswer(prompt, brand, domain, aliases, competitors, country, market, strictCountry);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CopilotApi#copilotMeasureABrandSVisibilityInACopilotAnswer");
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
| **prompt** | **String**| The prompt to ask Copilot. | |
| **brand** | **String**| Brand name to look for in the answer. | |
| **domain** | **String**| Brand domain, for citation matching. | [optional] |
| **aliases** | **String**| Comma-separated alternative names. | [optional] |
| **competitors** | **String**| Comma-separated competitor names. | [optional] |
| **country** | **String**| ISO-3166 alpha-2 country to ask from, e.g. &#39;JP&#39;, &#39;US&#39;, &#39;GB&#39;. Unless &#x60;market&#x60; is set, Copilot also answers in that country&#39;s market. | [optional] |
| **market** | **String**| Bing market (language-COUNTRY), e.g. &#39;ja-JP&#39;, &#39;en-GB&#39;. Defaults to the country&#39;s. | [optional] |
| **strictCountry** | **Boolean**| Answer only from an exit in &#x60;country&#x60;, never another one; 503 &#x60;country_unavailable&#x60; (not billed) when none answers. Requires &#x60;country&#x60;. | [optional] [default to false] |

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

<a id="copilotMeasureABrandSVisibilityInACopilotAnswerPost"></a>
# **copilotMeasureABrandSVisibilityInACopilotAnswerPost**
> Object copilotMeasureABrandSVisibilityInACopilotAnswerPost()

Measure a brand&#39;s visibility in a Copilot answer (POST)

POST form, for longer prompts and larger competitor sets.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.CopilotApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    CopilotApi apiInstance = new CopilotApi(defaultClient);
    try {
      Object result = apiInstance.copilotMeasureABrandSVisibilityInACopilotAnswerPost();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CopilotApi#copilotMeasureABrandSVisibilityInACopilotAnswerPost");
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

