# Barcode Generator

A single-page web app to generate, preview, and print barcodes for different product categories.

## Features
- **Format selector**: EAN-13 (default), UPC-A, Code 128, QR Code, GS1 DataMatrix, ISBN, ISSN, Pharmacode, GS1-128.
- **Type selector**: Loaded dynamically from an inline JSON block (`<script type="application/json" id="product-types">`). Easy to edit to add/remove categories like Retail, Book, Magazine, Pharmaceutical, Logistics, Coupon, Apparel, etc.
- **Color picker**: Choose barcode foreground color.
- **Remember option**: Save current settings to browser localStorage.
- **Batch generator**: Supports serial placeholders (`{n}`) with start and padding options.
- **A4 sheet printing**: Adds multiple barcodes to a 3×8 grid with dashed cut marks. One-click print support.

## Usage
1. Open `index.html` in a modern browser (no server needed).
2. Choose a **Type** and **Format**.
3. Enter your base code (numbers or text). Use `{n}` for auto-serials.
4. Set batch count, serial start, and padding (optional).
5. Click **Preview** to check, then **Add to Sheet** to stage barcodes.
6. **Print Sheet** generates an A4-ready layout with cut marks.

## Customizing
- Update **types and default format hints** by editing the JSON in the `<script id="product-types">` block.
- Adjust **sheet layout** (`cols` and `rows`) in the same JSON block for different page sizes.

## Tech
- [bwip-js](https://github.com/metafloor/bwip-js) renders barcodes into `<canvas>`.
- Pure HTML/CSS/JS. No backend required.

## Notes
- ISBN and ISSN codes are auto-expanded into EAN-13.
- Add-on fields support magazine 2- or 5-digit codes and GS1 Application Identifiers.
- For print accuracy, disable scaling in your browser’s print dialog.

---
