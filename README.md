# ![LOGO](logo.png) ApiManagementClient **flow**ground Connector

## Description

A generated **flow**ground connector for the ApiManagementClient API (version 2016-10-10).

Generated from: https://api.apis.guru/v2/specs/azure.com/apimanagement-apimusers/2016-10-10/swagger.json<br/>
Generated at: 2019-06-11T18:13:17+03:00

## API Description

Use these REST APIs for performing operations on User entity in Azure API Management deployment. The User entity in API Management represents the developers that call the APIs of the products to which they are subscribed.

## Authorization

Supported authorization schemes:
- OAuth2

For OAuth 2.0 you need to specify OAuth Client credentials as environment variables in the connector repository:
* `OAUTH_CLIENT_ID` - your OAuth client id
* `OAUTH_CLIENT_SECRET` - your OAuth client secret

## Actions

### Lists a collection of registered users in the specified service instance.

*Tags:* `Users`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `$filter` - _optional_ - | Field            | Supported operators    | Supported functions               |
|------------------|------------------------|-----------------------------------|
| id               | ge, le, eq, ne, gt, lt | substringof, contains, startswith, endswith |
| firstName        | ge, le, eq, ne, gt, lt | substringof, contains, startswith, endswith |
| lastName         | ge, le, eq, ne, gt, lt | substringof, contains, startswith, endswith |
| email            | ge, le, eq, ne, gt, lt | substringof, contains, startswith, endswith |
| state            | eq                     | N/A                               |
| registrationDate | ge, le, eq, ne, gt, lt | N/A                               |
| note             | ge, le, eq, ne, gt, lt | substringof, contains, startswith, endswith |
* `$top` - _optional_ - Number of records to return.
* `$skip` - _optional_ - Number of records to skip.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Deletes specific user.

*Tags:* `Users`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `uid` - _required_ - User identifier. Must be unique in the current API Management service instance.
* `deleteSubscriptions` - _optional_ - Whether to delete user's subscription or not.
* `If-Match` - _required_ - The entity state (Etag) version of the user to delete. A value of "*" can be used for If-Match to unconditionally apply the operation.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Gets the details of the user specified by its identifier.

*Tags:* `Users`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `uid` - _required_ - User identifier. Must be unique in the current API Management service instance.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Updates the details of the user specified by its identifier.

*Tags:* `Users`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `uid` - _required_ - User identifier. Must be unique in the current API Management service instance.
* `If-Match` - _required_ - The entity state (Etag) version of the user to update. A value of "*" can be used for If-Match to unconditionally apply the operation.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Creates or Updates a user.

*Tags:* `Users`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `uid` - _required_ - User identifier. Must be unique in the current API Management service instance.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Retrieves a redirection URL containing an authentication token for signing a given user into the developer portal.

*Tags:* `Users`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `uid` - _required_ - User identifier. Must be unique in the current API Management service instance.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Lists all user groups.

*Tags:* `UserGroups`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `uid` - _required_ - User identifier. Must be unique in the current API Management service instance.
* `$filter` - _optional_ - | Field       | Supported operators    | Supported functions                         |
|-------------|------------------------|---------------------------------------------|
| id          | ge, le, eq, ne, gt, lt | substringof, contains, startswith, endswith |
| name        | ge, le, eq, ne, gt, lt | substringof, contains, startswith, endswith |
| description | ge, le, eq, ne, gt, lt | substringof, contains, startswith, endswith |
* `$top` - _optional_ - Number of records to return.
* `$skip` - _optional_ - Number of records to skip.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Lists all user identities.

*Tags:* `UserIdentities`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `uid` - _required_ - User identifier. Must be unique in the current API Management service instance.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Lists the collection of subscriptions of the specified user.

*Tags:* `UserSubscriptions`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `uid` - _required_ - User identifier. Must be unique in the current API Management service instance.
* `$filter` - _optional_ - | Field        | Supported operators    | Supported functions                         |
|--------------|------------------------|---------------------------------------------|
| id           | ge, le, eq, ne, gt, lt | substringof, contains, startswith, endswith |
| name         | ge, le, eq, ne, gt, lt | substringof, contains, startswith, endswith |
| stateComment | ge, le, eq, ne, gt, lt | substringof, contains, startswith, endswith |
| userId       | ge, le, eq, ne, gt, lt | substringof, contains, startswith, endswith |
| productId    | ge, le, eq, ne, gt, lt | substringof, contains, startswith, endswith |
| state        | eq                     |                                             |
* `$top` - _optional_ - Number of records to return.
* `$skip` - _optional_ - Number of records to skip.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Gets the Shared Access Authorization Token for the User.

*Tags:* `Users`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `uid` - _required_ - User identifier. Must be unique in the current API Management service instance.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

## License

**flow**ground :- Telekom iPaaS / azure-com-apimanagement-apimusers-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
