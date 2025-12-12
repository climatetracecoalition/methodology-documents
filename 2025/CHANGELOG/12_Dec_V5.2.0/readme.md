# [5.2.0] - 2025-12-12
## ClimateTRACE,deprecation-warning
For the current (V5.2.0) release, the following Deprecation Warning is now in effect:
- [Deprecation Warning] The following BigQuery tables are now deprecated and removed in V5.2.0: 
`climate_trace.road-segments_road-transportation_202505` and `climate_trace.shipping-voyages_shipping_2025`. These tables have been replaced by the following BigQuery tables: `climate_trace.road_segments` and `climate_trace.shipping_voyages` respectively. All future updates will be applied to the new tables only.

## ClimateTRACE,multiple-sectors,post-processing
### Fixed
- [Fixed] Country emissions for domestic-wastewater-treatment were missing in V5.1.0 for January 2015 for all countries. Fixed in this release.
### Known Issues
- [Known Issues] For sectors with native temporal granularity of “quarterly”, published monthly data (including emissions_quantity, activity, capacity, etc.) are rounded to the 5th decimal place, which results in very small values being rounded down to 0. Affected sectors: ‘enteric-fermentation-cattle-operation’ and ‘manure-management-cattle-operation’.

## ClimateTRACE,individual-changelogs
See indiviudal text files and the '5.2.0_combined-changelog-climate-trace.pdf'. 
