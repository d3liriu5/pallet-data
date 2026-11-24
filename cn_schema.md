
## cn_drivers

> Stores drivers of a company.

### Table
| Column                              | Type         | Nullable | Default           | Description                                       |
|-------------------------------------|--------------|----------|-------------------|---------------------------------------------------|
| id                                  | int8         | NO       |                   | Unique identifier of the driver                   |
| email                               | text         | YES      | NULL              |                                                   |
| first_name                          | text         | YES      | NULL              |                                                   | 
| last_name                           | text         | YES      | NULL              |                                                   |
| group_ids                           | int8[]       | YES      | NULL              |                                                   |
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
| created_at                          | timestamptz  | NO       | now()             |                                                   |
| updated_at                          | timestamptz  | YES      | NULL              |                                                   |

### DDL
CREATE TABLE cn_drivers (
  id bigint not null,
  email text null,
  first_name text null,
  last_name text null,
  group_ids bigint[] null,
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
  created_at timestamp with time zone not null default now(),
  updated_at timestamp with time zone null,
  constraint cn_drivers_pkey primary key (id),
  constraint cn_drivers_id_key unique (id)
);


## cn_vehicles

> Stores the vehicles of a company.

### Table
| Column                              | Type         | Nullable | Default           | Description                                       |
|-------------------------------------|--------------|----------|-------------------|---------------------------------------------------|
| id                                  | int8         | NO       |                   | Unique identifier of the vehicle                  |
| number                              | text         | YES      | NULL              | Company-defined vehicle identifier                |
| status                              | text         | YES      | NULL              | Values: active, deactivated                       |
| ifta                                | boolean      | YES      | NULL              | Is vehicle is subject to IFTA reporting?          |
| vin                                 | text         | YES      | NULL              | Vehicle Identification Number (VIN)               |
| make                                | text         | YES      | NULL              | Manufacturer of the vehicle                       |
| model                               | text         | YES      | NULL              | Model of the vehicle                              |
| year                                | text         | YES      | NULL              | Year the vehicle was manufactured                 |
| license_plate_state                 | text         | YES      | NULL              | State of the vehicle's license plate              |
| license_plate_number                | text         | YES      | NULL              | License plate number                              |
| license_plate_country               | text         | YES      | NULL              | ISO country code of the vehicle's license plate   |
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

### DDL
create table cn_vehicles (
  id bigint not null,
  number text null,
  status text null,
  ifta boolean null,
  vin text null,
  make text null,
  model text null,
  year text null,
  license_plate_state text null,
  license_plate_number text null,
  license_plate_country text null,
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
  availability_status text null,
  constraint cn_vehicles_pkey primary key (id),
  constraint cn_vehicles_id_key unique (id),
  constraint cn_vehicles_current_driver_id_fkey foreign KEY (current_driver_id) references cn_drivers (id)
);
create index IF not exists idx_cn_vehicles_current_driver on cn_vehicles using btree (current_driver_id);


## cn_vehicle_locations

> Stores the locations of vehicles.

### Table
| Column                              | Type         | Nullable | Default           | Description                                       |
|-------------------------------------|--------------|----------|-------------------|---------------------------------------------------|
| id                                  | uuid         | NO       |                   | Unique identifier of the vehicle location         |
| vehicle_id                          | int8         | NO       |                   | Unique identifier of the vehicle                  |
| vehicle_number                      | text         | NO       |                   | Company-defined vehicle identifier                |
| location_time                       | timestamptz  | NO       |                   | Timestamp when the location data was recorded     |
| location_point                      | geography    | YES      | NULL              | Lat/Lon of the vehicle's current location         |
| location_description                | text         | YES      | NULL              | Description of the vehicle's current location     |
| location_lat                        | float8       | NO       |                   | Latitude of the vehicle's current location        |
| location_lon                        | float8       | NO       |                   | Longitude of the vehicle's current location       |
| location_bearing                    | float8       | YES      | NULL              | Bearing of the vehicle, in degrees                |
| location_type                       | text         | YES      | NULL              | Type of movement or status of vehicle             |
| h3cell                              | text[]       | YES      | NULL              | Hexagonal cell ids current location belongs to    |
| odometer                            | float8       | YES      | NULL              | Vehicle's odometer reading, in miles              |
| engine_hours                        | float8       | YES      | NULL              | Total engine hours of the vehicle                 |
| fuel_in_tank                        | float8       | YES      | NULL              | Current amount of fuel in the vehicle's tank      |
| speed                               | float8       | YES      | NULL              | Speed of the vehicle at time of location (in mph) |
| created_at                          | timestamptz  | NO       |                   |                                                   |
| driver_id                           | int8         | YES      | NULL              | Unique identifier of the current driver           |

