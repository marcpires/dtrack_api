# swagger_client.PermissionApi

All URIs are relative to */api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**add_permission_to_team**](PermissionApi.md#add_permission_to_team) | **POST** /v1/permission/{permission}/team/{uuid} | Adds the permission to the specified team.
[**add_permission_to_user**](PermissionApi.md#add_permission_to_user) | **POST** /v1/permission/{permission}/user/{username} | Adds the permission to the specified username.
[**get_all_permissions**](PermissionApi.md#get_all_permissions) | **GET** /v1/permission | Returns a list of all permissions
[**remove_permission_from_team**](PermissionApi.md#remove_permission_from_team) | **DELETE** /v1/permission/{permission}/team/{uuid} | Removes the permission from the team.
[**remove_permission_from_user**](PermissionApi.md#remove_permission_from_user) | **DELETE** /v1/permission/{permission}/user/{username} | Removes the permission from the user.

# **add_permission_to_team**
> Team add_permission_to_team(uuid, permission)

Adds the permission to the specified team.

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
api_instance = swagger_client.PermissionApi(swagger_client.ApiClient(configuration))
uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | A valid team uuid
permission = 'permission_example' # str | A valid permission

try:
    # Adds the permission to the specified team.
    api_response = api_instance.add_permission_to_team(uuid, permission)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling PermissionApi->add_permission_to_team: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uuid** | [**str**](.md)| A valid team uuid | 
 **permission** | **str**| A valid permission | 

### Return type

[**Team**](Team.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **add_permission_to_user**
> UserPrincipal add_permission_to_user(username, permission)

Adds the permission to the specified username.

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
api_instance = swagger_client.PermissionApi(swagger_client.ApiClient(configuration))
username = 'username_example' # str | A valid username
permission = 'permission_example' # str | A valid permission

try:
    # Adds the permission to the specified username.
    api_response = api_instance.add_permission_to_user(username, permission)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling PermissionApi->add_permission_to_user: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **username** | **str**| A valid username | 
 **permission** | **str**| A valid permission | 

### Return type

[**UserPrincipal**](UserPrincipal.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_all_permissions**
> str get_all_permissions()

Returns a list of all permissions

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
api_instance = swagger_client.PermissionApi(swagger_client.ApiClient(configuration))

try:
    # Returns a list of all permissions
    api_response = api_instance.get_all_permissions()
    pprint(api_response)
except ApiException as e:
    print("Exception when calling PermissionApi->get_all_permissions: %s\n" % e)
```

### Parameters
This endpoint does not need any parameter.

### Return type

**str**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **remove_permission_from_team**
> Team remove_permission_from_team(uuid, permission)

Removes the permission from the team.

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
api_instance = swagger_client.PermissionApi(swagger_client.ApiClient(configuration))
uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | A valid team uuid
permission = 'permission_example' # str | A valid permission

try:
    # Removes the permission from the team.
    api_response = api_instance.remove_permission_from_team(uuid, permission)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling PermissionApi->remove_permission_from_team: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uuid** | [**str**](.md)| A valid team uuid | 
 **permission** | **str**| A valid permission | 

### Return type

[**Team**](Team.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **remove_permission_from_user**
> UserPrincipal remove_permission_from_user(username, permission)

Removes the permission from the user.

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
api_instance = swagger_client.PermissionApi(swagger_client.ApiClient(configuration))
username = 'username_example' # str | A valid username
permission = 'permission_example' # str | A valid permission

try:
    # Removes the permission from the user.
    api_response = api_instance.remove_permission_from_user(username, permission)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling PermissionApi->remove_permission_from_user: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **username** | **str**| A valid username | 
 **permission** | **str**| A valid permission | 

### Return type

[**UserPrincipal**](UserPrincipal.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

