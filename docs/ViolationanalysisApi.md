# swagger_client.ViolationanalysisApi

All URIs are relative to */api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**retrieve_analysis1**](ViolationanalysisApi.md#retrieve_analysis1) | **GET** /v1/violation/analysis | Retrieves a violation analysis trail
[**update_analysis1**](ViolationanalysisApi.md#update_analysis1) | **PUT** /v1/violation/analysis | Records a violation analysis decision

# **retrieve_analysis1**
> ViolationAnalysis retrieve_analysis1(component, policy_violation)

Retrieves a violation analysis trail

<p>Requires permission <strong>VIEW_POLICY_VIOLATION</strong></p>

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
api_instance = swagger_client.ViolationanalysisApi(swagger_client.ApiClient(configuration))
component = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | The UUID of the component
policy_violation = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | The UUID of the policy violation

try:
    # Retrieves a violation analysis trail
    api_response = api_instance.retrieve_analysis1(component, policy_violation)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling ViolationanalysisApi->retrieve_analysis1: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **component** | [**str**](.md)| The UUID of the component | 
 **policy_violation** | [**str**](.md)| The UUID of the policy violation | 

### Return type

[**ViolationAnalysis**](ViolationAnalysis.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_analysis1**
> ViolationAnalysis update_analysis1(body=body)

Records a violation analysis decision

<p>Requires permission <strong>POLICY_VIOLATION_ANALYSIS</strong></p>

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
api_instance = swagger_client.ViolationanalysisApi(swagger_client.ApiClient(configuration))
body = swagger_client.ViolationAnalysisRequest() # ViolationAnalysisRequest |  (optional)

try:
    # Records a violation analysis decision
    api_response = api_instance.update_analysis1(body=body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling ViolationanalysisApi->update_analysis1: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**ViolationAnalysisRequest**](ViolationAnalysisRequest.md)|  | [optional] 

### Return type

[**ViolationAnalysis**](ViolationAnalysis.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

