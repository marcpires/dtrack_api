# swagger_client.SearchApi

All URIs are relative to */api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**aggregate_search**](SearchApi.md#aggregate_search) | **GET** /v1/search | Processes and returns search results
[**component_search**](SearchApi.md#component_search) | **GET** /v1/search/component | Processes and returns search results
[**license_search**](SearchApi.md#license_search) | **GET** /v1/search/license | Processes and returns search results
[**project_search**](SearchApi.md#project_search) | **GET** /v1/search/project | Processes and returns search results
[**reindex**](SearchApi.md#reindex) | **POST** /v1/search/reindex | Rebuild lucene indexes for search operations
[**service_search**](SearchApi.md#service_search) | **GET** /v1/search/service | Processes and returns search results
[**vulnerability_search**](SearchApi.md#vulnerability_search) | **GET** /v1/search/vulnerability | Processes and returns search results
[**vulnerable_software_search**](SearchApi.md#vulnerable_software_search) | **GET** /v1/search/vulnerablesoftware | Processes and returns search results

# **aggregate_search**
> SearchResult aggregate_search(query=query)

Processes and returns search results

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
api_instance = swagger_client.SearchApi(swagger_client.ApiClient(configuration))
query = 'query_example' # str |  (optional)

try:
    # Processes and returns search results
    api_response = api_instance.aggregate_search(query=query)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling SearchApi->aggregate_search: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **query** | **str**|  | [optional] 

### Return type

[**SearchResult**](SearchResult.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **component_search**
> SearchResult component_search(query=query)

Processes and returns search results

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
api_instance = swagger_client.SearchApi(swagger_client.ApiClient(configuration))
query = 'query_example' # str |  (optional)

try:
    # Processes and returns search results
    api_response = api_instance.component_search(query=query)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling SearchApi->component_search: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **query** | **str**|  | [optional] 

### Return type

[**SearchResult**](SearchResult.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **license_search**
> SearchResult license_search(query=query)

Processes and returns search results

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
api_instance = swagger_client.SearchApi(swagger_client.ApiClient(configuration))
query = 'query_example' # str |  (optional)

try:
    # Processes and returns search results
    api_response = api_instance.license_search(query=query)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling SearchApi->license_search: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **query** | **str**|  | [optional] 

### Return type

[**SearchResult**](SearchResult.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **project_search**
> SearchResult project_search(query=query)

Processes and returns search results

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
api_instance = swagger_client.SearchApi(swagger_client.ApiClient(configuration))
query = 'query_example' # str |  (optional)

try:
    # Processes and returns search results
    api_response = api_instance.project_search(query=query)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling SearchApi->project_search: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **query** | **str**|  | [optional] 

### Return type

[**SearchResult**](SearchResult.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **reindex**
> BomUploadResponse reindex(type=type)

Rebuild lucene indexes for search operations

<p>Requires permission <strong>SYSTEM_CONFIGURATION</strong></p>

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
api_instance = swagger_client.SearchApi(swagger_client.ApiClient(configuration))
type = ['type_example'] # list[str] |  (optional)

try:
    # Rebuild lucene indexes for search operations
    api_response = api_instance.reindex(type=type)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling SearchApi->reindex: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **type** | [**list[str]**](str.md)|  | [optional] 

### Return type

[**BomUploadResponse**](BomUploadResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **service_search**
> SearchResult service_search(query=query)

Processes and returns search results

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
api_instance = swagger_client.SearchApi(swagger_client.ApiClient(configuration))
query = 'query_example' # str |  (optional)

try:
    # Processes and returns search results
    api_response = api_instance.service_search(query=query)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling SearchApi->service_search: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **query** | **str**|  | [optional] 

### Return type

[**SearchResult**](SearchResult.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **vulnerability_search**
> SearchResult vulnerability_search(query=query)

Processes and returns search results

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
api_instance = swagger_client.SearchApi(swagger_client.ApiClient(configuration))
query = 'query_example' # str |  (optional)

try:
    # Processes and returns search results
    api_response = api_instance.vulnerability_search(query=query)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling SearchApi->vulnerability_search: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **query** | **str**|  | [optional] 

### Return type

[**SearchResult**](SearchResult.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **vulnerable_software_search**
> SearchResult vulnerable_software_search(query=query, cpe=cpe)

Processes and returns search results

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
api_instance = swagger_client.SearchApi(swagger_client.ApiClient(configuration))
query = 'query_example' # str |  (optional)
cpe = 'cpe_example' # str |  (optional)

try:
    # Processes and returns search results
    api_response = api_instance.vulnerable_software_search(query=query, cpe=cpe)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling SearchApi->vulnerable_software_search: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **query** | **str**|  | [optional] 
 **cpe** | **str**|  | [optional] 

### Return type

[**SearchResult**](SearchResult.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

