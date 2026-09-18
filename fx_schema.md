
## fx_drivers

> Stores drivers of a company.

### Table
| Column                              | Type         | Nullable | Default           | Description                                       |
|-------------------------------------|--------------|----------|-------------------|---------------------------------------------------|
| id                                  | int8         | NO       |                   | Unique identifier of the driver                   |
| email                               | text         | YES      | NULL              |                                                   |
| first_name                          | text         | YES      | NULL              |                                                   | 
| last_name                           | text         | YES      | NULL              |                                                   |
| group_ids                           | int8[]       | YES      | NULL              |                                                   |
| company_reference_id                | int8         | YES      | NULL              |                                                   |
| phone                               | text         | YES      | NULL              |                                                   |
| phone_country_code                  | text         | YES      | NULL              |                                                   |
| phone_ext                           | text         | YES      | NULL              |                                                   |
| time_zone                           | text         | YES      | NULL              |                                                   |
| metric_units                        | boolean      | YES      | NULL              |                                                   |
| carrier_name                        | text         | YES      | NULL              |                                                   |
| carrier_street                      | text         | YES      | NULL              |                                                   |
| carrier_city                        | text         | YES      | NULL              |                                                   |
| carrier_state                       | text         | YES      | NULL              |                                                   |
| carrier_zip                         | text         | YES      | NULL              |                                                   |
| carrier_country                     | text         | YES      | NULL              |                                                   |
| violation_alerts                    | text         | YES      | NULL              |                                                   |
| terminal_street                     | text         | YES      | NULL              |                                                   |
| terminal_city                       | text         | YES      | NULL              |                                                   |
| terminal_state                      | text         | YES      | NULL              |                                                   |
| terminal_zip                        | text         | YES      | NULL              |                                                   |
| terminal_country                    | text         | YES      | NULL              |                                                   |
| cycle                               | text         | YES      | NULL              |                                                   |
| exception_24_hour_restart           | boolean      | YES      | NULL              |                                                   |
| exception_8_hour_break              | boolean      | YES      | NULL              |                                                   |
| exception_wait_time                 | boolean      | YES      | NULL              |                                                   |
| exception_short_haul                | boolean      | YES      | NULL              |                                                   |
| exception_ca_farm_school_bus        | boolean      | YES      | NULL              |                                                   |
| cycle2                              | text         | YES      | NULL              |                                                   |
| exception_24_hour_restart2          | boolean      | YES      | NULL              |                                                   |
| exception_8_hour_break2             | boolean      | YES      | NULL              |                                                   |
| exception_wait_time2                | boolean      | YES      | NULL              |                                                   |
| exception_short_haul2               | boolean      | YES      | NULL              |                                                   |
| exception_ca_farm_school_bus2       | boolean      | YES      | NULL              |                                                   |
| exception_adverse_driving           | boolean      | YES      | NULL              |                                                   |
| exception_adverse_driving2          | boolean      | YES      | NULL              |                                                   |
| export_combined                     | boolean      | YES      | NULL              |                                                   |
| export_recap                        | boolean      | YES      | NULL              |                                                   |
| export_odometers                    | boolean      | YES      | NULL              |                                                   |
| username                            | text         | YES      | NULL              |                                                   |
| driver_company_id                   | text         | YES      | NULL              |                                                   |
| minute_logs                         | boolean      | YES      | NULL              |                                                   |
| duty_status                         | text         | YES      | NULL              | Values: off_duty, on_duty                         |
| eld_mode                            | text         | YES      | NULL              |                                                   |
| drivers_license_number              | text         | YES      | NULL              |                                                   |
| drivers_license_state               | text         | YES      | NULL              |                                                   |
| drivers_license_country             | text         | YES      | NULL              |                                                   |
| yard_moves_enabled                  | boolean      | YES      | NULL              |                                                   |
| personal_conveyance_enabled         | boolean      | YES      | NULL              |                                                   |
| manual_driving_enabled              | boolean      | YES      | NULL              |                                                   |
| mobile_last_active_at               | timestamptz  | YES      | NULL              |                                                   |
| mobile_current_sign_in_at           | timestamptz  | YES      | NULL              |                                                   |
| mobile_last_sign_in_at              | timestamptz  | YES      | NULL              |                                                   |
| web_last_active_at                  | timestamptz  | YES      | NULL              |                                                   |
| role                                | text         | YES      | 'driver'          |                                                   |
| status                              | text         | YES      | NULL              | Values: active, deactivated                       |
| web_current_sign_in_at              | timestamptz  | YES      | NULL              |                                                   |
| web_last_sign_in_at                 | timestamptz  | YES      | NULL              |                                                   |
| external_ids                        | int8[]       | YES      | NULL              |                                                   |
| created_at                          | timestamptz  | NO       | now()             |                                                   |
| updated_at                          | timestamptz  | YES      | NULL              |                                                   |

