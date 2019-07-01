
# Find Data Related to Taxonomic Group #

## Status ##
_Proposed_

## Description ##
I want to find all datasets with observations made about _calanus finmarchicus_.

## What is Needed ##

1. To know how and where taxonomic information is recorded. This may be in the following places:
    1. dataset descriptive text, 
    2. in a parameter name, 
    3. or as a recoreded observation value (data cell, etc.)
2. (optional) know taxonomic identifiers such as WoRMS.

## How is BCO-DMO Addressing the Needs ##

1. Currently, dataset search can find the mention of _calanus finmarchicus_ in the dataset description, project description and other free text descriptions as well as in any reported parameter name.
2. Identify when a dataset parameter contains taxonomic information: a text label for a classification or a column of identifiers such as WoRMS.
3. For these datasets, calculate the unqiue taxons and record in the metadata for search.

## TO-DO ##

1. For any parameter marked as `taxon` process the data for unique values and record the result in the metadata.
2. For any parameter marked as `identifier` determine if it is a taxonomic identifier. If so, calculate the unique result set of these identifiers, resolve them to retrieve the taxonomic name and record in the metadata.
3. Add this list of unique taxonomic names (and identifiers, if avaialble) into the metadata at BCO-DMO for use in Elasticsearch.
3. Provide a capability in the dataset set for a taxonomic filter so that datasets can be explicitly filtered by this value.
