# swagger_client.BomApi

All URIs are relative to */api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**export_component_as_cyclone_dx**](BomApi.md#export_component_as_cyclone_dx) | **GET** /v1/bom/cyclonedx/component/{uuid} | Returns dependency metadata for a specific component in CycloneDX format
[**export_project_as_cyclone_dx**](BomApi.md#export_project_as_cyclone_dx) | **GET** /v1/bom/cyclonedx/project/{uuid} | Returns dependency metadata for a project in CycloneDX format
[**is_token_being_processed**](BomApi.md#is_token_being_processed) | **GET** /v1/bom/token/{uuid} | Determines if there are any tasks associated with the token that are being processed, or in the queue to be processed.
[**upload_bom**](BomApi.md#upload_bom) | **POST** /v1/bom | Upload a supported bill of material format document
[**upload_bom_base64_encoded**](BomApi.md#upload_bom_base64_encoded) | **PUT** /v1/bom | Upload a supported bill of material format document

# **export_component_as_cyclone_dx**
> str export_component_as_cyclone_dx(uuid, format=format)

Returns dependency metadata for a specific component in CycloneDX format

<p>Requires permission <strong>VIEW_PORTFOLIO</strong></p>

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
api_instance = swagger_client.BomApi(swagger_client.ApiClient(configuration))
uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | The UUID of the component to export
format = 'format_example' # str | The format to output (defaults to JSON) (optional)

try:
    # Returns dependency metadata for a specific component in CycloneDX format
    api_response = api_instance.export_component_as_cyclone_dx(uuid, format=format)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling BomApi->export_component_as_cyclone_dx: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uuid** | [**str**](.md)| The UUID of the component to export | 
 **format** | **str**| The format to output (defaults to JSON) | [optional] 

### Return type

**str**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.cyclonedx+xml, application/vnd.cyclonedx+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **export_project_as_cyclone_dx**
> str export_project_as_cyclone_dx(uuid, format=format, variant=variant, download=download)

Returns dependency metadata for a project in CycloneDX format

<p>Requires permission <strong>VIEW_PORTFOLIO</strong></p>

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
api_instance = swagger_client.BomApi(swagger_client.ApiClient(configuration))
uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | The UUID of the project to export
format = 'format_example' # str | The format to output (defaults to JSON) (optional)
variant = 'variant_example' # str | Specifies the CycloneDX variant to export. Value options are 'inventory' and 'withVulnerabilities'. (defaults to 'inventory') (optional)
download = true # bool | Force the resulting BOM to be downloaded as a file (defaults to 'false') (optional)

try:
    # Returns dependency metadata for a project in CycloneDX format
    api_response = api_instance.export_project_as_cyclone_dx(uuid, format=format, variant=variant, download=download)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling BomApi->export_project_as_cyclone_dx: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uuid** | [**str**](.md)| The UUID of the project to export | 
 **format** | **str**| The format to output (defaults to JSON) | [optional] 
 **variant** | **str**| Specifies the CycloneDX variant to export. Value options are &#x27;inventory&#x27; and &#x27;withVulnerabilities&#x27;. (defaults to &#x27;inventory&#x27;) | [optional] 
 **download** | **bool**| Force the resulting BOM to be downloaded as a file (defaults to &#x27;false&#x27;) | [optional] 

### Return type

**str**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.cyclonedx+xml, application/vnd.cyclonedx+json, application/octet-stream

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **is_token_being_processed**
> IsTokenBeingProcessedResponse is_token_being_processed(uuid)

Determines if there are any tasks associated with the token that are being processed, or in the queue to be processed.

<p>   This endpoint is intended to be used in conjunction with uploading a supported BOM document.   Upon upload, a token will be returned. The token can then be queried using this endpoint to   determine if any tasks (such as vulnerability analysis) is being performed on the BOM:   <ul>     <li>A value of <code>true</code> indicates processing is occurring.</li>     <li>A value of <code>false</code> indicates that no processing is occurring for the specified token.</li>   </ul>   However, a value of <code>false</code> also does not confirm the token is valid,   only that no processing is associated with the specified token. </p> <p>Requires permission <strong>BOM_UPLOAD</strong></p> <p><strong>Deprecated</strong>. Use <code>/v1/event/token/{uuid}</code> instead.</p>

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
api_instance = swagger_client.BomApi(swagger_client.ApiClient(configuration))
uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | The UUID of the token to query

try:
    # Determines if there are any tasks associated with the token that are being processed, or in the queue to be processed.
    api_response = api_instance.is_token_being_processed(uuid)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling BomApi->is_token_being_processed: %s\n" % e)
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

# **upload_bom**
> BomUploadResponse upload_bom(project=project, auto_create=auto_create, project_name=project_name, project_version=project_version, project_tags=project_tags, parent_name=parent_name, parent_version=parent_version, parent_uuid=parent_uuid, is_latest=is_latest, bom=bom)

Upload a supported bill of material format document

<p>    Expects CycloneDX and a valid project UUID. If a UUID is not specified,    then the <code>projectName</code> and <code>projectVersion</code> must be specified.    Optionally, if <code>autoCreate</code> is specified and <code>true</code> and the project does not exist,    the project will be created. In this scenario, the principal making the request will    additionally need the <strong>PORTFOLIO_MANAGEMENT</strong> or    <strong>PROJECT_CREATION_UPLOAD</strong> permission.  </p>  <p>    The BOM will be validated against the CycloneDX schema. If schema validation fails,    a response with problem details in RFC 9457 format will be returned. In this case,    the response's content type will be <code>application/problem+json</code>.  </p>  <p>Requires permission <strong>BOM_UPLOAD</strong></p>

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
api_instance = swagger_client.BomApi(swagger_client.ApiClient(configuration))
project = 'project_example' # str |  (optional)
auto_create = true # bool |  (optional)
project_name = 'project_name_example' # str |  (optional)
project_version = 'project_version_example' # str |  (optional)
project_tags = 'project_tags_example' # str |  (optional)
parent_name = 'parent_name_example' # str |  (optional)
parent_version = 'parent_version_example' # str |  (optional)
parent_uuid = 'parent_uuid_example' # str |  (optional)
is_latest = true # bool |  (optional)
bom = 'bom_example' # str |  (optional)

try:
    # Upload a supported bill of material format document
    api_response = api_instance.upload_bom(project=project, auto_create=auto_create, project_name=project_name, project_version=project_version, project_tags=project_tags, parent_name=parent_name, parent_version=parent_version, parent_uuid=parent_uuid, is_latest=is_latest, bom=bom)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling BomApi->upload_bom: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project** | **str**|  | [optional] 
 **auto_create** | **bool**|  | [optional] 
 **project_name** | **str**|  | [optional] 
 **project_version** | **str**|  | [optional] 
 **project_tags** | **str**|  | [optional] 
 **parent_name** | **str**|  | [optional] 
 **parent_version** | **str**|  | [optional] 
 **parent_uuid** | **str**|  | [optional] 
 **is_latest** | **bool**|  | [optional] 
 **bom** | **str**|  | [optional] 

### Return type

[**BomUploadResponse**](BomUploadResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **upload_bom_base64_encoded**
> BomUploadResponse upload_bom_base64_encoded(body)

Upload a supported bill of material format document

<p>   Expects CycloneDX and a valid project UUID. If a UUID is not specified,   then the <code>projectName</code> and <code>projectVersion</code> must be specified.   Optionally, if <code>autoCreate</code> is specified and <code>true</code> and the project does not exist,   the project will be created. In this scenario, the principal making the request will   additionally need the <strong>PORTFOLIO_MANAGEMENT</strong> or   <strong>PROJECT_CREATION_UPLOAD</strong> permission. </p> <p>   The BOM will be validated against the CycloneDX schema. If schema validation fails,   a response with problem details in RFC 9457 format will be returned. In this case,   the response's content type will be <code>application/problem+json</code>. </p> <p>   The maximum allowed length of the <code>bom</code> value is 20'000'000 characters.   When uploading large BOMs, the <code>POST</code> endpoint is preferred,   as it does not have this limit. </p> <p>Requires permission <strong>BOM_UPLOAD</strong></p>

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
api_instance = swagger_client.BomApi(swagger_client.ApiClient(configuration))
body = swagger_client.BomSubmitRequest() # BomSubmitRequest | 

try:
    # Upload a supported bill of material format document
    api_response = api_instance.upload_bom_base64_encoded(body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling BomApi->upload_bom_base64_encoded: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**BomSubmitRequest**](BomSubmitRequest.md)|  | 

### Return type

[**BomUploadResponse**](BomUploadResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

