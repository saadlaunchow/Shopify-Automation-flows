# Step 1 – Google Sheets Trigger

## Purpose
This step acts as the entry point for the Shopify product automation.
A new automation run starts when a product URL is added to Google Sheets.

---

## Trigger Type
**Google Sheets – Row Added**

---

## Google Sheet Structure

| Column Name | Description |
|------------|------------|
| product_url | Official product page URL (required) |

Only one column is required to keep the automation simple and fast.

---

## Trigger Conditions
- Automation triggers when:
  - A new row is added
  - `product_url` is not empty

---

## Why a Single Column?
- Faster setup
- No manual status handling
- Ideal for MVP, demos, and bulk imports
- Easy to extend later if needed

---

## Output of This Step
- Passes `product_url` to the HTTP scraping step
