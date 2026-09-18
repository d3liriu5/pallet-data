
## cd_drivers

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
CREATE TABLE cd_drivers (
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
  constraint cd_drivers_pkey primary key (id),
  constraint cd_drivers_id_key unique (id)
);


## cd_vehicles

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
create table cd_vehicles (
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
  constraint cd_vehicles_pkey primary key (id),
  constraint cd_vehicles_id_key unique (id),
  constraint cd_vehicles_number_key unique (number),
  constraint cd_vehicles_current_driver_id_fkey foreign KEY (current_driver_id) references cd_drivers (id)
);


## cd_latest_vehicle_locations

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
create table cd_latest_vehicle_locations (
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
  constraint cd_latest_vehicle_locations_pkey primary key (vehicle_id),
  constraint cd_latest_vehicle_locations_vehicle_id_key unique (vehicle_id),
  constraint cd_latest_vehicle_locations_vehicle_id_fkey foreign KEY (vehicle_id) references cd_vehicles (id)
);
create index IF not exists cd_latest_vehicle_locations_location_point_idx on cd_latest_vehicle_locations using gist (location_point);


## cd_assets

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
create table cd_assets (
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
  constraint cd_assets_pkey primary key (id),
  constraint cd_assets_id_key unique (id)
);


## cd_geofences

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
create table cd_geofences (
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
  constraint cd_geofences_pkey primary key (id)
);


## cd_spend_profiles

> Stores spend profiles of the users in the company.

### Table
| Column                                          | Type         | Nullable | Default           | Description                                           |
|-------------------------------------------------|--------------|----------|-------------------|-------------------------------------------------------|
| id                                              | uuid         | NO       |                   | Unique identifier of the fault code                   |
| name                                            | text         | YES      | NULL              | The fault code as reported by the vehicle             |
| is_default                                      | boolean      | YES      | NULL              | Is this profile the default profile?                  |
| created_at                                      | timestamptz  | YES      | NULL              | When the profile was created                          |
| updated_at                                      | timestamptz  | YES      | NULL              | When the profile was last updated                     |
| spend_categories                                | text[]       | YES      | NULL              | The allowed spending categories for this profile      |
| spend_limits_daily_limit_in_cents               | int8         | YES      | NULL              |                                                       |
| spend_limits_weekly_limit_in_cents              | int8         | YES      | NULL              |                                                       |
| spend_limits_monthly_limit_in_cents             | int8         | YES      | NULL              |                                                       |
| spend_limits_transaction_limit_in_cents         | int8         | YES      | NULL              |                                                       |
| spend_limits_billing_cycle_spend_limit_in_cents | int8         | YES      | NULL              |                                                       |
| spend_limits_daily_withdrawal_limit_in_cents    | int8         | YES      | NULL              |                                                       |
| spend_limits_weekly_withdrawal_limit_in_cents   | int8         | YES      | NULL              |                                                       |
| spend_limits_atm_withdrawal_enabled             | boolean      | YES      | false             | Are ATM withdrawals allowed?                          |
| spend_limits_enable_days                        | text         | YES      | NULL              | Days of the week when the card can be used            |
| spend_limits_enable_start_time                  | time         | YES      | NULL              |                                                       |
| spend_limits_enable_end_time                    | time         | YES      | NULL              |                                                       |
| spend_limits_created_by                         | int8         | YES      | NULL              |                                                       |

### DDL
create table cd_spend_profiles (
  id uuid not null,
  name text null,
  is_default boolean null,
  created_at timestamp with time zone null,
  updated_at timestamp with time zone null,
  spend_categories text[] null,
  spend_limits_daily_limit_in_cents bigint null,
  spend_limits_weekly_limit_in_cents bigint null,
  spend_limits_monthly_limit_in_cents bigint null,
  spend_limits_transaction_limit_in_cents bigint null,
  spend_limits_billing_cycle_spend_limit_in_cents bigint null,
  spend_limits_daily_withdrawal_limit_in_cents bigint null,
  spend_limits_weekly_withdrawal_limit_in_cents bigint null,
  spend_limits_atm_withdrawal_enabled boolean null default false,
  spend_limits_enable_days text[] null,
  spend_limits_enable_start_time time without time zone null,
  spend_limits_enable_end_time time without time zone null,
  spend_limits_created_by bigint null,
  constraint cd_spend_profiles_pkey primary key (id)
);


