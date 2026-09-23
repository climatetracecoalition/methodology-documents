# [5.11.0] - 2026-09-23

## ClimateTRACE,deprecation-warning

- The ‘other-fossil-fuel-operations’ subsector has been deprecated, as
coal-mining, oil-and-gas-production, and oil-and-gas-transport will
include all of the emissions previously captured by this subsector.

## ClimateTRACE,multiple-sectors,post-processing

### Added

- [Added] None

### Changed

- [Changed] Non-team-submitted PM2.5 emissions data were generated
using a new methodology that incorporates higher asset-level
specificity, related to combustion/flaring/process/etc. splits. Affects
all sectors *except* the following: cropland-fires, domestic-shipping,
electricity-generation, international-shipping,
non-residential-onsite-fuel-usage, residential-onsite-fuel-usage, and
road-transportation.

### Deprecated

- [Deprecated] None

### Fixed

- [Fixed] None

### Known Issues

- [Known Issues] None

## ClimateTRACE,individual-changelogs

## agriculture,enteric-fermentation-cattle-operation

### Added

- [Added] Indonesia (IDN) asset-level emissions for years 2015 to
2025. Total heads of cattle are based on 2024 province-level data and
backfilled to 2015.

- [Added] 2025 emissions estimates for all individual cattle
operations.

- [Added] 2025 county level emission estimates.

### Changed

- [Changed] Current V5.11 coverage = 41 countries and an estimated
285,824 cattle operations (assets) identified. Previous V5.10 coverage =
40 countries and an estimated 285,517 cattle operations (assets)
identified.

- [Changed] Imputed missing state counts for US beef and dairy cattle
using U.S. Department of Agriculture (USDA) regional averages (if
available), falling back to national averages. This includes estimating
total heads of beef and dairy cattle, and estimating beef capacity
factors.

- [Changed] Updated Australian and Canadian beef/dairy cattle
estimates from national to territory/province-level averages. This
includes estimating total heads of beef and dairy cattle, and estimating
beef capacity factors.

### Deprecated

- [Deprecated] None

### Fixed

- [Fixed] V5.10 may be missing cattle operation coverage in some
counties, i.e. RUS, UKR, POL, and GBR. This has been fixed in V5.11.

- [Fixed] Operations that were assigned, solid storage manure
management were silently skipped last release, V5.10. As a result,
enteric fermentation emissions were not estimated for these operations.
This has been fixed in V5.11.

### Known Issues

- [Known Issues] AUS country-level emissions jump after 2019. This is
because the mean dairy cattle count applied to identified operations is
derived from two datasets whose reported year coverage doesn't overlap.
As a result, 2015–2018 show a lower mean dairy cattle count relative to
2019 onward. This will be fixed in a future release.

- [Known Issues] Effort has been made to reduce duplicate operations
in the U.S. and globally. In the U.S. this was caused when a reported
state government CAFOs had location coordinates set away from the
operation not within the operation. For example, at the end of the CAFO
driveway leading into the operation or the owners home away from the
CAFO. Further work will continue to deduplicate Climate TRACE cattle
operations in the U.S.

- [Known Issues] Duplicates and false-positive locations can exist
for this sector. If found, please let us know via email and provide the
asset id and latitude and longitude information.

- [Known Issues] Certain cattle operations may be multiple cattle
operations combined into one. As a result, the regression model
overestimated the total head of cattle at these operations. Any beef
cattle operation with a total head (capacity) greater than 40,000 had
their capacity capped at 40,000. Additionally, any dairy farm operation
with a total head (capacity) greater than 4,000 had their capacity
capped at 4,000. These are marked in the ‘other2’ column. Future updates
will address this issue.

## agriculture,manure-management-cattle-operation

### Added

- [Added] Indonesia (IDN) asset-level emissions for years 2015 to
2025. Total heads of cattle are based on 2024 province-level data and
backfilled to 2015.

- [Added] 2025 emissions estimates for all individual cattle
operations.

- [Added] 2025 county level emission estimates.

### Changed

- [Changed] Updated underlying dataset to estimate climate zones to
the Climatic Research Unit gridded Time Series (CRU TS) v4.10 NetCDF
files (version June 7, 2026) from the University of East Anglia. CRU TS
v4.10 was used to estimate monthly climate zones for years 2015 to 2025.

- [Changed] Current V5.11 coverage = 41 countries and an estimated
285,824 cattle operations (assets) identified. Previous V5.10 coverage =
40 countries and an estimated 285,517 cattle operations (assets)
identified.

- [Changed] Imputed missing state counts for US beef and dairy cattle
using U.S. Department of Agriculture (USDA) regional averages (if
available), falling back to national averages. This includes estimating
total heads of beef and dairy cattle, and estimating beef capacity
factors.

- [Changed] Updated Australian and Canadian beef/dairy cattle
estimates from national to territory/province-level averages. This
includes estimating total heads of beef and dairy cattle, and estimating
beef capacity factors.

### Deprecated

- [Deprecated] None

### Fixed

- [Fixed] V5.10 may be missing cattle operation coverage in some
counties, i.e. RUS, UKR, POL, and GBR. This has been fixed in V5.11.

- [Fixed] Fixed ef4 assignment to include wet climate values.
Previously, dry climate values were assigned. This affects N2O emissions
derived for locations in wet climates.

- [Fixed] N2O emissions for cattle operations using pasture
management in multiple manure management systems (specifically in
Western countries like AUS, CAN, and NZL) may have been omitted in
V5.10. This has been resolved in V5.11.

- [Fixed] Operations that were assigned, solid storage manure
management were silently skipped last release, V5.10. As a result,
manure emissions were not estimated for these operations. This has been
fixed in V5.11.

### Known Issues

- [Known Issues] AUS country-level emissions jump after 2019. This is because the mean dairy cattle count applied to identified operations is derived from two datasets whose reported year coverage doesn't overlap. As a result, 2015–2018 show a lower mean dairy cattle count relative to 2019 onward. This will be fixed in a future release.

