# OpenActive Facility Types List [![Google Drive](https://img.shields.io/badge/Google%20Drive-4285F4?logo=google-drive&logoColor=white)](https://drive.google.com/drive/folders/1O7qjm1mickj0Ftdn9BFV5Srn8l2CkCBS)

This repository holds the data and documentation for the OpenActive Facility Types controlled vocabulary.

A Facility Type is a category of places or venues where physical activities, sports, or other forms of bodily movement occur.
Facility types include not just sports venues, but also a variety of facilities such as gyms, swimming pools, and fitness studios.
A Facility Types List defines a list of these physical activity venues.

A standardised facility types list, that provides unique identifiers, labels and descriptions for facility types can:

* support integration of data published by multiple activity providers
* improve user experience across applications through use of a standard set of facility names and definitions
* enable better discovery and recommendation tools to enable participants to find more opportunities to be active

The list is publicly available at [https://www.openactive.io/facility-types/](https://www.openactive.io/facility-types/).

## Dataset Documentation

The dataset is structured according to the [SKOS](https://www.w3.org/TR/skos-primer/) standard for publishing controlled vocabularies.

It consists of:

* a list of terms with an identifier (a URI) and a preferred label (`skos:prefLabel`)
* relationships between terms (`skos:broader`, `skos:narrower` and `skos:related`)
* alternative labels / synonyms (`skos:altLabel`)

### Identifiers

Terms in the list have been assigned a UUID to generate a unique identifier. The URIs for each term are [Patterned URIs](http://patterns.dataincubator.org/book/patterned-uris.html) that combine these UUIDs with a common prefix:

E.g. Squash Court has been assigned a UUID of `a1f82b7a-1258-4d9a-8dc5-bfc2ae961651`. Its URI is `https://openactive.io/facility-types#a1f82b7a-1258-4d9a-8dc5-bfc2ae961651`

### JSON-LD

The [JSON-LD version of the list](https://openactive.io/facility-types/facility-types.jsonld) provides a simple JSON version of the list that conforms to the [JSON-LD](https://www.w3.org/TR/json-ld/) specification.

This controlled vocabulary MUST be referenced within a `Concept` via `inScheme` using the URL `"https://openactive.io/facility-types"`.

The JSON-LD version of this controlled vocabulary SHOULD be retrieved frequently using an HTTP GET and cached within an application, to ensure that the most up-to-date version is displayed to the user, while also protecting against network failure when accessing the underlying resource. To access this controlled vocabulary the application MUST GET the URL [`"https://openactive.io/facility-types/facility-types.jsonld"`](https://openactive.io/facility-types/facility-types.jsonld) (note there is no www in the URL) which does not require a specific `Accept` header, and is cached via CDN. The controlled vocabulary is also available via a GET of the URL [`"https://openactive.io/facility-types"`](https://openactive.io/facility-types) using an `Accept` header of `application/ld+json`, for completeness, however this shorter URL MUST NOT be used in production.

## Example use

The example below illustrates a `"facilityType"` property for an `FacilityUse` that describes a Squash Court.

```json
"facilityType": [
  {
    "type": "Concept",
    "id": "https://openactive.io/facility-types#a1f82b7a-1258-4d9a-8dc5-bfc2ae961651",
    "prefLabel": "Squash Court",
    "inScheme": "https://openactive.io/facility-types"
  }
]
```

## Publication process

The master ('canonical') version of the Facility Types List is that found at [https://www.openactive.io/facility-types/](https://www.openactive.io/facility-types/). That list is stored within [iQvoc](http://iqvoc.net/), and the list editor can choose to trigger a [workflow](https://github.com/openactive/skos-vocabulary-workflows) to update this repository. The resulting `facility-types.jsonld` is updated and served at `https://openactive.io/facility-types/facility-types.jsonld` via GitHub pages.

Note that new `Concepts` will not be validated unless a machine-readable (no spaces, all lowercase) `notation` is provided with them, and this `notation` value must be unique within the List.

## Licence

The documentation and data in this repository is published under 
the [Creative Commons CC-BY 4.0](https://creativecommons.org/licenses/by/4.0/) license.