## cd_cards

> Stores available Motive Cards in the company.

### Table
| Column                                          | Type         | Nullable | Default           | Description                                              |
|-------------------------------------------------|--------------|----------|-------------------|----------------------------------------------------------|
| id                                              | uuid         | NO       |                   | Unique identifier of the fault code                      |
| last_four_digits                                | int8         | YES      | NULL              | Last four digits of the card number                      |
| display_card_id                                 | text         | YES      | NULL              | A display-friendly identifier for the card               |
| name_line_1                                     | text         | YES      | NULL              | First line of the cardholder's name (e.g. driver name)   |
| name_line_2                                     | text         | YES      | NULL              | Second line of the cardholder's name (e.g. company name) |
| status                                          | text         | YES      | NULL              | Current status of the card (e.g. active)                 |
| created_at                                      | timestamptz  | YES      | NULL              | Timestamp when card was created                          |
| updated_at                                      | timestamptz  | YES      | NULL              | Timestamp when card was last updated                     |
| assigned_to_driver                              | int8         | YES      | NULL              | The driver to whom the card is assigned                  |
| assigned_to_vehicle                             | int8         | YES      | NULL              | The vehicle to whom the card is assigned                 |
| assigned_to_asset                               | int8         | YES      | NULL              | The asset to whom the card is assigned                   |
| assigned_to_fleet_user                          | int8         | YES      | NULL              | The fleet user to whom the card is assigned              |
| security_settings_status                        | text         | YES      | NULL              | Security status of the card (e.g. active)                |
| security_settings_is_locked                     | boolean      | YES      | NULL              | Is the card currently locked?                            |
| security_settings_unlocked_till                 | timestamptz  | YES      | NULL              | Timestamp until which the card remains unlocked          |
| security_settings_proximity_based_decline       | boolean      | YES      | NULL              | Are proximity-based declines enabled?                    |
| spend_profile_id                                | uuid         | YES      | NULL              | Unique identifier of the spend control profile           |

### DDL
create table cd_cards (
  id uuid not null,
  last_four_digits bigint null,
  display_card_id text null,
  name_line_1 text null,
  name_line_2 text null,
  status text null,
  created_at timestamp with time zone null,
  updated_at timestamp with time zone null,
  assigned_to_driver bigint null,
  assigned_to_vehicle bigint null,
  assigned_to_asset bigint null,
  assigned_to_fleet_user bigint null,
  security_settings_status text null,
  security_settings_is_locked boolean null,
  security_settings_unlocked_till timestamp with time zone null,
  security_settings_proximity_based_decline boolean null,
  spend_profile_id uuid null,
  constraint cd_cards_pkey primary key (id),
  constraint cd_cards_assigned_to_asset_fkey foreign KEY (assigned_to_asset) references cd_assets (id),
  constraint cd_cards_assigned_to_driver_fkey foreign KEY (assigned_to_driver) references cd_drivers (id),
  constraint cd_cards_assigned_to_vehicle_fkey foreign KEY (assigned_to_vehicle) references cd_vehicles (id),
  constraint cd_cards_spend_profile_id_fkey foreign KEY (spend_profile_id) references cd_spend_profiles (id)
);


## cd_card_transactions

> Stores all Motive Card transactions that happened at the company.

