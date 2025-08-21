# 📘 Noon Report & MRV/FOC Calculation Template

## 1. Overview
This Excel template is designed for ship operators to record daily **Noon Reports** and automatically calculate:
- Fuel Oil Consumption (**FOC**) per fuel type (HFO, MDO)
- Remaining On Board (**ROB**) consistency check
- CO₂ emissions according to **EU MRV emission factors**
- Key performance indicators (tCO₂/nm, optional cargo tonne-nm)

## 2. Sheets
### `Noon_Report`
- Date / Time
- Position (Lat / Long)
- Distance sailed (nm)
- Average speed (knots)
- Fuel consumption (HFO, MDO)
- ROB (HFO, MDO)
- Remarks (anchorage, course changes, weather, etc.)

### `Calcul`
- FOC/day per fuel type and total
- ROB check: `ROB_prev + Bunkered – Consumed = ROB_today`
- CO₂ emissions:
  - HFO × 3.114 tCO₂/ton fuel
  - MDO × 3.206 tCO₂/ton fuel
- Indicators:
  - tCO₂ / nm
  - tCO₂ / cargo tonne-nm (if cargo weight is reported)

## 3. Example Data (fictional)
- **2025-08-20** – 480 nm, HFO 28 mt, MDO 2 mt, ROB HFO 220 mt, ROB MDO 35 mt
- **2025-08-21** – 510 nm, HFO 30 mt, MDO 1.5 mt, ROB HFO 190 mt, ROB MDO 33.5 mt
- **2025-08-22** – 0 nm (anchorage), HFO 2 mt, MDO 0.5 mt, ROB HFO 188 mt, ROB MDO 33 mt

---

## 4. Usage
1. Fill in the `Noon_Report` sheet daily with actual vessel data.
2. Check the `Calcul` sheet for:
   - Fuel consumption per day
   - ROB consistency (highlighted if mismatch)
   - Estimated CO₂ emissions
3. Use the results for **MRV pre-calculations**, logbook support, and fuel efficiency monitoring.

---

## 5. Notes
- Emission factors are based on EU MRV Regulation (2015/757).
- For compliance, ensure data is verified and aligned with third-party verifiers (e.g., DNV, Verifavia, Lloyd’s).
