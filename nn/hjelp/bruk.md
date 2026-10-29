# Bruk

Denne rettleiinga er for deg som nett har byrja å bruke Voss HPK-wikien.

## Finn fram

- Opne ei gruppe i sidemenyen for å sjå sidene ho inneheld.
- Bruk søkjefeltet når du leitar etter eit ord, ein stad eller eit dokument.
- Bruk språkveljaren øvst for å byte mellom nynorsk og engelsk.
- Vel **Bla gjennom** dersom du vil navigere etter mappestrukturen.

## Mapper og navigasjon er ulike ting

Ei sidemappe bestemmer kvar wiki-sidene ligg og kva sidesti dei får.
Navigasjonsmenyen er ei eiga samling av overskrifter, lenkjer og undermenyar i sidestolpen.
Ei mappe lagar ikkje automatisk ei navigasjonsgruppe, og ei navigasjonsgruppe flyttar ikkje sidene.
Du kan til dømes lagre ei side i `ny-mappe/ny-side` utan at det finst ei tilsvarande gruppe i sidemenyen.

Ei automatisk navigasjonsjobb les sidene som er lagra i wikien og lagar menylenkjer for dei.
Nye toppmapper som er lagde inn i gruppelista for navigasjonen, kjem under den tilhøyrande gruppa når gruppa finst i sidemenyen.
Undermapper og sider blir viste under menylenkja til den overordna mappa når ho har ei landingsside.
Viss ei mappe ikkje er kopla til ei navigasjonsgruppe, kjem ho under **Ugruppert**.
Sider på rotplanet som ikkje er kopla til ei gruppe, kjem òg under **Ugruppert**.
Har ei mappe inga landingsside, blir sidene viste som direkte lenkjer med mappestigen i lenkjeteksten.
**Ugruppert** er ei utvidbar mappe etter Hjelp med ei skiljelinje over, og både mappa og linja forsvinn når ingen lenkjer står att under henne.
Menyen blir oppdatert automatisk etter at det lagra sideinnhaldet er synkronisert, så endringar kan bruke nokre minutt på å kome fram.
Navigasjonsjobben tek vare på plasseringa til menylenkjer som finst frå før.
Viss plasseringa til ei eksisterande lenkje skal endrast, må ein redaktør flytte henne i Wiki.js.
Viss ei ny mappe skal kome automatisk i ei ny eller eksisterande gruppe, må wikiforvaltaren leggje mappestigen inn i den tekniske gruppelista.

## Opprett ei side og ei mappe samstundes

Vel **New Page** i Wiki.js og opne dialogen **Save As** for å velje kvar sida skal liggje.
Vel mappa som skal vere foreldermappe, eller vel rotmappa dersom du vil lage ei ny toppmappe.
Bruk valet **New Folder** i mappetreet og skriv inn namnet på den nye mappa.
Skriv inn sidetittelen og eit kort sidestignamn med små bokstavar og bindestrek, til dømes `ny-mappe/ny-side`.
Ta ikkje med `nn/` eller `en/` i sidestigen, sidan Wiki.js brukar språket som er valt.
Lagre sida i den nye mappa, slik at mappa får ei side og blir synleg i innhaldet.