### Table
| Column                                          | Type         | Nullable | Default           | Description                                                       |
|-------------------------------------------------|--------------|----------|-------------------|-------------------------------------------------------------------|
| id                                              | uuid         | NO       |                   | Unique identifier of the transaction                              |
| card_id                                         | uuid         | NO       |                   | Unique identifier of the Motive Card used in the transaction      |                                                      |
| transaction_status                              | text         | YES      | NULL              | Status of the transaction (e.g. "posted")                         |
| transaction_type                                | text         | YES      | NULL              | Type of transaction, one of: purchase, fee, credit, adjustment    |
| transaction_time                                | timestamptz  | YES      | NULL              | Timestamp when the transaction occurred                           |
| posted_at                                       | timestamptz  | YES      | NULL              | Timestamp when the transaction was posted                         |
| updated_at                                      | timestamptz  | YES      | NULL              | Timestamp when the transaction was last updated                   |
| transaction_reversed_time                       | timestamptz  | YES      | NULL              | Timestamp when the transaction was reversed, if applicable        |
| driver_id                                       | int8         | YES      | NULL              | Unique identifier of the driver associated with the transaction   |
| vehicle_id                                      | int8         | YES      | NULL              | Unique identifier of the vehicle associated with the transaction  |
| invoice_number                                  | int8         | YES      | NULL              | Invoice number for the transaction                                |
| authorized_amount                               | numeric      | YES      | NULL              | Authorized amount in dollars                                      |
| total_rebate                                    | numeric      | YES      | NULL              | Total rebate amout applied to the transaction in dollars          |
| total_amount_before_rebate                      | numeric      | YES      | NULL              | Total amount before applying the rebate, in dollars               |
| total_amount                                    | numeric      | YES      | NULL              | Total amount after applying the rebate, in dollars                |
| decline_reason_code                             | text         | YES      | NULL              | Code indicating the reason for transaction decline, if applicable |
| decline_reason                                  | text         | YES      | NULL              | Description of the reason for transaction decline, if applicable  |
| pre_transaction_metadata_odometer_reading       | int8         | YES      | NULL              | Odometer reading before the transaction                           |
| pre_transaction_metadata_odometer_unit          | text         | YES      | NULL              | Unit of the odometer reading (e.g. "km")                          |
| post_transaction_metadata_receipt_available     | boolean      | YES      | NULL              | Is a receipt available for the transaction?                       |
| post_transaction_metadata_comment               | text         | YES      | NULL              | Additional comments related to the transaction                    |
| merchant_name                                   | text         | YES      | NULL              | Name of the merchant                                              |
| merchant_city                                   | text         | YES      | NULL              | City where the merchant is located                                |
| merchant_state                                  | text         | YES      | NULL              | State where the merchant is located                               |
| merchant_street                                 | text         | YES      | NULL              | Street address of the merchant                                    |
| merchant_country                                | text         | YES      | NULL              | Country where the merchant is located                             |
| merchant_zipcode                                | text         | YES      | NULL              | ZIP code of the merchant's location                               |
| currency                                        | text         | YES      | NULL              | Currency used in the transaction (e.g. "USD")                     |
| asset_id                                        | int8         | YES      | NULL              | Unique identifier of the asset associated with the transaction    |

### DDL
create cd_card_transactions (
  id uuid not null,
  card_id uuid not null,
  transaction_status text null,
  transaction_type text null,
  transaction_time timestamp with time zone null,
  posted_at timestamp with time zone null,
  updated_at timestamp with time zone null,
  transaction_reversed_time timestamp with time zone null,
  driver_id bigint null,
  vehicle_id bigint null,
  invoice_number bigint null,
  authorized_amount numeric null,
  total_rebate numeric null,
  total_amount_before_rebate numeric null,
  total_amount numeric null,
  decline_reason_code text null,
  decline_reason text null,
  pre_transaction_metadata_odometer_reading bigint null,
  pre_transaction_metadata_odometer_unit text null,
  post_transaction_metadata_receipt_available boolean null,
  post_transaction_metadata_comment text null,
  merchant_name text null,
  merchant_city text null,
  merchant_state text null,
  merchant_street text null,
  merchant_country text null,
  merchant_zipcode text null,
  currency text null,
  asset_id bigint null,
  constraint cd_card_transactions_pkey primary key (id),
  constraint cd_card_transactions_card_id_fkey foreign KEY (card_id) references cd_cards (id)
);


## cd_card_transaction_items

> Stores items involved in Motive Card transactions

