# RufusApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**rufusAmazonRufusScraperHealthCheck**](RufusApi.md#rufusAmazonRufusScraperHealthCheck) | **GET** /v1/rufus/health | Amazon Rufus scraper health check |
| [**rufusAmazonRufusScraperHealthCheckHead**](RufusApi.md#rufusAmazonRufusScraperHealthCheckHead) | **HEAD** /v1/rufus/health | Amazon Rufus scraper health check |
| [**rufusAskAmazonRufusAQuestion**](RufusApi.md#rufusAskAmazonRufusAQuestion) | **GET** /v1/rufus/ask | Ask Amazon Rufus a question |
| [**rufusAskAmazonRufusAQuestionPost**](RufusApi.md#rufusAskAmazonRufusAQuestionPost) | **POST** /v1/rufus/ask | Ask Amazon Rufus a question (POST) |
| [**rufusListAmazonRufusModels**](RufusApi.md#rufusListAmazonRufusModels) | **GET** /v1/rufus/models | List Amazon Rufus models |


<a id="rufusAmazonRufusScraperHealthCheck"></a>
# **rufusAmazonRufusScraperHealthCheck**
> Object rufusAmazonRufusScraperHealthCheck()

Amazon Rufus scraper health check

Check health of the Amazon service that serves Rufus (accepts HEAD).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.RufusApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    RufusApi apiInstance = new RufusApi(defaultClient);
    try {
      Object result = apiInstance.rufusAmazonRufusScraperHealthCheck();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling RufusApi#rufusAmazonRufusScraperHealthCheck");
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

<a id="rufusAmazonRufusScraperHealthCheckHead"></a>
# **rufusAmazonRufusScraperHealthCheckHead**
> Object rufusAmazonRufusScraperHealthCheckHead()

Amazon Rufus scraper health check

Check health of the Amazon service that serves Rufus (accepts HEAD).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.RufusApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    RufusApi apiInstance = new RufusApi(defaultClient);
    try {
      Object result = apiInstance.rufusAmazonRufusScraperHealthCheckHead();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling RufusApi#rufusAmazonRufusScraperHealthCheckHead");
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

<a id="rufusAskAmazonRufusAQuestion"></a>
# **rufusAskAmazonRufusAQuestion**
> Object rufusAskAmazonRufusAQuestion(prompt, asin)

Ask Amazon Rufus a question

Ask Alexa for Shopping (Rufus) and get its answer and product cards.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.RufusApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    RufusApi apiInstance = new RufusApi(defaultClient);
    String prompt = "prompt_example"; // String | The shopping question to ask (max 4000 characters).
    String asin = "asin_example"; // String | Optional product ASIN whose page should provide the shopping context.
    try {
      Object result = apiInstance.rufusAskAmazonRufusAQuestion(prompt, asin);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling RufusApi#rufusAskAmazonRufusAQuestion");
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
| **prompt** | **String**| The shopping question to ask (max 4000 characters). | |
| **asin** | **String**| Optional product ASIN whose page should provide the shopping context. | [optional] |

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

<a id="rufusAskAmazonRufusAQuestionPost"></a>
# **rufusAskAmazonRufusAQuestionPost**
> Object rufusAskAmazonRufusAQuestionPost(rufusAskRequest)

Ask Amazon Rufus a question (POST)

POST form of &#x60;/ask&#x60;, accepting prompt and optional asin in the JSON body.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.RufusApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    RufusApi apiInstance = new RufusApi(defaultClient);
    RufusAskRequest rufusAskRequest = new RufusAskRequest(); // RufusAskRequest | 
    try {
      Object result = apiInstance.rufusAskAmazonRufusAQuestionPost(rufusAskRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling RufusApi#rufusAskAmazonRufusAQuestionPost");
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
| **rufusAskRequest** | [**RufusAskRequest**](RufusAskRequest.md)|  | |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |

<a id="rufusListAmazonRufusModels"></a>
# **rufusListAmazonRufusModels**
> Object rufusListAmazonRufusModels()

List Amazon Rufus models

List the Amazon shopping assistant surface exposed by this API.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.RufusApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    RufusApi apiInstance = new RufusApi(defaultClient);
    try {
      Object result = apiInstance.rufusListAmazonRufusModels();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling RufusApi#rufusListAmazonRufusModels");
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

