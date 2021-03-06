# Changelog for 2.3.5

## Documents the changes implemented from version 2.3.4 to 2.3.5

### Release date: 2021-02-02

This is a bugfix release to fix bugs introdused by Skatteetaten in in FREG information model v3.0. This release is according to v3.1 of FREG information model released 2021-01-25.

## Files change description

|Date|File|Change description|FREG description|
|-
|2021-02-02|gd-guardianship.StructureDefinition-extension.xml|omfangetErInnenPersonligOmråde er påkrevd - changed cardinality for personalScope|PBI 7291|
|2021-02-02|gd-address-metadata.StructureDefinition-extension.xml|klientadresseOgFortrolig removed the description of klientadresseOgFortrolig|PBI 7291|

## Documentation changes after the 2.3.5 release

|Date|File|Change description|
|-
|2021-02-17|gd-Person-Server-Requirements.xml|Added description of the total parameter default value|PBI 6621|
|2021-02-17|gd-Person-Server-Requirements-v300.xml|Added description of the total parameter default value|PBI 6621|
|2021-02-17|gd-Person-Server-Requirements-v300.xml|Corrected validation errors for CapabilityStatement (duplicate searchParams)||
|2021-02-17|Documentation changes|Added description of total and element parameter to the IG FAQ|PBI 6621|
|2021-03-11|gd-RelatedPerson.StructureDefinition-profile.xml documentation changes|Removed documentation of logical reference in RelatedPerson.patient reference|PBI 8563|
|2021-03-11|gd-RelatedPerson.StructureDefinition-profile.xml|Removed must-support from RelatedPerson.patient.identifier element|PBI 8563|
|2021-03-11|ImplementationGuide update|Changed the documentation for RelatedPerson search, removed info on search by RelatedPerson.patient.identifier|PBI 8563|

# Changelog for 2.3.4

## Documents the changes implemented from version 2.3.3 to 2.3.4

### Release date: 2021-01-19

This is a service release to update the FHIR model according to the new FREG v3.0/2.0 information model released 2021-01-03

## Files change description