### DDL
create table cn_vehicle_locations (
  id uuid not null default gen_random_uuid (),
  vehicle_id bigint not null,
  vehicle_number text not null,
  location_time timestamp with time zone not null,
  location_point geography null,
  location_description text null,
  location_lat double precision not null,
  location_lon double precision not null,
  location_type text null,
  location_bearing double precision null,
  h3cell text[] null,
  odometer double precision null,
  engine_hours double precision null,
  fuel_in_tank double precision null,
  speed double precision null,
  created_at timestamp with time zone not null default now(),
  driver_id bigint null,
  constraint cn_vehicle_locations_partitioned_pkey primary key (id, location_time)
)
partition by
  RANGE (location_time);
create index IF not exists idx_cn_vehicle_locations_driver_time on only cn_vehicle_locations using btree (driver_id, location_time desc);
create index IF not exists idx_cn_vehicle_locations_h3cell on only cn_vehicle_locations using gin (h3cell);
create index IF not exists idx_cn_vehicle_locations_time on only cn_vehicle_locations using btree (location_time desc);
create index IF not exists idx_cvl_p_vehicle_location_time on only cn_vehicle_locations using btree (vehicle_id, location_time desc);
create index IF not exists idx_cvl_p_location_point on only cn_vehicle_locations using gist (location_point);
create index IF not exists idx_cvl_p_location_time on only cn_vehicle_locations using btree (location_time desc);
create index IF not exists idx_cn_vehicle_locations_point on only cn_vehicle_locations using gist (location_point);


## cn_latest_vehicle_locations

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
create table cn_latest_vehicle_locations (
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
  constraint cn_latest_vehicle_locations_pkey primary key (vehicle_id),
  constraint cn_latest_vehicle_locations_vehicle_id_key unique (vehicle_id),
  constraint cn_latest_vehicle_locations_vehicle_id_fkey foreign KEY (vehicle_id) references cn_vehicles (id)
);
create index IF not exists cn_latest_vehicle_locations_location_point_idx on cn_latest_vehicle_locations using gist (location_point);
create index IF not exists idx_cn_latest_vehicle_locations_driver on cn_latest_vehicle_locations using btree (driver_id);
create index IF not exists idx_cn_latest_vehicle_locations_h3cell on cn_latest_vehicle_locations using gin (h3cell);


## cn_assets

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
| license_plate_country               | text         | YES      | NULL              | Country where asset's license plate is registered |
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
create table cn_assets (
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
  constraint cn_assets_pkey primary key (id),
  constraint cn_assets_id_key unique (id)
);


## cn_geofences

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
| created_at                          | timestamptz  | NO       |                   |                                                   |

### DDL
create table cn_geofences (
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
  constraint cn_geofences_pkey primary key (id)
);
create index IF not exists cn_geofences_centroid_idx on cn_geofences using gist (centroid);
create index IF not exists idx_cn_geofences_h3cell on cn_geofences using gin (h3cell);
create index IF not exists idx_cn_geofences_location_points on cn_geofences using gist (location_points);


## cn_events

> Stores drivers' performance events, including speeding.

