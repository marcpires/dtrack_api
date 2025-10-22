# swagger_client.AnalysisApi

All URIs are relative to */api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**retrieve_analysis**](AnalysisApi.md#retrieve_analysis) | **GET** /v1/analysis | Retrieves an analysis trail
[**update_analysis**](AnalysisApi.md#update_analysis) | **PUT** /v1/analysis | Records an analysis decision

# **retrieve_analysis**
> Analysis retrieve_analysis(component, vulnerability, project=project)

Retrieves an analysis trail

<p>Requires permission <strong>VIEW_VULNERABILITY</strong></p>

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
api_instance = swagger_client.AnalysisApi(swagger_client.ApiClient(configuration))
component = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | The UUID of the component
vulnerability = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | The UUID of the vulnerability
project = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | The UUID of the project (optional)

try:
    # Retrieves an analysis trail
    api_response = api_instance.retrieve_analysis(component, vulnerability, project=project)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling AnalysisApi->retrieve_analysis: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **component** | [**str**](.md)| The UUID of the component | 
 **vulnerability** | [**str**](.md)| The UUID of the vulnerability | 
 **project** | [**str**](.md)| The UUID of the project | [optional] 

### Return type

[**Analysis**](Analysis.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_analysis**
> Analysis update_analysis(body=body)

Records an analysis decision

<p>Requires permission <strong>VULNERABILITY_ANALYSIS</strong></p>

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
api_instance = swagger_client.AnalysisApi(swagger_client.ApiClient(configuration))
body = swagger_client.AnalysisRequest() # AnalysisRequest |  (optional)

try:
    # Records an analysis decision
    api_response = api_instance.update_analysis(body=body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling AnalysisApi->update_analysis: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**AnalysisRequest**](AnalysisRequest.md)|  | [optional] 

### Return type

[**Analysis**](Analysis.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

