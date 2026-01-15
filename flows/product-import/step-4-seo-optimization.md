# Step 4 – AI SEO Optimization

## Purpose
This step uses AI to transform structured product data into SEO-optimized,
customer-ready content for Shopify.

This step focuses on:
- SEO-friendly product title
- Optimized product description
- Product tags and collections text

No factual extraction happens here — only rewriting and optimization.

---

## Input
Structured JSON output from Step 3 (AI Data Organization).

---

## Output
Strict JSON only containing SEO-optimized fields.

---

## JSON Schema

```json
{
  "seo_title": "",
  "seo_description": "",
  "seo_tags": [],
  "product_type": "",
  "vendor": ""
}
```
---
## System Prompt
You are an expert Shopify SEO copywriter.

Your task:
- Optimize product content for search engines and conversions
- Use ONLY the provided structured product data
- Do NOT invent features or specifications
- Do NOT change factual information
- Write clear, persuasive, and SEO-friendly content
- Output ONLY valid JSON following the provided schema
---
## User Prompt
Using the structured product data below, generate SEO-optimized Shopify content.

Rules:
- Keep titles concise and keyword-focused
- Write clear, benefit-driven descriptions
- Generate relevant SEO tags
- Do NOT add information not present in the input data

Structured Product Data:
{{$json}}