### Table
| Column                                          | Type         | Nullable | Default           | Description                                              |
|-------------------------------------------------|--------------|----------|-------------------|----------------------------------------------------------|
| id                                              | int8         | NO       |                   | Unique identifier of the transaction item                |
| transaction_id                                  | uuid         | NO       |                   | Unique identifier of the transaction                     |
| quantity                                        | numeric      | YES      | NULL              | Quantity of the item                                     |
| unit                                            | text         | YES      | NULL              | Unit of measurement for the item                         |
| unit_price                                      | numeric      | YES      | NULL              | Unit price of the item                                   |
| gross_amount                                    | numeric      | YES      | NULL              | Gross amount of the item in dollars                      |
| rebate_amount                                   | numeric      | YES      | NULL              | Rebate amount applied to the item in dollars             |
| product_type                                    | text         | YES      | NULL              | Type of the product (e.g. "Cash", "ATM fee")             |
| line_number                                     | int2         | NO       |                   | The line number of the item in the transaction           |

### DDL
create table cd_card_transaction_items (
  id bigint generated by default as identity not null,
  transaction_id uuid not null default gen_random_uuid (),
  quantity numeric null,
  unit text null,
  unit_price numeric null,
  gross_amount numeric null,
  rebate_amount numeric null,
  product_type text null,
  line_number smallint not null,
  constraint cd_card_transaction_items_pkey primary key (id),
  constraint cd_card_transaction_items_txn_line_key unique (transaction_id, line_number),
  constraint cd_card_transaction_items_transaction_id_fkey foreign KEY (transaction_id) references cd_card_transactions (id) on delete CASCADE
);


## Entity Relationships

### Plain-English Summary
A **Driver** can be assigned to one Vehicle at a time. Each **Vehicle** has one current Latest Vehicle Location record representing its most recent telemetry snapshot. **Assets** are non-vehicle fleet items such as trailers and equipment, tracked separately from vehicles. **Geofences** define named geographic boundaries used for monitoring and alerting.

**Cards** are Motive fleet cards that can be assigned to a Driver, Vehicle, or Asset — but only one at a time. Each Card is governed by a **Spend Profile** that controls spending categories, daily/weekly/monthly limits, ATM access, and permitted hours of use. **Card Transactions** record every purchase, fee, credit, and adjustment made against a card, linked back to the card, and optionally to the driver, vehicle, or asset involved. Each transaction can have one or more **Card Transaction Items** representing the individual line items on a receipt — for example a fuel purchase might have separate line items for gallons, unit price, and any applicable fees.

### Relationship Table
| From                 | Relationship | To                          | Via (FK)                                                           |
|----------------------|--------------|-----------------------------|--------------------------------------------------------------------|
| cd_drivers           | has one      | cd_vehicles                 | cd_vehicles.current_driver_id → cd_drivers.id                      |
| cd_vehicles          | has one      | cd_latest_vehicle_locations | cd_latest_vehicle_locations.vehicle_id → cd_vehicles.id            |
| cd_spend_profiles    | has many     | cd_cards                    | cd_cards.spend_profile_id → cd_spend_profiles.id                   |
| cd_drivers           | has many     | cd_cards                    | cd_cards.assigned_to_driver → cd_drivers.id                        |
| cd_vehicles          | has many     | cd_cards                    | cd_cards.assigned_to_vehicle → cd_vehicles.id                      |
| cd_assets            | has many     | cd_cards                    | cd_cards.assigned_to_asset → cd_assets.id                          |
| cd_cards             | has many     | cd_card_transactions        | cd_card_transactions.card_id → cd_cards.id                         |
| cd_card_transactions | has many     | cd_card_transaction_items   | cd_card_transaction_items.transaction_id → cd_card_transactions.id |

### Notes
- `cd_latest_vehicle_locations` is a snapshot table — it stores only the most recent location per vehicle, not a history.
- `cd_geofences` has no FK relationships — geofence monitoring is done elsewhere and mapping is done using PostGIS (location_points, centroid) or the h3cell array.
- `cd_assets` has no FK relationships to drivers or vehicles — assets are tracked independently and linked only through card assignment.
- Monetary amounts (`authorized_amount`, `total_amount`, `unit_price`, etc.) are stored as numeric in dollars. Spend limits on `cd_spend_profiles` are stored as `int8` in cents — be careful not to mix units when comparing transaction amounts against profile limits.

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
CREATE TABLE cd_drivers (
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
  constraint cd_drivers_pkey primary key (id),
  constraint cd_drivers_id_key unique (id)
);


