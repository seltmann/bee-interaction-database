## Bee Interaction Database

[![Build Status](https://travis-ci.org/seltmann/bee-interaction-database.svg)](https://travis-ci.org/seltmann/bee-interaction-database)  [![GloBI](http://api.globalbioticinteractions.org/interaction.svg?accordingTo=globi:seltmann/bee-interaction-database)](http://globalbioticinteractions.org/?accordingTo=globi:seltmann/bee-interaction-database) 

[```Citation```](#Citation) / [```Interaction Types```](#interaction-types) / [```Data Definitions```](#data-definitions) / [```Included Resources```](#included-resources) /  [```Data Issues```](#data-issues) / [```Summary```](#summary)


### Description

bee-interaction-database is a repository for interaction data about bees (Hymenoptera). The observations are from the literature and focused on food, parasites and other interactions of bees in North America.

This GitHub repository was cloned from [globalbioticinteractions/template-dataset](https://github.com/globalbioticinteractions/template-dataset), which includes a blank interactions.tsv, README and globi.json. GloBI requires that the interactions.tsv be called interactions.tsv and for the globi.json file to exist. Some column headers of inteteractions.tsv file was modified from the cloned template, but follow the naming conventions.

### Citation

2020. Biotic species interactions about bees (Anthophila) manually extracted from literature.


### Interaction Types

The biotic species interactions in this dataset were mapped to terms in the Relations Ontology (RO).

interactionTypeName | interactionTypeId
--- | --- |
visits | http://purl.obolibrary.org/obo/RO_0002618
visits flowers of | http://purl.obolibrary.org/obo/RO_0002622

 
### Data Definitions

The definitions of the columns used in the interactions.tsv dataset are described here. If these correspond with Darwin Core they are mapped to those classes. Some of the columns in the template were unused.

  * A **InteractionID** : An non-unique identifier that links two interactions as part of the same observation in the dataset.
  * A **basisOfRecord** [DWC:BasisOfRecord](http://rs.tdwg.org/dwc/terms/basisOfRecord) : The specific nature of the data record. For literature use LiteratureRecord.
  * A **sourceTaxonId** [DWC:scientificNameID](http://rs.tdwg.org/dwc/terms/scientificNameID) : An identifier for the nomenclatural (not taxonomic) details of a scientific name.
  * A **sourceTaxonName** [DWC:scientificName](http://rs.tdwg.org/dwc/terms/scientificName) : The lowest level taxonomic rank that can be determined.
  * A **sourceFamilyName** [DWC:family](http://rs.tdwg.org/dwc/terms/family) : The family name of the source taxon.
  * A **sourceCommonName** [DWC:vernacularName](http://rs.tdwg.org/dwc/terms/Taxon) : A common or vernacular name.
  * A **sourceSexName** [DWC:sex](http://rs.tdwg.org/dwc/terms/sex) : The sex of the biological individual(s) represented in the Occurrence.
  * A **sourceSexID**  : Identifer for the sex name.
  * A **interactionTypeId** : Identifier for the interaction type.
  * A **isNegated** : This field is presently not supported in GloBI. It is intended to relate that a specific interaction was explicitly not observed.
  * A **interactionTypeName** : A interaction type (ex. eats, piercing). The name of the interaction type should be the name as it is listed in the original text, which is not always the name of the term it is mapped to. As long as the definition to the mapping is compatible with the ```interactionTypeName```, it is usable as a ```interactionTypeId```.
  * A **targetBodyPartName**  : The specific name of the target body part. The name of the body part should be the name as it is listed in the original text, which is not always the name of the term it is mapped to. As long as the definition to the mapping is compatible with the ```targetBodyPartName```, it is usable as a ```targetBodyPartId```.
  * A **targetBodyPartId**  : Identifer for the body part name.
  * A **experimentalConditionName**  : ("in nature" - most common)
  * A **experimentalConditionId** : 
  * A **targetTaxonId** [DWC:scientificNameID](http://rs.tdwg.org/dwc/terms/scientificNameID) : An identifier for the nomenclatural (not taxonomic) details of a scientific name.
  * A **targetTaxonName** [DWC:scientificName](http://rs.tdwg.org/dwc/terms/scientificName) : The lowest level taxonomic rank that can be determined.
  * A **targetFamilyName** [DWC:family](http://rs.tdwg.org/dwc/terms/family) : The family name of the source taxon.
  * A **targetCommonName** [DWC:vernacularName](http://rs.tdwg.org/dwc/terms/Taxon) : A common or vernacular name.
  * A **country** [DWC:country](http://rs.tdwg.org/dwc/terms/country) : The name of the country or major administrative unit in which the Location occurs.
  * A **stateProvince** [DWC:stateProvince](http://rs.tdwg.org/dwc/terms/stateProvince) : The name of the next smaller administrative region than country (state, province, canton, department, region, etc.) in which the Location occurs.
  * A **county** [DWC:county](http://rs.tdwg.org/dwc/terms/county) : The full, unabbreviated name of the next smaller administrative region than stateProvince (county, shire, department, etc.) in which the Location occurs.
  * A **verbatimLocality** [DWC:locality](http://rs.tdwg.org/dwc/terms/verbatimLocality) : The specific description of the place. Less specific geographic information can be provided in other geographic terms (higherGeography, continent, country, stateProvince, county, municipality, waterBody, island, islandGroup). This term may contain information modified from the original to correct perceived errors or standardize the description.
  * A **localityId** : Specific identifier for the locality. This field was not populated in this dataset.
  * A **locality** [DWC:locality](http://rs.tdwg.org/dwc/terms/locality) : The specific description of the place. Less specific geographic information can be provided in other geographic terms (higherGeography, continent, country, stateProvince, county, municipality, waterBody, island, islandGroup). This term may contain information modified from the original to correct perceived errors or standardize the description.
  * A **habitat** [DWC:habitat](http://rs.tdwg.org/dwc/terms/habitat) : A category or description of the habitat in which the Event occurred.
  * A **decimalLatitude** [DWC:decimalLatitude](http://rs.tdwg.org/dwc/terms/decimalLatitude) : 	The geographic latitude (in decimal degrees, using the spatial reference system given in geodeticDatum) of the geographic center of a Location. Positive values are north of the Equator, negative values are south of it. Legal values lie between -90 and 90, inclusive.
  * A **decimalLongitude** [DWC:decimalLongitude](http://rs.tdwg.org/dwc/terms/decimalLongitude) : The geographic longitude (in decimal degrees, using the spatial reference system given in geodeticDatum) of the geographic center of a Location. Positive values are east of the Greenwich Meridian, negative values are west of it. Legal values lie between -180 and 180, inclusive.
  * A **minimumElevationInMeters** [DWC:minimumElevationInMeters](http://rs.tdwg.org/dwc/terms/minimumElevationInMeters)
  * A **maximumElevationInMeters** [DWC:maximumElevationInMeters](http://rs.tdwg.org/dwc/terms/maximumElevationInMeters)
  * A **verbatimEventDate** [DWC:eventDate](http://rs.tdwg.org/dwc/terms/verbatimEventDate) : The verbatim original representation of the date and time information for an Event.
  * A **eventDate** [DWC:eventDate](http://rs.tdwg.org/dwc/terms/eventDate) : The date-time or interval during which an Event occurred.
  * A **eventTime** [DWC:eventDate](http://rs.tdwg.org/dwc/terms/eventTime) : The time or interval during which an Event occurred.
  * A **referenceDoi** : This field was not populated in this dataset.
  * A **referenceCitation**  : The reference for the interaction.
  * A **referenceType**  : The type of reference.
  * A **primarySource**  : Is the reference the primary source for the observation (TRUE/FALSE)? If it is not, include the primary source citation in the notes.  
  * A **enteredBy**  : The person entering the data.
  * A **notes**  : Notes about the database entry.


### Included Resources
Literature used in this project is recorded on each record. If you have a new paper to add, please submit a [new github issue](https://github.com/seltmann/bee-interaction-database/issues/new) or add it to the [Bee Interaction Database group](https://www.mendeley.com/community/bee-interaction-database/) on Mendeley.


### Data Issues



### Summary