- [Known Issues] Effort has been made to reduce duplicate operations
in the U.S. and globally. In the U.S. this was caused when a reported
state government CAFOs had location coordinates set away from the
operation not within the operation. For example, at the end of the CAFO
driveway leading into the operation or the owners home away from the
CAFO. Further work will continue to deduplicate Climate TRACE cattle
operations in the U.S.

- [Known Issues] Duplicates and false-positive locations can exist
for this sector. If found, please let us know via email and provide the
asset id and latitude and longitude information.

- [Known Issues] Certain cattle operations may be multiple cattle
operations combined into one. As a result, the regression model
overestimated the total head of cattle at these operations. Any beef
cattle operation with a total head (capacity) greater than 40,000 had
their capacity capped at 40,000. Additionally, any dairy farm operation
with a total head (capacity) greater than 4,000 had their capacity
capped at 4,000. These are marked in the ‘other2’ column. Future updates
will address this issue.

- [Known Issues] Manure emissions in conflict-affected regions with
large cattle populations (e.g., Afghanistan, East Africa) may
overestimate emissions due to IPCC 2019 animal waste management system
regional defaults assigned. Future updates will implement
country-specific MMS to resolve this issue.

- [Known Issues] Current country-level manure emissions assume a
single climate zone and one multiple MMS type per cattle category
(beef/dairy), potentially biasing CH4 and N2O emissions’ estimates,
especially in temperate climates (i.e. Russia and Canada) where CH4
production is reduced in cooler/temperate climates. Future updates will
improve accuracy by implementing multi-MMS allocations and refined
country-specific climate zones.

## agriculture,net-soil-organic-carbon

### Added

- [Added] None

### Changed

- [Changed] None

### Deprecated

- [Deprecated] None

### Fixed

- [Fixed] None

### Known Issues

- [Known Issues] Asset-level activity values (tonnes change in soil
organic carbon) for CH4 and N2O are incorrectly set to 0 across the
board. For true activity values, users are pointed to the CO2 rows,
which represent the true SOC change. To be fixed in V5.12.0.

- [Known Issues] GADM and city aggregation asset_activity,
emissions_factor, and capacity_factor are incorrect. To be fixed in
V5.12.0.

## agriculture,rice-cultivation

### Added

- [Added] Monthly disaggregation for 2021-2024 used the pattern of
rice production modeled in 2025.

- [Added] Rice production data (SPAM 2020) appended as a new other4
field to 2021-2024, matched to assets at the GADM2 level and aggregated
by summation to GADM1 and GADM0 assets. This data is not broken down to
monthly values but appears as yearly values (rice yield per year for a
given area).

- [Added] Coverage to 58 countries.

### Changed

- [Changed] None

### Deprecated

- [Deprecated] None

### Removed

### Fixed

- [Fixed] Corrected the emissions factor for North Korea (PRK) which
lowered emissions going back to 2021.

- [Fixed] Corrected 2021-2024 production in China where northwestern
provinces had misclassified other crops as rice. Validated this finding
using external estimates and reported values.

### Known Issues

- [Known Issues] 2021-2024 monthly data is not directly modeled, but
extrapolated based on 2025 patterns. A future release will likely more
directly model these values historically.

## buildings,non-residential-onsite-fuel-usage

### Added

- [Added] Data period extended for existing sources. Start_date
2026-07-01 to end_date 2026-07-31.

- [Added] Energy use intensity (capacity factor) is now delivered as
annual layers. Start_date 2015-01-01 to end_date 2026-12-31.

- [Added] Biomass energy is now delivered as its own activity layer
(other8), separate from the main activity layer. Start_date 2015-01-01
to end_date 2026-07-31.

- [Added] A biomass PM2.5 emissions factor is now delivered (other7).
Start_date 2015-01-01 to end_date 2026-07-31.

### Changed

- [Changed] Updated historical data for existing sources. Start_date
2015-01-01 to end_date 2026-06-30.

- [Changed] Building activity is now estimated with Microsoft TEMPO
data. TEMPO supplies the building volume from which floor area is
derived (previously the Global Human Settlement Layer volume data); The
Global Human Settlement Layer data are still used only to classify the
proportion of floor area in each grid cell between residential and
nonresidential buildings, and to estimate the year-to-year growth of
buildings for years TEMPO does not observe. Start_date 2015-01-01 to
end_date 2026-12-31.

- [Changed] Energy use intensity (capacity factor) is now delivered
as annual layers. Energy use intensity was rebuilt from national energy
statistics and is now reported separately for fossil fuel and for
biomass, in each of the residential and nonresidential sectors, for
every year. The values are drawn from the U.S. Energy Information
Administration (EIA), the United Nations Statistics Division (UNSD), the
Africa Energy Database (AFREC) and the UN Food and Agriculture
Organization (FAOSTAT). One result is a shift in the balance between
residential and nonresidential emissions for most locations. Start_date
2015-01-01 to end_date 2026-07-31.

- [Changed] Biomass is now separated from fossil fuel at the energy
use intensity level, so biomass and fossil energy are estimated
independently as are the corresponding emissions. IPCC conventions are
followed regarding whether emissions totals include only fossil
emissions (as for CO2) or both fossil and biomass emissions (for other
gases and pollutants). Start_date 2015-01-01 to end_date 2026-07-31.

- [Changed] Emissions were re-estimated against the EDGAR 2025
release, which revises residential and other-sectors emissions for most
gases. Start_date 2015-01-01 to end_date 2026-07-31.

### Deprecated

- [Deprecated] The biomass CO2, CH4 and N2O emissions layers
(previously other7, other8 and other9) are no longer delivered. While
other7 and other8 have been reassigned, other9 has been deprecated and
is no longer used. Start_date 2015-01-01 to end_date 2026-07-31.

### Fixed

- [Fixed] Resolved issue with orphaned emissions (grid cells with
nonzero emissions and zero activity) that impacted a minor fraction of
global emissions. Start_date 2015-01-01 to end_date 2026-07-31.

- [Fixed] Resolved a 1-cell (~1km) grid shift for several countries
and pollutants. Start_date 2015-01-01 to end_date 2026-07-31.

### Known Issues