## cd_vehicles

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
create table cd_vehicles (
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
  constraint cd_vehicles_pkey primary key (id),
  constraint cd_vehicles_id_key unique (id),
  constraint cd_vehicles_number_key unique (number),
  constraint cd_vehicles_current_driver_id_fkey foreign KEY (current_driver_id) references cd_drivers (id)
);


## cd_latest_vehicle_locations

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
create table cd_latest_vehicle_locations (
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
  constraint cd_latest_vehicle_locations_pkey primary key (vehicle_id),
  constraint cd_latest_vehicle_locations_vehicle_id_key unique (vehicle_id),
  constraint cd_latest_vehicle_locations_driver_id_fkey foreign KEY (driver_id) references cd_drivers (id),
  constraint cd_latest_vehicle_locations_vehicle_id_fkey foreign KEY (vehicle_id) references cd_vehicles (id)
);


## cd_assets

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
create table cd_assets (
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
  constraint cd_assets_pkey primary key (id),
  constraint cd_assets_id_key unique (id)
);


## cd_geofences

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
create table cd_geofences (
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
  constraint cd_geofences_pkey primary key (id)
)

## cd_events

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
create table cd_events (
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
  constraint cd_events_pkey primary key (id),
  constraint cd_events_id_key unique (id),
  constraint cd_events_driver_id_fkey foreign KEY (driver_id) references cd_drivers (id),
  constraint cd_events_vehicle_id_fkey foreign KEY (vehicle_id) references cd_vehicles (id)
)


## cd_spend_profiles

> Stores the spend profiles of a company.

### Table
| Column                                          | Type         | Nullable | Default    | Description                                       |
|-------------------------------------------------|--------------|----------|------------|---------------------------------------------------|
| id                                              | uuid         | NO       |            | Unique identifier of the spend control profile    |
| name                                            | text         | YES      | NULL       | Name of the spend control profile                 |
| is_default                                      | boolean      | YES      | NULL       | Is this profile the default profile?              |
| created_at                                      | timestamptz  | YES      | NULL       | When the spend control profile was created        |
| updated_at                                      | timestamptz  | YES      | NULL       | When the spend control profile was updated        |
| spend_categories                                | text[]       | YES      | NULL       | Allowed spend categories for this profile         |
| spend_limits_daily_limit_in_cents               | int8         | YES      | NULL       | Daily spend limit in cents                        |
| spend_limits_weekly_limit_in_cents              | int8         | YES      | NULL       | Weekly spend limit in cents                       |
| spend_limits_monthly_limit_in_cents             | int8         | YES      | NULL       | Monthly spend limit in cents                      |
| spend_limits_transaction_limit_in_cents         | int8         | YES      | NULL       | Per-transaction spend limit in cents              |
| spend_limits_billing_cycle_spend_limit_in_cents | int8         | YES      | NULL       | Spend limit for current billing cycle in cents    |
| spend_limits_daily_withdrawal_limit_in_cents    | int8         | YES      | NULL       | Daily withdrawal limit in cents                   |
| spend_limits_weekly_withdrawal_limit_in_cents   | int8         | YES      | NULL       | Weekly withdrawal limit in cents                  |
| spend_limits_atm_withdrawal_enabled             | boolean      | YES      | NULL       | Are ATM withdrawals allowed?                      |
| spend_limits_enable_days                        | text[]       | YES      | NULL       | Days of the week when the card can be used        |
| spend_limits_enable_start_time                  | time         | YES      | NULL       | Start time from which card usage is enabled       |
| spend_limits_enable_end_time                    | time         | YES      | NULL       | End time from which card usage is enabled         |
| spend_limits_created_by                         | int8         | YES      | NULL       | Unique identifier of the user who created profile |

### DDL
create table cd_spend_profiles (
  id uuid not null,
  name text null,
  is_default boolean null,
  created_at timestamp with time zone null,
  updated_at timestamp with time zone null,
  spend_categories text[] null,
  spend_limits_daily_limit_in_cents bigint null,
  spend_limits_weekly_limit_in_cents bigint null,
  spend_limits_monthly_limit_in_cents bigint null,
  spend_limits_transaction_limit_in_cents bigint null,
  spend_limits_billing_cycle_spend_limit_in_cents bigint null,
  spend_limits_daily_withdrawal_limit_in_cents bigint null,
  spend_limits_weekly_withdrawal_limit_in_cents bigint null,
  spend_limits_atm_withdrawal_enabled boolean null default false,
  spend_limits_enable_days text[] null,
  spend_limits_enable_start_time time without time zone null,
  spend_limits_enable_end_time time without time zone null,
  spend_limits_created_by bigint null,
  constraint cd_spend_profiles_pkey primary key (id)
);


