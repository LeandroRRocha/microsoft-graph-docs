---
title: "unifiedRoleEligibilityScheduleRequest: filterByCurrentUser"
description: "In PIM, retrieve the requests for role eligibilities for a particular principal. The principal can be the creator or approver of the unifiedRoleEligibilityScheduleRequest object, or they can be the target of the role eligibility."
author: "rkarim-ms"
ms.localizationpriority: medium
ms.prod: "governance"
doc_type: apiPageType
---

# unifiedRoleEligibilityScheduleRequest: filterByCurrentUser
Namespace: microsoft.graph

In PIM, retrieve the requests for role eligibilities for a particular principal. The principal can be the creator or approver of the **unifiedRoleEligibilityScheduleRequest** object, or they can be the target of the role eligibility.

> [!NOTE]
> This API doesn't return eligible role assignments through group memberships.

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type|Permissions (from least to most privileged)|
|:---|:---|
|Delegated (work or school account)|RoleEligibilitySchedule.Read.Directory, RoleManagement.Read.Directory, RoleManagement.Read.All, RoleEligibilitySchedule.ReadWrite.Directory, RoleManagement.ReadWrite.Directory	|
|Delegated (personal Microsoft account)|Not supported|
|Application|RoleManagement.Read.Directory, RoleManagement.Read.All, RoleManagement.ReadWrite.Directory |

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /roleManagement/directory/roleEligibilityScheduleRequests/filterByCurrentUser(on='parameterValue')
```

## Function parameters
In the request URL, provide the following query parameters with values.
The following table shows the parameters that can be used with this function.

|Parameter|Type|Description|
|:---|:---|:---|
|on|roleEligibilityScheduleRequestFilterByCurrentUserOptions|The possible values are `principal`, `createdBy`, `approver`, `unknownFutureValue`. Only `principal` and `approver` are currently supported.|

## Optional query parameters

This method supports the `$select`, `$filter`, and `$expand` OData query parameters to help customize the response. For general information, see [OData query parameters](/graph/query-parameters).

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|

## Request body
Do not supply a request body for this method.

## Response

If successful, this function returns a `200 OK` response code and a [unifiedRoleEligibilityScheduleRequest](../resources/unifiedroleeligibilityschedulerequest.md) collection in the response body.

## Examples

### Request

# [HTTP](#tab/http)
<!-- {
  "blockType": "request",
  "name": "unifiedroleeligibilityschedulerequestthis.filterbycurrentuser"
}
-->
``` http
GET https://graph.microsoft.com/v1.0/roleManagement/directory/roleEligibilityScheduleRequests/filterByCurrentUser(on='principal')
```
# [C#](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/unifiedroleeligibilityschedulerequestthisfilterbycurrentuser-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [JavaScript](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/unifiedroleeligibilityschedulerequestthisfilterbycurrentuser-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [Objective-C](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/unifiedroleeligibilityschedulerequestthisfilterbycurrentuser-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [Java](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/unifiedroleeligibilityschedulerequestthisfilterbycurrentuser-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [Go](#tab/go)
[!INCLUDE [sample-code](../includes/snippets/go/unifiedroleeligibilityschedulerequestthisfilterbycurrentuser-go-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---



### Response
>**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "Collection(microsoft.graph.unifiedRoleEligibilityScheduleRequest)"
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
    "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#Collection(unifiedRoleEligibilityScheduleRequest)",
    "value": [
        {
            "@odata.type": "#microsoft.graph.unifiedRoleEligibilityScheduleRequest",
            "id": "50877283-9d40-433c-bab8-7986dc10458a",
            "status": "Provisioned",
            "createdDateTime": "2022-04-12T09:05:41.807Z",
            "completedDateTime": "2022-04-12T09:05:41.853Z",
            "approvalId": null,
            "customData": null,
            "action": "adminAssign",
            "principalId": "071cc716-8147-4397-a5ba-b2105951cc0b",
            "roleDefinitionId": "8424c6f0-a189-499e-bbd0-26c1753c96d4",
            "directoryScopeId": "/",
            "appScopeId": null,
            "isValidationOnly": false,
            "targetScheduleId": "50877283-9d40-433c-bab8-7986dc10458a",
            "justification": "Assign Attribute Assignment Admin eligibility to restricted user",
            "createdBy": {
                "application": null,
                "device": null,
                "user": {
                    "displayName": null,
                    "id": "3fbd929d-8c56-4462-851e-0eb9a7b3a2a5"
                }
            },
            "scheduleInfo": {
                "startDateTime": "2022-04-12T09:05:41.8532931Z",
                "recurrence": null,
                "expiration": {
                    "type": "afterDateTime",
                    "endDateTime": "2024-04-10T00:00:00Z",
                    "duration": null
                }
            },
            "ticketInfo": {
                "ticketNumber": null,
                "ticketSystem": null
            }
        },
        {
            "@odata.type": "#microsoft.graph.unifiedRoleEligibilityScheduleRequest",
            "id": "f341269e-c926-41fa-a905-cef3b01b2a67",
            "status": "Revoked",
            "createdDateTime": "2022-04-12T09:12:18.187Z",
            "completedDateTime": null,
            "approvalId": null,
            "customData": null,
            "action": "adminRemove",
            "principalId": "071cc716-8147-4397-a5ba-b2105951cc0b",
            "roleDefinitionId": "8424c6f0-a189-499e-bbd0-26c1753c96d4",
            "directoryScopeId": "/",
            "appScopeId": null,
            "isValidationOnly": false,
            "targetScheduleId": null,
            "justification": null,
            "scheduleInfo": null,
            "createdBy": {
                "application": null,
                "device": null,
                "user": {
                    "displayName": null,
                    "id": "3fbd929d-8c56-4462-851e-0eb9a7b3a2a5"
                }
            },
            "ticketInfo": {
                "ticketNumber": null,
                "ticketSystem": null
            }
        }
    ]
}
```
