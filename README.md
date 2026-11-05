# Power Quality Assessment and Photovoltaic Sizing for a Plant Growth Chamber

## Overview
This repository contains high-resolution electrical measurement datasets collected during experimental campaigns conducted on a controlled-environment Plant Growth Chamber (PGC). The primary objective of these campaigns is to assess power quality characteristics, analyze energy consumption patterns under different operational scenarios, and enable accurate photovoltaic (PV) system sizing and integration.

The collected data encompasses internal environmental control components, air conditioning units, and direct solar PV generation metrics across multiple experimental runs.

---

## Repository Structure

```text
.
├── Experiment_1/
│   ├── chamber_loads.csv
│   ├── air_conditioning.csv
│   └── pv_system.csv
└── Experiment_2/
    ├── chamber_loads.csv
    ├── air_conditioning.csv
    └── pv_system.csv
```

---

## Dataset Description

The experimental datasets are organized by measurement campaigns (`Experiment_1` and `Experiment_2`) and divided into three primary CSV files per folder:

1. **`chamber_loads.csv`**: Captures electrical parameters corresponding to internal auxiliary loads (e.g., LED lighting arrays, ventilation fans, and electronic control circuits) monitored via PZEM-004T energy metering modules.
2. **`air_conditioning.csv`**: Contains electrical consumption and power quality metrics strictly dedicated to the HVAC (Heating, Ventilation, and Air Conditioning) thermal regulation unit, measured using PZEM-004T modules.
3. **`pv_system.csv`**: Records direct-current (DC) photovoltaic generation parameters, including operational voltage, current, and instantaneous power outputs.

---

## Variable Specifications

### Table 1: Electrical & Power Quality Parameters (`chamber_loads.csv` & `air_conditioning.csv`)

| Variable | Description | Unit | Data Type / Format |
| :--- | :--- | :---: | :---: |
| `Date` | Timestamp recording date | - | `YYYY-MM-DD` or |
| `Time` | Timestamp recording time | - | `HH:MM:SS` |
| `vRMS` | Root Mean Square AC Voltage | V | Float |
| `iRMS` | Root Mean Square AC Current | A | Float |
| `P` | Active Power | W | Float |
| `E` | Accumulated Active Energy | kWh | Float |
| `f` | Line Frequency | $\text{Hz}$ | Float |
| `fp` | Power Factor ($\cos\phi$) | Dimensionless | Float |
| `phi_rad` | Phase Angle in Radians | rad | Float |
| `phi_deg` | Phase Angle in Degrees | Degree | Float |
| `vm` | Measured Peak Voltage Amplitude | V | Float |
| `im` | Measured Peak Current Amplitude | A | Float |
| `S` | Apparent Power ($S = vRMS \times iRMS$) | VA | Float |
| `Q` | Reactive Power ($Q = \sqrt{S^2 - P^2}$) | VAR | Float |
| `P2` | Calculated Active Power (Validation metric) | W | Float |
| `E'` | Incremental Active Energy per sample interval | Wh | Float |

### Table 2: Photovoltaic Generation Parameters (`pv_system.csv`)

| Variable | Description | Unit | Data Type / Format |
| :--- | :--- | :---: | :---: |
| `Date` | Timestamp recording date | - | `DD-MM-YYYY` |
| `Time` | Timestamp recording time | - | `HH:MM:SS` |
| `vPV` | Photovoltaic Array DC Voltage | V | Float |
| `iPV` | Photovoltaic Array DC Current | A | Float |
| `pPV` | Photovoltaic Array Instantaneous Power | W | Float |

---

## Usage & License

The datasets provided in this repository are structured for straightforward processing in Python (`pandas`), R, or MATLAB. Feel free to use this data for research, power quality modeling, or energy optimization studies. Please reference this repository if used in academic publications.