### DDL
CREATE TABLE fx_drivers (
  id bigint not null,
  email text null,
  first_name text null,
  last_name text null,
  group_ids bigint[] null,
  company_reference_id bigint null,
  phone text null,
  phone_country_code text null,
  phone_ext text null,
  time_zone text null,
  metric_units boolean null,
  carrier_name text null,
  carrier_street text null,
  carrier_city text null,
  carrier_state text null,
  carrier_zip text null,
  carrier_country text null,
  violation_alerts text null,
  terminal_street text null,
  terminal_city text null,
  terminal_state text null,
  terminal_zip text null,
  terminal_country text null,
  cycle text null,
  exception_24_hour_restart boolean null,
  exception_8_hour_break boolean null,
  exception_wait_time boolean null,
  exception_short_haul boolean null,
  exception_ca_farm_school_bus boolean null,
  cycle2 text null,
  exception_24_hour_restart2 boolean null,
  exception_8_hour_break2 boolean null,
  exception_wait_time2 boolean null,
  exception_short_haul2 boolean null,
  exception_ca_farm_school_bus2 boolean null,
  exception_adverse_driving boolean null,
  exception_adverse_driving2 boolean null,
  export_combined boolean null,
  export_recap boolean null,
  export_odometers boolean null,
  username text null,
  driver_company_id text null,
  minute_logs boolean null,
  duty_status text null,
  eld_mode text null,
  drivers_license_number text null,
  drivers_license_state text null,
  drivers_license_country text null,
  yard_moves_enabled boolean null,
  personal_conveyance_enabled boolean null,
  manual_driving_enabled boolean null,
  mobile_last_active_at timestamp with time zone null,
  mobile_current_sign_in_at timestamp with time zone null,
  mobile_last_sign_in_at timestamp with time zone null,
  web_last_active_at timestamp with time zone null,
  role text null,
  status text null,
  web_current_sign_in_at timestamp with time zone null,
  web_last_sign_in_at timestamp with time zone null,
  external_ids bigint[] null,
  created_at timestamp with time zone not null default now(),
  updated_at timestamp with time zone null,
  constraint fx_drivers_pkey primary key (id),
  constraint fx_drivers_id_key unique (id)
);


## fx_vehicles

> Stores the vehicles of a company.

### Table
| Column                              | Type         | Nullable | Default           | Description                                       |
|-------------------------------------|--------------|----------|-------------------|---------------------------------------------------|
| id                                  | int8         | NO       |                   | Unique identifier of the vehicle                  |
| company_id                          | int8         | YES      | NULL              |                                                   |
| number                              | text         | YES      | NULL              | Company-defined vehicle identifier                |
| status                              | text         | YES      | NULL              | Values: active, deactivated                       |
| ifta                                | boolean      | YES      | NULL              | Is vehicle is subject to IFTA reporting?          |
| vin                                 | text         | YES      | NULL              | Vehicle Identification Number (VIN)               |
| make                                | text         | YES      | NULL              | Manufacturer of the vehicle                       |
| model                               | text         | YES      | NULL              | Model of the vehicle                              |
| year                                | text         | YES      | NULL              | Year the vehicle was manufactured                 |
| license_plate_state                 | text         | YES      | NULL              | State of the vehicle's license plate              |
| license_plate_number                | text         | YES      | NULL              | License plate number                              |
| license_plate_country_code          | text         | YES      | NULL              | ISO country code of the vehicle's license plate   |
| metric_units                        | boolean      | YES      | NULL              | Vehicle uses metric units?                        |
| fuel_type                           | text         | YES      | NULL              | Fuel type of the vehicle                          |
| prevent_auto_odometer_entry         | boolean      | YES      | NULL              |                                                   |
| notes                               | text         | YES      | NULL              |                                                   |
| driver_facing_camera                | int8         | YES      | NULL              | Assume: -1 is False, 1 is True                    |
| incab_audio_recording               | int8         | YES      | NULL              | Assume: -1 is False, 1 is True                    |
| incab_alert_live_stream_enable      | int8         | YES      | NULL              | Assume: -1 is False, 1 is True                    |
| group_ids                           | int8[]       | YES      | NULL              | Groups the vehicle belongs to                     |
| created_at                          | timestamptz  | YES      | NULL              | Vehicle creation datetime                         |
| updated_at                          | timestamptz  | YES      | NULL              | Datetime when availability status was updated     |
| availability_status                 | text         | YES      | NULL              | Values: in_service, out_of_service                |
| eld_device_id                       | int8         | YES      | NULL              |                                                   |
| eld_device_identifier               | text         | YES      | NULL              | Manufacturer-assigned serial number of ELD device |
| eld_device_model                    | text         | YES      | NULL              | Manufacturer model name of ELD device             |
| current_driver_id                   | int8         | YES      | NULL              | Unique identifier of vehicle's current driver     |
| external_ids                        | int8[]       | YES      | NULL              |                                                   |

### DDL
create table fx_vehicles (
  id bigint not null,
  company_id bigint null,
  number text null,
  status text null,
  ifta boolean null,
  vin text null,
  make text null,
  model text null,
  year text null,
  license_plate_state text null,
  license_plate_number text null,
  metric_units boolean null,
  fuel_type text null,
  prevent_auto_odometer_entry boolean null,
  notes text null,
  driver_facing_camera bigint null,
  incab_audio_recording bigint null,
  incab_alert_live_stream_enable bigint null,
  group_ids bigint[] null,
  created_at timestamp with time zone null,
  updated_at timestamp with time zone null,
  eld_device_id bigint null,
  eld_device_identifier text null,
  eld_device_model text null,
  current_driver_id bigint null,
  external_ids bigint[] null,
  availability_status text null,
  license_plate_country_code text null,
  constraint fx_vehicles_pkey primary key (id),
  constraint fx_vehicles_id_key unique (id),
  constraint fx_vehicles_number_key unique (number),
  constraint fx_vehicles_current_driver_id_fkey foreign KEY (current_driver_id) references fx_drivers (id)
);


## fx_latest_vehicle_locations

> Stores the most recent location, assigned driver, and telemetry snapshot for each vehicle in a company's fleet.