![Dialogen for å lagre ei side, velje sidesti og opprette ei ny mappe](https://raw.githubusercontent.com/vosshpk/wiki/main/assets/help/pages/create-page-and-folder.png)

Ei mappe for wiki-sider kjem med i innhaldsrepositoriet når ho inneheld minst éi lagra side.
Vil du lage ei mappe for opplasta bilete eller andre filer, brukar du **Filhandsamar** i staden.

### Lag mappa først

Bruk **New Folder** i sidebanetreet og vel mappa ho skal liggje under.
Opprett ei side i den nye mappa eller flytt ei eksisterande side dit.
Ei tom mappe kjem ikkje med i innhaldsrepositoriet eller navigasjonsmenyen fordi navigasjonsjobben byggjer menyen frå lagra sider.

## Flytt ei side inn i ei mappe

Opne sidetreet eller sideoversikta, og opne handlingsmenyen for sida du vil flytte.
Vel **Rename / Move Page...**, og skriv inn den nye sidestigen med mappa først.
Kontroller sidetittelen og sidestigen før du lagrar flyttinga.
Når sidestigen blir endra, bør du kontrollere lenkjer til sida frå andre sider og dokument.
Navigasjonsjobben oppdaterer menylenkjene etter at den nye sidestigen er synkronisert.

![Handlingsmenyen for ei wiki-side med valet Endre namn / flytt side](https://raw.githubusercontent.com/vosshpk/wiki/main/assets/help/pages/page-rename-or-move.png)

## Lag eller endre ei navigasjonsgruppe

Navigasjonsgrupper blir redigerte i Wiki.js, uavhengig av sidemappene.
Vel **Edit Nav** nedst i sidemenyen, og opne **Edit Menu Items** for den delte menyen.
Viss Wiki.js viser menyinnstillingane, rediger menyen som blir brukt på tvers av sidene i wikien.

![Sidemenyen med knappen Rediger navigasjon nedst](https://raw.githubusercontent.com/vosshpk/wiki/main/assets/help/navigation/sidebar-help-and-edit-navigation.png)

![Innstillingane for å redigere den delte navigasjonen](https://raw.githubusercontent.com/vosshpk/wiki/main/assets/help/navigation/edit-navigation-settings.png)

Trykk **Add** for å sjå menytypane **Header**, **Link**, **Menu** og **Separator**.
Bruk **Header** for å lage namnet på ei navigasjonsgruppe.
Ikkje bruk typen **Menu** for ei slik gruppe, sidan navigasjonsjobben brukar overskrifter og nøsta lenkjer.
Bruk **Link** for å lage ei klikkbar lenkje eller ein utvidbar forelder for ei undermeny.
For ein utvidbar forelder vel du **Link (as trigger)**, skriv inn ei målside dersom gruppa har ei landingsside, og set ikonet til `mdi:folder-outline`.
Navigasjonsjobben set dette mappeikonet på mappe-lenkjer han kjenner att, også når dei alt finst i menyen.
Legg sidelenkjene under denne forelderen og bruk **Nest Item** for å plassere dei som undermenyelement.
Skal lenkjene berre stå under ei overskrift utan ei utvidbar mappe, legg du dei etter overskrifta utan å nøste dei.

![Menyen for å leggje til ei overskrift, lenkje, meny eller skiljelinje](https://raw.githubusercontent.com/vosshpk/wiki/main/assets/help/navigation/add-navigation-item-types.png)

![Innstillingane for ei lenkje og eit døme på eit nøsta element](https://raw.githubusercontent.com/vosshpk/wiki/main/assets/help/navigation/link-trigger-and-nesting.png)

![Legg til-knappen i navigasjonsredigeraren](https://raw.githubusercontent.com/vosshpk/wiki/main/assets/help/navigation/add-navigation-item-button.png)

Lagre menyelementa og navigasjonsinnstillingane når du er ferdig.
Navigasjonsjobben held på overskrifter og plasseringar som finst frå før, men brukar gruppelista for å plassere nye lenkjer.
For at nye sider i ei mappe skal gå direkte til ei bestemt gruppe, må wikiforvaltaren få den nøyaktige gruppeteksten og mappestigen.
Viss mappa ikkje er kopla til gruppelista, eller gruppa ikkje finst i Wiki.js, kjem nye lenkjer under **Ugruppert**.

## Filhandsamaren

Filhandsamaren er for opplasta bilete, PDF-ar og andre filer som blir brukte på wiki-sider.
Han endrar ikkje sidemapper eller navigasjonsgrupper.
Opne ein sideredigerar, opne verktøymenyen øvst til høgre, og vel **File Manager**.

![Menyen i sideredigeraren med valet File Manager](https://raw.githubusercontent.com/vosshpk/wiki/main/assets/help/pages/open-file-manager.png)

Vel mappa der fila skal liggje, og bruk **New Folder** for å lage ei undermappe for filer.
Opne handlingsmenyen for ei fil eller mappe og vel **Rename** eller **Move**.
Når du flyttar ei mappe, blir filene i henne flytta saman med mappa.
Viss du endrar namn eller flyttar ei fil eller mappe, må lenkjer til filene oppdaterast på wiki-sidene som brukar dei.
For å flytte wiki-sider mellom sidemapper brukar du **Rename / Move Page...** i staden for Filhandsamaren.

For meir om gruppelista og den tekniske navigasjonsjobben kan du lese [Infrastruktur](/hjelp/infrastruktur).

## Les ei side

Klikk på ei lenkje i sidemenyen eller i teksten for å opne sida.
Bruk overskriftene på sida for å finne den delen du treng.
Nokre sider har lenkjer til skjema, kart eller andre dokument.

## Rediger og bidra

Du kan redigere ei side dersom gruppene dine gir deg skrivetilgang.
Vel **Rediger** for å opne redigeringsverktøyet.
Bruk verktøylinja for å lage overskrifter, lister og lenkjer.
Førehandsvis sida dersom valet er tilgjengeleg, og lagre når du er ferdig.
Opne sida på nytt i vanleg vising for å kontrollere at endringa ser rett ut.
Sidehistorikken viser tidlegare versjonar og kan brukast til å samanlikne endringar.
Bidragsytarar kan opprette og redigere sider, men kan ikkje flytte eller slette dei.
Be ein redaktør om hjelp dersom ei side må flyttast eller slettast.
Hald nynorsk og engelsk innhald oppdatert når ei side finst på begge språka.

## Kven kan gjere kva?

| Gruppe | Kva du kan gjere |
| --- | --- |
| Guests | Kan berre lese sider. |
| Contributors | Kan lese, opprette og redigere sider, laste opp filer og sende inn tilbakemelding. |
| Editors | Kan redigere, vurdere, flytte og slette sider, og kan styre navigasjonen. |
| Administrators | Forvaltar Wiki.js-innstillingar, brukarar, grupper og drift. |

Bidragsytarar kan ikkje godkjenne bidrag, flytte eller slette sider eller styre navigasjonen.
Tilgangen din kjem an på kva grupper du høyrer til, og sider kan ha eigne tilgangsreglar.
Spør ein redaktør dersom du er usikker på kva du har tilgang til.
