# TenantSnapshotDto

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**tenant** | [**TenantEntityDto**](TenantEntityDto.md) | The tenant entity itself. | [optional] 
**subjects** | [SubjectEntityDto] | All subjects (users/service accounts) belonging to this tenant. | [optional] 
**passkeyCredentials** | [PasskeyCredentialEntityDto] | All passkey credentials registered for this tenant&#39;s subjects. | [optional] 
**roles** | [TenantRoleEntityDto] | All tenant-scoped roles. | [optional] 
**members** | [TenantMemberEntityDto] | All tenant membership records linking subjects to the tenant. | [optional] 
**memberRoles** | [TenantMemberRoleEntityDto] | All role assignments for tenant members. | [optional] 
**oAuthClients** | [OAuthClientEntityDto] | All OAuth client registrations for this tenant. | [optional] 
**connectorConfigurations** | [ConnectorConfigSnapshotDto] | All connector configurations (with secrets decrypted) for this tenant. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


