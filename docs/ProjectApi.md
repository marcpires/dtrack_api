# swagger_client.ProjectApi

All URIs are relative to */api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**clone_project**](ProjectApi.md#clone_project) | **PUT** /v1/project/clone | Clones a project
[**create_project**](ProjectApi.md#create_project) | **PUT** /v1/project | Creates a new project
[**delete_project**](ProjectApi.md#delete_project) | **DELETE** /v1/project/{uuid} | Deletes a project
[**delete_projects**](ProjectApi.md#delete_projects) | **POST** /v1/project/batchDelete | Deletes a list of projects specified by their UUIDs
[**get_children_projects**](ProjectApi.md#get_children_projects) | **GET** /v1/project/{uuid}/children | Returns a list of all children for a project
[**get_children_projects_by_classifier**](ProjectApi.md#get_children_projects_by_classifier) | **GET** /v1/project/{uuid}/children/classifier/{classifier} | Returns a list of all children for a project by classifier
[**get_children_projects_by_tag**](ProjectApi.md#get_children_projects_by_tag) | **GET** /v1/project/{uuid}/children/tag/{tag} | Returns a list of all children for a project by tag
[**get_latest_project_by_name**](ProjectApi.md#get_latest_project_by_name) | **GET** /v1/project/latest/{name} | Returns the latest version of a project by its name
[**get_project**](ProjectApi.md#get_project) | **GET** /v1/project/{uuid} | Returns a specific project
[**get_project_by_name_and_version**](ProjectApi.md#get_project_by_name_and_version) | **GET** /v1/project/lookup | Returns a specific project by its name and version
[**get_projects**](ProjectApi.md#get_projects) | **GET** /v1/project | Returns a list of all projects
[**get_projects_by_classifier**](ProjectApi.md#get_projects_by_classifier) | **GET** /v1/project/classifier/{classifier} | Returns a list of all projects by classifier
[**get_projects_by_tag**](ProjectApi.md#get_projects_by_tag) | **GET** /v1/project/tag/{tag} | Returns a list of all projects by tag
[**get_projects_without_descendants_of**](ProjectApi.md#get_projects_without_descendants_of) | **GET** /v1/project/withoutDescendantsOf/{uuid} | Returns a list of all projects without the descendants of the selected project
[**patch_project**](ProjectApi.md#patch_project) | **PATCH** /v1/project/{uuid} | Partially updates a project
[**update_project**](ProjectApi.md#update_project) | **POST** /v1/project | Updates a project

# **clone_project**
> BomUploadResponse clone_project(body=body)

Clones a project

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
api_instance = swagger_client.ProjectApi(swagger_client.ApiClient(configuration))
body = swagger_client.CloneProjectRequest() # CloneProjectRequest |  (optional)

try:
    # Clones a project
    api_response = api_instance.clone_project(body=body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling ProjectApi->clone_project: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**CloneProjectRequest**](CloneProjectRequest.md)|  | [optional] 

### Return type

[**BomUploadResponse**](BomUploadResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_project**
> Project create_project(body=body)

Creates a new project

<p>If a parent project exists, <code>parent.uuid</code> is required</p> <p>   When portfolio access control is enabled, one or more teams to grant access   to can be provided via <code>accessTeams</code>. Either <code>uuid</code> or   <code>name</code> of a team must be specified. Only teams which the authenticated   principal is a member of can be assigned. Principals with <strong>ACCESS_MANAGEMENT</strong>   permission can assign <em>any</em> team. </p> <p>Requires permission <strong>PORTFOLIO_MANAGEMENT</strong></p> 

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
api_instance = swagger_client.ProjectApi(swagger_client.ApiClient(configuration))
body = swagger_client.Project() # Project |  (optional)

try:
    # Creates a new project
    api_response = api_instance.create_project(body=body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling ProjectApi->create_project: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**Project**](Project.md)|  | [optional] 

### Return type

[**Project**](Project.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_project**
> delete_project(uuid)

Deletes a project

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
api_instance = swagger_client.ProjectApi(swagger_client.ApiClient(configuration))
uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | The UUID of the project to delete

try:
    # Deletes a project
    api_instance.delete_project(uuid)
except ApiException as e:
    print("Exception when calling ProjectApi->delete_project: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uuid** | [**str**](.md)| The UUID of the project to delete | 

### Return type

void (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_projects**
> delete_projects(body=body)

Deletes a list of projects specified by their UUIDs

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
api_instance = swagger_client.ProjectApi(swagger_client.ApiClient(configuration))
body = ['body_example'] # list[str] |  (optional)

try:
    # Deletes a list of projects specified by their UUIDs
    api_instance.delete_projects(body=body)
except ApiException as e:
    print("Exception when calling ProjectApi->delete_projects: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**list[str]**](str.md)|  | [optional] 

### Return type

void (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_children_projects**
> list[Project] get_children_projects(uuid, page_number=page_number, page_size=page_size, offset=offset, limit=limit, sort_name=sort_name, sort_order=sort_order, exclude_inactive=exclude_inactive)

Returns a list of all children for a project

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
api_instance = swagger_client.ProjectApi(swagger_client.ApiClient(configuration))
uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | The UUID of the project to get the children from
page_number = '1' # str | The page to return. To be used in conjunction with <code>pageSize</code>. (optional) (default to 1)
page_size = '100' # str | Number of elements to return per page. To be used in conjunction with <code>pageNumber</code>. (optional) (default to 100)
offset = 'offset_example' # str | Offset to start returning elements from. To be used in conjunction with <code>limit</code>. (optional)
limit = 'limit_example' # str | Number of elements to return per page. To be used in conjunction with <code>offset</code>. (optional)
sort_name = 'sort_name_example' # str | Name of the resource field to sort on. (optional)
sort_order = 'sort_order_example' # str | Ordering of items when sorting with <code>sortName</code>. (optional)
exclude_inactive = true # bool | Optionally excludes inactive projects from being returned (optional)

try:
    # Returns a list of all children for a project
    api_response = api_instance.get_children_projects(uuid, page_number=page_number, page_size=page_size, offset=offset, limit=limit, sort_name=sort_name, sort_order=sort_order, exclude_inactive=exclude_inactive)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling ProjectApi->get_children_projects: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uuid** | [**str**](.md)| The UUID of the project to get the children from | 
 **page_number** | **str**| The page to return. To be used in conjunction with &lt;code&gt;pageSize&lt;/code&gt;. | [optional] [default to 1]
 **page_size** | **str**| Number of elements to return per page. To be used in conjunction with &lt;code&gt;pageNumber&lt;/code&gt;. | [optional] [default to 100]
 **offset** | **str**| Offset to start returning elements from. To be used in conjunction with &lt;code&gt;limit&lt;/code&gt;. | [optional] 
 **limit** | **str**| Number of elements to return per page. To be used in conjunction with &lt;code&gt;offset&lt;/code&gt;. | [optional] 
 **sort_name** | **str**| Name of the resource field to sort on. | [optional] 
 **sort_order** | **str**| Ordering of items when sorting with &lt;code&gt;sortName&lt;/code&gt;. | [optional] 
 **exclude_inactive** | **bool**| Optionally excludes inactive projects from being returned | [optional] 

### Return type

[**list[Project]**](Project.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_children_projects_by_classifier**
> list[Project] get_children_projects_by_classifier(classifier, uuid, page_number=page_number, page_size=page_size, offset=offset, limit=limit, sort_name=sort_name, sort_order=sort_order, exclude_inactive=exclude_inactive)

Returns a list of all children for a project by classifier

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
api_instance = swagger_client.ProjectApi(swagger_client.ApiClient(configuration))
classifier = 'classifier_example' # str | The classifier to query on
uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | The UUID of the project to get the children from
page_number = '1' # str | The page to return. To be used in conjunction with <code>pageSize</code>. (optional) (default to 1)
page_size = '100' # str | Number of elements to return per page. To be used in conjunction with <code>pageNumber</code>. (optional) (default to 100)
offset = 'offset_example' # str | Offset to start returning elements from. To be used in conjunction with <code>limit</code>. (optional)
limit = 'limit_example' # str | Number of elements to return per page. To be used in conjunction with <code>offset</code>. (optional)
sort_name = 'sort_name_example' # str | Name of the resource field to sort on. (optional)
sort_order = 'sort_order_example' # str | Ordering of items when sorting with <code>sortName</code>. (optional)
exclude_inactive = true # bool | Optionally excludes inactive projects from being returned (optional)

try:
    # Returns a list of all children for a project by classifier
    api_response = api_instance.get_children_projects_by_classifier(classifier, uuid, page_number=page_number, page_size=page_size, offset=offset, limit=limit, sort_name=sort_name, sort_order=sort_order, exclude_inactive=exclude_inactive)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling ProjectApi->get_children_projects_by_classifier: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **classifier** | **str**| The classifier to query on | 
 **uuid** | [**str**](.md)| The UUID of the project to get the children from | 
 **page_number** | **str**| The page to return. To be used in conjunction with &lt;code&gt;pageSize&lt;/code&gt;. | [optional] [default to 1]
 **page_size** | **str**| Number of elements to return per page. To be used in conjunction with &lt;code&gt;pageNumber&lt;/code&gt;. | [optional] [default to 100]
 **offset** | **str**| Offset to start returning elements from. To be used in conjunction with &lt;code&gt;limit&lt;/code&gt;. | [optional] 
 **limit** | **str**| Number of elements to return per page. To be used in conjunction with &lt;code&gt;offset&lt;/code&gt;. | [optional] 
 **sort_name** | **str**| Name of the resource field to sort on. | [optional] 
 **sort_order** | **str**| Ordering of items when sorting with &lt;code&gt;sortName&lt;/code&gt;. | [optional] 
 **exclude_inactive** | **bool**| Optionally excludes inactive projects from being returned | [optional] 

### Return type

[**list[Project]**](Project.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_children_projects_by_tag**
> list[Project] get_children_projects_by_tag(tag, uuid, page_number=page_number, page_size=page_size, offset=offset, limit=limit, sort_name=sort_name, sort_order=sort_order, exclude_inactive=exclude_inactive)

Returns a list of all children for a project by tag

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
api_instance = swagger_client.ProjectApi(swagger_client.ApiClient(configuration))
tag = 'tag_example' # str | The tag to query on
uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | The UUID of the project to get the children from
page_number = '1' # str | The page to return. To be used in conjunction with <code>pageSize</code>. (optional) (default to 1)
page_size = '100' # str | Number of elements to return per page. To be used in conjunction with <code>pageNumber</code>. (optional) (default to 100)
offset = 'offset_example' # str | Offset to start returning elements from. To be used in conjunction with <code>limit</code>. (optional)
limit = 'limit_example' # str | Number of elements to return per page. To be used in conjunction with <code>offset</code>. (optional)
sort_name = 'sort_name_example' # str | Name of the resource field to sort on. (optional)
sort_order = 'sort_order_example' # str | Ordering of items when sorting with <code>sortName</code>. (optional)
exclude_inactive = true # bool | Optionally excludes inactive projects from being returned (optional)

try:
    # Returns a list of all children for a project by tag
    api_response = api_instance.get_children_projects_by_tag(tag, uuid, page_number=page_number, page_size=page_size, offset=offset, limit=limit, sort_name=sort_name, sort_order=sort_order, exclude_inactive=exclude_inactive)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling ProjectApi->get_children_projects_by_tag: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **tag** | **str**| The tag to query on | 
 **uuid** | [**str**](.md)| The UUID of the project to get the children from | 
 **page_number** | **str**| The page to return. To be used in conjunction with &lt;code&gt;pageSize&lt;/code&gt;. | [optional] [default to 1]
 **page_size** | **str**| Number of elements to return per page. To be used in conjunction with &lt;code&gt;pageNumber&lt;/code&gt;. | [optional] [default to 100]
 **offset** | **str**| Offset to start returning elements from. To be used in conjunction with &lt;code&gt;limit&lt;/code&gt;. | [optional] 
 **limit** | **str**| Number of elements to return per page. To be used in conjunction with &lt;code&gt;offset&lt;/code&gt;. | [optional] 
 **sort_name** | **str**| Name of the resource field to sort on. | [optional] 
 **sort_order** | **str**| Ordering of items when sorting with &lt;code&gt;sortName&lt;/code&gt;. | [optional] 
 **exclude_inactive** | **bool**| Optionally excludes inactive projects from being returned | [optional] 

### Return type

[**list[Project]**](Project.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_latest_project_by_name**
> Project get_latest_project_by_name(name)

Returns the latest version of a project by its name

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
api_instance = swagger_client.ProjectApi(swagger_client.ApiClient(configuration))
name = 'name_example' # str | The name of the project to retrieve the latest version of

try:
    # Returns the latest version of a project by its name
    api_response = api_instance.get_latest_project_by_name(name)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling ProjectApi->get_latest_project_by_name: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **name** | **str**| The name of the project to retrieve the latest version of | 

### Return type

[**Project**](Project.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_project**
> Project get_project(uuid)

Returns a specific project

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
api_instance = swagger_client.ProjectApi(swagger_client.ApiClient(configuration))
uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | The UUID of the project to retrieve

try:
    # Returns a specific project
    api_response = api_instance.get_project(uuid)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling ProjectApi->get_project: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uuid** | [**str**](.md)| The UUID of the project to retrieve | 

### Return type

[**Project**](Project.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_project_by_name_and_version**
> Project get_project_by_name_and_version(name, version)

Returns a specific project by its name and version

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
api_instance = swagger_client.ProjectApi(swagger_client.ApiClient(configuration))
name = 'name_example' # str | The name of the project to query on
version = 'version_example' # str | The version of the project to query on

try:
    # Returns a specific project by its name and version
    api_response = api_instance.get_project_by_name_and_version(name, version)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling ProjectApi->get_project_by_name_and_version: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **name** | **str**| The name of the project to query on | 
 **version** | **str**| The version of the project to query on | 

### Return type

[**Project**](Project.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_projects**
> list[Project] get_projects(page_number=page_number, page_size=page_size, offset=offset, limit=limit, sort_name=sort_name, sort_order=sort_order, name=name, exclude_inactive=exclude_inactive, only_root=only_root, not_assigned_to_team_with_uuid=not_assigned_to_team_with_uuid)

Returns a list of all projects

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
api_instance = swagger_client.ProjectApi(swagger_client.ApiClient(configuration))
page_number = '1' # str | The page to return. To be used in conjunction with <code>pageSize</code>. (optional) (default to 1)
page_size = '100' # str | Number of elements to return per page. To be used in conjunction with <code>pageNumber</code>. (optional) (default to 100)
offset = 'offset_example' # str | Offset to start returning elements from. To be used in conjunction with <code>limit</code>. (optional)
limit = 'limit_example' # str | Number of elements to return per page. To be used in conjunction with <code>offset</code>. (optional)
sort_name = 'sort_name_example' # str | Name of the resource field to sort on. (optional)
sort_order = 'sort_order_example' # str | Ordering of items when sorting with <code>sortName</code>. (optional)
name = 'name_example' # str | The optional name of the project to query on (optional)
exclude_inactive = true # bool | Optionally excludes inactive projects from being returned (optional)
only_root = true # bool | Optionally excludes children projects from being returned (optional)
not_assigned_to_team_with_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | The UUID of the team which projects shall be excluded (optional)

try:
    # Returns a list of all projects
    api_response = api_instance.get_projects(page_number=page_number, page_size=page_size, offset=offset, limit=limit, sort_name=sort_name, sort_order=sort_order, name=name, exclude_inactive=exclude_inactive, only_root=only_root, not_assigned_to_team_with_uuid=not_assigned_to_team_with_uuid)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling ProjectApi->get_projects: %s\n" % e)
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
 **name** | **str**| The optional name of the project to query on | [optional] 
 **exclude_inactive** | **bool**| Optionally excludes inactive projects from being returned | [optional] 
 **only_root** | **bool**| Optionally excludes children projects from being returned | [optional] 
 **not_assigned_to_team_with_uuid** | [**str**](.md)| The UUID of the team which projects shall be excluded | [optional] 

### Return type

[**list[Project]**](Project.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_projects_by_classifier**
> list[Project] get_projects_by_classifier(classifier, page_number=page_number, page_size=page_size, offset=offset, limit=limit, sort_name=sort_name, sort_order=sort_order, exclude_inactive=exclude_inactive, only_root=only_root)

Returns a list of all projects by classifier

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
api_instance = swagger_client.ProjectApi(swagger_client.ApiClient(configuration))
classifier = 'classifier_example' # str | The classifier to query on
page_number = '1' # str | The page to return. To be used in conjunction with <code>pageSize</code>. (optional) (default to 1)
page_size = '100' # str | Number of elements to return per page. To be used in conjunction with <code>pageNumber</code>. (optional) (default to 100)
offset = 'offset_example' # str | Offset to start returning elements from. To be used in conjunction with <code>limit</code>. (optional)
limit = 'limit_example' # str | Number of elements to return per page. To be used in conjunction with <code>offset</code>. (optional)
sort_name = 'sort_name_example' # str | Name of the resource field to sort on. (optional)
sort_order = 'sort_order_example' # str | Ordering of items when sorting with <code>sortName</code>. (optional)
exclude_inactive = true # bool | Optionally excludes inactive projects from being returned (optional)
only_root = true # bool | Optionally excludes children projects from being returned (optional)

try:
    # Returns a list of all projects by classifier
    api_response = api_instance.get_projects_by_classifier(classifier, page_number=page_number, page_size=page_size, offset=offset, limit=limit, sort_name=sort_name, sort_order=sort_order, exclude_inactive=exclude_inactive, only_root=only_root)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling ProjectApi->get_projects_by_classifier: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **classifier** | **str**| The classifier to query on | 
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

# **get_projects_by_tag**
> list[Project] get_projects_by_tag(tag, page_number=page_number, page_size=page_size, offset=offset, limit=limit, sort_name=sort_name, sort_order=sort_order, exclude_inactive=exclude_inactive, only_root=only_root)

Returns a list of all projects by tag

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
api_instance = swagger_client.ProjectApi(swagger_client.ApiClient(configuration))
tag = 'tag_example' # str | The tag to query on
page_number = '1' # str | The page to return. To be used in conjunction with <code>pageSize</code>. (optional) (default to 1)
page_size = '100' # str | Number of elements to return per page. To be used in conjunction with <code>pageNumber</code>. (optional) (default to 100)
offset = 'offset_example' # str | Offset to start returning elements from. To be used in conjunction with <code>limit</code>. (optional)
limit = 'limit_example' # str | Number of elements to return per page. To be used in conjunction with <code>offset</code>. (optional)
sort_name = 'sort_name_example' # str | Name of the resource field to sort on. (optional)
sort_order = 'sort_order_example' # str | Ordering of items when sorting with <code>sortName</code>. (optional)
exclude_inactive = true # bool | Optionally excludes inactive projects from being returned (optional)
only_root = true # bool | Optionally excludes children projects from being returned (optional)

try:
    # Returns a list of all projects by tag
    api_response = api_instance.get_projects_by_tag(tag, page_number=page_number, page_size=page_size, offset=offset, limit=limit, sort_name=sort_name, sort_order=sort_order, exclude_inactive=exclude_inactive, only_root=only_root)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling ProjectApi->get_projects_by_tag: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **tag** | **str**| The tag to query on | 
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

# **get_projects_without_descendants_of**
> list[Project] get_projects_without_descendants_of(uuid, page_number=page_number, page_size=page_size, offset=offset, limit=limit, sort_name=sort_name, sort_order=sort_order, name=name, exclude_inactive=exclude_inactive)

Returns a list of all projects without the descendants of the selected project

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
api_instance = swagger_client.ProjectApi(swagger_client.ApiClient(configuration))
uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | The UUID of the project which descendants will be excluded
page_number = '1' # str | The page to return. To be used in conjunction with <code>pageSize</code>. (optional) (default to 1)
page_size = '100' # str | Number of elements to return per page. To be used in conjunction with <code>pageNumber</code>. (optional) (default to 100)
offset = 'offset_example' # str | Offset to start returning elements from. To be used in conjunction with <code>limit</code>. (optional)
limit = 'limit_example' # str | Number of elements to return per page. To be used in conjunction with <code>offset</code>. (optional)
sort_name = 'sort_name_example' # str | Name of the resource field to sort on. (optional)
sort_order = 'sort_order_example' # str | Ordering of items when sorting with <code>sortName</code>. (optional)
name = 'name_example' # str | The optional name of the project to query on (optional)
exclude_inactive = true # bool | Optionally excludes inactive projects from being returned (optional)

try:
    # Returns a list of all projects without the descendants of the selected project
    api_response = api_instance.get_projects_without_descendants_of(uuid, page_number=page_number, page_size=page_size, offset=offset, limit=limit, sort_name=sort_name, sort_order=sort_order, name=name, exclude_inactive=exclude_inactive)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling ProjectApi->get_projects_without_descendants_of: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uuid** | [**str**](.md)| The UUID of the project which descendants will be excluded | 
 **page_number** | **str**| The page to return. To be used in conjunction with &lt;code&gt;pageSize&lt;/code&gt;. | [optional] [default to 1]
 **page_size** | **str**| Number of elements to return per page. To be used in conjunction with &lt;code&gt;pageNumber&lt;/code&gt;. | [optional] [default to 100]
 **offset** | **str**| Offset to start returning elements from. To be used in conjunction with &lt;code&gt;limit&lt;/code&gt;. | [optional] 
 **limit** | **str**| Number of elements to return per page. To be used in conjunction with &lt;code&gt;offset&lt;/code&gt;. | [optional] 
 **sort_name** | **str**| Name of the resource field to sort on. | [optional] 
 **sort_order** | **str**| Ordering of items when sorting with &lt;code&gt;sortName&lt;/code&gt;. | [optional] 
 **name** | **str**| The optional name of the project to query on | [optional] 
 **exclude_inactive** | **bool**| Optionally excludes inactive projects from being returned | [optional] 

### Return type

[**list[Project]**](Project.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **patch_project**
> Project patch_project(uuid, body=body)

Partially updates a project

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
api_instance = swagger_client.ProjectApi(swagger_client.ApiClient(configuration))
uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | The UUID of the project to modify
body = swagger_client.Project() # Project |  (optional)

try:
    # Partially updates a project
    api_response = api_instance.patch_project(uuid, body=body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling ProjectApi->patch_project: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uuid** | [**str**](.md)| The UUID of the project to modify | 
 **body** | [**Project**](Project.md)|  | [optional] 

### Return type

[**Project**](Project.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_project**
> Project update_project(body=body)

Updates a project

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
api_instance = swagger_client.ProjectApi(swagger_client.ApiClient(configuration))
body = swagger_client.Project() # Project |  (optional)

try:
    # Updates a project
    api_response = api_instance.update_project(body=body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling ProjectApi->update_project: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**Project**](Project.md)|  | [optional] 

### Return type

[**Project**](Project.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