### Table
| Column                               | Type         | Nullable | Default           | Description                                       |
|--------------------------------------|--------------|----------|-------------------|---------------------------------------------------|
| id                                   | int8         | NO       |                   | Unique identifier of the event                    |
| acceleration                         | float8       | YES      |                   | Acceleration during the event, in g-force         |
| duration                             | int8         | YES      |                   | Duration of the event, in seconds                 |
| end_bearing                          | float8       | YES      |                   | Bearing at the end of the event, in degrees       |
| end_speed                            | float8       | YES      |                   | Speed at the end of the event, in km/h            |
| end_time                             | timestamptz  | YES      |                   |                                                   |
| end_point                            | geography    | YES      |                   | Lat/Lon of event end location                     |
| m_gps_heading                        | float8[]     | YES      |                   | Array of GPS headings during the event            |
| m_gps_points                         | geography    | YES      |                   | Array of Lat/Lon during the event                 |
| m_veh_odo                            | float8       | YES      | NULL              | Odometer reading during the event                 |
| m_veh_spd                            | float8[]     | YES      |                   | Array of vehicle speeds during the event, in km/h |
| start_bearing                        | float8       | YES      |                   | Bearing at the start of the event, in degrees     |
| start_speed                          | float8       | YES      |                   | Speed at the start of the event, in km/h          |
| start_time                           | timestamptz  | YES      |                   |                                                   |
| type                                 | text         | YES      |                   | Type of performance event                         |
| type_pretty                          | text         | YES      |                   | Type of performance event, for display            |
| driver_id                            | int8         | YES      |                   | Unique identifier of the driver                   |
| vehicle_id                           | int8         | YES      |                   | Unique identifier of the vehicle                  |
| eld_device_id                        | int8         | YES      |                   | Unique identifier of the ELD device               |
| eld_device_identifier                | text         | YES      |                   | ELD device identifier                             |
| eld_device_model                     | text         | YES      |                   | ELD device model                                  |
| camera_media_id                      | int8         | YES      |                   | Unique identifier of the camera media             |
| camera_media_available               | boolean      | YES      | NULL              |                                                   |
| camera_media_front_facing_video_url  | text         | YES      |                   |                                                   |
| camera_media_front_facing_image_url  | text         | YES      |                   |                                                   |
| camera_media_driver_facing_video_url | text         | YES      |                   |                                                   |
| camera_media_driver_facing_image_url | text         | YES      |                   |                                                   |
| camera_type                          | text         | YES      | NULL              |                                                   |
| company_name                         | text         | YES      |                   |                                                   |
| location                             | text         | YES      |                   |                                                   |
| coaching_status                      | text         | YES      |                   | Coaching status of the event                      |
| coached_at                           | timestamptz  | YES      |                   |                                                   |
| edited_by_fm                         | boolean      | YES      | FALSE             |                                                   |
| annotation_tags                      | text[]       | YES      |                   | Annotation tags for the event                     |
| severity                             | text         | YES      |                   | Severity of the event                             |
| event_intensity_name                 | text         | YES      |                   |                                                   |
| event_intensity_value                | text         | YES      |                   |                                                   |
| min_time_to_hit_range                | float8       | YES      |                   | Min time to hit, in seconds                       |
| max_time_to_hit_range                | float8       | YES      |                   | Max time to hit, in seconds                       |
| speeding_distance                    | float8       | YES      |                   | Speeding event: distance traveled while speeding  |
| max_over_speed                       | float8       | YES      |                   | Speeding event: max speed over posted limit       |
| avg_over_speed                       | float8       | YES      |                   | Speeding event: avg speed over posted limit       |
| min_posted_speed_limit               | float8       | YES      |                   | Speeding event: min posted speed limit            |
| max_posted_speed_limit               | float8       | YES      |                   | Speeding event: max posted speed limit            |
| max_speed                            | float8       | YES      |                   |                                                   |
| min_speed                            | float8       | YES      |                   |                                                   |
| avg_speed                            | float8       | YES      |                   |                                                   |
| start_point                          | geography    | YES      |                   | Speeding event: Lat/Long of event start location  |
| speeding_event_type                  | text         | YES      |                   | Speeding event: Type, e.g. "posted"               |
| speeding_event_status                | text         | YES      |                   | Speeding event: Status, e.g. "invalid"            |

### DDL
create table cn_events (
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
  speeding_event_type text null,
  speeding_event_status text null,
  camera_media_driver_facing_video_url text null,
  camera_media_driver_facing_image_url text null,
  constraint cn_events_pkey primary key (id),
  constraint cn_events_id_key unique (id),
  constraint cn_events_driver_id_fkey foreign KEY (driver_id) references cn_drivers (id),
  constraint cn_events_vehicle_id_fkey foreign KEY (vehicle_id) references cn_vehicles (id)
);
create index IF not exists idx_cn_events_start_time on cn_events using btree (start_time desc);
create index IF not exists idx_cn_events_vehicle_start on cn_events using btree (vehicle_id, start_time desc);
create index IF not exists idx_cn_events_driver_start on cn_events using btree (driver_id, start_time desc);
create index IF not exists idx_cn_events_type_start on cn_events using btree (type, start_time desc);


## Entity Relationships

