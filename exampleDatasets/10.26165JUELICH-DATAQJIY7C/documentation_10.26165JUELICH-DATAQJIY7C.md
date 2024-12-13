# Analysis and annotation of "Field Phenotyping of Ten Wheat Cultivars under Elevated CO2 Shows Seasonal Differences in Chlorophyll Fluorescence, Plant Height and Vegetation Indices"
- Entities identified: Crop, Plot, Camera/Sensor
- Dataset summary: Field phenotyping experiment on CO2 addition, references camera files


# Crop
- outcome: instead of drafting a new Type for Crop, we explored the possibility of modeling a Crop as a BioSample and adding the properties that we need for findability as additionalProperty of a Biosample. By pointing to a terminology (AGROVOC) in this case, we can enrich these additionalProperty instances with semantic concepts. The entities relevant to us are connected to each other via a LabProcess entity

## Challenges
- value for taxonomicRange: model as its own complex taxon object vs. just providing a link to terminology (e.g. NCBI Taxon)
- do we need a name for a crop? Is an identifier enough?
- do we need variety and cultivar properties?
	- variety seems to be enough, but we need to extend the variety property definition to also inlcude cultivars
- links to varieties in terminologies might be nice, but isnt realistic
- do we need a plantedIn as a property? --> having the more generic way of using LabProcess LabProtocol 
- Using LabProcess/LabProtocol
	- how do we provide units in the LabProtocol as input properties?
- do we lose something if we change the type from "Crop" to "Plant"? --> shouldn't be a problem
- questions to Bioschemas: is creating a new property 'enough' for creating a new type?
- question to ARC guys: where would we need to put the information that we currently model as a "Crop" (variety) when following the LabProcess/LabProtocol route?
	- discussion result: modeling an object as BioSample instead of creating a new type

# Plot
## Challenges
- most likely a plot will be some kind of "Place" with geocoordinates --> is this enough for searching?
	- after the current discussions it be added to a dataset using the "location" property of LabProcess

# Camera/Sensor


## Challenges
- likely no new type as subtype of "Product" needed, more likely an approach using "DefinedTerm" makes more sense
	- linked to the dataset via "equipmentUsed" of a LabProtocol