# RelatedPerson information

FREG exposes severeal relationship between persons as registered in the Master Person Index. This page gives a quick intro to the relationships exposed through the FHIR interface of Grunndata Person. The relationship model exposed in the FHIR interface is exposes the same relationshiops described in Skatteetaten FREG but is rendered using FHIR Resources. Please refer to the documentation from [Skatteetaten](https://skatteetaten.github.io/folkeregisteret-api-dokumentasjon/informasjonsmodell/) for more complete information about the relationships model exposed from FREG.

## FREG exposes four relationship types

The relationship types exposed in FREG is:
- sivilstand (maritalStatus)
- familierelasjon (familyRelation)
- foreldreansvar (parental)
- vergemål (guardianship)

The main difference in how the FREG model works compared to the FHIR model is that a relationship in FREG is recorded as a relationship to another person in one person's person information (document). In the FHIR model each relationship is recorded in a separate RelatedPerson resource instance containting a record of all relationships recorded for a RelatedPerson.patient -> RelatedPerson.

The FREG relationships can be represented by this logical model:
<a href="https://raw.githubusercontent.com/HL7Norway/Grunndata-profiles/master/images/Relationship-Logical-FREG.png">
<img src="https://raw.githubusercontent.com/HL7Norway/Grunndata-profiles/master/images/Relationship-Logical-FREG.png" alt="Drawing" style="width: 100%;max-width: 1000px"/></a>

The corresponding FHIR model can be expressed like this:
<a href="https://raw.githubusercontent.com/HL7Norway/Grunndata-profiles/master/images/Relationship-Logical-FHIR.png">
<img src="https://raw.githubusercontent.com/HL7Norway/Grunndata-profiles/master/images/Relationship-Logical-FHIR.png" alt="Drawing" style="width: 100%;max-width: 1000px"/></a>

The main difference on how the relationships is exposed to the readers of the services is that while FREG exposes relationships as part of a person document, the FHIR model exposes each persons relations to another person through a separate RelatedPerson instance containing a reference to the person and a record of every relationship between the person and the relatedperson.

