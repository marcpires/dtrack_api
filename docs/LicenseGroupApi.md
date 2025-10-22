# swagger_client.LicenseGroupApi

All URIs are relative to */api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**add_license_to_license_group**](LicenseGroupApi.md#add_license_to_license_group) | **POST** /v1/licenseGroup/{uuid}/license/{licenseUuid} | Adds the license to the specified license group.
[**create_license_group**](LicenseGroupApi.md#create_license_group) | **PUT** /v1/licenseGroup | Creates a new license group
[**delete_license_group**](LicenseGroupApi.md#delete_license_group) | **DELETE** /v1/licenseGroup/{uuid} | Deletes a license group
[**get_license_group**](LicenseGroupApi.md#get_license_group) | **GET** /v1/licenseGroup/{uuid} | Returns a specific license group
[**get_license_groups**](LicenseGroupApi.md#get_license_groups) | **GET** /v1/licenseGroup | Returns a list of all license groups
[**remove_license_from_license_group**](LicenseGroupApi.md#remove_license_from_license_group) | **DELETE** /v1/licenseGroup/{uuid}/license/{licenseUuid} | Removes the license from the license group.
[**update_license_group**](LicenseGroupApi.md#update_license_group) | **POST** /v1/licenseGroup | Updates a license group

# **add_license_to_license_group**
> LicenseGroup add_license_to_license_group(uuid, license_uuid)

Adds the license to the specified license group.

<p>Requires permission <strong>POLICY_MANAGEMENT</strong></p>

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
api_instance = swagger_client.LicenseGroupApi(swagger_client.ApiClient(configuration))
uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | A valid license group
license_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | A valid license

try:
    # Adds the license to the specified license group.
    api_response = api_instance.add_license_to_license_group(uuid, license_uuid)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling LicenseGroupApi->add_license_to_license_group: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uuid** | [**str**](.md)| A valid license group | 
 **license_uuid** | [**str**](.md)| A valid license | 

### Return type

[**LicenseGroup**](LicenseGroup.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_license_group**
> LicenseGroup create_license_group(body=body)

Creates a new license group

<p>Requires permission <strong>POLICY_MANAGEMENT</strong></p>

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
api_instance = swagger_client.LicenseGroupApi(swagger_client.ApiClient(configuration))
body = swagger_client.LicenseGroup() # LicenseGroup |  (optional)

try:
    # Creates a new license group
    api_response = api_instance.create_license_group(body=body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling LicenseGroupApi->create_license_group: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**LicenseGroup**](LicenseGroup.md)|  | [optional] 

### Return type

[**LicenseGroup**](LicenseGroup.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_license_group**
> delete_license_group(uuid)

Deletes a license group

<p>Requires permission <strong>POLICY_MANAGEMENT</strong></p>

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
api_instance = swagger_client.LicenseGroupApi(swagger_client.ApiClient(configuration))
uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | The UUID of the license group to delete

try:
    # Deletes a license group
    api_instance.delete_license_group(uuid)
except ApiException as e:
    print("Exception when calling LicenseGroupApi->delete_license_group: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uuid** | [**str**](.md)| The UUID of the license group to delete | 

### Return type

void (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_license_group**
> LicenseGroup get_license_group(uuid)

Returns a specific license group

<p>Requires permission <strong>POLICY_MANAGEMENT</strong></p>

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
api_instance = swagger_client.LicenseGroupApi(swagger_client.ApiClient(configuration))
uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | The UUID of the license group to retrieve

try:
    # Returns a specific license group
    api_response = api_instance.get_license_group(uuid)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling LicenseGroupApi->get_license_group: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uuid** | [**str**](.md)| The UUID of the license group to retrieve | 

### Return type

[**LicenseGroup**](LicenseGroup.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_license_groups**
> list[LicenseGroup] get_license_groups(page_number=page_number, page_size=page_size, offset=offset, limit=limit, sort_name=sort_name, sort_order=sort_order)

Returns a list of all license groups

<p>Requires permission <strong>POLICY_MANAGEMENT</strong></p>

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
api_instance = swagger_client.LicenseGroupApi(swagger_client.ApiClient(configuration))
page_number = '1' # str | The page to return. To be used in conjunction with <code>pageSize</code>. (optional) (default to 1)
page_size = '100' # str | Number of elements to return per page. To be used in conjunction with <code>pageNumber</code>. (optional) (default to 100)
offset = 'offset_example' # str | Offset to start returning elements from. To be used in conjunction with <code>limit</code>. (optional)
limit = 'limit_example' # str | Number of elements to return per page. To be used in conjunction with <code>offset</code>. (optional)
sort_name = 'sort_name_example' # str | Name of the resource field to sort on. (optional)
sort_order = 'sort_order_example' # str | Ordering of items when sorting with <code>sortName</code>. (optional)

try:
    # Returns a list of all license groups
    api_response = api_instance.get_license_groups(page_number=page_number, page_size=page_size, offset=offset, limit=limit, sort_name=sort_name, sort_order=sort_order)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling LicenseGroupApi->get_license_groups: %s\n" % e)
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

[**list[LicenseGroup]**](LicenseGroup.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **remove_license_from_license_group**
> LicenseGroup remove_license_from_license_group(uuid, license_uuid)

Removes the license from the license group.

<p>Requires permission <strong>POLICY_MANAGEMENT</strong></p>

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
api_instance = swagger_client.LicenseGroupApi(swagger_client.ApiClient(configuration))
uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | A valid license group
license_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | A valid license

try:
    # Removes the license from the license group.
    api_response = api_instance.remove_license_from_license_group(uuid, license_uuid)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling LicenseGroupApi->remove_license_from_license_group: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uuid** | [**str**](.md)| A valid license group | 
 **license_uuid** | [**str**](.md)| A valid license | 

### Return type

[**LicenseGroup**](LicenseGroup.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_license_group**
> LicenseGroup update_license_group(body=body)

Updates a license group

<p>Requires permission <strong>POLICY_MANAGEMENT</strong></p>

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
api_instance = swagger_client.LicenseGroupApi(swagger_client.ApiClient(configuration))
body = swagger_client.LicenseGroup() # LicenseGroup |  (optional)

try:
    # Updates a license group
    api_response = api_instance.update_license_group(body=body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling LicenseGroupApi->update_license_group: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**LicenseGroup**](LicenseGroup.md)|  | [optional] 

### Return type

[**LicenseGroup**](LicenseGroup.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

