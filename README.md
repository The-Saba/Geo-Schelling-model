# Geospatial-project

The aim of the project is to implement a data-augmented version of the MESA-geo model. 

The model does not to start from a randomize initial situation but from a real one, simulating the segregation of the census tract of New York. 
The population data used are from 2010 and the two group analyzed are Americans and Forgeiners.

The first part of the project is dedicated on collecting the data and creating a file to use for the simulation.  
The MESA-geo model is an agent based model with two agent class, RegionAgents, in our case the Census tracts, and the PersonAgents, that move between the Regions. 

The model was modified to take directly from the file the exact number of resident in each tract. During the preparation phase, where the model's agent are added, at each PersonAgent is assigned a color (red for Forgeiners and blue for Americans)

#### Data sources
* Census info - [US Census Bureau](https://www.census.gov/cgi-bin/geo/shapefiles/index.php?year=2010&layergroup=Census+Tracts) (year 2010, the state of New York, the County of New York)
* Population info - [OpportunityInsights](https://opportunityinsights.org/wp-content/uploads/2018/10/tract_covariates.csv)
