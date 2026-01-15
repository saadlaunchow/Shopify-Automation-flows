# Step 5 – Shopify Product Creation

## Purpose
This step creates a new product in Shopify using the SEO-optimized data
generated in Step 4.

Only core product fields are created here.
Advanced data (metafields, variants, pricing logic) is handled in later steps.

---

## Input
SEO-optimized JSON output from Step 4.

---

## Shopify Node Used
Shopify → Product → Create

---

## Required Shopify Credentials
- Store Subdomain
- Admin API Access Token
- API Key / Secret (from Shopify Admin)

Credentials must be configured once and reused.

---

## Fields Mapped to Shopify

| Shopify Field | Source |
|-------------|-------|
| Title | `seo_title` |
| Body HTML | `seo_description` |
| Vendor | `vendor` |
| Product Type | `product_type` |
| Tags | `seo_tags` |
| Status | Active |

---

## Images Handling
- Images are added using public image URLs
- Each image URL is mapped individually
- Image upload happens during product creation

---

## Output of This Step
- Shopify Product ID
- Product Handle
- Product Admin URL

The Product ID is required for:
- Metafields creation
- Variants & pricing updates
- Inventory configuration

---

## Notes
- Shopify native node is used for reliability
- Metafields are NOT created here due to node limitations
- Product ID is passed to the next HTTP-based steps
