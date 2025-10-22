# swagger_client.FindingApi

All URIs are relative to */api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**analyze_project**](FindingApi.md#analyze_project) | **POST** /v1/finding/project/{uuid}/analyze | Triggers Vulnerability Analysis on a specific project
[**export_findings_by_project**](FindingApi.md#export_findings_by_project) | **GET** /v1/finding/project/{uuid}/export | Returns the findings for the specified project as FPF
[**get_all_findings**](FindingApi.md#get_all_findings) | **GET** /v1/finding/grouped | Returns a list of all findings grouped by vulnerability
[**get_all_findings1**](FindingApi.md#get_all_findings1) | **GET** /v1/finding | Returns a list of all findings
[**get_findings_by_project**](FindingApi.md#get_findings_by_project) | **GET** /v1/finding/project/{uuid} | Returns a list of all findings for a specific project or generates SARIF file if Accept: application/sarif+json header is provided

# **analyze_project**
> BomUploadResponse analyze_project(uuid)

Triggers Vulnerability Analysis on a specific project

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
api_instance = swagger_client.FindingApi(swagger_client.ApiClient(configuration))
uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | The UUID of the project to analyze

try:
    # Triggers Vulnerability Analysis on a specific project
    api_response = api_instance.analyze_project(uuid)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling FindingApi->analyze_project: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uuid** | [**str**](.md)| The UUID of the project to analyze | 

### Return type

[**BomUploadResponse**](BomUploadResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **export_findings_by_project**
> str export_findings_by_project(uuid)

Returns the findings for the specified project as FPF

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
api_instance = swagger_client.FindingApi(swagger_client.ApiClient(configuration))
uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | The UUID of the project

try:
    # Returns the findings for the specified project as FPF
    api_response = api_instance.export_findings_by_project(uuid)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling FindingApi->export_findings_by_project: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uuid** | [**str**](.md)| The UUID of the project | 

### Return type

**str**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_all_findings**
> list[Finding] get_all_findings(show_inactive=show_inactive, severity=severity, publish_date_from=publish_date_from, publish_date_to=publish_date_to, text_search_field=text_search_field, text_search_input=text_search_input, cvssv2_from=cvssv2_from, cvssv2_to=cvssv2_to, cvssv3_from=cvssv3_from, cvssv3_to=cvssv3_to, occurrences_from=occurrences_from, occurrences_to=occurrences_to)

Returns a list of all findings grouped by vulnerability

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
api_instance = swagger_client.FindingApi(swagger_client.ApiClient(configuration))
show_inactive = true # bool | Show inactive projects (optional)
severity = 'severity_example' # str | Filter by severity (optional)
publish_date_from = 'publish_date_from_example' # str | Filter published from this date (optional)
publish_date_to = 'publish_date_to_example' # str | Filter published to this date (optional)
text_search_field = 'text_search_field_example' # str | Filter the text input in these fields (optional)
text_search_input = 'text_search_input_example' # str | Filter by this text input (optional)
cvssv2_from = 'cvssv2_from_example' # str | Filter CVSSv2 from this value (optional)
cvssv2_to = 'cvssv2_to_example' # str | Filter CVSSv2 to this value (optional)
cvssv3_from = 'cvssv3_from_example' # str | Filter CVSSv3 from this value (optional)
cvssv3_to = 'cvssv3_to_example' # str | Filter CVSSv3 to this value (optional)
occurrences_from = 'occurrences_from_example' # str | Filter occurrences in projects from this value (optional)
occurrences_to = 'occurrences_to_example' # str | Filter occurrences in projects to this value (optional)

try:
    # Returns a list of all findings grouped by vulnerability
    api_response = api_instance.get_all_findings(show_inactive=show_inactive, severity=severity, publish_date_from=publish_date_from, publish_date_to=publish_date_to, text_search_field=text_search_field, text_search_input=text_search_input, cvssv2_from=cvssv2_from, cvssv2_to=cvssv2_to, cvssv3_from=cvssv3_from, cvssv3_to=cvssv3_to, occurrences_from=occurrences_from, occurrences_to=occurrences_to)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling FindingApi->get_all_findings: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **show_inactive** | **bool**| Show inactive projects | [optional] 
 **severity** | **str**| Filter by severity | [optional] 
 **publish_date_from** | **str**| Filter published from this date | [optional] 
 **publish_date_to** | **str**| Filter published to this date | [optional] 
 **text_search_field** | **str**| Filter the text input in these fields | [optional] 
 **text_search_input** | **str**| Filter by this text input | [optional] 
 **cvssv2_from** | **str**| Filter CVSSv2 from this value | [optional] 
 **cvssv2_to** | **str**| Filter CVSSv2 to this value | [optional] 
 **cvssv3_from** | **str**| Filter CVSSv3 from this value | [optional] 
 **cvssv3_to** | **str**| Filter CVSSv3 to this value | [optional] 
 **occurrences_from** | **str**| Filter occurrences in projects from this value | [optional] 
 **occurrences_to** | **str**| Filter occurrences in projects to this value | [optional] 

### Return type

[**list[Finding]**](Finding.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_all_findings1**
> list[Finding] get_all_findings1(show_inactive=show_inactive, show_suppressed=show_suppressed, severity=severity, analysis_status=analysis_status, vendor_response=vendor_response, publish_date_from=publish_date_from, publish_date_to=publish_date_to, attributed_on_date_from=attributed_on_date_from, attributed_on_date_to=attributed_on_date_to, text_search_field=text_search_field, text_search_input=text_search_input, cvssv2_from=cvssv2_from, cvssv2_to=cvssv2_to, cvssv3_from=cvssv3_from, cvssv3_to=cvssv3_to)

Returns a list of all findings

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
api_instance = swagger_client.FindingApi(swagger_client.ApiClient(configuration))
show_inactive = true # bool | Show inactive projects (optional)
show_suppressed = true # bool | Show suppressed findings (optional)
severity = 'severity_example' # str | Filter by severity (optional)
analysis_status = 'analysis_status_example' # str | Filter by analysis status (optional)
vendor_response = 'vendor_response_example' # str | Filter by vendor response (optional)
publish_date_from = 'publish_date_from_example' # str | Filter published from this date (optional)
publish_date_to = 'publish_date_to_example' # str | Filter published to this date (optional)
attributed_on_date_from = 'attributed_on_date_from_example' # str | Filter attributed on from this date (optional)
attributed_on_date_to = 'attributed_on_date_to_example' # str | Filter attributed on to this date (optional)
text_search_field = 'text_search_field_example' # str | Filter the text input in these fields (optional)
text_search_input = 'text_search_input_example' # str | Filter by this text input (optional)
cvssv2_from = 'cvssv2_from_example' # str | Filter CVSSv2 from this value (optional)
cvssv2_to = 'cvssv2_to_example' # str | Filter CVSSv2 from this Value (optional)
cvssv3_from = 'cvssv3_from_example' # str | Filter CVSSv3 from this value (optional)
cvssv3_to = 'cvssv3_to_example' # str | Filter CVSSv3 from this Value (optional)

try:
    # Returns a list of all findings
    api_response = api_instance.get_all_findings1(show_inactive=show_inactive, show_suppressed=show_suppressed, severity=severity, analysis_status=analysis_status, vendor_response=vendor_response, publish_date_from=publish_date_from, publish_date_to=publish_date_to, attributed_on_date_from=attributed_on_date_from, attributed_on_date_to=attributed_on_date_to, text_search_field=text_search_field, text_search_input=text_search_input, cvssv2_from=cvssv2_from, cvssv2_to=cvssv2_to, cvssv3_from=cvssv3_from, cvssv3_to=cvssv3_to)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling FindingApi->get_all_findings1: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **show_inactive** | **bool**| Show inactive projects | [optional] 
 **show_suppressed** | **bool**| Show suppressed findings | [optional] 
 **severity** | **str**| Filter by severity | [optional] 
 **analysis_status** | **str**| Filter by analysis status | [optional] 
 **vendor_response** | **str**| Filter by vendor response | [optional] 
 **publish_date_from** | **str**| Filter published from this date | [optional] 
 **publish_date_to** | **str**| Filter published to this date | [optional] 
 **attributed_on_date_from** | **str**| Filter attributed on from this date | [optional] 
 **attributed_on_date_to** | **str**| Filter attributed on to this date | [optional] 
 **text_search_field** | **str**| Filter the text input in these fields | [optional] 
 **text_search_input** | **str**| Filter by this text input | [optional] 
 **cvssv2_from** | **str**| Filter CVSSv2 from this value | [optional] 
 **cvssv2_to** | **str**| Filter CVSSv2 from this Value | [optional] 
 **cvssv3_from** | **str**| Filter CVSSv3 from this value | [optional] 
 **cvssv3_to** | **str**| Filter CVSSv3 from this Value | [optional] 

### Return type

[**list[Finding]**](Finding.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_findings_by_project**
> list[Finding] get_findings_by_project(uuid, suppressed=suppressed, source=source, accept=accept)

Returns a list of all findings for a specific project or generates SARIF file if Accept: application/sarif+json header is provided

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
api_instance = swagger_client.FindingApi(swagger_client.ApiClient(configuration))
uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | The UUID of the project
suppressed = true # bool | Optionally includes suppressed findings (optional)
source = 'source_example' # str | Optionally limit findings to specific sources of vulnerability intelligence (optional)
accept = 'accept_example' # str |  (optional)

try:
    # Returns a list of all findings for a specific project or generates SARIF file if Accept: application/sarif+json header is provided
    api_response = api_instance.get_findings_by_project(uuid, suppressed=suppressed, source=source, accept=accept)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling FindingApi->get_findings_by_project: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uuid** | [**str**](.md)| The UUID of the project | 
 **suppressed** | **bool**| Optionally includes suppressed findings | [optional] 
 **source** | **str**| Optionally limit findings to specific sources of vulnerability intelligence | [optional] 
 **accept** | **str**|  | [optional] 

### Return type

[**list[Finding]**](Finding.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/sarif+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

