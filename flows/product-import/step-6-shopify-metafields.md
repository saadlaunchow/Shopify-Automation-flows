# Step 6 – Shopify Metafields Creation (HTTP API)

## Purpose
This step creates Shopify metafields that cannot be added using the native
Shopify product creation node.

Metafields are attached AFTER the product is created, using the Product ID.

---

## Input
- Shopify Product ID from Step 5
- SEO-optimized data from Step 4
- Structured product data from Step 3

---

## Method Used
HTTP Request (POST)

---

## Shopify API Endpoint

POST
/admin/api/2023-10/products/{PRODUCT_ID}/metafields.json

`{PRODUCT_ID}` is dynamically mapped from Step 5 output.

---

## Authentication
- Header Authentication
- X-Shopify-Access-Token

---

## Headers

```json
{
  "Content-Type": "application/json",
  "X-Shopify-Access-Token": "YOUR_ACCESS_TOKEN"
}
```
 ## Example Metafield Payload (SEO Title)
 ```json
{
  "metafield": {
    "namespace": "seo",
    "key": "title",
    "type": "single_line_text_field",
    "value": "{{ $json.seo_title }}"
  }
}
