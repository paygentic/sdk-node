# GetEntitlementRequest

## Example Usage

```typescript
import { GetEntitlementRequest } from "@paygentic/sdk/models/operations";

let value: GetEntitlementRequest = {
  entitlementId: "<id>",
};
```

## Fields

| Field                                                                                                                                                                        | Type                                                                                                                                                                         | Required                                                                                                                                                                     | Description                                                                                                                                                                  |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `entitlementId`                                                                                                                                                              | *string*                                                                                                                                                                     | :heavy_check_mark:                                                                                                                                                           | The unique identifier of the entitlement.                                                                                                                                    |
| `at`                                                                                                                                                                         | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)                                                                                | :heavy_minus_sign:                                                                                                                                                           | Evaluate balance and access at this point in time (RFC 3339 datetime with any UTC offset, e.g. 2024-01-15T10:30:00Z or 2024-01-15T15:30:00+05:30). Defaults to current time. |