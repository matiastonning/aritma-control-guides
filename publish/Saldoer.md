Saldo for både bank og regnskap presenteres på to måter. Den første er ==Balance==, som er saldoen vi har kalkulert ved å summere alle transaksjonene som tilhører kontoen.
Den andre er ==Statement Balance==, som er saldoen vi henter direkte fra kontoutskriften. Det vil si saldoen slik banken eller regnskapssystemet har kalkulert den.

==Balance== skal alltid være lik ==Statement Balance==. Dersom det er en differanse, betyr det sannsynligvis at Control mangler noen transaksjoner, eller at det har blitt lagt inn feil oppstartsbalanse under [[Opprette nye kontogrupper#Steg 2: Kontroller saldoer|kontooppsettet]].


> [!EXAMPLE] Eksempel
> I bildet nedenfor viser vi til to eksempelsaldoer. Balance for 1920 har vi kalkulert til kr 20 376 215,80. Statement Balance viser saldoen slik vi har hentet den fra regnskapet, og som vi ser foreligger det en differanse. Her er det altså noe som ikke stemmer.
> 
> Balance og Statement Balance for bankkontoen har derimot ingen differanse, og vi kan trygt anta at Control ikke mangler noen transaksjoner.
> 
> ---
> 
> ![[Balance Difference.png|550]]


> [!ERROR] Slik løser du en saldodifferanse
> Det første du bør gjøre er å dobbeltsjekke at den inngående balansen du la inn under [[Opprette nye kontogrupper|kontooppsettet]] er riktig. For å sjekke oppstartsbalansen, gå til [[Kontogrupper|kontogruppen]] det gjelder og sett "To Date" til den første dagen i oppstartsperioden. Hvis kontogruppen er satt opp til å avstemme fra 202201, setter du "To Date" til 01.01.2022. Du vil nå se oppstartsbalansen i balanseoversikten. Sammenlikn denne med den inngående balansen til perioden på kontoutskriften. Hvis den har blitt lagt inn feil, må [[Slett kontogruppe|kontogruppen slettes]] og opprettes på nytt med riktig oppstartsbalanse.
> 
> ---
> 
> ![[Starting Balance.png|550]]
> 
> ---
> 
> Dersom oppstartsbalansen er lagt inn riktig, skyldes sannsynligvis differansen at Control mangler noen transaksjoner. Hvis det er tilfellet bør du ta kontakt med  [Aritma Support](mailto:support@aritma.com), så hjelper vi deg videre.
> 