|Date|File|Change description|FREG description|
|-
|2021-01-20|gd-additional-humanname.StructureDefinition-extension.xml|Update description originalName according to FREG||
|2021-01-20|gd-migration.StructureDefinition-extension.xml|Update definition|Litt tillegg i Utflytting ifm passivitetsvedtak.|
|2021-01-20|gd-birth.StructureDefinition-extension.xml|gdBirth, added definition of birthYear, updated placeOfBirth, landOfBirth, placeOfBirthDistrict||
|2021-01-20|gd-birth-in-norway.StructureDefinition-extension.xml|updated definition multipleBirthInteger|5.3 Noen endringer ifm f.eks. fødssel i Norge|
|2021-01-20|gd-Person.StructureDefinition-profile.xml|Added FREG definition to GdPerson.name|5.4 Punktum er nå lovlig tegn i navn|
|2021-01-20|gd-migration.StructureDefinition-extension.xml|handled by new element migrationDate|innflyttingsdato finnes ikke i XSD eller informasjonsmodell 5.18 Innflytting har fått ny egenskap, innflyttingsdato|
|2021-01-20|gd-migration.StructureDefinition-extension.xml|Added migrationDate to GdMigration-extension|5.19 Utflytting har fått ny egenskap, utflyttingsdato|
|2021-01-20|gd-person-identifier-status.StructureDefinition-extension.xml changed definition|5.2.4 Endret definisjon for identifikatortype|
|2021-01-20|gd-Person.StructureDefinition-profile.xml|update birthDate definition|5.3 Endret definisjon for fødselsdato|
|2021-01-20|gd-Person.StructureDefinition-profile.xml|GdPerson updated meta.addressConfidentiality slice definition|5.10 Endret definisjon for adressebeskyttelse|
|2021-01-20|gd-marital-status.StructureDefinition-extension.xml|Updated locationName definition|5.6 Endret definisjon for sted (stedsnavn)|
|2021-01-20|gd-address-metadata.StructureDefinition-extension.xml|updated description NB! koden eksisterer ikke i FREG xsd, har ikke oppdatert kodeverket eller valueset med den nye koden koden.|5.9.1 og flere innen adresse. Beskrivelse av klientadresseOgFortrolig|
|2021-01-20|gd-Identifier-foreign.StructureDefinition-profile.xml|updated definitions|5.12 Endret definisjon for utlendingsmyndighetenesIdentifikasjonsnummer|
|2021-01-20|gd-guardianship.StructureDefinition-extension.xml|updated definitions NB ny kode eksisterer ikke i FREG xsd, har ikke oppdatert kodeverket eller valueset med den nye koden.|5.20 Endret definisjon for representant for enslig mindreårig asylsøker. Nytt kodeinnslag: annenType for skjult informasjon|
|2021-01-20|gd-residence-permit.StructureDefinition-extension.xml|Updated definition GdResidencePermit.residencePermitType|5.21 Endret definisjon for oppholdstillatelse. Opphold registreres på personer med enten fødselsnummer og d-nummer|
|2021-01-20|gd-residence-permit.StructureDefinition-extension.xml|Se over|5.20 Endret definisjon for representant for enslig mindreårig asylsøker|
|2021-01-20|gd-Address-box.StructureDefinition-profile.xml|Updated GdAddressBox.line.postBox definition|5.25.5 Beskrevet postboks med postboksanleggets navn|
|2021-01-20|gd-birth.StructureDefinition-extension.xml|birthPlace|Dokumentasjon: Endring av beskrivelsen av fødested.|
|2021-01-20|gd-residence-permit.StructureDefinition-extension.xml|Changed definition|Dokumentasjon: Endring av beskrivelse av begrepet/entiteten Opphold.|
|2021-01-20|gd-residence-permit.StructureDefinition-extension.xml||Se over: Endring i beskrivelse av "opphold"|
|2021-01-20|gd-guardianship.StructureDefinition-extension.xml|Already added, added mapping information|Dokumentasjon (gjort før): Endring av VergeEllerFremtidsfullmakt til VergemålEllerFremtidsfullmakt.|
|2021-01-20|gd-guardianship.StructureDefinition-extension.xml|Added element personalScope| La til element: Nytt flagg i sistnevntes vergeinformasjon: omfangetErInnenPersonligOmråde| 
|2021-01-20|gd-Address.StructureDefinition-profile.xml|Updated definition of parishId|Tilleggsinformasjon om kretstyper.|
|2021-01-20|gd-Address-street.StructureDefinition-profile.xml|Corrected writing error in mapping definition adresssenummer.husnummer-> adressenummer.husnummer||
|2021-01-21|gd-Person.png and gd-RelatedPerson.png|Updated images according to FHIR model changes|Nye elementer nevnt over|

# Changelog for 2.3.3

## Documents the changes implemented from version 2.3.2 to 2.3.3

### Release date: 2020-12-22

This is a service release publish a new package including the changes to the active element and urbandistrict information.

## Files change description

|Date|File|Change description|
|-
||Changes to the active element|From the last release|PBI 5091|
|2020-12-18|gd-Address.StructureDefinition-profile.xml|Added mapping to FREG (n/a) and shortname "bydelsnummer" to code|PBI 6786|
|2020-12-18|gd-Address-cadastral.StructureDefinition-profile.xml|Added missing must support information|PBI 6786|
|2020-12-18|gd-Address-street.StructureDefinition-profile.xml|Added missing must support information|PBI 6786|
|2020-12-21|HL7 FHIR extensions copies|Removed the copy of adxp extensions, patient citizenship and patient nathionality from Grunndata-R4 as the definition is part of HL7 FHIR standard|N/A|

## Documentation changes after the 2.3.3 release

|Date|File|Change description|
|-
|2021-01-08|gd-Person-Server-Requirements.xml|Change of the documentation element for better mardown rendering||