### Table
| Column                              | Type         | Nullable | Default           | Description                                       |
|-------------------------------------|--------------|----------|-------------------|---------------------------------------------------|
| vehicle_id                          | int8         | NO       |                   | Unique identifier of the vehicle                  |
| vehicle_number                      | text         | NO       | NULL              | Company-defined vehicle identifier                |
| driver_id                           | int8         | YES      | NULL              | Unique identifier of the current driver           |
| location_point                      | geography    | YES      | NULL              | Lat/Lon of the vehicle's current location         |
| location_time                       | timestamptz  | NO       | NULL              | Timestamp when the location data was recorded     |
| location_description                | text         | YES      | NULL              | Description of the vehicle's current location     |
| location_lat                        | float8       | NO       | NULL              | Latitude of the vehicle's current location        |
| location_lon                        | float8       | NO       | NULL              | Longitude of the vehicle's current location       |
| location_bearing                    | float8       | YES      | NULL              | Bearing of the vehicle, in degrees                |
| location_type                       | text         | YES      | NULL              | Type of movement or status of vehicle             |
| location_id                         | uuid         | YES      | NULL              | Unique identifier of the vehicle location         |
| h3cell                              | text[]       | YES      | NULL              | Hexagonal cell ids current location belongs to    |
| odometer                            | float8       | YES      | NULL              | Vehicle's odometer reading, in miles              |
| engine_hours                        | float8       | YES      | NULL              | Total engine hours of the vehicle                 |
| fuel_in_tank                        | float8       | YES      | NULL              | Current amount of fuel in the vehicle's tank      |
| speed                               | float8       | YES      | NULL              | The speed of the vehicle in miles per hour        |
| updated_at                          | timestamptz  | NO       | NULL              |                                                   |

### DDL
create table fx_latest_vehicle_locations (
  driver_id bigint null,
  location_point geography null,
  vehicle_id bigint not null,
  location_time timestamp with time zone not null,
  location_description text null,
  location_lat double precision not null,
  location_lon double precision not null,
  vehicle_number text not null,
  location_bearing double precision null,
  location_type text null,
  h3cell text[] null,
  odometer double precision null,
  engine_hours double precision null,
  fuel_in_tank double precision null,
  location_id uuid null default gen_random_uuid (),
  speed double precision null,
  updated_at timestamp with time zone not null default now(),
  constraint fx_latest_vehicle_locations_pkey primary key (vehicle_id),
  constraint fx_latest_vehicle_locations_vehicle_id_key unique (vehicle_id),
  constraint fx_latest_vehicle_locations_vehicle_id_fkey foreign KEY (vehicle_id) references fx_vehicles (id)
);
create index IF not exists fx_latest_vehicle_locations_location_point_idx on fx_latest_vehicle_locations using gist (location_point);


## fx_assets

> Stores the assets of a company.

### Table
| Column                              | Type         | Nullable | Default           | Description                                       |
|-------------------------------------|--------------|----------|-------------------|---------------------------------------------------|
| id                                  | int8         | NO       |                   | Unique identifier of the asset                    |
| name                                | text         | YES      | NULL              | Company-defined asset identifier                  |
| status                              | text         | YES      | NULL              | Values: active, deactivated                       |
| type                                | text         | YES      | NULL              | Type of asset                                     |
| custom_type                         | text         | YES      | NULL              | Custom type of asset, if applicable               |
| vin                                 | text         | YES      | NULL              | Vehicle Identification Number (VIN)               |
| make                                | text         | YES      | NULL              | Manufacturer of the asset                         |
| model                               | text         | YES      | NULL              | Model of the asset                                |
| year                                | text         | YES      | NULL              | Year the asset was manufactured                   |
| license_plate_state                 | text         | YES      | NULL              | State where asset's license plate is registered   |
| license_plate_number                | text         | YES      | NULL              | License plate number of the asset                 |
| axle                                | text         | YES      | NULL              | Number of axles on the asset                      |
| weight_metric_units                 | boolean      | YES      | NULL              | Is asset's weight measured in metric units?       |
| length_metric_units                 | boolean      | YES      | NULL              | Is asset's length measured in metric units?       |
| leased                              | boolean      | YES      | NULL              | Is asset leased?                                  |
| notes                               | text         | YES      | NULL              | Additional notes or information about the asset   |
| group_ids                           | int8[]       | YES      | NULL              | Groups the asset belongs to                       |
| length                              | float8       | YES      | NULL              | Length of the asset                               |
| gvwr                                | float8       | YES      | NULL              | Gross Vehicle Weight Rating (GVWR) of the asset   |
| gawr                                | float8       | YES      | NULL              | Gross Axle Weight Rating (GAWR) of the asset      |
| asset_gateway_id                    | int8         | YES      | NULL              |                                                   |
| asset_gateway_identifier            | text         | YES      | NULL              | Manufacturer-assigned serial number of gateway    |
| asset_gateway_active                | boolean      | YES      | NULL              | Is asset's gateway device active?                 |
| external_ids                        | int8[]       | YES      | NULL              |                                                   |
| availability_status                 | text         | YES      | NULL              | Values: in_service, out_of_service                | 

### DDL
create table fx_assets (
  id bigint not null,
  name text null,
  status text null,
  type text null,
  custom_type text null,
  vin text null,
  license_plate_state text null,
  license_plate_number text null,
  make text null,
  model text null,
  year text null,
  axle text null,
  weight_metric_units boolean null,
  length_metric_units boolean null,
  leased boolean null,
  notes text null,
  group_ids bigint[] null,
  length double precision null,
  gvwr double precision null,
  gawr double precision null,
  asset_gateway_id bigint null,
  asset_gateway_identifier text null,
  asset_gateway_active boolean null,
  external_ids bigint[] null,
  availability_status text null,
  constraint fx_assets_pkey primary key (id),
  constraint fx_assets_id_key unique (id)
);


## fx_geofences

> Store geofences of a company.

### Table
| Column                              | Type         | Nullable | Default           | Description                                       |
|-------------------------------------|--------------|----------|-------------------|---------------------------------------------------|
| id                                  | int8         | NO       |                   | Unique identifier of the geofence                 |
| name                                | text         | YES      | NULL              | Name of the geofence                              |
| category                            | text         | YES      | NULL              | Category of the geofence                          |
| status                              | text         | YES      | NULL              | Values: active, deactivated                       |
| address                             | text         | YES      | NULL              | Physical address associated with the geofence     |
| description                         | text         | YES      | NULL              |                                                   |
| location_points                     | geography    | YES      | NULL              | Points that define the boundaries of the geofence |
| centroid                            | geography    | YES      | NULL              | Geometric balancing point of the geofence         |
| h3cell                              | text[]       | YES      | NULL              | Hexagonal cell ids the geofence belongs to        |
| area                                | float8       | YES      | NULL              | Geodesic area of the geofence, in square meters   |

