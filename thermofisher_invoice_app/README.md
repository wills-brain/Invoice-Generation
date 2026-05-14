# Simplex Sciences ThermoFisher Invoice Processing

For internal use by Simplex Sciences Operations team.

## Run on Mac

```bash
cd /Users/williamshiu/Downloads/thermofisher_invoice_app_final_delivery
chmod +x run_mac_linux.sh
./run_mac_linux.sh
```

Direct run:

```bash
cd /Users/williamshiu/Downloads/thermofisher_invoice_app_final_delivery
python3 -m pip install -r requirements.txt
python3 -m streamlit run app.py
```

OCR for scanned Thermo Fisher PDFs requires Tesseract:

```bash
brew install tesseract
```

## Workflow

1. The bundled Simplex invoice template (`simplex_invoice_template.docx`) is used by default. Tick **Use my own invoice template** in the sidebar only if you want to upload a different one.
2. Upload one or more Thermo Fisher/Fisher Scientific purchase order PDFs.
3. Invoice date and sales rep are entered once and apply to every uploaded PDF.
4. For each uploaded PDF, enter its own shipping date, internal order number (defaults to FS), shipping cost, and FedEx tracking number.
5. Review OCR fields and line items for each PDF.
6. Check the OCR review acknowledgement.
7. Download individual Word invoices or download all generated invoices as a ZIP.
