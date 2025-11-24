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

Despite the availability of information in the EXIOBASE, some variables needed in the NEMESIS-World were not available the database, such as the gross fixed capital formation (only available at the regional level, see Table above) and the income accounts for households and the governments. In the next sub-sections we discuss the strategy to address these gaps.

## 3.2 Energy data

to complete

## 3.3 GHG emissions data

to complete

## 3.4 Other data

to complete