# Changelog for 3.0.0

## Documents the changes implemented from version 2.x.x to 3.0.0

### Release date: 2021-xx-xx

This is a new release completing the information model according to FREG information. This release adds several new features.

## Files change description

|Date|File|Change description|DevOps|
|-
|2021-04-09|gdPerson|Person.active, added: In some special cases where a Person document is nullified because it was registered in error||
|2021-04-09|gdRelatedPerson|RelatedPerson.active, added: In some special cases where a Person document is nullified because it was registered in error||
|2021-04-08|gd-fake-identity.StructureDefinition-extension.xml|Added feature for fake identity in separate extension|Feature 3830|
|2021-04-08|gd-Person|Added fake identity to the gd-Person definition|Feature 3830, PBI 10481|
|2021-04-16|Why use different structure for fregMetadata in different extensions? See gdBirth and gdResidencepermit?||
|2021-04-16|gd-identitycontrolstatus.ValueSet.xml||PBI 10357|
|2021-04-16|gd-identitycontrolstatus.CodeSystem.xml||PBI 10357|
|2021-04-16|gd-identity-control.StructureDefinition-extension.xml||PBI 10357|
|2021-05-31|GdPerson|bugfix of Person.meta.security:addressConfidentiality.system, added fixed uri for system|BUG 11440|
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
|2021-06-16|gd-Person-Fred-pajord-identity-control.xml|.NET validert både positivt (riktig kode) og negativt (feil kode) (JAVA validerer ikke)|PBI 10357|
|2021-06-16|gdIdentityDocument|Added extension for idenity document information from FREG|PBI 10361|
|2021-06-16|gd-Person-Fred-pajord-identity-document.xml|Added example person with idenity document extension (Validert mot profil .NET)|PBI 10361|
|2021-06-16|Design decision for contact information deceased|Add the contact address as a no-basis-address|PBI 10358|
|2021-06-17|GdResidueContact|Added (validated)|PBI 10358|
|2021-06-17|GdContactLawyer|Added (validated), added documentation of elements|PBI 10358|
|2021-06-17|GdContactPerson|Added (validated)|PBI 10358|
|2021-06-17|GdContactOrganization|Added (validated)|PBI 10358|
|2021-06-17|Updated all Conformance resources to FHIR 4.0.1|Validated Java 0 errors|Feature 6323|
|2021-06-18|GdResidueContact|Updated documentation of all new extensions|PBI 10358|
|2021-06-18|gd-person-formoftransfer.ValueSet.xml|New Valueset|PBI 10358|
|2021-06-18|gd-person-formoftransfer.CodeSystem.xml|New CodeSystem|PBI 10358|
|2021-06-18|GdPerson|Added residueContact element|PBI 10358|

Ser ut til å være utfordring med snapshot generering av profiler på profiler (profiler utledet fra no-basis) når kildekoden genereres av Forge for de utlede profilene.

* Fremdeles ingen løsning på his element does not match any known slice defined in the profile http://ehelse.no/fhir/StructureDefinition/gd-person-status (information)
