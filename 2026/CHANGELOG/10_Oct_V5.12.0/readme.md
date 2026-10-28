# [5.12.0] - 2026-10-29
## ClimateTRACE,deprecation-warning
- None
## ClimateTRACE,multiple-sectors,post-processing
### Added
- [Added] For reductions from ERS, cost estimates are now available for nearly each asset-strategy combination.
- [Added] For ERS, carbon-sink sectors (net-soil-organic-carbon, removals) now include a "do nothing" option for some instances, to not yield negative-reduction strategies.
### Changed
- [Changed] Reductions from emissions reducing solutions (ERS) have been re-calculated from new sector strategies and a revised ranking method, with ~5% increase in emission reduction potential in total.
- [Changed] Previously in V5.11.0, cropland-fires reduction totals were based on old emission baselines. This has changed in V5.12.0, where emission reduction is adjusted to current asset emissions and for crop residue effects. As a result, emission reduction potential has decreased by 95% from V5.11.0 to V5.12.0, since V5.11.0 measured reductions against baseline emissions about 30x the sector’s actual emissions, based on estimates from when Climate TRACE reported CO2 emissions from cropland fires. A new emissions reduction solution (ERS) retains crop residue instead of burning it, now counting soil carbon gain.
- [Changed] Non-GHG pollutants are estimated with a new method. Where a sector doesn't report a pollutant directly, it's now estimated from updated pollutant-to-co2e_100yr ratios based on the EDGAR and CEDS inventories.
### Deprecated
- [Deprecated] None
### Fixed
- [Fixed] None
### Known Issues
- [Known Issues] In rice-cultivation country emissions, off-season months for 24 countries are filled with extrapolated values, but not at the asset-level; this is due to a mismatch in null vs 0 handling in extrapolation, and as a result, country totals can be higher than the summed asset totals by 13–18% in these countries. To be fixed in V5.13.0.
## ClimateTRACE,individual-changelogs
## agriculture,enteric-fermentation-cattle-operation
### Added
- [Added] New emissions reduction solution added - Raise fewer beef or dairy cattle since consumption is down as consumer habits shift - identified as reducing beef demand (b_demand1) and reducing dairy demand (d_demand1). This assumes the total head of cattle (activity) is reduced by 10%, thereby reducing emissions by 10%. This was applied to a subset of countries based on Organisation for Economic Co-operation and Development (OECD) and the Food and Agriculture Organization (FAO) human consumption and fresh dairy consumption per capita: ARG, AUS, AUT, BEL, BGR, BRA, CAN, CHE, CHL (beef only), CHN, COL, CYP, CZE, DEU, DNK, ESP, EST, FIN, FRA, GBR, GRC, HRV, HUN, IND (dairy only), IRL, ISR (beef only), ITA, JPN (beef only), KAZ, KOR (beef only), LTU, LUX, LVA, MEX, MLT, MYS (beef only), NLD, NOR, NZL, PAK, POL, PRT, PRY, ROU, RUS, SVK, SVN, SWE, TUR, UKR (dairy only), USA, and ZAF (beef only).
### Changed
- [Changed] None
### Deprecated
- [Deprecated] None
### Fixed
- [Fixed] AUS country-level emissions no longer jump after 2019. Previously, in V5.11, dairy cattle counts were calculated using two non-overlapping datasets, causing 2015–2018 values to appear lower than 2019 onward. This has been fixed by switching to a single, unified AUS dataset.
- [Fixed] Previously in changelog v5.10 it was mentioned new emission reduction solutions were provided. However, these were delayed and are now released in V5.12. This includes - New emissions reduction solutions (ERS) for each cattle operation have been generated for v5.10. This includes additional feed additives; The new ERS in v5.10 are ranked based on a weighted approach that includes cost, safety, confidence in use, and emission reduction potential when applying feed additives to mitigate enteric fermentation; The error with the agolin emission reduction solution (ERS) applied to individual cattle operations, since the v4.8.0 release, has been fixed.
### Known Issues
- [Known Issues] The current Feed Additives Emissions Reduction Solutions (ERS) methodology contains three structural limitations: using broad categorical tiers groups vastly different efficacy values together (e.g., a 9% vs. 19% reduction receive identical scores), internal min-max cost normalization causes rank shifts whenever additives or prices are updated, and scoring raw LD50 numbers misrepresents actual toxicity risk by ignoring label dosages. Future releases will resolve these issues by transitioning to continuous actual efficacy percentages, adopting a fixed outside cost baseline, and evaluating toxicity based on a true margin of safety.
- [Known Issues] Effort has been made to reduce duplicate operations in the U.S. and globally. In the U.S. this was caused when a reported state government CAFOs had location coordinates set away from the operation not within the operation. For example, at the end of the CAFO driveway leading into the operation or the owners home away from the CAFO. Further work will continue to deduplicate Climate TRACE cattle operations in the U.S.
- [Known Issues] Duplicates and false-positive locations can exist for this sector. If found, please let us know via email and provide the asset id and latitude and longitude information.
- [Known Issues] Certain cattle operations may be multiple cattle operations combined into one. As a result, the regression model overestimated the total head of cattle at these operations. Any beef cattle operation with a total head (capacity) greater than 40,000 had their capacity capped at 40,000. Additionally, any dairy farm operation with a total head (capacity) greater than 4,000 had their capacity capped at 4,000. These are marked in the ‘other2’ column. Future updates will address this issue.
## agriculture,enteric-fermentation-cattle-pasture
### Added
- [Added] None
### Changed
- [Changed] None
### Deprecated
- [Deprecated] None
### Fixed
- [Fixed]  Previously in changelog v5.10 it was mentioned new emission reduction solutions were provided. However, these were delayed and are now released in V5.12. This includes - New emissions reduction solutions (ERS) were generated for pasture-based enteric fermentation. These include stocking-rate optimization and herd-size reduction, feed additives, and silvopastoral rotation with improved forage quality.
### Known Issues
- [Known Issues] None
## agriculture,manure-left-on-pasture-cattle
### Added
- [Added] None
### Changed
- [Changed] None
### Deprecated
- [Deprecated] None
### Fixed
- [Fixed] Previously in changelog v5.10 it was mentioned new emission reduction solutions were provided. However, these were delayed and are now released in V5.12. This includes- New emissions reduction solutions (ERS) were generated for manure left on pasture. These include pasture rotation with optimized stocking and nitrogen-reducing fodder crops, and silvopastoral rotation.
### Known Issues
- [Known Issues] None
## agriculture,manure-management-cattle-operation
### Added
- [Added] New emissions reduction solution added - Raise fewer beef or dairy cattle since consumption is down as consumer habits shift - identified as reducing beef demand (b_demand1) and reducing dairy demand (d_demand1). This assumes the total head of cattle (activity) is reduced by 10%, thereby reducing emissions by 10%. This was applied to a subset of countries based on Organisation for Economic Co-operation and Development (OECD) and the Food and Agriculture Organization (FAO)human consumption and fresh dairy consumption per capita: ARG, AUS, AUT, BEL, BGR, BRA, CAN, CHE, CHL (beef only), CHN, COL, CYP, CZE, DEU, DNK, ESP, EST, FIN, FRA, GBR, GRC, HRV, HUN, IND (dairy only), IRL, ISR (beef only), ITA, JPN (beef only), KAZ, KOR (beef only), LTU, LUX, LVA, MEX, MLT, MYS (beef only), NLD, NOR, NZL, PAK, POL, PRT, PRY, ROU, RUS, SVK, SVN, SWE, TUR, UKR (dairy only), USA, and ZAF (beef only).
### Changed
- [Changed] None
### Deprecated
- [Deprecated] None
### Fixed
- [Fixed] AUS country-level emissions no longer jump after 2019. Previously, in V5.11, dairy cattle counts were calculated using two non-overlapping datasets, causing 2015–2018 values to appear lower than 2019 onward. This has been fixed by switching to a single, unified AUS dataset.
- [Fixed] Previously in changelog v5.10 it was mentioned new emission reduction solutions were provided. However, these were delayed and are now released in V5.12. This includes- each asset (cattle operations) has new emissions reduction solutions (ERS) based on changing a single MMS in multiple MMS; the new manure management emissions reduction solutions (ERS) are ranked based on a weighted approach that includes cost and emission reduction potential when retrofitting a single MMS in the multiple MMS at each cattle operation; previous emissions reduction solutions (ERS)before v5.10 are now deprecated.
### Known Issues
- [Known Issues] Effort has been made to reduce duplicate operations in the U.S. and globally. In the U.S. this was caused when a reported state government CAFOs had location coordinates set away from the operation not within the operation. For example, at the end of the CAFO driveway leading into the operation or the owners home away from the CAFO. Further work will continue to deduplicate Climate TRACE cattle operations in the U.S.
- [Known Issues] Duplicates and false-positive locations can exist for this sector. If found, please let us know via email and provide the asset id and latitude and longitude information.
- [Known Issues] Certain cattle operations may be multiple cattle operations combined into one. As a result, the regression model overestimated the total head of cattle at these operations. Any beef cattle operation with a total head (capacity) greater than 40,000 had their capacity capped at 40,000. Additionally, any dairy farm operation with a total head (capacity) greater than 4,000 had their capacity capped at 4,000. These are marked in the ‘other2’ column. Future updates will address this issue.
- [Known Issues] Manure emissions in conflict-affected regions with large cattle populations (e.g., Afghanistan, East Africa) may overestimate emissions due to IPCC 2019 animal waste management system regional defaults assigned. Future updates will implement country-specific MMS to resolve this issue.
- [Known Issues] Current country-level manure emissions assume a single climate zone and one multiple MMS type per cattle category (beef/dairy), potentially biasing CH4 and N2O emissions’ estimates, especially in temperate climates (i.e. Russia and Canada) where CH4 production is reduced in cooler/temperate climates. Future updates will improve accuracy by implementing multi-MMS allocations and refined country-specific climate zones.
## agriculture,net-soil-organic-carbon
### Added
- [Added] Emission Reduction Solution (ERS) for this sector are now included.
### Changed
- [Changed] None
### Deprecated
- [Deprecated] None
### Fixed
- [Fixed] None
### Known Issues
- [Known Issues] None
## agriculture,rice-cultivation
### Added
- [Added] Extended country-level history back to 2015 for the 57 independently modeled countries (previously 2021-2025) at monthly resolution, indexed to each country's 2021 baseline using FAOSTAT interannual variation.
- [Added] Included full 2015-2025 country-level estimates for countries not independently modeled, aligned to the FAOSTAT rice cultivation inventory (release dated October 28, 2025), reported at annual resolution.
- [Added] Backfilled 2021-2024 for countries first modeled in 2025, which were previously reported as zero, using the FAOSTAT year-over-year trend anchored to each country's first modeled year and carrying the modeled 2025 spatial pattern and monthly shape.
### Changed
- [Changed] Replaced the previously submitted emissions for non-independently-modeled countries with FAOSTAT-reported values. The prior estimates applied a single flooded-rice emission factor to all harvested areas without adjusting for upland or rainfed water regimes, which overstated emissions where rice is predominantly upland or rainfed (most notably in West Africa). FAOSTAT's inventory applies water-regime scaling; this lowers the non-modeled-country total by roughly 69%.
- [Changed] 27 countries had a full modeled series applied: University of Malaysia/PaddyWatch directly modeled every year from 2021 to 2025. The 2021–2024 annual estimates were split into monthly values using the 2025 monthly pattern. Years 2015–2020 were back-cast using FAOSTAT’s year-to-year change, anchored to 2021. Countries: BGD, BRA, CHN, ESP, IDN, IND, IRN, ITA, JPN, KHM, KOR, LAO, LKA, MDG, MLI, MMR, MYS, NGA, NPL, PAK, PHL, PRK, THA, TWN, TZA, USA, VNM.
- [Changed] 12 countries had a first modeled series applied: University of Malaysia/PaddyWatch directly modeled each year from the country’s first modeled year through 2025, and those years were split into monthly values. The years from 2021 up to the first modeled year, and all of 2015–2020, were back-filled using FAOSTAT’s year-to-year change, anchored to the first modeled year. Countries (first modeled year): BTN (2024), ECU (2023), EGY (2022), ETH (2022), GUY (2023), MEX (2023), PER (2023), RUS (2023), SUR (2023), TLS (2024), TUR (2023), URY (2023).
- [Changed] 18 countries had modeled for only 2025: University of Malaysia/PaddyWatch directly modeled 2025 only. All years from 2015 to 2024 were back-filled using FAOSTAT’s year-to-year change, anchored to the 2025 model. Countries: BDI, BFA, BGR, CMR, FRA, GIN, GMB, GNB, GRC, KEN, MAR, MRT, NER, PRT, RWA, SEN, SLE, UGA.
- [Changed] 61 countries only had FAOSTAT data applied: University of Malaysia/PaddyWatch did not model these countries in any year. Emissions come from the FAOSTAT rice cultivation inventory (release 2025-10-28), reported annually (one value per year) for 2015–2025. 2024 is derived from FAOSTAT implied emission factors, and 2025 is held at the 2024 value (see Known Issues). Countries: AFG, AGO, ARG, AUS, AZE, BEN, BLZ, BOL, BRN, CAF, CHL, CIV, COD, COG, COL, COM, CRI, CUB, DOM, DZA, FJI, FSM, GAB, GHA, GTM, HND, HTI, HUN, IRQ, JAM, KAZ, KGZ, LBR, MKD, MOZ, MUS, MWI, NIC, PAN, PNG, PRI, PRY, ROU, SAU, SDN, SLB, SLV, SOM, SSD, SWZ, TCD, TGO, TJK, TKM, TTO, UKR, UZB, VEN, ZAF, ZMB, ZWE.
### Deprecated
- [Deprecated] None
### Fixed
- [Fixed] None
### Known Issues
- [Known Issues] Non-modeled-country emissions follow FAOSTAT's Tier-1 methodology, which recent field literature (Chen et al. 2023; Nikolaisen et al. 2023) suggests may underestimate African rice emissions. A future release may adopt a water-regime-resolved, elevated-emission-factor approach for these regions.
- [Known Issues] 2024 values for non-modeled countries are derived from FAOSTAT implied emission factors applied to 2024 harvested area; 2025 is held at the 2024 value pending FAOSTAT's next inventory release.
## buildings,non-residential-onsite-fuel-usage
### Added
- [Added] Data period extended for existing sources. Start_date 2026-08-01 to end_date 2026-08-31.
### Changed
- [Changed] Updated historical data for existing sources. Start_date 2026-01-01 to end_date 2026-07-31.
### Deprecated
- [Deprecated] None
### Fixed
- [Fixed] None
### Known Issues
- [Known Issues] The residential/non-residential split still relies on Global Human Settlement Layer (GHSL) data for defining which buildings are residential or nonresidential, even though the building volume itself now comes from TEMPO. The definition used by GHSL for this tends to label more building area as residential than non-residential. This may introduce a bias towards attributing additional emissions as residential rather than nonresidential. This has been present in all previous versions of this subsector.
- [Known Issues] The emissions factors are back-calculated from a combination of emissions data (disaggregated EDGAR) and activity data. This leads to some emissions factors being well-outside of a standard range of values for those quantities. This has been present in all previous versions of this subsector.
- [Known Issues] Regional totals for some very small territories that border a much larger emitter can include part of the neighbour's emissions and exceed that territory's own national total. This arises because national totals are distributed across a fine grid and then summed back up by country, and border cells are not resolved identically in both steps. This is most pronounced for Macau, Hong Kong and Syria. This has been present in all previous versions of this subsector.
- [Known Issues] Our statistical data on several countries report no energy use at all of one fuel in one sector, so the corresponding energy and emissions are zero for those countries. This has been present in all previous versions of this subsector.
- [Known Issues] There are several cases of orphaned emissions (emissions with no corresponding activity) due to following the IPCC convention that most gases and pollutants except CO2 report both fossil and biomass emissions together since our activity basis is fossil activity, this leads to a mismatch. This also prevents activity x emissions factors from achieving full equality with emissions. However, the biomass activity data are now reported (other8) and can be used to correct this issue and back out the appropriate fossil or biomass emissions factors. This has been present in all previous versions of this subsector.
## buildings,residential-onsite-fuel-usage
### Added
- [Added] Data period extended for existing sources. Start_date 2026-08-01 to end_date 2026-08-31.
### Changed
- [Changed] Updated historical data for existing sources. Start_date 2026-01-01 to end_date 2026-07-31.
### Deprecated
- [Deprecated] None
### Fixed
- [Fixed] None
### Known Issues
- [Known Issues] The residential/non-residential split still relies on Global Human Settlement Layer (GHSL) data for defining which buildings are residential or nonresidential, even though the building volume itself now comes from TEMPO. The definition used by GHSL for this tends to label more building area as residential than non-residential. This may introduce a bias towards attributing additional emissions as residential rather than nonresidential. This has been present in all previous versions of this subsector.
- [Known Issues] The emissions factors are back-calculated from a combination of emissions data (disaggregated EDGAR) and activity data. This leads to some emissions factors being well-outside of a standard range of values for those quantities. This has been present in all previous versions of this subsector.
- [Known Issues] Regional totals for some very small territories that border a much larger emitter can include part of the neighbour's emissions and exceed that territory's own national total. This arises because national totals are distributed across a fine grid and then summed back up by country, and border cells are not resolved identically in both steps. This is most pronounced for Macau, Hong Kong and Syria. This has been present in all previous versions of this subsector.
- [Known Issues] Our statistical data on several countries report no energy use at all of one fuel in one sector, so the corresponding energy and emissions are zero for those countries. This has been present in all previous versions of this subsector.
- [Known Issues] There are several cases of orphaned emissions (emissions with no corresponding activity) due to following the IPCC convention that most gases and pollutants except CO2 report both fossil and biomass emissions together since our activity basis is fossil activity, this leads to a mismatch. This also prevents activity x emissions factors from achieving full equality with emissions. However, the biomass activity data are now reported (other8) and can be used to correct this issue and back out the appropriate fossil or biomass emissions factors. This has been present in all previous versions of this subsector.
## forestry-and-land-use,forest-land-clearing
### Added
- [Added] Added GADM (asset) level dominant landcover types for years 2015-2025. The land cover data is based on 2015 Copernicus Global Land Cover (CGLS) data and is applied to all years. Note that the landcover types are based on the dominant landcover type for each GADM level, and may not reflect the actual landcover type described in the CGLS for that asset level.
### Changed
- [Changed] None
### Deprecated
- [Deprecated] None
### Fixed
- [Fixed] None
### Known Issues
- [Known Issues] At least fifty assets in the USA have anomalous spikes in emissions in January 2026.
## forestry-and-land-use,forest-land-degradation
### Added
- [Added] Added GADM (asset) level dominant landcover types for years 2015-2025. The land cover data is based on 2015 Copernicus Global Land Cover (CGLS) data and is applied to all years. Note that the landcover types are based on the dominant landcover type for each GADM level, and may not reflect the actual landcover type described in the CGLS for that asset level.
### Changed
- [Changed] None
### Deprecated
- [Deprecated] None
### Fixed
- [Fixed] None
### Known Issues
- [Known Issues] None
## forestry-and-land-use,forest-land-fires
### Added
- [Added] Added GADM (asset) level dominant landcover types for years 2015-2025. The land cover data is based on 2015 Copernicus Global Land Cover (CGLS) data and is applied to all years. Note that the landcover types are based on the dominant landcover type for each GADM level, and may not reflect the actual landcover type described in the CGLS for that asset level.
### Changed
- [Changed] None
### Deprecated
- [Deprecated] None
### Fixed
- [Fixed] None
### Known Issues
- [Known Issues] None
## forestry-and-land-use,shrubgrass-fires
### Added
- [Added] Added GADM (asset) level dominant landcover types for years 2015-2025. The land cover data is based on 2015 Copernicus Global Land Cover (CGLS) data and is applied to all years. Note that the landcover types are based on the dominant landcover type for each GADM level, and may not reflect the actual landcover type described in the CGLS for that asset level.
### Changed
- [Changed] None
### Deprecated
- [Deprecated] None
### Fixed
- [Fixed] None
### Known Issues
- [Known Issues] None
## forestry-and-land-use,wetland-fires
### Added
- [Added] Added GADM (asset) level dominant landcover types for years 2015-2025. The land cover data is based on 2015 Copernicus Global Land Cover (CGLS) data and is applied to all years. Note that the landcover types are based on the dominant landcover type for each GADM level, and may not reflect the actual landcover type described in the CGLS for that asset level.
### Changed
- [Changed] None
### Deprecated
- [Deprecated] None
### Fixed
- [Fixed] None
### Known Issues
- [Known Issues] None
## fossil-fuel-operations,coal-mining
### Added
- [Added] None
### Changed
- [Changed] None
### Deprecated
- [Deprecated] None
### Fixed
- [Fixed] Previously in changelog v5.10 it was mentioned new emission reduction solutions were provided. However, these were delayed and are now released in V5.12. This includes- updated the emission reduction strategy (ERS) list and ERS crosswalk to include a new emission reduction solution, Electrification of mobile equipment, relevant to emissions from fuel combustion. Also updated previous ERS values.
### Known Issues
- [Known Issues] None
## fossil-fuel-operations,oil-and-gas-production
### Added
- [Added] None
### Changed
- [Changed] None
### Deprecated
- [Deprecated] None
### Fixed
- [Fixed] None
### Known Issues
- [Known Issues] induced electricity values for reductions strategies are deflated due to bug in calculations
## fossil-fuel-operations,oil-and-gas-refining
### Added
- [Added] Data period extended for all existing assets. Start_date 2025-10-01 to end_date 2025-12-31.
### Changed
- [Changed] None
### Deprecated
- [Deprecated] None
### Fixed
- [Fixed] Updated the names of 25 refineries to correct typos and translation issues. Asset IDs remain unchanged.
### Known Issues
- [Known Issues] None
## fossil-fuel-operations,oil-and-gas-transport
### Added
- [Added] None
### Changed
- [Changed] None
### Deprecated
- [Deprecated] None
### Fixed
- [Fixed] None
### Known Issues
- [Known Issues] induced electricity values for reductions strategies are most likely inflated due to bug in calculations
## manufacturing,aluminum
### Added
- [Added] August 2026 data added.
### Changed
- [Changed] 0 emissions now reported with zeros (previously assets for months where activity/emissions is 0 were not included).
### Deprecated
- [Deprecated] None
### Fixed
- [Fixed] None
### Known Issues
- [Known Issues] None
## manufacturing,cement
### Added
- [Added] New month added (August 2026).
### Changed
- [Changed] Added zeros where 0 production is reported.
### Deprecated
- [Deprecated] None
### Fixed
- [Fixed] Previously in changelog v5.10 it was mentioned new emission reduction solutions were provided. However, these were delayed and are now released in V5.12. Updated mission reduction strategy (ERS) and ERS crosswalk files for emission reduction solutions.
### Known Issues
- [Known Issues] Four cement assets that represent plants in Ningxia, China are listed under the location, country and owners of European plants that previously used the same source identifiers: 32437351 (Ningxia Haolong Building Materials Zhongwei Cement Plant) and 1895356 (Ningxia Jinyuyuan Resource Recycling Guyuan Cement Plant)are placed at the Wildegg and Cornaux sites in Switzerland, and 32439137 (Ningxia Guoda Cement Wuzhong Cement Plant) at the Skövde site in Sweden. 1897806 (Ningxia Jinyuyuan Resource Recycling Wuzhong Cement Plant) is correctly located in China but still lists the owners of the Slite plant in Sweden. Locations, countries and ownership for these four assets will be corrected in a future release.
## manufacturing,petrochemical-steam-cracking
### Added
- [Added] Data period extended for existing sources. Start_date 2025-10-01 to end_date 2025-12-31.
- [Added] Assets 242 and 243 with historical data.
### Changed
- [Changed] None
### Deprecated
- [Deprecated] None
### Fixed
- [Fixed] None
### Known Issues
- [Known Issues] None
## manufacturing,pulp-and-paper
### Added
- [Added] None
### Changed
- [Changed] Updated metadata. Asset `type` made more descriptive to provide information on the pulping process types used at the facility. New values cover the following methods: Kraft (all kraft softwood and hardwood pulp, bleached and unbleached), Chemical (chemical wood pulp), Semi-chemical (semi-chemical wood pulp), Mechanical (mechanical wood pulp), Mechanical and semi-chemical (mechanical and semi-chemical wood pulp), Recycled (recycled fibre pulp), Non-wood fibre (pulp from fibres other than wood) and Unspecified (miscellaneous pulp and unmatched products). Pulping process is a key driver of emissions intensity; emissions factors are applied at the granular output product level within each category.
- [Changed] Asset TZPAP2602000000175 updated. From 2023 onwards the asset’s fuel type was updated to biogenic, which lowers its direct emission factor from 2023. Under CMPC’s BioCMPC modernisation project, the coal-fired boiler was decommissioned and a new black-liquor recovery boiler installed.
- [Changed] Brazil country data updated as a result of this asset change, since country totals include the asset’s emissions.
### Deprecated
- [Deprecated] None
### Fixed
- [Fixed] None
### Known Issues
- [Known Issues] None
## manufacturing,iron-and-steel
### Added
- [Added] New data columns added. other9: share of indirect (scope 2) emissions from captive power (0–1); ;other10: emission factor of captive power (tCO2/MWh)
- [Added] New month added (August 2026).
- [Added] Updated the strategy list and strategy crosswalk to include new strategies and new assets for emission reduction solutions.
### Changed
- [Changed] Updated model for all data  (January 2021 - August 2026). Electricity use factors are now sourced per production route (MPP = Mission Possible Partnership (steel model, Technology Business Cases; RITE = Research Institute of Innovative Technology for the Earth, Japan (DNE21+ model); CEEW = Council on Energy, Environment and Water, India (coal DRI plant survey; the Indian Ministry of Steel’s published route emission ranges). BF/BOF plants are modelled as generating their electricity on site from off-gases (0.25 MWh/t-steel at 2.04 tCO2/MWh), reported as indirect emissions. BF/BOF direct emission factor for the US, Europe and the UK is 1.4 tCO2/t-steel, calibrated against EU ETS and validated using US EPA. Coal-based DRI direct emission factors updated (DRI–EAF 2.27, DRI–IF 2.20 tCO2/t-steel).
- [Changed] Updated metadata. CO2_emissions_factor updated across routes, with new regional specificity. BF/BOF becomes 1.4 in EU ETS countries, the UK and the US (previously 1.9); coal DRI-EAF becomes 2.27 (previously 2.5); coal DRI-IF becomes 2.20 (previously 2.43).
- [Changed] Updated metadata definition. other1 and other2 indirect emissions include captive as well as grid power. other3 and other4 electricity use includes captive (self-generated) power.
- [Changed] Updated emissions reduction strategy parameters. Hydrogen DRI strategies: end-state direct emission factor of 0.08 tCO2/t-steel applied as an absolute value for all three strategies; route electricity use of 4.3 MWh/t-steel, with induced electricity calculated as the extra grid electricity over each plant's current use. BF/BOF –> EAF induced electricity updated to 0.64 MWh/t-steel.
### Deprecated
- [Deprecated] India-specific DRI emission factor overrides removed. Indian plants without DRI fuel-mix data now default to coal-based DRI.
### Fixed
- [Fixed] BF/BOF –> EAF strategy induced electricity corrected (0.04 –> 0.64 MWh/t-steel).
- [Fixed] Shutdown strategy induced activity units corrected from "t of CO2 per t of steel" to "t of steel per t of steel". Meaning, when a plant closes, we assume its output is made at other steel plants instead, so each tonne no longer produced induces 1 tonne of steel elsewhere.
### Known Issues
- [Known Issues] None
## power,electricity-generation
### Added
- [Added] Data period extended for existing sources. Start_date 2019-01-01 to end_date 2026-08-30.
### Changed
- [Changed] Updated PM2.5 methodology to use uncontrolled US EPA AP-42 emission factors (supplemented by EMEP/EEA for some fuels) for filterable and condensable primary particulate separately, updated PM2.5-specific control efficiencies for both filterable and condensable particulate, improved pollution control mapping, added country-specific typical coal quality, and now report primary PM2.5 as filterable + condensable.
### Deprecated
- [Deprecated] None
### Fixed
- [Fixed] None
### Known Issues
- [Known Issues] For non-operational plants the data is reported as zero values for capacity, capacity factor, activity, emissions intensity, and emissions.  The related uncertainties are also reported as zero. This is not strictly correct since there can be uncertainty in the operating status in a given month. Future work will better quantify the uncertainty when the plant is reported as non-operational.
- [Known Issues] Our remote sensing-based estimates of plant activity are biased low in some grid regions including China. We are working to address the bias in future releases.
- [Known Issues] PM2.5 emission factors may be overestimated for some biomass and oil units These will be reviewed in future updates.
## transportation,domestic-aviation
### Added
- [Added] Data period extended for existing sources. Start_date 2015-01-01 to end_date 2026-08-31.
- [Added] Added coverage. 8 new sources added, based on International Air Transport Association (iata) code: {'iata_ALY', 'iata_DEZ', 'iata_DJT', 'iata_DTI', 'iata_GXM', 'iata_IAX', 'iata_JDR', 'iata_VEV'}
- [Added] New emissions-reducing solution: fleet renewal to current-generation aircraft (13% lower fuel burn per affected flight applied to each airport's previous-generation activity share).
### Changed
- [Changed] None
### Deprecated
- [Deprecated] None
### Fixed
- [Fixed] None
### Known Issues
- [Known Issues] None
## transportation,domestic-shipping
### Added
- [Added] Data period extended. Start_date 2015-01-01 to 2026-08-31.
### Changed
- [Changed] None
### Deprecated
- [Deprecated] None
### Fixed
- [Fixed] Extended port stays with large emissions are no longer showing up more than once for the same vessel
### Known Issues
- [Known Issues] OM Invalid transmissions can cause interpolation of trips over extended data gaps which may result in large erroneous emissions spikes at a port at the time when the data gap ends.
- [Known Issues] OM Attribution of emissions to ports as 50/50 on trips with significant loitering can cause emissions reductions assigned to a port that is greater than the emissions assigned to that port.
- [Known Issues] Extended port stays occasionally show up more than once for the same vessel, a fix has been implemented to mitigate this effect for port stays with large emissions but it still may be observed for some smaller port stays.
## transportation,international-aviation
### Added
- [Added] Data period extended for existing sources. Start_date 2015-01-01 to end_date 2026-08-31.
- [Added] Added coverage. 4 new sources added, based on International Air Transport Association (iata) code: {'iata_CAE', 'iata_DEZ', 'iata_DJT', 'iata_PLW'}.
- [Added] New emissions-reducing solution: fleet renewal to current-generation aircraft (13% lower fuel burn per affected flight applied to each airport's previous-generation activity share).
### Changed
- [Changed] None
### Deprecated
- [Deprecated] None
### Fixed
- [Fixed] None
### Known Issues
- [Known Issues] None
## transportation,international-shipping
### Added
- [Added] Data period extended. Start_date 2015-01-01 to 2026-08-31.
### Changed
- [Changed] None
### Deprecated
- [Deprecated] None
### Fixed
- [Fixed] Extended port stays with large emissions are no longer showing up more than once for the same vessel
### Known Issues
- [Known Issues] OM Invalid transmissions can cause interpolation of trips over extended data gaps which may result in large erroneous emissions spikes at a port at the time when the data gap ends
- [Known Issues] OM Attribution of emissions to ports as 50/50 on trips with significant loitering can cause emissions reductions assigned to a port that is greater than the emissions assigned to that port.
- [Known Issues] Extended port stays occasionally show up more than once for the same vessel, a fix has been implemented to mitigate this effect for port stays with large emissions but it still may be observed for some smaller port stays.
## transportation,road-transportation
- [Note] The changes marked "(from v5.11)" were included in the v5.11 data release but were left out of the v5.11 changelog. They are documented here for completeness.
### Added
- [Added] (from v5.11) Data period extended for existing sources. New end_date 2026-07-31.
### Changed
- [Changed] (from v5.11) Emissions factors within the USA were updated to use regional (state) vehicle fleet mix and fuel mix inventories.
- [Changed] (from v5.11) Incorporated temperature values from the latest CRU 4.10 dataset, which results in updated fuel efficiency and electrical consumption modifiers for 2025 and 2026.
### Deprecated
- [Deprecated] None
### Fixed
- [Fixed] (from v5.11) Within India, the fraction of vehicles represented by the LightDutyTruck and SingleUnitTruck classes was incorrectly zeroed out; this has now been corrected.
### Known Issues
- [Known Issues] Have not updated to the latest Climate TRACE patch of GADM data (v1.1.2).
- [Known Issues] Data has limited coverage for BEV/PHEV fuel mix information.
- [Known Issues] Data has limited regional-level vehicle fleet mix information, resulting in lack of regional variance outside of the USA.
### Removed
- [Removed] None
## waste,industrial-wastewater-treatment-and-discharge
### Added
- [Added] Data period extended for existing sources. Start_date 2026-01-01 to end_date 2026-08-31.
### Changed
- [Changed]
### Deprecated
- [Deprecated] None
### Fixed
- [Fixed] None
### Known Issues
- [Known Issues] Potential duplicate assets exist.
## waste,solid-waste-disposal
### Added
- [Added] Monthly estimates for July and August 2026 for all 13,656 assets and 252 countries (asset, confidence, uncertainty, and country data).
### Changed
- [Changed] None. Methodology and asset coverage are unchanged from the v5.10 08/03/26 submission. This release extends the existing time series by two months and does not revise any earlier month.
### Deprecated
- [Deprecated] None
### Fixed
- [Fixed] None
### Known Issues
- [Known Issues] Disjoint in the timeseries of some Russian assets, leading to an inflated YOY trend in Russia.
<img width="500" height="690" alt="image" src="https://github.com/user-attachments/assets/e9cd1a7b-697f-40e7-bd1e-8a4bed7d57c7" />
