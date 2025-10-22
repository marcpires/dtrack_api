# swagger_client.CalculatorApi

All URIs are relative to */api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_cvss_scores**](CalculatorApi.md#get_cvss_scores) | **GET** /v1/calculator/cvss | Returns the CVSS base score, impact sub-score and exploitability sub-score
[**get_owasp_rr_scores**](CalculatorApi.md#get_owasp_rr_scores) | **GET** /v1/calculator/owasp | Returns the OWASP Risk Rating likelihood score, technical impact score and business impact score

# **get_cvss_scores**
> Score get_cvss_scores(vector)

Returns the CVSS base score, impact sub-score and exploitability sub-score

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
api_instance = swagger_client.CalculatorApi(swagger_client.ApiClient(configuration))
vector = 'vector_example' # str | A valid CVSSv2 or CVSSv3 vector

try:
    # Returns the CVSS base score, impact sub-score and exploitability sub-score
    api_response = api_instance.get_cvss_scores(vector)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling CalculatorApi->get_cvss_scores: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **vector** | **str**| A valid CVSSv2 or CVSSv3 vector | 

### Return type

[**Score**](Score.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_owasp_rr_scores**
> Score get_owasp_rr_scores(vector)

Returns the OWASP Risk Rating likelihood score, technical impact score and business impact score

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
api_instance = swagger_client.CalculatorApi(swagger_client.ApiClient(configuration))
vector = 'vector_example' # str | A valid OWASP Risk Rating vector

try:
    # Returns the OWASP Risk Rating likelihood score, technical impact score and business impact score
    api_response = api_instance.get_owasp_rr_scores(vector)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling CalculatorApi->get_owasp_rr_scores: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **vector** | **str**| A valid OWASP Risk Rating vector | 

### Return type

[**Score**](Score.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

