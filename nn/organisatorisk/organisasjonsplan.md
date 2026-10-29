# Organisasjonsplan

Kjelde: Organisasjonsplan for Voss Hang- og Paragliderklubb, vedteke av årsmøtet 27.02.2025.

## Organisasjonskart

Organisasjonskartet i kjelda er attgjeve nedanfor som PlantUML.

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

Det same organisasjonskartet står òg i [styringsdokumentet](/organisatorisk/styringsdokument).

## Kjønnsfordeling

I samsvar med idrettslaget si lov § 5 skal begge kjønn vere representert i styret, råd og utval.
Det skal vere minst to representantar frå kvart kjønn i styret og eventuelle komitear med meir enn tre medlemmar.

## Årsmøtet

Årsmøtet er klubbens øvste myndigheit og blir halde kvart år i februar.
Oppgåver og reglar for årsmøtet følgjer idrettslaget si lov, spesielt § 13–17.

### Stemmerett og valbarheit

For å kunne stemme og vere valbar må medlemmet:

- Ha fylt 15 år
- Ha vore medlem i klubben i minst éin månad
- Ha betalt kontingent

Protokoll frå årsmøtet blir publisert på klubben si heimeside.

## Styret

Styret er klubbens øvste myndigheit mellom årsmøta.

### Lovpålagte oppgåver for styret

- Iverksetje vedtak frå årsmøtet og overordna organisasjonsledd
- Sikre forsvarleg økonomistyring og disponering av midlar
- Oppnemne komitear, utval eller personar for spesielle oppgåver
- Representere idrettslaget eksternt
- Oppnemne ansvarleg for politiattestordninga
- Oppnemne ansvarleg for barneidrett

### Andre viktige oppgåver

- Planleggje og styre klubbens totale drift
- Utarbeide strategi- og budsjettplan
- Sikre at klubbens aktivitetar følgjer idrettens retningslinjer
- Vere arbeidsgivar for eventuelle tilsette
- Sikre at økonomiske disposisjonar følgjer vedtak og retningslinjer
- Oppdatere klubbhandboka

### Fordeling av oppgåver i styret

Styremedlemmar kan veljast til spesifikke oppgåver (t.d. kasserar, sekretær) på årsmøtet, eller styret kan sjølv fordele oppgåvene internt etter konstituering.

## Styret sitt arbeid

Styremøter blir normalt halde éin gong per månad i klubbhuset på Bømoen eller digitalt.
Styret er vedtaksført når fleirtalet av styremedlemmane er til stades.

- Protokoll blir ført frå alle styremøte
- Spørsmål om habilitet skal behandlast i starten av kvart møte
- Ved stemmelikskap har leiar si stemme avgjerande betyding

## Utval og komitear

### Valkomite

Valkomiteen har ansvar for å finne eigna kandidatar til styret og sikre kontinuitet i klubbdrifta.

### Kontrollutval

Kontrollutvalet skal vurdere klubbens økonomi og sikre at rekneskap blir ført i samsvar med reglane.

### Fagleg leiar og sikkerheitsgruppa

Henta frå Sikkerheitssystemet kap. 2.4.2.

#### Fagleg leiar i Voss Hang- og Paragliderklubb

Den faglege leiaren i klubben har ansvar for følgjande:

- Klubbens system for sikkerheits- og utdanningsarbeid.
- At klubben opererer i tråd med sikkerheitssystemet.
- At faglege og sikkerheitsrelaterte saker frå NLF/HPS sin fagsjef blir kommuniserte til klubbens medlemmer.
- At faglege og sikkerheitsrelaterte saker blir kommuniserte frå klubben til NLF/HPS sin fagsjef.
- Å informere klubbens styre og fagpersonell om forhold som vedkjem deira ansvarsområde.
- At det blir arrangert eit årleg sikkerheitsmøte for klubbens medlemmer.
- Å følgje opp klubbens instruktørar.
- At klubben rekrutterer nye instruktørkandidatar ved å sikre at det blir utdanna hjelpeinstruktørar i klubben.
- Årleg godkjenning av klubbens instruktørar og tandemflygarar.

Den faglege leiaren skal delta på NLF/HPS sitt leiarseminar minst annakvart år.

#### Faglege funksjonar i klubben

Klubben skal ha følgjande faglege funksjonar under den faglege leiaren, med tilhøyrande stillingsskildringar:

- Utdanningsansvarleg, dersom klubben driv utdanning.
- Sikkerheitsansvarleg
- Regelverksansvarleg
- Miljøansvarleg
- Politiattestansvarleg

Den faglege leiaren kan inneha alle desse funksjonane, føresett at han/ho har nødvendig kompetanse, eller delegere dei til andre.
I praksis fungerar dette ved sikkerheitsgruppa som vert nedsett av fagleg leiar.

Miljøansvarleg skal sette seg inn i NLF sin miljøinstruks og kommunisere med NLF sitt miljøutval ved behov.
Miljøspørsmål innan hang-, para- eller speedgliding kan omfatte:

- Omsyn til dyreliv og fauna på flystadene våre.
- Støyproblem dersom klubben har aktive utøvarar som flyr med motor.
- Problemstillingar knytt til grunneigarar og bruken av flystadene.

Eit arkiv med oversikt over personar som til ei kvar tid har dei ulike fagfunksjonane i klubben skal vere tilgjengeleg.

## Dagleg leiar

Stilling: Fast tilsett dagleg leiar

### Ansvarsområde

- Dagleg drift av klubben
- Økonomistyring og budsjettoppfølging
- Marknadsføring og medlemshandsaming
- Oppfølging av kurs og instruktørverksemd
- Koordinering av dugnadsarbeid

## Kurs- og instruktørar

Ansvar for gjennomføring av kurs, instruktørgodkjenning og oppfølging av sikkerheitsprosedyrar.

## Teknisk ansvar

Ansvarleg for vedlikehald og investeringar knytt til:

- Redningsbåtar
- Startplassar
- Klubbhus og klubbvogn

## Sosial- og arrangementskomité

Ansvar for sosiale arrangement, inkludert Ekstremsportveko, Påskeflytreff, samlingar og klubbturar.

Arbeidsinstruks DL: Utarbeidd av styret og dagleg leiar.

## Revisjon av organisasjonsplanen

Organisasjonsplanen skal handsamast av årsmøtet og kan berre endrast av årsmøtet.

## Relaterte sider

- [Styringsdokument](/organisatorisk/styringsdokument)
- [Dagleg leiar](/dagleg-leiar/dagleg-leiar)
