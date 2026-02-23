# EntitlementTemplateMetered

## Example Usage

```typescript
import { EntitlementTemplateMetered } from "@paygentic/sdk/models";

let value: EntitlementTemplateMetered = {
  type: "metered",
  usagePeriod: {
    interval: "<value>",
  },
};
```

## Fields

| Field                                                        | Type                                                         | Required                                                     | Description                                                  |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| `type`                                                       | *"metered"*                                                  | :heavy_check_mark:                                           | N/A                                                          |
| `usagePeriod`                                                | [models.UsagePeriod](../models/usageperiod.md)               | :heavy_check_mark:                                           | N/A                                                          |
| `isSoftLimit`                                                | *boolean*                                                    | :heavy_minus_sign:                                           | When true, access is granted even when balance is exhausted. |
| `issueAfterReset`                                            | *number*                                                     | :heavy_minus_sign:                                           | Amount of grants to issue after each period reset.           |
| `issueAfterResetPriority`                                    | *number*                                                     | :heavy_minus_sign:                                           | Priority for grants issued after reset.                      |
| `preserveOverageAtReset`                                     | *boolean*                                                    | :heavy_minus_sign:                                           | When true, overage from the previous period carries over.    |
| `resetMaxRollover`                                           | *number*                                                     | :heavy_minus_sign:                                           | Maximum amount of unused balance that rolls over on reset.   |
| `resetMinRollover`                                           | *number*                                                     | :heavy_minus_sign:                                           | Minimum amount of balance guaranteed to roll over on reset.  |