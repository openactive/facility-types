# Facility Types

> Status: Draft | [Please Provide Feedback via GitHub](https://github.com/openactive/facility-types/issues)

## Status

This list is in a draft state, however every effort will be made in subsequent revisions to maintain the IDs associated with the concepts enumerated here.

## Documentation

This repository holds the [JSON-LD definition](https://www.openactive.io/facility-types/facility-types.jsonld) of the OpenActive Accessibility Support controlled vocabulary.

This controlled vocabulary MUST be referenced within a `Concept` via `inScheme` using the URL `"https://openactive.io/facility-types"` (which will return the [JSON-LD definition](https://www.openactive.io/facility-types/facility-types.jsonld) if the `Accept` header contains `application/ld+json`).

Please raise requests for content or issues related to this controlled vocabulary via [GitHub](https://github.com/openactive/facility-types/issues). 

## Example use

The example below illustrates an `"beta:facilityType"` property for an `FacilityUse` that supports all defined accessibility groups.

```json
"beta:facilityType": [
  {
    "type": "Concept",
    "id": "https://openactive.io/facility-types#a5ac16fe-06ac-4bc1-93f7-69ff3bfcf3b9",
    "prefLabel": "3G Artificial Grass",
    "inScheme": "https://openactive.io/facility-types"
  }
]
```

## Source data

Please see a link to spreadsheet used to generate the JSON-LD representation [here](https://docs.google.com/spreadsheets/d/1ZZ1J13Ry3y8p5nA2Voady98A3dZocvGebuNu1PYIveI/edit#gid=1428772490), comments welcome!


## Licence

The documentation and data in this repository is published under the [Creative Commons CC-BY 4.0](https://creativecommons.org/licenses/by/4.0/) license.

