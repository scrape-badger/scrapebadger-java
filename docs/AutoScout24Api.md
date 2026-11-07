# AutoScout24Api

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**autoscout24CheckAutoscout24Health**](AutoScout24Api.md#autoscout24CheckAutoscout24Health) | **GET** /v1/autoscout24/health | Check AutoScout24 health |
| [**autoscout24ListMarkets**](AutoScout24Api.md#autoscout24ListMarkets) | **GET** /v1/autoscout24/markets | List markets |
| [**autoscout24ListSearchFilters**](AutoScout24Api.md#autoscout24ListSearchFilters) | **GET** /v1/autoscout24/filters | List search filters |
| [**autoscout24SearchVehicles**](AutoScout24Api.md#autoscout24SearchVehicles) | **GET** /v1/autoscout24/search | Search vehicles |


<a id="autoscout24CheckAutoscout24Health"></a>
# **autoscout24CheckAutoscout24Health**
> Object autoscout24CheckAutoscout24Health()

Check AutoScout24 health

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.AutoScout24Api;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    AutoScout24Api apiInstance = new AutoScout24Api(defaultClient);
    try {
      Object result = apiInstance.autoscout24CheckAutoscout24Health();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AutoScout24Api#autoscout24CheckAutoscout24Health");
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

<a id="autoscout24ListMarkets"></a>
# **autoscout24ListMarkets**
> AutoScout24MarketsResponse autoscout24ListMarkets()

List markets

Verified marketplaces, domains, languages and currency. Free reference endpoint.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.AutoScout24Api;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    AutoScout24Api apiInstance = new AutoScout24Api(defaultClient);
    try {
      AutoScout24MarketsResponse result = apiInstance.autoscout24ListMarkets();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AutoScout24Api#autoscout24ListMarkets");
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

[**AutoScout24MarketsResponse**](AutoScout24MarketsResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |

<a id="autoscout24ListSearchFilters"></a>
# **autoscout24ListSearchFilters**
> AutoScout24FiltersResponse autoscout24ListSearchFilters(market, make)

List search filters

Current native make, model and vehicle filter options. Set make for its models.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.AutoScout24Api;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    AutoScout24Api apiInstance = new AutoScout24Api(defaultClient);
    String market = "de"; // String | 
    String make = "make_example"; // String | 
    try {
      AutoScout24FiltersResponse result = apiInstance.autoscout24ListSearchFilters(market, make);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AutoScout24Api#autoscout24ListSearchFilters");
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
| **market** | **String**|  | [optional] [default to de] [enum: de, at, be, es, fr, it, lu, nl] |
| **make** | **String**|  | [optional] |

### Return type

[**AutoScout24FiltersResponse**](AutoScout24FiltersResponse.md)

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

<a id="autoscout24SearchVehicles"></a>
# **autoscout24SearchVehicles**
> AutoScout24SearchResponse autoscout24SearchVehicles(market, make, model, priceMin, priceMax, mileageMin, mileageMax, yearMin, yearMax, powerMin, powerMax, fuelType, transmission, bodyType, sellerType, condition, zip, radius, sortBy, page)

Search vehicles

Search live vehicle cards, seller/location information and current filter taxonomy.  Browsing is capped at 200 pages (normally 20 cards each). Narrow the query to reach more inventory. Empty results cost zero credits. Listing detail is not included in this API.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.AutoScout24Api;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    AutoScout24Api apiInstance = new AutoScout24Api(defaultClient);
    String market = "de"; // String | 
    String make = "make_example"; // String | Native make slug, e.g. volkswagen or bmw.
    String model = "model_example"; // String | Native model slug, e.g. golf. Requires make.
    Integer priceMin = 56; // Integer | 
    Integer priceMax = 56; // Integer | 
    Integer mileageMin = 56; // Integer | Kilometres.
    Integer mileageMax = 56; // Integer | 
    Integer yearMin = 56; // Integer | 
    Integer yearMax = 56; // Integer | 
    Integer powerMin = 56; // Integer | Engine power in kW.
    Integer powerMax = 56; // Integer | 
    String fuelType = "petrol"; // String | 
    String transmission = "automatic"; // String | 
    String bodyType = "compact"; // String | 
    String sellerType = "dealer"; // String | 
    String condition = "new"; // String | 
    String zip = "zip_example"; // String | Postal code in the requested market.
    Integer radius = 56; // Integer | Kilometres; requires zip.
    String sortBy = "best_match"; // String | 
    Integer page = 1; // Integer | 
    try {
      AutoScout24SearchResponse result = apiInstance.autoscout24SearchVehicles(market, make, model, priceMin, priceMax, mileageMin, mileageMax, yearMin, yearMax, powerMin, powerMax, fuelType, transmission, bodyType, sellerType, condition, zip, radius, sortBy, page);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AutoScout24Api#autoscout24SearchVehicles");
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
| **market** | **String**|  | [optional] [default to de] [enum: de, at, be, es, fr, it, lu, nl] |
| **make** | **String**| Native make slug, e.g. volkswagen or bmw. | [optional] |
| **model** | **String**| Native model slug, e.g. golf. Requires make. | [optional] |
| **priceMin** | **Integer**|  | [optional] |
| **priceMax** | **Integer**|  | [optional] |
| **mileageMin** | **Integer**| Kilometres. | [optional] |
| **mileageMax** | **Integer**|  | [optional] |
| **yearMin** | **Integer**|  | [optional] |
| **yearMax** | **Integer**|  | [optional] |
| **powerMin** | **Integer**| Engine power in kW. | [optional] |
| **powerMax** | **Integer**|  | [optional] |
| **fuelType** | **String**|  | [optional] [enum: petrol, diesel, electric, hybrid_petrol, hybrid_diesel, cng, hydrogen, lpg, ethanol, other] |
| **transmission** | **String**|  | [optional] [enum: automatic, manual, semi_automatic] |
| **bodyType** | **String**|  | [optional] [enum: compact, convertible, coupe, suv, station_wagon, sedan, van, transporter, other] |
| **sellerType** | **String**|  | [optional] [enum: dealer, private] |
| **condition** | **String**|  | [optional] [enum: new, used, annual, classic, demo, day_registration] |
| **zip** | **String**| Postal code in the requested market. | [optional] |
| **radius** | **Integer**| Kilometres; requires zip. | [optional] |
| **sortBy** | **String**|  | [optional] [default to best_match] [enum: best_match, price_asc, price_desc, mileage_asc, mileage_desc, registration_asc, registration_desc, power_asc, power_desc, newest] |
| **page** | **Integer**|  | [optional] [default to 1] |

### Return type

[**AutoScout24SearchResponse**](AutoScout24SearchResponse.md)

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

