This dataset was provided by @universaldilettant


# Description
It includes multiple sheets on management activities of an experiment
- Site (location name, soil type, NStE [?], number of plots, temperature[yearly average], precipitation [yearly average])
- A_u_P (year, location name, previous crop, soil, basic tillage [date], sowing [date], harvest [date], seeding strength)
- Soil (year, location name, date, ph value, K2O [mg in 100g soil], P2O5 [mg in 100g soil], Mg [mg in 100g soil], B [mg in 1000g soil], Cu [mg in 1000g soil], S [mg in 1000g soil], Mn [mg in 1000g soil])
- Nmin (year, location name, date, n-min 0-30cm [N-min in kg/ha], n-min in 30-60cm [N-min in kg/ha], n-min in 60-90cm [N-min in kg/ha])
- Dueng_konst (year, location name, date, BBCH, fertilizer name, N, P2O5, K2O, MgO, CaO, S)
- PSM_konst (year, location, date, BBCH, pesticide name, volume, area)
- PSM_fakt (year, location name, date, BBCH, pesticide name, volume, area, stage)

## Modelling approach
- Each of the locations, where experiments were held, is modelled as a Study (following ISAs meaning)
- Each of the different activities (sowing, tilling, etc.) is modelled as an assay. This also means having different assays for the same acitivity  in different years
- Each of the assays has one LabProcess, which links to a LabProtocol, that can be shared between LabProcesses
- Entities (people, locations, etc.) are reused as much as possible by refering to their ids

# Challenges
## Study layer
- Modeling each experiment site as a study and modeling the general experimental design (contents of 'Site' sheet) as a ISA study
-- LabProcess for the Study design, the related LabProtocol requires a BioSample --> what would this be in such a case?
-- LabProtocol requires a 'labEquipment' --> what would this be when modeling general study design as a LabProtocol?
-- same question for 'reagent'

## Assay layer
- Should each activity (sowing, soil preparation, etc.) at a location be modeled as its own assay or should it be one assay with multiple LabProcess/LabProtocol pairs?