### Plain-English Summary
A **Driver** can be assigned to one **Vehicle** at a time. Each **Vehicle** has one current **Latest Vehicle Location** record, which may also reveal the currently assigned **Driver**. **Assets** are non-vehicle fleet items (trailers, equipment, etc.).

**Geofences** define named geographic boundaries used for monitoring and alerting, mapped spatially via PostGIS geometry and H3 cell indices. **Events** capture driver performance incidents (speeding, hard braking, etc.) and are associated with a vehicle and optionally a driver.

### Relationship Table
| From                 | Relationship | To                          | Via (FK)                                                           |
|----------------------|--------------|-----------------------------|--------------------------------------------------------------------|
| cn_drivers           | has one      | cn_vehicles                 | cn_vehicles.current_driver_id → cn_drivers.id                      |
| cn_vehicles          | has one      | cn_latest_vehicle_locations | cn_latest_vehicle_locations.vehicle_id → cn_vehicles.id            |
| cn_drivers           | has many     | cn_vehicle_locations        | cn_vehicle_locations.driver_id → cn_drivers.id                     |
| cn_vehicles          | has many     | cn_vehicle_locations        | cn_vehicle_locations.vehicle_id → cn_vehicles.id                   |
| cn_drivers           | has many     | cn_events                   | cn_events.driver_id → cn_drivers.id                                |
| cn_vehicles          | has many     | cn_events                   | cn_events.vehicle_id → cn_vehicles.id                              |


## Database Functions

### cn_get_trips_by_vehicle

> Detects and summarizes trips for a vehicle over a date range. Populates the left column trip list on the vehicle history page.

**Parameters**
| Parameter       | Type        | Default | Description                                          |
|-----------------|-------------|---------|------------------------------------------------------|
| p_vehicle_id    | bigint      |         | Unique identifier of the vehicle                     |
| p_start_time    | timestamptz |         | Start of the date range                              |
| p_end_time      | timestamptz |         | End of the date range                                |
| p_min_stop_mins | int         | 5       | Minutes of inactivity between pings to define a stop |

**Returns**
| Column             | Type        | Description                                     |
|--------------------|-------------|-------------------------------------------------|
| trip_number        | int         | Sequential trip number within the date range    |
| trip_start         | timestamptz | Timestamp of the first ping in the trip         |
| trip_end           | timestamptz | Timestamp of the last ping in the trip          |
| duration_mins      | numeric     | Duration of the trip in minutes                 |
| distance_km        | numeric     | Distance traveled during the trip in kilometers |
| start_description  | text        | Location description at trip start              |
| end_description    | text        | Location description at trip end                |
| max_speed          | numeric     | Maximum speed recorded during the trip in mph   |
| avg_speed          | numeric     | Average speed recorded during the trip in mph   |
| ping_count         | bigint      | Number of location pings in the trip            |

**Notes**
- Trip boundaries are detected when the gap between consecutive pings exceeds `p_min_stop_mins`, or when `location_type = 'engine_off'`.
- Trips with only one ping are excluded (`HAVING COUNT(*) > 1`).
- Distance is calculated by summing `ST_Distance` between consecutive pings within each trip.

---

### cn_get_pings_by_trip

> Returns every individual location ping between a trip's start and end time for a specific vehicle. Used to draw the route polyline on the map when a user selects a trip.

**Parameters**
| Parameter    | Type        | Description                      |
|--------------|-------------|----------------------------------|
| p_vehicle_id | bigint      | Unique identifier of the vehicle |
| p_trip_start | timestamptz | Start timestamp of the trip      |
| p_trip_end   | timestamptz | End timestamp of the trip        |

**Returns**
| Column               | Type             | Description                           |
|----------------------|------------------|---------------------------------------|
| location_time        | timestamptz      | Timestamp when the ping was recorded  |
| lat                  | double precision | Latitude of the ping                  |
| lon                  | double precision | Longitude of the ping                 |
| bearing              | double precision | Bearing of the vehicle in degrees     |
| speed                | double precision | Speed of the vehicle in mph           |
| location_type        | text             | Type of movement or status            |
| location_description | text             | Human-readable location description   |
| odometer             | double precision | Odometer reading in miles             |
| engine_hours         | double precision | Total engine hours at time of ping    |

**Notes**
- Results are ordered by `location_time ASC`.
- Use `trip_start` and `trip_end` from `cn_get_trips_by_vehicle` as inputs.

