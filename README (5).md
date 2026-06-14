# De interdisciplinaire tafel

Een onderwijstool waarin een student een dilemma voorlegt aan drie experts uit
verschillende disciplines. De experts debatteren erover — vanuit hun eigen vakgebied,
met elkaar oneens — en betrekken de student als vierde aan tafel bij het gesprek.
Het doel is dat de student leert verschillende perspectieven te wegen in plaats van
één "juist" antwoord te zoeken.

De hele app is één HTML-bestand zonder server of installatie; je opent het gewoon
in je browser.

## Hoe gebruik je het?

1. **Zet je tafel.** Kies je eigen vakgebied en drie experts uit andere disciplines.
   Alle vier de vakgebieden moeten van elkaar verschillen, zodat de perspectieven echt botsen.
2. **Kies hoeveel bijdragen** elke expert per ronde inbrengt (1 = kort en bondig,
   3 = uitgebreid debat).
3. **Voer een dilemma in.** De drie experts reageren om de beurt, spreken elkaar bij
   naam aan en sluiten af met een vraag aan jou.
4. **Reageer** zo vaak je wilt; het gesprek bouwt door.
5. **Exporteer naar Word** om het volledige gesprek als verslag te bewaren of in te
   leveren. Het verslag bevat de deelnemers, het dilemma, het gesprek en een blok
   reflectievragen.

## Welke tools zijn gebruikt?

De app is bewust eenvoudig en zelfstandig opgebouwd:

- **Claude (Anthropic)** — het taalmodel `claude-sonnet-4-6`, aangeroepen via de
  Anthropic Messages API, genereert het debat. Dit is het enige onderdeel dat een
  internetverbinding nodig heeft.
- **HTML, CSS en JavaScript** — puur en zonder frameworks. Eén bestand, geen
  backend, geen build-stap, geen externe code-afhankelijkheden.
- **Micah-avatars** — de drie experts worden getekend met de stijl **Micah** van
  Micah Lanier (CC BY 4.0), gegenereerd met **DiceBear** (MIT-licentie). De figuren
  zijn vooraf gegenereerd en als SVG vast in het bestand opgenomen, dus er is géén
  externe API-aanroep tijdens het gebruik. Het zijn getekende personages, geen echte
  gezichten — dus geen portret- of gelijkenisrechten. Omdat Micah onder CC BY 4.0
  valt, staat er een bronvermelding onderaan de app (verplicht bij deze licentie).
- **Met de hand getekende SVG-decor** — de kamer, het raam, de planten, de tafel en
  de stoel zijn volledig in code getekend (geen foto's of externe afbeeldingen).
- **UU-huisstijl** — lettertypen Merriweather en Open Sans (via Google Fonts) en de
  officiële UU-kleuren (geel `#FFD200`, donkerblauw `#001240`) met het accentpalet.
- **Web Speech API** — de ingebouwde spraakfunctie van de browser, optioneel, om de
  experts hardop te laten spreken.
- **Word-export** — wordt in de browser opgebouwd als een Word-compatibel
  HTML-document (`.doc`), zonder externe bibliotheek.

> De avatars gebruiken nu de Micah-stijl. Wil je realistischer, dan kom je bij
> fotorealistische (synthetische) gezichten of 3D-avatars — die vragen een externe
> dienst of vaste beeldbestanden en vallen buiten deze self-contained opzet.

## Privacy

- Wat je intypt (je dilemma en je reacties) wordt naar **Claude van Anthropic**
  gestuurd om het antwoord te genereren. Dat is nodig om de app te laten werken.
- De app heeft **geen eigen server** en bewaart zelf **niets**. Je gesprek leeft
  alleen in je browser en verdwijnt zodra je de pagina sluit — behalve het
  Word-verslag dat je zelf downloadt.
- **Voer geen bijzondere of tot personen herleidbare gegevens in.** De verwerking bij
  Anthropic valt onder hun privacybeleid: <https://www.anthropic.com/legal/privacy>.
- De experts zijn door AI gegenereerde personages. Ze kunnen zich vergissen of
  stellig klinken zonder gelijk te hebben — toets hun beweringen altijd kritisch.

## Licentie en hergebruik

De code en het decor in dit bestand zijn voor dit onderwijsproject gemaakt en
vrij aan te passen. De avatars zijn gemaakt met de **Micah**-stijl (Micah Lanier,
**CC BY 4.0 — attributie verplicht**, vandaar de bronvermelding in de app) via
**DiceBear** (MIT-licentie). De
lettertypen vallen onder de Open Font License (Google Fonts). Het officiële UU-logo
is hier niet ingesloten; voor productie plaats je dat zelf volgens de
UU-huisstijlrichtlijnen.
