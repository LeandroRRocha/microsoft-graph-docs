---
description: "Automatically generated file. DO NOT MODIFY"
---

```go


import (
	  "context"
	  msgraphsdk "github.com/microsoftgraph/msgraph-sdk-go"
	  graphconfig "github.com/microsoftgraph/msgraph-sdk-go/admin"
	  //other-imports
)

graphClient := msgraphsdk.NewGraphServiceClientWithCredentials(cred, scopes)


requestParameters := &graphconfig.AdminServiceAnnouncementHealthOverviewsRequestBuilderGetQueryParameters{
	Expand: [] string {"issues"},
}
configuration := &graphconfig.AdminServiceAnnouncementHealthOverviewsRequestBuilderGetRequestConfiguration{
	QueryParameters: requestParameters,
}

result, err := graphClient.Admin().ServiceAnnouncement().HealthOverviews().Get(context.Background(), configuration)


```