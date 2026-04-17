<!-- Start SDK Example Usage [usage] -->
### Create a customer

Create a customer for each organization you bill. This is the first step in the billing setup — see the [Quickstart](https://docs.paygentic.io/getting-started/quickstart) for the full flow.

```typescript
import { Paygentic } from "@paygentic/sdk";

const paygentic = new Paygentic({
  bearerAuth: process.env["PAYGENTIC_BEARER_AUTH"] ?? "",
});

async function run() {
  const result = await paygentic.customers.create({
    consumer: {
      name: "Jane Smith",
      email: "jane@example.com",
      address: {
        city: "San Francisco",
        state: "CA",
        country: "US",
      },
    },
    merchantId: "org_YS8jkP59V71TdUvj",
  });

  console.log(result);
}

run();

```

### Create a subscription

Subscribe a customer to a plan. If the plan includes in-advance charges, Paygentic generates an initial invoice and the subscription activates once paid.

```typescript
import { Paygentic } from "@paygentic/sdk";

const paygentic = new Paygentic({
  bearerAuth: process.env["PAYGENTIC_BEARER_AUTH"] ?? "",
});

async function run() {
  const result = await paygentic.subscriptions.create({
    customerId: "cus_abc123",
    name: "Monthly API Service",
    planId: "plan_abc123",
    startedAt: new Date("2024-01-15T00:00:00Z"),
  });

  console.log(result);
}

run();

```

### Report usage

Send meter events to record consumption once a subscription is active. The endpoint is fire-and-forget — it always returns `202 Accepted`.

```typescript
import { Paygentic } from "@paygentic/sdk";

const paygentic = new Paygentic({
  bearerAuth: process.env["PAYGENTIC_BEARER_AUTH"] ?? "",
});

async function run() {
  const result = await paygentic.events.ingest({
    type: "ai.inference",
    source: "https://api.myapp.com",
    subject: "cus_abc123",
    data: {
      "tokens": 1500,
      "model": "gpt-4o",
    },
  });

  console.log(result);
}

run();

```
<!-- End SDK Example Usage [usage] -->