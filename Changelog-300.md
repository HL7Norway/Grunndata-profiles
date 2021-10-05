# Changelog for 3.0.0

## Documents the changes implemented from version 2.3.5 to 3.0.0

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
|2021-04-16|gd-identity-control.StructureDefinition-extension.xml|Added|PBI 10357|
|2021-05-31|gdPerson|bugfix of Person.meta.security:addressConfidentiality.system, added fixed uri for system|BUG 11440|
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
|2021-06-18|gd-Person-Fred-pajord-residue-contact.xml|Added example (validated Java)|PBI 10358|
|2021-06-18|gd-Person-Fred-pajord-residue-contact.xml|Added containing contact-person (validates .NET, don't validate in Java,)|PBI 10358|
|2021-06-22|GdPerson|Validation error|BUG 24365|
|2021-06-22|GdCodingSecurity.StructureDefinition-profile.xml|New security profiel for adressebeskyttelse|
|2021-06-22|GdCodingSecurity|Validation error|BUG 24365|
|2021-06-22|GdFregMetadata|Added Coding Context of extension|BUG 24365|
|2021-06-22|gd-Person-Nabo-Eksempel-adressebeskyttelse-klientadresse.xml|Updated addressConfidentiality coding to working code value|BUG 24365|
|2021-06-23|GdCodingSecurity|File rename for consistency|BUG 24365|
|2021-06-23|GdPersonSamiLanguageCodeSystem|Added codesystem containing codes from SamiskSpraakType|PBI 10363|
|2021-06-23|GdPersonSamiLanguageValueSet|Added valueset containing codes from SamiskSpraakType|PBI 10363|
|2021-06-23|GdSamiLanguage|Added extension for samilanguage|PBI 10363|
|2021-06-23|GdPersonSametingElectorRelationCodeSystem|Rename|name consistency|
|2021-06-23|GdPersonSametingElectorRelationValueSet|Rename|name consistency|
|2021-06-23|GdPersonCitizenshipRetention|Added extension for bibehold|PBI 10359|
|2021-06-30|GdPerson|Added extension for bibehold to GdPerson|PBI 10359|
|2021-06-30|GdPersonCitizenshipRetentionCodeSystem|Added codesystem for bibehold|PBI 10359|
|2021-06-30|GdPersonCitizenshipRetentionValueSet|Added valueset for bibehold|PBI 10359|
|2021-06-30|GdPerson|Added extension for samilanguage to GdPerson|PBI 10363|
|2021-06-30|gd-Person-Fred-pajord-sami-language.xml|Added samiLanguage example (Validated .NET)|PBI 10363|
|2021-07-02|Documentation|Updated diagrams for documentation|Feature 3830|
|2021-07-02|GdPersonCitizenshipRetention|Bugfix mapping and missing datoForBibehold element, changed norwegian element name to englishbibeholdStatus|Bugfix|
|2021-07-02|GdPerson|Fixed wrong cardinality of citizenshipRetention|Bugfix|
|2021-09-14|gd-municipalitycoded.StructureDefinition.xml|New extension to incorporate coded values for Norwegian county's (kommunenummer)|PBI 6787|
|2021-09-14|gd-Address.StructureDefinition-profile.xml|Include extension:propertyInformation, updated documentation for kommunenummer|PBI 6787|
|2021-09-14|gd-Address-street.StructureDefinition-profile.xml|Documentation changes, Change must-support for propertyinformation.extension, added must support for Address.district, removed address.city|PBI 6787|
|2021-09-14|gd-Address-unknown.StructureDefinition-profile.xml|Documentation changes, Change must-support for propertyinformation.extension, added must support for Address.district|PBI 6787|
|2021-09-14|gd-Address-cadastral.StructureDefinition-profile.xml|Removed alias element, added definition element.|PBI 6787|
|2021-09-14|gd-person-sametingelectorrelation.codesystem|Added new code aldriInnmeldt|PBI 27915|
|2021-10-04|gd-AddressContentType.SearchParameter.xml|Clean up unused elements|
|2021-10-04|gd-AddressType.SearchParameter.xml|Clean up unused elements|
|2021-10-04|gd-AddressDistrictExtension-Municipality.SearchParameter.xml|New search paramter on municipality|
|2021-10-04|gd-AddressLine-BuildingNumberSuffix.SearchParameter.xml|New search paramter on building number suffix|
|2021-10-04|gd-AddressLine-HouseNumber.SearchParameter.xml|New search paramter on house number numeric|
|2021-10-04|gd-AddressLine-StreetName.SearchParameter.xml|New search paramter on streetname|
|2021-10-05|gd-HumanName.StructureDefinition-profile.xml|Added humanName.extension, changed must-support on middlename, removed min value and definition on HumanName.extension:fregMetadata|
|2021-10-05|gd-family-relation.StructureDefinition-extension.xml|Removed extensions elements.|
|2021-10-05|gd-guardianship.StructureDefinition-extension.xml|Removed min value because of skatt|
