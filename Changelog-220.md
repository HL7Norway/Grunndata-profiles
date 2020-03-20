#Changelog for 2.2.0
## Documents the changes implemented from version 2.1.0 to 2.2.0
### Release date: 2020-03-20

This is a service release to includes changes to the documentation based on feedback on the 2.1.0 version. No breaking changes in the capabilities are documented in this version, but several updated to extend the capabilites described in the CapabilityStatement.
- Added search parameter support for several search parameters in the CapabilityStatement
- Added SearchParameter definitions for AddressContentType and AddressType
- Updated CapabilityStatement to include several new search parameters
- Major update to the documentation of RelatedPerson to clarify how this Resource is used to code FREG data
- Updates to the "Readers Guide" to clarify the use of POST transaction and the meaning of must-support flags in this ImplementationGuide
- Some minor documentation changes in the gd-Person StructureDefinition updates to clearify the documentation concerning birtDate and foreignIdentifier
- gd-birth-in-norway bugfix, added freg-metadata to extension
- gd-person-citizenship Change the name of the codesytem/valueset, updated to documentation


## Files change description
|File|Change description|
|-
|StructureDefinition/gd-birth-in-norway.StructureDefinition-extension.xml|Added freg-metadata to the extension to hold metadata from freg about this content|
|CapabilityStatement/gd-Server-Requirements.xml|Several updates and bugfixes|
|SearchParameter/gd-AddressType.SearchParameter.xml|New File|
|SearchParameter/gd-AddressType.SearchParameter.xml|New File|
|StructureDefinition/gd-deceased.StructureDefinition-extension.xml|Added gd-RelatedPerson context|
|StructureDefinition/gd-person-status.StructureDefinition-extension.xml|Added gd-RelatedPerson context|
|StructureDefinition/gd-Person.StructureDefinition-profile.xml|Gd-Person update of the documentation based on feedback from consumers: Updated Foreign identifier documentation. Updated information about the birtDate and birthYear that will coexist in information from FREG.|
|gd-RelatedPerson.StructureDefinition-profile.xml|Documentation changes|
|gd-guardianship.StructureDefinition-extension.xml|Documentation changes|
|StructureDefinition/gd-parental.StructureDefinition-extension.xml|Documentation changes|
|StructureDefinition/gd-person-citizenship.structuredefinition-extension.xml|Documentatio changes to clearify the use of the gd-person-citizenship.structuredefinition-extension structure; only period.start is set, code and system is used to represent the actual citizenship|
|CodeSystem/gd-person-citizenshipextension.CodeSystem.xml|File name change, removed version number in url and filenames|
|ValueSet/gd-person-citizenship.ValueSet.xml|File name change, removed version number in url and filenames|
|ValueSet/gd-person-gender.ValueSet.xml|New file defining valueset for gender to reflect male/female values used by FREG for administrative gender|
|StructureDefinition/gd-Person.StructureDefinition-profile.xml|Changed reference to gender valueset ValueSet/gd-person-gender.ValueSet.xml|
|odeSystem/gd-person-migration-pattern.CodeSystem.xml






# Changelog for 2.1.0
## Changes implemented from version 2.0.6 to 2.1.0
### Release date: 2019-12-19

The update includes changes for:
- Using all address-types in gd-Person
- Representing unknown bostedsadresse and kontaktadresse from FREG
- Include original event codes from FREG in gd-Provenance
- Added extension to represent information regarding preferred address
- Updated examples, images and documentation to represent changes in the definition

## Files change description

|File|Change description|
|-
|CodeSystem/gd-address-contenttype-v210|Updated codesystem to include types for "UkjentBosted" and "AdressenErUkjent"|
|CodeSystem/gd-address-physicaladdresstype-v201|Updated version information|
|CodeSystem/gd-provenance-freg-hendelsestype-v210.CodeSystem.xml|New codesystem to include all event types from FREG|
|StructureDefinition/gd-Address-box.StructureDefinition-profile.xml|Updated with must support information|
|StructureDefinition/gd-Address-cadastral.StructureDefinition-profile.xml|Removed Snapshot|
|StructureDefinition/gd-Address-freeform.StructureDefinition-profile.xml|Documentation changes, include preferred-address extension |
|StructureDefinition/gd-Address-international.StructureDefinition-profile.xml|Included must-support information|
|StructureDefinition/gd-Address-street.StructureDefinition-profile.xml|Included must support information|
|StructureDefinition/gd-Address-unknown.StructureDefinition-profile.xml|New profile for unknown addresses|
|StructureDefinition/gd-Address.StructureDefinition-profile.xml|fixedUri -> fixedString|
|StructureDefinition/gd-Person.StructureDefinition-profile.xml|Added all possible addresstypes: cadastral, international, street, box, freeform and unknown|
|StructureDefinition/gd-Provenance.StructureDefinition-profile.xml|Added reason code from FREG to the profile|
|StructureDefinition/gd-address-metadata.StructureDefinition-extension.xml|Added cadastralIdentifier and addressIsUnknown elements, documentation changes|
|StructureDefinition/gd-preferred-address.StructureDefinition-extension.xml|New extension for preferred address information|
|ValueSet/gd-address-contenttype-v210.ValueSet.xml|updated the ValueSet to use the updated CodeSystem|
|ValueSet/gd-address-preferredaddresstype-v210.ValueSet.xml|New ValueSet to define possible adresstypes for preferred address|
|ValueSet/gd-provenance-freg-hendelsestype-v210.ValueSet.xml|ValueSet for the new FREG hendelsestype CodeSystem|
|examples|New and updated examples to reflect the changes in the definition|
|images/Hendelse Filter.png|New image to document Filter use-case|
|images/gd-Address.png|Updated documentation of the gd-Address definitions|
|images/gd-Person.png|Updated documentation of the gd-Person definitions|
|images/gd-Provenance.png|Updated documentation of the gd-Provenance defintions|
|ImplementationGuide/Address-documentation.md|Added better documentation about address types and address content types|

## Documentation changes after 2.1.0 release
|Date|File|Change description|
|-
|2020-01-06|CapabilityStatement/gd-Person-Server-Requirements.xml|Updated identifier searches to use POST transaction|
|2020-01-06|Implementation guide text|Readers guide: Updated description of read and search by RESTful FHIR API using POST transaction|
|2020-02-28|Implementation guide text|Readers guide: Updated description of must support in the Readers Guide. Added description of must-support="false" and not-set|