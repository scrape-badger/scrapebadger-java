# LinkedInApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**linkedinGetACompanySJobPostings**](LinkedInApi.md#linkedinGetACompanySJobPostings) | **GET** /v1/linkedin/companies/{company_id}/jobs | Get a company&#39;s job postings |
| [**linkedinGetACourse**](LinkedInApi.md#linkedinGetACourse) | **GET** /v1/linkedin/learning/{course_slug} | Get a course |
| [**linkedinGetAPublicArticle**](LinkedInApi.md#linkedinGetAPublicArticle) | **GET** /v1/linkedin/articles/{article_slug} | Get a public article |
| [**linkedinGetAPublicPost**](LinkedInApi.md#linkedinGetAPublicPost) | **GET** /v1/linkedin/posts/{post_slug} | Get a public post |
| [**linkedinGetCompany**](LinkedInApi.md#linkedinGetCompany) | **GET** /v1/linkedin/companies/{universal_name} | Get company |
| [**linkedinGetJobDetail**](LinkedInApi.md#linkedinGetJobDetail) | **GET** /v1/linkedin/jobs/{job_id} | Get job detail |
| [**linkedinGetPublicProfile**](LinkedInApi.md#linkedinGetPublicProfile) | **GET** /v1/linkedin/profiles/{public_id} | Get public profile |
| [**linkedinGetSchool**](LinkedInApi.md#linkedinGetSchool) | **GET** /v1/linkedin/schools/{universal_name} | Get school |
| [**linkedinLinkedinScraperHealthCheck**](LinkedInApi.md#linkedinLinkedinScraperHealthCheck) | **GET** /v1/linkedin/health | LinkedIn scraper health check |
| [**linkedinLinkedinScraperHealthCheckHead**](LinkedInApi.md#linkedinLinkedinScraperHealthCheckHead) | **HEAD** /v1/linkedin/health | LinkedIn scraper health check |
| [**linkedinSearchLinkedinJobs**](LinkedInApi.md#linkedinSearchLinkedinJobs) | **GET** /v1/linkedin/jobs/search | Search LinkedIn jobs |
| [**linkedinSuggestLocationGeoIds**](LinkedInApi.md#linkedinSuggestLocationGeoIds) | **GET** /v1/linkedin/geo/suggest | Suggest location geo ids |


<a id="linkedinGetACompanySJobPostings"></a>
# **linkedinGetACompanySJobPostings**
> Object linkedinGetACompanySJobPostings(companyId, start, country)

Get a company&#39;s job postings

Public job postings for a company (numeric company id from the company endpoint).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.LinkedInApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    LinkedInApi apiInstance = new LinkedInApi(defaultClient);
    String companyId = "companyId_example"; // String | 
    Integer start = 0; // Integer | Pagination offset (0, 25, 50, ...)
    String country = "us"; // String | Residential proxy country
    try {
      Object result = apiInstance.linkedinGetACompanySJobPostings(companyId, start, country);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling LinkedInApi#linkedinGetACompanySJobPostings");
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
| **companyId** | **String**|  | |
| **start** | **Integer**| Pagination offset (0, 25, 50, ...) | [optional] [default to 0] |
| **country** | **String**| Residential proxy country | [optional] [default to us] |

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

<a id="linkedinGetACourse"></a>
# **linkedinGetACourse**
> Object linkedinGetACourse(courseSlug, country)

Get a course

A public LinkedIn Learning course — provider, workload, instructors, rating.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.LinkedInApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    LinkedInApi apiInstance = new LinkedInApi(defaultClient);
    String courseSlug = "courseSlug_example"; // String | 
    String country = "us"; // String | Residential proxy country
    try {
      Object result = apiInstance.linkedinGetACourse(courseSlug, country);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling LinkedInApi#linkedinGetACourse");
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
| **courseSlug** | **String**|  | |
| **country** | **String**| Residential proxy country | [optional] [default to us] |

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

<a id="linkedinGetAPublicArticle"></a>
# **linkedinGetAPublicArticle**
> Object linkedinGetAPublicArticle(articleSlug, country)

Get a public article

A public Pulse article — title, body, author, reactions (JSON-LD).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.LinkedInApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    LinkedInApi apiInstance = new LinkedInApi(defaultClient);
    String articleSlug = "articleSlug_example"; // String | 
    String country = "us"; // String | Residential proxy country
    try {
      Object result = apiInstance.linkedinGetAPublicArticle(articleSlug, country);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling LinkedInApi#linkedinGetAPublicArticle");
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
| **articleSlug** | **String**|  | |
| **country** | **String**| Residential proxy country | [optional] [default to us] |

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

<a id="linkedinGetAPublicPost"></a>
# **linkedinGetAPublicPost**
> Object linkedinGetAPublicPost(postSlug, country)

Get a public post

A public activity share — text, author, reactions, comments (JSON-LD).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.LinkedInApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    LinkedInApi apiInstance = new LinkedInApi(defaultClient);
    String postSlug = "postSlug_example"; // String | 
    String country = "us"; // String | Residential proxy country
    try {
      Object result = apiInstance.linkedinGetAPublicPost(postSlug, country);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling LinkedInApi#linkedinGetAPublicPost");
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
| **postSlug** | **String**|  | |
| **country** | **String**| Residential proxy country | [optional] [default to us] |

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

<a id="linkedinGetCompany"></a>
# **linkedinGetCompany**
> Object linkedinGetCompany(universalName, country)

Get company

Public company page — industry, size, HQ, followers, specialties (JSON-LD + SSR).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.LinkedInApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    LinkedInApi apiInstance = new LinkedInApi(defaultClient);
    String universalName = "universalName_example"; // String | 
    String country = "us"; // String | Residential proxy country
    try {
      Object result = apiInstance.linkedinGetCompany(universalName, country);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling LinkedInApi#linkedinGetCompany");
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
| **universalName** | **String**|  | |
| **country** | **String**| Residential proxy country | [optional] [default to us] |

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

<a id="linkedinGetJobDetail"></a>
# **linkedinGetJobDetail**
> Object linkedinGetJobDetail(jobId, country)

Get job detail

Full detail for one job posting (guest API, no login).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.LinkedInApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    LinkedInApi apiInstance = new LinkedInApi(defaultClient);
    String jobId = "jobId_example"; // String | 
    String country = "us"; // String | Residential proxy country
    try {
      Object result = apiInstance.linkedinGetJobDetail(jobId, country);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling LinkedInApi#linkedinGetJobDetail");
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
| **country** | **String**| Residential proxy country | [optional] [default to us] |

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

<a id="linkedinGetPublicProfile"></a>
# **linkedinGetPublicProfile**
> Object linkedinGetPublicProfile(publicId, country)

Get public profile

Public profile by vanity id (the &#x60;&#x60;/in/{public_id}&#x60;&#x60; slug) — name, headline, location, about, experience, education (public JSON-LD + SSR subset).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.LinkedInApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    LinkedInApi apiInstance = new LinkedInApi(defaultClient);
    String publicId = "publicId_example"; // String | 
    String country = "us"; // String | Residential proxy country
    try {
      Object result = apiInstance.linkedinGetPublicProfile(publicId, country);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling LinkedInApi#linkedinGetPublicProfile");
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
| **publicId** | **String**|  | |
| **country** | **String**| Residential proxy country | [optional] [default to us] |

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

<a id="linkedinGetSchool"></a>
# **linkedinGetSchool**
> Object linkedinGetSchool(universalName, country)

Get school

Public school page — name, description, website, follower/alumni counts.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.LinkedInApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    LinkedInApi apiInstance = new LinkedInApi(defaultClient);
    String universalName = "universalName_example"; // String | 
    String country = "us"; // String | Residential proxy country
    try {
      Object result = apiInstance.linkedinGetSchool(universalName, country);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling LinkedInApi#linkedinGetSchool");
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
| **universalName** | **String**|  | |
| **country** | **String**| Residential proxy country | [optional] [default to us] |

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

<a id="linkedinLinkedinScraperHealthCheck"></a>
# **linkedinLinkedinScraperHealthCheck**
> Object linkedinLinkedinScraperHealthCheck()

LinkedIn scraper health check

Check health of the LinkedIn scraper service (accepts HEAD).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.LinkedInApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    LinkedInApi apiInstance = new LinkedInApi(defaultClient);
    try {
      Object result = apiInstance.linkedinLinkedinScraperHealthCheck();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling LinkedInApi#linkedinLinkedinScraperHealthCheck");
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

<a id="linkedinLinkedinScraperHealthCheckHead"></a>
# **linkedinLinkedinScraperHealthCheckHead**
> Object linkedinLinkedinScraperHealthCheckHead()

LinkedIn scraper health check

Check health of the LinkedIn scraper service (accepts HEAD).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.LinkedInApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    LinkedInApi apiInstance = new LinkedInApi(defaultClient);
    try {
      Object result = apiInstance.linkedinLinkedinScraperHealthCheckHead();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling LinkedInApi#linkedinLinkedinScraperHealthCheckHead");
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

<a id="linkedinSearchLinkedinJobs"></a>
# **linkedinSearchLinkedinJobs**
> Object linkedinSearchLinkedinJobs(keywords, location, geoId, companyId, datePosted, experience, jobType, workplace, sort, start, country)

Search LinkedIn jobs

Search public LinkedIn job postings (guest API, no login).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.LinkedInApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    LinkedInApi apiInstance = new LinkedInApi(defaultClient);
    String keywords = "keywords_example"; // String | Job title / keywords
    String location = "location_example"; // String | Location text, e.g. 'New York'
    String geoId = "geoId_example"; // String | LinkedIn numeric geo id (overrides location)
    String companyId = "companyId_example"; // String | Restrict to a company (numeric id)
    String datePosted = "datePosted_example"; // String | past_24h | past_week | past_month | any
    String experience = "experience_example"; // String | internship|entry|associate|mid_senior|director|executive (comma-separated)
    String jobType = "jobType_example"; // String | full_time|part_time|contract|temporary|internship|volunteer|other
    String workplace = "workplace_example"; // String | onsite|remote|hybrid (comma-separated)
    String sort = "sort_example"; // String | relevant | recent
    Integer start = 0; // Integer | Pagination offset (0, 25, 50, ...)
    String country = "us"; // String | Residential proxy country
    try {
      Object result = apiInstance.linkedinSearchLinkedinJobs(keywords, location, geoId, companyId, datePosted, experience, jobType, workplace, sort, start, country);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling LinkedInApi#linkedinSearchLinkedinJobs");
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
| **keywords** | **String**| Job title / keywords | [optional] |
| **location** | **String**| Location text, e.g. &#39;New York&#39; | [optional] |
| **geoId** | **String**| LinkedIn numeric geo id (overrides location) | [optional] |
| **companyId** | **String**| Restrict to a company (numeric id) | [optional] |
| **datePosted** | **String**| past_24h | past_week | past_month | any | [optional] |
| **experience** | **String**| internship|entry|associate|mid_senior|director|executive (comma-separated) | [optional] |
| **jobType** | **String**| full_time|part_time|contract|temporary|internship|volunteer|other | [optional] |
| **workplace** | **String**| onsite|remote|hybrid (comma-separated) | [optional] |
| **sort** | **String**| relevant | recent | [optional] |
| **start** | **Integer**| Pagination offset (0, 25, 50, ...) | [optional] [default to 0] |
| **country** | **String**| Residential proxy country | [optional] [default to us] |

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

<a id="linkedinSuggestLocationGeoIds"></a>
# **linkedinSuggestLocationGeoIds**
> Object linkedinSuggestLocationGeoIds(query, type)

Suggest location geo ids

Resolve a name to LinkedIn ids (job-search &#x60;&#x60;geo_id&#x60;&#x60; / &#x60;&#x60;company_id&#x60;&#x60; helper).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.LinkedInApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    LinkedInApi apiInstance = new LinkedInApi(defaultClient);
    String query = "query_example"; // String | Location text, e.g. 'London'
    String type = "geo"; // String | geo | company
    try {
      Object result = apiInstance.linkedinSuggestLocationGeoIds(query, type);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling LinkedInApi#linkedinSuggestLocationGeoIds");
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
| **query** | **String**| Location text, e.g. &#39;London&#39; | |
| **type** | **String**| geo | company | [optional] [default to geo] |

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

