The file `ro-crate-metadata.json` is a draft example trying to model the dataset contained in the parent folder (doi:10.7910/DVN/M9ZT0F/NKX5XD) based on RO-Crate and bioschemas vocabulary.

As per the RO-Crate specification, the "center"/focus of the metadata file is the dataset. The individual files pertaining to the dataset are described via the `hasPart` relationship.

We do not try to fully model the complex semantic relationships between the dataset, included studies, individual treatments and plots. Instead, the idea is to have a morge lightweight relationship between the dataset and key concepts to enhance findability of the dataset.

Currently included key concepts:

- Relationship between the dataset and the crop that was used (via `schema:about->bioschemas:Taxon`)
  - including the crop variety, at two individual taxonomic definitions (one for the species, one for the variety)

An alternative would be to connect the Dataset to the crop via `isBasedOn -> a bioschemas:Study -> studySubject -> a BioChemEntity (a Crop)`, see also the more MIAPPE-oriented approach as in here: https://github.com/BioSchemas/specifications/issues/478 / here: https://docs.google.com/spreadsheets/d/19yacJXhjmq-jBBCgli43yZ_BLerdeU0bmHWKvmkwxmE/edit#gid=0

Next TODOs: include soil information, measured variables / measurementTechnique ?

NOTE: actual data files have not been commited, purpose is the demonstration of the metadatafile
