# RuleCondition

A single condition that must be met for a rule to trigger auto-acceptance. Multiple conditions in a rule use AND logic.

## Example Usage

```typescript
import { RuleCondition } from "@paygentic/sdk/models";

let value: RuleCondition = {
  operator: "equals",
  type: "date",
  value: "<value>",
};
```

## Fields

| Field                                                      | Type                                                       | Required                                                   | Description                                                |
| ---------------------------------------------------------- | ---------------------------------------------------------- | ---------------------------------------------------------- | ---------------------------------------------------------- |
| `operator`                                                 | [models.Operator](../models/operator.md)                   | :heavy_check_mark:                                         | The comparison operator to use                             |
| `type`                                                     | [models.RuleConditionType](../models/ruleconditiontype.md) | :heavy_check_mark:                                         | The type of field to evaluate                              |
| `value`                                                    | *models.ValueUnion*                                        | :heavy_check_mark:                                         | The value to compare against                               |