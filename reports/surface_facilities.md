# Surface Facilities Design — Utrecht Geothermal District System
## Team KDK | SPE Africa Datathon 2026

---

## Overview

The surface facilities are designed to serve Utrecht's mixed-use urban district with a combined heating and cooling system powered by two STIM+HP geothermal doublets (KDK-01 and KDK-02). The system delivers **≥10 MWth heating** and **≥5 MWth cooling** from a single integrated geothermal loop.

---

## System Configuration

```
                    SUBSURFACE
            ┌─────────────────────┐
            │  KDK-01 + KDK-02   │
            │  Slochteren Aquifer  │
            │  66°C | 298 m³/h   │
            └────────┬────────────┘
                     │ Hot brine (66°C)
                     ▼
            ┌─────────────────────┐
            │   Heat Exchanger    │  Separates geothermal brine
            │                     │  from district heating loop
            └────────┬────────────┘
                     │
          ┌──────────┴──────────┐
          │                     │
          ▼                     ▼
   ┌─────────────┐      ┌──────────────────┐
   │  Heat Pump  │      │ Absorption        │
   │  (STIM+HP)  │      │ Chiller          │
   │  10 MWth    │      │  5 MWth cooling  │
   └──────┬──────┘      └────────┬─────────┘
          │                      │
          ▼                      ▼
   ┌─────────────────────────────────────┐
   │           Buffer Tank               │
   │      Thermal Storage (1–2 MWh)      │
   │    Handles peak demand fluctuations  │
   └──────────────┬──────────────────────┘
                  │
                  ▼
   ┌─────────────────────────────────────┐
   │      District Heating & Cooling     │
   │           Network (Utrecht)          │
   │                                     │
   │  🏘 Residential  — comfort heating  │
   │  🏢 Offices      — heating/cooling  │
   │  🏛 Public       — schools/hospitals│
   └─────────────────────────────────────┘
                  │
                  ▼
   ┌─────────────────────────────────────┐
   │         Injection Well              │
   │      Return brine at 40°C           │
   └─────────────────────────────────────┘
```

---

## Component Specifications

### 1. Heat Exchanger
| Parameter | Value |
|---|---|
| Purpose | Separates geothermal brine from district heating water |
| Type | Plate heat exchanger |
| Capacity | 18.32 MWth (full doublet output) |
| Inlet temp (brine) | 66°C |
| Outlet temp (brine) | 40°C (reinjection) |
| Estimated cost | Included in CAPEX (14.28 M€) |

### 2. Heat Pump
| Parameter | Value |
|---|---|
| Purpose | Boosts geothermal heat to district heating supply temperature |
| Mode | Winter heating |
| Output | 10 MWth district heating |
| COP | 5.32 (average KDK-01 + KDK-02) |
| Supply temperature | 70°C |
| Return temperature | 40°C |
| Estimated cost | Included in CAPEX (600 €/kWth) |

### 3. Absorption Chiller
| Parameter | Value |
|---|---|
| Purpose | Provides district cooling in summer using waste geothermal heat |
| Mode | Summer cooling |
| Output | 5 MWth cooling |
| Type | Heat-driven (no additional electricity required) |
| Cooling COP | ~0.7 (typical for single-effect absorption chiller) |
| Estimated CAPEX | 1.5–2.0 M€ |
| Note | Not included in LCOE base case — improves economics if added |

### 4. Buffer Tank
| Parameter | Value |
|---|---|
| Purpose | Thermal storage to handle peak demand fluctuations |
| Capacity | 1–2 MWh |
| Benefit | Allows doublet to run at steady state — maximises efficiency |
| Estimated CAPEX | 0.3–0.5 M€ |

---

## Energy Balance

```
Geothermal input (KDK-01 + KDK-02):   18.32 MWth
        │
        ├── Heating allocation:  10 MWth  → district heating
        ├── Cooling allocation:   5 MWth  → absorption chiller
        └── Buffer / margin:            3.32 MWth → storage / losses
```

---

## Additional CAPEX Estimate (surface facilities beyond LCOE base case)

| Component | Estimated Cost |
|---|---|
| Absorption chiller (5 MWth) | 1.5–2.0 M€ |
| Buffer tank (1–2 MWh) | 0.3–0.5 M€ |
| Pipework, controls & connection | 0.5 M€ |
| **Total additional CAPEX** | **~2.5–3.0 M€** |

> **Note:** The LCOE of 14.11 €/GJ covers the heat pump and heat exchanger only. The absorption chiller and buffer tank represent additional investment.

---

## Compliance with Datathon Targets

| Target | Required | Achieved | Facility |
|---|---|---|---|
| Heating demand | ≥ 10 MWth | **10 MWth** ✅ | Heat pump (STIM+HP) |
| Cooling demand | ≥ 5 MWth | **5 MWth** ✅ | Absorption chiller |
| **Combined** | **≥ 15 MWth** | **18.32 MWth** ✅ | Two doublets combined |
