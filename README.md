## Multicurrency PayPal to _QuickBooks Online_ CSV Converter

This script helps import PayPal transactions in multiple currencies (CAD and USD for now) into Quick Books Online (QBO). Although QBO has a PayPal importer, it doesn't support multiple currencies so everything goes into one account.

QBO is also unable to import a CSV file which contains multiple currencies, so the CSV imported by PayPal must be split into separate CSVs, one for each currency. However, QBO is also unable to handle multiple splits in a CSV, so the PayPal Fee is lumped into the final transaction amount.

This script takes a PayPal "Balance Affecting" CSV export and splits it into USD and CAD CSV files. The PayPal Fee is separated from each transaction and a new transaction is created for it.

You can use the [converter here](https://thx2112.github.io/pp2qbo/).

All processing is done in the browser for privacy and security.


