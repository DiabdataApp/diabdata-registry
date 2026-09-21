# Contributing to DiabData Registry

Thank you for helping improve the DiabData Registry! This guide explains how to add new medical devices or medications to the dataset.

## Before you start

- Check that the device or medication is **not already listed** in the relevant CSV file
- Make sure you have the **exact GTIN/CIP barcode** (14 digits, found on the product packaging)
- Contributions are reviewed by maintainers before being merged

## Adding a new medical device

Edit `medical_devices.csv` and add a new row with the following columns:

| Column | Description | Example |
|---|---|---|
| `CIP/GTIN` | 14-digit barcode from the DataMatrix | `00386270004901` |
| `MANUFACTURER` | Manufacturer name | `Dexcom` |
| `DEVICE_TYPE` | One of the types listed below | `CONTINUOUS_GLUCOSE_MONITORING_SYSTEM_SENSOR` |
| `FULL_NAME` | Full commercial name as printed on packaging | `Dexcom G7 Sensor` |
| `DAYS_LIFESPAN` | Lifespan in days (`0` if not applicable) | `10` |

**Available `DEVICE_TYPE` values:**

| Value | Description |
|---|---|
| `WIRELESS_PATCH` | Insulin pump pod/patch |
| `WIRELESS_PATCH_REMOTE` | Insulin pump with remote/PDM |
| `CONTINUOUS_GLUCOSE_MONITORING_SYSTEM_SENSOR` | CGM sensor |
| `CONTINUOUS_GLUCOSE_MONITORING_SYSTEM_TRANSMITTER` | CGM transmitter |

## Adding a new medication

Edit `medication_data.csv` and add a new row with the following columns:

| Column | Description | Example |
|---|---|---|
| `CIP/GTIN` | 14-digit barcode from the DataMatrix | `3400930083178` |
| `INSULIN` | Brand name | `Fiasp` |
| `TREATMENT_TYPE` | One of the types listed below | `FAST_ACTING_INSULIN_VIAL` |
| `FULL_NAME` | Full commercial name as printed on packaging | `Fiasp 100 U/mL – 10 mL` |

**Available `TREATMENT_TYPE` values:**

| Value | Description |
|---|---|
| `FAST_ACTING_INSULIN_VIAL` | Fast-acting insulin, vial |
| `FAST_ACTING_INSULIN_CARTRIDGE` | Fast-acting insulin, cartridge |
| `FAST_ACTING_INSULIN_SYRINGE` | Fast-acting insulin, pre-filled syringe |
| `SLOW_ACTING_INSULIN_VIAL` | Long-acting insulin, vial |
| `SLOW_ACTING_INSULIN_CARTRIDGE` | Long-acting insulin, cartridge |
| `SLOW_ACTING_INSULIN_SYRINGE` | Long-acting insulin, pre-filled syringe |
| `GLUCAGON_SYRINGE` | Glucagon, injectable |
| `GLUCAGON_SPRAY` | Glucagon, nasal spray |
| `B_KETONE_TEST_STRIP` | Blood ketone test strip |
| `BLOOD_GLUCOSE_TEST_STRIP` | Blood glucose test strip |

## Submitting your contribution

1. [Fork this repository](https://github.com/DiabdataApp/diabdata-registry/fork)
2. Edit the relevant CSV file
3. Open a Pull Request with a short description of what you added
4. A maintainer will review and merge your PR

## Questions?

Open an [issue](https://github.com/DiabdataApp/diabdata-registry/issues) if you're unsure about anything.