## Documents the changes implemented from version 2.3.1 to 2.3.2

### Release date: 2020-09-30

This is a service release to fix bugs in codesystem bindings and update documentation

## Files change description

|Date|File|Change description|
|-
|2020-09-23|gd-person-status.StructureDefinition-extension.xml|Bugfix of the valueset binding removed incorrect binding to http://ehelse.no/fhir/ValueSet/gd-person-status-v05||
|2020-09-24|gd-Address-street.StructureDefinition-profile.xml|Bugfix to documentation, added kommunenummer mapping information, won't affect the package||
|2020-09-24|gd-Person.StructureDefinition-profile.xml|Bugfix to the meta.security.addressConfidentiality element removed the valueset fixed value of system||
|2020-09-30|gd-person-identificationnumbertype.CodeSystem.xml|Updated the codesystem name according to naming conventions||

## Documentation changes after the release

|Date|File|Change description|
|-
|2020-10-06|gd-Person-Nabo-Eksempel-klientadresse.xml|Endret eksempel for å inkludere klientadresse i metainformasjon||
|2020-10-06|gd-Identifier-foreign.StructureDefinition-profile.xml|Oppdaterte type.coding.system til binding til CodeSystem||
|2020-10-14|examples/gd-Person-04021950128-version-3.xml|Endret eksempel for å tydeliggjøre bruk av line extensions||
|2020-11-13|gd-RelatedPerson.StructureDefinition-profile.xml|Oppdaterte informasjonen for å klargjøre bruk av identifikator||
|2020-11-17|Documentation changes|Oppdaterte informasjon om Must support på Readers guide, lagring er SHOULD, avhenger av konsumentens behov||
|2020-11-17|Documentation changes|Oppdaterte informasjon om MANDATORY elements adressebeskyttelse|Feature 3372|
|2020-11-19|Documentation changes|Updated information on the GdPerson to include information about persons related to the kingdom of Norway in addition to citizens||
|2020-12-04|gd-Person.StructureDefinition-profile.xml|Added must support to the active element, updated active documentation|PBI 5091|
|2020-12-04|gd-RelatedPerson.StructureDefinition-profile.xml|Added must support to the active element, updated active documentation|PBI 5091|

# Changelog for 2.3.1

## Documents the changes implemented from version 2.3.0 to 2.3.1

### Release date: 2020-09-18

This is a service release to fix SearchParameters to work on Vonk server

## Files change description

|File|Change description|Dev-ops id|
|- 
|gd-Address-type.SearchParameter|Updated expression with '.value' to work on Vonk server|Task 4343|
|gd-Address-contenttype.SearchParameter|Updated expression with '.value' to work on Vonk server|Task  4343|
|gd-Address.StructureDefinition-profile.xml|Described the mapping from FREG flyttedato, bostedsadressedato, startdatoForKontrakt and sluttdatoForKontrakt into the Address.Period element|Bug 4545|
|gd-Address-cadastral.StructureDefinition-profile|Added must support to the Period.element for the relevant profiles|Bug 4545|
|gd-Address-international.StructureDefinition-profile.xml|Added must support to the Period.element for the relevant profiles|Bug 4545|
|gd-Address-street.StructureDefinition-profile.xml|Added must support to the Period.element for the relevant profiles|Bug 4545|
|gd-Address-unknown.StructureDefinition-profile.xml|Added must support to the Period.element for the relevant profiles|Bug 4545|
|gd-Provenance.StructureDefinition-profile.xml|Cleanup in the XML||
|gd-birth-in-norway.StructureDefinition-extension.xml|Cleanup in the XML||
|Several files|Removed some snapshot with errors generated by Forge||
|gd-Person-Server-Requirements.xml and gd-Person-Server-Requirements-v300.xml|Corrected the birthdate search parameter birthDate -> birthdate||
|gd-Person-Fred-pajord.xml|Updatedet the example with birthDate||

