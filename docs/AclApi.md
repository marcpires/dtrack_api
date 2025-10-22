# swagger_client.AclApi

All URIs are relative to */api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**add_mapping**](AclApi.md#add_mapping) | **PUT** /v1/acl/mapping | Adds an ACL mapping
[**delete_mapping**](AclApi.md#delete_mapping) | **DELETE** /v1/acl/mapping/team/{teamUuid}/project/{projectUuid} | Removes an ACL mapping
[**retrieve_projects**](AclApi.md#retrieve_projects) | **GET** /v1/acl/team/{uuid} | Returns the projects assigned to the specified team

# **add_mapping**
> add_mapping(body=body)

Adds an ACL mapping

<p>Requires permission <strong>ACCESS_MANAGEMENT</strong></p>

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
api_instance = swagger_client.AclApi(swagger_client.ApiClient(configuration))
body = swagger_client.AclMappingRequest() # AclMappingRequest |  (optional)

try:
    # Adds an ACL mapping
    api_instance.add_mapping(body=body)
except ApiException as e:
    print("Exception when calling AclApi->add_mapping: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**AclMappingRequest**](AclMappingRequest.md)|  | [optional] 

### Return type

void (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: */*
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_mapping**
> delete_mapping(team_uuid, project_uuid)

Removes an ACL mapping

<p>Requires permission <strong>ACCESS_MANAGEMENT</strong></p>

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
api_instance = swagger_client.AclApi(swagger_client.ApiClient(configuration))
team_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | The UUID of the team to delete the mapping for
project_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | The UUID of the project to delete the mapping for

try:
    # Removes an ACL mapping
    api_instance.delete_mapping(team_uuid, project_uuid)
except ApiException as e:
    print("Exception when calling AclApi->delete_mapping: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **team_uuid** | [**str**](.md)| The UUID of the team to delete the mapping for | 
 **project_uuid** | [**str**](.md)| The UUID of the project to delete the mapping for | 

### Return type

void (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **retrieve_projects**
> list[Project] retrieve_projects(uuid, page_number=page_number, page_size=page_size, offset=offset, limit=limit, sort_name=sort_name, sort_order=sort_order, exclude_inactive=exclude_inactive, only_root=only_root)

Returns the projects assigned to the specified team

<p>Requires permission <strong>ACCESS_MANAGEMENT</strong></p>

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
api_instance = swagger_client.AclApi(swagger_client.ApiClient(configuration))
uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | The UUID of the team to retrieve mappings for
page_number = '1' # str | The page to return. To be used in conjunction with <code>pageSize</code>. (optional) (default to 1)
page_size = '100' # str | Number of elements to return per page. To be used in conjunction with <code>pageNumber</code>. (optional) (default to 100)
offset = 'offset_example' # str | Offset to start returning elements from. To be used in conjunction with <code>limit</code>. (optional)
limit = 'limit_example' # str | Number of elements to return per page. To be used in conjunction with <code>offset</code>. (optional)
sort_name = 'sort_name_example' # str | Name of the resource field to sort on. (optional)
sort_order = 'sort_order_example' # str | Ordering of items when sorting with <code>sortName</code>. (optional)
exclude_inactive = true # bool | Optionally excludes inactive projects from being returned (optional)
only_root = true # bool | Optionally excludes children projects from being returned (optional)

try:
    # Returns the projects assigned to the specified team
    api_response = api_instance.retrieve_projects(uuid, page_number=page_number, page_size=page_size, offset=offset, limit=limit, sort_name=sort_name, sort_order=sort_order, exclude_inactive=exclude_inactive, only_root=only_root)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling AclApi->retrieve_projects: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uuid** | [**str**](.md)| The UUID of the team to retrieve mappings for | 
 **page_number** | **str**| The page to return. To be used in conjunction with &lt;code&gt;pageSize&lt;/code&gt;. | [optional] [default to 1]
 **page_size** | **str**| Number of elements to return per page. To be used in conjunction with &lt;code&gt;pageNumber&lt;/code&gt;. | [optional] [default to 100]
 **offset** | **str**| Offset to start returning elements from. To be used in conjunction with &lt;code&gt;limit&lt;/code&gt;. | [optional] 
 **limit** | **str**| Number of elements to return per page. To be used in conjunction with &lt;code&gt;offset&lt;/code&gt;. | [optional] 
 **sort_name** | **str**| Name of the resource field to sort on. | [optional] 
 **sort_order** | **str**| Ordering of items when sorting with &lt;code&gt;sortName&lt;/code&gt;. | [optional] 
 **exclude_inactive** | **bool**| Optionally excludes inactive projects from being returned | [optional] 
 **only_root** | **bool**| Optionally excludes children projects from being returned | [optional] 

### Return type

[**list[Project]**](Project.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