- [Known Issues] The residential/nonresidential split still relies on
Global Human Settlement Layer (GHSL) data for defining which buildings
are residential or nonresidential, even though the building volume
itself now comes from TEMPO. The definition used by GHSL for this tends
to label more building area as residential than nonresidential. This may
introduce a bias towards attributing additional emissions as residential
rather than nonresidential. This has been present in all previous
versions of this subsector.

- [Known Issues] The emissions factors are back-calculated from a
combination of emissions data (disaggregated EDGAR) and activity data.
This leads to some emissions factors being well-outside of a standard
range of values for those quantities. This has been present in all
previous versions of this subsector.

- [Known Issues] Regional totals for some very small territories that
border a much larger emitter can include part of the neighbour's
emissions and exceed that territory's own national total. This arises
because national totals are distributed across a fine grid and then
summed back up by country, and border cells are not resolved identically
in both steps. This is most pronounced for Macau, Hong Kong and Syria.
This has been present in all previous versions of this subsector.

- [Known Issues] Our statistical data on several countries report no
energy use at all of one fuel in one sector, so the corresponding energy
and emissions are zero for those countries. This has been present in all
previous versions of this subsector.

- [Known Issues] There are several cases of orphaned emissions
(emissions with no corresponding activity) due to following the IPCC
convention that most gases and pollutants except CO2 report both fossil
and biomass emissions together since our activity basis is fossil
activity, this leads to a mismatch. This also prevents activity x
emissions factors from achieving full equality with emissions. However,
the biomass activity data are now reported (other8) and can be used to
correct this issue and back out the appropriate fossil or biomass
emissions factors. This has been present in all previous versions of
this subsector.

## buildings,residential-onsite-fuel-usage

### Added

- [Added] Data period extended for existing sources. Start_date
2026-07-01 to end_date 2026-07-31.

- [Added] Energy use intensity (capacity factor) is now delivered as
annual layers. Start_date 2015-01-01 to end_date 2026-12-31.

- [Added] Biomass energy is now delivered as its own activity layer
(other8), separate from the main activity layer. Start_date 2015-01-01
to end_date 2026-07-31.

- [Added] A biomass PM2.5 emissions factor is now delivered (other7).
Start_date 2015-01-01 to end_date 2026-07-31.

### Changed

- [Changed] Updated historical data for existing sources. Start_date
2015-01-01 to end_date 2026-06-30.

- [Changed] Building activity is now estimated with Microsoft TEMPO
data. TEMPO supplies the building volume from which floor area is
derived (previously the Global Human Settlement Layer volume data); The
Global Human Settlement Layer data are still used only to classify the
proportion of floor area in each grid cell between residential and
nonresidential buildings, and to estimate the year-to-year growth of
buildings for years TEMPO does not observe. Start_date 2015-01-01 to
end_date 2026-12-31.

- [Changed] Energy use intensity (capacity factor) is now delivered
as annual layers. Energy use intensity was rebuilt from national energy
statistics and is now reported separately for fossil fuel and for
biomass, in each of the residential and nonresidential sectors, for
every year. The values are drawn from the U.S. Energy Information
Administration (EIA), the United Nations Statistics Division (UNSD), the
Africa Energy Database (AFREC) and the UN Food and Agriculture
Organization (FAOSTAT). One result is a shift in the balance between
residential and nonresidential emissions for most locations. Start_date
2015-01-01 to end_date 2026-07-31.

- [Changed] Biomass is now separated from fossil fuel at the energy
use intensity level, so biomass and fossil energy are estimated
independently as are the corresponding emissions. IPCC conventions are
followed regarding whether emissions totals include only fossil
emissions (as for CO2) or both fossil and biomass emissions (for other
gases and pollutants). Start_date 2015-01-01 to end_date 2026-07-31.

- [Changed] Emissions were re-estimated against the EDGAR 2025
release, which revises residential and other-sectors emissions for most
gases. Start_date 2015-01-01 to end_date 2026-07-31.

### Deprecated

- [Deprecated] The biomass CO2, CH4 and N2O emissions layers
(previously other7, other8 and other9) are no longer delivered. While
other7 and other8 have been reassigned, other9 has been deprecated and
is no longer used. Start_date 2015-01-01 to end_date 2026-07-31.

### Fixed

- [Fixed] Resolved issue with orphaned emissions (grid cells with
nonzero emissions and zero activity) that impacted a minor fraction of
global emissions. Start_date 2015-01-01 to end_date 2026-07-31.

- [Fixed] Resolved a 1-cell (~1km) grid shift for several countries
and pollutants. Start_date 2015-01-01 to end_date 2026-07-31.

### Known Issues

- [Known Issues] The residential/nonresidential split still relies on
Global Human Settlement Layer (GHSL) data for defining which buildings
are residential or nonresidential, even though the building volume
itself now comes from TEMPO. The definition used by GHSL for this tends
to label more building area as residential than nonresidential. This may
introduce a bias towards attributing additional emissions as residential
rather than nonresidential. This has been present in all previous
versions of this subsector.

- [Known Issues] The emissions factors are back-calculated from a
combination of emissions data (disaggregated EDGAR) and activity data.
This leads to some emissions factors being well-outside of a standard
range of values for those quantities. This has been present in all
previous versions of this subsector.

- [Known Issues] Regional totals for some very small territories that
border a much larger emitter can include part of the neighbour's
emissions and exceed that territory's own national total. This arises
because national totals are distributed across a fine grid and then
summed back up by country, and border cells are not resolved identically
in both steps. This is most pronounced for Macau, Hong Kong and Syria.
This has been present in all previous versions of this subsector.

- [Known Issues] Our statistical data on several countries report no
energy use at all of one fuel in one sector, so the corresponding energy
and emissions are zero for those countries. This has been present in all
previous versions of this subsector.

- [Known Issues] There are several cases of orphaned emissions
(emissions with no corresponding activity) due to following the IPCC
convention that most gases and pollutants except CO2 report both fossil
and biomass emissions together since our activity basis is fossil
activity, this leads to a mismatch. This also prevents activity x
emissions factors from achieving full equality with emissions. However,
the biomass activity data are now reported (other8) and can be used to
correct this issue and back out the appropriate fossil or biomass
emissions factors. This has been present in all previous versions of
this subsector.

