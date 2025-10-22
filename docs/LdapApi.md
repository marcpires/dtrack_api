# swagger_client.LdapApi

All URIs are relative to */api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**add_mapping1**](LdapApi.md#add_mapping1) | **PUT** /v1/ldap/mapping | Adds a mapping
[**delete_mapping1**](LdapApi.md#delete_mapping1) | **DELETE** /v1/ldap/mapping/{uuid} | Removes a mapping
[**retrieve_ldap_groups**](LdapApi.md#retrieve_ldap_groups) | **GET** /v1/ldap/groups | Returns the DNs of all accessible groups within the directory
[**retrieve_ldap_groups1**](LdapApi.md#retrieve_ldap_groups1) | **GET** /v1/ldap/team/{uuid} | Returns the DNs of all groups mapped to the specified team

# **add_mapping1**
> MappedLdapGroup add_mapping1(body=body)

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
api_instance = swagger_client.LdapApi(swagger_client.ApiClient(configuration))
body = swagger_client.MappedLdapGroupRequest() # MappedLdapGroupRequest |  (optional)

try:
    # Adds a mapping
    api_response = api_instance.add_mapping1(body=body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling LdapApi->add_mapping1: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**MappedLdapGroupRequest**](MappedLdapGroupRequest.md)|  | [optional] 

### Return type

[**MappedLdapGroup**](MappedLdapGroup.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: */*
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_mapping1**
> delete_mapping1(uuid)

Removes a mapping

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
api_instance = swagger_client.LdapApi(swagger_client.ApiClient(configuration))
uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | The UUID of the mapping to delete

try:
    # Removes a mapping
    api_instance.delete_mapping1(uuid)
except ApiException as e:
    print("Exception when calling LdapApi->delete_mapping1: %s\n" % e)
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

# **retrieve_ldap_groups**
> list[str] retrieve_ldap_groups()

Returns the DNs of all accessible groups within the directory

<p>   This API performs a pass-through query to the configured LDAP server.   Search criteria results are cached using default Alpine CacheManager policy. <p> <p>Requires permission <strong>ACCESS_MANAGEMENT</strong></p>

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
api_instance = swagger_client.LdapApi(swagger_client.ApiClient(configuration))

try:
    # Returns the DNs of all accessible groups within the directory
    api_response = api_instance.retrieve_ldap_groups()
    pprint(api_response)
except ApiException as e:
    print("Exception when calling LdapApi->retrieve_ldap_groups: %s\n" % e)
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

# **retrieve_ldap_groups1**
> list[MappedLdapGroup] retrieve_ldap_groups1(uuid)

Returns the DNs of all groups mapped to the specified team

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
api_instance = swagger_client.LdapApi(swagger_client.ApiClient(configuration))
uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | The UUID of the team to retrieve mappings for

try:
    # Returns the DNs of all groups mapped to the specified team
    api_response = api_instance.retrieve_ldap_groups1(uuid)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling LdapApi->retrieve_ldap_groups1: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uuid** | [**str**](.md)| The UUID of the team to retrieve mappings for | 

### Return type

[**list[MappedLdapGroup]**](MappedLdapGroup.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