---

### cn_get_routes_by_vehicle

> Returns all pings for all trips in a date range with the trip number attached. Used to draw accumulated route lines on the map, one colored polyline per trip.

**Parameters**
| Parameter       | Type        | Default | Description                                          |
|-----------------|-------------|---------|------------------------------------------------------|
| p_vehicle_id    | bigint      |         | Unique identifier of the vehicle                     |
| p_start_time    | timestamptz |         | Start of the date range                              |
| p_end_time      | timestamptz |         | End of the date range                                |
| p_min_stop_mins | int         | 5       | Minutes of inactivity between pings to define a stop |

**Returns**
| Column               | Type             | Description                                 |
|----------------------|------------------|---------------------------------------------|
| trip_number          | int              | Trip number — use to group pings by trip    |
| location_time        | timestamptz      | Timestamp when the ping was recorded        |
| lat                  | double precision | Latitude of the ping                        |
| lon                  | double precision | Longitude of the ping                       |
| bearing              | double precision | Bearing of the vehicle in degrees           |
| speed                | double precision | Speed of the vehicle in mph                 |
| location_type        | text             | Type of movement or status                  |
| location_description | text             | Human-readable location description         |

**Notes**
- Uses the same trip detection logic as `cn_get_trips_by_vehicle` — trip numbers are consistent between the two functions.
- Results are ordered by `trip_number, location_time ASC`.
- Group by `trip_number` in the frontend to draw one polyline per trip.

---

### cn_get_positions_at

> Returns each vehicle's most recent location ping at or before a given point in time. Used to reconstruct where the fleet was at a specific moment — for playback, historical snapshots, or time-scrubbing on the map.

**Parameters**
| Parameter  | Type        | Default  | Description                                                              |
|------------|-------------|----------|--------------------------------------------------------------------------|
| p_time     | timestamptz |          | The point in time to look up — returns pings at or before this timestamp |
| p_lookback | interval    | 24 hours | How far back to search for each vehicle's most recent ping               |

**Returns**
| Column               | Type        | Description                                 |
|----------------------|-------------|---------------------------------------------|
| vehicle_id           | text        | Unique identifier of the vehicle            |
| driver_id            | text        | Unique identifier of the assigned driver    |
| vehicle_number       | text        | Company-defined vehicle identifier          |
| location_time        | timestamptz | Timestamp of the ping                       |
| location_lat         | float8      | Latitude at the time of the ping            |
| location_lon         | float8      | Longitude at the time of the ping           |
| location_bearing     | float8      | Bearing of the vehicle in degrees           |
| location_type        | text        | Type of movement or status of vehicle       |
| speed                | float8      | Speed of the vehicle in mph                 |
| location_description | text        | Human-readable location description         |
| odometer             | float8      | Odometer reading in miles                   |
| engine_hours         | float8      | Total engine hours at time of ping          |
| fuel_in_tank         | float8      | Fuel in tank at time of ping                |

**Notes**
- Returns one row per vehicle — the most recent ping within the lookback window at or before `p_time`.
- Vehicles with no pings in the lookback window are excluded from results.
- `vehicle_id` and `driver_id` are returned as `text` to prevent JavaScript precision loss on large `bigint` values.

---

### lab_ids

> Helper function that validates and converts an array of text IDs to `bigint[]`. Returns `NULL` when the input is null or empty, which is treated as "no filter" by the list functions. Raises an exception if any value is not a valid integer.

**Parameters**
| Parameter | Type   | Description                        |
|-----------|--------|------------------------------------|
| p         | text[] | Array of ID strings to validate    |

**Returns** `bigint[]` — validated IDs, or `NULL` if input is null or empty.

**Notes**
- Called internally by `lab_list_events` and `lab_list_entities` before passing ID filters to queries.
- Raises `22023` if any value in the array is not a valid integer (1–18 digits).

---

### lab_list_events

> Returns a paged list of safety events with optional filtering, sorting, and search. Supports a grouped mode that buckets results by vehicle group. Security invoker — RLS policies on `cn_events` apply.

