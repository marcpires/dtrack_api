# swagger_client.PolicyApi

All URIs are relative to */api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**add_project_to_policy**](PolicyApi.md#add_project_to_policy) | **POST** /v1/policy/{policyUuid}/project/{projectUuid} | Adds a project to a policy
[**add_tag_to_policy**](PolicyApi.md#add_tag_to_policy) | **POST** /v1/policy/{policyUuid}/tag/{tagName} | Adds a tag to a policy
[**create_policy**](PolicyApi.md#create_policy) | **PUT** /v1/policy | Creates a new policy
[**delete_policy**](PolicyApi.md#delete_policy) | **DELETE** /v1/policy/{uuid} | Deletes a policy
[**get_policies**](PolicyApi.md#get_policies) | **GET** /v1/policy | Returns a list of all policies
[**get_policy**](PolicyApi.md#get_policy) | **GET** /v1/policy/{uuid} | Returns a specific policy
[**remove_project_from_policy**](PolicyApi.md#remove_project_from_policy) | **DELETE** /v1/policy/{policyUuid}/project/{projectUuid} | Removes a project from a policy
[**remove_tag_from_policy**](PolicyApi.md#remove_tag_from_policy) | **DELETE** /v1/policy/{policyUuid}/tag/{tagName} | Removes a tag from a policy
[**update_policy**](PolicyApi.md#update_policy) | **POST** /v1/policy | Updates a policy

# **add_project_to_policy**
> Policy add_project_to_policy(policy_uuid, project_uuid)

Adds a project to a policy

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
api_instance = swagger_client.PolicyApi(swagger_client.ApiClient(configuration))
policy_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | The UUID of the policy to add a project to
project_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | The UUID of the project to add to the rule

try:
    # Adds a project to a policy
    api_response = api_instance.add_project_to_policy(policy_uuid, project_uuid)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling PolicyApi->add_project_to_policy: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **policy_uuid** | [**str**](.md)| The UUID of the policy to add a project to | 
 **project_uuid** | [**str**](.md)| The UUID of the project to add to the rule | 

### Return type

[**Policy**](Policy.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **add_tag_to_policy**
> Policy add_tag_to_policy(policy_uuid, tag_name)

Adds a tag to a policy

<p><strong>Deprecated</strong>. Use <code>POST /api/v1/tag/{name}/policy</code> instead.</p> <p>Requires permission <strong>POLICY_MANAGEMENT</strong></p> 

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
api_instance = swagger_client.PolicyApi(swagger_client.ApiClient(configuration))
policy_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | The UUID of the policy to add a project to
tag_name = 'tag_name_example' # str | The name of the tag to add to the rule

try:
    # Adds a tag to a policy
    api_response = api_instance.add_tag_to_policy(policy_uuid, tag_name)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling PolicyApi->add_tag_to_policy: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **policy_uuid** | [**str**](.md)| The UUID of the policy to add a project to | 
 **tag_name** | **str**| The name of the tag to add to the rule | 

### Return type

[**Policy**](Policy.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_policy**
> Policy create_policy(body=body)

Creates a new policy

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
api_instance = swagger_client.PolicyApi(swagger_client.ApiClient(configuration))
body = swagger_client.Policy() # Policy |  (optional)

try:
    # Creates a new policy
    api_response = api_instance.create_policy(body=body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling PolicyApi->create_policy: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**Policy**](Policy.md)|  | [optional] 

### Return type

[**Policy**](Policy.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_policy**
> delete_policy(uuid)

Deletes a policy

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
api_instance = swagger_client.PolicyApi(swagger_client.ApiClient(configuration))
uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | The UUID of the policy to delete

try:
    # Deletes a policy
    api_instance.delete_policy(uuid)
except ApiException as e:
    print("Exception when calling PolicyApi->delete_policy: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uuid** | [**str**](.md)| The UUID of the policy to delete | 

### Return type

void (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_policies**
> list[Policy] get_policies(page_number=page_number, page_size=page_size, offset=offset, limit=limit, sort_name=sort_name, sort_order=sort_order)

Returns a list of all policies

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
api_instance = swagger_client.PolicyApi(swagger_client.ApiClient(configuration))
page_number = '1' # str | The page to return. To be used in conjunction with <code>pageSize</code>. (optional) (default to 1)
page_size = '100' # str | Number of elements to return per page. To be used in conjunction with <code>pageNumber</code>. (optional) (default to 100)
offset = 'offset_example' # str | Offset to start returning elements from. To be used in conjunction with <code>limit</code>. (optional)
limit = 'limit_example' # str | Number of elements to return per page. To be used in conjunction with <code>offset</code>. (optional)
sort_name = 'sort_name_example' # str | Name of the resource field to sort on. (optional)
sort_order = 'sort_order_example' # str | Ordering of items when sorting with <code>sortName</code>. (optional)

try:
    # Returns a list of all policies
    api_response = api_instance.get_policies(page_number=page_number, page_size=page_size, offset=offset, limit=limit, sort_name=sort_name, sort_order=sort_order)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling PolicyApi->get_policies: %s\n" % e)
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

[**list[Policy]**](Policy.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_policy**
> Policy get_policy(uuid)

Returns a specific policy

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
api_instance = swagger_client.PolicyApi(swagger_client.ApiClient(configuration))
uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | The UUID of the policy to retrieve

try:
    # Returns a specific policy
    api_response = api_instance.get_policy(uuid)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling PolicyApi->get_policy: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uuid** | [**str**](.md)| The UUID of the policy to retrieve | 

### Return type

[**Policy**](Policy.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **remove_project_from_policy**
> Policy remove_project_from_policy(policy_uuid, project_uuid)

Removes a project from a policy

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
api_instance = swagger_client.PolicyApi(swagger_client.ApiClient(configuration))
policy_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | The UUID of the policy to remove the project from
project_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | The UUID of the project to remove from the policy

try:
    # Removes a project from a policy
    api_response = api_instance.remove_project_from_policy(policy_uuid, project_uuid)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling PolicyApi->remove_project_from_policy: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **policy_uuid** | [**str**](.md)| The UUID of the policy to remove the project from | 
 **project_uuid** | [**str**](.md)| The UUID of the project to remove from the policy | 

### Return type

[**Policy**](Policy.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **remove_tag_from_policy**
> Policy remove_tag_from_policy(policy_uuid, tag_name)

Removes a tag from a policy

<p><strong>Deprecated</strong>. Use <code>DELETE /api/v1/tag/{name}/policy</code> instead.</p> <p>Requires permission <strong>POLICY_MANAGEMENT</strong></p> 

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
api_instance = swagger_client.PolicyApi(swagger_client.ApiClient(configuration))
policy_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | The UUID of the policy to remove the tag from
tag_name = 'tag_name_example' # str | The name of the tag to remove from the policy

try:
    # Removes a tag from a policy
    api_response = api_instance.remove_tag_from_policy(policy_uuid, tag_name)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling PolicyApi->remove_tag_from_policy: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **policy_uuid** | [**str**](.md)| The UUID of the policy to remove the tag from | 
 **tag_name** | **str**| The name of the tag to remove from the policy | 

### Return type

[**Policy**](Policy.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_policy**
> Policy update_policy(body=body)

Updates a policy

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
api_instance = swagger_client.PolicyApi(swagger_client.ApiClient(configuration))
body = swagger_client.Policy() # Policy |  (optional)

try:
    # Updates a policy
    api_response = api_instance.update_policy(body=body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling PolicyApi->update_policy: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**Policy**](Policy.md)|  | [optional] 

### Return type

[**Policy**](Policy.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

