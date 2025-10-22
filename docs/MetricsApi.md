# swagger_client.MetricsApi

All URIs are relative to */api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_component_current_metrics**](MetricsApi.md#get_component_current_metrics) | **GET** /v1/metrics/component/{uuid}/current | Returns current metrics for a specific component
[**get_component_metrics_since**](MetricsApi.md#get_component_metrics_since) | **GET** /v1/metrics/component/{uuid}/since/{date} | Returns historical metrics for a specific component from a specific date
[**get_component_metrics_x_days**](MetricsApi.md#get_component_metrics_x_days) | **GET** /v1/metrics/component/{uuid}/days/{days} | Returns X days of historical metrics for a specific component
[**get_portfolio_current_metrics**](MetricsApi.md#get_portfolio_current_metrics) | **GET** /v1/metrics/portfolio/current | Returns current metrics for the entire portfolio
[**get_portfolio_metrics_since**](MetricsApi.md#get_portfolio_metrics_since) | **GET** /v1/metrics/portfolio/since/{date} | Returns historical metrics for the entire portfolio from a specific date
[**get_portfolio_metrics_x_days**](MetricsApi.md#get_portfolio_metrics_x_days) | **GET** /v1/metrics/portfolio/{days}/days | Returns X days of historical metrics for the entire portfolio
[**get_project_current_metrics**](MetricsApi.md#get_project_current_metrics) | **GET** /v1/metrics/project/{uuid}/current | Returns current metrics for a specific project
[**get_project_metrics_since**](MetricsApi.md#get_project_metrics_since) | **GET** /v1/metrics/project/{uuid}/since/{date} | Returns historical metrics for a specific project from a specific date
[**get_project_metrics_x_days**](MetricsApi.md#get_project_metrics_x_days) | **GET** /v1/metrics/project/{uuid}/days/{days} | Returns X days of historical metrics for a specific project
[**get_vulnerability_metrics**](MetricsApi.md#get_vulnerability_metrics) | **GET** /v1/metrics/vulnerability | Returns the sum of all vulnerabilities in the database by year and month
[**refresh_component_metrics**](MetricsApi.md#refresh_component_metrics) | **GET** /v1/metrics/component/{uuid}/refresh | Requests a refresh of a specific components metrics
[**refresh_portfolio_metrics**](MetricsApi.md#refresh_portfolio_metrics) | **GET** /v1/metrics/portfolio/refresh | Requests a refresh of the portfolio metrics
[**refresh_project_metrics**](MetricsApi.md#refresh_project_metrics) | **GET** /v1/metrics/project/{uuid}/refresh | Requests a refresh of a specific projects metrics

# **get_component_current_metrics**
> DependencyMetrics get_component_current_metrics(uuid)

Returns current metrics for a specific component

<p>Requires permission <strong>VIEW_PORTFOLIO</strong></p>

### Example
```python
from __future__ import print_function
import time
import swagger_client
from swagger_client.rest import ApiException
from pprint import pprint

# Configure API key authorization: ApiKeyAuth
configuration = swagger_client.Configuration()
configuration.api_key['X-Api-Key'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['X-Api-Key'] = 'Bearer'

# create an instance of the API class
api_instance = swagger_client.MetricsApi(swagger_client.ApiClient(configuration))
uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | The UUID of the component to retrieve metrics for

try:
    # Returns current metrics for a specific component
    api_response = api_instance.get_component_current_metrics(uuid)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling MetricsApi->get_component_current_metrics: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uuid** | [**str**](.md)| The UUID of the component to retrieve metrics for | 

### Return type

[**DependencyMetrics**](DependencyMetrics.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_component_metrics_since**
> list[DependencyMetrics] get_component_metrics_since(uuid, _date)

Returns historical metrics for a specific component from a specific date

<p>Date format must be <code>YYYYMMDD</code></p> <p>Requires permission <strong>VIEW_PORTFOLIO</strong></p>

### Example
```python
from __future__ import print_function
import time
import swagger_client
from swagger_client.rest import ApiException
from pprint import pprint

# Configure API key authorization: ApiKeyAuth
configuration = swagger_client.Configuration()
configuration.api_key['X-Api-Key'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['X-Api-Key'] = 'Bearer'

# create an instance of the API class
api_instance = swagger_client.MetricsApi(swagger_client.ApiClient(configuration))
uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | The UUID of the component to retrieve metrics for
_date = '_date_example' # str | The start date to retrieve metrics for

try:
    # Returns historical metrics for a specific component from a specific date
    api_response = api_instance.get_component_metrics_since(uuid, _date)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling MetricsApi->get_component_metrics_since: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uuid** | [**str**](.md)| The UUID of the component to retrieve metrics for | 
 **_date** | **str**| The start date to retrieve metrics for | 

### Return type

[**list[DependencyMetrics]**](DependencyMetrics.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_component_metrics_x_days**
> list[DependencyMetrics] get_component_metrics_x_days(uuid, days)

Returns X days of historical metrics for a specific component

<p>Requires permission <strong>VIEW_PORTFOLIO</strong></p>

### Example
```python
from __future__ import print_function
import time
import swagger_client
from swagger_client.rest import ApiException
from pprint import pprint

# Configure API key authorization: ApiKeyAuth
configuration = swagger_client.Configuration()
configuration.api_key['X-Api-Key'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['X-Api-Key'] = 'Bearer'

# create an instance of the API class
api_instance = swagger_client.MetricsApi(swagger_client.ApiClient(configuration))
uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | The UUID of the component to retrieve metrics for
days = 56 # int | The number of days back to retrieve metrics for

try:
    # Returns X days of historical metrics for a specific component
    api_response = api_instance.get_component_metrics_x_days(uuid, days)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling MetricsApi->get_component_metrics_x_days: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uuid** | [**str**](.md)| The UUID of the component to retrieve metrics for | 
 **days** | **int**| The number of days back to retrieve metrics for | 

### Return type

[**list[DependencyMetrics]**](DependencyMetrics.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_portfolio_current_metrics**
> PortfolioMetrics get_portfolio_current_metrics()

Returns current metrics for the entire portfolio

<p>Requires permission <strong>VIEW_PORTFOLIO</strong></p>

### Example
```python
from __future__ import print_function
import time
import swagger_client
from swagger_client.rest import ApiException
from pprint import pprint

# Configure API key authorization: ApiKeyAuth
configuration = swagger_client.Configuration()
configuration.api_key['X-Api-Key'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['X-Api-Key'] = 'Bearer'

# create an instance of the API class
api_instance = swagger_client.MetricsApi(swagger_client.ApiClient(configuration))

try:
    # Returns current metrics for the entire portfolio
    api_response = api_instance.get_portfolio_current_metrics()
    pprint(api_response)
except ApiException as e:
    print("Exception when calling MetricsApi->get_portfolio_current_metrics: %s\n" % e)
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**PortfolioMetrics**](PortfolioMetrics.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_portfolio_metrics_since**
> list[PortfolioMetrics] get_portfolio_metrics_since(_date)

Returns historical metrics for the entire portfolio from a specific date

<p>Date format must be <code>YYYYMMDD</code></p> <p>Requires permission <strong>VIEW_PORTFOLIO</strong></p>

### Example
```python
from __future__ import print_function
import time
import swagger_client
from swagger_client.rest import ApiException
from pprint import pprint

# Configure API key authorization: ApiKeyAuth
configuration = swagger_client.Configuration()
configuration.api_key['X-Api-Key'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['X-Api-Key'] = 'Bearer'

# create an instance of the API class
api_instance = swagger_client.MetricsApi(swagger_client.ApiClient(configuration))
_date = '_date_example' # str | The start date to retrieve metrics for

try:
    # Returns historical metrics for the entire portfolio from a specific date
    api_response = api_instance.get_portfolio_metrics_since(_date)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling MetricsApi->get_portfolio_metrics_since: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **_date** | **str**| The start date to retrieve metrics for | 

### Return type

[**list[PortfolioMetrics]**](PortfolioMetrics.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_portfolio_metrics_x_days**
> list[PortfolioMetrics] get_portfolio_metrics_x_days(days)

Returns X days of historical metrics for the entire portfolio

<p>Requires permission <strong>VIEW_PORTFOLIO</strong></p>

### Example
```python
from __future__ import print_function
import time
import swagger_client
from swagger_client.rest import ApiException
from pprint import pprint

# Configure API key authorization: ApiKeyAuth
configuration = swagger_client.Configuration()
configuration.api_key['X-Api-Key'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['X-Api-Key'] = 'Bearer'

# create an instance of the API class
api_instance = swagger_client.MetricsApi(swagger_client.ApiClient(configuration))
days = 56 # int | The number of days back to retrieve metrics for

try:
    # Returns X days of historical metrics for the entire portfolio
    api_response = api_instance.get_portfolio_metrics_x_days(days)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling MetricsApi->get_portfolio_metrics_x_days: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **days** | **int**| The number of days back to retrieve metrics for | 

### Return type

[**list[PortfolioMetrics]**](PortfolioMetrics.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_project_current_metrics**
> ProjectMetrics get_project_current_metrics(uuid)

Returns current metrics for a specific project

<p>Requires permission <strong>VIEW_PORTFOLIO</strong></p>

### Example
```python
from __future__ import print_function
import time
import swagger_client
from swagger_client.rest import ApiException
from pprint import pprint

# Configure API key authorization: ApiKeyAuth
configuration = swagger_client.Configuration()
configuration.api_key['X-Api-Key'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['X-Api-Key'] = 'Bearer'

# create an instance of the API class
api_instance = swagger_client.MetricsApi(swagger_client.ApiClient(configuration))
uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | The UUID of the project to retrieve metrics for

try:
    # Returns current metrics for a specific project
    api_response = api_instance.get_project_current_metrics(uuid)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling MetricsApi->get_project_current_metrics: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uuid** | [**str**](.md)| The UUID of the project to retrieve metrics for | 

### Return type

[**ProjectMetrics**](ProjectMetrics.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_project_metrics_since**
> list[ProjectMetrics] get_project_metrics_since(uuid, _date)

Returns historical metrics for a specific project from a specific date

<p>Date format must be <code>YYYYMMDD</code></p> <p>Requires permission <strong>VIEW_PORTFOLIO</strong></p>

### Example
```python
from __future__ import print_function
import time
import swagger_client
from swagger_client.rest import ApiException
from pprint import pprint

# Configure API key authorization: ApiKeyAuth
configuration = swagger_client.Configuration()
configuration.api_key['X-Api-Key'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['X-Api-Key'] = 'Bearer'

# create an instance of the API class
api_instance = swagger_client.MetricsApi(swagger_client.ApiClient(configuration))
uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | The UUID of the project to retrieve metrics for
_date = '_date_example' # str | The start date to retrieve metrics for

try:
    # Returns historical metrics for a specific project from a specific date
    api_response = api_instance.get_project_metrics_since(uuid, _date)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling MetricsApi->get_project_metrics_since: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uuid** | [**str**](.md)| The UUID of the project to retrieve metrics for | 
 **_date** | **str**| The start date to retrieve metrics for | 

### Return type

[**list[ProjectMetrics]**](ProjectMetrics.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_project_metrics_x_days**
> list[ProjectMetrics] get_project_metrics_x_days(uuid, days)

Returns X days of historical metrics for a specific project

<p>Requires permission <strong>VIEW_PORTFOLIO</strong></p>

### Example
```python
from __future__ import print_function
import time
import swagger_client
from swagger_client.rest import ApiException
from pprint import pprint

# Configure API key authorization: ApiKeyAuth
configuration = swagger_client.Configuration()
configuration.api_key['X-Api-Key'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['X-Api-Key'] = 'Bearer'

# create an instance of the API class
api_instance = swagger_client.MetricsApi(swagger_client.ApiClient(configuration))
uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | The UUID of the project to retrieve metrics for
days = 56 # int | The number of days back to retrieve metrics for

try:
    # Returns X days of historical metrics for a specific project
    api_response = api_instance.get_project_metrics_x_days(uuid, days)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling MetricsApi->get_project_metrics_x_days: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uuid** | [**str**](.md)| The UUID of the project to retrieve metrics for | 
 **days** | **int**| The number of days back to retrieve metrics for | 

### Return type

[**list[ProjectMetrics]**](ProjectMetrics.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_vulnerability_metrics**
> list[VulnerabilityMetrics] get_vulnerability_metrics()

Returns the sum of all vulnerabilities in the database by year and month

<p>Requires permission <strong>VIEW_PORTFOLIO</strong></p>

### Example
```python
from __future__ import print_function
import time
import swagger_client
from swagger_client.rest import ApiException
from pprint import pprint

# Configure API key authorization: ApiKeyAuth
configuration = swagger_client.Configuration()
configuration.api_key['X-Api-Key'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['X-Api-Key'] = 'Bearer'

# create an instance of the API class
api_instance = swagger_client.MetricsApi(swagger_client.ApiClient(configuration))

try:
    # Returns the sum of all vulnerabilities in the database by year and month
    api_response = api_instance.get_vulnerability_metrics()
    pprint(api_response)
except ApiException as e:
    print("Exception when calling MetricsApi->get_vulnerability_metrics: %s\n" % e)
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**list[VulnerabilityMetrics]**](VulnerabilityMetrics.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **refresh_component_metrics**
> refresh_component_metrics(uuid)

Requests a refresh of a specific components metrics

<p>Requires permission <strong>PORTFOLIO_MANAGEMENT</strong></p>

### Example
```python
from __future__ import print_function
import time
import swagger_client
from swagger_client.rest import ApiException
from pprint import pprint

# Configure API key authorization: ApiKeyAuth
configuration = swagger_client.Configuration()
configuration.api_key['X-Api-Key'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['X-Api-Key'] = 'Bearer'

# create an instance of the API class
api_instance = swagger_client.MetricsApi(swagger_client.ApiClient(configuration))
uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | The UUID of the component to refresh metrics on

try:
    # Requests a refresh of a specific components metrics
    api_instance.refresh_component_metrics(uuid)
except ApiException as e:
    print("Exception when calling MetricsApi->refresh_component_metrics: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uuid** | [**str**](.md)| The UUID of the component to refresh metrics on | 

### Return type

void (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **refresh_portfolio_metrics**
> refresh_portfolio_metrics()

Requests a refresh of the portfolio metrics

<p>Requires permission <strong>PORTFOLIO_MANAGEMENT</strong></p>

### Example
```python
from __future__ import print_function
import time
import swagger_client
from swagger_client.rest import ApiException
from pprint import pprint

# Configure API key authorization: ApiKeyAuth
configuration = swagger_client.Configuration()
configuration.api_key['X-Api-Key'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['X-Api-Key'] = 'Bearer'

# create an instance of the API class
api_instance = swagger_client.MetricsApi(swagger_client.ApiClient(configuration))

try:
    # Requests a refresh of the portfolio metrics
    api_instance.refresh_portfolio_metrics()
except ApiException as e:
    print("Exception when calling MetricsApi->refresh_portfolio_metrics: %s\n" % e)
```

### Parameters
This endpoint does not need any parameter.

### Return type

void (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **refresh_project_metrics**
> refresh_project_metrics(uuid)

Requests a refresh of a specific projects metrics

<p>Requires permission <strong>PORTFOLIO_MANAGEMENT</strong></p>

### Example
```python
from __future__ import print_function
import time
import swagger_client
from swagger_client.rest import ApiException
from pprint import pprint

# Configure API key authorization: ApiKeyAuth
configuration = swagger_client.Configuration()
configuration.api_key['X-Api-Key'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['X-Api-Key'] = 'Bearer'

# create an instance of the API class
api_instance = swagger_client.MetricsApi(swagger_client.ApiClient(configuration))
uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | The UUID of the project to refresh metrics on

try:
    # Requests a refresh of a specific projects metrics
    api_instance.refresh_project_metrics(uuid)
except ApiException as e:
    print("Exception when calling MetricsApi->refresh_project_metrics: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uuid** | [**str**](.md)| The UUID of the project to refresh metrics on | 

### Return type

void (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

