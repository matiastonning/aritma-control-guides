Alle nye [[Kontogrupper]] kommer med et standard sett avstemmingsregler som brukes for automatisk avstemming. Det er også mulighet for å endre på disse, eller opprette egne regler etter behov. Så lenge det finnes et mønster i transaksjonene som som skal matches, vil det være mulig å opprette en regel som fanger disse opp automatisk. For å endre reglene til en kontogruppe trykker du på "Settings" øverst i høyre hjørne.


## Maks datoavvik
Maksimalt datoavvik bestemmer hvor stort datoavviket kan være på transaksjoner som skal matches. Denne settes som standard til 3. Det er mulig å sette maks datoavvik på tvers av alle reglene for gruppen, eller du kan finjustere maks datoavvik per regel.

> [!Warning] Advarsel
> Hvis du endrer "Max Date Deviation" under "Rules", vil maks datoavvik endres for alle reglene i gruppen. Vi anbefaler at du først setter denne til ønsket verdi, før du finjusterer maks datoavvik per regel.
> 
> ![[Max Date Deviation.png|350]]


## Avanserte regler
Avanserte regler sorteres etter prioritet. Prioritet kan justeres ved å dra en regel opp eller ned. Dersom transaksjoner treffer på flere regler, vil prioriteten bestemme hvilken regel de avstemmes på.

![[Advanced Rules.png]]

### Regeltyper
| Navn           | Beskrivelse                                        |
| -------------- | -------------------------------------------------- |
| PostToPost     | Matcher poster en mot en                           |
| OneToMany      | Matcher en regnskapspost mot flere bankposter      |
| ManyToOne      | Matcher flere regnskapsposter mot en bankpost      |
| ManyToMany     | Matcher flere regnskapsposter mot flere bankposter |
| PostToPostLeft | Matcher regnskapsposter en mot en                  |

### Opprette eller endre avansert regel
Trykk på den blå "New Rule" knappen for å opprette en ny regel. For å endre en regel trykker du på blyant-knappen til høyre for regelen. Her vil du få valg om regeltype, maks datoavvik, og hvilke felter transaksjonene skal grupperes på. Gruppering er kun relevant for regeltypene OneToMany, ManyToOne, og ManyToMany.

![[New Rule.png]]

I skjermbildet over, oppretter vi en regel som vil forsøke å gruppere flere regnskapsposter basert på bilagsbeskrivelsen. Dersom den fanger opp en gruppe med bilag som har identisk beskrivelse, vil den sammenlikne summen av beløpene og bokføringsdatoene mot en enkelt post på banksiden. Postene blir automatisk avstemt hvis regelen finner en bankpost med identisk beløp, så lenge avviket mellom bokføringsdatoene ikke overstiger maks datoavvik.

Basert på regelen over, ville disse eksempelpostene blitt avstemt automatisk:

| Bokføringsdato | Beløp | Beskrivelse | Type     |
| -------------- | ----- | ----------- | -------- |
| 01.01.2022     | 150kr | ABC123      | Regnskap |
| 02.01.2022     | 100kr | ABC123      | Regnskap |
| 03.01.2022     | 25kr  | ABC123      | Regnskap |
|                |       |             |          |
| 01.01.2022     | 275kr |             | Bank     |


#### Tekstfilter
Tekstfilter kan brukes til å filtrere transaksjoner basert på diverse tekstoperatører. For å opprette et tekstfilter, trykker du på den grå TT-knappen til høyre for det aktuelle feltet, og legger inn de filtrene du trenger. Husk å trykk Enter for å bekrefte nøkkelord under "FilterValues".

![[Text Filter Rule.png]]

I skjermbildet over vil regelen kun gruppere regnskapsposter med identisk konto, og med en beskrivelse som begynner med "ARITMA". Basert på denne regelen, ville disse eksempelpostene blitt  avstemt automatisk:

| Bokføringsdato | Beløp | Beskrivelse   | Konto       | Type     |
| -------------- | ----- | ------------- | ----------- | -------- |
| 01.01.2022     | 150kr | ARITMA 1      | 1520        | Regnskap |
| 02.01.2022     | 100kr | ARTIMA 2      | 1520        | Regnskap |
| 03.01.2022     | 25kr  | ARTIMA BERGEN | 1520        | Regnskap |
|                |       |               |             |          |
| 01.01.2022     | 275kr |               | 12345678900 | Bank     |
