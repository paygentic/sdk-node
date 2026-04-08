# CreateBillableMetricAggregation

Aggregation calculation method for metric values.

## Example Usage

```typescript
import { CreateBillableMetricAggregation } from "@paygentic/sdk/models/operations";

let value: CreateBillableMetricAggregation = "LATEST";
```

## Values

```typescript
"SUM" | "COUNT" | "AVG" | "MIN" | "MAX" | "UNIQUE_COUNT" | "LATEST"
```