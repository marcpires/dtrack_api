# ServiceComponent

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**provider** | [**OrganizationalEntity**](OrganizationalEntity.md) |  | [optional] 
**group** | **str** |  | [optional] 
**name** | **str** |  | [optional] 
**version** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**endpoints** | **list[str]** |  | [optional] 
**authenticated** | **bool** |  | [optional] 
**crosses_trust_boundary** | **bool** |  | [optional] 
**data** | [**list[DataClassification]**](DataClassification.md) |  | [optional] 
**external_references** | [**list[ExternalReference]**](ExternalReference.md) |  | [optional] 
**parent** | [**ServiceComponent**](ServiceComponent.md) |  | [optional] 
**children** | [**list[ServiceComponent]**](ServiceComponent.md) |  | [optional] 
**vulnerabilities** | [**list[Vulnerability]**](Vulnerability.md) |  | [optional] 
**project** | [**Project**](Project.md) |  | 
**last_inherited_risk_score** | **float** |  | [optional] 
**notes** | **str** |  | [optional] 
**uuid** | **str** |  | 
**bom_ref** | **str** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