**Parameters**
| Parameter            | Type        | Default      | Description                                                          |
|----------------------|-------------|--------------|----------------------------------------------------------------------|
| p_limit              | int         | 25           | Page size (1–200)                                                    |
| p_offset             | int         | 0            | Page offset (0–100000)                                               |
| p_sort               | text        | start_time   | Sort column: `start_time`, `type`, `severity`, `driver`, `vehicle`, `coaching_status`, `max_over_speed` |
| p_dir                | text        | desc         | Sort direction: `asc` or `desc`                                      |
| p_search             | text        | null         | Free-text search across driver name, vehicle number, type, location  |
| p_start              | timestamptz | null         | Filter events with `start_time >=` this value                        |
| p_end                | timestamptz | null         | Filter events with `start_time <` this value                         |
| p_types              | text[]      | null         | Filter by event `type` values                                        |
| p_severities         | text[]      | null         | Filter by `severity` values                                          |
| p_coaching_statuses  | text[]      | null         | Filter by `coaching_status` values                                   |
| p_driver_ids         | text[]      | null         | Filter by driver IDs (passed as text to preserve JS precision)       |
| p_vehicle_ids        | text[]      | null         | Filter by vehicle IDs (passed as text)                               |
| p_group_ids          | text[]      | null         | Filter by vehicle group IDs — matches events whose vehicle belongs to any of these groups |
| p_grouped            | boolean     | false        | When `true`, returns grouped mode response instead of flat list      |
| p_max_groups         | int         | 25           | Grouped mode: max number of groups to return (1–100)                 |
| p_rows_per_group     | int         | 10           | Grouped mode: max rows per group (1–50)                              |

**Returns (flat mode)**
```json
{
  "total": 1240,
  "limit": 25,
  "offset": 0,
  "rows": [{ "id": "...", "type": "...", ... }]
}
```

**Returns (grouped mode)**
```json
{
  "total": 1240,
  "group_total": 8,
  "groups": [{ "group_id": "123", "count": 312, "rows": [...] }]
}
```

**Notes**
- Date range filters on `start_time` only — events are intervals, not points in time.
- Group filtering (`p_group_ids`) matches against the **vehicle's** `group_ids`, not the driver's.
- Camera URLs and GPS/speed arrays are excluded from list rows for performance. Fetch the full event record separately if needed.
- IDs in the response are returned as `text` to prevent JavaScript precision loss on large `bigint` values.
- Empty arrays (`'{}'`) passed as filter parameters are treated the same as `NULL` (no filter).

---

### lab_list_entities

> Returns a paged list of drivers, vehicles, or assets with optional filtering, sorting, search, and grouping. Security invoker — RLS policies on the underlying `cn_*` table apply.

**Parameters**
| Parameter        | Type    | Default | Description                                                                          |
|------------------|---------|---------|--------------------------------------------------------------------------------------|
| p_entity         | text    |         | Entity type: `drivers`, `vehicles`, or `assets`                                      |
| p_limit          | int     | 25      | Page size (1–200)                                                                    |
| p_offset         | int     | 0       | Page offset (0–100000)                                                               |
| p_sort           | text    | null    | Sort column — allowlisted per entity (see Notes)                                     |
| p_dir            | text    | asc     | Sort direction: `asc` or `desc`                                                      |
| p_search         | text    | null    | Free-text search — searched fields vary by entity (see Notes)                        |
| p_statuses       | text[]  | null    | Filter by `status` values (e.g. `active`, `deactivated`)                             |
| p_availability   | text[]  | null    | Filter by `availability_status` — applies to vehicles and assets only                |
| p_group_ids      | text[]  | null    | Filter by group IDs — matches entities whose `group_ids` contains any of these       |
| p_grouped        | boolean | false   | When `true`, returns grouped mode response instead of flat list                      |
| p_max_groups     | int     | 25      | Grouped mode: max number of groups to return (1–100)                                 |
| p_rows_per_group | int     | 10      | Grouped mode: max rows per group (1–50)                                              |

**Sort columns by entity**
| Entity   | Allowed values                                              | Default  |
|----------|-------------------------------------------------------------|----------|
| drivers  | `name`, `status`, `created_at`, `last_active`               | `name`   |
| vehicles | `number`, `status`, `availability`, `make`, `model`, `year`, `created_at` | `number` |
| assets   | `name`, `status`, `type`, `availability`, `make`, `model`, `year` | `name` |

**Search fields by entity**
| Entity   | Fields searched                                                      |
|----------|----------------------------------------------------------------------|
| drivers  | first + last name, email, username, driver_company_id                |
| vehicles | number, VIN, make, model, license_plate_number                       |
| assets   | name, VIN, make, model, license_plate_number, type, custom_type      |

