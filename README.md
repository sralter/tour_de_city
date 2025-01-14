# Tour de City
Using the Citibike dataset, I will work on my SQL and Python skills to make sense of the data.

I named the project **Tour de City** as the ultimate goal of this project is to create a bicycle and running route recommendation model that also incorporates sightseeing. We'll see if that happens anytime soon! But I can be forgiven for dreaming big. In the meantime, we can work on more straightforward goals, described below.

I split the project into two phases, a _data engineering_ phase, and a _modeling_ phase.
- The data engineering phase includes identifying and downloading the data, combining the data into a `CSV`, and make a SQL database.
  - The last step of phase one is to create a Tableau dashboard and visualizations.
- The modeling phase will be done in Python and will take advantage of the GIS capabilities of various packages availabile to the platform to visualize and understand the flow of bike traffic on various timescales.

## Steps of the project are outlined below:
### Phase One: Data Engineering

I identified the data from [Citibike](https://ride.citibikenyc.com/system-data) 
![ezgif com-optimize](https://github.com/sralter/citibike_project/assets/25013680/b067f46f-cfc7-4eaa-afc9-3e3a5594ed8f)

- [X] Download the data using web inspector and Python (`requests`, `re`, and `zipfile`):  
![ezgif com-optimize-3](https://github.com/sralter/citibike_project/assets/25013680/31a6e954-7d0d-4867-a5f4-7ecd2fe88299)

- [X] Examine pattern of headers of CSV:  
![ezgif com-optimize-4](https://github.com/sralter/citibike_project/assets/25013680/ea312ded-27b6-43d7-b058-f265676634cc)

- [X] Combine CSVs that have the same headers
    - [X] Compare headers of CSVs:  
![ezgif com-optimize-5](https://github.com/sralter/citibike_project/assets/25013680/48976048-625f-4ba5-a25c-3f0ac73ae69e)

    - [X] Put into a dictionary the filenames of CSVs with the same headers as values to the common header as the key:  
![ezgif com-optimize-6](https://github.com/sralter/citibike_project/assets/25013680/42cb5f2b-95e0-408c-a149-4f60f82803fa)

    - [X] Add the CSV to a common CSV, but only adding the header from the first CSV in the group:  

- [X] Some simple EDA on the created file using the _polars_ package:  
![ezgif com-optimize-7](https://github.com/sralter/citibike_project/assets/25013680/640e439b-ef81-4f62-b5c2-bf987dbe32d2)

- [X] Normalize tables to prepare to...  
![ezgif com-optimize-8](https://github.com/sralter/citibike_project/assets/25013680/841121b7-05ed-489a-b642-6e740dd58a0d)


- [ ] ...Make SQL database  



- [ ] Run SQL queries either in Jupyter Lab or in MySQLWorkbench  

- [X] Make **Tableau** dashboard

- EDA on dataset:
![Pairplot showing relationship between features in dataset](https://github.com/sralter/tour_de_city/assets/25013680/2371da7e-f71d-445a-b152-fd900c9acf90)

### Phase Two: Modeling the Flow of Bike Traffic

- [ ] Present data in Python and use OpenStreetMap  

