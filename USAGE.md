<!-- Start SDK Example Usage [usage] -->
```typescript
import { Paygentic } from "@paygentic/sdk";

const paygentic = new Paygentic({
  bearerAuth: process.env["PAYGENTIC_BEARER_AUTH"] ?? "",
});

async function run() {
  const result = await paygentic.billableMetrics.createBillableMetric({
    aggregation: "SUM",
    description: "other gracefully hold",
    merchantId: "<id>",
    name: "<value>",
    productId: "<id>",
    unit: "becquerel",
  });

  console.log(result);
}

run();

```
<!-- End SDK Example Usage [usage] -->