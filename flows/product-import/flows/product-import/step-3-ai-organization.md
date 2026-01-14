# Step 3 – AI Data Organization

## Input
- Raw HTML content from Step 2 (HTTP Request)

---

## Output
- Strict JSON only (no additional text, explanations, or formatting)

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
- Extract ONLY factual product information from the provided HTML
- Output ONLY valid JSON
- Follow the JSON schema exactly
- Do NOT add explanations, notes, or formatting
- Do NOT guess or hallucinate information
- If data is missing, return empty strings, arrays, or objects
- Use ONLY the provided HTML as the data source


---

## User Prompt
Extract product data from the HTML below and return ONLY valid JSON
using the defined schema.

HTML CONTENT:
{{$json["body"]}}

---


### **STEP 4 – AI SEO OPTIMIZATION**
(turn raw data into sales copy)

Say:
> **“Next: Step 4 SEO”**

And we continue — strong and clean 💪
