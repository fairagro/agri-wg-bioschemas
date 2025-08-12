---
config:
  theme: redux
---
flowchart LR
    A(["Dataset001"]) -- @type --> B("schema.org:Dataset")
    A -- about --> C(["Sample001 (soil)"])
    C -- @type --> D("Bioschemas:Sample")
    C -- additionalProperty --> E([" "])
    E -- @type --> F("schema:PropertyValue")
    E -- name --> G(["soilTexture"])
    E -- propertyID --> H("link to semantic concept of soilTexture")
    E -- value --> I([" "])
    I -- @type --> J("schema:PropertyValue")
    I -- value --> K(["coarse sand"])
    I -- propertyID --> L("link to semantic concept of coarse sand")
