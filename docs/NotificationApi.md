# swagger_client.NotificationApi

All URIs are relative to */api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**add_project_to_rule**](NotificationApi.md#add_project_to_rule) | **POST** /v1/notification/rule/{ruleUuid}/project/{projectUuid} | Adds a project to a notification rule
[**add_team_to_rule**](NotificationApi.md#add_team_to_rule) | **POST** /v1/notification/rule/{ruleUuid}/team/{teamUuid} | Adds a team to a notification rule
[**create_notification_publisher**](NotificationApi.md#create_notification_publisher) | **PUT** /v1/notification/publisher | Creates a new notification publisher
[**create_notification_rule**](NotificationApi.md#create_notification_rule) | **PUT** /v1/notification/rule | Creates a new notification rule
[**create_scheduled_notification_rule**](NotificationApi.md#create_scheduled_notification_rule) | **PUT** /v1/notification/rule/scheduled | Creates a new scheduled notification rule
[**delete_notification_publisher**](NotificationApi.md#delete_notification_publisher) | **DELETE** /v1/notification/publisher/{notificationPublisherUuid} | Deletes a notification publisher and all related notification rules
[**delete_notification_rule**](NotificationApi.md#delete_notification_rule) | **DELETE** /v1/notification/rule | Deletes a notification rule
[**get_all_notification_publishers**](NotificationApi.md#get_all_notification_publishers) | **GET** /v1/notification/publisher | Returns a list of all notification publishers
[**get_all_notification_rules**](NotificationApi.md#get_all_notification_rules) | **GET** /v1/notification/rule | Returns a list of all notification rules
[**remove_project_from_rule**](NotificationApi.md#remove_project_from_rule) | **DELETE** /v1/notification/rule/{ruleUuid}/project/{projectUuid} | Removes a project from a notification rule
[**remove_team_from_rule**](NotificationApi.md#remove_team_from_rule) | **DELETE** /v1/notification/rule/{ruleUuid}/team/{teamUuid} | Removes a team from a notification rule
[**restore_default_templates**](NotificationApi.md#restore_default_templates) | **POST** /v1/notification/publisher/restoreDefaultTemplates | Restore the default notification publisher templates using the ones in the solution classpath
[**test_notification_rule**](NotificationApi.md#test_notification_rule) | **POST** /v1/notification/publisher/test/{uuid} | Dispatches a rule notification test
[**test_smtp_publisher_config**](NotificationApi.md#test_smtp_publisher_config) | **POST** /v1/notification/publisher/test/smtp | Dispatches a SMTP notification test
[**update_notification_publisher**](NotificationApi.md#update_notification_publisher) | **POST** /v1/notification/publisher | Updates a notification publisher
[**update_notification_rule**](NotificationApi.md#update_notification_rule) | **POST** /v1/notification/rule | Updates a notification rule

# **add_project_to_rule**
> NotificationRule add_project_to_rule(rule_uuid, project_uuid)

Adds a project to a notification rule

<p>Requires permission <strong>SYSTEM_CONFIGURATION</strong></p>

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
api_instance = swagger_client.NotificationApi(swagger_client.ApiClient(configuration))
rule_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | The UUID of the rule to add a project to
project_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | The UUID of the project to add to the rule

try:
    # Adds a project to a notification rule
    api_response = api_instance.add_project_to_rule(rule_uuid, project_uuid)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling NotificationApi->add_project_to_rule: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **rule_uuid** | [**str**](.md)| The UUID of the rule to add a project to | 
 **project_uuid** | [**str**](.md)| The UUID of the project to add to the rule | 

### Return type

[**NotificationRule**](NotificationRule.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **add_team_to_rule**
> NotificationRule add_team_to_rule(rule_uuid, team_uuid)

Adds a team to a notification rule

<p>Requires permission <strong>SYSTEM_CONFIGURATION</strong></p>

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
api_instance = swagger_client.NotificationApi(swagger_client.ApiClient(configuration))
rule_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | The UUID of the rule to add a team to
team_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | The UUID of the team to add to the rule

try:
    # Adds a team to a notification rule
    api_response = api_instance.add_team_to_rule(rule_uuid, team_uuid)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling NotificationApi->add_team_to_rule: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **rule_uuid** | [**str**](.md)| The UUID of the rule to add a team to | 
 **team_uuid** | [**str**](.md)| The UUID of the team to add to the rule | 

### Return type

[**NotificationRule**](NotificationRule.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_notification_publisher**
> NotificationPublisher create_notification_publisher(body=body)

Creates a new notification publisher

<p>Requires permission <strong>SYSTEM_CONFIGURATION</strong></p>

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
api_instance = swagger_client.NotificationApi(swagger_client.ApiClient(configuration))
body = swagger_client.NotificationPublisher() # NotificationPublisher |  (optional)

try:
    # Creates a new notification publisher
    api_response = api_instance.create_notification_publisher(body=body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling NotificationApi->create_notification_publisher: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**NotificationPublisher**](NotificationPublisher.md)|  | [optional] 

### Return type

[**NotificationPublisher**](NotificationPublisher.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_notification_rule**
> NotificationRule create_notification_rule(body=body)

Creates a new notification rule

<p>Requires permission <strong>SYSTEM_CONFIGURATION</strong></p>

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
api_instance = swagger_client.NotificationApi(swagger_client.ApiClient(configuration))
body = swagger_client.NotificationRule() # NotificationRule |  (optional)

try:
    # Creates a new notification rule
    api_response = api_instance.create_notification_rule(body=body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling NotificationApi->create_notification_rule: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**NotificationRule**](NotificationRule.md)|  | [optional] 

### Return type

[**NotificationRule**](NotificationRule.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_scheduled_notification_rule**
> NotificationRule create_scheduled_notification_rule(body=body)

Creates a new scheduled notification rule

<p>Requires permission <strong>SYSTEM_CONFIGURATION</strong></p>

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
api_instance = swagger_client.NotificationApi(swagger_client.ApiClient(configuration))
body = swagger_client.CreateScheduledNotificationRuleRequest() # CreateScheduledNotificationRuleRequest |  (optional)

try:
    # Creates a new scheduled notification rule
    api_response = api_instance.create_scheduled_notification_rule(body=body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling NotificationApi->create_scheduled_notification_rule: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**CreateScheduledNotificationRuleRequest**](CreateScheduledNotificationRuleRequest.md)|  | [optional] 

### Return type

[**NotificationRule**](NotificationRule.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_notification_publisher**
> delete_notification_publisher(notification_publisher_uuid)

Deletes a notification publisher and all related notification rules

<p>Requires permission <strong>SYSTEM_CONFIGURATION</strong></p>

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
api_instance = swagger_client.NotificationApi(swagger_client.ApiClient(configuration))
notification_publisher_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | The UUID of the notification publisher to delete

try:
    # Deletes a notification publisher and all related notification rules
    api_instance.delete_notification_publisher(notification_publisher_uuid)
except ApiException as e:
    print("Exception when calling NotificationApi->delete_notification_publisher: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **notification_publisher_uuid** | [**str**](.md)| The UUID of the notification publisher to delete | 

### Return type

void (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_notification_rule**
> delete_notification_rule(body=body)

Deletes a notification rule

<p>Requires permission <strong>SYSTEM_CONFIGURATION</strong></p>

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
api_instance = swagger_client.NotificationApi(swagger_client.ApiClient(configuration))
body = swagger_client.NotificationRule() # NotificationRule |  (optional)

try:
    # Deletes a notification rule
    api_instance.delete_notification_rule(body=body)
except ApiException as e:
    print("Exception when calling NotificationApi->delete_notification_rule: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**NotificationRule**](NotificationRule.md)|  | [optional] 

### Return type

void (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_all_notification_publishers**
> list[NotificationPublisher] get_all_notification_publishers()

Returns a list of all notification publishers

<p>Requires permission <strong>SYSTEM_CONFIGURATION</strong></p>

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
api_instance = swagger_client.NotificationApi(swagger_client.ApiClient(configuration))

try:
    # Returns a list of all notification publishers
    api_response = api_instance.get_all_notification_publishers()
    pprint(api_response)
except ApiException as e:
    print("Exception when calling NotificationApi->get_all_notification_publishers: %s\n" % e)
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**list[NotificationPublisher]**](NotificationPublisher.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_all_notification_rules**
> list[NotificationRule] get_all_notification_rules(page_number=page_number, page_size=page_size, offset=offset, limit=limit, sort_name=sort_name, sort_order=sort_order, trigger_type=trigger_type)

Returns a list of all notification rules

<p>Requires permission <strong>SYSTEM_CONFIGURATION</strong></p>

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
api_instance = swagger_client.NotificationApi(swagger_client.ApiClient(configuration))
page_number = '1' # str | The page to return. To be used in conjunction with <code>pageSize</code>. (optional) (default to 1)
page_size = '100' # str | Number of elements to return per page. To be used in conjunction with <code>pageNumber</code>. (optional) (default to 100)
offset = 'offset_example' # str | Offset to start returning elements from. To be used in conjunction with <code>limit</code>. (optional)
limit = 'limit_example' # str | Number of elements to return per page. To be used in conjunction with <code>offset</code>. (optional)
sort_name = 'sort_name_example' # str | Name of the resource field to sort on. (optional)
sort_order = 'sort_order_example' # str | Ordering of items when sorting with <code>sortName</code>. (optional)
trigger_type = 'trigger_type_example' # str | The notification trigger type to filter on (optional)

try:
    # Returns a list of all notification rules
    api_response = api_instance.get_all_notification_rules(page_number=page_number, page_size=page_size, offset=offset, limit=limit, sort_name=sort_name, sort_order=sort_order, trigger_type=trigger_type)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling NotificationApi->get_all_notification_rules: %s\n" % e)
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
 **trigger_type** | **str**| The notification trigger type to filter on | [optional] 

### Return type

[**list[NotificationRule]**](NotificationRule.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **remove_project_from_rule**
> NotificationRule remove_project_from_rule(rule_uuid, project_uuid)

Removes a project from a notification rule

<p>Requires permission <strong>SYSTEM_CONFIGURATION</strong></p>

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
api_instance = swagger_client.NotificationApi(swagger_client.ApiClient(configuration))
rule_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | The UUID of the rule to remove the project from
project_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | The UUID of the project to remove from the rule

try:
    # Removes a project from a notification rule
    api_response = api_instance.remove_project_from_rule(rule_uuid, project_uuid)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling NotificationApi->remove_project_from_rule: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **rule_uuid** | [**str**](.md)| The UUID of the rule to remove the project from | 
 **project_uuid** | [**str**](.md)| The UUID of the project to remove from the rule | 

### Return type

[**NotificationRule**](NotificationRule.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **remove_team_from_rule**
> NotificationRule remove_team_from_rule(rule_uuid, team_uuid)

Removes a team from a notification rule

<p>Requires permission <strong>SYSTEM_CONFIGURATION</strong></p>

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
api_instance = swagger_client.NotificationApi(swagger_client.ApiClient(configuration))
rule_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | The UUID of the rule to remove the project from
team_uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | The UUID of the project to remove from the rule

try:
    # Removes a team from a notification rule
    api_response = api_instance.remove_team_from_rule(rule_uuid, team_uuid)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling NotificationApi->remove_team_from_rule: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **rule_uuid** | [**str**](.md)| The UUID of the rule to remove the project from | 
 **team_uuid** | [**str**](.md)| The UUID of the project to remove from the rule | 

### Return type

[**NotificationRule**](NotificationRule.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **restore_default_templates**
> restore_default_templates()

Restore the default notification publisher templates using the ones in the solution classpath

<p>Requires permission <strong>SYSTEM_CONFIGURATION</strong></p>

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
api_instance = swagger_client.NotificationApi(swagger_client.ApiClient(configuration))

try:
    # Restore the default notification publisher templates using the ones in the solution classpath
    api_instance.restore_default_templates()
except ApiException as e:
    print("Exception when calling NotificationApi->restore_default_templates: %s\n" % e)
```

### Parameters
This endpoint does not need any parameter.

### Return type

void (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **test_notification_rule**
> test_notification_rule(uuid)

Dispatches a rule notification test

<p>Requires permission <strong>SYSTEM_CONFIGURATION</strong></p>

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
api_instance = swagger_client.NotificationApi(swagger_client.ApiClient(configuration))
uuid = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # str | The UUID of the rule to test

try:
    # Dispatches a rule notification test
    api_instance.test_notification_rule(uuid)
except ApiException as e:
    print("Exception when calling NotificationApi->test_notification_rule: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uuid** | [**str**](.md)| The UUID of the rule to test | 

### Return type

void (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **test_smtp_publisher_config**
> test_smtp_publisher_config(destination=destination)

Dispatches a SMTP notification test

<p>Requires permission <strong>SYSTEM_CONFIGURATION</strong></p>

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
api_instance = swagger_client.NotificationApi(swagger_client.ApiClient(configuration))
destination = 'destination_example' # str |  (optional)

try:
    # Dispatches a SMTP notification test
    api_instance.test_smtp_publisher_config(destination=destination)
except ApiException as e:
    print("Exception when calling NotificationApi->test_smtp_publisher_config: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **destination** | **str**|  | [optional] 

### Return type

void (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_notification_publisher**
> NotificationPublisher update_notification_publisher(body=body)

Updates a notification publisher

<p>Requires permission <strong>SYSTEM_CONFIGURATION</strong></p>

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
api_instance = swagger_client.NotificationApi(swagger_client.ApiClient(configuration))
body = swagger_client.NotificationPublisher() # NotificationPublisher |  (optional)

try:
    # Updates a notification publisher
    api_response = api_instance.update_notification_publisher(body=body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling NotificationApi->update_notification_publisher: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**NotificationPublisher**](NotificationPublisher.md)|  | [optional] 

### Return type

[**NotificationPublisher**](NotificationPublisher.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_notification_rule**
> NotificationRule update_notification_rule(body=body)

Updates a notification rule

<p>Requires permission <strong>SYSTEM_CONFIGURATION</strong></p>

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
api_instance = swagger_client.NotificationApi(swagger_client.ApiClient(configuration))
body = swagger_client.NotificationRule() # NotificationRule |  (optional)

try:
    # Updates a notification rule
    api_response = api_instance.update_notification_rule(body=body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling NotificationApi->update_notification_rule: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**NotificationRule**](NotificationRule.md)|  | [optional] 

### Return type

[**NotificationRule**](NotificationRule.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

