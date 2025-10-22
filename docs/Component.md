# Component

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**authors** | [**list[OrganizationalContact]**](OrganizationalContact.md) |  | [optional] 
**publisher** | **str** |  | [optional] 
**supplier** | [**OrganizationalEntity**](OrganizationalEntity.md) |  | [optional] 
**group** | **str** |  | [optional] 
**name** | **str** |  | [optional] 
**version** | **str** |  | [optional] 
**classifier** | **str** |  | 
**filename** | **str** |  | [optional] 
**extension** | **str** |  | [optional] 
**md5** | **str** |  | [optional] 
**sha1** | **str** |  | [optional] 
**sha256** | **str** |  | [optional] 
**sha384** | **str** |  | [optional] 
**sha512** | **str** |  | [optional] 
**sha3_256** | **str** |  | [optional] 
**sha3_384** | **str** |  | [optional] 
**sha3_512** | **str** |  | [optional] 
**blake2b_256** | **str** |  | [optional] 
**blake2b_384** | **str** |  | [optional] 
**blake2b_512** | **str** |  | [optional] 
**blake3** | **str** |  | [optional] 
**cpe** | **str** |  | [optional] 
**purl** | **str** |  | [optional] 
**purl_coordinates** | **str** |  | [optional] 
**swid_tag_id** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**copyright** | **str** |  | [optional] 
**license** | **str** |  | [optional] 
**license_expression** | **str** |  | [optional] 
**license_url** | **str** |  | [optional] 
**resolved_license** | [**License**](License.md) |  | [optional] 
**direct_dependencies** | **str** |  | [optional] 
**external_references** | [**list[ExternalReference]**](ExternalReference.md) |  | [optional] 
**parent** | [**Component**](Component.md) |  | [optional] 
**children** | [**list[Component]**](Component.md) |  | [optional] 
**properties** | [**list[ComponentProperty]**](ComponentProperty.md) |  | [optional] 
**vulnerabilities** | [**list[Vulnerability]**](Vulnerability.md) |  | [optional] 
**project** | [**Project**](Project.md) |  | 
**last_inherited_risk_score** | **float** |  | [optional] 
**notes** | **str** |  | [optional] 
**uuid** | **str** |  | 
**author** | **str** |  | [optional] 
**metrics** | [**DependencyMetrics**](DependencyMetrics.md) |  | [optional] 
**repository_meta** | [**RepositoryMetaComponent**](RepositoryMetaComponent.md) |  | [optional] 
**dependency_graph** | **list[str]** |  | [optional] 
**expand_dependency_graph** | **bool** |  | [optional] 
**is_internal** | **bool** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

