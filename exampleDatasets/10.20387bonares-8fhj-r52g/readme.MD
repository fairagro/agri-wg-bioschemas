

# Example dataset: "Long-term field experiment V140 Muencheberg from (launched in 1963) - Plots"
- Link: https://doi.org/10.20387/bonares-8fhj-r52g
- 

# Field
- Information taken from "PARZELLE_V140" file and modeled as schema:Place.
- Properties created:
	- Cell name -> Property
		- "Grobsand__0_bis_25__1980" -> "coarseSand"
		- "Mittelsand__0_bis_50__1980" -> "mediumSand"
		- "Feinsand__0_bis_25__1980" -> "fineSand"
		- "Grobschluff__0_bis_25__1980" -> "coarseSilt"
		- "Mittelschluff__0_bis_25__1980" -> "mediumSilt"
		- "Feinschluff__0_bis_25__1980" -> "fineSilt"
		- "Ton__0_bis_25__1980" -> "clay"
# Crop
- Information taken from "KULTUR" file and modeled as bioschemas:BioSample.
- Cell name -> Property
		- "Kultur" -> "taxonomicRange"
		- "Icc_Code" -> "iccCode"

# Soil
- Information taken from "BODENLABORWERTE" file and modeled as bioschemas:Sample.
- Properties created:
	- Cell name -> Property
		- "Ph_Wert" -> "soilpHValue"
		- "Ct" -> "soilCt"
		- "Nt" -> "soilNt"
		- "P" -> "soilP"
		- "K" -> "soilK"
		- "Mg" -> "soilMg"
		- "Ca" -> "soilCa"
		- "B" -> "soilB"
		- "Cu" -> "soilCu"
		- "Mn" -> "soilMn"
- Additional information was taken from "PROBENAHME_BODEN" file
	- Cell name -> Property
		- "Tiefe_Oben" -> "soilTopDepth"
		- "Tiefe_Unten" -> "soilBottomDepth"

# Pesticides
- Information taken from "PFLANZENSCHUTZ_MITTEL" file and modeled as bioschemas:ChemicalSubstance.
	- Cell name -> Property
		- "Name" -> "name"
		- "Zulassungsnummer" -> value of "identifer"


# To-Dos / Challenges
- How to deal with coordinates of Place entities?
- The "Parzelle" file includes properties that could be part of a soil entity
- Combine the different entities through modeling processes (e.g. sowing (AUSSAAT file)) by using LabProcess/LabProtocol