## cd_cards

> Stores the available Motive Cards of a company.

### Table
| Column                                    | Type         | Nullable | Default    | Description                                          |
|-------------------------------------------|--------------|----------|------------|------------------------------------------------------|
| id                                        | uuid         | NO       |            | Unique identifier of the card                        |
| last_four_digits                          | int8         | YES      | NULL       | Last four digits of the card number                  |
| display_card_id                           | text         | YES      | NULL       | Display-friendly identifier for the card             |
| name_line_1                               | text         | YES      | NULL       | First line of the cardholder’s name                  |
| name_line_2                               | text         | YES      | NULL       | Second line of the cardholder's name                 |
| status                                    | text         | YES      | NULL       | Current status of the card                           |
| created_at                                | timestamptz  | YES      | NULL       | Datetime when the card was created                   |
| updated_at                                | timestamptz  | YES      | NULL       | Datetime when the card info was last updated         |
| assigned_to_driver                        | int8         | YES      | NULL       | Unique identifier of the driver assigned to card     |
| assigned_to_vehicle                       | int8         | YES      | NULL       | Unique identifier of the vehicle assigned to card    |
| assigned_to_asset                         | int8         | YES      | NULL       | Unique identifier of the asset assigned to card      |
| assigned_to_fleet_user                    | int8         | YES      | NULL       | Unique identifier of the fleet user assigned to card |
| security_settings_status                  | text         | YES      | NULL       |                                                      |
| security_settings_is_locked               | boolean      | YES      | NULL       | Is the card currently locked?                        |
| security_settings_unlocked_till           | timestamptz  | YES      | NULL       | Datetime until which the card remains unlocked       |
| security_settings_proximity_based_decline | boolean      | YES      | NULL       | Are vehicle proximity-based declines enabled?        |
| spend_profile_id                          | uuid         | YES      | NULL       | Unique identifier of the spend profile               |

### DDL
create table cd_cards (
  id uuid not null,
  last_four_digits bigint null,
  display_card_id text null,
  name_line_1 text null,
  name_line_2 text null,
  status text null,
  created_at timestamp with time zone null,
  updated_at timestamp with time zone null,
  assigned_to_driver bigint null,
  assigned_to_vehicle bigint null,
  assigned_to_asset bigint null,
  assigned_to_fleet_user bigint null,
  security_settings_status text null,
  security_settings_is_locked boolean null,
  security_settings_unlocked_till timestamp with time zone null,
  security_settings_proximity_based_decline boolean null,
  spend_profile_id uuid null,
  constraint cd_cards_pkey primary key (id),
  constraint cd_cards_assigned_to_asset_fkey foreign KEY (assigned_to_asset) references cd_assets (id),
  constraint cd_cards_assigned_to_driver_fkey foreign KEY (assigned_to_driver) references cd_drivers (id),
  constraint cd_cards_assigned_to_vehicle_fkey foreign KEY (assigned_to_vehicle) references cd_vehicles (id),
  constraint cd_cards_spend_profile_id_fkey foreign KEY (spend_profile_id) references cd_spend_profiles (id)
);


## cd_card_transactions

> Stores Motive Card transactions of a company.

