---
title: "simulationAutomation resource type"
description: "Represents simulation automation created to run on a tenant."
author: "Gopal-MSFT"
ms.localizationpriority: medium
ms.prod: "security"
doc_type: resourcePageType
---

# simulationAutomation resource type

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Represents simulation automation created to run on a tenant.


## Methods
|Method|Return type|Description|
|:---|:---|:---|
|[List simulationAutomations](../api/attacksimulationroot-list-simulationautomations.md)|[simulationAutomation](../resources/simulationautomation.md) collection|Get a list of the [simulationAutomation](../resources/simulationautomation.md) objects and their properties.|
|[List runs](../api/simulationautomation-list-runs.md)|[simulationAutomationRun](../resources/simulationautomationrun.md) collection|Get a list of the attack simulation automation runs for a tenant.|

## Properties
|Property|Type|Description|
|:---|:---|:---|
|createdBy|[emailIdentity](../resources/emailidentity.md)|Identity of the user who created the attack simulation automation.|
|createdDateTime|DateTimeOffset|Date and time when the attack simulation automation was created.|
|description|String|Description of the attack simulation automation.|
|displayName|String|Display name of the attack simulation automation. Supports `$filter` and `$orderby`.|
|id|String|Unique identifier for the attack simulation automation.|
|lastModifiedBy|[emailIdentity](../resources/emailidentity.md)|Identity of the user who most recently modified the attack simulation automation.|
|lastModifiedDateTime|DateTimeOffset|Date and time when the attack simulation automation was most recently modified.|
|lastRunDateTime|DateTimeOffset|Date and time of the latest run of the attack simulation automation.|
|nextRunDateTime|DateTimeOffset|Date and time of the upcoming run of the attack simulation automation.|
|status|[simulationAutomationStatus](#simulationautomationstatus-values)|Status of the attack simulation automation. Supports `$filter` and `$orderby`. The possible values are: `unknown`, `draft`, `notRunning`, `running`, `completed`, `unknownFutureValue`.|

### simulationAutomationStatus values

|Member|Description |
|:---|:---|
|unknown| The status of the simulation automation is not defined. |
|draft| The simulation automation is in draft mode. |
|notRunning| The simulation automation is not running. |
|running| The simulation automation is running. |
|completed| The simulation automation has completed. |
|unknownFutureValue| Evolvable enumeration sentinel value. Do not use. |

## Relationships
|Relationship|Type|Description|
|:---|:---|:---|
|runs|[simulationAutomationRun](../resources/simulationautomationrun.md) collection|A collection of simulation automation runs. |

## JSON representation
The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.simulationAutomation",
  "baseType": "microsoft.graph.entity",
  "openType": false
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.simulationAutomation",
  "createdBy": {
    "@odata.type": "microsoft.graph.emailIdentity"
  },
  "createdDateTime": "String (timestamp)",
  "description": "String",
  "displayName": "String",
  "id": "String (identifier)",
  "lastModifiedBy": {
    "@odata.type": "microsoft.graph.emailIdentity"
  },
  "lastModifiedDateTime": "String (timestamp)",
  "lastRunDateTime": "String (timestamp)",
  "nextRunDateTime": "String (timestamp)",
  "status": "String"
}
```
