---
description: "Automatically generated file. DO NOT MODIFY"
---

```powershell

Import-Module Microsoft.Graph.Users.Actions

$params = @{
	AddLicenses = @(
		@{
			DisabledPlans = @(
				"8a256a2b-b617-496d-b51b-e76466e88db0"
			)
			SkuId = "84a661c4-e949-4bd2-a560-ed7766fcaf2b"
		}
		@{
			DisabledPlans = @(
			)
			SkuId = "f30db892-07e9-47e9-837c-80727f46fd3d"
		}
	)
	RemoveLicenses = @(
	)
}

# A UPN can also be used as -UserId.
Set-MgUserLicense -UserId $userId -BodyParameter $params

```