# PdfSource

Who produced the document at pdfUrl, or null when there is none. `paygentic` means pdfUrl is this API's download endpoint and the request must carry your API key; `tax_provider` means it is the provider's own link, which opens directly in a browser.

## Example Usage

```typescript
import { PdfSource } from "@paygentic/sdk/models";

let value: PdfSource = "paygentic";
```

## Values

```typescript
"paygentic" | "tax_provider"
```