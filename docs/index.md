# PSRIO Release Notes

📚 [PSRIO Documentation](https://docs.psr-inc.com/knowledge/additional_tools/psrio/getting_started/introduction.html)


## 3.0.0 (2026-02-14)

### Added
- `chart:enable_controls(int)`
- `chart:enable_timeline_controls(int) and chart:enable_timeline_controls()`
- `chart:tooltip_all_series()`
- `chart:disable_markers()`
- `chart:hide_play_control()`
- `--multiple_s3_load` argument
- `BY_CVAR_L_EXCLUDING(int, double)` aggregation
- `BY_CVAR_R_EXCLUDING(int, double)` aggregation
- `--old_dashboard_template` argument
- `TimeSeries():set_reference_date('dd/mm/yyyy')`
- `new dashboard template`

## 2.1.0 (2026-01-05)

### Added
- `exp:scenarios_percentile_indexes_left(int)`
- `exp:scenarios_percentile_index_right(int)`
- `exp:scenarios_percentile_index_range(int, int)`
- `exp:select_dummy_plants(string)`
- `exp:select_agent_by_code(string)`
- `exp:select_agents_by_code({string})`
- `exp:agents_to_scenarios()`
- `chart:add_horizontal_range(int, int, options)`
- `chart:add_horizontal_line(int, options)`
- `chart:add_vertical_range(int, int, options)`
- `chart:add_vertical_line(int, options)`
- `chart:add_vertical_range({day=int, month=int, year=int}, {day=int, month=int, year=int}, options)`
- `chart:add_vertical_line({day=int, month=int, year=int}, options)`
- `chart:add_vertical_line({day=int, month=int, year=int}, options)`
- `chart:hide_state_series()`
- `chart:enable_3d_view()`
- `chart:enable_vertical_grid()`
- `--not_found_output_list` argument
- `chart:add_line_block_categories(exp)`
- `chart:add_column_block_categories(exp)`
- `chart:xlabel_rotation(int)`
- `os.time()`
- `os.difftime(time1, time2)`
- `os.clock()`
- `BY_WEIGHTED_VAR_L(int)` aggregation
- `BY_WEIGHTED_VAR_R(int)` aggregation

#### Added (Input Data)
- `battery.oem_type`
- `thermal.dummy_plant_1`
- `thermal.dummy_plant_2`
- `thermal.dummy_plant_3`
- `renewable.curtailment_cost`
- `load.active_power`
- `Collection():get_vector_values(Attribute_name, Agent_name)`
- `InterconnectionSum():get_coefficients(Interconnection_name)`

### Fixed
- `chart data exports now open correctly in Excel, regardless of separation settings`

## 2.0.0 (2025-05-18)

### Added

#### Added (Collection)
- ACLine
- DCLine
- FlexibleDemand
- GenericVariable
- HydroGenerator
- PhaseShifter
- RenewableGenerator
- SerieCapacitor
- ThermalGenerator
- Transformer
- ThreeWindingTransformer

### Changed
- Update the studies database to SDDP 18

## 1.3.0 (2025-04-10)

### Added
- `GanttChart()` and `ganttchart:add(string, epoch, epoch)`
- `ganttchart:enable_labels()`
- `ganttchart:enable_grid()`
- `ganttchart:rows()`
- `ganttchart:first_max_visible_lines(int)`
- `ganttchart:set_height(int)`
- `ganttchart:set_auto_height()`  
- `exp:n_largest_indices(int, options)`
- `exp:n_smallest_indices(int, options)`
- `exp:hydro_from()`
- `exp:hydro_to()`
- `exp:aggregate_agents(function, string, weights)`
- `exp:aggregate_scenarios(function, weights)`
- `exp:remove_characters(string)`
- `chart:set_tooltip(series_index, point_index, tooltip)`
- `chart:shared_tooltip()`
- `chart:tooltip_point_format(string) and chart:tooltip_point_format({string1,string2,...})`
- `chart:tooltip_header_format(string) and chart:tooltip_header_format({string1,string2,...})`
- `chart:errorbar_category(exp, label)`
- `chart:save(filename)`
- `string.random(length)` and `string.trim(s)`
- `BY_WEIGHTED_AVERAGE()` aggregation
- `BY_VAR_R()` aggregation
- `BY_VAR_L()` aggregation
- `BY_SDTERROR()` aggregation
- `BY_STDERROR()` aggregation
- `Topology.FILTRATION_FROM`
- `--ifeedback` argument
- `--temporary` argument
- `--model optmain` argument
- `--undirected_relationship` argument
- `--timeout` argument (value in seconds)
- `--loads3` argument (require AWS_ACCESS_KEY_ID and AWS_SECRET_ACCESS_KEY) 

#### Added (Collection)
- `MaintenanceSolicitation` collection
- `WaterWay` collection
- `collection:get_scalars(i)`
- `collection:load_table(filename, bool load_from_output_path)`
- `collection:load_table_without_header(filename, bool load_from_output_path)`
- `generic:create_temporary_writer(filename)`  

#### Added (Input Data)
- `hydro.hourly_maintenance`
- `hydro.hourly_unavailability`
- `hydro.regulation_factor`
- `hydro.spillage_loss_factor`
- `hydro.turbining_loss_factor`
- `renewable.forced_outage_rate`
- `renewable.hourly_maintenance`
- `renewable.hourly_unavailability`
- `sddp/historical_inflow`
- `thermal.hourly_maintenance`
- `thermal.hourly_unavailability`
- `thermal.take_or_pay_cost`

### Changed
- `sddp/usedcl` where flow in negative (to -> from)

### Fixed
- `chart:add_categories` when adding expressions with different number of categories
- fix block load level length when running --model none

## 1.2.0 (2024-10-21)

### Added
- Interactive charts with animation controls
- `Spreadsheet()` and `spreadsheet:add(exp, string)`
- `exp:rainflow_count(exp1, range_min, range_max)`
- `exp:initial_date()`
- `exp:final_date()`
- `exp:data_info()`
- `exp:select_blocks({ i, j, k })` and `exp:select_blocks(i, k)`
- `circuit:bus_to(f)`
- `circuit:bus_from(f)`
- `chart:enable_controls()`
- `chart:invert_axes()`
- `chart:xlabel_datetime_format(string)`
- `chart:add_line(exp, { data_format = '...' })`, ...
- `chart:add_box_plot_categories(exp1, exp2, exp3, exp4, exp5, label, options)`
- `chart:add_heatmap_agents(exp)`
- `chart:enable_vertical_zoom()`
- `chart:horizontal_legend`
- `BY_AVERAGE_EXCLUDING(double)` aggregation
- `BY_SUM_EXCLUDING(double)` aggregation
- `BY_PERCENTILE_EXCLUDING(int, double)` aggregation
- `PSR.console_verbose_level(i)`
- `PSR.console_verbose_level()`
- `--skip_typical_days_validation` argument

#### Added (Collection)
- `ElectrificationFixedConverter`
- `ElectrificationFixedCommodity`

#### Added (Input Data)
- `circuit.decommissioned`
- `hydro.ramp_up`
- `hydro.ramp_down`
- `hydro.bid_price`
- `expansion_project.integration_cost`
- `expansion_project.invest_cost_unit`
- `expansion_project.invest_cost`
- `expansion_project.annualized_invest_cost`
- `thermal.commitment_type`
- `battery.charge_ramp`
- `battery.discharge_ramp`
- `battery.max_reserve`
- `battery.bid_price`
- `renewable.max_reserve`
- `renewable.bid_price`

### Submodules
- lua `5.4.6` -> `5.4.7`

## 1.1.0 (2024-05-22)

### Added
- `exp:stage_profile_day(f)`
- `exp:cumsum_stages()`
- `exp:select_scenarios_kth_largest(i)`
- `exp:select_scenarios_kth_smallest(i)`
- `exp:convert()`
- `exp:aggregate_stages(..., Profile.PER_SEMESTER)`
- `exp:aggregate_stages(..., Profile.SEMESTER)`
- `exp:reshape_stages(Profile.PER_SEMESTER)`
- `chart:add_line_categories(...)`
- `chart:add_line_stacking_categories(...)`
- `chart:add_spline_categories(...)`
- `chart:add_column_stacking_categories(...)`
- `chart:add_column_percent_categories(...)`
- `--load_format` argument

#### Added (Input Data)
- `Battery().max_storage`
- `Battery().min_storage`
- `Battery().om_cost`

### Syntax Changes
- `chart:add_categories(...)` to `chart:add_column_categories(...)`

### Removed
- `--binf_rule` argument

### Submodules
- PSRClasses `6a8cd0db` -> `c4e86064`

## 1.0.0 (2024-03-17)

### Added
- responsive containers to side by side charts
- marketplace documentation
- `exp:save(..., { index = false })`
- `toml:get_keys()`
- `toml:get_table(key)`
- `toml:get_table(key, fallback)`
- `toml:get_table_array(key)`
- `--binf_rule` argument
- `hydro.discharge_ramp_up`
- `hydro.discharge_ramp_down`
- `chart:add_waterfall(...)`
- `collection:force_load(file_name)`
- `concentrated_solar_power.system`

#### Added (Input Data)
- `demand.is_enabled`

### Changed
- major performance improvements in `exp:select_agents(query)` method
- major performance improvements in `exp:remove_zeros()` method
- minor performance improvements in `exp:convert(...)` method
- `toml:get_string(key, fallback)` where fallback is dynamic
- `toml:get_string_array(key, fallback)` where fallback is dynamic
- `toml:get_integer(key, fallback)` where fallback is dynamic
- `toml:get_integer_array(key, fallback)` where fallback is dynamic
- `toml:get_real(key, fallback)` where fallback is dynamic
- `toml:get_real_array(key, fallback)` where fallback is dynamic
- `toml:get_boolean(key, fallback)` where fallback is dynamic

### Fixed
- `GasNode` collection
- `collection:print_elements()` index
- error in `exp:aggregate_blocks()` when exp is null

### Removed
- `--load_only_csv` argument

### Submodules
- bootstrap `5.3.2` -> `5.3.3`
- bootstrap-icons `1.11.1` -> `1.11.2`
- github-markdown-css `5.4.0` -> `5.5.1`
- json `3.11.2` -> `3.11.3`
- psrplot `0.11.0` -> `0.12.0`

## 0.27.0 (2023-12-12)

### Added
- `datetime` library
- `table` extension
- `exp:collection()`
- `exp:study_index()`
- `exp:reshape_stages(Profile.QUARTER)`
- `exp:to_block()` and `exp:to_hour()` with automatic unit solver
- `chart:add_thermal_merit_order_curve(...)`
- `collection:ids()`
- `collection:get_study_index()`
- `study:get_relationship_array(...)`
- `toml:get_real_array(key)`
- `BY_RAINFLOW_COUNT()` aggregation
- `Reader` class
- `debug(...)` and `trace(...)`
- `base/sddp/deficit_cost_segment.lua`
- `--modeloutput`, `--relative_tolerance`, `--absolute_tolerance` arguments
- `PSR.interpolate_colors(color1, color2, color3, n)`

#### Added (Collection)
- `OptPriceAgent` collection
- `OptPriceContract` collection
- `OptPriceLoad` collection
- `OptPricePlant` collection
- `OptPriceSystem` collection

#### Added (Input Data)
- `battery.system`
- `hydro.initial_condition`
- `hydro.initial_condition_type`
- `powerinjection.system`
- `system.risk_aversion_curve`

### Syntax Changes
- `study:get_relationship(...)` to `study:get_relationship_map(...)`
- `powerinjection.hour_capacity` -> `powerinjection.capacity`
- `powerinjection.hour_price` -> `powerinjection.price`

### Changed
- internal changes in reshape_stages

### Fixed
- `GasEmission` collection
- error when loading an csv file inside a subdirectory
- error in concatenate(...)
- error saving an expression that has stage type = quarter

### Removed
- `writer:open()`

### Submodules
- github-markdown-css `5.3.0` -> `5.4.0`
- PSRClasses `5aa8e761` -> `57b055d9`
- zlib `v1.2.13` -> `v1.3`

## 0.26.0 (2023-10-18)

### Added
- `exp:shift_values(shift)`
- `exp:aggregate_stages_weighted(by, weights, profile)`
- `exp:assignments_mask(k)`
- `safe_divide(exp1, exp2)`
- `chart:add_line_exclude_zeros(...)`
- `chart:add_heatmap_series_exclude_zeros(...)`
- `study:final_year_without_buffer_years()`
- `study:get_parameter(model, key, fallback)`
- `toml:get_string_array(...)`
- `GenericConstraintInterpolation` collection
- `$/kW`, `m3` as favorite units
- `base/sddp/unitary_variable_cost.lua`

### Changed
- charts front-end improvements
- `psrio.pmk` to `PSRIO.pmk`
- `psrio.pmd` to `PSRIO.pmd`
- `psrio.ver` to `PSRIO.ver`
- `psrio.exe` to `PSRIO.exe`
- `psrio` to `PSRIO` (linux)

### Fixed
- AWS S3 header reading when there are duplicated agents
- unit when `exp:force_unit(...)` is the last operation
- optgen study horizon
- binary expression backwards relationship
- `base/sddp/reservoir_stored_energy.lua`

### Submodules
- PSRClasses `2cfa7e4a` -> `5aa8e761`
- bootstrap `5.3.1` -> `5.3.2`
- bootstrap icons `1.11.0` -> `1.11.1`
- github-markdown-css `5.2.0` -> `5.3.0`
- KaTeX `0.16.8` -> `0.16.9`
- highlightjs `11.8.0` -> `11.9.0`

## 0.25.0 (2023-08-11)

### Added
- PSRIO Marketplace
- PSRIO Extensions
- collections relationship rework with an internal graph search
- `collection:file_exists(path)`
- `PSR.source_line(level)`
- `expansion_project.capacity`
- `renewable.system`
- `chart:add_heatmap_series(...)`
- `chart:add_cumulative_distribution_function(...)`
- `chart:push_annotation(x, y, text)`
- `xLabel` and `yLabel` for the chart options
- `#tab` length operator
- `tab:push_table(...)`
- `tab:push_divider()`
- `exp:aggregate_agents_by_label(...)`
- `exp:reorder_agents(...)`
- `exp:bus_from()` and `exp:bus_to()`
- `exp:select_and_rename_agent(agent, label)`
- `exp:set(stage, scenario, block, agent, data)`
- `exp:add_agent_right(label)`
- `exp:add_agent_left(label)`
- `study:get_relationship(collection_from, collection_to)`
- `study.deficit_segment_1`, ..., `study.deficit_segment_4`
- `study.deficit_cost_1`, ..., `study.deficit_cost_4`
- `study:initial_hydrology_stage()` and `study:initial_hydrology_year()`
- `hydro_gauging_station:final_hydrology_year()`

### Fixed
- histogram chart
- errors handling huge graf files

### Removed
- `GaugingStation` collection (users should use `HydroGaugingStation` collection)
- `exp:save(..., { remove_zeros = true })`, the users should use the `exp:remove_zeros()` method

### Submodules
- bootstrap `5.2.3` -> `5.3.1`
- fast_float `4.0.0` -> `5.2.0`
- GitHub Flavored Markdown `0.29.0.gfm.11` -> `0.29.0.gfm.13`
- highlightjs `11.7.0` -> `11.8.0`
- KaTeX `0.16.4` -> `0.16.8`
- Lua `5.4.4` -> `5.4.6`
- PSRClasses `5ce7fe6e` -> `2cfa7e4a`

## 0.24.0 (2023-05-12)

### Added
- improved NCP integration
- `chart:add_box_plot(...)`
- `dashboard:set_refresh_rate(...)`
- `toml:get_integer_array(key)`
- `exp:select_agents(collection)` when exp is from a generic collection
- `exp:uncouple_blocks(clear_first_data)`
- `exp:uncouple_stages_blocks()`
- `exp:uncouple_stages_blocks(clear_first_data)`
- `exp:spread_hours()`
- `exp:aggregate_broadcast_blocks(f, profile)`
- collection length operator: `#collection`
- `--upload_dashboards` argument (require AWS_ACCESS_KEY_ID and AWS_SECRET_ACCESS_KEY)
- `--incremental_progress_bar` argument
- `circuit_flow.lua`, `thermal_operation.lua` and `thermal_dispatch_factor.lua`
- `hydro.min_total_outflow_hourly`
- `hydro.max_total_outflow_hourly`
- `hydro.min_operative_storage_hourly`
- `hydro.max_operative_storage_hourly`
- `hydro.flood_control_hourly`
- `hydro.alert_storage_hourly`
- `hydro.min_spillage_hourly`
- `hydro.max_spillage_hourly`
- `hydro.min_bio_spillage_hourly`
- `hydro.target_storage_hourly`
- `hydro.max_turbining_hourly`

### Syntax Changes
- `toml:get_array_size(...)` to `toml:get_table_array_size(...)`
- `toml:get_array(...)` to `toml:get_table_array(...)`
- `thermal_generation_running_hours.lua` to `thermal_plant_running_hours.lua`
- `concentratedsolarpower.hour_generation` to `concentratedsolarpower.hour_scenarios`

### Changed
- if the binary expression relationship can not be found, try the other way around
- `collection:load_table` and `collection:load_table_without_header` behavior when the file does not exist; now return an empty table

### Fixed
- binary expression relationship issue that occurred when the collection consisted of only one agent
- missing trim in collection:load_table(...)
- `chart:add_probability_of_exceedance(...)` and `chart:add_probability_of_exceedance(...)` last point (100%)
- `collection:load_table_without_header` loading (#133)
- issue that occurred when attempting to save a dashboard or report within a nested folder
- error that occurred while running a script with a report in dependency mode

### Removed
- `Dashboard("title")`
- `dashboard + dashboard` operator
- `dashboard:push(dashboard)`
- `dashboard:push(chart)`
- `dashboard:push(markdown)`
- `area.imported`
- `area.exported`
- `circuit.international_cost_right`
- `circuit.international_cost_left`
- `dclink.capacity_right`
- `dclink.capacity_left`
- `fuelcontract.max_offtake`
- `interconnection.capacity_right`
- `interconnection.capacity_left`
- `interconnection.cost_right`
- `interconnection.cost_left`
- `renewable.hour_generation`
- `renewable.block_generation`
- `renewable_gauging_station.hour_generation`
- `renewable_gauging_station.block_generation`
- `renewable_gauging_station.hour_historical_generation`

### Submodules
- Bootstrap Icons `1.10.2` -> `1.10.4`
- fast_float `3.10.0` -> `4.0.0`
- GitHub Flavored Markdown `0.29.0.gfm.9` -> `0.29.0.gfm.11`
- PSRClasses `62b06eab` -> `5ce7fe6e`

## 0.23.0 (2023-04-03)

### Added
- dashboard loading overlay
- `HydroGaugingStation` collection (alias to `GaugingStation`, to be deprecated in the future)
- `collection:avids()`
- `relational:add(header, vector)`
- `exp:spread_stages(int)`
- `exp:replace_scenarios(src, {int, int, ...})`
- `study:stages_without_buffer_years()` and `study:buffer_stages()`
- `hydro.storage_x_elevation__storage_1`, ..., `hydro.storage_x_elevation__storage_5`
- `hydro.storage_x_elevation__elevation_1`, ..., `hydro.storage_x_elevation__elevation_5`

### Changed
- `BY_PERCENTILE(p)` to be the same as Excel PERCENTILE.EXC

### Fixed
- `fuel.emission_factor`
- `collection:labels()`
- `--magent` intermittent error

### Removed
- `writer:open()`, now the open function is called in the constructor

### Submodules
- PSRClasses `c72d7788` -> `62b06eab`

## 0.22.0 (2023-03-09)

### Added
- new AWS S3 saving implementation
- `exp:aggregate_scenarios_blocks(f)`
- `exp:aggregate_topology(f, topology, min_level, max_level)`
- `chart:add_heatmap(exp)`
- `chart:add_column_range(exp, exp)`
- `chart:add_error_bar(exp, exp)`
- `chart:set_digits(int)` and `timeseries:set_digits(int)`
- `chart:add_probability_of_nonexceedance(...)`
- `Topology.SPILLED_FROM`
- `--load_only_csv` argument

### Syntax Changes
- `Collection.DCLINK` to `Collection.DC_LINK`

### Changed
- improved heatmap rendering performance
- improved the significant digits in the fast_csv
- `collection:labels()`, `collection:codes()`, and `collection:inputs()` now it returns a table

### Fixed
- error in `collection:get_files(...)` and `collection:get_directories(...)` when the directory does not exist
- error when trying to save data in a subfolder (#93)
- error loading netplan bases
- error when converting units with negative stages (#96)

### Removed
- `chart:add_heatmap_hourly(...)`
- awsintegration

### Submodules
- fast_float `3.8.1` -> `3.10.0`
- GitHub Flavored Markdown `0.29.0.gfm.7` -> `0.29.0.gfm.9`
- Github Markdown CSS `5.1.0` -> `5.2.0`
- PSRClasses `1ce193dd` -> `66c9973f`
- PSRPlot `0.4` -> `0.7`

## 0.21.0 (2023-01-16)

### Added
- NCP support
- `exp:aggregate_blocks()` with automatic aggregation function selection
- `GenericConstraint` collection
- `exp:map_scenarios(filename)`
- `--load_from_output_path` reading in `collection:load_toml(...)`
- `dashboard:set_title(string)`
- `generic:create_writer(filename)`
- `writer:open()`
- `writer:is_open()`
- `writer:write(string)`
- `writer:write_line(string)`
- `writer:close()`
- `--log_append` argument

### Syntax Changes
- `--logname` to `--log_name` argument
- `toml:get_bool(...)` to `toml:get_boolean(...)`
- `toml:get_int(...)` to `toml:get_integer(...)`
- `toml:get_double(...)` to `toml:get_real(...)`

### Fixed
- intermittent error in `Load` collection
- `relational:add(string, study, from, to)` when the collection is empty
- error in `aggregate_stages when `first_stage > 1` (#86)
- error using `aggregate_stages(..., Profile.PER_WEEK)` when exp has weekly stages (#89)

### Removed
- some trace messages
- loadfile and dofile functions

### Submodules
- PSRClasses `07a23f47` -> `1ce193dd`

## 0.20.0 (2022-12-23)

### Added
- `study:has_flexible_demand()`
- `study:has_hourly_renewable_scenarios()`

### Syntax Changes
- all base functions now receive the study index, ex: `sddpgrxxd(i, suffix)`
- `battery.existing` to `battery.state`
- `fuel_reservoir.maxinjection` to `fuel_reservoir.max_injection`
- `fuel_reservoir.maxinjection_chronological` to `fuel_reservoir.max_injection_constraint`
- `hydro.min_total_outflow_penalty` to `hydro.min_total_outflow_unit_violation_cost`
- `hydro.max_total_outflow_penalty` to `hydro.max_total_outflow_unit_violation_cost`
- `hydro.min_operative_storage_penalty` to `hydro.min_operative_storage_unit_violation_cost`
- `hydro.max_operative_storage_penalty` to `hydro.max_operative_storage_unit_violation_cost`
- `hydro.alert_storage_penalty` to `hydro.alert_storage_unit_violation_cost`
- `hydro.min_spillage_penalty` to `hydro.min_spillage_unit_violation_cost`
- `hydro.max_spillage_penalty` to `hydro.max_spillage_unit_violation_cost`
- `hydro.min_bio_spillage_penalty` to `hydro.min_bio_spillage_unit_violation_cost`
- `hydro.min_turbining_penalty` to `hydro.min_turbining_unit_violation_cost`
- `hydro.max_turbining_penalty` to `hydro.max_turbining_unit_violation_cost`
- `hydro.min_total_outflow_penalty_type` to `hydro.min_total_outflow_violation_type`
- `hydro.max_total_outflow_penalty_type` to `hydro.max_total_outflow_violation_type`
- `hydro.min_operative_storage_penalty_type` to `hydro.min_operative_storage_violation_type`
- `hydro.max_operative_storage_penalty_type` to `hydro.max_operative_storage_violation_type`
- `hydro.alert_storage_penalty_type` to `hydro.alert_storage_violation_type`
- `hydro.min_spillage_penalty_type` to `hydro.min_spillage_violation_type`
- `hydro.max_spillage_penalty_type` to `hydro.max_spillage_violation_type`
- `hydro.min_bio_spillage_penalty_type` to `hydro.min_bio_spillage_violation_type`
- `hydro.min_turbining_penalty_type` to `hydro.min_turbining_violation_type`
- `hydro.max_turbining_penalty_type` to `hydro.max_turbining_violation_type`
- `renewable.hour_generation` to `renewable.hour_scenarios`
- `renewable.block_generation` to `renewable.block_scenarios`
- `renewable_gauging_station.hour_generation` to `renewable_gauging_station.hour_scenarios`
- `renewable_gauging_station.block_generation` to `renewable_gauging_station.block_scenarios`
- `renewable_gauging_station.hour_historical_generation` to `renewable_gauging_station.hour_historical_scenarios`

### Changed
- disabled tab behavior when there are sub tabs

### Fixed
- `exp:to_hour(BY_AVERAGE())`
- `hblock` loading when `--model none` and there is no duraci
- error adding the same tab to a dashboard more the once
- error converting to csv when the binary has negative stages
- intermittent error loading an output on linux
- `system.load_level_length` floating point approximation

### Submodules
- PSRClasses updated
- Highlight.js `11.6.0` -> `11.7.0`
- KaTeX `0.16.3` -> `0.16.4`

## 0.19.0 (2022-12-15)

### Added
- new AWS S3 downloader
- `exp:select_scenarios(int, int)`
- `tab:set_disabled()`
- `tab:set_collapsed(boolean)`
- `study:has_hour_block_map()`
- `study:get_parameter(string, string)`
- `concatenate_blocks(...)`
- `info(std::vector<std::string>)`
- `ConcentratedSolarPower` collection (variables: hour_generation)
- `ElectrificationDemand` collection
- `ElectrificationDemandSegment` collection (variables: hour, block, cost, hour_price)
- `ElectrificationNetwork` collection
- `ElectrificationNode` collection
- `ElectrificationProcess` collection
- `ElectrificationProducer` collection
- `ElectrificationStorage` collection
- `ElectrificationTransport` collection
- `GasEmission` collection (variables: code, cost)
- `GasNode` collection (variables: code, production_cost_constraint)
- `Load` collection (variables: code, bus, hour_bus)
- `ReservoirSet` collection (variables: code, security_energy, flood_control_energy, alert_energy)
- `dclink.wheeling_cost_from` and `dclink.wheeling_cost_to`
- `fuel.min_consumption`, `fuel.max_consumption` and `fuel.availability`
- `system.carbon_credit_cost`
- `thermal.startup_cost_constraint`, `thermal.spinning_reserve`, `thermal.max_reserve`, and `thermal.bid_price`
- `balancing_area.regulation_up` and `balancing_area.regulation_down`
- `demand.variable_block_duration`
- `demand_segment.hour_price` and `demand_segment.block_price`
- error check in `exp:to_block()` and `exp:to_hour()` when the case has no hour block map

### Syntax Changes
- `study:is_hourly_load()` to `study:has_hourly_load()`
- `circuit.existing` to `circuit.state`
- `dclink.existing` to `dclink.state`
- `generation_constraint.existing` to `generation_constraint.state`
- `generation_constraint.capacity` to `generation_constraint.data`
- `hydro.existing` to `hydro.state`
- `renewable.existing` to `renewable.state`
- `thermal.existing` to `thermal.state`

### Fixed
- docs publish (tag)
- errors in concatenate_stages and concatenate_scenarios when first_stage > 1
- add_index_translation
- active tab when the first ones are disabled
- error when creating the output path

### Removed
- `thermal.forced_generation`
- `include` folder (julia users should use the PSRIO.jl package)

### Submodules
- AWS `1.9.379` added
- zlib `1.2.13` added
- AWS Integration updated 
- Bootstrap `5.2.2` -> `5.2.3`
- Bootstrap Icons `1.9.1` -> `1.10.2`
- S3Integrations removed 

## 0.18.0 (2022-11-21)

### Added
- `BY_ORDER(i)`
- `collection:inputs()`
- `study:stage_type()`, `study:blocks(stage)`, and `study:initial_stage()`
- `--load_from_output_path` reading in `collection:load_table(...)`
- `exp:moving(f, window)`
- `Profile.PER_QUARTER` and `Profile.QUARTER`
- `hydro.alert_storage_penalty` and `hydro.alert_storage_penalty_type`
- `hydro.min_total_outflow_penalty` and `hydro.min_total_outflow_penalty_type`
- `hydro.max_total_outflow_penalty` and `hydro.max_total_outflow_penalty_type`
- `hydro.min_spillage_penalty` and `hydro.min_spillage_penalty_type`
- `hydro.max_spillage_penalty` and `hydro.max_spillage_penalty_type`
- `hydro.max_turbining_penalty` and `hydro.max_turbining_penalty_type`
- `hydro.min_bio_spillage_penalty` and `hydro.min_bio_spillage_penalty_type`
- `hydro.min_turbining_penalty` and `hydro.min_turbining_penalty_type`
- `hydro.min_operative_storage_penalty` and `hydro.min_operative_storage_penalty_type`
- `hydro.max_operative_storage_penalty` and `hydro.max_operative_storage_penalty_type`

### Syntax Changes
- `study.blocks` to `study.blocks_per_stage`
- `hydro.capacity` to `hydro.max_generation`
- `hydro.capacity_maintenance` to `hydro.max_generation_available`
- `hydro.vmin` to `hydro.min_storage`
- `hydro.vmax` to `hydro.max_storage`
- `hydro.qmin` to `hydro.min_turbining_outflow`
- `hydro.qmax` to `hydro.max_turbining_outflow`
- `hydro.vmin_chronological_historical_scenarios_nodata` to `hydro.min_operative_storage_historical_scenarios_nodata`
- `hydro.vmin_chronological_historical_scenarios` to `hydro.min_operative_storage_historical_scenarios`
- `hydro.vmin_chronological` to `hydro.min_operative_storage`
- `hydro.vmax_chronological_historical_scenarios_nodata` to `hydro.max_operative_storage_historical_scenarios_nodata`
- `hydro.vmax_chronological_historical_scenarios` to `hydro.max_operative_storage_historical_scenarios`
- `hydro.vmax_chronological` to `hydro.max_operative_storage`

### Changed
- internal log structure
- internal compiler structure

### Fixed
- temporary psrclasses files leftovers error
- relationship error
- `--model none` parameters check
- `exp:to_hour(f, "hblock file")` and `exp:to_block(f, "hblock file")` error when the file does not exist

### Submodules
- KaTeX `0.16.2` -> `0.16.3`

## 0.17.0 (2022-10-19)

### Added
- `exp:sort_agents_descending()` and `exp:sort_agents_ascending()`
- `exp:uncouple_stages(clear_first_stage)`
- `ExpansionConstraint` and `ExpansionDecision` collections
- `base/sddp/vere15.lua`
- `hydro.max_turbining`, `hydro.spinning_reserve`, and `hydro.max_reserve`
- `thermal.alternative_fuel`
- `$` to favorite units
- CI/CD: psr-update-modules

### Syntax Changes
- `chart:add_heatmap(exp)` to `chart:add_heatmap_hourly(exp)`
- `generic:create(values, unit)` to `generic:create(label, unit, values)`
- `exp:sort_agents` to `exp:sort_agents_labels`
- `demand.maximum_increase` to `demand.max_increase`
- `demand.maximum_decrease` to `demand.max_decrease`
- `demand.maximum_curtailment` to `demand.max_curtailment`
- `hydro.omcost` to `hydro.om_cost`
- `hydro.FOR` to `hydro.forced_outage_rate`
- `hydro.COR` to `hydro.historical_outage_factor`
- `expansion_project.omcost` to `expansion_project.om_cost`
- `renewable.omcost` to `renewable.om_cost`
- `system.duraci` to `system.load_level_length`
- `system.hblock` to `system.hour_block_map`
- `thermal.omcost` to `thermal.om_cost`
- `thermal.germin` to `thermal.min_generation`
- `thermal.germin_maintenance` to `thermal.min_generation_available`
- `thermal.capacity` to `thermal.max_generation`
- `thermal.capacity_maintenance` to `thermal.max_generation_available`
- `thermal.FOR` to `thermal.forced_outage_rate`
- `thermal.COR` to `thermal.historical_outage_factor`
- `thermal.cesp1` to `thermal.specific_consumption_segment_1`
- `thermal.cesp2` to `thermal.specific_consumption_segment_2`
- `thermal.cesp3` to `thermal.specific_consumption_segment_3`
- `thermal.transport_cost` to `thermal.fuel_transportation_cost`
- `thermal.must_run` to `thermal.operation_mode`
- `thermal.minimum_uptime` to `thermal.min_uptime`
- `thermal.minimum_downtime` to `thermal.min_downtime`
- `thermal.maximum_startups` to `thermal.max_startups`
- `thermal.maximum_shutdowns` to `thermal.max_shutdowns`

### Fixed
- output selection
- `aggregate_stages` when the first_stage > 1
- missing columns when the series are added individually
- error when adding a chart more than once in the dashboard

### Submodules
- Bootstrap `5.2.1` -> `5.2.2`

## 0.16.0 (2022-09-21)

### Added
- `Tab` class
- dashboard submenu support
- `dashboard:set_icon(url)` and `dashboard:set_logo(url)`
- `exp:spread_blocks(blocks)`
- `exp:select_agents_by_regex(regex)` and `exp:remove_agents_by_regex(regex)`

### Fixed
- data literal when using a `--model none`
- `exp:to_block(f, "hblock file")`
- `exp:spread_stages()`

### Removed
- `Dashboard` concatenation operator (!)

### Submodules
- Bootstrap `5.2.1`
- GitHub Flavored Markdown `0.29.0.gfm.6`

## 0.15.0 (2022-09-02)

### Added
- improved CI/CD
- `PSR.assert_version(version)`, ex: `PSR.assert_version(=0.15.0)`, `PSR.assert_version(>0.15.0)`
- `collection:codes()`
- `exp:fill(value)`
- `BY_KTH_LARGEST(p)` and `BY_KTH_LARGEST_INDEX(p)`
- `BY_KTH_SMALLEST(p)` and `BY_KTH_SMALLEST_INDEX(p)`
- `BY_MAX_INDEX()` and `BY_MIN_INDEX()`
- `exp:reshape_stages(Profile.MONTH)`

### Syntax Changes
- `BY_NTH_ELEMENT(p)` to `BY_PERCENTILE_INDEX(p)`

### Changed
- `BY_NPV(pu)` to `BY_NPV(percent)`, ex: `BY_NPV(0.2)` to `BY_NPV(20)`

### Fixed
- `exp:select_agents({...})` with duplicate agents
- `exp:reshape_stages(Profile.DAY)` when exp has weekly stages

### Submodules
- GitHub Flavored Markdown `0.29.0.gfm.5`
- KaTeX `0.16.2`
- JSON `3.11.2`

## 0.14.3 (2022-08-19)

### Added
- CI/CD: notify on slack

### Fixed
- CI/CD: publish on master
- hourly scenarios data dimensions check
- `exp:aggregate_stages(f, profile)` initial stage

## 0.14.0 (2022-08-17)

### Added
- multi-language code syntax highlighting
- CI/CD via github actions
- require(...) access to .lua files next to the recipes  
- `exp:circuit_from()` and `exp:circuit_to()` to map buses to circuits
- `exp:dclink_from()` and `exp:dclink_to()` to map buses to dclinks
- relationship from buses to dclinks in `exp:aggregate_agents()`
- `exp:uncouple_blocks()`
- `exp:aggregate_slices(f, size)`

### Fixed
- units check in report
- data reading with "0/1" unit

## 0.13.0 (2022-07-28)

### Added
- subhourly support (1 min, 5 min, 10 min, 15 min, 20 min, 30 min)
- `TimeSeries` and `Relational` classes
- `FlowController` collection
- `chart:add_line_stacking(exp)`
- `#chart` length
- `study:initial_year()` and `study:final_year()`
- `collection.code` input data
- `exp:to_list(stage, scenario, block)` and `exp:to_int_list(stage, scenario, block)`
- `exp:remove_scenarios({int, ...})`
- `exp:spread_stages()`
- `compare:set_relative_tolerance(double)` and `compare:set_absolute_tolerance(double)`

### Syntax Changes
- `Compare(title, rtol = 1e-4, atol = 0)` to `Compare(title)`

### Changed
- lua `5.4.2` to `5.4.4`
- sol `3.2.3` to `3.3.0`
- feather-icons replaced by [lucide.dev](https://lucide.dev)
- `collection:load_table(...)` and `collection:load_table_without_header(...)` from now on it considers all data as string
- update to `0.29.0.gfm.4`

### Fixed
- utf8 encoding
- error in `concatenate_scenarios(...)`
- ternary operator when there were negative stages

### Removed
- psrclasses epoch check
- study:save_relationship(...)
- `--return_errors` argument

## 0.12.0 (2022-05-29)

### Added
- raw HTML parsing in markdown
- `chart:add_categories(exp, label)` and `chart:add_categories(exp1, exp2, label)`
- `chart:add_line(exp, {color = {"#9b5de5", "#f15bb5", ...}})`
- `study:save_relationship("filename", from, to)`
- `Topology.TURBINED_FROM`
- `concatenate_scenarios(exp1, exp2, ...)` and `clamp(exp, low, hi)`
- `exp:repeat_on_buffer_years()`
- `exp:to_hour(f, "hblock file")` and `exp:to_block(f, "hblock file")`
- `exp:force_blocks()`
- `exp:set_initial_stage(int)`
- `exp:select_agents(collection, {label1, label2, ...})`
- `exp:aggregate_stages(f, {stage1, stage2, ...})` and `exp:aggregate_scenarios_stages(f, {stage1, stage2, ...})`
- `exp:cumsum_agents()`
- `exp:fill_agents({int or string, int or string, ...}, value)`
- `collection:load_table_without_header("filename")`
- `psrclasses-netplan.dat` loading
- `--load_from_output_path` argument

### Syntax Changes
- `PSR.colors({"#ff0029", "#377eb8", ...})` to `PSR.set_global_colors({"#ff0029", "#377eb8", ...})`

### Changed
- improvements in dashboard frontend
- incremental progress bar in psrcloud

### Fixed
- error in `exp:select_agents(query)` when the attributes were different
- error in `exp:select_agents(collection, {label})` when there were multiple agents with the same label

## 0.11.0 (2022-04-11)

### Added
- dashboard frontend rework
- new unit matching algorithm
- input data dimensions check rework
- `--label name`, `--label code`, and `--label avid` arguments
- `--ignore_hrbmap` argument
- `exp:save(filename, {label="name"})`, `exp:save(filename, {label="code"})`, and `exp:save(filename, {label="avid"})`
- `exp:first_stage()`, `exp:last_stage()`, and `exp:code(index)`
- `Chart(title, subtitle)`
- `chart:add_spline(exp)`
- `chart:add_area_spline(exp)`, `chart:add_area_spline_stacking(exp)`, `chart:add_area_spline_percent(exp)`, and `chart:add_area_spline_range(exp1, exp2)`
- `exp:remove_agent(index)`, `exp:remove_agent(label)`, and `exp:rename_agent(label)`
- `exp:select_agent_by_code(code)` and `exp:select_agents_by_code({code1, code2, ...})`
- `exp:remove_agent_by_code(code)` and `exp:remove_agents_by_code({code1, code2, ...})`
- `exp:rename_agents_with_codes()`
- `exp:select_agents(collection, label)`
- `exp:spread_scenarios(scenarios)`
- `collection:language()`
- `study:get_parameter(key, double)`
- `PSR.colors({"#ff0029", "#377eb8", ...})` and `PSR.interpolate_colors("#ff0000", "#00ff00", 4)`
- `toml:get_array_size(key)` and `toml:get_array(key, i)`
- `sfd`, `R$` units

### Syntax Changes
- `exp:select_stages(stage)` to `exp:select_stage(stage)`
- `exp:select_stages(first_stage, -1)` to `exp:select_first_stage(first_stage)`
- `exp:select_stages(-1, last_stage)` to `exp:select_last_stage(last_stage)`
- `study:macro_agents(...)` to `collection:load_tag(...)`
- `study:load_table(filename)` to `collection:load_table(filename)`
- `study:load_toml(filename)` to `collection:load_toml(filename)`
- `study:get_parameter(key)` to `study:get_parameter(key, int)`
- `Compare(title, rtol = 1e-4)` to `Compare(title, rtol = 1e-4, atol = 0)`

### Fixed
- fast_csv warning when the csv was locked
- saving in a directory that does not exist

### Removed
- `--avid` argument
- `chart:add_line_stacking(exp)` and `chart:add_line_percent(exp)`

## 0.10.1 (2022-02-14)

### Fixed
- intermittent error in dependencies mode

## 0.10.0 (2022-02-07)

### Added
- improved error messages
- linear domain axis chart (stage_type = 0)
- `chart:add_heatmap(exp)` and `chart:save(filename, title)`
- `dashboard:set_icon(string)` based on [feathericons](https://feathericons.com)
- `collection:cloudname()`
- `collection:get_directories(regex)` and `collection:get_directories(subpath, regex)`
- `exp:select_agent(index)` and `exp:select_agent(label)`
- `exp:set_stage_type(int)`
- `exp:save(filename, {fast_csv = true})` and `exp:save(filename, {bin = true})`
- `exp:add_prefix(string)`
- `exp:rename_agent(string)`
- `exp:has_agent(label)`
- `exp:stages_to_agents()` and `exp:stages_to_agents(selected)`
- `PSR.sleep(seconds)` `PSR.version()`
- `info(table)`
- all aggregation functions in `exp:to_block(function)`

### Syntax Changes
- `study:load_table(filename)` no longer assume the extension is a .csv
- `exp:rename_agents_with_suffix(string)` to `exp:add_suffix(string)`

### Fixed
- `exp:select_scenarios({int, ...})` when the first stage was different than 1
- `chart:add_area_range(exp, exp) with data considering leap years

### Removed
- `exp:save(filename, {tmp = true})`

## 0.9.0 (2022-01-03)

### Added
- guards in the loading method to protect from psrclasses unknown error 
- `report:add_header(string)`
- `generic:create({value1, value2, ...})` and `generic:create({value1, value2, ...}, "unit")`
- `study:load_table(filename)` and `collection:get_files(regex)`
- `PSR.studies()`
- negative epoch 
- relationship thermal/hydro/renewable plant to network areas
- `CO`, `tCO` units

### Syntax Changes
- `add_index_translation` to `PSR.add_index_translation`

### Changed
- improvements in security
- improvements in report classes
- improvements in units classes
- improvements in makefile and psrcloud deploy
- argument `--recipes` can be a directory, and the psrio will search for all *.lua files 

### Fixed
- CVAR aggregation when the values were equal
- error in dependencies mode when saving a not selected output
- error loading an output with upper case filename in linux
- memory constraint on loading large hourly scenarios
- error in BY_SUM(), BY_MIN(), and BY_MAX() when there were no values to aggregate
- rollback to lua 5.4.2 (https://github.com/ThePhD/sol2/issues/1266)

## 0.8.0 (2021-11-18)

### Added
- LaTeX math support in markdown (`$$ ... $$`)
- `exp:select_agents(std::vector<std::string>)`
- `exp:replace(exp)`
- `int = study:get_parameter(string)`
- `exp:select_largest_agents(k)` and `exp:select_smallest_agents(k)`
- `study:openings()`
- `exp:sort_agents()`
- `Compare(title, epsilon = 1e-4)`
- `100` max errors in Compare 
- `sddpconfig.dat` reading
- `exp:force_collection(collection)`
- parm reference relationship 
- `--return_errors` argument

### Syntax Changes
- `study.stages` to `study:stages()`
- `study.stages_per_year` to `study:stages_per_year()`
- `study.scenarios` to `study:scenarios()`
- `study:parent_path()` to `study:dirname()`
- `collection:load(filename, true)` to `collection:load_or_error(filename)`

### Changed
- performance improvement in `concatenate(exp1, exp2, ...)`
- performance improvement in `exp:select_agents(query)`

### Fixed
- stderr when the case does not exists
- unit in power binary expression (^)
- study.discount_rate unit
- error using remove_zeros and horizon

## 0.7.0 (2021-09-24)

### Added
- new dashboard structure with markdown support
- multiple cases support
- output comparison with report files
- lua helpers, e.g. require("lua/spairs")
- `exp:rename_agents_with_suffix(string)`
- `exp:select_block(block)`
- `collection:load(filename, true)` to raise error if the file is not found
- `exp:force_unit(unit)`
- `exp = exp:save_cache()`
- `exp:aggregate_scenarios_stages(f)`
- `exp:remove_zeros()`
- `exp:aggregate_agents(f, group_size)`
- `exp:uncouple_stages()`
- `study:path()` and `study:parent_path()`
- `exp:set_initial_year(year)`
- `do_string(code)` (meta programming)
- `shift_stages(stages)`
- topology enumerate and `exp:aggregate_topology(f, topology)`
- `info(msg)`, `warning(msg)`, `error(msg)`
- forward and backward reading 

### Changed
- `exp:agents()` return a vector of lua objects
- unit conversion in logical binary expressions

### Fixed
- `exp:aggregate_stages()` in monthly-hourly cases
- missing blocks in binary expression
- eps in logical binary operations (lq, le, gt, ge)
- `exp:to_hour()` and `exp:to_block()` when the input has no blocks
- stderr not showing in the log in release mode
- optgen study loading

## 0.6.0 (2021-06-04)

### Added
- interactive mode (REPL)
- psrio-base and `require("<base>")`
- `include("<file>")` with relative directory
- runtime input data loading: `collection:load_vector(attribute, unit)` and `collection:load_parameter(attribute, unit)`
- `exp:select_stages(stage)`, `exp:select_stages_by_year(initial_year, final_year)`, `exp:reset_stages()`
- `exp:select_scenarios(scenario)` and `exp:select_scenarios({scenario})` [per stage]
- `exp:select_agents(query)`
- `exp:round(digits)`
- `exp:force_hourly()`
- `exp:save("<file>", { horizon = true })`
- attributes getters: 
    - `exp:loaded()`, `exp:unit()`, `exp:agents()`, `exp:agents_size()`,`exp:agent(int i)`, `exp:scenarios()`
    - `exp:stage_type()`, `exp:initial_year()`, `exp:initial_stage()`, `exp:stages()`, `exp:week(stage)`, `exp:month(stage)`, `exp:year(stage)`
    - `exp:blocks(int)`, `exp:has_blocks()`, `exp:is_hourly()`, `exp:to_list()`, `exp:to_int_list()` 
- `study:is_hourly()` and `study:is_genesys()` methods
- `pu` unit
- `add_index_translation(...)` and `macro_agents()` functions
- single binary support
- relationship from buses to circuits in `exp:aggregate_agents()`

### Changed
- added files in indice.grf even if it is not in indexdat.fmt
- deleted bin/hdr files in CSV mode

### Fixed
- several fixes of methods with first_stage > 1
- error handling when loading an output with the wrong collection
- error in concatenate when expression agents = 0
- input hourly data loading when there is no hour-block mapping file
- `exp:to_block()` and historical scenarios performance

### Removed
- variable_by_scenario metadata (variable_by_scenario = false is now scenarios = 1)
- `--skip` argument, now it is automatic

## 0.5.0 (2021-01-27)

### Added
- Lua
- dashboard support
- `--horizon <date>` to change to initial date
- `--model none` to load an empty study

### Syntax Changes
- several breaking changes due to Lua introduction

### Removed
- bison scanner and parser
- verbose 1f, 2f, and 3f (use 1, 2, or 3)

## 0.4.1 (2021-01-12)

### Added
- first and last stage attributes to all variables and operators
- `select_stages(exp, first_stage, last_stage)`
- `rename_agents(exp, [string, string, ...])`
- argument `--logname <string>` to rename the log files (`psrio.log` and `psrio-psrclasses.log` to `<string>.log` and `<string>-psrclasses.log`)

### Changed
- `crop_stages(exp)` is now `select_stages(exp)`

### Fixed
- `indexdat.fmt` concurrent access

## 0.4.0 (2020-12-01)

### Changed
- agents selection by order or name: `select_agents(exp, {int or string, int or string, ...})`
- scenarios selection parameter in aggregation: `aggregate_scenarios(type, exp, {int, int, ...})`

### Removed
- argument `--append`