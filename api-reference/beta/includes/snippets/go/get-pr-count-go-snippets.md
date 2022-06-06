---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)

requestParameters := &msgraphsdk.UserRequestBuilderGetQueryParameters{
	Count: true,
	Orderby: "displayName",
	Search: "%22displayName:Pr%22",
	Select: "displayName,id",
}
headers := map[string]string{
	"ConsistencyLevel": "eventual"
}
options := &msgraphsdk.UserRequestBuilderGetRequestConfiguration{
	QueryParameters: requestParameters,
	Headers: headers,
}
groupId := "group-id"
result, err := graphClient.GroupsById(&groupId).Members().User(group-id).GetWithRequestConfigurationAndResponseHandler(options, nil)


```