## forestry-and-land-use,forest-land-clearing

### Added

- [Added] None

### Changed

- [Changed] Updated 2026 Q1 emissions estimates using the newly
updated 2025 emissions from 08/21/26 as baseline.

- [Changed] Updated emission factors for all emission types and
revised disturbance masking. Fire masking was changed from Global Annual
Burned Area Map (GABAM; Landsat product) product to MODIS Burned Area
(MCD64) and Global Forest Loss Due to Fire (GFL; Hansen, Univ. Of
Maryland GFC). While deforestation and degradation masking in the
tropical region was updated to use CTrees Integrated Deforestation,
Degradation, and Regeneration (CIDDR) data. And the deforestation
masking in the non-tropical region still sources from Global Forest Loss
(Hansen, Univ. Of Maryland GFC). The annual dataset covers 2015-01-01 to
2025-12-31, and the quarterly dataset covers 2023-01-01 to 2025-12-31.

- [Changed] Fire masking was changed from GABAM to MCD64 and GFL,
while deforestation and degradation masking was updated to use CTrees
Integrated Deforestation, Degradation, and Regeneration data. The annual
dataset covers 2015-01-01 to 2025-12-31, and the quarterly dataset
covers 2023-01-01 to 2025-12-31.

- [Changed] Updated 2025 quarterly emissions estimates using newly
available 2025 annual disturbance masks from the CTrees Integrated
Deforestation, Degradation, and Regeneration (CIDDR) dataset and Forest
Loss from Global Forest Change (Hansen, Univ. Of Maryland GFC).

### Deprecated

- [Deprecated] None

### Fixed

- [Fixed] None

### Known Issues

- [Known Issue] The 2026 quarterly emissions dataset utilizes CTrees
2026 land use change alert (LUCA) data as the basis for estimating
disturbance-related emissions. The current 2026 quarterly emission
estimates may not fully attribute specific disturbance types
(deforestation, degradation, and fire) that occurred in 2026.

- [Known Issue] Unrealistic spike in emissions in Jan 2026 for over
50 USA assets.

## forestry-and-land-use,forest-land-degradation

### Added

- [Added] None

### Changed

- [Changed] Updated 2026 Q1 emissions estimates using the newly
updated 2025 emissions from 08/21/26 as baseline.

- [Changed] Updated emission factors for all emission types and
revised disturbance masking. Fire masking was changed from Global Annual
Burned Area Map (GABAM; Landsat product) product to MODIS Burned Area
(MCD64) and Global Forest Loss Due to Fire (GFL; Hansen, Univ. Of
Maryland GFC). While deforestation and degradation masking in the
tropical region was updated to use CTrees Integrated Deforestation,
Degradation, and Regeneration (CIDDR) data. And the deforestation
masking in the non-tropical region still sources from Global Forest Loss
(Hansen, Univ. Of Maryland GFC). The annual dataset covers 2015-01-01 to
2025-12-31, and the quarterly dataset covers 2023-01-01 to 2025-12-31.

- [Changed] Updated 2025 quarterly emissions estimates using newly
available 2025 annual disturbance masks from the CTrees Integrated
Deforestation, Degradation, and Regeneration (CIDDR) dataset and Forest
Loss from Global Forest Change (Hansen, Univ. Of Maryland GFC).

### Deprecated

- [Deprecated] None

### Fixed

- [Fixed] None

### Known Issues

- [Known Issue] The 2026 quarterly emissions dataset utilizes CTrees
2026 land use change alert (LUCA) data as the basis for estimating
disturbance-related emissions. The current 2026 quarterly emission
estimates may not fully attribute specific disturbance types
(deforestation, degradation, and fire) that occurred in 2026.

## forestry-and-land-use,forest-land-fires

### Added

- [Added] None

### Changed

- [Changed] Updated 2026 Q1 emissions estimates using the newly
updated 2025 emissions from 08/21/26 as baseline.

- [Changed] Updated emission factors for all emission types and
revised disturbance masking. Fire masking was changed from Global Annual
Burned Area Map (GABAM; Landsat product) product to MODIS Burned Area
(MCD64) and Global Forest Loss Due to Fire (GFL; Hansen, Univ. Of
Maryland GFC). While deforestation and degradation masking in the
tropical region was updated to use CTrees Integrated Deforestation,
Degradation, and Regeneration (CIDDR) data,the deforestation masking in
the non-tropical region still sources from Global Forest Loss (Hansen,
Univ. Of Maryland GFC). The annual dataset covers 2015-01-01 to
2025-12-31, and the quarterly dataset covers 2023-01-01 to 2025-12-31.

- [Changed] Updated 2025 quarterly emissions estimates using newly
available 2025 annual disturbance masks from the CTrees Integrated
Deforestation, Degradation, and Regeneration (CIDDR) dataset and Forest
Loss from Global Forest Change (Hansen, Univ. Of Maryland GFC).

### Deprecated

- [Deprecated] None

### Fixed

- [Fixed] None

### Known Issues

- [Known Issue] The 2026 quarterly emissions dataset utilizes CTrees
2026 land use change alert (LUCA) data as the basis for estimating
disturbance-related emissions. The current 2026 quarterly emission
estimates may not fully attribute specific disturbance types
(deforestation, degradation, and fire) that occurred in 2026.

## forestry-and-land-use,net-forest-land

### Added

- [Added] None

### Changed

- [Changed] The Copernicus land cover input was updated from the 2019
map to the 2015 map to align with the starting point of our project's
time series (2015–current_year). Because Copernicus land cover data is
only available for the 2015–2019 period, utilizing the 2015 baseline
ensures that all subsequent emissions, removals, and net sector rasters
are evaluated consistently from the origin year onward. This prevents
backward projections onto earlier years and maintains methodological
integrity across the entire 2015–current_year analysis window.

### Deprecated

- [Deprecated] None

### Fixed

- [Fixed] None

### Known Issues

- [Known Issues] None

## forestry-and-land-use,net-shrubgrass

