# WebApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**webDetectAntiBotAndCaptchaSystems**](WebApi.md#webDetectAntiBotAndCaptchaSystems) | **POST** /v1/web/detect | Detect anti-bot and CAPTCHA systems |
| [**webExtractStructuredData**](WebApi.md#webExtractStructuredData) | **POST** /v1/web/extract | Extract structured data |
| [**webPollAnAutoUnblockDiscoveryJob**](WebApi.md#webPollAnAutoUnblockDiscoveryJob) | **GET** /v1/web/unblock/{job_id} | Poll an auto-unblock discovery job |
| [**webScrapeAUrl**](WebApi.md#webScrapeAUrl) | **POST** /v1/web/scrape | Scrape a URL |
| [**webTakeAScreenshot**](WebApi.md#webTakeAScreenshot) | **POST** /v1/web/screenshot | Take a screenshot |
| [**webWebScraperHealthCheck**](WebApi.md#webWebScraperHealthCheck) | **GET** /v1/web/health | Web scraper health check |
| [**webWebScraperHealthCheckHead**](WebApi.md#webWebScraperHealthCheckHead) | **HEAD** /v1/web/health | Web scraper health check |


<a id="webDetectAntiBotAndCaptchaSystems"></a>
# **webDetectAntiBotAndCaptchaSystems**
> Object webDetectAntiBotAndCaptchaSystems()

Detect anti-bot and CAPTCHA systems

Detect which anti-bot and CAPTCHA systems are present on a URL.  Uses rnet to fetch the page and identify DataDome, Cloudflare, Akamai, Kasada, Amazon WAF, reCAPTCHA, hCaptcha, GeeTest, and more. Cost: 1 credit.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.WebApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    WebApi apiInstance = new WebApi(defaultClient);
    try {
      Object result = apiInstance.webDetectAntiBotAndCaptchaSystems();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WebApi#webDetectAntiBotAndCaptchaSystems");
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

<a id="webExtractStructuredData"></a>
# **webExtractStructuredData**
> Object webExtractStructuredData(extractRequest)

Extract structured data

Scrape a URL and extract fields with CSS/XPath selectors and/or AI.  &#x60;&#x60;extract_rules&#x60;&#x60; maps a field to a selector and returns &#x60;&#x60;data&#x60;&#x60;; &#x60;&#x60;ai_extract_rules&#x60;&#x60; (field -&gt; description) and &#x60;&#x60;ai_query&#x60;&#x60; return &#x60;&#x60;ai_extraction&#x60;&#x60;. Billed as a scrape, plus the AI extraction credits when AI is asked for and succeeds.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.WebApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    WebApi apiInstance = new WebApi(defaultClient);
    ExtractRequest extractRequest = new ExtractRequest(); // ExtractRequest | 
    try {
      Object result = apiInstance.webExtractStructuredData(extractRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WebApi#webExtractStructuredData");
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
| **extractRequest** | [**ExtractRequest**](ExtractRequest.md)|  | |

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

<a id="webPollAnAutoUnblockDiscoveryJob"></a>
# **webPollAnAutoUnblockDiscoveryJob**
> Object webPollAnAutoUnblockDiscoveryJob(jobId)

Poll an auto-unblock discovery job

Return the status + progress narration for an auto-unblock job.  Polled by the playground loader. &#x60;&#x60;job_id&#x60;&#x60; is an unguessable UUID handed out in the &#x60;&#x60;202 unblocking&#x60;&#x60; envelope and acts as a capability token, so any authenticated caller holding it can read the job (this is what lets several users share one discovery run&#39;s loader).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.WebApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    WebApi apiInstance = new WebApi(defaultClient);
    String jobId = "jobId_example"; // String | 
    try {
      Object result = apiInstance.webPollAnAutoUnblockDiscoveryJob(jobId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WebApi#webPollAnAutoUnblockDiscoveryJob");
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
| **jobId** | **String**|  | |

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

<a id="webScrapeAUrl"></a>
# **webScrapeAUrl**
> Object webScrapeAUrl()

Scrape a URL

Scrape a URL and return its content.  The Generic Web Scraping API is fully user-driven: callers pick their own request parameters (engine, proxy tier, country, JS rendering, …). A blocked target surfaces the raw 422 &#x60;&#x60;blocking_page_detected&#x60;&#x60; so the caller can tune parameters themselves — we do NOT auto-trigger host discovery. Curated per-origin overrides (which the dedicated scraper APIs depend on) still apply.  One exception, added for SB-001083/SCR-64: a plain &#x60;&#x60;google.com/search&#x60;&#x60; web-SERP fetch is served by the dedicated Google scraper, whose rotation loop is built for SearchGuard. Same request shape, same response shape, billed at what it actually cost — the caller sees only a better hit rate. &#x60;&#x60;serp_adapter&#x60;&#x60; fails closed, so any request carrying a parameter it does not recognise as route-or-cost takes the generic path unchanged, and the user-driven contract above still holds.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.WebApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    WebApi apiInstance = new WebApi(defaultClient);
    try {
      Object result = apiInstance.webScrapeAUrl();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WebApi#webScrapeAUrl");
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

<a id="webTakeAScreenshot"></a>
# **webTakeAScreenshot**
> Object webTakeAScreenshot(screenshotRequest)

Take a screenshot

Render a URL in the browser engine and return a PNG screenshot.  &#x60;&#x60;screenshot&#x60;&#x60; is the PNG, base64-encoded. &#x60;&#x60;width&#x60;&#x60;/&#x60;&#x60;height&#x60;&#x60; set the viewport; &#x60;&#x60;full_page&#x60;&#x60; captures the whole scrollable page. Billed as a browser scrape (plus the proxy tier); a page that loads without a screenshot is a 502 and costs nothing.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.WebApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    WebApi apiInstance = new WebApi(defaultClient);
    ScreenshotRequest screenshotRequest = new ScreenshotRequest(); // ScreenshotRequest | 
    try {
      Object result = apiInstance.webTakeAScreenshot(screenshotRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WebApi#webTakeAScreenshot");
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
| **screenshotRequest** | [**ScreenshotRequest**](ScreenshotRequest.md)|  | |

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

<a id="webWebScraperHealthCheck"></a>
# **webWebScraperHealthCheck**
> Object webWebScraperHealthCheck()

Web scraper health check

Check health of the web scraper service.  Bypasses the proxy abstraction because web-scraper exposes &#x60;&#x60;/health&#x60;&#x60; at the root (no &#x60;&#x60;/api/v1&#x60;&#x60; prefix, unlike the other scraper services).  Accepts &#x60;&#x60;HEAD&#x60;&#x60; so external uptime checkers (UptimeRobot uses HEAD by default for HTTP monitors) don&#39;t get a 405 Method Not Allowed.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.WebApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    WebApi apiInstance = new WebApi(defaultClient);
    try {
      Object result = apiInstance.webWebScraperHealthCheck();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WebApi#webWebScraperHealthCheck");
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

<a id="webWebScraperHealthCheckHead"></a>
# **webWebScraperHealthCheckHead**
> Object webWebScraperHealthCheckHead()

Web scraper health check

Check health of the web scraper service.  Bypasses the proxy abstraction because web-scraper exposes &#x60;&#x60;/health&#x60;&#x60; at the root (no &#x60;&#x60;/api/v1&#x60;&#x60; prefix, unlike the other scraper services).  Accepts &#x60;&#x60;HEAD&#x60;&#x60; so external uptime checkers (UptimeRobot uses HEAD by default for HTTP monitors) don&#39;t get a 405 Method Not Allowed.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.WebApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    WebApi apiInstance = new WebApi(defaultClient);
    try {
      Object result = apiInstance.webWebScraperHealthCheckHead();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WebApi#webWebScraperHealthCheckHead");
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

