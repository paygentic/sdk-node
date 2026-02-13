# UpdateRuleRequest

## Example Usage

```typescript
import { UpdateRuleRequest } from "@paygentic/sdk/models";

let value: UpdateRuleRequest = {};
```

## Fields

| Field                                                                  | Type                                                                   | Required                                                               | Description                                                            |
| ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| `conditions`                                                           | [models.RuleCondition](../models/rulecondition.md)[]                   | :heavy_minus_sign:                                                     | List of conditions that must ALL be met (AND logic)                    |
| `description`                                                          | *string*                                                               | :heavy_minus_sign:                                                     | Detailed description of what this source rule does                     |
| `enabled`                                                              | *boolean*                                                              | :heavy_minus_sign:                                                     | Whether this rule should be active                                     |
| `name`                                                                 | *string*                                                               | :heavy_minus_sign:                                                     | Human-readable name for the source rule                                |
| `order`                                                                | *number*                                                               | :heavy_minus_sign:                                                     | Priority order for rule evaluation (lower numbers are evaluated first) |