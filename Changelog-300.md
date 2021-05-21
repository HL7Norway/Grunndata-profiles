# Changelog for 3.0.0

## Documents the changes implemented from version 2.x.x to 3.0.0

### Release date: 2021-xx-xx

This is a new release completing the information model according to FREG information. This release adds several new features.

## Files change description

|Date|File|Change description|FREG description|
|-
|2021-04-09|gdPerson|Person.active, added: In some special cases where a Person document is nullified because it was registered in error||
|2021-04-09|gdRelatedPerson|RelatedPerson.active, added: In some special cases where a Person document is nullified because it was registered in error||
|2021-04-08|gd-fake-identity.StructureDefinition-extension.xml|Added feature for fake identity in separate extension|Feature 3830|
|2021-04-08|gd-Person|Added fake identity to the gd-Person definition|Feature 3830|PBI 10481|
|2021-04-16|Why use different structure for fregMetadata in different extensions? See gdBirth and gdResidencepermit?||
|2021-04-16|gd-identitycontrolstatus.ValueSet.xml||PBI 10357|
|2021-04-16|gd-identitycontrolstatus.CodeSystem.xml||PBI 10357|
|2021-04-16|gd-identity-control.StructureDefinition-extension.xml||PBI 10357|
