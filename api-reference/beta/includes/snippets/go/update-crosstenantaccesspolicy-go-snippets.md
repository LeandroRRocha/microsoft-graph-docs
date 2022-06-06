---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)

requestBody := msgraphsdk.NewCrossTenantAccessPolicy()
requestBody.SetAdditionalData(map[string]interface{}{
	"allowedCloudEndpoints":  []String {
		"microsoftonline.us",
		"partner.microsoftonline.cn",
	}
}
graphClient.Policies().CrossTenantAccessPolicy().Patch(requestBody)


```