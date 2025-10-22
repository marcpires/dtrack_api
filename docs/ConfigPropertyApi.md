# swagger_client.ConfigPropertyApi

All URIs are relative to */api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_config_properties**](ConfigPropertyApi.md#get_config_properties) | **GET** /v1/configProperty | Returns a list of all ConfigProperties for the specified groupName
[**get_public_config_property**](ConfigPropertyApi.md#get_public_config_property) | **GET** /v1/configProperty/public/{groupName}/{propertyName} | Returns a public ConfigProperty
[**update_config_property**](ConfigPropertyApi.md#update_config_property) | **POST** /v1/configProperty | Updates a config property
[**update_config_property1**](ConfigPropertyApi.md#update_config_property1) | **POST** /v1/configProperty/aggregate | Updates an array of config properties

# **get_config_properties**
> list[ConfigProperty] get_config_properties()

Returns a list of all ConfigProperties for the specified groupName

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
api_instance = swagger_client.ConfigPropertyApi(swagger_client.ApiClient(configuration))

try:
    # Returns a list of all ConfigProperties for the specified groupName
    api_response = api_instance.get_config_properties()
    pprint(api_response)
except ApiException as e:
    print("Exception when calling ConfigPropertyApi->get_config_properties: %s\n" % e)
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**list[ConfigProperty]**](ConfigProperty.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_public_config_property**
> ConfigProperty get_public_config_property(group_name, property_name)

Returns a public ConfigProperty

<p></p>

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
api_instance = swagger_client.ConfigPropertyApi(swagger_client.ApiClient(configuration))
group_name = 'group_name_example' # str | The group name of the value to retrieve
property_name = 'property_name_example' # str | The property name of the value to retrieve

try:
    # Returns a public ConfigProperty
    api_response = api_instance.get_public_config_property(group_name, property_name)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling ConfigPropertyApi->get_public_config_property: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **group_name** | **str**| The group name of the value to retrieve | 
 **property_name** | **str**| The property name of the value to retrieve | 

### Return type

[**ConfigProperty**](ConfigProperty.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_config_property**
> ConfigProperty update_config_property(body=body)

Updates a config property

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
api_instance = swagger_client.ConfigPropertyApi(swagger_client.ApiClient(configuration))
body = swagger_client.ConfigProperty() # ConfigProperty |  (optional)

try:
    # Updates a config property
    api_response = api_instance.update_config_property(body=body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling ConfigPropertyApi->update_config_property: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**ConfigProperty**](ConfigProperty.md)|  | [optional] 

### Return type

[**ConfigProperty**](ConfigProperty.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_config_property1**
> list[ConfigProperty] update_config_property1(body=body)

Updates an array of config properties

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
api_instance = swagger_client.ConfigPropertyApi(swagger_client.ApiClient(configuration))
body = [swagger_client.ConfigProperty()] # list[ConfigProperty] |  (optional)

try:
    # Updates an array of config properties
    api_response = api_instance.update_config_property1(body=body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling ConfigPropertyApi->update_config_property1: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**list[ConfigProperty]**](ConfigProperty.md)|  | [optional] 

### Return type

[**list[ConfigProperty]**](ConfigProperty.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

