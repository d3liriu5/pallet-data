
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
CREATE TABLE cd_drivers (
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
  constraint cd_drivers_pkey primary key (id),
  constraint cd_drivers_id_key unique (id)
);


## cd_vehicles

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
create table cd_vehicles (
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
| vehicle_number                      | text         | NO       |                   | Company-defined vehicle identifier                |
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
| created_at                          | timestamptz  | NO       |                   |                                                   |

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
  created_at timestamp with time zone not null default now(),
  constraint cd_geofences_pkey primary key (id)
);
create index IF not exists geofences_centroid_index on public.fx_geofences using gist (centroid) TABLESPACE pg_default;


## cd_spend_profiles

> Stores spend profiles of the users in the company.

### Table
| Column                                          | Type         | Nullable | Default           | Description                                           |
|-------------------------------------------------|--------------|----------|-------------------|-------------------------------------------------------|
| id                                              | uuid         | NO       |                   | Unique identifier of the spend_profile                |
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
| spend_limits_enable_days                        | text[]       | YES      | NULL              | Days of the week when the card can be used            |
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
| id                                              | uuid         | NO       |                   | Unique identifier of the card                            |
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
