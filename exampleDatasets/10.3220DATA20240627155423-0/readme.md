
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



# To-Dos 


