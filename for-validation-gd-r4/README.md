# To use the Official FHIR Validator
## A collection of files to work with the official FHIR validator

There are some problems using oid identified ValueSets in profiles that the official FHIR validator don't handle well. This collection of files should solve the validator problems and validate examples conforming to the profiles correctly.

The official validator can be downloaded here: https://www.hl7.org/fhir/downloads.html

no-basis-propertyinformation fix for official validator - removed oid binding of valueset in profiles, replace with http reference e.g. http://hl7.no/fhir/ValueSet/2.16.578.1.12.4.1.1.3402
* C:\GitRepo\Grunndata-R4\for-validation-gd-r4\gd-Address-cadastral.StructureDefinition-profile.xml (2 hits)
	Line 1634:         <valueSet value="urn:oid:2.16.578.1.12.4.1.1.3402" />
	Line 1789:         <valueSet value="urn:oid:2.16.578.1.12.4.1.1.3402" />
  C:\GitRepo\Grunndata-R4\for-validation-gd-r4\gd-Address-street.StructureDefinition-profile.xml (2 hits)
	Line 1637:         <valueSet value="urn:oid:2.16.578.1.12.4.1.1.3402" />
	Line 1792:         <valueSet value="urn:oid:2.16.578.1.12.4.1.1.3402" />

