# swagger_client.PolicyConditionApi

All URIs are relative to */api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_policy_condition**](PolicyConditionApi.md#create_policy_condition) | **PUT** /v1/policy/{uuid}/condition | Creates a new policy condition
[**delete_policy_condition**](PolicyConditionApi.md#delete_policy_condition) | **DELETE** /v1/policy/condition/{uuid} | Deletes a policy condition
[**update_policy_condition**](PolicyConditionApi.md#update_policy_condition) | **POST** /v1/policy/condition | Updates a policy condition

# **create_policy_condition**
> PolicyCondition create_policy_condition(uuid, body=body)

Creates a new policy condition

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
api_instance = swagger_client.PolicyConditionApi(swagger_client.ApiClient(configuration))
uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | The UUID of the policy
body = swagger_client.PolicyCondition() # PolicyCondition |  (optional)

try:
    # Creates a new policy condition
    api_response = api_instance.create_policy_condition(uuid, body=body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling PolicyConditionApi->create_policy_condition: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uuid** | [**str**](.md)| The UUID of the policy | 
 **body** | [**PolicyCondition**](PolicyCondition.md)|  | [optional] 

### Return type

[**PolicyCondition**](PolicyCondition.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_policy_condition**
> delete_policy_condition(uuid)

Deletes a policy condition

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
api_instance = swagger_client.PolicyConditionApi(swagger_client.ApiClient(configuration))
uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | The UUID of the policy condition to delete

try:
    # Deletes a policy condition
    api_instance.delete_policy_condition(uuid)
except ApiException as e:
    print("Exception when calling PolicyConditionApi->delete_policy_condition: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uuid** | [**str**](.md)| The UUID of the policy condition to delete | 

### Return type

void (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_policy_condition**
> PolicyCondition update_policy_condition(body=body)

Updates a policy condition

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
api_instance = swagger_client.PolicyConditionApi(swagger_client.ApiClient(configuration))
body = swagger_client.PolicyCondition() # PolicyCondition |  (optional)

try:
    # Updates a policy condition
    api_response = api_instance.update_policy_condition(body=body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling PolicyConditionApi->update_policy_condition: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**PolicyCondition**](PolicyCondition.md)|  | [optional] 

### Return type

[**PolicyCondition**](PolicyCondition.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

