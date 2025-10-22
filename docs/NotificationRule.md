# NotificationRule

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | 
**enabled** | **bool** |  | [optional] 
**notify_children** | **bool** |  | [optional] 
**log_successful_publish** | **bool** |  | [optional] 
**scope** | **str** |  | 
**notification_level** | **str** |  | [optional] 
**projects** | [**list[Project]**](Project.md) |  | [optional] 
**tags** | [**list[Tag]**](Tag.md) |  | [optional] 
**teams** | [**list[Team]**](Team.md) |  | [optional] 
**notify_on** | **list[str]** |  | [optional] 
**message** | **str** |  | [optional] 
**publisher** | [**NotificationPublisher**](NotificationPublisher.md) |  | [optional] 
**publisher_config** | **str** |  | [optional] 
**trigger_type** | **str** |  | 
**schedule_last_triggered_at** | **int** | When the schedule last triggered, as UNIX epoch timestamp in milliseconds | [optional] 
**schedule_next_trigger_at** | **int** | When the schedule triggers next, as UNIX epoch timestamp in milliseconds | [optional] 
**schedule_cron** | **str** | Schedule of this rule as cron expression. Must not be set for rules with trigger type EVENT. | [optional] 
**schedule_skip_unchanged** | **bool** | Whether to skip emitting a scheduled notification if it doesn&#x27;t contain any changes since its last emission. Must not be set for rules with trigger type EVENT. | [optional] 
**uuid** | **str** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