### Added

- [Added] None

### Changed

- [Changed] The Copernicus land cover input was updated from the 2019
map to the 2015 map to align with the starting point of our project's
time series (2015–current_year). Because Copernicus land cover data is
only available for the 2015–2019 period, utilizing the 2015 baseline
ensures that all subsequent emissions, removals, and net sector rasters
are evaluated consistently from the origin year onward. This prevents
backward projections onto earlier years and maintains methodological
integrity across the entire 2015–current_year analysis window.

### Deprecated

- [Deprecated] None

### Fixed

- [Fixed] None

### Known Issues

- [Known Issues] None

## forestry-and-land-use,net-wetland

### Added

- [Added] None

### Changed

- [Changed] The Copernicus land cover input was updated from the 2019
map to the 2015 map to align with the starting point of our project's
time series (2015–current_year). Because Copernicus land cover data is
only available for the 2015–2019 period, utilizing the 2015 baseline
ensures that all subsequent emissions, removals, and net sector rasters
are evaluated consistently from the origin year onward. This prevents
backward projections onto earlier years and maintains methodological
integrity across the entire 2015–current_year analysis window.

### Deprecated

- [Deprecated] None

### Fixed

- [Fixed] None

### Known Issues

- [Known Issues] None

## forestry-and-land-use,removals

### Added

- [Added] None

### Changed

- [Changed] The Copernicus land cover input was updated from the 2019
map to the 2015 map to align with the starting point of our project's
time series (2015–current_year). Because Copernicus land cover data is
only available for the 2015–2019 period, utilizing the 2015 baseline
ensures that all subsequent emissions, removals, and net sector rasters
are evaluated consistently from the origin year onward. This prevents
backward projections onto earlier years and maintains methodological
integrity across the entire 2015–current_year analysis window.

### Deprecated

- [Deprecated] None

### Fixed

- [Fixed] None

### Known Issues

- [Known Issues] None

## forestry-and-land-use,shrubgrass-fires

### Added

- [Added] None

### Changed

- [Changed] Updated 2026 Q1 emissions estimates using the newly
updated 2025 emissions from 08/21/26 as baseline.

- [Changed] Updated emission factors for all emission types and
revised disturbance masking. Fire masking was changed from Global Annual
Burned Area Map (GABAM; Landsat product) product to MODIS Burned Area
(MCD64) and Global Forest Loss Due to Fire (GFL; Hansen, Univ. Of
Maryland GFC). While deforestation and degradation masking in the
tropical region was updated to use CTrees Integrated Deforestation,
Degradation, and Regeneration (CIDDR) data, the deforestation masking in
the non-tropical region still sources from Global Forest Loss (Hansen,
Univ. Of Maryland GFC). The annual dataset covers 2015-01-01 to
2025-12-31, and the quarterly dataset covers 2023-01-01 to 2025-12-31.

- [Changed] Updated 2025 quarterly emissions estimates using newly
available 2025 annual disturbance masks from the CTrees Integrated
Deforestation, Degradation, and Regeneration (CIDDR) dataset and Forest
Loss from Global Forest Change (Hansen, Univ. Of Maryland GFC).

### Deprecated

- [Deprecated] None

### Fixed

- [Fixed] None

### Known Issues

- [Known Issue] The 2026 quarterly emissions dataset utilizes CTrees
2026 land use change alert (LUCA) data as the basis for estimating
disturbance-related emissions. The current 2026 quarterly emission
estimates may not fully attribute specific disturbance types
(deforestation, degradation, and fire) that occurred in 2026.

## forestry-and-land-use,wetland-fires

### Added

- [Added] None

### Changed

- [Changed] Updated 2026 Q1 emissions estimates using the newly
updated 2025 emissions from 08/21/26 as baseline.

- [Changed] Updated emission factors for all emission types and
revised disturbance masking. Fire masking was changed from Global Annual
Burned Area Map (GABAM; Landsat product) product to MODIS Burned Area
(MCD64) and Global Forest Loss Due to Fire (GFL; Hansen, Univ. Of
Maryland GFC). While deforestation and degradation masking in the
tropical region was updated to use CTrees Integrated Deforestation,
Degradation, and Regeneration (CIDDR) data, the deforestation masking in
the non-tropical region still sources from Global Forest Loss (Hansen,
Univ. Of Maryland GFC). The annual dataset covers 2015-01-01 to
2025-12-31, and the quarterly dataset covers 2023-01-01 to 2025-12-31.

- [Changed] Updated 2025 quarterly emissions estimates using newly
available 2025 annual disturbance masks from the CTrees Integrated
Deforestation, Degradation, and Regeneration (CIDDR) dataset and Forest
Loss from Global Forest Change (Hansen, Univ. Of Maryland GFC).

### Deprecated

- [Deprecated] None

### Fixed

- [Fixed] None

### Known Issues

- [Known Issue] The 2026 quarterly emissions dataset utilizes CTrees
2026 land use change alert (LUCA) data as the basis for estimating
disturbance-related emissions. The current 2026 quarterly emission
estimates may not fully attribute specific disturbance types
(deforestation, degradation, and fire) that occurred in 2026.

## fossil-fuel-operations,coal-mining

### Added

- [Added] Added ch4 and n2o fuel combustion emissions estimates to
the other columns (other8 and other9, respectively), which replaced
values for prior columns: Total Resource (Inferred, Indicated, Measured)
and Primary Consumer, Destination Name. This data is still accessible
via the GEM website for those interested.

- [Added] Updated the terajoule (TJ) fuel to tonnes of coal
production ratio for India based on updated United Nations Framework
Convention on Climate Change (UNFCCC) data. Emissions decreased 4.5% in
India as compared to V5.10.0.

### Changed

- [Changed] None

### Deprecated

- [Deprecated] None

### Fixed

- [Fixed] None

### Known Issues

- [Known Issues] None

## fossil-fuel-operations,oil-and-gas-production

### Added

- [Added] Data period calculated for all sources to the end of May
2026.