### Table
| Column                                      | Type         | Nullable | Default    | Description                                                      |
|---------------------------------------------|--------------|----------|------------|------------------------------------------------------------------|
| id                                          | uuid         | NO       |            | Unique identifier of the transaction                             |
| card_id                                     | uuid         | NO       |            | Unique identifier of the card                                    |
| transaction_status                          | text         | YES      | NULL       | Status of the transaction                                        |
| transaction_type                            | text         | YES      | NULL       | Values: purchase, fee, credit, adjustment                        |
| transaction_time                            | timestamptz  | YES      | NULL       | Datetime of the transaction                                      |
| posted_at                                   | timestamptz  | YES      | NULL       | Datetime when the transaction was posted                         |
| updated_at                                  | timestamptz  | YES      | NULL       | Datetime when the transaction was last updated                   |
| transaction_reversed_time                   | timestamptz  | YES      | NULL       | Datetime when the transaction was reversed                       |
| driver_id                                   | int8         | YES      | NULL       | Unique identifier of the driver associated with the transaction  |
| vehicle_id                                  | int8         | YES      | NULL       | Unique identifier of the vehicle associated with the transaction |
| asset_id                                    | int8         | YES      | NULL       | Unique identifier of the asset associated with the transaction   |
| invoice_number                              | int8         | YES      | NULL       | Invoice number for the transaction                               |
| authorized_amount                           | numeric      | YES      | NULL       | Authorized amount, in dollars                                    |
| total_rebate                                | numeric      | YES      | NULL       | Total rebate amount applied to the transaction, in dollars       |
| total_amount_before_rebate                  | numeric      | YES      | NULL       | Total amount before applying the rebate, in dollars              |
| total_amount                                | numeric      | YES      | NULL       | Total amount after applying the rebate, in dollars               |
| decline_reason_code                         | text         | YES      | NULL       | Code indicating the reason for transaction decline               |
| decline_reason                              | text         | YES      | NULL       | Description of the reason for transaction decline                |
| pre_transaction_metadata_odometer_reading   | int8         | YES      | NULL       | Odometer reading before the transaction                          |
| pre_transaction_metadata_odometer_unit      | text         | YES      | NULL       |                                                                  |
| post_transaction_metadata_receipt_available | boolean      | YES      | NULL       | Is a receipt available for the transaction?                      |
| post_transaction_metadata_comment           | text         | YES      | NULL       | Additional comments related to the transaction                   |
| merchant_name                               | text         | YES      | NULL       | Name of the merchant                                             |
| merchant_city                               | text         | YES      | NULL       | City where the merchant is located                               |
| merchant_state                              | text         | YES      | NULL       | State where the merchant is located                              |
| merchant_street                             | text         | YES      | NULL       | Street address of the merchant                                   |
| merchant_country                            | text         | YES      | NULL       | Country where the merchant is located                            |
| merchant_zipcode                            | text         | YES      | NULL       | ZIP/Postal code of the merchant's location                       |
| currency                                    | text         | YES      | NULL       | Currency used in the transaction                                 |

### DDL
create table cd_card_transactions (
  id uuid not null,
  card_id uuid not null,
  transaction_status text null,
  transaction_type text null,
  transaction_time timestamp with time zone null,
  posted_at timestamp with time zone null,
  updated_at timestamp with time zone null,
  transaction_reversed_time timestamp with time zone null,
  driver_id bigint null,
  vehicle_id bigint null,
  invoice_number bigint null,
  authorized_amount numeric null,
  total_rebate numeric null,
  total_amount_before_rebate numeric null,
  total_amount numeric null,
  decline_reason_code text null,
  decline_reason text null,
  pre_transaction_metadata_odometer_reading bigint null,
  pre_transaction_metadata_odometer_unit text null,
  post_transaction_metadata_receipt_available boolean null,
  post_transaction_metadata_comment text null,
  merchant_name text null,
  merchant_city text null,
  merchant_state text null,
  merchant_street text null,
  merchant_country text null,
  merchant_zipcode text null,
  currency text null,
  asset_id bigint null,
  constraint cd_card_transactions_pkey primary key (id),
  constraint cd_card_transactions_asset_id_fkey foreign KEY (asset_id) references cd_assets (id),
  constraint cd_card_transactions_card_id_fkey foreign KEY (card_id) references cd_cards (id),
  constraint cd_card_transactions_driver_id_fkey foreign KEY (driver_id) references cd_drivers (id),
  constraint cd_card_transactions_vehicle_id_fkey foreign KEY (vehicle_id) references cd_vehicles (id)
);


## cd_card_transaction_items

> Stores items involved in each Motive Card transaction.

