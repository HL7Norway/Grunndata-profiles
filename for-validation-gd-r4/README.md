# To use the Official FHIR Validator
## A collection of files to work with the official FHIR validator

There are some problems using oid identified ValueSets in profiles that the official FHIR validator don't handle well. This collection of files should solve the validator problems and validate examples conforming to the profiles correctly.

The official validator can be downloaded here: https://www.hl7.org/fhir/downloads.html

The gd-Person lacks a discriminator definition from Forge, this happens on derived profiles (this one derives from no-basis-Person).
 Error @ StructureDefinition.differential.element[19].slicing (line 177, col16) : eld-1: If there are no discriminators, there must be a definition [discriminator.exists() or description.exists()]
    <element id="Person.identifier">
      <path value="Person.identifier" />
      <slicing>
        <discriminator>
          <type value="value" />
          <path value="system" />
        </discriminator>
        <rules value="closed" />
      </slicing>
Add to gd-Person:
		<discriminator>
          <type value="value" />
          <path value="system" />
        </discriminator>

no-basis-propertyinformation fix for official validator - removed oid binding of valueset in profiles, replace with http reference e.g. http://hl7.no/fhir/ValueSet/2.16.578.1.12.4.1.1.3402
* C:\GitRepo\Grunndata-R4\for-validation-gd-r4\gd-Address-cadastral.StructureDefinition-profile.xml (2 hits)
	Line 1634:         <valueSet value="urn:oid:2.16.578.1.12.4.1.1.3402" />
	Line 1789:         <valueSet value="urn:oid:2.16.578.1.12.4.1.1.3402" />
  C:\GitRepo\Grunndata-R4\for-validation-gd-r4\gd-Address-street.StructureDefinition-profile.xml (2 hits)
	Line 1637:         <valueSet value="urn:oid:2.16.578.1.12.4.1.1.3402" />
	Line 1792:         <valueSet value="urn:oid:2.16.578.1.12.4.1.1.3402" />

Feil ved validering av eksempler:
 validate [c:\GitRepo\Grunndata-r4\examples\gd-Person-02121998516-AdressenErUkjent.xml, c:\GitRepo\Grunndata-r4\examples\gd-Person-03121999934-UkjentBosted.xml, c:\GitRepo\Grunndata-r4\examples\gd-Person-04021950128-version-2.xml, c:\GitRepo\Grunndata-r4\examples\gd-Person-04021950128.xml, c:\GitRepo\Grunndata-r4\examples\gd-Provenance-Create.xml, c:\GitRepo\Grunndata-r4\examples\gd-Provenance-UPDATE-2.xml, c:\GitRepo\Grunndata-r4\examples\gd-Provenance-UPDATE.xml, c:\GitRepo\Grunndata-r4\examples\gd-RelatedPerson-example.xml]
Unable to generate snapshot for gd-Address from no-basis-Address because Profile GdAddress (http://ehelse.no/fhir/StructureDefinition/gd-Address). Error generating snapshot: Error sorting Differential: StructureDefinition http://ehelse.no/fhir/StructureDefinition/gd-Address: Differential contains path Address.extension.value[x].display which is actually Element.display, which is not found in the base
org.hl7.fhir.exceptions.DefinitionException: Profile GdAddress (http://ehelse.no/fhir/StructureDefinition/gd-Address). Error generating snapshot: Error sorting Differential: StructureDefinition http://ehelse.no/fhir/StructureDefinition/gd-Address: Differential contains path Address.extension.value[x].display which is actually Element.display, which is not found in the base
        at org.hl7.fhir.r5.context.SimpleWorkerContext.generateSnapshot(SimpleWorkerContext.java:619)
        at org.hl7.fhir.r5.context.SimpleWorkerContext.allStructures(SimpleWorkerContext.java:479)
        at org.hl7.fhir.r5.validation.ValidationEngine.prepare(ValidationEngine.java:1326)
        at org.hl7.fhir.r5.validation.Validator.main(Validator.java:652)
 
Forslag til fix: 
 - Forsøkte å lage ny GdAddress uten endringene i urban-district for å se om det glir igjennom.
