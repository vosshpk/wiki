# Styringsdokument

**For Voss Hang- og Paragliderklubb 2024-2028**

Teksten nedanfor attgjev teksten og figurane i presentasjonen så fullstendig som mogleg.

## Innhald

1. Innleiing og hensikt
2. Organisasjonskart
3. Årshjul
4. Strategisamandrag
5. Posisjon og målgruppe
6. Visjon
7. Misjon
8. Verktøy
9. Verdiar
10. Løfte og bevis

## Innleiing og hensikt

Styret i Voss Hang- og Paragliderklubb ynskjer ei heilskapleg, berekraftig og langsiktig satsing for å leggje til rette for stabile og gode rammevilkår for hanggliding, paragliding og speedgliding på Voss.
Dette dokumentet er eit bidrag for å sikre utvikling.
Utkast til styringsdokumentet 2024-2028 er eit resultat av strategisamlinga til styret og tilsette i 2024.
Det ferdige produktet vil vere prega av innspel frå medlemmer i klubben.
Det vedtekne styringsdokumentet legg føringar for korleis styret planlegg og administrasjonen driftar klubben.
På bakgrunn av dette utarbeidar styret og administrasjonen eit årleg arbeidsprogram som vert lagt fram for årsmøtet.
Klubben treng engasjerte medlemmar med innsikt i klubbens kortsiktige og langsiktige prioriteringar.
Me håpar dette dokumentet aukar engasjementet kring drift og utvikling av klubben.
Styret oppmodar til innspel på medlemsmøte, medlemsundersøking og direkte til leiinga i klubben.
Hjelp styret og klubben til å bli enda betre.

Styret og tilsette
Voss Hang- og Paragliderklubb 2024

## Organisasjonskart

Organisasjonskartet frå presentasjonen er attgjeve nedanfor som PlantUML.

```plantuml
title Organisasjonskart
top to bottom direction
skinparam classAttributeIconSize 0
skinparam linetype ortho

class "Seksjon" as Seksjon
class "Fagleg leiar" as FaglegLeiar
class "Sikkerheitsgruppa" as Sikkerheitsgruppa
class "Utdanningsansvarleg og regelverk" as UtdanningRegelverk
class "Tandemansvarleg" as Tandemansvarleg
class "Materialforvaltar" as Materialforvaltar
class "Sikkerheitsansvarleg\nKan vere ein tilsett." as Sikkerheitsansvarleg
class "Sekretær\nKan vere ein tilsett." as Sekretaer
class "Årsmøte" as Aarsmoete
class "Styret" as Styret
class "Dagleg leiar" as DaglegLeiar
class "Driftsansvarleg og kurskoordinator" as DriftKurs
class "Miljø" as Miljoe
class "Politiattest" as Politiattest
class "Materiell" as Materiell
class "Kursinstruktørar" as Kursinstruktoerar
class "Tandeminstruktørar" as Tandeminstruktoerar
class "Administrasjon og medlemsservice" as Administrasjon
class "Nettside/butikk" as NettsideButikk
class "Fasilitetar" as Fasilitetar
class "Reinhald og vedlikehald" as ReinhaldVedlikehald
class "Økonomi" as Oekonomi
class "Arrangement" as Arrangement

Seksjon -- FaglegLeiar
Seksjon -- Aarsmoete
FaglegLeiar -- Sikkerheitsgruppa
Sikkerheitsgruppa -- UtdanningRegelverk
Sikkerheitsgruppa -- Tandemansvarleg
Sikkerheitsgruppa -- Materialforvaltar
Sikkerheitsgruppa -- Sikkerheitsansvarleg
Sikkerheitsgruppa -- Sekretaer
Aarsmoete -- Styret
Styret -- DaglegLeiar
DaglegLeiar -- DriftKurs
DriftKurs -- Miljoe
DriftKurs -- Politiattest
DriftKurs -- Materiell
DriftKurs -- Kursinstruktoerar
DriftKurs -- Tandeminstruktoerar
DaglegLeiar -- Administrasjon
Administrasjon -- NettsideButikk
Administrasjon -- Fasilitetar
Fasilitetar -- ReinhaldVedlikehald
Administrasjon -- Oekonomi
Administrasjon -- Arrangement
```

Sjå òg [organisasjonsplanen](/organisatorisk/organisasjonsplan).

## Årshjul

### 01 Fokus: Planlegge fulldrift

- Instruktørsamling og møte SPG
- Representantar Luftsportsting
- Saker til årsmøte seksjon
- Årsmøte
- Vårdugnad
- Klubbkveld

### 02 Fokus: Gjennomføre fulldrift

- Instruktørsamling og møte for PG og tandem.
- Evaluering SPG grunnkurs
- Kjernestab planleggingsmøte
- Tryggleiksdag
- Dugnad
- Klubbkveld
- Ekstremsportveko

### 03 Fokus: Evaluering fulldrift

- Evaluering av sommarsesong
- Debrief kjernestab
- Oppfølging elevar
- Oppgjer tandem og kurs
- Medarbeidarsamtalar
- Klubbkveld

### 04 Fokus: Forbetre organisasjon

