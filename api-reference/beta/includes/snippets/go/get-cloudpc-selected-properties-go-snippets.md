---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)

requestParameters := &msgraphsdk.CloudPCRequestBuilderGetQueryParameters{
	Select: "id,displayName,imageDisplayName,lastModifiedDateTime,lastRemoteActionResult,lastLoginResult",
}
options := &msgraphsdk.CloudPCRequestBuilderGetRequestConfiguration{
	QueryParameters: requestParameters,
}
cloudPCId := "cloudPC-id"
result, err := graphClient.DeviceManagement().VirtualEndpoint().CloudPCsById(&cloudPCId).GetWithRequestConfigurationAndResponseHandler(options, nil)


```