# [5.13.0] - 2026-11-24
## ClimateTRACE,deprecation-warning
- None
## ClimateTRACE,multiple-sectors,post-processing
### Added
- [Added] None
### Changed
- [Changed] None
### Deprecated
- [Deprecated] None
### Fixed
- [Fixed] In V5.12.0, 2026 air pollutant emissions for forest-land-fires, shrubgrass-fires and wetland-fires were overstated: a full year of emissions was placed in January–March 2026. V5.13.0 corrects this. 2026 PM2.5 for forest-land-fires is now 5.6 Mt (previously 41.2 Mt), shrubgrass-fires 2.5 Mt and wetland-fires 0.2 Mt.
### Known Issues
- [Known Issues] None
## ClimateTRACE,individual-changelogs
## buildings,non-residential-onsite-fuel-usage
### Added
- [Added] Data period extended for existing sources. Start_date 2026-09-01 to end_date 2026-09-30.
### Changed
- [Changed] Updated historical data for existing sources. Start_date 2026-01-01 to end_date 2026-08-31.
### Deprecated
- [Deprecated] None
### Fixed
- [Fixed] None
### Known Issues
- [Known Issues] The residential/nonresidential split still relies on Global Human Settlement Layer (GHSL) data for defining which buildings are residential or nonresidential, even though the building volume itself now comes from TEMPO. The definition used by GHSL for this tends to label more building area as residential than nonresidential. This may introduce a bias towards attributing additional emissions as residential rather than nonresidential. This has been present in all previous versions of this subsector.
- [Known Issues] The emissions factors are back-calculated from a combination of emissions data (disaggregated EDGAR) and activity data. This leads to some emissions factors being well-outside of a standard range of values for those quantities. This has been present in all previous versions of this subsector.
- [Known Issues] Regional totals for some very small territories that border a much larger emitter can include part of the neighbour's emissions and exceed that territory's own national total. This arises because national totals are distributed across a fine grid and then summed back up by country, and border cells are not resolved identically in both steps. This is most pronounced for Macau, Hong Kong and Syria. This has been present in all previous versions of this subsector.
- [Known Issues] Our statistical data on several countries report no energy use at all of one fuel in one sector, so the corresponding energy and emissions are zero for those countries. This has been present in all previous versions of this subsector.
- [Known Issues] There are several cases of orphaned emissions (emissions with no corresponding activity) due to following the IPCC convention that most gases and pollutants except CO2 report both fossil and biomass emissions together since our activity basis is fossil activity, this leads to a mismatch. This also prevents activity x emissions factors from achieving full equality with emissions. However, the biomass activity data are now reported (other8) and can be used to correct this issue and back out the appropriate fossil or biomass emissions factors. This has been present in all previous versions of this subsector.
## buildings,residential-onsite-fuel-usage
### Added
- [Added] Data period extended for existing sources. Start_date 2026-09-01 to end_date 2026-09-30.
### Changed
- [Changed] Updated historical data for existing sources. Start_date 2026-01-01 to end_date 2026-08-31.
### Deprecated
- [Deprecated] None
### Fixed
- [Fixed] None
### Known Issues
- [Known Issues] The residential/nonresidential split still relies on Global Human Settlement Layer (GHSL) data for defining which buildings are residential or nonresidential, even though the building volume itself now comes from TEMPO. The definition used by GHSL for this tends to label more building area as residential than nonresidential. This may introduce a bias towards attributing additional emissions as residential rather than nonresidential. This has been present in all previous versions of this subsector.
- [Known Issues] The emissions factors are back-calculated from a combination of emissions data (disaggregated EDGAR) and activity data. This leads to some emissions factors being well-outside of a standard range of values for those quantities. This has been present in all previous versions of this subsector.
- [Known Issues] Regional totals for some very small territories that border a much larger emitter can include part of the neighbour's emissions and exceed that territory's own national total. This arises because national totals are distributed across a fine grid and then summed back up by country, and border cells are not resolved identically in both steps. This is most pronounced for Macau, Hong Kong and Syria. This has been present in all previous versions of this subsector.
- [Known Issues] Our statistical data on several countries report no energy use at all of one fuel in one sector, so the corresponding energy and emissions are zero for those countries. This has been present in all previous versions of this subsector.
- [Known Issues] There are several cases of orphaned emissions (emissions with no corresponding activity) due to following the IPCC convention that most gases and pollutants except CO2 report both fossil and biomass emissions together since our activity basis is fossil activity, this leads to a mismatch. This also prevents activity x emissions factors from achieving full equality with emissions. However, the biomass activity data are now reported (other8) and can be used to correct this issue and back out the appropriate fossil or biomass emissions factors. This has been present in all previous versions of this subsector.
## forestry-and-land-use,forest-land-clearing
### Added
- [Added] None
### Changed
- [Changed] None
### Deprecated
- [Deprecated] None
### Fixed
- [Fixed] Adjusted abnormal spikes in 2026 Q1.
### Known Issues
- [Known Issues] The 2026 quarterly emissions dataset utilizes CTrees 2026 land use change alert (LUCA) data as the basis for estimating disturbance-related emissions. The current 2026 quarterly emission estimates may not fully attribute specific disturbance types (deforestation, degradation, and fire) that occurred in 2026.
## forestry-and-land-use,forest-land-degradation
### Added
- [Added] None
### Changed
- [Changed] None
### Deprecated
- [Deprecated] None
### Fixed
- [Fixed] Adjusted abnormal spikes in 2026 Q1.
### Known Issues
- [Known Issues] The 2026 quarterly emissions dataset utilizes CTrees 2026 land use change alert (LUCA) data as the basis for estimating disturbance-related emissions. The current 2026 quarterly emission estimates may not fully attribute specific disturbance types (deforestation, degradation, and fire) that occurred in 2026.
## forestry-and-land-use,net-forest-land
### Added
- [Added] None
### Changed
- [Changed] Updated model for 2021-2025 data. Years after 2020 are built year on year from the 2020 base map. In non-forest and mixed pixels (forest cover below 50%), 2021-2025 carbon stock values are now aligned with the change since 2020 in the CTrees 100m biomass time series. Dense forest and all years up to 2020 are unchanged.
- [Changed] Activity and emissions rasters for all years were updated to reflect the changes.
### Deprecated
- [Deprecated] None
### Fixed
- [Fixed] Corrected cloud-related drops in 2024–2025 carbon stock values in the cloudy coastal forests of West and Central Africa and on the Andes slope. Pixels whose 1 km value fell sharply while the CTrees 100m series did not now follow the 100m change. Largest national effects on 2024 stock: Nigeria +8.3%, Liberia +6.2%, Gabon +4.7%, Republic of the Congo +3.7%, Cameroon +2.4%, Colombia +1.1%. Global stock 2024 and 2025: about +0.3%.
### Known Issues
- [Known Issues] None
## forestry-and-land-use,net-shrubgrass
### Added
- [Added] None
### Changed
- [Changed] Updated model for 2021-2025 data. Years after 2020 are built year on year from the 2020 base map. In non-forest and mixed pixels (forest cover below 50%), 2021-2025 carbon stock values are now aligned with the change since 2020 in the CTrees 100m biomass time series. Dense forest and all years up to 2020 are unchanged.
- [Changed] Activity and emissions rasters for all years were updated to reflect the changes.
### Deprecated
- [Deprecated] None
### Fixed
- [Fixed] Corrected cloud-related drops in 2024–2025 carbon stock values in the cloudy coastal forests of West and Central Africa and on the Andes slope. Pixels whose 1 km value fell sharply while the CTrees 100m series did not now follow the 100m change. Largest national effects on 2024 stock: Nigeria +8.3%, Liberia +6.2%, Gabon +4.7%, Republic of the Congo +3.7%, Cameroon +2.4%, Colombia +1.1%. Global stock 2024 and 2025: about +0.3%.
### Known Issues
- [Known Issues] None
## forestry-and-land-use,net-wetland
### Added
- [Added] None
### Changed
- [Changed] Updated model for 2021-2025 data. Years after 2020 are built year on year from the 2020 base map. In non-forest and mixed pixels (forest cover below 50%), 2021-2025 carbon stock values are now aligned with the change since 2020 in the CTrees 100m biomass time series. Dense forest and all years up to 2020 are unchanged.
- [Changed] Activity and emissions rasters for all years were updated to reflect the changes.
### Deprecated
- [Deprecated] None
### Fixed
- [Fixed] Corrected cloud-related drops in 2024–2025 carbon stock values in the cloudy coastal forests of West and Central Africa and on the Andes slope. Pixels whose 1 km value fell sharply while the CTrees 100m series did not now follow the 100m change. Largest national effects on 2024 stock: Nigeria +8.3%, Liberia +6.2%, Gabon +4.7%, Republic of the Congo +3.7%, Cameroon +2.4%, Colombia +1.1%. Global stock 2024 and 2025: about +0.3%.
### Known Issues
- [Known Issues] None
## forestry-and-land-use,removals
### Added
- [Added] None
### Changed
- [Changed] Updated model for 2021-2025 data. Years after 2020 are built year on year from the 2020 base map. In non-forest and mixed pixels (forest cover below 50%), 2021-2025 carbon stock values are now aligned with the change since 2020 in the CTrees 100m biomass time series. Dense forest and all years up to 2020 are unchanged.
- [Changed] Activity and emissions rasters for all years were updated to reflect the changes.
### Deprecated
- [Deprecated] None
### Fixed
- [Fixed] Corrected cloud-related drops in 2024–2025 carbon stock values in the cloudy coastal forests of West and Central Africa and on the Andes slope. Pixels whose 1 km value fell sharply while the CTrees 100m series did not now follow the 100m change. Largest national effects on 2024 stock: Nigeria +8.3%, Liberia +6.2%, Gabon +4.7%, Republic of the Congo +3.7%, Cameroon +2.4%, Colombia +1.1%. Global stock 2024 and 2025: about +0.3%.
### Known Issues
- [Known Issues] None
## forestry-and-land-use,water-reservoirs
### Added
- [Added] Data period extended for existing sources; added May through September 2026. End date is now September 30, 2026.
- [Added] A trophic state adjustment factor for the CH4 emissions factors, based on each reservoir’s seasonal median chlorophyll-a concentration. Chlorophyll-a is estimated from Sentinel-2 imagery using NASA STREAM: ACOLITE removes the atmospheric signal to give water-surface reflectance, and the Mixture Density Network (MDN), a neural network trained on paired field and satellite measurements, estimates chlorophyll-a per pixel and stays reliable in turbid or highly eutrophic water. See our methodology in the Climate TRACE GitHub repo: https://github.com/climatetracecoalition/emissions-methodology/tree/main/Sector-Methodologies/1-Sectors/forestry-and-land-use/reservoirs
### Changed
- [Changed] None
### Deprecated
- [Deprecated] None
### Fixed
- [Fixed] None
### Known Issues
- [Known Issues] Globally, emissions appear to jump between 2016 and 2017, which we currently attribute to the discrepancy in data sources - i.e., Landsat NDWI versus Sentinel-2 SCL.
## manufacturing,aluminum
### Added
- [Added] September 2026 data added
### Changed
- [Changed] None
### Deprecated
- [Deprecated] None
### Fixed
- [Fixed] None
### Known Issues
- [Known Issues] None
## manufacturing,cement
### Added
- [Added] New month added (September 2026).
### Changed
- [Changed] Full history (January 2021 – September 2026) resubmitted to apply the fixes below to all months.
### Deprecated
- [Deprecated] TZCMT2404000001096 removed. Global Energy Monitor confirmed it is a duplicate of TZCMT2404000002732 (Ningxia Guoda Cement Wuzhong Cement Plant).
### Fixed
- [Fixed] Corrected locations for TZCMT2404000000277, TZCMT2404000000278 and TZCMT2404000002732. These IDs now carry the coordinates and satellite readings of their Ningxia, China plants instead of the European plants previously linked to them. TZCMT2404000002733 was already correct.
- [Fixed] The European plants previously linked to these IDs (Skövde and Slite, Sweden; Wildegg and Cornaux, Switzerland) are reported under their own IDs.
### Known Issues
- [Known Issues] None
## manufacturing,iron-and-steel
### Added
- [Added] September 2026 data added
### Changed
- [Changed] None
### Deprecated
- [Deprecated] None
### Fixed
- [Fixed] None
### Known Issues
- [Known Issues] None
## power,electricity-generation
### Added
- [Added] Data period extended for existing sources. Start_date 2019-01-01 to end_date 2026-09-30.
### Changed
- [Changed] Extended condensable PM2.5 removal credit to all Flue-gas desulfurization (FGD) types, in addition to wet FGD, which was previously the only type credited for condensable removal. This can change primary PM2.5 emissions factors and estimates.
- [Changed] EIA 860m was updated to include the latest month. This can change emission estimates.
- [Changed] GEM biomass tracker was updated (September, 2026 version). This can change emission estimates.
- [Changed] Manually verified and updated plant/unit information (ex: plant locations, unit level information, etc). This can change emission estimates.
- [Changed] Pulled new most recent months from reported generation sources. These can reflect changes in our estimates.
### Deprecated
- [Deprecated] None
### Fixed
- [Fixed] Corrected how the turbine class is assigned to gas units in the carbon intensity model. Each unit now consistently gets its gas turbine class (matched to its combined- or simple-cycle configuration), fixing cases where the resulting emissions intensity could be assigned non-deterministically for a subset of gas-fired assets.
### Known Issues
- [Known Issues] For non-operational plants the data is reported as zero values for capacity, capacity factor, activity, emissions intensity, and emissions. The related uncertainties are also reported as zero. This is not strictly correct since there can be uncertainty in the operating status in a given month. Future work will better quantify the uncertainty when the plant is reported as non-operational.
- [Known Issues] Our remote sensing-based estimates of plant activity are biased low in some grid regions including China. We are working to address the bias in future releases.
- [Known Issues] PM2.5 emission factors may be overestimated for some biomass and oil units These will be reviewed in future updates.
## transportation,domestic-aviation
### Added
- [Added] Data period extended for existing sources. Start_date 2015-01-01 to end_date 2026-09-30.
- [Added] Added coverage. 4 new sources added: {'iata_AMC', 'iata_AYK', 'iata_CWF', 'iata_SXQ'}
### Changed
- [Changed] None
### Deprecated
- [Deprecated] None
### Fixed
- [Fixed] None
### Known Issues
- [Known Issues] None
## transportation,non-broadcasting-vessels
### Added
- [Added] Non-broadcasting estimates for July, August and September 2026, replacing the placeholder values (repeated June 2026 values) delivered in 080126, 090126 and 100126.
- [Added] NMVOC, PM2.5 and PM10 emissions (NMVOC_emissions_tonnes, PM2_5_emissions_tonnes, PM10_emissions_tonnes), added to the country, uncertainty and confidence files.
### Changed
- [Changed] Non-broadcasting vessel emissions are now estimated with a new random forest model (replacing the previous KNN-based model), trained on 2017-2026 Sentinel-1 detections and AIS emissions. The full series (2017-01-01 through 2026-09-30) is redelivered. See our methodology host on the Climate TRACE GitHub: https://github.com/climatetracecoalition/emissions-methodology/tree/main/Sector-Methodologies/1-Sectors/transportation/non-broadcasting-vessels
- [Changed] Uncertainty estimates recomputed for 2017-2025 with the new model.
### Deprecated
- [Deprecated] None
### Fixed
- [Fixed] None
### Known Issues
- [Known Issues] From July 2026, Sentinel-1 imagery comes from Sentinel-1C and 1D (two satellites, previously one). The added coverage raises non-broadcasting estimates by about 6% relative to single-satellite coverage.
- [Known Issues] Non-broadcasting emissions rise in 2026. This mirrors a drop in AIS-based emissions over the same period, so the combined total stays close to the previous year. The shift has two causes: (1) Iran conflict: since March 2026, many vessels in the Persian Gulf, Gulf of Oman and nearby waters have switched off their AIS, so their emissions now show up as non-broadcasting. (2) New AIS provider at GFW: since 22 April 2026, GFW’s new AIS feed (Kpler provider) receives less Dynamic AIS receiver positions, reducing broadcasting signals specially far from shore, so some activity is now captured by satellite data instead. The dark model is working as intended. Emissions just move from the broadcasting component to the non-broadcasting one, which is exactly what our fused approach is designed to handle, so the totals keep their normal trends.
## transportation,domestic-shipping
### Added
- [Added] Data period extended. Start_date 2026-09-01 to 2026-09-30.
### Changed
- [Changed] None
### Deprecated
- [Deprecated] None
### Fixed
- [Fixed] None
### Known Issues
- [Known Issues] OM Invalid transmissions can cause interpolation of trips over extended data gaps which may result in large erroneous emissions spikes at a port at the time when the data gap ends
- [Known Issues] OM Attribution of emissions to ports as 50/50 on trips with significant loitering can cause emissions reductions assigned to a port that is greater than the emissions assigned to that port
- [Known Issues] Extended port stays occasionally show up more than once for the same vessel, a fix has been implemented to mitigate this effect for port stays with large emissions but it still may be observed for some smaller port stays.
## transportation,international-aviation
### Added
- [Added] Data period extended for existing sources. Start_date 2015-01-01 to end_date 2026-09-30.
- [Added] Added coverage. 3 new sources added: {'iata_BFN', 'iata_CPS', 'iata_GAJ'}
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
- [Added] Data period extended. Start_date 2026-09-01 to 2026-09-30.
### Changed
- [Changed] None
### Deprecated
- [Deprecated] None
### Fixed
- [Fixed] None
### Known Issues
- [Known Issues] OM Invalid transmissions can cause interpolation of trips over extended data gaps which may result in large erroneous emissions spikes at a port at the time when the data gap ends
- [Known Issues] OM Attribution of emissions to ports as 50/50 on trips with significant loitering can cause emissions reductions assigned to a port that is greater than the emissions assigned to that port
- [Known Issues] Extended port stays occasionally show up more than once for the same vessel, a fix has been implemented to mitigate this effect for port stays with large emissions but it still may be observed for some smaller port stays.
## transportation,road-transportation
### Added
- [Added] Data period extended for existing sources. New end_date 2026-09-30.
- [Added] Added spatial interpolation for EV inventories, using a nearest neighbor approach with ClimateTRACE GADM boundaries. When no neighbors are found, we default to using the average of the corresponding UN Region.
### Changed
- [Changed] Emissions factors updated for various countries by updating data sources to include BEV/PHEV fuel type inventories. For all updated data sources, a larger proportion of BEV/PHEVs are reported, leading to a trend of emissions reductions across a number of countries. Notable affected countries include POL, THA, RUS, AUS, CHN, TWN, JPN, KOR.
- [Changed] Replaced constant-value backfilling of historical BEV/PHEV inventory values with an exponential model. This approach better represents the rapid growth in EV adoption while reducing the risk of overestimating EV values in earlier years.
### Deprecated
- [Deprecated] None
### Fixed
- [Fixed] None
### Known Issues
- [Known Issues] Have not updated to the latest Climate TRACE patch of GADM data (v1.1.2).
- [Known Issues] Data has limited coverage for BEV/PHEV fuel mix information.
- [Known Issues] Data has limited regional-level vehicle fleet mix information, resulting in lack of regional variance outside of the USA.
## waste,domestic-wastewater-treatment-and-discharge
### Added
- [Added] Data period extended for existing sources. Start_date 2015-01-01 to end_date 2026-08-31.
### Changed
- [Changed] Sanitation pathway percentages (e.g., "sewer", "septic") changed with update to latest WASH survey data release.
### Deprecated
- [Deprecated] None
### Fixed
- [Fixed] None
### Known Issues
- [Known Issues] All wastewater treatment plants in the set of 5,403 new satellite-identified assets are assumed to treat domestic wastewater. Industrial wastewater treatment plants and water purification facilities have not been filtered out, which will lead to an overestimate in asset emissions, in some cases causing the sum of asset-level emissions for a country to exceed estimated country-level emissions.
- [Known Issues] Inconsistent year-over-year population values for Kiribati in the underlying population source data are carried forward into country-level emissions estimates. To be addressed in a future release.
- [Known Issues] The dilution factor column (other1) relies on HydroWASTE values and will remain blank for non-HydroWASTE assets.