### DDL
create table fx_geofences (
  id bigint generated by default as identity not null,
  name text null,
  category text null,
  status text null,
  address text null,
  description text null,
  location_points geography null,
  centroid geography null,
  h3cell text[] null,
  area double precision null,
  constraint fx_geofences_pkey primary key (id)
);


## fx_fault_codes

> Stores vehicle fault codes.

### Table
| Column                              | Type         | Nullable | Default           | Description                                           |
|-------------------------------------|--------------|----------|-------------------|-------------------------------------------------------|
| id                                  | int8         | NO       |                   | Unique identifier of the fault code                   |
| code                                | text         | YES      | NULL              | The fault code as reported by the vehicle             |
| code_label                          | text         | YES      | NULL              | Label associated with the fault code                  |
| code_description                    | text         | YES      | NULL              | Description of the fault code                         |
| source_address_label                | text         | YES      | NULL              | Label for the source address                          |
| status                              | text         | YES      | NULL              | Status of the fault code (e.g. open, closed)          |
| first_observed_at                   | timestamptz  | YES      | NULL              | When the fault code was first observed                |
| last_observed_at                    | timestamptz  | YES      | NULL              | When the fault code was last observed                 |
| type                                | text         | YES      | NULL              | Type of fault code (e.g. constant, intermittent)      |
| fmi                                 | text         | YES      | NULL              | Failure Mode Identifier (additional detail)           |
| occurrence_count                    | int4         | YES      | NULL              | Number of times the fault code has occurred           |
| num_observations                    | int4         | YES      | NULL              | Number of times the fault code was observed           |
| sum_num_observations                | int4         | YES      | NULL              | Cumulative number of observations for fault code      |
| source_address_name                 | text         | YES      | NULL              | Name associated with the source address               |
| source_address                      | text         | YES      | NULL              | Source address from which the fault code originated   |
| is_sid                              | boolean      | YES      | NULL              | Is code a System Identification Number (SID)?         |
| fmi_description                     | text         | YES      | NULL              | Description of the Failure Mode Identifier            |
| dtc_status                          | text         | YES      | NULL              | Status of the Diagnostic Trouble Code                 |
| dtc_severity                        | text         | YES      | NULL              | Severity of the Diagnostic Trouble Code               |
| functional_grp_id                   | int4         | YES      | NULL              | Functional group identifier                           |
| ftb                                 | text         | YES      | NULL              | Fault code Trouble Board identifier                   |
| eld_device_id                       | int8         | YES      | NULL              | Unique identifier for the Vehicle Gateway             |
| eld_device_identifier               | text         | YES      | NULL              | The identifier of the Vehicle Gateway                 |
| eld_device_model                    | text         | YES      | NULL              | The model of the Vehicle Gateway                      |
| vehicle_id                          | int8         | NO       |                   | Unique identifier for the associated vehicle          |
| network                             | text         | YES      | NULL              | Network through which the fault code was communicated |

### DDL
create table fx_fault_codes (
  id bigint generated by default as identity not null,
  code text null,
  code_label text null,
  code_description text null,
  source_address_label text null,
  status text null,
  first_observed_at timestamp with time zone null,
  last_observed_at timestamp with time zone null,
  type text null,
  fmi text null,
  occurrence_count integer null,
  num_observations integer null,
  sum_num_observations integer null,
  source_address_name text null,
  source_address text null,
  is_sid boolean null,
  fmi_description text null,
  dtc_status text null,
  dtc_severity text null,
  functional_grp_id integer null,
  ftb text null,
  eld_device_id bigint null,
  eld_device_identifier text null,
  eld_device_model text null,
  vehicle_id bigint not null,
  network text null,
  constraint fx_fault_codes_pkey primary key (id),
  constraint fx_fault_codes_vehicle_id_fkey foreign KEY (vehicle_id) references fx_vehicles (id)
);


## Entity Relationships

### Plain-English Summary
A **Driver** can be assigned to one **Vehicle** at a time. Each **Vehicle** has one current **Latest Vehicle Location** record representing its most recent telemetry snapshot, which may also reveal the currently assigned **Driver**. **Assets** are non-vehicle fleet items such as trailers and equipment, tracked separately from vehicles.

**Geofences** define named geographic boundaries used for monitoring and alerting, mapped spatially via PostGIS geometry and H3 cell indices. **Fault Codes** record diagnostic trouble codes generated by a vehicle's onboard computer — both open and closed — and are updated in place as the vehicle's status changes rather than appended as new rows.

### Relationship Table
| From                 | Relationship | To                          | Via (FK)                                                           |
|----------------------|--------------|-----------------------------|--------------------------------------------------------------------|
| fx_drivers           | has one      | fx_vehicles                 | fx_vehicles.current_driver_id → fx_drivers.id                      |
| fx_vehicles          | has one      | fx_latest_vehicle_locations | fx_latest_vehicle_locations.vehicle_id → fx_vehicles.id            |
| fx_vehicles          | has many     | fx_fault_codes              | fx_fault_codes.vehicle_id → fx_vehicles.id                         |

