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

class "Seksjon" as Seksjon <<organisasjonsledd>>
class "Fagleg leiar" as FaglegLeiar <<rolle>>
class "Sikkerheitsgruppa" as Sikkerheitsgruppa <<gruppe>>
class "Utdanningsansvarleg og regelverk" as UtdanningRegelverk <<rolle>>
class "Tandemansvarleg" as Tandemansvarleg <<rolle>>
class "Materialforvaltar" as Materialforvaltar <<rolle>>
class "Sikkerheitsansvarleg\nKan vere ein tilsett." as Sikkerheitsansvarleg <<rolle>>
class "Sekretær\nKan vere ein tilsett." as Sekretaer <<rolle>>
class "Årsmøte" as Aarsmoete <<organisasjonsledd>>
class "Styret" as Styret <<organisasjonsledd>>
class "Dagleg leiar" as DaglegLeiar <<rolle>>
class "Driftsansvarleg og kurskoordinator" as DriftKurs <<rolle>>
class "Miljø" as Miljoe <<ansvar>>
class "Politiattest" as Politiattest <<ansvar>>
class "Materiell" as Materiell <<ansvar>>
class "Kursinstruktørar" as Kursinstruktoerar <<rolle>>
class "Tandeminstruktørar" as Tandeminstruktoerar <<rolle>>
class "Administrasjon og medlemsservice" as Administrasjon <<funksjon>>
class "Nettside/butikk" as NettsideButikk <<funksjon>>
class "Fasilitetar" as Fasilitetar <<funksjon>>
class "Reinhald og vedlikehald" as ReinhaldVedlikehald <<funksjon>>
class "Økonomi" as Oekonomi <<funksjon>>
class "Arrangement" as Arrangement <<funksjon>>

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

class "Konsept\nOpplevtande erfaringar med luftsport" as Konsept <<strategi>>
class "Bevis\nEi kjensle av eigarskap og tilhøyrsle" as Bevis <<strategi>>
class "Velfungerande fasilitetar" as Fasilitetar <<bevis>>
class "Sunn kultur" as Kultur <<bevis>>
class "Gode kurs og oppfølging" as KursOppfoelging <<bevis>>
class "Løfte\nAktive og nøgde pilotar" as Loefte <<strategi>>
class "Posisjon\nEin ressurssterk klubb som er drivande for\nutviklinga av ekstremsport." as Posisjon <<strategi>>
class "Målgruppe\nMedlemmar som vil ha det kjekt i eit fykande\nfellesskap på Voss!" as Maalgruppe <<strategi>>
package "Kommunikasjon" {
  class "Omsynsfull" as Omsynsfull <<eigenskap>>
  class "Samlande" as Samlande <<eigenskap>>
  class "Nysgjerrig" as Nysgjerrig <<eigenskap>>
  class "Leiken gledesspreiar" as Profil <<klubbmedlem>>
}
package "Organisasjon" {
  class "Inkludering" as Inkludering <<verdi>>
  class "Utvikling" as Utvikling <<verdi>>
  class "Tryggleik" as Tryggleik <<verdi>>
  class "Spennande moglegheiter" as Moglegheiter <<resultat>>
}
class "Misjon\nLeggje til rette for gode opplevingar i lufta,\nog mellom menneske." as Misjon <<strategi>>
class "Visjon\nSkapa trygg og ekte flyglede!" as Visjon <<strategi>>

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
