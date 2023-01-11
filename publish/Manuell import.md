Dersom dere har satt opp en [[Kontogrupper|kontogruppe]] med oppstartsdato før bankintegrasjonen mot Aritma ble bestilt - eller med andre ord, dere vil avstemme tilbake i tid - må manglende transaksjonsdata importeres manuelt. Dette er fordi bankene ikke sender transaksjonsdata fra før bestillingsdato.
Heldigvis er det veldig enkelt å importere historiske data i Control, og det må kun gjøres en gang etter kontogruppeoppsett.

Begynn med å gå til ![[Import.png|24]] Import i sidemenyen. Velg klienten du vil importere bankfiler for, og dra bankfilen inn i det rutete området.

![[Import Screenshot.png]]

## Hvor finner jeg bankfilene?
Bankfilene må hentes fra nettbanken. For de fleste nettbanker kan dette gjøres selvstendig, men hvis du ikke er kjent hvordan du skal gå frem kan vi hjelpe deg. Control støtter filformatene Camt.053 (kan også kalles C053, ISO Kontoinformasjon, eller XML Kontoinformasjon) - og Telepay.
Pass på at du velger et datointervall som ikke overlapper med transaksjonene vi allerede får fra bank. Pass også på at du velger riktig konto, og et av formatene nevnt ovenfor. 


> [!Warning] Merk
> Kontogruppen må allerede være opprettet før du importerer filer. Ellers vet ikke Control hvor transaksjonene skal gå.
