# swagger_client.ViolationApi

All URIs are relative to */api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_violations**](ViolationApi.md#get_violations) | **GET** /v1/violation | Returns a list of all policy violations for the entire portfolio
[**get_violations_by_component**](ViolationApi.md#get_violations_by_component) | **GET** /v1/violation/component/{uuid} | Returns a list of all policy violations for a specific component
[**get_violations_by_project**](ViolationApi.md#get_violations_by_project) | **GET** /v1/violation/project/{uuid} | Returns a list of all policy violations for a specific project

# **get_violations**
> list[PolicyViolation] get_violations(page_number=page_number, page_size=page_size, offset=offset, limit=limit, sort_name=sort_name, sort_order=sort_order, suppressed=suppressed, show_inactive=show_inactive, violation_state=violation_state, risk_type=risk_type, policy=policy, analysis_state=analysis_state, occurred_on_date_from=occurred_on_date_from, occurred_on_date_to=occurred_on_date_to, text_search_field=text_search_field, text_search_input=text_search_input)

Returns a list of all policy violations for the entire portfolio

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
api_instance = swagger_client.ViolationApi(swagger_client.ApiClient(configuration))
page_number = '1' # str | The page to return. To be used in conjunction with <code>pageSize</code>. (optional) (default to 1)
page_size = '100' # str | Number of elements to return per page. To be used in conjunction with <code>pageNumber</code>. (optional) (default to 100)
offset = 'offset_example' # str | Offset to start returning elements from. To be used in conjunction with <code>limit</code>. (optional)
limit = 'limit_example' # str | Number of elements to return per page. To be used in conjunction with <code>offset</code>. (optional)
sort_name = 'sort_name_example' # str | Name of the resource field to sort on. (optional)
sort_order = 'sort_order_example' # str | Ordering of items when sorting with <code>sortName</code>. (optional)
suppressed = true # bool | Optionally includes suppressed violations (optional)
show_inactive = true # bool | Optionally includes inactive projects (optional)
violation_state = 'violation_state_example' # str | Filter by violation state (optional)
risk_type = 'risk_type_example' # str | Filter by risk type (optional)
policy = 'policy_example' # str | Filter by policy (optional)
analysis_state = 'analysis_state_example' # str | Filter by analysis state (optional)
occurred_on_date_from = 'occurred_on_date_from_example' # str | Filter occurred on from (optional)
occurred_on_date_to = 'occurred_on_date_to_example' # str | Filter occurred on to (optional)
text_search_field = 'text_search_field_example' # str | Filter the text input in these fields (optional)
text_search_input = 'text_search_input_example' # str | Filter by this text input (optional)

try:
    # Returns a list of all policy violations for the entire portfolio
    api_response = api_instance.get_violations(page_number=page_number, page_size=page_size, offset=offset, limit=limit, sort_name=sort_name, sort_order=sort_order, suppressed=suppressed, show_inactive=show_inactive, violation_state=violation_state, risk_type=risk_type, policy=policy, analysis_state=analysis_state, occurred_on_date_from=occurred_on_date_from, occurred_on_date_to=occurred_on_date_to, text_search_field=text_search_field, text_search_input=text_search_input)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling ViolationApi->get_violations: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page_number** | **str**| The page to return. To be used in conjunction with &lt;code&gt;pageSize&lt;/code&gt;. | [optional] [default to 1]
 **page_size** | **str**| Number of elements to return per page. To be used in conjunction with &lt;code&gt;pageNumber&lt;/code&gt;. | [optional] [default to 100]
 **offset** | **str**| Offset to start returning elements from. To be used in conjunction with &lt;code&gt;limit&lt;/code&gt;. | [optional] 
 **limit** | **str**| Number of elements to return per page. To be used in conjunction with &lt;code&gt;offset&lt;/code&gt;. | [optional] 
 **sort_name** | **str**| Name of the resource field to sort on. | [optional] 
 **sort_order** | **str**| Ordering of items when sorting with &lt;code&gt;sortName&lt;/code&gt;. | [optional] 
 **suppressed** | **bool**| Optionally includes suppressed violations | [optional] 
 **show_inactive** | **bool**| Optionally includes inactive projects | [optional] 
 **violation_state** | **str**| Filter by violation state | [optional] 
 **risk_type** | **str**| Filter by risk type | [optional] 
 **policy** | **str**| Filter by policy | [optional] 
 **analysis_state** | **str**| Filter by analysis state | [optional] 
 **occurred_on_date_from** | **str**| Filter occurred on from | [optional] 
 **occurred_on_date_to** | **str**| Filter occurred on to | [optional] 
 **text_search_field** | **str**| Filter the text input in these fields | [optional] 
 **text_search_input** | **str**| Filter by this text input | [optional] 

### Return type

[**list[PolicyViolation]**](PolicyViolation.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_violations_by_component**
> list[PolicyViolation] get_violations_by_component(uuid, page_number=page_number, page_size=page_size, offset=offset, limit=limit, sort_name=sort_name, sort_order=sort_order, suppressed=suppressed)

Returns a list of all policy violations for a specific component

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
api_instance = swagger_client.ViolationApi(swagger_client.ApiClient(configuration))
uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | The UUID of the component
page_number = '1' # str | The page to return. To be used in conjunction with <code>pageSize</code>. (optional) (default to 1)
page_size = '100' # str | Number of elements to return per page. To be used in conjunction with <code>pageNumber</code>. (optional) (default to 100)
offset = 'offset_example' # str | Offset to start returning elements from. To be used in conjunction with <code>limit</code>. (optional)
limit = 'limit_example' # str | Number of elements to return per page. To be used in conjunction with <code>offset</code>. (optional)
sort_name = 'sort_name_example' # str | Name of the resource field to sort on. (optional)
sort_order = 'sort_order_example' # str | Ordering of items when sorting with <code>sortName</code>. (optional)
suppressed = true # bool | Optionally includes suppressed violations (optional)

try:
    # Returns a list of all policy violations for a specific component
    api_response = api_instance.get_violations_by_component(uuid, page_number=page_number, page_size=page_size, offset=offset, limit=limit, sort_name=sort_name, sort_order=sort_order, suppressed=suppressed)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling ViolationApi->get_violations_by_component: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uuid** | [**str**](.md)| The UUID of the component | 
 **page_number** | **str**| The page to return. To be used in conjunction with &lt;code&gt;pageSize&lt;/code&gt;. | [optional] [default to 1]
 **page_size** | **str**| Number of elements to return per page. To be used in conjunction with &lt;code&gt;pageNumber&lt;/code&gt;. | [optional] [default to 100]
 **offset** | **str**| Offset to start returning elements from. To be used in conjunction with &lt;code&gt;limit&lt;/code&gt;. | [optional] 
 **limit** | **str**| Number of elements to return per page. To be used in conjunction with &lt;code&gt;offset&lt;/code&gt;. | [optional] 
 **sort_name** | **str**| Name of the resource field to sort on. | [optional] 
 **sort_order** | **str**| Ordering of items when sorting with &lt;code&gt;sortName&lt;/code&gt;. | [optional] 
 **suppressed** | **bool**| Optionally includes suppressed violations | [optional] 

### Return type

[**list[PolicyViolation]**](PolicyViolation.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_violations_by_project**
> list[PolicyViolation] get_violations_by_project(uuid, page_number=page_number, page_size=page_size, offset=offset, limit=limit, sort_name=sort_name, sort_order=sort_order, suppressed=suppressed)

Returns a list of all policy violations for a specific project

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
api_instance = swagger_client.ViolationApi(swagger_client.ApiClient(configuration))
uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | The UUID of the project
page_number = '1' # str | The page to return. To be used in conjunction with <code>pageSize</code>. (optional) (default to 1)
page_size = '100' # str | Number of elements to return per page. To be used in conjunction with <code>pageNumber</code>. (optional) (default to 100)
offset = 'offset_example' # str | Offset to start returning elements from. To be used in conjunction with <code>limit</code>. (optional)
limit = 'limit_example' # str | Number of elements to return per page. To be used in conjunction with <code>offset</code>. (optional)
sort_name = 'sort_name_example' # str | Name of the resource field to sort on. (optional)
sort_order = 'sort_order_example' # str | Ordering of items when sorting with <code>sortName</code>. (optional)
suppressed = true # bool | Optionally includes suppressed violations (optional)

try:
    # Returns a list of all policy violations for a specific project
    api_response = api_instance.get_violations_by_project(uuid, page_number=page_number, page_size=page_size, offset=offset, limit=limit, sort_name=sort_name, sort_order=sort_order, suppressed=suppressed)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling ViolationApi->get_violations_by_project: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uuid** | [**str**](.md)| The UUID of the project | 
 **page_number** | **str**| The page to return. To be used in conjunction with &lt;code&gt;pageSize&lt;/code&gt;. | [optional] [default to 1]
 **page_size** | **str**| Number of elements to return per page. To be used in conjunction with &lt;code&gt;pageNumber&lt;/code&gt;. | [optional] [default to 100]
 **offset** | **str**| Offset to start returning elements from. To be used in conjunction with &lt;code&gt;limit&lt;/code&gt;. | [optional] 
 **limit** | **str**| Number of elements to return per page. To be used in conjunction with &lt;code&gt;offset&lt;/code&gt;. | [optional] 
 **sort_name** | **str**| Name of the resource field to sort on. | [optional] 
 **sort_order** | **str**| Ordering of items when sorting with &lt;code&gt;sortName&lt;/code&gt;. | [optional] 
 **suppressed** | **bool**| Optionally includes suppressed violations | [optional] 

### Return type

[**list[PolicyViolation]**](PolicyViolation.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

