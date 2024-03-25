# Introduction
The repository is used by the Agri Bioschemas working group for drafting and discussing modelling ideas for extending the [Bioschemas](https://bioschemas.org/) vocabulary with new types, properties and profiles.

# Structure
Developments are distinguished between Types and Profiles, each with their respective folders and subfolders. Each Type/Profile then follows the same structure, which is derived from the [Bioschemas specificiation Github repository](https://github.com/BioSchemas/specifications):

 - useCases : A markdown file with a textual description of the use cases that reflect the requirements for the specific Type/Profile. This is meant to motivate the developments of the new Types/Profiles.
 - examples: A sub-directory to develop modelling ideas e.g. by modelling schema.org/bioschemas metadata descriptions of use-case datasets. Each dataset should be worked on in its own subdirectory
 - jsonld_type: A folder containing the JSON-LD markup, that is meant to be submitted to Bioschemas via the [DDE](https://discovery.biothings.io/schema-playground). 