### Notes
- `fx_latest_vehicle_locations` is a snapshot table — it stores only the most recent location per vehicle, not a history.
- `fx_geofences` has no FK relationships — geofence monitoring is done elsewhere and mapping is done using PostGIS (location_points, centroid) or the h3cell array.
- `cd_assets` has no FK relationships to drivers or vehicles — assets are tracked independently and linked only through card assignment.
- `fx_fault_codes` stores fault codes that are updated in place — `status` moves from `open` → `closed`, `last_observed_at` advances, and `occurrence_count` increments. Do not treat rows as immutable; always read the current state rather than assuming historical rows reflect past states.
- H3 cell arrays (`h3cell`) on `fx_latest_vehicle_locations` store 16 resolution levels (0–15) generated at insert time. Postgres arrays are 1-indexed, so `h3cell[1]` = resolution 0 (coarsest) and `h3cell[16]` = resolution 15 (finest).| export_combined                     | boolean      | YES      | NULL              |                                                   |
| export_recap                        | boolean      | YES      | NULL              |                                                   |
| export_odometers                    | boolean      | YES      | NULL              |                                                   |
| username                            | text         | YES      | NULL              |                                                   |
| driver_company_id                   | text         | YES      | NULL              |                                                   |
| minute_logs                         | boolean      | YES      | NULL              |                                                   |
| duty_status                         | text         | YES      | NULL              | Values: off_duty, on_duty                         |
| eld_mode                            | text         | YES      | NULL              |                                                   |
| drivers_license_number              | text         | YES      | NULL              |                                                   |
| drivers_license_state               | text         | YES      | NULL              |                                                   |
| yard_moves_enabled                  | boolean      | YES      | NULL              |                                                   |
| personal_conveyance_enabled         | boolean      | YES      | NULL              |                                                   |
| manual_driving_enabled              | boolean      | YES      | NULL              |                                                   |
| mobile_last_active_at               | timestamptz  | YES      | NULL              |                                                   |
| mobile_current_sign_in_at           | timestamptz  | YES      | NULL              |                                                   |
| mobile_last_sign_in_at              | timestamptz  | YES      | NULL              |                                                   |
| web_last_active_at                  | timestamptz  | YES      | NULL              |                                                   |
| role                                | text         | YES      | 'driver'          |                                                   |
| status                              | text         | YES      | NULL              | Values: active, deactivated                       |
| web_current_sign_in_at              | timestamptz  | YES      | NULL              |                                                   |
| web_last_sign_in_at                 | timestamptz  | YES      | NULL              |                                                   |
| external_ids                        | int8         | YES      | NULL              |                                                   |
| created_at                          | timestamptz  | NO       | now()             |                                                   |
| updated_at                          | timestamptz  | YES      | NULL              |                                                   |

### DDL
CREATE TABLE fx_drivers (
  id bigint not null,
  email text null,
  first_name text null,
  last_name text null,
  group_ids bigint[] null,
  company_reference_id bigint null,
  phone text null,
  phone_country_code text null,
  phone_ext text null,
  time_zone text null,
  metric_units boolean null,
  carrier_name text null,
  carrier_street text null,
  carrier_city text null,
  carrier_state text null,
  carrier_zip text null,
  violation_alerts text null,
  terminal_street text null,
  terminal_city text null,
  terminal_state text null,
  terminal_zip text null,
  cycle text null,
  exception_24_hour_restart boolean null,
  exception_8_hour_break boolean null,
  exception_wait_time boolean null,
  exception_short_haul boolean null,
  exception_ca_farm_school_bus boolean null,
  cycle2 text null,
  exception_24_hour_restart2 boolean null,
  exception_8_hour_break2 boolean null,
  exception_wait_time2 boolean null,
  exception_short_haul2 boolean null,
  exception_ca_farm_school_bus2 boolean null,
  exception_adverse_driving boolean null,
  exception_adverse_driving2 boolean null,
  export_combined boolean null,
  export_recap boolean null,
  export_odometers boolean null,
  username text null,
  driver_company_id text null,
  minute_logs boolean null,
  duty_status text null,
  eld_mode text null,
  drivers_license_number text null,
  drivers_license_state text null,
  yard_moves_enabled boolean null,
  personal_conveyance_enabled boolean null,
  manual_driving_enabled boolean null,
  mobile_last_active_at timestamp with time zone null,
  mobile_current_sign_in_at timestamp with time zone null,
  mobile_last_sign_in_at timestamp with time zone null,
  web_last_active_at timestamp with time zone null,
  role text null,
  status text null,
  web_current_sign_in_at timestamp with time zone null,
  web_last_sign_in_at timestamp with time zone null,
  external_ids bigint[] null,
  created_at timestamp with time zone not null default now(),
  updated_at timestamp with time zone null,
  constraint fx_drivers_pkey primary key (id),
  constraint fx_drivers_id_key unique (id)
);


## fx_vehicles

> Stores the vehicles of a company.

### Table
| Column                              | Type         | Nullable | Default           | Description                                       |
|-------------------------------------|--------------|----------|-------------------|---------------------------------------------------|
| id                                  | int8         | NO       |                   | Unique identifier of the vehicle                  |
| company_id                          | int8         | YES      | NULL              |                                                   |
| number                              | text         | YES      | NULL              | Company-defined vehicle identifier                |
| status                              | text         | YES      | NULL              | Values: active, deactivated                       |
| ifta                                | boolean      | YES      | NULL              | Is vehicle is subject to IFTA reporting?          |
| vin                                 | text         | YES      | NULL              | Vehicle Identification Number (VIN)               |
| make                                | text         | YES      | NULL              | Manufacturer of the vehicle                       |
| model                               | text         | YES      | NULL              | Model of the vehicle                              |
| year                                | text         | YES      | NULL              | Year the vehicle was manufactured                 |
| license_plate_state                 | text         | YES      | NULL              | State of the vehicle's license plate              |
| license_plate_number                | text         | YES      | NULL              | License plate number                              |
| license_plate_country_code          | text         | YES      | NULL              | ISO country code of the vehicle's license plate   |
| metric_units                        | boolean      | YES      | NULL              | Vehicle uses metric units?                        |
| fuel_type                           | text         | YES      | NULL              | Fuel type of the vehicle                          |
| prevent_auto_odometer_entry         | boolean      | YES      | NULL              |                                                   |
| notes                               | text         | YES      | NULL              |                                                   |
| driver_facing_camera                | int8         | YES      | NULL              | Assume: -1 is False, 1 is True                    |
| incab_audio_recording               | int8         | YES      | NULL              | Assume: -1 is False, 1 is True                    |
| incab_alert_live_stream_enable      | int8         | YES      | NULL              | Assume: -1 is False, 1 is True                    |
| group_ids                           | int8[]       | YES      | NULL              | Groups the vehicle belongs to                     |
| created_at                          | timestamptz  | YES      | NULL              | Vehicle creation datetime                         |
| updated_at                          | timestamptz  | YES      | NULL              | Datetime when availability status was updated     |
| availability_status                 | text         | YES      | NULL              | Values: in_service, out_of_service                |
| eld_device_id                       | int8         | YES      | NULL              |                                                   |
| eld_device_identifier               | text         | YES      | NULL              | Manufacturer-assigned serial number of ELD device |
| eld_device_model                    | text         | YES      | NULL              | Manufacturer model name of ELD device             |
| current_driver_id                   | int8         | YES      | NULL              | Unique identifier of vehicle's current driver     |
| external_ids                        | int8[]       | YES      | NULL              |                                                   |