- [Added] CO2 emissions source percentage breakout between combustion
(the burning of fuels onsite to either generate electricity or directly
power various processes), fugitives, flaring, and venting. Saved to
columns ‘other2’, ‘other3’, ‘other4’, and ‘other5’, respectively.

- [Added] Greater coverage in the United States to include smaller
assets both in states with large production volumes and newly covered
states with low production volumes.

### Changed

- [Changed] For assets in the United States, our primary data
provider has incomplete production data for 2025 and 2026. For 2025 and
2026, United States data is duplicated from 2024 due to this lack of
data.

- [Changed] Lag changed to 2 months to match other sectors due to the
ease of copying earlier years.

- [Changed] Emissions intensity calculation methodology has changed
to reduce variability and uncertainty. Further explanation can be found
in methodology documentation for the oil and gas production and
transportation sectors.

- [Changed] Some aggregation of assets outside of the United States
changed to better account for similarities within the sector and data
privacy requirements.

- [Changed] Grid electricity emissions not included in emissions.

### Fixed

- [Fixed] Anomalous NMVOC emissions values in BIH corrected.

### Known Issues

- [Known Issues] Outside of the United States, only annual production
data is available, which are distributed based upon normal distributions
of monthly production for various regions and countries. Changes have
not yet been made to account for production disruptions in 2026 that
deviate from the normal pattern. Annual production numbers are
continuously being updated based on data from our providers and will be
reflected in future updates with a note in the corresponding changelog.

- [Known Issues] Jumps in emissions between December and January are
currently expected. Due to modelling being conducted on an annual basis,
and monthly data being the result of splitting annual data, there are
natural jumps in the data that will be centralized between different
years.

- [Known Issues] Data for California prior to 2024 is unavailable
presently due to source data issues.

- [Known Issues] Onsite electricity generation included in emissions.

## fossil-fuel-operations,oil-and-gas-transport

### Added

- [Added] Data period calculated for all sources to the end of May
2026.

- [Added] CO2 emissions source percentage breakout between combustion
(the burning of fuels onsite to either generate electricity or directly
power various processes), fugitives, flaring, and venting. Saved to
columns ‘other2’, ‘other3’, ‘other4’, and ‘other5’, respectively. Note -
‘other2’ (combustion) is always 100% of the emissions.

- [Added] Greater coverage in the United States to include smaller
assets both in states with large production volumes and newly covered
states with low production volumes.

### Changed

- [Changed] For assets in the United States, our primary data
provider has incomplete production data for 2025 and 2026. For 2025 and
2026, United States data is duplicated from 2024 due to this lack of
data.

- [Changed] Lag changed to 2 months to match other sectors due to the
ease of copying earlier years.

- [Changed] Emissions intensity calculation methodology has changed
to reduce variability and uncertainty. Further explanation can be found
in methodology documentation for the oil and gas production and
transportation sectors.

- [Changed] Some aggregation of assets outside of the United States
changed to better account for similarities within the sector and data
privacy requirements.

- [Changed] Grid electricity emissions not included in emissions.

### Fixed

- [Fixed] Anomalous NMVOC emissions values in BIH corrected.

### Known Issues

- [Known Issues] Outside of the United States, only annual production
data is available, which are distributed based upon normal distributions
of monthly production for various regions and countries. Changes have
not yet been made to account for production disruptions in 2026 that
deviate from the normal pattern. Annual production numbers are
continuously being updated based on data from our providers and will be
reflected in future updates with a note in the corresponding changelog.

- [Known Issues] Jumps in emissions between December and January are
currently expected. Due to modelling being conducted on an annual basis,
and monthly data being the result of splitting annual data, there are
natural jumps in the data that will be centralized between different
years. git s

- [Known Issues] Data for California prior to 2024 is unavailable
presently due to source data issues.

- [Known Issues] Onsite electricity generation included in emissions.

## manufacturing,aluminum

### Added

- [Added] Full historical refresh (2021–present) of asset data, full
refresh (2015-present) of country data - note that the actual emissions
have not changed, only the distribution of emissions across scope 1 and
2 have changed.

### Changed

- [Changed] Scope 1 now represents direct process emissions only;
captive and grid electricity are both reported under Scope 2
(previously, captive power generation was included in Scope 1).

### Deprecated

- [Deprecated] None

### Known Issues

- [Known Issues] Asset emissions exceed country emissions in CHN,
AUS, and USA. This will be fixed in a future release.

## manufacturing,cement

### Added

- [Added] Full refresh of asset-level emissions from 2021 to July
2026.

- [Added] Full refresh of country-level emissions from 2021 to July
2026.

- [Added] Updated the asset list based on the new release of the GEM
Global Cement and Concrete Tracker.

### Changed

- [Changed] Emissions factors now account for plant-level clinker
substitution rate, kiln configuration (pre-calciner and preheater), and
on-site waste heat recovery, where reported by GEM.

- [Changed] Adjusted the calibration curve between satellite
detection and capacity factor using the latest available data.

### Deprecated

- [Deprecated] None

### Fixed

- [Fixed] None

### Known Issues

- [Known Issues] None

## manufacturing,petrochemical-steam-cracking

### Added

- [Added] None

### Changed

- [Changed] None

### Deprecated

- [Deprecated] None

### Fixed

- [Fixed] None

### Known Issues

- [Known Issues] Post-processing artifact results in country-level
PM2.5 emissions discontinuity where 2015-2023 (~60-100 tonnes per year)
and 2026 emissions are ~4-6x greater than 2024 and 2025 emissions (~18
tonnes per year).

## manufacturing,pulp-and-paper

### Added

- [Added] Full historical refresh (2015–present) of asset and country
data.

- [Added] Zero-production months now included as explicit rows
(previously omitted).

### Changed

- [Changed] Scope 1 now represents direct process emissions only;
captive and grid electricity are both reported under Scope 2
(previously, captive power generation was included in Scope 1).

- [Changed] Asset scope narrowed to pulp-producing and integrated
mills (previously included standalone paper-only facilities).

- [Changed] Asset-level, technology-specific emissions factors
replace the previous flat industry-wide factor.

- [Changed] Industrial Information Resources (IIR) data included
alongside Spatial Finance Initiative (SFI). Previously SFI-only.

