# RevenueSummaryResponseRevenueRange

Where the caller's revenue actually lies in time. Scoped by the same filters as the request (merchant, and where given customer, subscription and currency), so it is not an account-wide statement. Present only when the selected range returned nothing. An object carries the bounds of the real revenue; null means no revenue under these filters at any time; an absent field means the extent was not resolved, because the result was not empty or because the lookup failed. An absent field must never be read as an absence. The bounds may span more than this endpoint's maximum queryable range, so clamp before re-querying.

## Example Usage

```typescript
import { RevenueSummaryResponseRevenueRange } from "@paygentic/sdk/models";

let value: RevenueSummaryResponseRevenueRange = {
  from: new Date("2025-06-20T07:07:51.501Z"),
  to: new Date("2026-07-22T16:46:16.811Z"),
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `from`                                                                                        | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | Earliest invoice issue instant.                                                               |
| `to`                                                                                          | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | Latest invoice issue instant.                                                                 |