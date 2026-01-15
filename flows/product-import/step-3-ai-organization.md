# Step 3 – AI Data Organization (Strict JSON)

## Purpose
Convert raw HTML from the product page into structured, Shopify-ready data.

This step ONLY extracts factual information. No SEO or rewriting happens here.

---

## Input
- Raw HTML from Step 2 (HTTP Request)

---

## Output
- Valid JSON only
- No extra text or explanations

---

## JSON Schema

```json
{
  "product_title": "",
  "product_description_raw": "",
  "vendor": "",
  "product_type": "",
  "tags": [],
  "images": [],
  "price": "",
  "currency": "",
  "features": [],
  "specifications": {}
}
```
---
## System Prompt
You are a strict product data extraction engine.

Rules:
- Output ONLY valid JSON
- Follow the schema exactly
- Do NOT guess or hallucinate
- Do NOT add explanations
- Use empty values if data is missing
- Use ONLY the provided HTML as the data source

---

## User Prompt
Extract product data from the HTML below and return ONLY valid JSON
using the provided schema.

HTML:
{{$json["body"]}}

