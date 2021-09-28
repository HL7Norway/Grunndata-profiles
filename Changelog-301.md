# Changelog for 3.0.1

## Documents the changes implemented from version 3.0.1 to 3.0.1

### Release date: 2021-xx-xx

This is a new release completing the information model according to FREG information. This release adds several new features.

## Files change description

|Date|File|Change description|DevOps|
|-

|2021-04-08|gd-fake-identity.StructureDefinition-extension.xml|Added feature for fake identity in separate extension|Feature 3830|
|2021-04-08|gd-Person|Added fake identity to the gd-Person definition|Feature 3830, PBI 10481|
|2021-06-02|gd-Person|removed active documentation concerning fake-id persons (active not set on fakeid)|Feature 3830, PBI 10481|
|2021-06-02|gd-Person, GdFakeIdentity|Added isModifier=true to GdFakeIdentity to signify the importance of the fake identity information if present|Feature 3830, PBI 10481|
|2021-06-09|gd-Person-Fred-pajord-identity-control.xml|Added example of gd-identity-control use (.NET validert)|PBI 10357|
|2021-06-10|gd-person-sametingelectorrelation.CodeSystem.xml|Fixed validation error||
|2021-06-10|gd-Person|Added fixed value of http://ehelse.no/fhir/CodeSystem/gd-person-identificationnumbertype to Identifier.system on foreign identifier slice definition|validation|
|2021-06-10|gd-address-metadata|Removed errondous source element from constraint in Extension.extension:addressIsUnknown|validation|
|2021-06-11|gd-Person-Nabo-Eksempel-fakeid.xml|Validated example for fake-id use, two errors one-identity invariant and Valueset validation iso3166|Feature 3830|
|2021-06-11|gd-fake-identity.StructureDefinition-extension.xml|Rewrite for validation purpose|Feature 3830|
|2021-06-14|GdPerson|Added identityControl extension|PBI 10357|
|2021-06-14|GdIdentifierStatus|removed "-05" from valueset reference|Bug|
|2021-06-16|FakeIdentityIdentifyingInformationBirthDate|Added hl7 namespace to  definition|Bug|

