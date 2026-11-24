# SnapKit — Zero-Storage Document & Web Micro-Tools

A fast, privacy-first toolkit of 4 standalone web micro-tools built for everyday document, spreadsheet, screenshot, and invoicing workflows. **No signup walls, no monthly subscriptions, and zero server-side file retention** — every file is processed in ephemeral RAM and discarded immediately.

## Tools in the Suite

| Tool | Live URL | What it does | Free Tier |
| :--- | :--- | :--- | :--- |
| **TableSnap** | https://tablesnap.wan-3.dev/ | Extract tables from digital PDFs (bank statements, invoices, reports) into styled Excel (`.xlsx`), UTF-8 CSV, Markdown, or JSON with automatic multi-page merging. | Up to 30 pages / PDF, unlimited exports |
| **DiffSnap** | https://diffsnap.wan-3.dev/ | Side-by-side comparison for Excel (`.xlsx`), CSV, PDF, JSON, and text with smart SKU/ID key-column matching and color-coded Excel diff exports. | Up to 5,000 rows or 50 PDF pages |
| **WebSnap** | https://websnap.wan-3.dev/ | Headless Chromium website screenshot & HTML-to-PDF renderer supporting 1440px desktop, 390px iPhone mobile, 1200×630 OG cards, dark mode, and full Noto CJK fonts. | Full-page PNG, JPEG, and A4 PDF with zero watermarks |
| **InvoiceSnap** | https://invoicesnap.wan-3.dev/ | Real-time vector PDF invoice, quote, estimate, and receipt generator supporting 9 currencies (USD, EUR, GBP, JPY, CNY, CAD, AUD, CHF, SGD), VAT/discounts, and local browser drafts. | Unlimited live previews & Minimal Slate vector PDFs |

---

## Quick API & Automation Examples

### 1. Render a Webpage or HTML Template to A4 PDF via WebSnap API

```bash
curl -X POST https://websnap.wan-3.dev/api/render \
  -H "Content-Type: application/json" \
  -d '{"mode":"url","url":"https://example.com","format":"pdf","paper_format":"A4"}' \
  --output page.pdf
```

For 2× Retina HiDPI screenshots or higher rate limits, include your one-time Pro Key in the `X-Pro-Key` header.

### 2. Batch CSV → ZIP Invoicing (InvoiceSnap)

Upload a standard CSV with client billing rows to generate up to 50 branded vector PDF invoices packaged into a single ZIP archive:

```csv
invoice_number,client_name,client_details,currency,item_description,quantity,rate,tax_rate
INV-2026-201,Acme SaaS Inc.,ap@acme.example,USD,Monthly Retainer,1,1500,0
INV-2026-202,Tokyo Studio KK,billing@tokyo.example,JPY,UI Design Sprint,10,12000,10
```

---

## Architecture & Privacy Principles

- **Zero Server Storage**: Uploaded PDFs, spreadsheets, and invoice drafts are processed purely in RAM and discarded immediately after streaming the response.
- **Pay-Once Pro Packs ($9)**: No recurring monthly subscription traps; optional one-time packs unlock large-file / batch / Retina API quotas with credits that never expire.
- **Full Bilingual & CJK Typography**: Native English/Chinese UI and bundled Noto CJK fonts for crisp international documents.

---

## Useful Direct Links

- PDF Bank Statement to CSV: https://tablesnap.wan-3.dev/bank-statement-pdf-to-csv
- Compare Two Excel Files Online: https://diffsnap.wan-3.dev/compare-two-excel-files
- HTML to PDF & Full-Page Screenshot: https://websnap.wan-3.dev/html-to-pdf
- Free Online Vector Invoice Generator: https://invoicesnap.wan-3.dev/free-invoice-generator

Contact: hello@wan-3.dev
