# swagger_client.DependencyGraphApi

All URIs are relative to */api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_components_and_services_by_component_uuid**](DependencyGraphApi.md#get_components_and_services_by_component_uuid) | **GET** /v1/dependencyGraph/component/{uuid}/directDependencies | Returns a list of specific components and services from component UUID
[**get_components_and_services_by_project_uuid**](DependencyGraphApi.md#get_components_and_services_by_project_uuid) | **GET** /v1/dependencyGraph/project/{uuid}/directDependencies | Returns a list of specific components and services from project UUID

# **get_components_and_services_by_component_uuid**
> list[DependencyGraphResponse] get_components_and_services_by_component_uuid(uuid)

Returns a list of specific components and services from component UUID

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
api_instance = swagger_client.DependencyGraphApi(swagger_client.ApiClient(configuration))
uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | The UUID of the component

try:
    # Returns a list of specific components and services from component UUID
    api_response = api_instance.get_components_and_services_by_component_uuid(uuid)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling DependencyGraphApi->get_components_and_services_by_component_uuid: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uuid** | [**str**](.md)| The UUID of the component | 

### Return type

[**list[DependencyGraphResponse]**](DependencyGraphResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_components_and_services_by_project_uuid**
> list[DependencyGraphResponse] get_components_and_services_by_project_uuid(uuid)

Returns a list of specific components and services from project UUID

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
api_instance = swagger_client.DependencyGraphApi(swagger_client.ApiClient(configuration))
uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | The UUID of the project

try:
    # Returns a list of specific components and services from project UUID
    api_response = api_instance.get_components_and_services_by_project_uuid(uuid)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling DependencyGraphApi->get_components_and_services_by_project_uuid: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uuid** | [**str**](.md)| The UUID of the project | 

### Return type

[**list[DependencyGraphResponse]**](DependencyGraphResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

