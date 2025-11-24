# 4 Detailed model features

## 4.1 General structure

The model is structured around several interconnected blocks (Figure below).

!["NEMESIS-World general scheme"](figs/NeW_general_structure.png)

It starts with **households**, whose income—composed of labour and capital earnings and adjusted for taxes and transfers from or to the government—determines both the level and composition of final consumption.
On the other side, the **government** collects taxes and provides support to households and firms through social benefits and subsidies. The government also directly demands products and services from various economic sectors.
Household and government final consumption, combined with intermediate consumption and investment goods demanded by other economic sectors, constitute the domestic **demand addressed** to domestic firms. Adding exports leads to the total demand faced by the domestic economy.
In response to this total demand, domestic firms decide whether to meet it through **domestic production or imports**. In the case of imports, the product or service imported from one region corresponds to the exports of the supplying region.
For the portion of demand covered by domestic production, the **production** process requires intermediate consumption from other sectors, capital (or investments accounting for net of installed capital and obsolescence), and labour. All **production factors** are remunerated at market prices: intermediate and investment goods are paid at production prices plus margins, while labour is paid through wages.
Wage formation depends on the **labour** demand from firms, differentiated by qualification levels, and on the labour supply, which results from the population structure in terms of age and education, but also on the tension on the labour market, proxied by the unemployment rate by educational level. Labour supply is exogenous in the model.
Domestic production of goods and services requires, among other inputs, energy—part of which comes **from fossil fuel sources**. The use of fossil energy leads to **GHG emissions** into the atmosphere. Household consumption, particularly for heating, cooling, and private transportation, also involves fossil energy use and therefore contributes to GHG emissions. Additionally, some specific production processes directly generate GHG emissions into the air.

## 4.2 Supply side

to complete

!["Production function nested structure"](figs/NeW_SupplySide_nested_ces.png)

## 4.3 Households' consumption

### 4.3.1 Aggregated consumption

to complete

### 4.3.2 Consumption allocation by purpose

to complete

!["Households' consumption nested structure"](figs/NeW_ConsoAll_nested_ces.png)
**: Trade is modelled as a fixed share of households’ consumption of products*

## International trade

to complete

## Labour market

to complete

## Energy and climate module

to complete

| Technology           | Overnight investments cost (€2019/kW) | Fixed O&M cost (€2019/kW) | Variable O&M cost (€2019/MWh) | Effective capacity factor (%) | Technical capacity factor (%) | Net conversion efficiency (%) | Lifetime (years) | Construction time (years) |
|---------------------|--------------------------------------|----------------------------|-------------------------------|-------------------------------|-------------------------------|------------------------------|-----------------|---------------------------|
| Nuclear             | 3,853                                | 122                        | 7.9                           | 0.75                          | 0.85                          | 0.38                         | 50              | 8.0                       |
| Coal                | 1,511                                | 38                         | 3.7                           | 0.60                          | 0.80                          | 0.46                         | 40              | 3.0                       |
| Coal (CCUS)*        | 3,629                                | 69                         | 6.4                           | 0.50                          | 0.80                          | 0.29                         | 40              | 5.0                       |
| Gas                 | 755                                  | 21                         | 2.5                           | 0.35                          | 0.35                          | 0.57                         | 30              | 3.0                       |
| Gas (CCUS)*         | 1,931                                | 45                         | 3.5                           | 0.30                          | 0.80                          | 0.46                         | 30              | 5.0                       |
| Oil                 | 1,273                                | 22                         | 2.9                           | 0.40                          | 0.40                          | 0.35                         | 40              | 1.0                       |
| Biomass (wastes)    | 2,136                                | 47                         | 0.9                           | 0.60                          | 0.10                          | 0.34                         | 20              | 3.0                       |
| Biomass (biogas)    | 1,208                                | 26                         | 2.7                           | 0.60                          | 0.20                          | 0.38                         | 25              | 2.0                       |
| Biomass             | 2,069                                | 43                         | 3.8                           | 0.60                          | 0.80                          | 0.50                         | 40              | 3.0                       |
| Biomass (CCUS)*     | 3,820                                | 24                         | 2.9                           | 0.50                          | 0.70                          | 0.43                         | 30              | 5.0                       |
| Hydro               | 3,183                                | 27                         | 0.3                           | 0.50                          | 1.00                          | 1.00                         | 60              | 8.0                       |
| Geothermal          | 4,743                                | 101                        | 0.3                           | 0.45                          | 0.45                          | 0.30                         | 30              | 4.0                       |
| Solar PV            | 363                                  | 13                         | 0.0                           | 0.17                          | 0.17                          | 1.00                         | 20              | 1.5                       |
| CSP                 | 4,032                                | 105                        | 0.1                           | 0.26                          | 0.26                          | 0.33                         | 25              | 2.5                       |
| Wind Onshore        | 1,171                                | 19                         | 0.5                           | 0.26                          | 0.26                          | 1.00                         | 25              | 1.5                       |
| Wind Offshore       | 1,722                                | 35                         | 0.5                           | 0.39                          | 0.39                          | 1.00                         | 25              | 2.5                       |
| Tidal               | 5,093                                | 128                        | 0.1                           | 0.27                          | 0.27                          | 1.00                         | 80              | 5.0                       |

Source: Authors calculation based on [IEA (2024)](https://iea.blob.core.windows.net/assets/a2aaddf1-a0f8-4ecb-8b20-31622423bc2e/GlobalEnergyandClimateModelDocumentation2024.pdf), [Mantzos, et al. (2019)](https://data.europa.eu/doi/10.2760/32835) and [UNData (2025a)](https://unstats.un.org/unsd/energystats/).
*NB: values differ overtime (except lifetime and construction time) and according to region.*
**: In fact CCS technologies are not available on production before 2035 in the model*





