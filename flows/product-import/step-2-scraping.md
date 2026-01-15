# Step 2 – Product Page Scraping (HTTP Request)

## Purpose
Fetch raw product data from the official product website using the product URL provided in Google Sheets.

---

## Node Type
HTTP Request

---

## HTTP Configuration

- Method: GET
- URL: Mapped from `product_url`
- Authentication: None
- Response Format: Text (HTML)

---

## Why Raw HTML?
- Preserves full product context
- Includes descriptions, specifications, features, images
- Allows AI to extract accurate structured data
- Reduces hallucinations

---

## Error Handling
- Retry on temporary failures
- Fail execution if page is unreachable

---

## Output of This Step
- Raw HTML content of the product page
- Passed directly to AI data organization step
