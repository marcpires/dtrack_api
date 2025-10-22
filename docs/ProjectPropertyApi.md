# swagger_client.ProjectPropertyApi

All URIs are relative to */api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_property1**](ProjectPropertyApi.md#create_property1) | **PUT** /v1/project/{uuid}/property | Creates a new project property
[**delete_property1**](ProjectPropertyApi.md#delete_property1) | **DELETE** /v1/project/{uuid}/property | Deletes a config property
[**get_properties1**](ProjectPropertyApi.md#get_properties1) | **GET** /v1/project/{uuid}/property | Returns a list of all ProjectProperties for the specified project
[**update_property**](ProjectPropertyApi.md#update_property) | **POST** /v1/project/{uuid}/property | Updates a project property

# **create_property1**
> ProjectProperty create_property1(uuid, body=body)

Creates a new project property

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
api_instance = swagger_client.ProjectPropertyApi(swagger_client.ApiClient(configuration))
uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | The UUID of the project to create a property for
body = swagger_client.ProjectProperty() # ProjectProperty |  (optional)

try:
    # Creates a new project property
    api_response = api_instance.create_property1(uuid, body=body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling ProjectPropertyApi->create_property1: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uuid** | [**str**](.md)| The UUID of the project to create a property for | 
 **body** | [**ProjectProperty**](ProjectProperty.md)|  | [optional] 

### Return type

[**ProjectProperty**](ProjectProperty.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_property1**
> delete_property1(uuid, body=body)

Deletes a config property

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
api_instance = swagger_client.ProjectPropertyApi(swagger_client.ApiClient(configuration))
uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | The UUID of the project to delete a property from
body = swagger_client.ProjectProperty() # ProjectProperty |  (optional)

try:
    # Deletes a config property
    api_instance.delete_property1(uuid, body=body)
except ApiException as e:
    print("Exception when calling ProjectPropertyApi->delete_property1: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uuid** | [**str**](.md)| The UUID of the project to delete a property from | 
 **body** | [**ProjectProperty**](ProjectProperty.md)|  | [optional] 

### Return type

void (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_properties1**
> list[ProjectProperty] get_properties1(uuid)

Returns a list of all ProjectProperties for the specified project

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
api_instance = swagger_client.ProjectPropertyApi(swagger_client.ApiClient(configuration))
uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | The UUID of the project to retrieve properties for

try:
    # Returns a list of all ProjectProperties for the specified project
    api_response = api_instance.get_properties1(uuid)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling ProjectPropertyApi->get_properties1: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uuid** | [**str**](.md)| The UUID of the project to retrieve properties for | 

### Return type

[**list[ProjectProperty]**](ProjectProperty.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_property**
> ProjectProperty update_property(uuid, body=body)

Updates a project property

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
api_instance = swagger_client.ProjectPropertyApi(swagger_client.ApiClient(configuration))
uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | The UUID of the project to create a property for
body = swagger_client.ProjectProperty() # ProjectProperty |  (optional)

try:
    # Updates a project property
    api_response = api_instance.update_property(uuid, body=body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling ProjectPropertyApi->update_property: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uuid** | [**str**](.md)| The UUID of the project to create a property for | 
 **body** | [**ProjectProperty**](ProjectProperty.md)|  | [optional] 

### Return type

[**ProjectProperty**](ProjectProperty.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

