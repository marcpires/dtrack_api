# swagger_client.VexApi

All URIs are relative to */api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**export_project_as_cyclone_dx1**](VexApi.md#export_project_as_cyclone_dx1) | **GET** /v1/vex/cyclonedx/project/{uuid} | Returns a VEX for a project in CycloneDX format
[**upload_vex**](VexApi.md#upload_vex) | **PUT** /v1/vex | Upload a supported VEX document
[**upload_vex1**](VexApi.md#upload_vex1) | **POST** /v1/vex | Upload a supported VEX document

# **export_project_as_cyclone_dx1**
> str export_project_as_cyclone_dx1(uuid, download=download)

Returns a VEX for a project in CycloneDX format

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
api_instance = swagger_client.VexApi(swagger_client.ApiClient(configuration))
uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | The UUID of the project to export
download = true # bool | Force the resulting VEX to be downloaded as a file (defaults to 'false') (optional)

try:
    # Returns a VEX for a project in CycloneDX format
    api_response = api_instance.export_project_as_cyclone_dx1(uuid, download=download)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling VexApi->export_project_as_cyclone_dx1: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uuid** | [**str**](.md)| The UUID of the project to export | 
 **download** | **bool**| Force the resulting VEX to be downloaded as a file (defaults to &#x27;false&#x27;) | [optional] 

### Return type

**str**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.cyclonedx+json, application/octet-stream

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **upload_vex**
> BomUploadResponse upload_vex(body=body)

Upload a supported VEX document

<p>   Expects CycloneDX and a valid project UUID. If a UUID is not specified,   then the <code>projectName</code> and <code>projectVersion</code> must be specified. </p> <p>   The VEX will be validated against the CycloneDX schema. If schema validation fails,   a response with problem details in RFC 9457 format will be returned. In this case,   the response's content type will be <code>application/problem+json</code>. </p> <p>   The maximum allowed length of the <code>vex</code> value is 20'000'000 characters.   When uploading large VEX files, the <code>POST</code> endpoint is preferred,   as it does not have this limit. </p> <p>Requires permission <strong>VULNERABILITY_ANALYSIS</strong></p>

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
api_instance = swagger_client.VexApi(swagger_client.ApiClient(configuration))
body = swagger_client.VexSubmitRequest() # VexSubmitRequest |  (optional)

try:
    # Upload a supported VEX document
    api_response = api_instance.upload_vex(body=body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling VexApi->upload_vex: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**VexSubmitRequest**](VexSubmitRequest.md)|  | [optional] 

### Return type

[**BomUploadResponse**](BomUploadResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **upload_vex1**
> BomUploadResponse upload_vex1(project=project, project_name=project_name, project_version=project_version, vex=vex)

Upload a supported VEX document

<p>   Expects CycloneDX and a valid project UUID. If a UUID is not specified,   then the <code>projectName</code> and <code>projectVersion</code> must be specified. </p> <p>   The VEX will be validated against the CycloneDX schema. If schema validation fails,   a response with problem details in RFC 9457 format will be returned. In this case,   the response's content type will be <code>application/problem+json</code>. </p> <p>Requires permission <strong>VULNERABILITY_ANALYSIS</strong></p>

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
api_instance = swagger_client.VexApi(swagger_client.ApiClient(configuration))
project = 'project_example' # str |  (optional)
project_name = 'project_name_example' # str |  (optional)
project_version = 'project_version_example' # str |  (optional)
vex = 'vex_example' # str |  (optional)

try:
    # Upload a supported VEX document
    api_response = api_instance.upload_vex1(project=project, project_name=project_name, project_version=project_version, vex=vex)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling VexApi->upload_vex1: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project** | **str**|  | [optional] 
 **project_name** | **str**|  | [optional] 
 **project_version** | **str**|  | [optional] 
 **vex** | **str**|  | [optional] 

### Return type

[**BomUploadResponse**](BomUploadResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