**Returns (flat mode)**
```json
{
  "total": 842,
  "limit": 25,
  "offset": 0,
  "rows": [{ "id": "...", "number": "...", ... }]
}
```

**Returns (grouped mode)**
```json
{
  "total": 842,
  "group_total": 12,
  "groups": [{ "group_id": "123", "count": 94, "rows": [...] }]
}
```

**Notes**
- `p_availability` is silently ignored for drivers since `cn_drivers` has no `availability_status` column.
- IDs in the response are returned as `text` to prevent JavaScript precision loss.
- Group filtering matches against the entity's own `group_ids`, unlike `lab_list_events` which uses the vehicle's group IDs.

---

### lab_list_group_options

> Returns a list of group IDs with member counts for use in filter dropdowns. There is no separate groups table — options are derived from the `group_ids` arrays on the entity tables. Security invoker.

**Parameters**
| Parameter | Type   | Default | Description                                                                  |
|-----------|--------|---------|------------------------------------------------------------------------------|
| p_entity  | text   |         | Entity type: `drivers`, `vehicles`, `assets`, or `events`                    |
| p_search  | text   | null    | Numeric prefix search on group ID                                            |
| p_limit   | int    | 50      | Max options to return (1–200)                                                |
| p_offset  | int    | 0       | Offset (0–100000)                                                            |

**Returns**
```json
{
  "total": 14,
  "options": [{ "group_id": "9007199254740993", "count": 312 }]
}
```

**Notes**
- `p_entity = 'events'` returns group options from `cn_vehicles` — Safety Events are filtered by vehicle group membership, not driver group.
- Options are ordered by count descending.
- There is no label for group IDs — only the numeric ID and member count are available.

---

### lab_event_filter_options

> Returns distinct values with counts for a given event filter field, optionally scoped to a date window. Used to populate filter dropdowns dynamically. Security invoker.

**Parameters**
| Parameter | Type        | Default | Description                                                         |
|-----------|-------------|---------|---------------------------------------------------------------------|
| p_field   | text        |         | Field to enumerate: `type`, `severity`, or `coaching_status`        |
| p_search  | text        | null    | Free-text search on value or label                                  |
| p_start   | timestamptz | null    | Scope counts to events with `start_time >=` this value              |
| p_end     | timestamptz | null    | Scope counts to events with `start_time <` this value               |
| p_limit   | int         | 50      | Max options to return (1–200)                                       |

**Returns**
```json
{
  "options": [{ "value": "speeding", "label": "Speeding", "count": 487 }]
}
```

**Notes**
- `type` returns both `value` (raw `type`) and `label` (`type_pretty`). `severity` and `coaching_status` return the same string for both.
- Scoping by date range (`p_start` / `p_end`) returns counts that match the current list filter, keeping dropdown counts accurate to what the user is looking at.
- Options are ordered by count descending.


## Notes
- `cn_latest_vehicle_locations` is a snapshot table — it stores only the most recent location per vehicle, not a history. It is updated in place on every location ping via upsert on `vehicle_id`.
- `cn_vehicle_locations` is partitioned by day and stores a rolling 15-day history of location pings. Partitions older than 15 days are dropped nightly via pg_cron. Querying beyond 15 days will return no results.
- `cn_events` stores safety and performance events (speeding, harsh braking, etc.) from the past two weeks — filter on `type` for programmatic use, display `type_pretty` in the UI.
- Events cover an interval, not a point in time. Always filter on `start_time` rather than mixing `start_time` and `end_time` across queries.
- `cn_geofences` has no FK relationships — geofence monitoring is handled separately. Spatial mapping uses PostGIS (`location_points`, `centroid`) or the `h3cell` array.
- `cn_assets` has no FK relationships — assets are tracked independently of drivers and vehicles.
- Driver assignment on `cn_latest_vehicle_locations.driver_id` is updated separately from location data and may lag behind `location_time` by up to the sync interval.
- H3 cell arrays (`h3cell`) store 16 resolution levels (0–15) generated at insert time. Postgres arrays are 1-indexed, so `h3cell[1]` = resolution 0 (coarsest) and `h3cell[16]` = resolution 15 (finest).
- Trip detection logic (5-minute stop rule) is implemented in `cn_get_trips_by_vehicle` and `cn_get_routes_by_vehicle` — see Database Functions.