### Table
| Column                              | Type         | Nullable | Default           | Description                                           |
|-------------------------------------|--------------|----------|-------------------|-------------------------------------------------------|
| id                                  | int8         | NO       |                   | Unique identifier of the item                         |
| transaction_id                      | uuid         | NO       |                   | Unique identifier of the associated transaction       |
| quantity                            | numeric      | YES      | NULL              | Quantity of the item                                  |
| unit                                | text         | YES      | NULL              | Unit of measurement for the item                      |
| unit_price                          | numeric      | YES      | NULL              | Unit price of the item                                |
| gross_amount                        | numeric      | YES      | NULL              | Gross amount of the item, in dollars                  |
| rebate_amount                       | numeric      | YES      | NULL              | Rebate amount applied to the product type, in dollars |
| product_type                        | text         | YES      | NULL              | Type of product                                       |

### DDL
create table cd_card_transaction_items (
  id bigint generated by default as identity not null,
  transaction_id uuid not null default gen_random_uuid (),
  quantity numeric null,
  unit text null,
  unit_price numeric null,
  gross_amount numeric null,
  rebate_amount numeric null,
  product_type text null,
  constraint cd_card_transaction_items_pkey primary key (id),
  constraint cd_card_transaction_items_transaction_id_fkey foreign KEY (transaction_id) references cd_card_transactions (id)
);


## Entity Relationships

### Plain-English Summary
A **Driver** can be assigned to one **Vehicle** at a time. Each **Vehicle** has one current **Latest Vehicle Location** record, which may also reveal the currently assigned **Driver**. **Assets** are non-vehicle fleet items (trailers, equipment, etc.).

**Events** capture driver performance incidents (speeding, hard braking, etc.) and are linked to both a **Driver** and a **Vehicle**. **Geofences** define geographic boundaries and can be mapped spatially via location_points / h3cell.

**Cards** (Motive Cards) can be assigned to a **Driver**, **Vehicle**, or **Asset** - but only one at a time. Each **Card** is governed by a **Spend Profile** that controls spending limits, allowed categories, and usage schedules.

**Transactions** are created when a **Card** is used. Each **Transaction** belongs to one **Card** and can reference a **Driver**, **Vehicle**, or **Asset**. Each **Transaction** may have one or more **Transaction Items** that break down what was purchased (fuel, fees, etc.) and rebated.

### Relationship Table
| From                 | Relationship | To                          | Via (FK)                                                           |
|----------------------|--------------|-----------------------------|--------------------------------------------------------------------|
| cd_drivers           | has one      | cd_vehicles                 | cd_vehicles.current_driver_id → cd_drivers.id                      |
| cd_vehicles          | has one      | cd_latest_vehicle_locations | cd_latest_vehicle_locations.vehicle_id → cd_vehicles.id            |
| cd_drivers           | has one      | cd_latest_vehicle_locations | cd_latest_vehicle_locations.driver_id → cd_drivers.id              |
| cd_drivers           | has many     | cd_events                   | cd_events.driver_id → cd_drivers.id                                |
| cd_vehicles          | has many     | cd_events                   | cd_events.vehicle_id → cd_vehicles.id                              |
| cd_spend_profiles    | has many     | cd_cards                    | cd_cards.spend_profile_id → cd_spend_profiles.id                   |
| cd_cards             | has many     | cd_card_transactions        | cd_card_transactions.card_id → cd_cards.id                         |
| cd_drivers           | has many     | cd_card_transactions        | cd_card_transactions.driver_id → cd_drivers.id                     |
| cd_vehicles          | has many     | cd_card_transactions        | cd_card_transactions.vehicle_id → cd_vehicles.id                   |
| cd_assets            | has many     | cd_card_transactions        | cd_card_transactions.asset_id → cd_assets.id                       |
| cd_card_transactions | has many     | cd_card_transaction_items   | cd_card_transaction_items.transaction_id → cd_card_transactions.id |

### Notes
- A `cd_cards` row can be assigned to a driver, vehicle, or asset — but the schema doesn't enforce mutual exclusivity. When querying card assignments, check which of the three `assigned_to_*` columns is non-null.
- `cd_latest_vehicle_locations` is a snapshot table — it stores only the most recent location per vehicle, not a history.
- All monetary values in `cd_card_transactions` and `cd_card_transaction_items` are in dollars (numeric), while `cd_spend_profiles` limits are in cents (int8). Be careful not to mix units when comparing or aggregating across tables.
