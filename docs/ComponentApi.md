# swagger_client.ComponentApi

All URIs are relative to */api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_component**](ComponentApi.md#create_component) | **PUT** /v1/component/project/{uuid} | Creates a new component
[**delete_component**](ComponentApi.md#delete_component) | **DELETE** /v1/component/{uuid} | Deletes a component
[**get_all_components**](ComponentApi.md#get_all_components) | **GET** /v1/component/project/{uuid} | Returns a list of all components for a given project
[**get_component_by_hash**](ComponentApi.md#get_component_by_hash) | **GET** /v1/component/hash/{hash} | Returns a list of components that have the specified hash value
[**get_component_by_identity**](ComponentApi.md#get_component_by_identity) | **GET** /v1/component/identity | Returns a list of components that have the specified component identity. This resource accepts coordinates (group, name, version) or purl, cpe, or swidTagId
[**get_component_by_uuid**](ComponentApi.md#get_component_by_uuid) | **GET** /v1/component/{uuid} | Returns a specific component
[**get_dependency_graph_for_component**](ComponentApi.md#get_dependency_graph_for_component) | **GET** /v1/component/project/{projectUuid}/dependencyGraph/{componentUuids} | Returns the expanded dependency graph to every occurrence of a component
[**identify_internal_components**](ComponentApi.md#identify_internal_components) | **GET** /v1/component/internal/identify | Requests the identification of internal components in the portfolio
[**update_component**](ComponentApi.md#update_component) | **POST** /v1/component | Updates a component

# **create_component**
> Component create_component(uuid, body=body)

Creates a new component

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
api_instance = swagger_client.ComponentApi(swagger_client.ApiClient(configuration))
uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | The UUID of the project to create a component for
body = swagger_client.Component() # Component |  (optional)

try:
    # Creates a new component
    api_response = api_instance.create_component(uuid, body=body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling ComponentApi->create_component: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uuid** | [**str**](.md)| The UUID of the project to create a component for | 
 **body** | [**Component**](Component.md)|  | [optional] 

### Return type

[**Component**](Component.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_component**
> delete_component(uuid)

Deletes a component

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
api_instance = swagger_client.ComponentApi(swagger_client.ApiClient(configuration))
uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | The UUID of the component to delete

try:
    # Deletes a component
    api_instance.delete_component(uuid)
except ApiException as e:
    print("Exception when calling ComponentApi->delete_component: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uuid** | [**str**](.md)| The UUID of the component to delete | 

### Return type

void (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_all_components**
> list[Component] get_all_components(uuid, page_number=page_number, page_size=page_size, offset=offset, limit=limit, sort_name=sort_name, sort_order=sort_order, only_outdated=only_outdated, only_direct=only_direct)

Returns a list of all components for a given project

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
api_instance = swagger_client.ComponentApi(swagger_client.ApiClient(configuration))
uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | The UUID of the project to retrieve components for
page_number = '1' # str | The page to return. To be used in conjunction with <code>pageSize</code>. (optional) (default to 1)
page_size = '100' # str | Number of elements to return per page. To be used in conjunction with <code>pageNumber</code>. (optional) (default to 100)
offset = 'offset_example' # str | Offset to start returning elements from. To be used in conjunction with <code>limit</code>. (optional)
limit = 'limit_example' # str | Number of elements to return per page. To be used in conjunction with <code>offset</code>. (optional)
sort_name = 'sort_name_example' # str | Name of the resource field to sort on. (optional)
sort_order = 'sort_order_example' # str | Ordering of items when sorting with <code>sortName</code>. (optional)
only_outdated = true # bool | Optionally exclude recent components so only outdated components are returned (optional)
only_direct = true # bool | Optionally exclude transitive dependencies so only direct dependencies are returned (optional)

try:
    # Returns a list of all components for a given project
    api_response = api_instance.get_all_components(uuid, page_number=page_number, page_size=page_size, offset=offset, limit=limit, sort_name=sort_name, sort_order=sort_order, only_outdated=only_outdated, only_direct=only_direct)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling ComponentApi->get_all_components: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uuid** | [**str**](.md)| The UUID of the project to retrieve components for | 
 **page_number** | **str**| The page to return. To be used in conjunction with &lt;code&gt;pageSize&lt;/code&gt;. | [optional] [default to 1]
 **page_size** | **str**| Number of elements to return per page. To be used in conjunction with &lt;code&gt;pageNumber&lt;/code&gt;. | [optional] [default to 100]
 **offset** | **str**| Offset to start returning elements from. To be used in conjunction with &lt;code&gt;limit&lt;/code&gt;. | [optional] 
 **limit** | **str**| Number of elements to return per page. To be used in conjunction with &lt;code&gt;offset&lt;/code&gt;. | [optional] 
 **sort_name** | **str**| Name of the resource field to sort on. | [optional] 
 **sort_order** | **str**| Ordering of items when sorting with &lt;code&gt;sortName&lt;/code&gt;. | [optional] 
 **only_outdated** | **bool**| Optionally exclude recent components so only outdated components are returned | [optional] 
 **only_direct** | **bool**| Optionally exclude transitive dependencies so only direct dependencies are returned | [optional] 

### Return type

[**list[Component]**](Component.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_component_by_hash**
> list[Component] get_component_by_hash(hash, page_number=page_number, page_size=page_size, offset=offset, limit=limit, sort_name=sort_name, sort_order=sort_order)

Returns a list of components that have the specified hash value

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
api_instance = swagger_client.ComponentApi(swagger_client.ApiClient(configuration))
hash = 'hash_example' # str | The MD5, SHA-1, SHA-256, SHA-384, SHA-512, SHA3-256, SHA3-384, SHA3-512, BLAKE2b-256, BLAKE2b-384, BLAKE2b-512, or BLAKE3 hash of the component to retrieve
page_number = '1' # str | The page to return. To be used in conjunction with <code>pageSize</code>. (optional) (default to 1)
page_size = '100' # str | Number of elements to return per page. To be used in conjunction with <code>pageNumber</code>. (optional) (default to 100)
offset = 'offset_example' # str | Offset to start returning elements from. To be used in conjunction with <code>limit</code>. (optional)
limit = 'limit_example' # str | Number of elements to return per page. To be used in conjunction with <code>offset</code>. (optional)
sort_name = 'sort_name_example' # str | Name of the resource field to sort on. (optional)
sort_order = 'sort_order_example' # str | Ordering of items when sorting with <code>sortName</code>. (optional)

try:
    # Returns a list of components that have the specified hash value
    api_response = api_instance.get_component_by_hash(hash, page_number=page_number, page_size=page_size, offset=offset, limit=limit, sort_name=sort_name, sort_order=sort_order)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling ComponentApi->get_component_by_hash: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **hash** | **str**| The MD5, SHA-1, SHA-256, SHA-384, SHA-512, SHA3-256, SHA3-384, SHA3-512, BLAKE2b-256, BLAKE2b-384, BLAKE2b-512, or BLAKE3 hash of the component to retrieve | 
 **page_number** | **str**| The page to return. To be used in conjunction with &lt;code&gt;pageSize&lt;/code&gt;. | [optional] [default to 1]
 **page_size** | **str**| Number of elements to return per page. To be used in conjunction with &lt;code&gt;pageNumber&lt;/code&gt;. | [optional] [default to 100]
 **offset** | **str**| Offset to start returning elements from. To be used in conjunction with &lt;code&gt;limit&lt;/code&gt;. | [optional] 
 **limit** | **str**| Number of elements to return per page. To be used in conjunction with &lt;code&gt;offset&lt;/code&gt;. | [optional] 
 **sort_name** | **str**| Name of the resource field to sort on. | [optional] 
 **sort_order** | **str**| Ordering of items when sorting with &lt;code&gt;sortName&lt;/code&gt;. | [optional] 

### Return type

[**list[Component]**](Component.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_component_by_identity**
> list[Component] get_component_by_identity(page_number=page_number, page_size=page_size, offset=offset, limit=limit, sort_name=sort_name, sort_order=sort_order, group=group, name=name, version=version, purl=purl, cpe=cpe, swid_tag_id=swid_tag_id, project=project)

Returns a list of components that have the specified component identity. This resource accepts coordinates (group, name, version) or purl, cpe, or swidTagId

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
api_instance = swagger_client.ComponentApi(swagger_client.ApiClient(configuration))
page_number = '1' # str | The page to return. To be used in conjunction with <code>pageSize</code>. (optional) (default to 1)
page_size = '100' # str | Number of elements to return per page. To be used in conjunction with <code>pageNumber</code>. (optional) (default to 100)
offset = 'offset_example' # str | Offset to start returning elements from. To be used in conjunction with <code>limit</code>. (optional)
limit = 'limit_example' # str | Number of elements to return per page. To be used in conjunction with <code>offset</code>. (optional)
sort_name = 'sort_name_example' # str | Name of the resource field to sort on. (optional)
sort_order = 'sort_order_example' # str | Ordering of items when sorting with <code>sortName</code>. (optional)
group = 'group_example' # str | The group of the component (optional)
name = 'name_example' # str | The name of the component (optional)
version = 'version_example' # str | The version of the component (optional)
purl = 'purl_example' # str | The purl of the component (optional)
cpe = 'cpe_example' # str | The cpe of the component (optional)
swid_tag_id = 'swid_tag_id_example' # str | The swidTagId of the component (optional)
project = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | The project the component belongs to (optional)

try:
    # Returns a list of components that have the specified component identity. This resource accepts coordinates (group, name, version) or purl, cpe, or swidTagId
    api_response = api_instance.get_component_by_identity(page_number=page_number, page_size=page_size, offset=offset, limit=limit, sort_name=sort_name, sort_order=sort_order, group=group, name=name, version=version, purl=purl, cpe=cpe, swid_tag_id=swid_tag_id, project=project)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling ComponentApi->get_component_by_identity: %s\n" % e)
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
 **group** | **str**| The group of the component | [optional] 
 **name** | **str**| The name of the component | [optional] 
 **version** | **str**| The version of the component | [optional] 
 **purl** | **str**| The purl of the component | [optional] 
 **cpe** | **str**| The cpe of the component | [optional] 
 **swid_tag_id** | **str**| The swidTagId of the component | [optional] 
 **project** | [**str**](.md)| The project the component belongs to | [optional] 

### Return type

[**list[Component]**](Component.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_component_by_uuid**
> Component get_component_by_uuid(uuid, include_repository_meta_data=include_repository_meta_data)

Returns a specific component

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
api_instance = swagger_client.ComponentApi(swagger_client.ApiClient(configuration))
uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | The UUID of the component to retrieve
include_repository_meta_data = true # bool | Optionally includes third-party metadata about the component from external repositories (optional)

try:
    # Returns a specific component
    api_response = api_instance.get_component_by_uuid(uuid, include_repository_meta_data=include_repository_meta_data)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling ComponentApi->get_component_by_uuid: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uuid** | [**str**](.md)| The UUID of the component to retrieve | 
 **include_repository_meta_data** | **bool**| Optionally includes third-party metadata about the component from external repositories | [optional] 

### Return type

[**Component**](Component.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_dependency_graph_for_component**
> object get_dependency_graph_for_component(project_uuid, component_uuids)

Returns the expanded dependency graph to every occurrence of a component

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
api_instance = swagger_client.ComponentApi(swagger_client.ApiClient(configuration))
project_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | The UUID of the project to get the expanded dependency graph for
component_uuids = 'component_uuids_example' # str | List of UUIDs of the components (separated by |) to get the expanded dependency graph for

try:
    # Returns the expanded dependency graph to every occurrence of a component
    api_response = api_instance.get_dependency_graph_for_component(project_uuid, component_uuids)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling ComponentApi->get_dependency_graph_for_component: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_uuid** | [**str**](.md)| The UUID of the project to get the expanded dependency graph for | 
 **component_uuids** | **str**| List of UUIDs of the components (separated by |) to get the expanded dependency graph for | 

### Return type

**object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **identify_internal_components**
> identify_internal_components()

Requests the identification of internal components in the portfolio

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
api_instance = swagger_client.ComponentApi(swagger_client.ApiClient(configuration))

try:
    # Requests the identification of internal components in the portfolio
    api_instance.identify_internal_components()
except ApiException as e:
    print("Exception when calling ComponentApi->identify_internal_components: %s\n" % e)
```

### Parameters
This endpoint does not need any parameter.

### Return type

void (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_component**
> Component update_component(body=body)

Updates a component

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
api_instance = swagger_client.ComponentApi(swagger_client.ApiClient(configuration))
body = swagger_client.Component() # Component |  (optional)

try:
    # Updates a component
    api_response = api_instance.update_component(body=body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling ComponentApi->update_component: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**Component**](Component.md)|  | [optional] 

### Return type

[**Component**](Component.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

