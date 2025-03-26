
# Example dataset: "Temporal dynamics in the compositional relationships of cropland microbiomes"
- Link: https://doi.org/10.3220/DATA20240627155423-0
- Crops, Agricultural management activities, Fields,, Weather, Soil, Genes


#  Crops
- Information taken from "F1_AgricMan" file/"Main crop" column
- Q: The crop species taken from agrovoc might not be perfectly accurate, how can this be improved?

#  Agricultural management activities
- Information taken from "F1_AgricMan" file
- The agricultural management activities are defined in a table and could most likely be modeled using the https://bioschemas.org/LabProcess and https://bioschemas.org/LabProtocol types
	- to do: create https://bioschemas.org/LabProcess and https://bioschemas.org/LabProtocol objects for each of the activities listed in the "Treatment" table and use them to connect the other entity objects (fields, crops, equipment, etc.)

# Fields
- Information taken from "F1_AgricMan" file
- Fields include coordinates and very basic soil information
- The field information also includes very general soil texture composition information. Currently this has been attached to the field objects via https://schema.org/additionalProperty
	- Q: how to separate soil information here? Should it belong to the field object or to the soil objects containing other soil information? where to draw the line?

# Soil
- information taken from "F3_SoilParam" file
- modeled as a https://bioschemas.org/Sample following the new drafted properties of the "Sample" type: https://discovery.biothings.io/ns/bioschemastemptype/bioschemastemptype:Sample
- Q: "locationOfOrigin" can point to a https://schema.org/Place. How do you correctly reference the Field object from the same JSON-LD file as a value of "locationOfOrigin"?
- beside a date of the sample creation (modeled via "dateCollected") the season a sample was taken in was modeled via https://schema.org/additionalProperty
	- Q: implications of providing the season as https://schema.org/Text vs. making it a https://schema.org/StructuredValue to use a semantic resource (e.g. https://agrovoc.fao.org/browse/agrovoc/en/page/c_6911)
- Soil parameters (carbon, nitrogen, pH and carbon to nitrogen ration) were modeled via https://schema.org/additionalProperty
	- Q: Units are essential for these values but were not added to the file. How can we make providing units as easy as possible? Make Unit Ontology usable? https://www.ebi.ac.uk/ols4/ontologies/uo
	- Q: The file "F4_GenCopNum" includes information of bacteria, archaea and fungi abundance in soil samples. Is this a relevant property for our FAIRagro use cases?
	
# Weather
- information taken from "F2_Meteorol" file
- Q: The measurements of "Precipitation (per two weeks)" and "Temperature" seem to be related to the same samples taken for the soil (same "SampleID, "site", "Sample year", "Date", "Sample Time", "seasons") --> Should they be attached to the soil sample objects, the Field place objects or be their own objects? Which type should they be?

# Fungi, prokaryots and protists
- The files "F5_ASV_Proka", "F6_ASV_Fungi" and "F7_ASV_Protists" include additional information on these types of entities
	- Q: Are these relevant for our FAIRagro use cases?

# To-Dos
- create https://bioschemas.org/LabProcess and https://bioschemas.org/LabProtocol version of the metadata set to explore agricultural management activity modeling