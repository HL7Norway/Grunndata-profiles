# Address types and address content types

FREG exposes several new types of addresses on the new interface. All address types defined by FREG are also exposed by the Master Person Index for health care. In the current version (called DSF) only one kind of address is recorded; the official address called "Bostedsadresse". Consumers of the service must read and store the different address types and content types coming from FREG and use the different address types according to their intended purpose. This page will give a quick overview of the addresses available, for the complete documentations please refer to [Skatteetaten](https://skatteetaten.github.io/folkeregisteret-api-dokumentasjon/informasjonsmodell/).

## FREG exposes 6 different AddressTypes

- Bostedsadresse 
- Oppholdsadresse 
- DeltBosted 
- Kontaktadresse 
- KontaktadresseUtlandet 
- PreferertKontaktadresse

### Bostedsadresse
Adressen hvor en person bor i henhold til folkeregisterforskriften
The address a person lives according to the "folkeregisterforskriften".

### Oppholdsadresse
En annen adresse enn bostedsadresse der personen faktisk oppholder seg.
Another registered address (different from bostedsadresse) where the person is actually staying.

### DeltBosted
En ordning hvor barnet bor fast hos begge foreldre.
When a child stays with both parents (the parents don't live at the same address).

### Kontaktadresse
Fellesbetegnelse for postadresse i Norge eller i utlandet.
Postal address in Norway or abroad.

### KontaktadresseUtlandet
Postadresse som adresserer et sted utenfor Norge.
Postal address for address outside Norway.

### PreferertKontaktadresse
Valg av hvilken av adressene en person er oppført med som skal benyttes til å
kontakte personen.
A personal choice of what address type should be used to contact the individual.

## FREG exposes 9 AddressContentTypes

The content types in FREG is used to structure the address information in different fasion for the different uses. FREG exposes addresses differently based on what information they have registered from the different sources. The different AddressTypes can only use predefined address content types to expose the information. The different content types used for each AddressTypes is documented below.

### The content types defined

- Vegadresse
- VegadresseForPost
- Postboksadresse
- Matrikkeladresse
- InternasjonalAdresse
- PostadresseFrittFormat
- InternasjonalAdresseFrittFormat
- UkjentBosted (only for "bostedsadresse" and "deltbosted")
- AdressenErUkjent (only for "oppholdsadresse")

### Bostedsadresse
Include any of these AddressContentTypes:
- Vegadresse (gd-Address-street)
- Matrikkeladresse (gd-Address-cadastral)
- UkjentBosted (gd-Address-unknown)

### Oppholdsadresse
Include any of these AddressContentTypes:
- Vegadresse (gd-Address-street)
- Matrikkeladresse (gd-Address-cadastral)
- AdressenErUkjent (gd-Address-unknown)
- InternasjonalAdresse (gd-Address-international)

### DeltBosted
Include any of these AddressContentTypes:
- Vegadresse (gd-Address-street)
- Matrikkeladresse (gd-Address-cadastral)
- UkjentBosted (gd-Address-unknown)

### Kontaktadresse
Include any of these AddressContentTypes:
- Postboksadresse (gd-Address-box)
- VegadresseForPost (gd-Address-street)
- PostadresseFrittFormat (gd-Address-freeform)

### KontaktadresseUtlandet
Include any of these AddressContentTypes:
- InternasjonalAdresse (gd-Address-international)
- InternasjonalAdresseFrittFormat (gd-Address-freeform)

### PreferertKontaktadresse
Include the AddressContentType of
- gd-Address-freeform

## Address metadata

The information regarding AddressContentTypes and AddressTypes  are contained in the gd-address-metadata extension. Five different gd-Address profiles have been created to accomodate the different information content in the AddressContentTypes from FREG, as some of the content types from FREG was to similar to differentiate on them in a meaningfull way in FHIR.