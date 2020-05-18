# Adressebeskyttelse (addressprotection valueset)
Hver folkeregisterperson har informasjon om adressebeskyttelse definisjon:
informasjon om gradering av adresseinformasjon for personer iht. Beskyttelsesinstruksen
Informasjonen benyttes til å beskrive det overordnede felles beskyttelsesnivået en person har på alle sine adresser av typen bostedsadresse, oppholdsadresse og delt bosted. Adressebeskyttelsen gjelder ikke kontaktadressene.	

## Beskyttelsesgraden angis i adressegradering elementet til personen (meta.security i FHIR):
nivå av beskyttelsesgrad på informasjon
Gyldige kodeverdier er:
 ugradert
 fortrolig
 strengtFortrolig (strengt fortrolig)


# Adressegradering oppsummering (address-confidentiality valueset)

## adressegradering
Adressene som kan graderes har elementet adressegradering i hver ankelt adresse (GdAddressMetadata.confidentiality i FHIR)
Definisjon av adressegradering:
kategori av beskyttelsesgrad på adresseinformasjon i Folkeregisteret
Gyldige kodeverdier er:
 ugradert
 klientadresse
 fortrolig
 strengtFortrolig (strengt fortrolig)
Bostedsadressen kan være beskyttet iht. Beskyttelsesinstruksen (fortrolig og strengtFortrolig) eller Folkeregisterloven (klientadresse). Adresse med gradering strengtFortrolig oppgis ikke av Folkeregisteret.

## For postadresser:
kategori av beskyttelsesgrad på adresseinformasjon i Folkeregisteret
Gyldige kodeverdier er:
 ugradert
 klientadresse
Postadressen kan være beskyttet iht. Folkeregisterloven (klientadresse).




# Gradering av Post og kontaktadresser
Post/kontaktadresser kan ikke ha beskyttelsesgrad i henhold til beskyttelsesinstruksen. Disse kan likevel kategoriseres som klientadresser i henhold til folkeregisterloven.
Adressene graderes i samme element som adresser som kan ha beskyttelse altså adressegradering  i hver ankelt adresse (GdAddressMetadata.confidentiality i FHIR). 
Kodene for beskyttelse kan ikke benyttes.
Disse har adressegradering:
kategori av beskyttelsesgrad på adresseinformasjon i Folkeregisteret
Gyldige kodeverdier er:
 ugradert
 klientadresse
Postadressen kan være beskyttet iht. Folkeregisterloven (klientadresse)
