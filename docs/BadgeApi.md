# swagger_client.BadgeApi

All URIs are relative to */api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_project_policy_violations_badge**](BadgeApi.md#get_project_policy_violations_badge) | **GET** /v1/badge/violations/project/{uuid} | Returns a policy violations badge for a specific project
[**get_project_policy_violations_badge1**](BadgeApi.md#get_project_policy_violations_badge1) | **GET** /v1/badge/violations/project/{name}/{version} | Returns a policy violations badge for a specific project
[**get_project_vulnerabilities_badge**](BadgeApi.md#get_project_vulnerabilities_badge) | **GET** /v1/badge/vulns/project/{uuid} | Returns current metrics for a specific project
[**get_project_vulnerabilities_badge1**](BadgeApi.md#get_project_vulnerabilities_badge1) | **GET** /v1/badge/vulns/project/{name}/{version} | Returns current metrics for a specific project

# **get_project_policy_violations_badge**
> str get_project_policy_violations_badge(uuid)

Returns a policy violations badge for a specific project

<p>Requires permission <strong>VIEW_BADGES</strong></p>

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
# Configure API key authorization: ApiKeyQueryAuth
configuration = swagger_client.Configuration()
configuration.api_key['apiKey'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['apiKey'] = 'Bearer'

# create an instance of the API class
api_instance = swagger_client.BadgeApi(swagger_client.ApiClient(configuration))
uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | The UUID of the project to retrieve a badge for

try:
    # Returns a policy violations badge for a specific project
    api_response = api_instance.get_project_policy_violations_badge(uuid)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling BadgeApi->get_project_policy_violations_badge: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uuid** | [**str**](.md)| The UUID of the project to retrieve a badge for | 

### Return type

**str**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [ApiKeyQueryAuth](../README.md#ApiKeyQueryAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: image/svg+xml

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_project_policy_violations_badge1**
> str get_project_policy_violations_badge1(name, version)

Returns a policy violations badge for a specific project

<p>Requires permission <strong>VIEW_BADGES</strong></p>

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
# Configure API key authorization: ApiKeyQueryAuth
configuration = swagger_client.Configuration()
configuration.api_key['apiKey'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['apiKey'] = 'Bearer'

# create an instance of the API class
api_instance = swagger_client.BadgeApi(swagger_client.ApiClient(configuration))
name = 'name_example' # str | The name of the project to query on
version = 'version_example' # str | The version of the project to query on

try:
    # Returns a policy violations badge for a specific project
    api_response = api_instance.get_project_policy_violations_badge1(name, version)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling BadgeApi->get_project_policy_violations_badge1: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **name** | **str**| The name of the project to query on | 
 **version** | **str**| The version of the project to query on | 

### Return type

**str**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [ApiKeyQueryAuth](../README.md#ApiKeyQueryAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: image/svg+xml

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_project_vulnerabilities_badge**
> str get_project_vulnerabilities_badge(uuid)

Returns current metrics for a specific project

<p>Requires permission <strong>VIEW_BADGES</strong></p>

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
# Configure API key authorization: ApiKeyQueryAuth
configuration = swagger_client.Configuration()
configuration.api_key['apiKey'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['apiKey'] = 'Bearer'

# create an instance of the API class
api_instance = swagger_client.BadgeApi(swagger_client.ApiClient(configuration))
uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | The UUID of the project to retrieve metrics for

try:
    # Returns current metrics for a specific project
    api_response = api_instance.get_project_vulnerabilities_badge(uuid)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling BadgeApi->get_project_vulnerabilities_badge: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uuid** | [**str**](.md)| The UUID of the project to retrieve metrics for | 

### Return type

**str**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [ApiKeyQueryAuth](../README.md#ApiKeyQueryAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: image/svg+xml

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_project_vulnerabilities_badge1**
> str get_project_vulnerabilities_badge1(name, version)

Returns current metrics for a specific project

<p>Requires permission <strong>VIEW_BADGES</strong></p>

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
# Configure API key authorization: ApiKeyQueryAuth
configuration = swagger_client.Configuration()
configuration.api_key['apiKey'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['apiKey'] = 'Bearer'

# create an instance of the API class
api_instance = swagger_client.BadgeApi(swagger_client.ApiClient(configuration))
name = 'name_example' # str | The name of the project to query on
version = 'version_example' # str | The version of the project to query on

try:
    # Returns current metrics for a specific project
    api_response = api_instance.get_project_vulnerabilities_badge1(name, version)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling BadgeApi->get_project_vulnerabilities_badge1: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **name** | **str**| The name of the project to query on | 
 **version** | **str**| The version of the project to query on | 

### Return type

**str**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [ApiKeyQueryAuth](../README.md#ApiKeyQueryAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: image/svg+xml

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

