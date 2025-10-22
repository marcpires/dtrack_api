# swagger_client.IntegrationApi

All URIs are relative to */api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_all_ecosystems**](IntegrationApi.md#get_all_ecosystems) | **GET** /v1/integration/osv/ecosystem | Returns a list of all ecosystems in OSV
[**get_inactive_ecosystems**](IntegrationApi.md#get_inactive_ecosystems) | **GET** /v1/integration/osv/ecosystem/inactive | Returns a list of available inactive ecosystems in OSV to be selected by user

# **get_all_ecosystems**
> list[str] get_all_ecosystems()

Returns a list of all ecosystems in OSV

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
api_instance = swagger_client.IntegrationApi(swagger_client.ApiClient(configuration))

try:
    # Returns a list of all ecosystems in OSV
    api_response = api_instance.get_all_ecosystems()
    pprint(api_response)
except ApiException as e:
    print("Exception when calling IntegrationApi->get_all_ecosystems: %s\n" % e)
```

### Parameters
This endpoint does not need any parameter.

### Return type

**list[str]**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_inactive_ecosystems**
> list[str] get_inactive_ecosystems()

Returns a list of available inactive ecosystems in OSV to be selected by user

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
api_instance = swagger_client.IntegrationApi(swagger_client.ApiClient(configuration))

try:
    # Returns a list of available inactive ecosystems in OSV to be selected by user
    api_response = api_instance.get_inactive_ecosystems()
    pprint(api_response)
except ApiException as e:
    print("Exception when calling IntegrationApi->get_inactive_ecosystems: %s\n" % e)
```

### Parameters
This endpoint does not need any parameter.

### Return type

**list[str]**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

