## Multicurrency PayPal to _QuickBooks Online_ CSV Converter

This script helps import PayPal transactions in multiple currencies (CAD and USD for now) into Quick Books Online (QBO). Although QBO has a PayPal importer, it doesn't support multiple currencies so everything goes into one account.

QBO is also unable to import a CSV file which contains multiple currencies, so the CSV imported by PayPal must be split into separate CSVs, one for each currency. However, QBO is also unable to handle multiple splits in a CSV, so the PayPal Fee is lumped into the final transaction amount.

This script takes a PayPal "Balance Affecting" CSV export and splits it into USD and CAD CSV files. The PayPal Fee is separated from each transaction and a new transaction is created for it.

The QBO import CSV only has three fields (date, description, and amount), so three descriptive fields were taken from the PayPal CSV and put onto the QBO "description" field to make it easier to write "rules" to automate sorting once they're imported. It looks messy but makes automation easy and accurate.

You can use the [converter here](https://thx2112.github.io/pp2qbo/).

All processing is done in the browser for privacy and security.

### To use: 

1. Create "PayPal CAD" and "PayPal USD" accounts in QBO to match your PayPal currencies. Make sure to set the currency for each.
2. On PayPal create a "Balance Affecting" CSV for the date range you want to import.
3. Run it through this converter and save the output files.
4. On QBO go to Transactions->Banking then "Upload from File" from the "Link Account" drop-down.
5. Import each currency CSV to the appropriate PayPal account. You should be able to use the defaults for all settings.
6. After the CSVs are imported, create "Rules" to separate the transactions to the appropriate accounts.


