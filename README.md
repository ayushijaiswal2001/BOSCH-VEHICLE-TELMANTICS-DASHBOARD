Project Title: BOSCH Vehicle Telematics Dashboard

File: BOSCH VEHICLE TELMANTICS DASHBOARD.pbix

Tool Used: Microsoft Power BI Desktop (Version: 2.147.1085.0, Published: 30 Sept 2025)

Objective: To visualize and analyze vehicle telematics data for fleet monitoring, driver behavior, and fuel efficiency.

Developer / Organization: Developed for Bosch Global Software Technologies (BGSW).

Key Features:

Real-time fleet tracking

Vehicle and driver KPIs

Fuel efficiency and usage trends

Event analytics (harsh braking, acceleration, overspeed)

Idle time and trip statistics

Dashboard Pages:

Fleet Overview

Vehicle Performance

Driver Analysis

Fuel & Efficiency

Trips & Routes (Map view)

Alerts and Exceptions

Data Sources:

Telematics Events (timestamped vehicle events)

Trips Data (distance, duration, average speed)

Vehicle and Driver Master tables

Fuel Records and GPS coordinates

KPIs Calculated:

Total Distance (km)

Average Speed (km/h)

Total Trips

Fuel Efficiency (L/100 km)

Total Harsh Events

Idle Hours

Example DAX Measures:

TotalDistanceKM = SUM(Trips[distance_km])
AvgSpeed = AVERAGE(Trips[avg_speed_kph])
FuelEfficiency = DIVIDE(SUM(Fuel[liters]), SUM(Trips[distance_km]) / 100)


Power Query (ETL): Used for data cleaning, transformations, and model relationships setup.

Model Design:

Star schema with fact tables (Trips, Events, Fuel)

Dimension tables (Date, Vehicle, Driver)

Relationships on IDs and Date fields

Filters & Slicers:

Date range, Vehicle ID, Driver Name, Event Type, and Region.

Map Visuals:

Displays trip routes and heatmaps of event locations using GPS data.

Performance Optimization:

Incremental data refresh

Aggregated tables

Query folding enabled in Power Query

Usage Instructions:

Open the .pbix file in Power BI Desktop.

Update data source paths/credentials.

Click Refresh to load the latest data.

Interact with filters and visuals.

Publishing:

Publish to Power BI Service for online access.

Configure dataset refresh schedule if connected to live sources.

System Requirements:

Windows OS

Power BI Desktop (latest or specified version)

Access to data source (SQL/CSV/API)

Limitations:

Requires pre-processed telemetry data.

Map visuals need valid latitude/longitude columns.

Not backward compatible with older Power BI builds.

License & Contributions:

Include LICENSE (e.g., MIT) in the repo.

Contributions welcome via pull requests or issues.
