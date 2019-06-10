---
title: "credentialUsageSummary resource type"
description: "Provides the summary of self-service password reset usage for a given tenant."
localization_priority: Normal
author: "dkershaw"
ms.prod: "identity and access reports"
doc_type: "resourcePageType"
---

# credentialUsageSummary resource type

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Provides the summary of self-service password reset usage for a given tenant. This API provides the current state of how many users in your organization are using self-service password reset capabilities.

## Methods

| Method       | Return Type | Description |
|:-------------|:------------|:------------|
| [Get credentialUsageSummary](../api/reportroot-getcredentialusagesummary.md) | credentialUsageSummary | Read properties and relationships of a credentialUsageSummary object. |

## Properties

| Property     | Type        | Description |
|:-------------|:------------|:------------|
| authMethod | string | Possible values are: `email`, `mobileSMS`, `mobileCall`, `officePhone`, `securityQuestion` (Can only be used for self-service password reset.), `appNotification`, `appCode`, `alternateMobileCall`, `fido` (Can only be registered through combined security info registration.), `appPassword` (Can only be used for MFA.), `unknownFutureValue`. |
| failureActivityCount | Int64 | Provides the count of failed resets or registration data. |
| feature | string | Possible values are: `registration`, `reset`, `unknownFutureValue`. |
| id | String | Read-only. |
| successfulActivityCount | Int64 | Provides the count of successful registrations or resets. |

## Relationships

None.

## JSON representation

The following is a JSON representation of the resource.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.credentialUsageSummary",
  "baseType": "",
  "keyProperty": "id"
}-->

```json
{
  "id" : "d3590ed6-52b3-4102-aeff-aad2292ab01234",
  "feature":"registration",
  "successfulActivityCount":"12345",
  "failureActivityCount": "123",
  "authMethod": "email"
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "credentialUsageSummary resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->