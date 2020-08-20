# Changelog for x.x.x

## Documents the changes implemented from version 2.3.0 to x.x.x
### Release date: 2020-xx-xx

This is a release to change the FHIR information model to better reflect the content from sources according to the HL7 FHIR standard. Some breaking changes from the 2.3.0 version is provided:
- Change the way municipality (kommunenummer) is handled in the model


## Files change description
|File|Change description|Dev-ops id|
|-
|gd-municipalitycoded.StructureDefinition.xml|New extension to incorporate coded values for Norwegian county's (kommunenummer)||
|gd-Address.StructureDefinition-profile.xml|Include the municipalitycoded extension, updated documentation for kommunenummer||
|gd-Address-street.StructureDefinition-profile.xml|Change must-support for district and propertyinformation.extension||
