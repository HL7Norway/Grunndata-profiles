# Område for profiler tilhørende Grunndata
# FHIR version R4 4.0.0

- Profiler av resources
- Extensions
- Eksempler
- Implementasjonsguider med metafiler
- CapabilityStatement
- PackageDefinition
- Figurer og illustrasjoner

## Publisering
Ferdige profiler publiseres også her: 
https://simplifier.net/grunndata-r4

## Vi benytter Feature branch workflow
![Feature branch workflow](https://git.sarepta.ehelse.no/utvikling/FHIR/raw/92dff80b4b825be384908a90a3abfa7d6a8d6a46/Feature-branch-workflow.JPG)

Vi baserer oss på at nye features utvikles i egne feature branches og merges inn i master branch etterhvert som de er klare. Arbeidsflyten er forklart i detalj her:
https://www.atlassian.com/git/tutorials/comparing-workflows/feature-branch-workflow

## Katalogstruktur

|\\[prosjektnavn]| | |
|---|---|---|
| |\\CapabilityStatement | Capability statement, API spesifikasjon |
| |\\CodeSystem | CodeSystem definisjoner |
| |\\examples | eksempler |
| |\\images | illustrasjoner og figurer |
| |\\REST-kall | Optional |
| |\\StructureDefinition | alle extensions og profiler |
| |\\ValueSet | ValueSet definisjoner |
| |[prosjektnavn]-[versjon].zip | Pakke med det ferdige resultatet for en versjon |

## Navngivning av filer
Inne i katalogene benytter vi navngivningsregler fra [SIMPLIFIER Best practices](https://simplifier.net/guide/ProfilingAcademy/Best-practices)

**Filnavn for profiler og extensions:**  

gd-Practitioner.structuredefinition-profile.xml  
gd-Person.structuredefinition-profile.xml

gd-additional-humanname.StructureDefinition-extension.xml

**URL'ene i koden:**  
http://ehelse.no/fhir/StructureDefinition/gd-Person

## kontakt

thomas punktum tveit punktum rosenlund at ehelse punktum no

michal punktum cermak at ehelse punktum no
