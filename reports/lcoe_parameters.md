# LCOE Parameter Justifications — Team KDK
## SPE Africa Datathon 2026 | Utrecht Geothermal Project (STIM+HP, 2 Doublets)

---

## Subsurface Parameters

| Parameter | Value | Unit | Justification |
|---|---|---|---|
| Flow rate | 165.59 | L/s | Combined flow rate of two doublets (KDK-01: 296.9 m³/h + KDK-02: 299.2 m³/h = 596.1 m³/h ÷ 3.6 = 165.6 L/s), derived directly from ThermoGIS STIM+HP simulation results |
| Along hole depth | 1,300 | m | Depth to top of Slochteren formation (avg 1,102 m from simulation `welld` field) plus formation penetration (~140 m average thickness) plus 10% directional drilling margin |
| Surface temperature | 10 | °C | Long-term average annual surface temperature for the Netherlands (KNMI reference value) |
| Production temperature | 66.26 | °C | Average production temperature of KDK-01 (66.3°C) and KDK-02 (65.6°C) from ThermoGIS STIM+HP simulation |
| Economic lifetime | 30 | Years | Standard design lifetime for geothermal doublet systems in the Netherlands, consistent with TNO/ThermoGIS guidelines |

---

## Well & Surface Costs

| Parameter | Value | Unit | Justification |
|---|---|---|---|
| Well cost scaling factor | 1.5 | — | Standard scaling factor for the Netherlands, accounting for local drilling market premiums and mobilisation costs relative to global benchmarks |
| Well costs | 2.247 | M€/well | Calculated using the standard ThermoGIS well cost formula: `1.5 × (0.2 × depth² + 700 × depth + 250,000) × 10⁻⁶` at 1,300 m depth |
| Stimulation cost | 0.5 | M€/well | Representative cost for hydraulic well stimulation in the Slochteren sandstone formation, consistent with Dutch geothermal practice |
| Pump investment | 0.3 | M€/pump | Standard downhole pump installation cost for geothermal wells at this depth and flow rate range |
| Number of wells | 4 | — | Two doublets (KDK-01 and KDK-02), each comprising one production well and one injection well |

---

## Heat System Parameters

| Parameter | Value | Unit | Justification |
|---|---|---|---|
| Reinjection temperature | 40 | °C | District heating return temperature (`dh_return_temp`) set in ThermoGIS STIM+HP simulation settings, consistent with Dutch district heating network standards |
| Direct heat production | 19.92 | MWth | Auto-calculated by ThermoGIS LCOE model from flow rate, production temperature, and reinjection temperature; includes heat pump contribution (KDK-01: 9.12 MWth + KDK-02: 9.20 MWth = 18.32 MWth geothermal + HP uplift) |
| Load hours | 6,000 | hr/yr | Effective annual operating hours set in ThermoGIS simulation settings; equivalent to ~68% capacity factor, consistent with Dutch district heating demand patterns |
| Direct heat plant investment | 150 | k€/MWth | Standard surface heat installation cost per unit of thermal capacity for geothermal district heating systems in the Netherlands |
| (co) heat relative starting temp | 0.99 | — | Set to maximum (99%) to utilise the full available temperature range from production temperature (66.26°C) down to reinjection temperature (40°C), maximising heat extraction |
| COP (heat pump) | 5.32 | — | Average heat pump coefficient of performance from ThermoGIS simulation: KDK-01 `cophp` = 5.369, KDK-02 `cophp` = 5.274 |
| Pressure of water loop | 6 | bar | Standard operating pressure for a medium-scale Dutch district heating network serving an urban area the size of Utrecht |
| Electricity price (pumps) | 150 | €/MWhe | Conservative industrial electricity price assumption for the Netherlands; actual large-scale geothermal operators may negotiate lower rates (~€100/MWhe) |

---

## Rock & Fluid Properties

| Parameter | Value | Unit | Justification |
|---|---|---|---|
| Cp water | 4,250 | J/kg·K | Specific heat capacity of saline formation brine, slightly higher than pure water (4,182 J/kg·K) due to dissolved salts in the Slochteren formation |
| ρ water | 1,078 | kg/m³ | Density of saline formation brine typical for the Slochteren aquifer at Utrecht conditions |
| Cp rock | 1,000 | J/kg·K | Specific heat capacity of Slochteren sandstone, consistent with TNO/ThermoGIS default values for this formation |
| ρ rock | 2,700 | kg/m³ | Bulk density of Slochteren sandstone, consistent with TNO/ThermoGIS default values |

---

## Ultimate Recovery

| Parameter | Value | Unit | Justification |
|---|---|---|---|
| Subsurface area | 10 | km² | Estimated combined drainage area of two doublets. Each doublet drains approximately π × 1,500² ≈ 7 km², with a 0.7 overlap factor applied for the two sites spaced ~6.4 km apart: 2 × 7 × 0.7 ≈ 10 km² |
| Subsurface thickness | 140 | m | Average net formation thickness from ThermoGIS simulation transmissivity data for KDK-01 (~134 m) and KDK-02 (~141 m) |

---

## Financial Parameters

| Parameter | Value | Unit | Justification |
|---|---|---|---|
| Inflation | 3 | % | Representative of current Dutch inflation environment; consistent with ECB medium-term inflation target and recent Netherlands CPI trends |
| Loan rate | 6.0 | % | Typical interest rate for infrastructure project finance in the Netherlands for geothermal developments at current market conditions |
| Required return on equity | 15 | % | Standard required return for renewable energy infrastructure projects reflecting moderate-to-high subsurface risk profile |
| Equity share | 20 | % | Typical equity contribution for capital-intensive infrastructure projects; the majority of financing is debt-funded |
| Debt share | 80 | % | Follows from 20% equity; standard for geothermal infrastructure projects with long operational lifetimes and stable cash flows |
| Tax rate | 25 | % | Approximation of Dutch corporate income tax rate (25.8% for profits above €200,000) |
| Term loan | 15 | Years | Standard loan term for geothermal infrastructure, covering the initial capital recovery period within the 30-year project lifetime |
| Depreciation period | 15 | Years | Linear depreciation over the loan term, consistent with Dutch fiscal treatment of geothermal assets |
| Fiscal stimulus | None | — | No fiscal stimulus applied in the base case. Note: Dutch SDE++ subsidies for renewable heat, if applied, would further improve project economics |

---

## Result

| Metric | Value | Unit |
|---|---|---|
| **LCOE** | **14.11** | **€/GJ** |
| Equivalent LCOE | 50.8 | €/MWh |
| Annual heat production | 430,319 | GJ/yr |
| Total CAPEX | 14.28 | M€ |