### Deprecated

- [Deprecated] None

### Known Issues

- [Known Issues] Asset identifiers differ substantially from prior
submissions due to the source and scope changes above; this reflects
intentional methodology improvements, not lost coverage.

- [Known Issues] One asset (An Hoa Pulp Mill, VNM) has no reported
ownership data.

## manufacturing,iron-and-steel

### Added

- [Added] Added new month, July 2026 asset data level emissions.

- [Added] Added new month, July 2026 country level emissions.

### Changed

- [Changed] None

### Deprecated

- [Deprecated] None

### Fixed

- [Fixed] None

### Known Issues

- [Known Issues] None

## manufacturing,glass

### Added

- [Added] Added 191 assets relative to V5.10.0.

### Changed

- [Changed] Capacity (tonnes), activity (tonnes of output), and
emissions factor (tonnes [GAS] per tonnes of output) units have been
updated.

- [Changed] Asset type now represents the category of output (i.e.
float glass vs. contained glass).

- [Changed] Estimate methodology now prioritizes constraining
country-level production totals, by output.

### Deprecated

- [Deprecated] Removed 88 assets relative to V5.10.0 (55 absent from
the 2026 registry pull; 33 held, presumed closed).

### Fixed

- [Fixed] Capacity factors are ≤ 1 everywhere and represent the
product output for the year relative to the maximum for all years for
that asset.

### Known Issues

- [Known Issues] All float-glass plants are located at administrative
centroids (flagged per row).

## manufacturing,lime

### Added

- [Added] Added 98 assets relative to V5.10.0.

### Changed

- [Changed] Estimate methodology now prioritizes constraining
country-level production totals, by output. Activity is anchored to U.S.
Geological Survey (USGS) national lime production (82 countries), with
the country factor derived as emissions ÷ production.

- [Changed] Asset type now represents the category of output (e.g.
quicklime, dolomitic lime, etc.).

### Deprecated

- [Deprecated] Removed 57 assets relative to V5.10.0 (51 absent from
the 2026 pull; 6 held, presumed closed).

### Fixed

- [Fixed] Capacity factors are ≤ 1 everywhere and represent the
product output for the year relative to the maximum for all years for
that asset.

### Known Issues

- [Known Issues] None

## manufacturing,food-beverage-tobacco

### Added

- [Added] Added 16,212 assets relative to V5.10.0.

### Changed

- [Changed] Capacity (tonnes), activity (tonnes of output), and
emissions factor (tonnes [GAS] per tonnes of output) units have been
updated.

[Changed] Biogenic fermentation CO2 is now included in emissions
totals and the process share.

- [Changed] Asset type now represents the category of output (e.g.
grain milling, brewery, etc.).

### Deprecated

- [Deprecated] Removed 387 assets relative to V5.10.0 (180 absent
from the 2026 pull; 205 held, presumed closed).

### Fixed

- [Fixed] Capacity factors are ≤ 1 everywhere and represent the
product output for the year relative to the maximum for all years for
that asset.

### Known Issues

- [Known Issues] None

## manufacturing,textiles-leather-apparel

### Added

- [Added] Added 9,254 assets relative to V5.10.0.

### Changed

- [Changed] Capacity (tonnes), activity (tonnes of output), and
emissions factor (tonnes [GAS] per tonnes of output) units have been
updated.

- [Changed] Estimate methodology now prioritizes constraining
country-level production totals, by output.

- [Changed] Asset type now represents the category of output (e.g.
dyeing, finishing, etc.).

### Deprecated

- [Deprecated] Removed 2 assets relative to V5.10.0.

### Fixed

- [Fixed] Capacity factors are ≤ 1 everywhere and represent the
product output for the year relative to the maximum for all years for
that asset.

### Known Issues

- [Known Issues] None

## mineral-extraction,other-mining-quarrying

### Added

- [Added] None

### Changed

- [Changed] None

### Deprecated

- [Deprecated] None

### Fixed

- [Fixed] None

### Known Issues

- [Known Issues] None

## mineral-extraction,copper-mining

### Added

- [Added] None

### Changed

- [Changed] None

### Deprecated

- [Deprecated] None

### Fixed

- [Fixed] None

### Known Issues

- [Known Issue] Country-level copper-mining co2e emissions show an
unrealistic step change at 2019→2020 — global totals roughly double from
~34 Mt CO2e/yr (2015–2019) to ~53–68 Mt CO2e/yr (2020–2024), affecting
many copper-producing countries simultaneously. Present since at least
V4.0.

## power,electricity-generation

### Added

- [Added] Data period extended for existing sources. Start_date
2019-01-01 to end_date 2026-07-31.

### Changed

- [Changed] Updated unit/plant level information due to manual
research. These can result in changes to our estimates.

- [Changed] Updated GEM coal tracker, and oil/gas tracker (August
2026). These can result in changes to our estimates and plant catalog.

- [Changed] Updated ownership data from new GEM tracker updates.

- [Changed] Updated EIA860 monthly data. These can result in changes
to our estimates and plant catalog.

### Fixed

- [Fixed] None

### Known Issues

- [Known Issues] For non-operational plants the data is reported as
zero values for capacity, capacity factor, activity, emissions
intensity, and emissions. The related uncertainties are also reported as
zero. This is not strictly correct since there can be uncertainty in the
operating status in a given month. Future work will better quantify the
uncertainty when the plant is reported as non-operational.

## transportation,domestic-aviation

### Added

- [Added] Data period extended for existing sources. Start_date
2015-01-01 to end_date 2026-07-31.

- [Added] Added coverage. 13 new sources added, identified by
International Air Transport Association (IATA) code: {'iata_GEB',
'iata_GWI', 'iata_HEZ', 'iata_INX', 'iata_IYO', 'iata_KGJ', 'iata_LMB',
'iata_NSA', 'iata_OQN', 'iata_ORK', 'iata_PMQ', 'iata_TBX', 'iata_UTA'}.

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

- [Added] Data period extended to cover 2026-07-01 through
2026-07-31. Non-broadcasting estimates for this period are placeholders
that repeat the June 2026 values, as we are transitioning to the new
Sentinel-1 products and have not yet reprocessed July detections (see
Known issues).

