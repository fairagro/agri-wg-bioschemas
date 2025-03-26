
# Example dataset: "Data from the winter wheat potential yield experiment in New Zealand and response to variable sowing dates and densities: field experiments and AgMIP-Wheat multi-model simulations"
- Link: https://doi.org/10.7910/DVN/XA4VA2
- Field, Crop and Soil metadata taken from NZ_AgMIP_dataset.xlsx file

# Field 
- Information taken from "Fields" sheet and modeled as https://schema.org/Place.
- "elevation" is currently modeled via https://schema.org/additionalProperty but we could also use https://schema.org/elevation if we attach the coordinates not directly to https://schema.org/Place but to a https://schema.org/GeoCoordinates object via https://schema.org/geo. What are the different implications?
- Is location metadata such as city names relevant? How to model?

# Crop
- information taken from "Genoytpe" sheet
- Only cultivar information available, taxonomy unclear, only named as "winter wheat"
- which propertyID to use? http://aims.fao.org/aos/agrovoc/c_8157 vs. http://aims.fao.org/aos/agrovoc/c_1423211760123
- use generic property such as http://aims.fao.org/aos/agrovoc/c_16022 for cultivar origin?

# Soil
- information taken from "Soil_metadata" and "Soil_profile_layers" sheet
- soil texture
	- Where to put code of value? Example: "CLLO" for "Clay loam"
	- How to model controlled vocabulary IRIs for values? There should for example be a semantic resource for "Clay loam" and other possible values of a soil texture classification

# Model
- To-Do: How to represent information on crop models in the metadata?


 # To-Dos 
 - Try to model experimental design and processes (Treatments etc.) via LabProcess/LabProtocol


