# swagger_client.TeamApi

All URIs are relative to */api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**available_teams**](TeamApi.md#available_teams) | **GET** /v1/team/visible | Returns a list of Teams that are visible
[**create_team**](TeamApi.md#create_team) | **PUT** /v1/team | Creates a new team
[**delete_api_key**](TeamApi.md#delete_api_key) | **DELETE** /v1/team/key/{publicIdOrKey} | Deletes the specified API key
[**delete_team**](TeamApi.md#delete_team) | **DELETE** /v1/team | Deletes a team
[**generate_api_key**](TeamApi.md#generate_api_key) | **PUT** /v1/team/{uuid}/key | Generates an API key and returns its value
[**get_self**](TeamApi.md#get_self) | **GET** /v1/team/self | Returns information about the current team.
[**get_team**](TeamApi.md#get_team) | **GET** /v1/team/{uuid} | Returns a specific team
[**get_teams**](TeamApi.md#get_teams) | **GET** /v1/team | Returns a list of all teams
[**regenerate_api_key**](TeamApi.md#regenerate_api_key) | **POST** /v1/team/key/{publicIdOrKey} | Regenerates an API key by removing the specified key, generating a new one and returning its value
[**update_api_key_comment**](TeamApi.md#update_api_key_comment) | **POST** /v1/team/key/{publicIdOrKey}/comment | Updates an API key&#x27;s comment
[**update_team**](TeamApi.md#update_team) | **POST** /v1/team | Updates a team&#x27;s fields

# **available_teams**
> list[VisibleTeams] available_teams()

Returns a list of Teams that are visible

<p></p>

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
api_instance = swagger_client.TeamApi(swagger_client.ApiClient(configuration))

try:
    # Returns a list of Teams that are visible
    api_response = api_instance.available_teams()
    pprint(api_response)
except ApiException as e:
    print("Exception when calling TeamApi->available_teams: %s\n" % e)
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**list[VisibleTeams]**](VisibleTeams.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_team**
> Team create_team(body=body)

Creates a new team

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
api_instance = swagger_client.TeamApi(swagger_client.ApiClient(configuration))
body = swagger_client.Team() # Team |  (optional)

try:
    # Creates a new team
    api_response = api_instance.create_team(body=body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling TeamApi->create_team: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**Team**](Team.md)|  | [optional] 

### Return type

[**Team**](Team.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_api_key**
> delete_api_key(public_id_or_key)

Deletes the specified API key

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
api_instance = swagger_client.TeamApi(swagger_client.ApiClient(configuration))
public_id_or_key = 'public_id_or_key_example' # str | The public ID for the API key or for Legacy the full Key to delete

try:
    # Deletes the specified API key
    api_instance.delete_api_key(public_id_or_key)
except ApiException as e:
    print("Exception when calling TeamApi->delete_api_key: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **public_id_or_key** | **str**| The public ID for the API key or for Legacy the full Key to delete | 

### Return type

void (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_team**
> delete_team(body=body)

Deletes a team

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
api_instance = swagger_client.TeamApi(swagger_client.ApiClient(configuration))
body = swagger_client.Team() # Team |  (optional)

try:
    # Deletes a team
    api_instance.delete_team(body=body)
except ApiException as e:
    print("Exception when calling TeamApi->delete_team: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**Team**](Team.md)|  | [optional] 

### Return type

void (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **generate_api_key**
> ApiKey generate_api_key(uuid)

Generates an API key and returns its value

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
api_instance = swagger_client.TeamApi(swagger_client.ApiClient(configuration))
uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | The UUID of the team to generate a key for

try:
    # Generates an API key and returns its value
    api_response = api_instance.generate_api_key(uuid)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling TeamApi->generate_api_key: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uuid** | [**str**](.md)| The UUID of the team to generate a key for | 

### Return type

[**ApiKey**](ApiKey.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_self**
> TeamSelfResponse get_self()

Returns information about the current team.

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
api_instance = swagger_client.TeamApi(swagger_client.ApiClient(configuration))

try:
    # Returns information about the current team.
    api_response = api_instance.get_self()
    pprint(api_response)
except ApiException as e:
    print("Exception when calling TeamApi->get_self: %s\n" % e)
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**TeamSelfResponse**](TeamSelfResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_team**
> Team get_team(uuid)

Returns a specific team

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
api_instance = swagger_client.TeamApi(swagger_client.ApiClient(configuration))
uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | The UUID of the team to retrieve

try:
    # Returns a specific team
    api_response = api_instance.get_team(uuid)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling TeamApi->get_team: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uuid** | [**str**](.md)| The UUID of the team to retrieve | 

### Return type

[**Team**](Team.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_teams**
> list[Team] get_teams()

Returns a list of all teams

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
api_instance = swagger_client.TeamApi(swagger_client.ApiClient(configuration))

try:
    # Returns a list of all teams
    api_response = api_instance.get_teams()
    pprint(api_response)
except ApiException as e:
    print("Exception when calling TeamApi->get_teams: %s\n" % e)
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**list[Team]**](Team.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **regenerate_api_key**
> ApiKey regenerate_api_key(public_id_or_key)

Regenerates an API key by removing the specified key, generating a new one and returning its value

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
api_instance = swagger_client.TeamApi(swagger_client.ApiClient(configuration))
public_id_or_key = 'public_id_or_key_example' # str | The public ID for the API key or for Legacy the complete Key to regenerate

try:
    # Regenerates an API key by removing the specified key, generating a new one and returning its value
    api_response = api_instance.regenerate_api_key(public_id_or_key)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling TeamApi->regenerate_api_key: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **public_id_or_key** | **str**| The public ID for the API key or for Legacy the complete Key to regenerate | 

### Return type

[**ApiKey**](ApiKey.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_api_key_comment**
> ApiKey update_api_key_comment(public_id_or_key, body=body)

Updates an API key's comment

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
api_instance = swagger_client.TeamApi(swagger_client.ApiClient(configuration))
public_id_or_key = 'public_id_or_key_example' # str | The public ID for the API key or for Legacy the complete Key to comment on
body = 'body_example' # str |  (optional)

try:
    # Updates an API key's comment
    api_response = api_instance.update_api_key_comment(public_id_or_key, body=body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling TeamApi->update_api_key_comment: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **public_id_or_key** | **str**| The public ID for the API key or for Legacy the complete Key to comment on | 
 **body** | [**str**](str.md)|  | [optional] 

### Return type

[**ApiKey**](ApiKey.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: text/plain
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_team**
> Team update_team(body=body)

Updates a team's fields

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
api_instance = swagger_client.TeamApi(swagger_client.ApiClient(configuration))
body = swagger_client.Team() # Team |  (optional)

try:
    # Updates a team's fields
    api_response = api_instance.update_team(body=body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling TeamApi->update_team: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**Team**](Team.md)|  | [optional] 

### Return type

[**Team**](Team.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

