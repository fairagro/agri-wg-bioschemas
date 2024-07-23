
# LabProcess and LabProtocol example data snippets

This folder includes example snippets of metadata expressed as [LabProcess](https://bioschemas.org/LabProcess) and [LabProtocol](https://bioschemas.org/LabProtocol)

- AuP_precrop.json
    - The LabProcess describes the sowing and harvest of a specific precrop ("Vorfrucht") as part of a specific agricultural experiment.
    - It includes:
	    - [startTime](https://bioschemas.org/startTime) (sowing) 
	    - [endTime](https://bioschemas.org/endTime) (harvest)
	    - information on the seeding strength ("Aussaat-stärke Körner/m²") via [parameterValue](https://bioschemas.org/types/LabProcess/0.1-DRAFT#parameterValue)
	    - information on the precrop (as our planned Crop type, including dummy information on a fictional variety) via [object](https://schema.org/object)
	    - a link to a precrop LabProtocol(https://bioschemas.org/LabProtocol)
   - The LabProtocol includes information on:
	    - bioSample, which points to the same resource as the [object](https://schema.org/object) property in the LabProcess
	    - intendedUse, containing a human readable description of the LabProtocol
			- two types of agricultural equipment used for executing the LabProtocol, modeled as [DefinedTerm](https://pending.schema.org/DefinedTerm)
	- Open questions:
	  - LabProcess:
		  - In this case there is no result that needs to be described through metadata. Is this still a valid LabProcess?
		  - If we would want to describe multiple objects (e.g. the soil that the precrop was planted in), is it possible to define a set of objects as an array?

- Dueng_konst_product.json
    - The two LabProcess objects describe the application of a fertilizer on different points in time during an experiment with different concentrations of its chemical components
		- They include:
		    - [startTime](https://bioschemas.org/startTime) and [endTime](https://bioschemas.org/endTime) for each application
        - information on the fertilizer "Nitrophoska" as a [ChemicalSubstance](https://bioschemas.org/ChemicalSubstance) via [object](https://schema.org/object)
				- information on the concentration of components the fertilizer via [parameterValue](https://bioschemas.org/types/LabProcess/0.1-DRAFT#parameterValue)
	- Both LabProcess objects link to the same LabProtocol object
		- It includes:
		    - intendedUse, containing a human readable description of the LabProtocol
				- the chemical components of the fertilizer as [PropertyValue](https://schema.org/PropertyValue)s, linked via [reagent](https://bioschemas.org/types/LabProtocol/0.5-DRAFT#reagent)
				
-	PSM_konst_product.json
    - The two LabProcess objects describe the application of two different pesticides at the same location at different points in time
		- They include:
		    - [startTime](https://bioschemas.org/startTime) and [endTime](https://bioschemas.org/endTime) for each application
				- information on the pesticides "FOXTRIL SUPER" and "CONCERT SX" as [ChemicalSubstance](https://bioschemas.org/ChemicalSubstance)s via [object](https://schema.org/object)
				- information on the specific application of the pesticides via [parameterValue](https://bioschemas.org/types/LabProcess/0.1-DRAFT#parameterValue)
	- Both LabProcess objects link to different LabProtocol objects, one for each used pesticide
		- They include:
				- intendedUse, containing a human readable description of the LabProtocol
				- General application instructions for the specific pesticide via [protcolApplication](https://bioschemas.org/types/LabProtocol/0.5-DRAFT#protocolApplication)
				
