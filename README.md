# DiabData Registry

Open reference data for diabetes-related medical devices and medications, used by the [DiabData Android app](https://github.com/DiabdataApp/diab-data-android).

This registry contains GTIN/CIP barcode mappings that allow the app to identify scanned devices and treatments without requiring an app update when new products are added.

## Data

| File | Description |
|---|---|
| `medical_devices.csv` | Insulin pumps, CGM sensors, transmitters and other devices |
| `medication_data.csv` | Insulins, glucagon and other diabetes-related medications |

## How it works

When a user scans a DataMatrix barcode in the DiabData app:
1. The app checks its local database first
2. If not found, it queries the DiabData API
3. The result is cached locally for future scans

This registry is the source of truth behind that API. Any merge to `main` automatically triggers a redeployment of the API with the updated data.

## Contributing

Found a missing device or medication? Contributions are welcome!

Please read [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines on how to add new entries.

## License

This data is released under the [CC0 1.0 Universal](LICENSE) license — public domain, no restrictions.