# Invoice Data Extraction Service

## Service Route
`/invoicedataextractor/invoicedataextraction`

## Description
The Invoice Data Extraction service allows an invoice document attached to a workflow to be exported from the process via a webhook. The integration service then sends the document to an MS Azure endpoint, which processes the invoice and extracts all listed business data. This data is then written back into the workflow's template variables prefixed with "invoice".

> 💡 **Synchronous Operation**: This integration service operates synchronously. It receives the export event from the workflow and returns the result, including updates to all `invoice` prefixed variable, within the same session. This ensures immediate availability of the data extracted from the document.

## Dedicated Template Variables
- **invoiceVendorName**
- **invoiceVendorAddress**
- **invoiceVendorAddressRecipient**
- **invoiceVendorTaxId**
- **invoiceCustomerName**
- **invoiceCustomerId**
- **invoiceCustomerTaxId**
- **invoiceCustomerAddress**
- **invoiceCustomerAddressRecipient**
- **invoiceInvoiceId**
- **invoiceInvoiceDate**
- **invoiceInvoiceTotal**
- **invoiceDueDate**
- **invoicePurchaseOrder**
- **invoiceBillingAddress**
- **invoiceBillingAddressRecipient**
- **invoiceShippingAddress**
- **invoiceShippingAddressRecipient**
- **invoiceSubTotal**
- **invoiceTotalTax**
- **invoiceAmountDue**
- **invoiceServiceStartDate**
- **invoiceServiceEndDate**
- **invoiceServiceAddress**
- **invoiceServiceAddressRecipient**
- **invoiceRemittanceAddress**
- **invoiceRemittanceAddressRecipient**
- **invoicePreviousUnpaidBalance**
- **invoiceCurrencyCode**

## Supported File Formats for Invoices
- **pdf**
- **jpeg**
- **jpg**
- **png**
- **bmp**
- **tiff**
- **heif**

For further information on the MS Azure service, please refer to the [Azure Invoice Field Extraction Documentation](https://learn.microsoft.com/en-us/azure/ai-services/document-intelligence/concept-invoice?view=doc-intel-4.0.0#field-extraction).

---

This service is part of the Itiner Workspace integrations and is designed to facilitate the extraction and processing of invoice data by leveraging MS Azure's document intelligence capabilities.