### DDL
create table fx_vehicles (
  id bigint not null,
  company_id bigint null,
  number text null,
  status text null,
  ifta boolean null,
  vin text null,
  make text null,
  model text null,
  year text null,
  license_plate_state text null,
  license_plate_number text null,
  metric_units boolean null,
  fuel_type text null,
  prevent_auto_odometer_entry boolean null,
  notes text null,
  driver_facing_camera bigint null,
  incab_audio_recording bigint null,
  incab_alert_live_stream_enable bigint null,
  group_ids bigint[] null,
  created_at timestamp with time zone null,
  updated_at timestamp with time zone null,
  eld_device_id bigint null,
  eld_device_identifier text null,
  eld_device_model text null,
  current_driver_id bigint null,
  external_ids bigint[] null,
  availability_status text null,
  license_plate_country_code text null,
  constraint fx_vehicles_pkey primary key (id),
  constraint fx_vehicles_id_key unique (id),
  constraint fx_vehicles_number_key unique (number),
  constraint fx_vehicles_current_driver_id_fkey foreign KEY (current_driver_id) references fx_drivers (id)
);


## fx_latest_vehicle_locations

> Stores the most recent location, assigned driver, and telemetry snapshot for each vehicle in a company's fleet.

### Table
| Column                              | Type         | Nullable | Default           | Description                                       |
|-------------------------------------|--------------|----------|-------------------|---------------------------------------------------|
| vehicle_id                          | int8         | NO       |                   | Unique identifier of the vehicle                  |
| vehicle_number                      | text         | YES      | NULL              | Company-defined vehicle identifier                |
| driver_id                           | int8         | YES      | NULL              | Unique identifier of the current driver           |
| location_point                      | geography    | YES      | NULL              | Lat/Lon of the vehicle's current location         |
| location_time                       | timestamptz  | YES      | NULL              | Timestamp when the location data was recorded     |
| location_description                | text         | YES      | NULL              | Description of the vehicle's current location     |
| location_lat                        | float8       | YES      | NULL              | Latitude of the vehicle's current location        |
| location_lon                        | float8       | YES      | NULL              | Longitude of the vehicle's current location       |
| location_bearing                    | float8       | YES      | NULL              | Bearing of the vehicle, in degrees                |
| location_type                       | text         | YES      | NULL              | Type of movement or status of vehicle             |
| h3cell                              | text[]       | YES      | NULL              | Hexagonal cell ids current location belongs to    |
| odometer                            | float8       | YES      | NULL              | Vehicle's odometer reading, in miles              |
| engine_hours                        | float8       | YES      | NULL              | Total engine hours of the vehicle                 |
| fuel_in_tank                        | float8       | YES      | NULL              | Current amount of fuel in the vehicle's tank      |

### DDL
create table fx_latest_vehicle_locations (
  driver_id bigint null,
  location_point geography null,
  vehicle_id bigint not null,
  location_time timestamp with time zone null,
  location_description text null,
  location_lat double precision null,
  location_lon double precision null,
  vehicle_number text not null,
  location_bearing double precision null,
  location_type text null,
  h3cell text[] null,
  odometer double precision null,
  engine_hours double precision null,
  fuel_in_tank double precision null,
  constraint fx_latest_vehicle_locations_pkey primary key (vehicle_id),
  constraint fx_latest_vehicle_locations_vehicle_id_key unique (vehicle_id),
  constraint fx_latest_vehicle_locations_driver_id_fkey foreign KEY (driver_id) references fx_drivers (id),
  constraint fx_latest_vehicle_locations_vehicle_id_fkey foreign KEY (vehicle_id) references fx_vehicles (id)
);


## fx_assets

> Stores the assets of a company.

