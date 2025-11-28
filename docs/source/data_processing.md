# Data and Data Processing

## 3.1 Main economic variables

The NEMESIS-World model uses different databases, with the main source for the economic data being the EXIOBASE v3.8.2 ([Stadler et al., 2021](https://doi.org/10.5281/ZENODO.5589597)).

Global Multi Regional Input-Output (MRIO) tables are key data for the large scale macroeconomic models. These databases have a worldwide coverage and describe the economic exchanges between economic activities and regions (inter-industry exchanges), the final demands by region, the value added and production and, for some, satellite accounts on economic inputs or environment.

We chose to rely on EXIOBASE due to (1) its extensive geographical coverage, including multiple “Rest of the World” regions, which is valuable for climate mitigation policy assessments and IPCC reporting; (2) its highly detailed sector disaggregation, enabling the modelling of key industrial and transport sectors in mitigation analyses; and (3) its good reputation within the scientific community, which provides confidence in the reliability of its data.

EXIOBASE is a GMRIO dataset that includes a set of satellite accounts. Data are available from 1995 to 2022, with the last two years (2021 and 2022) are based on top-down projections. All values are expressed in monetary units (current million euros). The reference year used for the model is 2019, avoiding 2020 because of COVID-19 and the projected years 2021 and 2022. The model directly uses the data presented in Table below from the database by region and by country.

| Variables                                                                 | Region | Sector/product | Agents/Final Uses |
|---------------------------------------------------------------------------|--------|----------------|-----------------|
| Production                                                                | x      | x              |                 |
| Intermediate consumption (excluding energy)                               | x      | x              |                 |
| Energy consumption                                                        | x      | x              |                 |
| Gross fixed capital formation                                             | x      |                |                 |
| Employment by level of qualification                                      | x      | x              |                 |
| Value added                                                               | x      | x              |                 |
| Imports by origin                                                         | x      | x              | x               |
| Exports by origin                                                         | x      | x              | x               |
| Demands addressed (intermediate consumption, gross fixed capital formation, final consumptions) | x | x | x |
| Households’ final consumption                                             | x      | x              | x               |
| NPISH final consumption                                                   | x      | x              | x               |
| Government final demand                                                   | x      | x              | x               |
| Change in inventories                                                     | x      | x              |                 |
| Compensation of employees                                                 | x      | x              |                 |
| Gross operating surplus                                                   | x      | x              |                 |
| Taxes less subsidies on products purchased                                | x      | x              |                 |
| Other net taxes on production                                             | x      | x              |                 |
*Note: All retrieved variables are in current million euros.*

Despite the availability of information in the EXIOBASE, some econoimic variables needed in the NEMESIS-World were not available the database, such as the gross fixed capital formation (only available at the regional level, see Table above) and the income accounts for households and the governments. In the next sub-sections we discuss the strategy to address these gaps.

## 3.2 Gross fixed capital formation

EXIOBASE provides information on total gross fixed capital formation (GFCF) for each region, and on the sector and region that produce these capital goods (supplying region and sector). Thus, the region and sector supplying the capital goods and the region demanding them are available in EXIOBASE, but not the demanding sector.
To calculate the GFCF by demanding region and sector, we calculate the GFCF intensity for each sector, i.e., GFCF divided by the level of production (or value added in some case) using different data sources. The main source ([OECD, 2024](https://data-explorer.oecd.org)) allows the calculation of these intensities for ten regions: Canada, Germany, Spain, France, United-Kingdom, Italy, Japan, Mexico, other EU countries and USA. For the remaining countries (Australia, China, India, South Korea, Russia and Saudi Arabia as a proxy of the region ‘RoW: Middle-East’), we used other sources, mainly based on the national statistical offices. Finally for the regions without statistical information (Brazil, RoW Asia & Pacific, RoW Europe, RoW Africa and RoW America) we proxied the GFCF intensity with the intensity of the geographically closest region(s) with available data. Once all GFCF intensities are calculated, we calculated their 5 years average value, 2015-2019 (when feasible). Thereafter, we multiplied this mean intensity by region and sector by the EXIOBASE production level to calculate first estimates of GFCF by region and sector. We rescaled these values, using a RAS method, to ensure the sum for each region equals the total value of GFCF by region in EXIOBASE, leading to the final value of GFCF by region and sector used in the model. 

## 3.3 Agents’ accounts: households and governments

EXIOBASE delivers information on households’ income, limited to the compensation of employees. Although this represents a large share of a household’s income, it does not represent all potential sources. To complete these data, we used sector national accounts from [OECD (2024)](https://data-explorer.oecd.org) that deliver statistical information for 45 countries. First, we calculate the gross balance of primary income using EXIOBASE information on compensation of employees (assuming that all are received by households) and gross operating surplus (only at the regional level—the share allocated to households is calculated based on OECD data). All other components of the gross balance of primary income (property incomes received and paid) are calculated from OECD data but are scaled on EXIOBASE based on the compensation of employees. A similar methodology is used for the calculation of the households’ gross disposable income (composed of global primary income, direct tax paid, social contribution received and paid, social benefits received and paid and current transfers received and paid), gross saving (calculated as the gross disposable income minus the households’ consumption expenditures and adjusted for the change in pension entitlements ) and net lending and borrowing (the gross savings plus net capital transfers and minus households' gross capital formation and acquisitions less disposals of non-financial non-produced assets).
We also do similar calculations for the government income using final consumption as a benchmark, instead of compensation of employees used for households.



## 3.4 Energy data

To ensure harmonisation across DIAMOND models, NEMESIS-World uses energy balances from the OMNIA model, which are based on processed and corrected data from UN Energy Statistics and the UN Energy Balance ([UNData, 2025](https://unstats.un.org/unsd/energystats/)). However, due to differences in geographical coverage between the two models, some OMNIA regions (i.e., Australia, Indonesia, Germany, France, Italy, and Spain) need to be split from their respective OMNIA aggregates to match the NEMESIS-World regional disaggregation. To do this, we used the raw UN Energy Balance data to calculate the share of each of these countries within their aggregated OMNIA region. These shares are then applied to the OMNIA dataset, allowing us to disaggregate these countries while maintaining overall consistency and preserving the data processing performed for the OMNIA model.
On top of energy quantities, the model requires energy prices to link physical units with monetary units. For the reference year, we used the IEA Energy Prices datasets ([IEA 2025](https://www.iea.org/data-and-statistics/data-product/energy-prices), namely the “Energy Prices and Taxes” and “Energy Prices Taxation Information”). These datasets offer partial information on wholesale and industrial energy prices, both with and without taxes, for oil, natural gas, solid fuels, and electricity and for numerous countries, beyond OECD countries. Since the data are incomplete, we supplemented them with taxation information from [OECD (2019)](https://doi.org/10.1787/058ca239-en), covering excise duties and carbon taxes. We then processed these data to derive consistent energy prices—with and without taxes—for industries, power generation, households, and services.



## 3.3 GHG emissions data

GHG emissions are sourced from the EDGAR database Global Greenhouse Gas Emissions ([Crippa et al., 2024]( https://data.europa.eu/doi/10.2760/4002897)) and are allocated across the NEMESIS-World sectors based first on the corresponding sector, and second, on the energy quantities, weighted by average emission factors.


## 3.4 Other data

The model also requires additional variables that are not included in the previously mentioned dataset, such as population by age and level of qualification, unemployment rate, and interest rates. The latter two are sourced from ([OECD, 2025](https://data-explorer.oecd.org)). Population data is taken from [KC et al. (2024)](https://doi.org/10.5281/ZENODO.14718294), which provides demographic information by age group, following the classification used in NEMESIS-World: [0-15[; [15-25[; [25-55[; [55-65[; [65-75[; [75+]. Additionally, this dataset includes information on qualification levels, which is essential for calibrating labour supply by education level in the model.