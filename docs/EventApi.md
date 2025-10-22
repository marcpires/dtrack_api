# swagger_client.EventApi

All URIs are relative to */api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**is_token_being_processed1**](EventApi.md#is_token_being_processed1) | **GET** /v1/event/token/{uuid} | Determines if there are any tasks associated with the token that are being processed, or in the queue to be processed.

# **is_token_being_processed1**
> IsTokenBeingProcessedResponse is_token_being_processed1(uuid)

Determines if there are any tasks associated with the token that are being processed, or in the queue to be processed.

<p>   This endpoint is intended to be used in conjunction with other API calls which return a token for asynchronous tasks.   The token can then be queried using this endpoint to determine if the task is complete:   <ul>     <li>A value of <code>true</code> indicates processing is occurring.</li>     <li>A value of <code>false</code> indicates that no processing is occurring for the specified token.</li>   </ul>   However, a value of <code>false</code> also does not confirm the token is valid,   only that no processing is associated with the specified token. </p>

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
api_instance = swagger_client.EventApi(swagger_client.ApiClient(configuration))
uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | The UUID of the token to query

try:
    # Determines if there are any tasks associated with the token that are being processed, or in the queue to be processed.
    api_response = api_instance.is_token_being_processed1(uuid)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling EventApi->is_token_being_processed1: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uuid** | [**str**](.md)| The UUID of the token to query | 

### Return type

[**IsTokenBeingProcessedResponse**](IsTokenBeingProcessedResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