### Table
| Column                              | Type         | Nullable | Default           | Description                                       |
|-------------------------------------|--------------|----------|-------------------|---------------------------------------------------|
| id                                  | int8         | NO       |                   | Unique identifier of the asset                    |
| name                                | text         | YES      | NULL              | Company-defined asset identifier                  |
| status                              | text         | YES      | NULL              | Values: active, deactivated                       |
| type                                | text         | YES      | NULL              | Type of asset                                     |
| custom_type                         | text         | YES      | NULL              | Custom type of asset, if applicable               |
| vin                                 | text         | YES      | NULL              | Vehicle Identification Number (VIN)               |
| make                                | text         | YES      | NULL              | Manufacturer of the asset                         |
| model                               | text         | YES      | NULL              | Model of the asset                                |
| year                                | text         | YES      | NULL              | Year the asset was manufactured                   |
| license_plate_state                 | text         | YES      | NULL              | State where asset's license plate is registered   |
| license_plate_number                | text         | YES      | NULL              | License plate number of the asset                 |
| axle                                | text         | YES      | NULL              | Number of axles on the asset                      |
| weight_metric_units                 | boolean      | YES      | NULL              | Is asset's weight measured in metric units?       |
| length_metric_units                 | boolean      | YES      | NULL              | Is asset's length measured in metric units?       |
| leased                              | boolean      | YES      | NULL              | Is asset leased?                                  |
| notes                               | text         | YES      | NULL              | Additional notes or information about the asset   |
| group_ids                           | int8[]       | YES      | NULL              | Groups the asset belongs to                       |
| length                              | float8       | YES      | NULL              | Length of the asset                               |
| gvwr                                | float8       | YES      | NULL              | Gross Vehicle Weight Rating (GVWR) of the asset   |
| gawr                                | float8       | YES      | NULL              | Gross Axle Weight Rating (GAWR) of the asset      |
| asset_gateway_id                    | int8         | YES      | NULL              |                                                   |
| asset_gateway_identifier            | text         | YES      | NULL              | Manufacturer-assigned serial number of gateway    |
| asset_gateway_active                | boolean      | YES      | NULL              | Is asset's gateway device active?                 |
| external_ids                        | int8[]       | YES      | NULL              |                                                   |
| availability_status                 | text         | YES      | NULL              | Values: in_service, out_of_service                | 

### DDL
create table fx_assets (
  id bigint not null,
  name text null,
  status text null,
  type text null,
  custom_type text null,
  vin text null,
  license_plate_state text null,
  license_plate_number text null,
  make text null,
  model text null,
  year text null,
  axle text null,
  weight_metric_units boolean null,
  length_metric_units boolean null,
  leased boolean null,
  notes text null,
  group_ids bigint[] null,
  length double precision null,
  gvwr double precision null,
  gawr double precision null,
  asset_gateway_id bigint null,
  asset_gateway_identifier text null,
  asset_gateway_active boolean null,
  external_ids bigint[] null,
  availability_status text null,
  constraint fx_assets_pkey primary key (id),
  constraint fx_assets_id_key unique (id)
);


## fx_geofences

> Store geofences of a company.

### Table
| Column                              | Type         | Nullable | Default           | Description                                       |
|-------------------------------------|--------------|----------|-------------------|---------------------------------------------------|
| id                                  | int8         | NO       |                   | Unique identifier of the geofence                 |
| name                                | text         | YES      | NULL              | Name of the geofence                              |
| category                            | text         | YES      | NULL              | Category of the geofence                          |
| status                              | text         | YES      | NULL              | Values: active, deactivated                       |
| address                             | text         | YES      | NULL              | Physical address associated with the geofence     |
| description                         | text         | YES      | NULL              |                                                   |
| location_points                     | geography    | YES      | NULL              | Points that define the boundaries of the geofence |
| centroid                            | geography    | YES      | NULL              | Geometric balancing point of the geofence         |
| h3cell                              | text[]       | YES      | NULL              | Hexagonal cell ids the geofence belongs to        |
| area                                | float8       | YES      | NULL              | Geodesic area of the geofence, in square meters   |

### DDL
create table fx_geofences (
  id bigint generated by default as identity not null,
  name text null,
  category text null,
  status text null,
  address text null,
  description text null,
  location_points geography null,
  created_at timestamp with time zone not null default now(),
  centroid geography null,
  h3cell text[] null,
  area double precision null,
  constraint fx_geofences_pkey primary key (id)
)

## fx_events

> Stores drivers' performance events, including speeding.

### Table
| Column                              | Type         | Nullable | Default           | Description                                       |
|-------------------------------------|--------------|----------|-------------------|---------------------------------------------------|
| id                                  | int8         | NO       |                   | Unique identifier of the event                    |
| acceleration                        | float8       | YES      |                   | Acceleration during the event, in g-force         |
| duration                            | int8         | YES      |                   | Duration of the event, in seconds                 |
| end_bearing                         | float8       | YES      |                   | Bearing at the end of the event, in degrees       |
| end_speed                           | float8       | YES      |                   | Speed at the end of the event, in km/h            |
| end_time                            | timestampz   | YES      |                   |                                                   |
| end_point                           | geography    | YES      |                   | Lat/Lon of event end location                     |
| m_gps_heading                       | float8[]     | YES      |                   | Array of GPS headings during the event            |
| m_gps_points                        | geography[]  | YES      |                   | Array of Lat/Lon during the event                 |
| m_veh_odo                           | float8       | YES      | NULL              | Odometer reading during the event                 |
| m_veh_spd                           | float8[]     | YES      |                   | Array of vehicle speeds during the event, in km/h |
| start_bearing                       | float8       | YES      |                   | Bearing at the start of the event, in degrees     |
| start_speed                         | float8       | YES      |                   | Speed at the start of the event, in km/h          |
| start_time                          | timestampz   | YES      |                   |                                                   |
| type                                | text         | YES      |                   | Type of performance event                         |
| type_pretty                         | text         | YES      |                   | Type of performance event, for display            |
| driver_id                           | int8         | YES      |                   | Unique identifier of the driver                   |
| vehicle_id                          | int8         | YES      |                   | Unique identifier of the vehicle                  |
| eld_device_id                       | int8         | YES      |                   | Unique identifier of the ELD device               |
| eld_device_identifier               | text         | YES      |                   | ELD device identifier                             |
| eld_device_model                    | text         | YES      |                   | ELD device model                                  |
| camera_media_id                     | int8         | YES      |                   | Unique identifier of the camera media             |
| camera_media_available              | boolean      | YES      | NULL              |                                                   |
| camera_media_front_facing_video_url | text         | YES      |                   |                                                   |
| camera_media_front_facing_photo_url | text         | YES      |                   |                                                   |
| camera_type                         | text         | YES      | NULL              |                                                   |
| company_name                        | text         | YES      |                   |                                                   |
| location                            | text         | YES      |                   |                                                   |
| coaching_status                     | text         | YES      |                   | Coaching status of the event                      |
| coached_at                          | timestampz   | YES      |                   |                                                   |
| max_speed                           | float8       | YES      |                   |                                                   |
| min_speed                           | float8       | YES      |                   |                                                   |
| edited_by_fm                        | boolean      | YES      | FALSE             |                                                   |
| annotation_tags                     | text[]       | YES      |                   | Annotation tags for the event                     |
| severity                            | text         | YES      |                   | Severity of the event                             |
| event_intensity_name                | text         | YES      |                   |                                                   |
| event_intensity_value               | text         | YES      |                   |                                                   |
| min_time_to_hit_range               | float8       | YES      |                   | Min time to hit, in seconds                       |
| max_time_to_hit_range               | float8       | YES      |                   | Max time to hit, in seconds                       |
| speeding_distance                   | float8       | YES      |                   | Speeding event: distance traveled while speeding  |
| max_over_speed                      | float8       | YES      |                   | Speeding event: max speed over posted limit       |
| avg_over_speed                      | float8       | YES      |                   | Speeding event: avg speed over posted limit       |
| min_posted_speed_limit              | float8       | YES      |                   | Speeding event: min posted speed limit            |
| max_posted_speed_limit              | float8       | YES      |                   | Speeding event: max posted speed limit            |
| avg_vehicle_speed                   | float8       | YES      |                   | Speeding event: avg vehicle speed during event    |
| min_vehicle_speed                   | float8       | YES      |                   | Speeding event: min vehicle speed during event    |
| max_vehicle_speed                   | float8       | YES      |                   | Speeding event: max vehicle speed during event    |
| start_point                         | geography    | YES      |                   | Speeding event: Lat/Long of event start location  |
| type_of_speeding                    | text         | YES      |                   | Speeding event: Type, e.g. "posted"               |
| speeding_event_status               | text         | YES      |                   | Speeding event: Status, e.g. "invalid"            |

