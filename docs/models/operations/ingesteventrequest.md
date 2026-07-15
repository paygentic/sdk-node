# IngestEventRequest


## Supported Types

### `operations.IngestEventRequestBody1`

```typescript
const value: operations.IngestEventRequestBody1 = {
  type: "ai.inference",
  source: "https://api.myapp.com",
  subject: "cus_abc123",
  data: {
    "tokens": 1500,
    "model": "gpt-4o",
  },
};
```

### `operations.IngestEventRequestBody2`

```typescript
const value: operations.IngestEventRequestBody2 = {
  type: "ai.inference",
  source: "https://api.myapp.com",
  subject: "cus_abc123",
  externalSubject: "<value>",
  data: {
    "tokens": 1500,
    "model": "gpt-4o",
  },
};
```

