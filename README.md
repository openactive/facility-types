# Facility Types

> Status: Draft | [Please Provide Feedback via GitHub](https://github.com/openactive/facility-types/issues)

## Status

This list is in a draft state, however every effort will be made in subsequent revisions to maintain the IDs associated with the concepts enumerated here.

## Documentation

This repository holds the [JSON-LD definition](https://openactive.io/facility-types/facility-types.jsonld) of the OpenActive Facility Types controlled vocabulary.

This controlled vocabulary MUST be referenced within a `Concept` via `inScheme` using the URL `"https://openactive.io/facility-types"` (which will return the [JSON-LD definition](https://openactive.io/facility-types/facility-types.jsonld) if the `Accept` header contains `application/ld+json`).

This controlled vocabulary SHOULD be retrieved frequently using an HTTP GET and cached within an application, to ensure that the most up-to-date version is displayed to the user, while also protecting against network failure when accessing the underlying resource. To access this controlled vocabulary the application MUST GET the URL `"https://openactive.io/facility-types/facility-types.jsonld"` (note there is no www in the URL) which does not require a specific `Accept` header, and is cached via CDN. The controlled vocabulary is also available via a GET of the URL `"https://openactive.io/facility-types"` using an `Accept` header of `application/ld+json`, for completeness, however this shorter URL MUST NOT be used in production.

Please raise requests for content or issues related to this controlled vocabulary via [GitHub](https://github.com/openactive/facility-types/issues). 

## Example use

The example below illustrates an `"facilityType"` property for an `FacilityUse` that describes a 3G Artificial Grass pitch.

```json
"facilityType": [
  {
    "type": "Concept",
    "id": "https://openactive.io/facility-types#a5ac16fe-06ac-4bc1-93f7-69ff3bfcf3b9",
    "prefLabel": "3G Artificial Grass",
    "inScheme": "https://openactive.io/facility-types"
  }
]
```

## Source data

Please see the [spreadsheet](https://docs.google.com/spreadsheets/d/1ZZ1J13Ry3y8p5nA2Voady98A3dZocvGebuNu1PYIveI/edit#gid=0) used to generate the JSON-LD representation, comments welcome!


## Licence

The documentation and data in this repository is published under the [Creative Commons CC-BY 4.0](https://creativecommons.org/licenses/by/4.0/) license.