### DDL
create table fx_events (
  id bigint not null,
  acceleration double precision null,
  duration bigint null,
  end_bearing double precision null,
  end_speed double precision null,
  end_time timestamp with time zone null,
  end_point geography null,
  m_gps_heading double precision[] null,
  m_gps_points geography null,
  m_veh_odo double precision null,
  m_veh_spd double precision[] null,
  start_bearing double precision null,
  start_speed double precision null,
  start_time timestamp with time zone null,
  type text null,
  type_pretty text null,
  driver_id bigint null,
  vehicle_id bigint null,
  eld_device_id bigint null,
  eld_device_identifier text null,
  eld_device_model text null,
  camera_media_id bigint null,
  camera_media_available boolean null,
  camera_media_front_facing_video_url text null,
  camera_media_front_facing_image_url text null,
  camera_type text null,
  company_name text null,
  location text null,
  coaching_status text null,
  coached_at timestamp with time zone null,
  max_speed double precision null,
  min_speed double precision null,
  edited_by_fm boolean null,
  annotation_tags text[] null,
  severity text null,
  created_at timestamp with time zone not null default now(),
  event_intensity_name text null,
  event_intensity_value text null,
  min_time_to_hit_range double precision null,
  max_time_to_hit_range double precision null,
  speeding_distance double precision null,
  max_over_speed double precision null,
  avg_over_speed double precision null,
  min_posted_speed_limit double precision null,
  max_posted_speed_limit double precision null,
  avg_speed double precision null,
  start_point geography null,
  type_of_speeding text null,
  speeding_event_status text null,
  constraint fx_events_pkey primary key (id),
  constraint fx_events_id_key unique (id),
  constraint fx_events_driver_id_fkey foreign KEY (driver_id) references fx_drivers (id),
  constraint fx_events_vehicle_id_fkey foreign KEY (vehicle_id) references fx_vehicles (id)
)


## Entity Relationships

### Plain-English Summary
A **Driver** can be assigned to one **Vehicle** at a time. Each **Vehicle** has one current **Latest Vehicle Location** record, which may also reveal the currently assigned **Driver**. **Assets** are non-vehicle fleet items (trailers, equipment, etc.).

**Events** capture driver performance incidents (speeding, hard braking, etc.) and are linked to both a **Driver** and a **Vehicle**. **Geofences** define geographic boundaries and can be mapped spatially via location_points / h3cell.

### Relationship Table
| From                 | Relationship | To                          | Via (FK)                                                           |
|----------------------|--------------|-----------------------------|--------------------------------------------------------------------|
| fx_drivers           | has one      | fx_vehicles                 | fx_vehicles.current_driver_id → fx_drivers.id                      |
| fx_vehicles          | has one      | fx_latest_vehicle_locations | fx_latest_vehicle_locations.vehicle_id → fx_vehicles.id            |
| fx_drivers           | has one      | fx_latest_vehicle_locations | fx_latest_vehicle_locations.driver_id → fx_drivers.id              |
| fx_drivers           | has many     | fx_events                   | fx_events.driver_id → fx_drivers.id                                |
| fx_vehicles          | has many     | fx_events                   | fx_events.vehicle_id → fx_vehicles.id                              |

### Notes
- A `fx_cards` row can be assigned to a driver, vehicle, or asset — but the schema doesn't enforce mutual exclusivity. When querying card assignments, check which of the three `assigned_to_*` columns is non-null.
- `fx_latest_vehicle_locations` is a snapshot table — it stores only the most recent location per vehicle, not a history.
- `fx_geofences has no FK relationships — geofence monitoring is likely done elsewhere and mapping is likely done using PostGIS (location_points) or the h3cell array.
