# swagger_client.ComponentPropertyApi

All URIs are relative to */api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_property**](ComponentPropertyApi.md#create_property) | **PUT** /v1/component/{uuid}/property | Creates a new component property
[**delete_property**](ComponentPropertyApi.md#delete_property) | **DELETE** /v1/component/{uuid}/property/{propertyUuid} | Deletes a config property
[**get_properties**](ComponentPropertyApi.md#get_properties) | **GET** /v1/component/{uuid}/property | Returns a list of all properties for the specified component

# **create_property**
> ComponentProperty create_property(uuid, body=body)

Creates a new component property

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
api_instance = swagger_client.ComponentPropertyApi(swagger_client.ApiClient(configuration))
uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | The UUID of the component to create a property for
body = swagger_client.ComponentProperty() # ComponentProperty |  (optional)

try:
    # Creates a new component property
    api_response = api_instance.create_property(uuid, body=body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling ComponentPropertyApi->create_property: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uuid** | [**str**](.md)| The UUID of the component to create a property for | 
 **body** | [**ComponentProperty**](ComponentProperty.md)|  | [optional] 

### Return type

[**ComponentProperty**](ComponentProperty.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_property**
> delete_property(uuid, property_uuid)

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
api_instance = swagger_client.ComponentPropertyApi(swagger_client.ApiClient(configuration))
uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | The UUID of the component to delete a property from
property_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | The UUID of the component property to delete

try:
    # Deletes a config property
    api_instance.delete_property(uuid, property_uuid)
except ApiException as e:
    print("Exception when calling ComponentPropertyApi->delete_property: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uuid** | [**str**](.md)| The UUID of the component to delete a property from | 
 **property_uuid** | [**str**](.md)| The UUID of the component property to delete | 

### Return type

void (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_properties**
> list[ComponentProperty] get_properties(uuid)

Returns a list of all properties for the specified component

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
api_instance = swagger_client.ComponentPropertyApi(swagger_client.ApiClient(configuration))
uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | The UUID of the component to retrieve properties for

try:
    # Returns a list of all properties for the specified component
    api_response = api_instance.get_properties(uuid)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling ComponentPropertyApi->get_properties: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uuid** | [**str**](.md)| The UUID of the component to retrieve properties for | 

### Return type

[**list[ComponentProperty]**](ComponentProperty.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

