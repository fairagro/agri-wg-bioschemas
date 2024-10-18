

# Project abstract

Research Data Infrastructures (RDIs) provide crucial publication services for researchers in the agrosystem domain. Due to their heterogeneous user communities and requirements, metadata standardization approaches to increase the FAIRness of resources can be a catalyst in simplifying data reusability and enabling cross-domain research.

One way for RDIs to increase the Findability of their resources is to provide metadata markup via Schema.org, a vocabulary consumed by well-known search engines. Bioschemas, an extension of schema.org focussed on the life sciences, is an open community effort, aiming at increasing the adoption of key metadata properties in a domain-targeted manner, through the creation of needed domain-associated types, agreed properties and usable metadata profiles for describing those life science resources. The project will work on developing new resources (types, properties, profiles) for Bioschemas, which will help to describe agrosystem datasets in a FAIR manner.

Participants will work on different topics, ranging from evaluating the current state of developed types and properties relevant to agrosystem resources to drafting new ones following use-case requirements and using example datasets. For increasing the metadata quality and supporting RDIs and their users in adopting the extension, participants will link properties to domain ontologies and facilitate mappings to other metadata standards, bolstering interoperability while following mapping frameworks like FAIR-IMPACT’s approach. To further ease the adoption for RDIs, participants will work on creating guidance and best practice documents on how to implement the extension into existing metadata description processes.

# Topics & requirements
## Evaluation of the current state of the extension by annotating example datasets [Task 1]
### Description
This task tests the limits of the extension in its current form. By trying to describe core agrosystem entities of example datasets with the drafted Types and Properties, participants will familarize themselves with the existing metadata resources and identify possible gaps, which can be closed by further developing the Types & Properties.
### Goals & outcomes
- participants familarize themselves with the basics of schema.org [1] (if needed)
- participants learn about the current state of the extension [2]
- participants choose example datasets based on their domain knowledge and annotate them withe the available Types & Properties [3] [4]
- participants will record the challenges and their feedback to generate insights needed for the following task of further schema development [5]
- a set of example datasets annotated with the extension [6]
### Preparation
- [1] A basic introduction to schema.org
- [2] https://github.com/fairagro/agri-wg-bioschemas/tree/main/Types
- [3] https://github.com/fairagro/agri-wg-bioschemas/blob/main/exampleDatasets/exampleDatasets.csv
- [4] readme on how to annotate and use the templates
- [5] template for data annotation notes
- [6] example dataset (done!)

## Development of new Types and Properties [Task 2]
### Description
With the outcomes of [Task 1] as a foundation participants will work together on further developing the core entities of the extension by defining new Properties for them or refining existing properties and their definitions. If new core entitites (Types) are identified as necessary, these will be drafted as well. These developments will follow well defined processes [1]. One of the outcomes, a new version of the extension, can then be used to revisit example datasets that could not be annotated beforehand.
### Goals & outcomes
- a further developed version of the extension
- an expanded set of example datasets annotated with the extension
### Preparation
- [1] A guide/process description on how to extend the Types & Properties

## Linking the extension to domain terminologies [Task 3]
### Description
Some of the properties of the extension provide benefits towards interoperability and findability if they are used in combination with semantical resources such as ontologies/terminologies/vocabularies [1]. The bolster the reuse of existing semantic resources participants will research fitting semantic resources and add references to them to the extension documentation.
A special case of these properties are measured variables in the example datasets. If datasets include descriptions of variables [2] they are rarely linked to semantic concepts. To evaluate how many and which of these variables already exist in ontologies/terminologies/vocabularies could grant insights on how to proceed in this regard in the future.
### Goals & outcomes
- a list of semantically appropriate domain ontologies/terminologies/vocabularies for the extension
- a list of terms of subsets and specific terms of these ontologies/terminologies/vocabularies linked to specific properties in the extension
### Preparation
- [1]: A list of possible relevant ontologies/terminologies/vocabularies and a way of searching through their contents (links to terminology repositores such as [OLS](https://www.ebi.ac.uk/ols4)?)
- [2]: A way of storing relations of properties to ontologies/terminologies/vocabularies in a consistent way (maybe as part of the general extension definition files?)

## Mapping to other schemas [Task 4]
### Description
To increase chances of uptake and adoption of the extension by service providers such as Research Data Infrastructures, this task will map [1] the Types & Properties of the extension to already existing metadata schemas & standards [2].
### Goals & outcomes
- a list of mapping statements between Types & Properties of the extension and other metadata resources
### Preparation
- [1]: A structure and vocabulary for defining the mappings (would [SSSOM](https://mapping-commons.github.io/sssom/) work here? In the proposal we mentioned [FAIR-IMPACT's mapping approach](https://fair-impact.eu/events/fairimpact-events/why-mappings-matter-and-how-make-them-fair), this might also be a good candidate)
- [2]: A list of possible relevant metadata schemas & standards to map to

## Guidance and best practice documents for Research Data Infrastructures when adopting the extension [Task 5]
### Description
The results of the previous tasks will lead to insights on how to support Research Data Infrastructures in adopting the extension. By creating best practice documents and collecting identified challenges during the Hackathon work, this task will condense the results and make them available to one of the relevant stakeholder groups.
### Goals & outcomes
- A (set) of document(s) that can be distributed to domain RDIs to support them if they decide to generate markup with the extension
### Preparation
- ?

## Development of conversion scripts for homogeneous field trial datasets [Task 6]
### Description
tbd
### Goals & outcomes
### Preparation
- datasets need to be well curated beforehand
