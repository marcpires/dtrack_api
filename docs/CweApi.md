# swagger_client.CweApi

All URIs are relative to */api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_cwe**](CweApi.md#get_cwe) | **GET** /v1/cwe/{cweId} | Returns a specific CWE
[**get_cwes**](CweApi.md#get_cwes) | **GET** /v1/cwe | Returns a list of all CWEs

# **get_cwe**
> Cwe get_cwe(cwe_id)

Returns a specific CWE

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
api_instance = swagger_client.CweApi(swagger_client.ApiClient(configuration))
cwe_id = 56 # int | The CWE ID of the CWE to retrieve

try:
    # Returns a specific CWE
    api_response = api_instance.get_cwe(cwe_id)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling CweApi->get_cwe: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **cwe_id** | **int**| The CWE ID of the CWE to retrieve | 

### Return type

[**Cwe**](Cwe.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_cwes**
> list[Cwe] get_cwes(page_number=page_number, page_size=page_size, offset=offset, limit=limit, sort_name=sort_name, sort_order=sort_order)

Returns a list of all CWEs

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
api_instance = swagger_client.CweApi(swagger_client.ApiClient(configuration))
page_number = '1' # str | The page to return. To be used in conjunction with <code>pageSize</code>. (optional) (default to 1)
page_size = '100' # str | Number of elements to return per page. To be used in conjunction with <code>pageNumber</code>. (optional) (default to 100)
offset = 'offset_example' # str | Offset to start returning elements from. To be used in conjunction with <code>limit</code>. (optional)
limit = 'limit_example' # str | Number of elements to return per page. To be used in conjunction with <code>offset</code>. (optional)
sort_name = 'sort_name_example' # str | Name of the resource field to sort on. (optional)
sort_order = 'sort_order_example' # str | Ordering of items when sorting with <code>sortName</code>. (optional)

try:
    # Returns a list of all CWEs
    api_response = api_instance.get_cwes(page_number=page_number, page_size=page_size, offset=offset, limit=limit, sort_name=sort_name, sort_order=sort_order)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling CweApi->get_cwes: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page_number** | **str**| The page to return. To be used in conjunction with &lt;code&gt;pageSize&lt;/code&gt;. | [optional] [default to 1]
 **page_size** | **str**| Number of elements to return per page. To be used in conjunction with &lt;code&gt;pageNumber&lt;/code&gt;. | [optional] [default to 100]
 **offset** | **str**| Offset to start returning elements from. To be used in conjunction with &lt;code&gt;limit&lt;/code&gt;. | [optional] 
 **limit** | **str**| Number of elements to return per page. To be used in conjunction with &lt;code&gt;offset&lt;/code&gt;. | [optional] 
 **sort_name** | **str**| Name of the resource field to sort on. | [optional] 
 **sort_order** | **str**| Ordering of items when sorting with &lt;code&gt;sortName&lt;/code&gt;. | [optional] 

### Return type

[**list[Cwe]**](Cwe.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

