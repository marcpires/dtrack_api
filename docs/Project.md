# Project

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**authors** | [**list[OrganizationalContact]**](OrganizationalContact.md) |  | [optional] 
**publisher** | **str** |  | [optional] 
**manufacturer** | [**OrganizationalEntity**](OrganizationalEntity.md) |  | [optional] 
**supplier** | [**OrganizationalEntity**](OrganizationalEntity.md) |  | [optional] 
**group** | **str** |  | [optional] 
**name** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**version** | **str** |  | [optional] 
**classifier** | **str** |  | [optional] 
**collection_logic** | **str** |  | [optional] 
**collection_tag** | [**Tag**](Tag.md) |  | [optional] 
**cpe** | **str** |  | [optional] 
**purl** | **str** |  | [optional] 
**swid_tag_id** | **str** |  | [optional] 
**direct_dependencies** | **str** |  | [optional] 
**uuid** | **str** |  | 
**parent** | [**Project**](Project.md) |  | [optional] 
**children** | [**list[Project]**](Project.md) |  | [optional] 
**properties** | [**list[ProjectProperty]**](ProjectProperty.md) |  | [optional] 
**tags** | [**list[Tag]**](Tag.md) |  | [optional] 
**last_bom_import** | **int** | UNIX epoch timestamp in milliseconds | 
**last_bom_import_format** | **str** |  | [optional] 
**last_inherited_risk_score** | **float** |  | [optional] 
**last_vulnerability_analysis** | **int** | UNIX epoch timestamp in milliseconds | [optional] 
**active** | **bool** |  | [optional] 
**is_latest** | **bool** |  | [optional] 
**access_teams** | [**list[Team]**](Team.md) |  | [optional] 
**external_references** | [**list[ExternalReference]**](ExternalReference.md) |  | [optional] 
**metadata** | [**ProjectMetadata**](ProjectMetadata.md) |  | [optional] 
**versions** | [**list[ProjectVersion]**](ProjectVersion.md) |  | [optional] 
**author** | **str** |  | [optional] 
**metrics** | [**ProjectMetrics**](ProjectMetrics.md) |  | [optional] 
**bom_ref** | **str** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