- Klubbkveld
- Planlegge neste år
- Rekneskap og budsjettering
- Strategisamling
- Dugnad: vêrstasjonar
- Vedlikehald køyretøy

## Strategisamandrag

Strategisamandraget frå presentasjonen er attgjeve nedanfor som PlantUML.

```plantuml
title Strategisamandrag
top to bottom direction
skinparam classAttributeIconSize 0
skinparam linetype ortho

class "Konsept\nOpplevtande erfaringar med luftsport" as Konsept
class "Bevis\nEi kjensle av eigarskap og tilhøyrsle" as Bevis
class "Velfungerande fasilitetar" as Fasilitetar
class "Sunn kultur" as Kultur
class "Gode kurs og oppfølging" as KursOppfoelging
class "Løfte\nAktive og nøgde pilotar" as Loefte
class "Posisjon\nEin ressurssterk klubb som er drivande for\nutviklinga av ekstremsport." as Posisjon
class "Målgruppe\nMedlemmar som vil ha det kjekt i eit fykande\nfellesskap på Voss!" as Maalgruppe
package "Kommunikasjon" {
  class "Omsynsfull" as Omsynsfull
  class "Samlande" as Samlande
  class "Nysgjerrig" as Nysgjerrig
  class "Leiken gledesspreiar" as Profil
}
package "Organisasjon" {
  class "Inkludering" as Inkludering
  class "Utvikling" as Utvikling
  class "Tryggleik" as Tryggleik
  class "Spennande moglegheiter" as Moglegheiter
}
class "Misjon\nLeggje til rette for gode opplevingar i lufta,\nog mellom menneske." as Misjon
class "Visjon\nSkapa trygg og ekte flyglede!" as Visjon

Bevis -- Fasilitetar
Bevis -- Kultur
Bevis -- KursOppfoelging
Profil -- Omsynsfull
Profil -- Samlande
Profil -- Nysgjerrig
Moglegheiter -- Inkludering
Moglegheiter -- Utvikling
Moglegheiter -- Tryggleik
```

### Konsept

Opplevtande erfaringar med luftsport

### Bevis

Ei kjensle av eigarskap og tilhøyrsle

- Velfungerande fasilitetar
- Sunn kultur
- Gode kurs og oppfølging

### Løfte

Aktive og nøgde pilotar

### Posisjon

Ein ressurssterk klubb som er drivande for utviklinga av ekstremsport.

### Målgruppe

Medlemmar som vil ha det kjekt i eit fykande fellesskap på Voss!

### Kommunikasjon

- Omsynsfull
- Samlande
- Nysgjerrig
- Leiken gledesspreiar

### Organisasjon

- Inkludering
- Utvikling
- Tryggleik
- Spennande moglegheiter

### Misjon

Leggje til rette for gode opplevingar i lufta, og mellom menneske.

### Visjon

Skapa trygg og ekte flyglede!

## Posisjon og målgruppe

Klubben skal vere til for medlemmar som vil ha det kjekt i eit fykande fellesskap på Voss!

Ein ressurssterk klubb som er drivande for utviklinga av ekstremsport.

## Visjon

Skape trygg og ekte flyglede!

## Misjon

### Kva er vår oppgåve?

Å leggje til rette for gode opplevingar i lufta, og mellom menneske.

## Verktøy

### Fokus

1. Utdanning og tryggleik: lokalt i klubb, sentralt mot seksjon og forbund.
2. Fellesskap og aktivitet: sosialt og aktivt miljø ved og utanfor flyging.
3. Organisasjon: velfungerande i sin heilheit, med gode fasilitetar og berekraftig økonomi.
4. Samarbeid: For å sikre gode rammevilkår og utvikling.
   Samarbeidspartnarar er Ekstremsportveko, Voss folkehøgskule, Voss fallskjermklubb, klubbar i seksjonen, klubbar lokalt på Voss, samt lokale aktørar.
5. Lokalmiljø: engasjert og positivt forankra rolle i nærmiljøet på Voss.
   Særleg innan saker som er viktig for idrett og miljø.

## Verdiar

### Klubbens verdiar

- Inkluderande miljø
- Utvikling
- Tryggleik

Godt forankra verdiar som pregar drifta og miljøet gir klubben ei evne til å skapa spennande moglegheiter for alle.

### Klubbens eigenskapar

- Omsynsfull
- Samlande
- Nysgjerrig

Eit typisk klubbmedlem vert skildra som ein leiken gledesspreiar.

### Våre verdiar

#### Fokus på tryggleik i alle ledd

Ta omsyn til folk, risiko, vêrforhold og lokalmiljø.

#### Inkluderande miljø

Klubben skal ha ei samlande effekt på medlemmar ved god oppfølging og variert aktivitetstilbod.

#### Utvikling

Vere nysgjerrig, ha evne til sjølvevaluering og vere mottakeleg for innspel og kritikk.

## Løfte og bevis

### Vårt løfte

Aktive og nøgde pilotar

### Bevis

- Velfungerande administrasjon og fasilitetar.
- Sunn kultur.
- Kvalitet på kurs og oppfølging.
- Årlege programplanar som vert følgd opp, samt evaluering av måloppnåing.

Gir ei kjensle av eigarskap og tilhøyrsle til klubben.
