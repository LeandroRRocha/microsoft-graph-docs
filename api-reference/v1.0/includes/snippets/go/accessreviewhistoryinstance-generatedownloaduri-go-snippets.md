---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)

accessReviewHistoryDefinitionId := "accessReviewHistoryDefinition-id"
accessReviewHistoryInstanceId := "accessReviewHistoryInstance-id"
result, err := graphClient.IdentityGovernance().AccessReviews().HistoryDefinitionsById(&accessReviewHistoryDefinitionId).InstancesById(&accessReviewHistoryInstanceId).GenerateDownloadUri(accessReviewHistoryDefinition-id, accessReviewHistoryInstance-id).Post()


```