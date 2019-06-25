
# Title - Find Data by Proximity to a Specified Location #

## Status ##
:_Proposed_

## Description ##
For an upcoming cruise, we will be collecting data at three stations - 
* Station 1 is supposed to be in a high O2 water column, 
* Station 2 is intended to be in intermediate O2 waters, and 
* Station 3 is intended to be in very low - anoxic / hypoxic waters. 

I want to find CTD data with Oxygen in the upper 1000 m close to each of the stations to see if my supposition about the oxygen levels was right. 

## What is Needed ##

1. Present the geolocation of station 1, 2, and 3.
2. Knowing the exact locations of collection for all geospatially-referenced data in the catalog.
3. Calculate the proximity of datasets to the geolocation of the stations.
3. The instrumentation used in collecting the data.
4. Subset relevant datasets on a depth parameter.

## How is BCO-DMO Addressing the Needs ##

1. Provide a geospatial search interface that lets a searcher articulate a Point on interest and provide a reasonable radius of proximity for data collected within that sphere. This capability is currently provided by Leaflet maps at https://www.bco-dmo.org/search/dataset 
2. BCO-DMO needs to update the metadata of its legacy catalog to include the discrete coordinates at which measurements have occurred. Bounding box spatial coverage is not enough becuase it could providee false positives and more than likely has a broader coverage area than a single point with proximity. 
3. Our Elasticsearch index can correctly calculate geo features within other features
4. BCO-DMO metadata includes instrumentation used in collecting the data.
5. ERDDAP provides subsetting on the depth variable

## TO-DO ##

1. Process BCO-DMO data through a geospatial indexer that will identify all unique points in all datasets.
2. Add this list of unique points into the metadata at BCO-DMO for use in Elasticsearch.
3. Provide a capability in Leaflet to specify tha tthe search shoudl only return datasets _within_ the selected proximity.
