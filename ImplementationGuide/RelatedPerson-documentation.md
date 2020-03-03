# RelatedPerson information

FREG exposes information about severeal real world relationships between persons as registered from different information sources in the Master Person Index (FREG). This page gives a quick intro to the relationships exposed through the HL7 FHIR interface of Grunndata Person. 

The relationship information exposed through the FHIR interface is equal to the information available from Skatteetaten FREG. However the information model for representing this information is mapped to a HL7 FHIR based model. The actual data available to the consumer of the API are represented using FHIR resource instances that are tailored to include all the information available from FREG. Please refer to the documentation from [Skatteetaten](https://skatteetaten.github.io/folkeregisteret-api-dokumentasjon/informasjonsmodell/) for more complete information about the relationships model, and the entire FREG information model, exposed from FREG.

## FREG exposes four relationship types

The relationship types exposed in FREG are:
- sivilstand (maritalStatus)
- familierelasjon (familyRelation)
- foreldreansvar (parental)
- vergemål (guardianship)

The main difference in how the FREG model works compared to the FHIR model is that a relationship in FREG is recorded as a relationship to another person registered as part of any given person's person-information (document). In the FHIR model each relationship is recorded in a separate RelatedPerson resource instance containting a record of all relationships recorded between a RelatedPerson.patient -> RelatedPerson. 

The RelatedPerson resource instances includes three main parts of information to describe the relationships.
- information about the identity of the RelatedPerson
- a reference to the person related to the RelatedPerson (called patient in the RelatedPerson instance) 
- information describing the nature of the relationships between the RelatedPerson and the patient referenced

The FREG relationships can be represented by this logical model:
<a href="https://raw.githubusercontent.com/HL7Norway/Grunndata-profiles/develop/images/Relationship-Logical-FREG.png">
<img src="https://raw.githubusercontent.com/HL7Norway/Grunndata-profiles/develop/images/Relationship-Logical-FREG.png" alt="Drawing" style="width: 100%;max-width: 1000px"/></a>

The corresponding FHIR model can be expressed like this:
<a href="https://raw.githubusercontent.com/HL7Norway/Grunndata-profiles/develop/images/Relationship-Logical-FHIR.png">
<img src="https://raw.githubusercontent.com/HL7Norway/Grunndata-profiles/develop/images/Relationship-Logical-FHIR.png" alt="Drawing" style="width: 100%;max-width: 1000px"/></a>

The main difference on how the relationships is exposed to the readers of the services is that while FREG exposes relationships as part of a person document, the FHIR model exposes each persons relations to another person through a separate RelatedPerson instance containing a reference to the person and a record of every relationship between the person and the RelatedPerson. A simple way of describing this is that while all relationships of a person is awailable in a single document in FREG, the same information is awailable throug one Person resource instance and several RelatedPerson resource instances in the FHIR model.

## Example FREG vs FHIR model

A simple example of the FHIR resource instances needed to describe a small family containing a married couple and a single child. The logical model of the relationships can be expressed like this:
<a href="https://raw.githubusercontent.com/HL7Norway/Grunndata-profiles/develop/images/Logical-family-relationships.png">
<img src="https://raw.githubusercontent.com/HL7Norway/Grunndata-profiles/develop/images/Logical-family-relationships.png" alt="Drawing" style="width: 100%;max-width: 1000px"/></a>

### FREG model example

Using the information model described by FREG this information is represented like this:
<a href="https://raw.githubusercontent.com/HL7Norway/Grunndata-profiles/develop/images/Relasjon-family-relationships-FREG-example.png">
<img src="https://raw.githubusercontent.com/HL7Norway/Grunndata-profiles/develop/images/Relasjon-family-relationships-FREG-example.png" alt="Drawing" style="width: 100%;max-width: 1000px"/></a>

### FHIR model example

Using the FHIR based model the same information can be represented like this:
<a href="https://raw.githubusercontent.com/HL7Norway/Grunndata-profiles/develop/images/RelatedPerson-family-relationships-FHIR-example.png">
<img src="https://raw.githubusercontent.com/HL7Norway/Grunndata-profiles/develop/images/RelatedPerson-family-relationships-FHIR-example.png" alt="Drawing" style="width: 100%;max-width: 1000px"/></a>
