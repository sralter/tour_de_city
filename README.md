# Tour de City

## Background

I named the project **Tour de City** as the ultimate goal of this project is to create a bicycle and running route recommendation model that also incorporates sightseeing. We'll see if that happens anytime soon! But I can be forgiven for dreaming big. In the meantime, we can work on more straightforward goals, described below.

## Overview of Project

I split the project into two phases, a _data engineering_ phase, and a _modeling_ phase.
- The data engineering phase includes identifying and downloading the data, combining the data into a `CSV`, and make a SQL database.
  - The last step of phase one is to create a Tableau dashboard and visualizations.
- The modeling phase will be done in Python and will take advantage of the GIS capabilities of various packages availabile to the platform to visualize and understand the flow of bike traffic on various timescales.

## Phase One: Data Engineering

I identified the data from [Citibike]([https://ride.citibikenyc.com/system-data](https://citibikenyc.com/system-data) and downloaded the data the Python tools `requests`, `re`, and `zipfile`.

After downloading each .zip file of trips, I combined the CSVs that have the same schema. I simplified some of the columns to create a basic database structure involving a few tables:
* Rides
  * ride_id
  * started_at
  * ended_at
  * start_station_id
  * end_station_id
  * ridertype
  * biketype
* Stations
  * start_station_name (Using the start_station_name rather than the end_station_name)
  * start_station_id
  * start_lat
  * start_lng
* Rider
  * type (member or casual)
  * id
* Bike
  * type (classic, electric, or unknown)
  * id

Fun fact: the `rides` table has over 55 million rows in it!

Using **DuckDB**'s functionality, I added the tables to a database. Given the size of the `rides` table, I used **DuckDB**'s CLI to directly add it to the database:

![Adding tables to database using DuckDB](figs/Screenshot 2025-01-05 at 00.09.20.png)

### Phase Two: Modeling the Flow of Bike Traffic

- [ ] Present data in Python and use OpenStreetMap or other tool

