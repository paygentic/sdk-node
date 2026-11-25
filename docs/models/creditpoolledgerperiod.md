# CreditPoolLedgerPeriod

This bucket's calendar-aligned period (UTC). The first and last bucket in the response are clamped to the requested `from`/`to` rather than the full calendar period.

## Example Usage

```typescript
import { CreditPoolLedgerPeriod } from "@paygentic/sdk/models";

let value: CreditPoolLedgerPeriod = {
  from: new Date("2025-05-01T19:29:29.517Z"),
  to: new Date("2024-06-07T01:26:36.813Z"),
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `from`                                                                                        | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `to`                                                                                          | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |