# Crop

## Schema.org hierarchy
[Thing](http://schema.org/Thing) > [BioChemEntity](https://bioschemas.org/BioChemEntity) > Crop

## Description
Any plant or plant product grown for a specific purpose.

## Properties

- Property Name: variety
	- Expected Type: [Text](https://schema.org/Text), [URL](https://schema.org/URL), 
	- Description: A plant variety represents a more precisely defined group of plants, selected from within a species, with a common set of characteristics. 
	- Example queries:
		- Finding datasets for which the variety "Absolut" was used
- Property Name: cultivar
	- Expected Type: [Text](https://schema.org/Text), [URL](https://schema.org/URL)
	- Description: A plant type cultivated through human manipulation. 
	- Example queries:
		- Finding datasets for which the cultivar "Harenda" was used		
- Property Name: plantedIn
	- Expected Type: Soil, Plot
	- Description: A soil or plot instance a specific crop was planted in.
	- Example queries:
		- Finding datasets where a crop was planted in soils with increased magnesium concentration
		- Finding datasets where a crop was planted in Northrhine Westfalia, Germany
- Property Name: cropSowingPeriod
	- Expected Type: [Date](https://schema.org/Date)
	- Description: A time period when the described crop was planted.
	- Example queries:
		- Finding datasets where a crop was planted between May and June 2024.
- Property Name: cropResiduesRemoval
	- Expected Type: [Text](https://schema.org/Text)
	- Description: Indicator if/how much residue of the described crop after harvest was removed.
	- Example queries:
		- Finding datasets where crop residues where removed completely after harvesting
- Property Name: cropResiduesIncorporation
	- Expected Type: [Text](https://schema.org/Text)
	- Description: Indicator if crop residue was incorporated into the soil after harvesting.
	- Example queries:
		- Finding datasets where crop residues incorporated after harvesting
- Property Name: cropResiduesBurning
	- Expected Type: [Text](https://schema.org/Text)
	- Description: Indicator if crop residue was burned after harvesting.
	- Example queries:
		- Finding datasets where crop residues were burned after harvesting
- Property Name: ?
	- Expected Type: ?
	- Description: ?
	- Example queries:
		- ?