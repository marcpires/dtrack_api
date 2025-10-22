# swagger_client.UserApi

All URIs are relative to */api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**add_team_to_user**](UserApi.md#add_team_to_user) | **POST** /v1/user/{username}/membership | Adds the username to the specified team.
[**create_ldap_user**](UserApi.md#create_ldap_user) | **PUT** /v1/user/ldap | Creates a new user that references an existing LDAP object.
[**create_managed_user**](UserApi.md#create_managed_user) | **PUT** /v1/user/managed | Creates a new user.
[**create_oidc_user**](UserApi.md#create_oidc_user) | **PUT** /v1/user/oidc | Creates a new user that references an existing OpenID Connect user.
[**delete_ldap_user**](UserApi.md#delete_ldap_user) | **DELETE** /v1/user/ldap | Deletes a user.
[**delete_managed_user**](UserApi.md#delete_managed_user) | **DELETE** /v1/user/managed | Deletes a user.
[**delete_oidc_user**](UserApi.md#delete_oidc_user) | **DELETE** /v1/user/oidc | Deletes an OpenID Connect user.
[**force_change_password**](UserApi.md#force_change_password) | **POST** /v1/user/forceChangePassword | Asserts login credentials and upon successful authentication, verifies passwords match and changes users password
[**get_ldap_users**](UserApi.md#get_ldap_users) | **GET** /v1/user/ldap | Returns a list of all LDAP users
[**get_managed_users**](UserApi.md#get_managed_users) | **GET** /v1/user/managed | Returns a list of all managed users
[**get_oidc_users**](UserApi.md#get_oidc_users) | **GET** /v1/user/oidc | Returns a list of all OIDC users
[**get_self1**](UserApi.md#get_self1) | **GET** /v1/user/self | Returns information about the current logged in user.
[**remove_team_from_user**](UserApi.md#remove_team_from_user) | **DELETE** /v1/user/{username}/membership | Removes the username from the specified team.
[**update_managed_user**](UserApi.md#update_managed_user) | **POST** /v1/user/managed | Updates a managed user.
[**update_self**](UserApi.md#update_self) | **POST** /v1/user/self | Updates information about the current logged in user.
[**validate_credentials**](UserApi.md#validate_credentials) | **POST** /v1/user/login | Assert login credentials
[**validate_oidc_access_token**](UserApi.md#validate_oidc_access_token) | **POST** /v1/user/oidc/login | Login with OpenID Connect

# **add_team_to_user**
> UserPrincipal add_team_to_user(body, username)

Adds the username to the specified team.

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
api_instance = swagger_client.UserApi(swagger_client.ApiClient(configuration))
body = swagger_client.IdentifiableObject() # IdentifiableObject | The UUID of the team to associate username with
username = 'username_example' # str | A valid username

try:
    # Adds the username to the specified team.
    api_response = api_instance.add_team_to_user(body, username)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling UserApi->add_team_to_user: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**IdentifiableObject**](IdentifiableObject.md)| The UUID of the team to associate username with | 
 **username** | **str**| A valid username | 

### Return type

[**UserPrincipal**](UserPrincipal.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_ldap_user**
> LdapUser create_ldap_user(body=body)

Creates a new user that references an existing LDAP object.

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
api_instance = swagger_client.UserApi(swagger_client.ApiClient(configuration))
body = swagger_client.LdapUser() # LdapUser |  (optional)

try:
    # Creates a new user that references an existing LDAP object.
    api_response = api_instance.create_ldap_user(body=body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling UserApi->create_ldap_user: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**LdapUser**](LdapUser.md)|  | [optional] 

### Return type

[**LdapUser**](LdapUser.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_managed_user**
> ManagedUser create_managed_user(body=body)

Creates a new user.

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
api_instance = swagger_client.UserApi(swagger_client.ApiClient(configuration))
body = swagger_client.ManagedUser() # ManagedUser |  (optional)

try:
    # Creates a new user.
    api_response = api_instance.create_managed_user(body=body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling UserApi->create_managed_user: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**ManagedUser**](ManagedUser.md)|  | [optional] 

### Return type

[**ManagedUser**](ManagedUser.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_oidc_user**
> OidcUser create_oidc_user(body=body)

Creates a new user that references an existing OpenID Connect user.

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
api_instance = swagger_client.UserApi(swagger_client.ApiClient(configuration))
body = swagger_client.OidcUser() # OidcUser |  (optional)

try:
    # Creates a new user that references an existing OpenID Connect user.
    api_response = api_instance.create_oidc_user(body=body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling UserApi->create_oidc_user: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**OidcUser**](OidcUser.md)|  | [optional] 

### Return type

[**OidcUser**](OidcUser.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_ldap_user**
> delete_ldap_user(body=body)

Deletes a user.

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
api_instance = swagger_client.UserApi(swagger_client.ApiClient(configuration))
body = swagger_client.LdapUser() # LdapUser |  (optional)

try:
    # Deletes a user.
    api_instance.delete_ldap_user(body=body)
except ApiException as e:
    print("Exception when calling UserApi->delete_ldap_user: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**LdapUser**](LdapUser.md)|  | [optional] 

### Return type

void (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_managed_user**
> delete_managed_user(body=body)

Deletes a user.

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
api_instance = swagger_client.UserApi(swagger_client.ApiClient(configuration))
body = swagger_client.ManagedUser() # ManagedUser |  (optional)

try:
    # Deletes a user.
    api_instance.delete_managed_user(body=body)
except ApiException as e:
    print("Exception when calling UserApi->delete_managed_user: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**ManagedUser**](ManagedUser.md)|  | [optional] 

### Return type

void (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_oidc_user**
> delete_oidc_user(body=body)

Deletes an OpenID Connect user.

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
api_instance = swagger_client.UserApi(swagger_client.ApiClient(configuration))
body = swagger_client.OidcUser() # OidcUser |  (optional)

try:
    # Deletes an OpenID Connect user.
    api_instance.delete_oidc_user(body=body)
except ApiException as e:
    print("Exception when calling UserApi->delete_oidc_user: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**OidcUser**](OidcUser.md)|  | [optional] 

### Return type

void (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **force_change_password**
> force_change_password(username=username, password=password, new_password=new_password, confirm_password=confirm_password)

Asserts login credentials and upon successful authentication, verifies passwords match and changes users password

Upon a successful login, a JSON Web Token will be returned in the response body. This functionality requires authentication to be enabled.

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
api_instance = swagger_client.UserApi(swagger_client.ApiClient(configuration))
username = 'username_example' # str |  (optional)
password = 'password_example' # str |  (optional)
new_password = 'new_password_example' # str |  (optional)
confirm_password = 'confirm_password_example' # str |  (optional)

try:
    # Asserts login credentials and upon successful authentication, verifies passwords match and changes users password
    api_instance.force_change_password(username=username, password=password, new_password=new_password, confirm_password=confirm_password)
except ApiException as e:
    print("Exception when calling UserApi->force_change_password: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **username** | **str**|  | [optional] 
 **password** | **str**|  | [optional] 
 **new_password** | **str**|  | [optional] 
 **confirm_password** | **str**|  | [optional] 

### Return type

void (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_ldap_users**
> list[LdapUser] get_ldap_users()

Returns a list of all LDAP users

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
api_instance = swagger_client.UserApi(swagger_client.ApiClient(configuration))

try:
    # Returns a list of all LDAP users
    api_response = api_instance.get_ldap_users()
    pprint(api_response)
except ApiException as e:
    print("Exception when calling UserApi->get_ldap_users: %s\n" % e)
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**list[LdapUser]**](LdapUser.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_managed_users**
> list[ManagedUser] get_managed_users()

Returns a list of all managed users

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
api_instance = swagger_client.UserApi(swagger_client.ApiClient(configuration))

try:
    # Returns a list of all managed users
    api_response = api_instance.get_managed_users()
    pprint(api_response)
except ApiException as e:
    print("Exception when calling UserApi->get_managed_users: %s\n" % e)
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**list[ManagedUser]**](ManagedUser.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_oidc_users**
> list[OidcUser] get_oidc_users()

Returns a list of all OIDC users

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
api_instance = swagger_client.UserApi(swagger_client.ApiClient(configuration))

try:
    # Returns a list of all OIDC users
    api_response = api_instance.get_oidc_users()
    pprint(api_response)
except ApiException as e:
    print("Exception when calling UserApi->get_oidc_users: %s\n" % e)
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**list[OidcUser]**](OidcUser.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_self1**
> UserPrincipal get_self1()

Returns information about the current logged in user.

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
api_instance = swagger_client.UserApi(swagger_client.ApiClient(configuration))

try:
    # Returns information about the current logged in user.
    api_response = api_instance.get_self1()
    pprint(api_response)
except ApiException as e:
    print("Exception when calling UserApi->get_self1: %s\n" % e)
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**UserPrincipal**](UserPrincipal.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **remove_team_from_user**
> UserPrincipal remove_team_from_user(body, username)

Removes the username from the specified team.

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
api_instance = swagger_client.UserApi(swagger_client.ApiClient(configuration))
body = swagger_client.IdentifiableObject() # IdentifiableObject | The UUID of the team to un-associate username from
username = 'username_example' # str | A valid username

try:
    # Removes the username from the specified team.
    api_response = api_instance.remove_team_from_user(body, username)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling UserApi->remove_team_from_user: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**IdentifiableObject**](IdentifiableObject.md)| The UUID of the team to un-associate username from | 
 **username** | **str**| A valid username | 

### Return type

[**UserPrincipal**](UserPrincipal.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_managed_user**
> ManagedUser update_managed_user(body=body)

Updates a managed user.

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
api_instance = swagger_client.UserApi(swagger_client.ApiClient(configuration))
body = swagger_client.ManagedUser() # ManagedUser |  (optional)

try:
    # Updates a managed user.
    api_response = api_instance.update_managed_user(body=body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling UserApi->update_managed_user: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**ManagedUser**](ManagedUser.md)|  | [optional] 

### Return type

[**ManagedUser**](ManagedUser.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_self**
> ManagedUser update_self(body=body)

Updates information about the current logged in user.

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
api_instance = swagger_client.UserApi(swagger_client.ApiClient(configuration))
body = swagger_client.ManagedUser() # ManagedUser |  (optional)

try:
    # Updates information about the current logged in user.
    api_response = api_instance.update_self(body=body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling UserApi->update_self: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**ManagedUser**](ManagedUser.md)|  | [optional] 

### Return type

[**ManagedUser**](ManagedUser.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: */*
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **validate_credentials**
> str validate_credentials(username=username, password=password)

Assert login credentials

Upon a successful login, a JSON Web Token will be returned in the response body. This functionality requires authentication to be enabled.

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
api_instance = swagger_client.UserApi(swagger_client.ApiClient(configuration))
username = 'username_example' # str |  (optional)
password = 'password_example' # str |  (optional)

try:
    # Assert login credentials
    api_response = api_instance.validate_credentials(username=username, password=password)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling UserApi->validate_credentials: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **username** | **str**|  | [optional] 
 **password** | **str**|  | [optional] 

### Return type

**str**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: text/plain

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **validate_oidc_access_token**
> str validate_oidc_access_token(id_token=id_token, access_token=access_token)

Login with OpenID Connect

Upon a successful login, a JSON Web Token will be returned in the response body. This functionality requires authentication to be enabled.

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
api_instance = swagger_client.UserApi(swagger_client.ApiClient(configuration))
id_token = 'id_token_example' # str |  (optional)
access_token = 'access_token_example' # str |  (optional)

try:
    # Login with OpenID Connect
    api_response = api_instance.validate_oidc_access_token(id_token=id_token, access_token=access_token)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling UserApi->validate_oidc_access_token: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id_token** | **str**|  | [optional] 
 **access_token** | **str**|  | [optional] 

### Return type

**str**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: text/plain

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

