# SourceRule

An auto-acceptance rule that automatically approves source events matching specified conditions. Rules help automate the approval process for trusted customers or specific transaction patterns.

## Example Usage

```typescript
import { SourceRule } from "@paygentic/sdk/models";

let value: SourceRule = {
  id: "<id>",
  conditions: [],
  createdAt: new Date("2024-10-03T20:30:49.400Z"),
  description:
    "that pull testify surprisingly unless without blah probable massive whoever",
  enabled: false,
  evaluationCount: 582094,
  matchCount: 781511,
  name: "<value>",
  order: 876468,
  sourceId: "<id>",
  updatedAt: new Date("2026-05-31T10:10:00.165Z"),
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `id`                                                                                          | *string*                                                                                      | :heavy_check_mark:                                                                            | Unique identifier for the rule                                                                |
| `conditions`                                                                                  | [models.RuleCondition](../models/rulecondition.md)[]                                          | :heavy_check_mark:                                                                            | List of conditions that must ALL be met (AND logic)                                           |
| `createdAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | When the rule was created                                                                     |
| `createdBy`                                                                                   | *string*                                                                                      | :heavy_minus_sign:                                                                            | User ID who created the rule                                                                  |
| `description`                                                                                 | *string*                                                                                      | :heavy_check_mark:                                                                            | Detailed description of what this source rule does                                            |
| `enabled`                                                                                     | *boolean*                                                                                     | :heavy_check_mark:                                                                            | Whether this rule is currently active                                                         |
| `evaluationCount`                                                                             | *number*                                                                                      | :heavy_check_mark:                                                                            | Total number of times this rule has been evaluated                                            |
| `lastEvaluatedAt`                                                                             | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_minus_sign:                                                                            | Last time this rule was evaluated against an invoice                                          |
| `matchCount`                                                                                  | *number*                                                                                      | :heavy_check_mark:                                                                            | Number of times this rule has matched and auto-accepted an invoice                            |
| `name`                                                                                        | *string*                                                                                      | :heavy_check_mark:                                                                            | Human-readable name for the source rule                                                       |
| `order`                                                                                       | *number*                                                                                      | :heavy_check_mark:                                                                            | Priority order for rule evaluation (lower numbers are evaluated first)                        |
| `sourceId`                                                                                    | *string*                                                                                      | :heavy_check_mark:                                                                            | ID of the source this rule belongs to                                                         |
| `updatedAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | When the rule was last updated                                                                |