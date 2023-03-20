# Data-driven Geo Schelling model

The project aims to implement a data-augmented version of the [MESA-geo](https://mesa-geo.readthedocs.io/en/latest/tutorials/intro_tutorial.html) model.

<p align="justify">The model does not start from a random initial situation but from a real one, simulating the segregation of the census tract of New York. 
The population data used are from 2010 and the two groups analyzed are Americans and Forgeiners.</p>

<p align="justify">The first part of the project is dedicated to collecting the data and creating a file to use for the simulation.  
The MESA-geo model is an agent-based model with two agent classes, RegionAgents, in our case the Census tracts, and the PersonAgents, that move between the Regions.</p> 

<p align="justify">The model was modified to take directly from the file the exact number of residents in each tract. During the preparation phase, where the model's agents are added, each PersonAgent is assigned a colour, red if is a Forgeiner or blue if is an American. Similar for RegionAgents, if inside them there are more American, the Region is blue, red otherwise. A visualization class was also added to have the possibility to visualize directly on the notebook the execution of the model.</p>

<p align="justify">Due to the heavily unbalanced class (72% Americans, 28% Forgeiners), the model with a similarity threshold around 50% is very slow, but this problem disappears with a more balanced class.</p>

### Project 
Please look at the [project](https://github.com/The-Saba/Geo-Schelling-model/blob/main/Data-driven%20Geo%20Schelling%20model.ipynb) for further details.

It was done for the Geospatial Analytics exam of the [Data Science and Business Informatics](https://didattica.di.unipi.it/en/master-programme-in-data-science-and-business-informatics/) master's degree course at the University of Pisa.

### Data sources
* Census info - [US Census Bureau](https://www.census.gov/cgi-bin/geo/shapefiles/index.php?year=2010&layergroup=Census+Tracts) (year 2010, State of New York, County of New York)
* Population info - [OpportunityInsights](https://opportunityinsights.org/wp-content/uploads/2018/10/tract_covariates.csv "Direct download")

### Base version of the model
* Mesa-geo model - [example](https://github.com/projectmesa/mesa-geo/tree/main/examples/geo_schelling_points)