### Changed

- [Changed] None

### Deprecated

- [Deprecated] None

### Fixed

- [Fixed] None

### Known Issues

- [Known Issues] We are transitioning to the new Sentinel satellite
products. Until that transition is complete, non-broadcasting estimates
for July 2026 remain placeholder values carried over from June 2026.

## transportation,domestic-shipping

### Added

- [Added] Data period extended. Start_date 2026-07-01 to 2026-07-31.

### Changed

- [Changed] None

### Deprecated

- [Deprecated] None

### Fixed

- [Fixed] None

### Known Issues

- [Known Issues] OceanMind Invalid transmissions can cause
interpolation of trips over extended data gaps which may result in large
erroneous emissions spikes at a port at the time when the data gap ends

- [Known Issues] OceanMind Attribution of emissions to ports as 50/50
on trips with significant loitering can cause emissions reductions
assigned to a port that is greater than the emissions assigned to that
port

## transportation,international-aviation

### Added

- [Added] Data period extended for existing sources. Start_date
2015-01-01 to end_date 2026-07-31.

- [Added] Added coverage. 6 new sources added, identified by
International Air Transport Association (IATA) code: {'iata_BGC',
'iata_DLZ', 'iata_ERS', 'iata_KSY', 'iata_NMI', 'iata_ZZU'}

### Changed

- [Changed] None

### Fixed

- [Fixed] None

## transportation,international-shipping

### Added

- [Added] Data period extended. Start_date 2026-07-01 to 2026-07-31.

### Changed

- [Changed[ None

### Deprecated

- [Deprecated] None

### Fixed

None

### Known Issues

- [Known Issues] OceanMind Invalid transmissions can cause
interpolation of trips over extended data gaps which may result in large
erroneous emissions spikes at a port at the time when the data gap ends

- [Known Issues] OceanMind Attribution of emissions to ports as 50/50
on trips with significant loitering can cause emissions reductions
assigned to a port that is greater than the emissions assigned to that
port

## transportation,road-transportation

### Added

- [Added] Data period extended for existing sources. New end_date
2026-06-30.

### Changed

- [Changed] Countries outside of the USA, CAN, PRI, and VIR will use
updated PM2.5 modeling based on PM2.5 emission ratios derived from
EDGAR. Most countries will see a noticeable increase in PM2.5 emissions.

- [Changed] Vehicle fuel mix was updated using road vehicle fleet
information from the United Nations Economic Commission for Europe
(UNECE) statistical database and various country-level inventories.
Relative to the previous baseline, the portions of the vehicle fleet
with EV and PHEV powertrains have been increased. Countries affected
include: ALB, AUT, BEL, BGR, BIG, BMU, CAN, CHE, CYR, CZE, DEU, DNK,
ESP, EST, FIN, FRA, GBR, GEO, GRC, GRL, HRV, HUN, IRL, ISL, ISR, ITA,
KAZ, LIE, LTU, LUX, LVA, MDA, MKD, MLT, MNE, NLD, NOR, POL, PRT, ROU,
SPM, SRB, SVK, SVN, SWE, TUR, UKR, USA, HKG, KOR, SGP, and UGY.

### Deprecated

- [Deprecated] None

### Fixed

- [Fixed] Remove null asset_identifier rows in asset data.

- [Fixed] Anomalous jump in non-GHG emissions starting in January
2026 has been corrected.

### Known Issues

- [Known Issues] spike in 2018 emissions in UZB may be a result of an
issue with reported data.

- [Known Issues] Have not updated to the latest Climate TRACE patch
of GADM data (v1.1.2).

## waste,domestic-wastewater-treatment-and-discharge

### Added

- [Added] Data period extended for existing sources. Start_date
2015-01-01 to end_date 2026-08-31.

- [Added] Preliminary emissions estimates for 5,403
satellite-identified assets in the following countries: CHN, IND, RUS,
EGY, TUR, UKR, ARG, IRQ, GBR, IRN, MEX, KOR, POL, MAR, SAU, CHL, GRC,
KAZ, ZAF, BRA, DZA, ROU, UZB, VNM, PAK, ISR, COL, BLR, TUN, HRV, BGR,
VEN, BGD, BIH, HUN, MKD, THA, ARE, ECU, KGZ, OMN, SRB, SYR, ALB, CZE,
TJK, USA, CUB, LBN, MNE, PER, QAT, TKM, LBY, MDA, SVK, EST, HND, LTU,
AFG, BOL, IDN, KHM, LVA, NIC, and SLV. Preliminary emissions estimates
start_date is 2015-01-01 to end_date 2026-08-31.

### Changed

- [Changed] Added other6 column with lagoon surface area estimations
for centralized wastewater treatment assets in the U.S., only in cases
where a pond was detected via satellite ML model and its location was
placed with high confidence. Units are in square meters.

### Deprecated

- [Deprecated] None

### Fixed

- [Fixed] None

### Known Issues

- [Known Issues] All wastewater treatment plants in the set of 5,403
new satellite-identified assets are assumed to treat domestic
wastewater. Industrial wastewater treatment plants and water
purification facilities have not been filtered out, which will lead to
an overestimate in asset emissions, in some cases causing the sum of
asset-level emissions for a country to exceed estimated country-level
emissions.

- [Known Issues] Inconsistent year-over-year population values for
Kiribati in the underlying population source data are carried forward
into country-level emissions estimates. To be addressed in future
releases.

- [Known Issues] The dilution factor column (other1) relies on
HydroWASTE values and will remain blank for non-HydroWASTE assets.

## waste,industrial-wastewater-treatment-and-discharge

### Added

- [Added] Data period extended for existing sources. Start_date
2026-05-01 to end_date 2026-08-31.

- [Added] 551 new assets- 482 assets that treat pulp wastewater and
69 assets that treat steel wastewater.

### Changed

- [Changed] None

### Deprecated

- [Deprecated] None

### Fixed

- [Fixed] None

### Known Issues

- [Known Issues] Potential duplicate assets.