# Changelog for 2.3.0

## Documents the changes implemented from version 2.2.0 to 2.3.0

### Release date: 2020-06-09

This is a service release to fix ValueSet and CodeSystem resource version numbering in filenames, id's an URL's, and removal of CodeSystem definitions not used in the specification.

## Files change description

|File|Change description|Dev-ops id|
|-
|gd-person-identifierstatus.ValueSet.xml|Rename file, remove version in id, filename and url|PBI 2981|
|gd-person-identifierstatus.CodeSystem.xml|Rename file, remove version in id, filename and url, changed code "opphørt" to "opphoert" like the actual data from FREG|PBI 2981|
|StructureDefinition\gd-person-identifier-status.StructureDefinition-extension.xml|changed valueset to http://ehelse.no/fhir/ValueSet/gd-person-identifierstatus |PBI 2981|
|gd-person-status.ValueSet.xml|Rename file, remove version in id, filename and url|PBI 2981|
|gd-person-status.CodeSystem.xml|Rename file, remove version in id, filename and url|PBI 2981|
|StructureDefinition\gd-person-status.StructureDefinition-extension.xml|changed valueset to http://ehelse.no/fhir/ValueSet/gd-person-status |PBI 2981|
|New file gd-person-probatetype.ValueSet.xml|New ValueSet to include codes from probatetype codesystem|PBI 2981|
|Rename gd-person-probateform-v05.CodeSystem.xml -> gd-person-probatetype.CodeSystem.xml | Changed the name into something meaningfull, removed version info in filenames and id's|PBI 2981|
|gd-person-gender.ValueSet.xml|Updated the documentation for the ValueSet|PBI 2981|
|Removed file: gd-person-addresstypeclassification-v05.codesystem.xml| This is a duplicate, the system defined is not in use http://ehelse.no/fhir/CodeSystem/gd-person-addresstypeclassification-v05.codesystem |PBI 2981|
|Rename gd-address-preferredaddresstype-v210.ValueSet -> gd-address-preferredaddresstype.ValueSet|removed version info in filenames and id's|PBI 2981|
|Removed gd-person-addresstype-v05.CodeSystem.xml|Not used by any extensions, StructureDefinition or ValueSet, gd-preferredaddrestype is used|PBI 2981|
|Rename gd-address-type-v201.CodeSystem.xml -> gd-address-type.CodeSystem.xml|removed version info in filenames and id's|PBI 2981|
|gd-address-type.CodeSystem.xml|Changed code KontaktadresseUtlandet -> KontaktadresseIUtlandet|PBI 2981|
|Rename gd-address-type-v201.ValueSet.xml -> gd-address-type.ValueSet.xml|removed version info in filenames and id's|PBI 2981|
|Rename gd-person-guardianscope-v05.CodeSystem.xml -> gd-person-guardianscope.CodeSystem.xml|removed version info in filenames and id's|PBI 2981|
|Rename gd-person-guardianscope-v05.ValueSet.xml -> gd-person-guardianscope.ValueSet.xml|removed version info in filenames and id's|PBI 2981|
|Rename gd-person-guardiantype-v05.CodeSystem.xml -> gd-person-guardiantype.CodeSystem.xml|removed version info in filenames and id's|PBI 2981|
|Rename gd-person-guardiantype-v05.ValueSet.xml -> gd-person-guardiantype.ValueSet.xml|removed version info in filenames and id's|PBI 2981|
|gd-person-RelatedPerson.StructureDefinition-profile.xml|Replaced http://ehelse.no/fhir/ValueSet/gd-person-guardiantype-05 with http://ehelse.no/fhir/ValueSet/gd-person-guardiantype |PBI 2981|
|Examples| replaced the use of guardiantype codesystem url to http://ehelse.no/fhir/Codesystem/gd-person-guardiantype |PBI 2981|
|New file gd-person-retaincitizenship.ValueSet.xml|Definition of Bibehold ValueSet|PBI 2981|
|New file gd-person-retaincitizenship.CodeSystem.xml|Definition of Bibehold CodeSystem|PBI 2981|
|Rename gd-person-residencepermittype-v05.valueset.xml -> gd-person-residencepermittype.valueset.xml|removed version info in filenames and id's|PBI 2981|
|Rename gd-person-residencepermittype-v05.codesystem.xml -> gd-person-residencepermittype.codesystem.xml|removed version info in filenames and id's|PBI 2981|
|gd-residence-permit.StructureDefinition-extension.xml|removed version info in valueset reference to residencepermittype|PBI 2981|
|gd-address-physicaladdresstype-v201.CodeSystem.xml|Changed militær -> militaer and påSvalbard -> paaSvalbard|PBI 2981|
|gd-address-physicaladdresstype-v201.CodeSystem.xml -> gd-address-physicaladdresstype.CodeSystem.xml|removed version info in filenames and id's|PBI 2981|
|gd-address-physicaladdresstype-v201.xml -> gd-address-physicaladdresstype.ValueSet.xml|removed version info in filenames and id's|PBI 2981|
|C:\GitRepo\Grunndata-R4\StructureDefinition\gd-address-metadata.StructureDefinition-extension.xml|removed version info in valueset reference for physicaladdresstype|PBI 2981|
|Removed file gd-person-familyrelation-v05.CodeSystem.xml|The CodeSystem in no-basis should be used|BUG 3141|
|Removed file gd-address-postaltype-v01.CodeSystem.xml|The codesystem have never been used|PBI 2981|
|Removed file gd-person-addresstypecategory-v05.CodeSystem.xml|The Codesystem have never been used|PBI 2981|
|Removed file gd-person-addresstypesensitivity-v05.CodeSystem.xml|Codesystem not in use (http://ehelse.no/fhir/CodeSystem/gd-address-confidentiality-v201 is used|PBI 2981|
|Rename gd-person-documentcontrollstatus-v05.CodeSystem.xml -> gd-person-documentcontrolstatus.CodeSystem.xml|New url without version and removed "ll", ValueSet not defined yet|PBI 2981|
|Removed gd-person-identificationdocumenttype-v05.CodeSystem.xml|identifikasjonsdokumenttype is not defined as a codesystem by Skatteetaten in their XML-schema|PBI 2981|
|Rename file gd-person-identityresasonstatus-v05.CodeSystem.xml -> gd-person-identityresasonstatus.CodeSystem.xml|New id and url without version number, ValueSet not defined yet|PBI 2981|
|Removed file gd-person-identityresasonunique-v05.CodeSystem.xml|CodeSystem not defined by FREG|PBI 2981|
|Removed file gd-person-maritalstatusauthorities-v05.CodeSystem.xml|CodeSystem not defined by FREG for Sivilstand.myndighet|PBI 2981|
|Rename file gd-person-registerchangesstatus-v05.CodeSystem.xml -> gd-provenance-freg-entitychangetype.CodeSystem.xml|Removed version info in id's and urls|PBI 2981|
|New file gd-provenance-freg-entitychangetype.ValueSet.xml|include all codes from gd-provenance-freg-entitychangetype codesystem|PBI 2981|
|New file gd-person-sametingelectorrelation.ValueSet.xml|Definition of forholdTilSametingetsValgmanntallValueSet|PBI 2981|
|New file gd-person-sametingelectorrelation.CodeSystem.xml|Definition of forholdTilSametingetsValgmanntallCodeSystem|PBI 2981|
|Rename gd-provenance-freg-hendelsestype-v210.ValueSet.xml -> gd-provenance-freg-eventtype.ValueSet.xml|Removed version info in id's and urls|PBI 2981|
|Rename gd-provenance-freg-hendelsestype-v210.CodeSystem.xml -> gd-provenance-freg-eventtype.CodeSystem.xml|Removed version info in id's and urls|PBI 2981|
|New code in gd-provenance-freg-eventtype.CodeSystem.xml|endringIVergemaal added from XSD from Skatteetaten|PBI 2981|
|Description in gd-address-preferredaddresstype.ValueSet.xml|Clarify the valueset is for choice of preferred address type|PBI 2981|
|Rename file gd-address-contenttype-v210.CodeSystem.xml -> gd-address-contenttype.CodeSystem.xml|Removed version info in id's and urls|PBI 2981|
|Rename file gd-address-contenttype-v210.ValueSet.xml -> gd-address-contenttype.ValueSet.xml|Removed version info in id's and urls|PBI 2981|
|gd-address-metadata.StructureDefinition-extension.xml|Changed the url used to reference gd-address-contenttype.Valueset, removed id in url|PBI 2981|
|Rename gd-address-confidentiality-v201.ValueSet.xml -> gd-address-confidentiality.ValueSet.xml|Removed version info in id's and urls|PBI 2981|
|Rename gd-address-confidentiality-v201.CodeSystem.xml -> gd-address-confidentiality.CodeSystem.xml|Removed version info in id's and urls|PBI 2981|
|New file gd-person-addressprotection.ValueSet.xml|Added Valueset for addressprotection gd-person-addressprotection.ValueSet.xml|PBI 2981|
|gd-Person.StructureDefinition-profile.xml|Changed valueset for meta.security slice to use gd-person-addressproctition.ValueSet|PBI 2981|
|gd-address-metadata.StructureDefinition-extension.xml|Changed the use of correct url for gd-address-confidentiality.ValueSet|PBI 2981|
|New file gd-person-documentcontrolstatus.ValueSet.xml|include all codes from gd-person-documentcontrolstatus codesystem|PBI 2981|
|New file gd-person-identityresasonstatus.ValueSet.xml|include all codes from gd-person-identityresasonstatus codesystem|PBI 2981|
|gd-provenance-freg-entitychangetype.CodeSystem.xml|Removed ".codesystem" from url value|PBI 2981|
|gd-person-identityresasonstatus.CodeSystem.xml|Removed ".codesystem" from url value|PBI 2981|
|gd-address-contenttype.CodeSystem.xml and gd-address-metadta.StructureDefinition-extension.xml|Fixed the CodeSystem value for InternasjonalAdresseIFrittFormat -> InternasjonalAdresseIIFrittFormat|PBI 2981, BUG 2610|
|gd-address-preferredaddresstype.ValueSet.xml|Fixed the KontaktadresseUtlandet -> KontaktadresseIUtlandet|PBI 2981|
|gd-person-citizenship.ValueSet.xml|Fixed the reference to http://ehelse.no/fhir/CodeSystem/gd-person-citizenshipextension |PBI 2981|
|gd-Identifier-foreign.StructureDefinition-profile.xml|Updated description of the profile|NA|
|gd-Identifier-freg.StructureDefinition-profile.xml|Updated description of the profile|NA|
|gd-Person.StructureDefinition-profile.xml|Updated description of the profile|NA|
|gd-preferred-address.StructureDefinition-extension.xml|Updated description of the extension|NA|
|gd-Provenance.StructureDefinition-profile.xml|Updated description of the profile|NA|

### Documentation changes after 2.3.0 release

|Date|File|Change description|
|-
|2020-06-17|Implementation Guide text|Updated the Provenance REST interactions description|
|2020-06-29|Implementation Guide text|Updated the Service Interface page, as well as the Readers guide and Person REST interactions to clarify search functionality available|
|2020-08-13|Implementation Guide text|Updated the "use cases" chapter with text to describe the use cases|
|2020-08-13|Implementation Guide text|Changed the ordring of text on the intro page of the guide|
|2020-08-13|Implementation Guide image|Updated the color scheme of Figure 1: Distribution platform for Core Data| 
|2020-08-13|CapabilityStatement/gd-Server-Requirements|Minor change in the wording in the documentation "The operation "MUST" be added"| 
|2020-08-13|Implementation Guide text|Updated Service Interface/History of a Resource with new wording|
|2020-09-03|Implementation Guide text|Introduction and Provenance REST interaction with new wording|
|2020-09-09|Several files|Fix some discripancies in mapping information regarding mapping to FREG. This version clarifies all mapping of Addresses and explains the mappings using the <mapping> element to make a clear connection to the FREG model.|
|2020-09-09|gd-Address.StructureDefinition-profile.xml|Fixed a bug where urban district was marked must-support, this is not the case for international adresses|
|2020-09-09|gd-fregmetadata.StructureDefinition-extension.xml|Added duplicated mapping information contains both alias and mapping tags|
|2020-09-09|gd-address-metadata.StructureDefinition-extension.xml|Added duplicated mapping information contains both alias and mapping tags|
|2020-09-09|gd-Address-box.StructureDefinition-profile.xml|Added duplicated mapping information contains both alias and mapping tags|
|2020-09-09|gd-separately-occupied-unit.StructureDefinition-extension.xml|Added duplicated mapping information contains both alias and mapping tags|
|2020-09-09|gd-Address-cadastral.StructureDefinition-profile.xml|Added duplicated mapping information contains both alias and mapping tags|
|2020-09-09|gd-cadastral-address.StructureDefinition-extension.xml|Added duplicated mapping information contains both alias and mapping tags|
|2020-09-09|gd-Address-freeform.StructureDefinition-profile.xml|Added top level mapping and included the use of mapping elements to describe freg mappings|
|2020-09-09|gd-preferred-address.StructureDefinition-extension.xml|Added duplicated aliases in mapping element|
|2020-09-09|gd-Address-international.StructureDefinition-profile.xml|Added top level mapping and included the use of mapping elements to describe freg mappings|
|2020-09-09|gd-Address-street.StructureDefinition-profile.xml|Added top level mapping and included the use of mapping elements to describe freg mappings|
|2020-09-09|gd-Address-unknown.StructureDefinition-profile.xml|Added top level mapping for all addresstypes (Bostedsadresse, DeltBosted and Oppholdsadresse). Included the use of mapping elements to describe freg mappings. Added mapping to municipality and addressIsUnknown elements|
|2020-09-11|Implementation Guide text|Updated description of *History of a resource* in the service interface description, to clearify what elements contains history information from FREG, specificly RelatedPerson|
|2020-09-16|gd-Provenance.StructureDefinition-profile|Documentation changes gd-Provenance.StructureDefinition-profile.xml|

## Documents the changes implemented from version 2.1.0 to 2.2.0

### Release date: 2020-04-02

This is a service release to includes changes to the documentation based on feedback on the 2.1.0 version. No breaking changes in the capabilities are documented in this version, but several updated to extend the capabilites described in the CapabilityStatement.

- Added search parameter support for several search parameters in the CapabilityStatement
- Added SearchParameter definitions for AddressContentType and AddressType
- Updated CapabilityStatement to include several new search parameters
- Major update to the documentation of RelatedPerson to clarify how this Resource is used to code FREG data
- Updates to the "Readers Guide" to clarify the use of POST transaction and the meaning of must-support flags in this ImplementationGuide
- Some minor documentation changes in the gd-Person StructureDefinition updates to clearify the documentation concerning birtDate and foreignIdentifier
- gd-birth-in-norway bugfix, added freg-metadata to extension
- gd-person-citizenship Change the name of the codesytem/valueset, updated to documentation
- gd-migration.StructureDefinition-extension, update to documentation and ValueSet
- gd-Identifier-foreign update to codesystems and documentation
- gd-Identifier update documentation
- Updated CapabilityStatement for both L0 and L1
- Search parameter definition for given and family names of a Person
- Updated documentation for RelatedPerson.patient references

## Files change description

|File|Change description|
|-
|StructureDefinition/gd-birth-in-norway.StructureDefinition-extension.xml|Added freg-metadata to the extension to hold metadata from freg about this content|
|CapabilityStatement/gd-Server-Requirements.xml|Several updates and bugfixes to describe L0 delivery|
|CapabilityStatement/gd-Server-Requirements-v300.xml|New file to describe L1 delivery|
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
|CodeSystem/gd-person-migration-pattern.CodeSystem.xml|Updated filename and url of the CodeSystem|
|ValueSet/gd-person-migration-pattern.ValueSet.xml|Updated filename and url of the ValueSet, updated reference to CodeSystem|
|StructureDefinition/gd-migration.StructureDefinition-extension.xml|Updated reference to migration-pattern ValueSet|
|StructureDefinition/gd-Identifier-foreign.StructureDefinition-profile|Description added for all elements not used in this profile, Updated must-support information, Removed the 1..1 cardinality for identifier.system, the identifier system value should not be set, Added description of the use of identifier.type for the foreign identifiers, Added description for period and assigner "This element is not used by gd-Identifier-foreign", updated codesystem and valueset to new naming sceme|
|CodeSystem/gd-person-identificationnumbertype.CodeSystem.xml|Updated filename and url of the CodeSystem|
ValueSet/gd-person-identificationnumbertype.ValueSet.xml|Updated filename and url of the ValueSet, updated reference to CodeSystem|
|StructureDefinition/gd-Identifier-foreign.StructureDefinition-profile.xml|Added must support information for elements, Added descripton for all elements not used in the profile "This element is not used by gd-Identifier"|
|examples/gd-RelatedPerson-example.xml|Bugfix of the Coded value for scope|
|StructureDefinition/gd-RelatedPerson.StructureDefinition-profile.xml|Added must support for RelatedPerson.patient.reference and updated documentation concerning references|

## Documentation changes after 2.2.0 release

|Date|File|Change description|
|-
|2020-04-15|Implementation Guide text|Updated the description of change and event types. Including new ValueSet rendering for gd-Provenance|
|2020-04-15| New file|The activity types used by Persontjenesten: ValueSet/gd-provenance-activity-types.valueset.xml|
|2020-04-29|2.2.1 version GdProvenance: gd-Provenance.StructureDefinition-profile.xml|ValueSet binding to the GdProvenance valueset|
|2020-04-29|2.2.1 version GdProvenance examples|ValueSet binding to the GdProvenance valueset|
|2020-04-29|gd-family-relation.StructureDefinition-extension|Changed the name of element roleOfPersonInstance -> roleOfRelatedPersonInstance|
|2020-04-29|gd-RelatedPerson.StructureDefinition-profile|Changed the name of element roleOfPersonInstance -> roleOfRelatedPersonInstance|
|2020-04-30|new file gd-RelatedPerson-example-family|New example|
|2020-04-30|Package update v2.2.2 created|Service Release to remove duplicate valuesets and codesystems generated by SIMPLIFIER|
|2020-05-04|Updated dependency|Updated dependency of hl7.fhir.no.basis to the latest patch 2.0.13|
|2020-05-04|Documentation|Some updates to the Implementation guide: Person information intro|
|2020-05-04|Package update v2.2.3 created|Service release to remove another CodeSystem duplicate from SIMPLIFIER. no-basis-dependency updated 2.0.13|
|2020-05-06|Documentation|Updates to the implementation guide, adding intro to profile pages to help readability|
|2020-05-06|Documentation|Update to RelatedPerson (roleOfRelatedPersonInstance)|
|2020-05-06|Package update v2.2.4 created|Fixed a technical issue with SIMPLIFIER sync to Github. The updates to gd-Provenance profile, gd-family-relation extension and gd-provenance-activity-type valueset was missing from SIMPLIFIER. Made an explicit sync of these files into SIMPLIFIER and created a new package to contain the updates|

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
|2020-03-26|ImplementationGuide text|Cleared up some confusing use of logical vs literal references on the RelatedPerson page|