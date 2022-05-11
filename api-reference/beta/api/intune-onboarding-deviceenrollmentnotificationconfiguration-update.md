---
title: "Update deviceEnrollmentNotificationConfiguration"
description: "Update the properties of a deviceEnrollmentNotificationConfiguration object."
author: "dougeby"
localization_priority: Normal
ms.prod: "intune"
doc_type: apiPageType
---

# Update deviceEnrollmentNotificationConfiguration

Namespace: microsoft.graph

> **Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.

> **Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.

Update the properties of a [deviceEnrollmentNotificationConfiguration](../resources/intune-onboarding-deviceenrollmentnotificationconfiguration.md) object.

## Prerequisites
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type|Permissions (from least to most privileged)|
|:---|:---|
|Delegated (work or school account)|DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementConfiguration.ReadWrite.All|
|Delegated (personal Microsoft account)|Not supported.|
|Application|DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementConfiguration.ReadWrite.All|

## HTTP Request
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceEnrollmentConfigurations/{deviceEnrollmentConfigurationId}
```

## Request headers
|Header|Value|
|:---|:---|
|Authorization|Bearer &lt;token&gt; Required.|
|Accept|application/json|

## Request body
In the request body, supply a JSON representation for the [deviceEnrollmentNotificationConfiguration](../resources/intune-onboarding-deviceenrollmentnotificationconfiguration.md) object.

The following table shows the properties that are required when you create the [deviceEnrollmentNotificationConfiguration](../resources/intune-onboarding-deviceenrollmentnotificationconfiguration.md).

|Property|Type|Description|
|:---|:---|:---|
|id|String|Unique Identifier for the account Inherited from [deviceEnrollmentConfiguration](../resources/intune-shared-deviceenrollmentconfiguration.md)|
|displayName|String|The display name of the device enrollment configuration Inherited from [deviceEnrollmentConfiguration](../resources/intune-shared-deviceenrollmentconfiguration.md)|
|description|String|The description of the device enrollment configuration Inherited from [deviceEnrollmentConfiguration](../resources/intune-shared-deviceenrollmentconfiguration.md)|
|priority|Int32|Priority is used when a user exists in multiple groups that are assigned enrollment configuration. Users are subject only to the configuration with the lowest priority value. Inherited from [deviceEnrollmentConfiguration](../resources/intune-shared-deviceenrollmentconfiguration.md)|
|createdDateTime|DateTimeOffset|Created date time in UTC of the device enrollment configuration Inherited from [deviceEnrollmentConfiguration](../resources/intune-shared-deviceenrollmentconfiguration.md)|
|lastModifiedDateTime|DateTimeOffset|Last modified date time in UTC of the device enrollment configuration Inherited from [deviceEnrollmentConfiguration](../resources/intune-shared-deviceenrollmentconfiguration.md)|
|version|Int32|The version of the device enrollment configuration Inherited from [deviceEnrollmentConfiguration](../resources/intune-shared-deviceenrollmentconfiguration.md)|
|roleScopeTagIds|String collection|Optional role scope tags for the enrollment restrictions. Inherited from [deviceEnrollmentConfiguration](../resources/intune-shared-deviceenrollmentconfiguration.md)|
|deviceEnrollmentConfigurationType|[deviceEnrollmentConfigurationType](../resources/intune-onboarding-deviceenrollmentconfigurationtype.md)|Support for Enrollment Configuration Type Inherited from [deviceEnrollmentConfiguration](../resources/intune-shared-deviceenrollmentconfiguration.md). Possible values are: `unknown`, `limit`, `platformRestrictions`, `windowsHelloForBusiness`, `defaultLimit`, `defaultPlatformRestrictions`, `defaultWindowsHelloForBusiness`, `defaultWindows10EnrollmentCompletionPageConfiguration`, `windows10EnrollmentCompletionPageConfiguration`, `deviceComanagementAuthorityConfiguration`, `singlePlatformRestriction`, `unknownFutureValue`, `enrollmentNotificationsConfiguration`.|
|platformType|[enrollmentRestrictionPlatformType](../resources/intune-onboarding-enrollmentrestrictionplatformtype.md)|Platform type of the Enrollment Notification. Possible values are: `allPlatforms`, `ios`, `windows`, `windowsPhone`, `android`, `androidForWork`, `mac`.|
|templateType|[enrollmentNotificationTemplateType](../resources/intune-onboarding-enrollmentnotificationtemplatetype.md)|Template type of the Enrollment Notification. Possible values are: `email`, `push`, `unknownFutureValue`.|
|notificationMessageTemplateId|Guid|Notification Message Template Id|
|brandingOptions|[enrollmentNotificationBrandingOptions](../resources/intune-onboarding-enrollmentnotificationbrandingoptions.md)|Branding Options for the Enrollment Notification. Possible values are: `none`, `includeCompanyLogo`, `includeCompanyName`, `includeContactInformation`, `includeCompanyPortalLink`, `includeDeviceDetails`.|
|defaultLocale|String|DefaultLocale for the Enrollment Notification|



## Response
If successful, this method returns a `200 OK` response code and an updated [deviceEnrollmentNotificationConfiguration](../resources/intune-onboarding-deviceenrollmentnotificationconfiguration.md) object in the response body.

## Example

### Request
Here is an example of the request.
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceEnrollmentConfigurations/{deviceEnrollmentConfigurationId}
Content-type: application/json
Content-length: 525

{
  "@odata.type": "#microsoft.graph.deviceEnrollmentNotificationConfiguration",
  "displayName": "Display Name value",
  "description": "Description value",
  "priority": 8,
  "version": 7,
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "deviceEnrollmentConfigurationType": "limit",
  "platformType": "ios",
  "templateType": "push",
  "notificationMessageTemplateId": "eba3ed57-ed57-eba3-57ed-a3eb57eda3eb",
  "brandingOptions": "includeCompanyLogo",
  "defaultLocale": "Default Locale value"
}
```

### Response
Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 697

{
  "@odata.type": "#microsoft.graph.deviceEnrollmentNotificationConfiguration",
  "id": "bdd0743a-743a-bdd0-3a74-d0bd3a74d0bd",
  "displayName": "Display Name value",
  "description": "Description value",
  "priority": 8,
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "version": 7,
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "deviceEnrollmentConfigurationType": "limit",
  "platformType": "ios",
  "templateType": "push",
  "notificationMessageTemplateId": "eba3ed57-ed57-eba3-57ed-a3eb57eda3eb",
  "brandingOptions": "includeCompanyLogo",
  "defaultLocale": "Default Locale value"
}
```



