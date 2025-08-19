# QR Code Redirect Setup for Fluidmaster Products

## Overview
This repository hosts the redirect logic for product QR codes. All QR codes point to the same `index.html` file, with a `?product=SKU` parameter. The script automatically redirects users to the correct YouTube or product page based on the SKU.

## Example
  - https://yourdomain.github.io/?product=(PRODUCT-SKU)
  - Example: https://fluidmaster-inc.github.io/QR_Code_Master/?product=400A
  - Link for the QR code: https://fluidmaster-inc.github.io/QR_Code_Master/?product=XXXX

## Files
- `index.html` – Main redirect page. Reads the `product` parameter, looks up the URL in `products.json`, and redirects the user. Also includes automatic YouTube conversion and fallback logic.
- `products.json` – Contains product SKUs and their destination URLs. Example:
```json
{
  "400A": "https://www.youtube.com/watch?v=dQw4w9WgXcQ",
  "500A": "https://www.youtube.com/watch?v=abc123xyz",
  "600A": "https://www.fluidmaster.com/some-product-page"
}
