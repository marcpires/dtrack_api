# swagger_client.VersionApi

All URIs are relative to */api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_version**](VersionApi.md#get_version) | **GET** /version | Returns application version information

# **get_version**
> About get_version()

Returns application version information

Returns a simple json object containing the name of the application and the version

### Example
```python
from __future__ import print_function
import time
import swagger_client
from swagger_client.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = swagger_client.VersionApi()

try:
    # Returns application version information
    api_response = api_instance.get_version()
    pprint(api_response)
except ApiException as e:
    print("Exception when calling VersionApi->get_version: %s\n" % e)
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**About**](About.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

