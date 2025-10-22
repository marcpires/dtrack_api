# swagger_client.OidcApi

All URIs are relative to */api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**add_mapping2**](OidcApi.md#add_mapping2) | **PUT** /v1/oidc/mapping | Adds a mapping
[**create_group**](OidcApi.md#create_group) | **PUT** /v1/oidc/group | Creates group
[**delete_group**](OidcApi.md#delete_group) | **DELETE** /v1/oidc/group/{uuid} | Deletes a group
[**delete_mapping2**](OidcApi.md#delete_mapping2) | **DELETE** /v1/oidc/group/{groupUuid}/team/{teamUuid}/mapping | Deletes a mapping
[**delete_mapping_by_uuid**](OidcApi.md#delete_mapping_by_uuid) | **DELETE** /v1/oidc/mapping/{uuid} | Deletes a mapping
[**is_available**](OidcApi.md#is_available) | **GET** /v1/oidc/available | Indicates if OpenID Connect is available for this application
[**retrieve_groups**](OidcApi.md#retrieve_groups) | **GET** /v1/oidc/group | Returns a list of all groups
[**retrieve_teams_mapped_to_group**](OidcApi.md#retrieve_teams_mapped_to_group) | **GET** /v1/oidc/group/{uuid}/team | Returns a list of teams associated with the specified group
[**update_group**](OidcApi.md#update_group) | **POST** /v1/oidc/group | Updates group

# **add_mapping2**
> MappedOidcGroup add_mapping2(body=body)

Adds a mapping

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
api_instance = swagger_client.OidcApi(swagger_client.ApiClient(configuration))
body = swagger_client.MappedOidcGroupRequest() # MappedOidcGroupRequest |  (optional)

try:
    # Adds a mapping
    api_response = api_instance.add_mapping2(body=body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling OidcApi->add_mapping2: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**MappedOidcGroupRequest**](MappedOidcGroupRequest.md)|  | [optional] 

### Return type

[**MappedOidcGroup**](MappedOidcGroup.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: */*
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_group**
> OidcGroup create_group(body=body)

Creates group

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
api_instance = swagger_client.OidcApi(swagger_client.ApiClient(configuration))
body = swagger_client.OidcGroup() # OidcGroup |  (optional)

try:
    # Creates group
    api_response = api_instance.create_group(body=body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling OidcApi->create_group: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**OidcGroup**](OidcGroup.md)|  | [optional] 

### Return type

[**OidcGroup**](OidcGroup.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_group**
> delete_group(uuid)

Deletes a group

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
api_instance = swagger_client.OidcApi(swagger_client.ApiClient(configuration))
uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | The UUID of the group to delete

try:
    # Deletes a group
    api_instance.delete_group(uuid)
except ApiException as e:
    print("Exception when calling OidcApi->delete_group: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uuid** | [**str**](.md)| The UUID of the group to delete | 

### Return type

void (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_mapping2**
> delete_mapping2(group_uuid, team_uuid)

Deletes a mapping

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
api_instance = swagger_client.OidcApi(swagger_client.ApiClient(configuration))
group_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | The UUID of the group to delete a mapping for
team_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | The UUID of the team to delete a mapping for

try:
    # Deletes a mapping
    api_instance.delete_mapping2(group_uuid, team_uuid)
except ApiException as e:
    print("Exception when calling OidcApi->delete_mapping2: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **group_uuid** | [**str**](.md)| The UUID of the group to delete a mapping for | 
 **team_uuid** | [**str**](.md)| The UUID of the team to delete a mapping for | 

### Return type

void (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_mapping_by_uuid**
> delete_mapping_by_uuid(uuid)

Deletes a mapping

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
api_instance = swagger_client.OidcApi(swagger_client.ApiClient(configuration))
uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | The UUID of the mapping to delete

try:
    # Deletes a mapping
    api_instance.delete_mapping_by_uuid(uuid)
except ApiException as e:
    print("Exception when calling OidcApi->delete_mapping_by_uuid: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uuid** | [**str**](.md)| The UUID of the mapping to delete | 

### Return type

void (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **is_available**
> bool is_available()

Indicates if OpenID Connect is available for this application

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
api_instance = swagger_client.OidcApi(swagger_client.ApiClient(configuration))

try:
    # Indicates if OpenID Connect is available for this application
    api_response = api_instance.is_available()
    pprint(api_response)
except ApiException as e:
    print("Exception when calling OidcApi->is_available: %s\n" % e)
```

### Parameters
This endpoint does not need any parameter.

### Return type

**bool**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **retrieve_groups**
> list[OidcGroup] retrieve_groups()

Returns a list of all groups

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
api_instance = swagger_client.OidcApi(swagger_client.ApiClient(configuration))

try:
    # Returns a list of all groups
    api_response = api_instance.retrieve_groups()
    pprint(api_response)
except ApiException as e:
    print("Exception when calling OidcApi->retrieve_groups: %s\n" % e)
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**list[OidcGroup]**](OidcGroup.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **retrieve_teams_mapped_to_group**
> list[Team] retrieve_teams_mapped_to_group(uuid)

Returns a list of teams associated with the specified group

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
api_instance = swagger_client.OidcApi(swagger_client.ApiClient(configuration))
uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | The UUID of the mapping to retrieve the team for

try:
    # Returns a list of teams associated with the specified group
    api_response = api_instance.retrieve_teams_mapped_to_group(uuid)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling OidcApi->retrieve_teams_mapped_to_group: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uuid** | [**str**](.md)| The UUID of the mapping to retrieve the team for | 

### Return type

[**list[Team]**](Team.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_group**
> OidcGroup update_group(body=body)

Updates group

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
api_instance = swagger_client.OidcApi(swagger_client.ApiClient(configuration))
body = swagger_client.OidcGroup() # OidcGroup |  (optional)

try:
    # Updates group
    api_response = api_instance.update_group(body=body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling OidcApi->update_group: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**OidcGroup**](OidcGroup.md)|  | [optional] 

### Return type

[**OidcGroup**](OidcGroup.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

