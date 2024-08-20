# Soil

## Schema.org hierarchy
[Thing](http://schema.org/Thing) > Soil

## Description
Any unconsolidated mineral or organic material on the immediate surface of the Earth that serves as a natural medium for the growth of land plants. [Source](https://www.nrcs.usda.gov/resources/education-and-teaching-materials/what-is-soil)

## Properties
- Property Name: soilTextureClass
	- Expected Type: [Text](https://schema.org/Text), [URL](https://schema.org/URL), [DefinedTerm](https://schema.org/DefinedTerm)
	- Description: Classification of this Soil based on its relative proportions of sand, silt or clay. 
	- Comment: should use values from the USDA soil classification: "S; LS; SL; SCL; SiL; SiCL; CL; L; Si; SC; SiC; C; HC; VFS; FS; MS; CS; US; LVFS; LFS; LCS; FSL; CSL"
	- Example queries:
		- Find a dataset with data on clay loam soil.
- Property Name: soilInitialSamplingDate
	- Expected Type: "[Date](https://schema.org/Date), [DateTime](https://schema.org/DateTime)"
	- Description: The date a sample of this specific soil was taken.
	- Example queries:
		- Find a dataset with soil data taken in April 2021.
- Property Name: soilBulkDensity
	- Expected Type: "[Text](https://schema.org/Text), [PropertyValue](https://schema.org/PropertyValue)"
	- Description: Indicator for this specific soils compaction.
	- Comment: unit: g.cm-3
	- Example queries:
		- Find a dataset with soil with a bulk density between 1.3 and 1.8.
- Property Name: soilPH
	- Expected Type: "[Text](https://schema.org/Text), [PropertyValue](https://schema.org/PropertyValue)"
	- Description: pH value of this specific soil.
	- Example queries:
		- Find a dataset with soil with a pH value between 6 and 8.
- Property Name: soilOrganicCarbon
	- Expected Type: "[Text](https://schema.org/Text), [PropertyValue](https://schema.org/PropertyValue)"
	- Description: Percentage of of measurable organic carbon components in this specific soil.
	- Example queries:
		- Find a dataset with organic carbon values between 3 and 5 percent.

