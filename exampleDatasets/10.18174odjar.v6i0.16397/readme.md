# Analysis and annotation of https://doi.org/10.18174/odjar.v6i0.16397
- Entities identified: Crop, Soil, Fertilizers, Weather, Pesticides


# Crop
- "name" --> unclear
- "taxonomicRange" --> "Triticum aestivum" taken from **"description"** field and provided as Agrovoc class
- "variety" --> no information available
- "cultivar" --> "Triticum aestivum, **c.v. Batis**" taken from **"description"** field and provided as string
- "plantedIn":"soil_001" --> reference to soil object
- "cropSowingPeriod" --> two dates available in the data file in **"phenology"** sheet
- "cropResiduesRemoval" --> no information available
- "cropResiduesIncorporation" --> no information available
- "cropResiduesBurning" --> no information availbale

## Challenges
- The "phenology" sheet includes additional information on the crop and its growth stages. Due to being bound to specific dates, this information doesn't lend itself well to attaching it directly to a single crop entity/object, but might be modeled using something process based like [https://bioschemas.org/LabProcess](https://bioschemas.org/LabProcess) --> discuss
- Additional crop information on **"grain growth"** and  **"grain quality"** available on corresponding sheets also date based --> needed for search capabilites? It might be possible to model the measured grain quality variables as https://schema.org/variableMeasured but this would need to be attached directly to the https://schema.org/Dataset, not the crop enitity --> discuss

# Soil 
- "name" --> unclear
- "soilTextureClass" --> taken from **"soil properties"** sheet and provided as string
- "soilInitialSamplingDate" --> taken from **"soil moisture"** sheet and provided as string
- "soilBulkDensity" -> taken from **"soil properties"** sheet and provided as string
- "soilPH" --> no information available
- "soilOrganicCarbon" --> no information available
- **"?soilMoisture"** --> sheets with data available --> **relevant property for extension?**

## Challenges
- Similar to the challenges for crop --> additional time based data on soil measurements (**""soil moisture""** sheets) --> discuss
- "soilInitialSamplingDate" --> should this also be modeled process based?

# Fertilizers
- "name" --> taken from **"management"** sheet
- "fertilizerType" --> information not available in the data but derived from fertilizer names and provided as Agrovoc class
- "fertilizerProductName" --> not available
- "fertilizerApplicationRate" --> taken from **"management"** sheet
- "fertilizerApplicationRateUnits" --> taken from **"management"** sheet

## Challenges
- The application rate for the "Kieserite" fertilizer is static, therefore it was provided directly via the properties of the fertilizer object. The application rates for the "ammonium nitrate" fertilizer change --> should this also be modeled process based?

# Weather
/
# Pesticides
- only information available: "exact names no more available" on **"management"** sheet



