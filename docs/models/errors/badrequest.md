# BadRequest

Bad Request - The request could not be understood or was missing required parameters


## Supported Types

### `errors.ErrorT`

```typescript
const value: errors.ErrorT = {
  error: "not_found",
  message: "The requested resource was not found",
};
```

### `errors.ValidationError`

```typescript
const value: errors.ValidationError = {
  message: "Validation failed",
  errors: [
    {
      field: "email",
      message: "Invalid email format",
      code: "invalid_format",
    },
  ],
};
```

