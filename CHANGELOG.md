# Ändringslogg

## 2026-09-25
- Statistik: varje muskelgrupp räknas bara en gång per pass, oavsett antal övningar för gruppen
- Buggfix: datumknappen öppnar nu kalendern var man än klickar (tidigare bara på texten i Chrome på dator)
- Buggfix: ett gammalt osparat utkast kunde ge ett nytt pass gårdagens datum. Utkastets datum återställs nu bara om det valts manuellt

## 2026-09-24 – Stor uppfräschning (bokmärke före: git-tagg `fore-uppfrasch-2026-09-24`)
- Ny design av passvyn: övningar visas som hopfällda kort med förra resultatet, fäll ut för att logga
- Större inmatningsrutor, förra passets värden som gråa förslag, Enter hoppar till nästa ruta
- "↺ Som förra" fyller i alla set från förra gången, PB och liten viktkurva per övning
- Egna övningar: välj muskelgrupp, typ (vikt/bara reps) och bildlänk – dyker upp i passlistan
- Redigera övningar (bild, grupp, typ, dölj) direkt från kortet eller övningsväljaren
- Sök i övningsväljaren, "Skapa" direkt från sökrutan
- Välj datum även för nya pass (logga i efterhand)
- Startsida: veckoremsa med dagens pass, "X dagar sedan" per kategori, banner för pågående pass
- Splash screen med bakgrundsbilden vid start
- Firande när ett pass sparas: konfetti/emoji-regn (varierar), uppräknade siffror, nya personbästa, roliga jämförelser (totalt lyft, förbränd energi), märken (veckor i rad, pass denna vecka, jubileer, comeback) och ett peppcitat
- Inloggningssidan borttagen – appen används bara av David
- Buggfix: Plankan m.fl. sparades som tomma 0-set varje pass
- Buggfix: redigering förstörde namn med parentes, t.ex. "Plankan (sek)"
- Buggfix: dubbeltryck på Spara skapade dubbletter
- Buggfix: fel aktivitet markerades vid redigering av cardio
- Buggfix: datum kunde hoppa en dag bakåt vid redigering (UTC)
- Buggfix: "Förra"-värden uppdaterades inte efter redigering
- Buggfix: redigerade pass kunde läcka in i nästa nya pass via utkastet
- Buggfix: tillagda övningar försvann vid omladdning mitt i passet
- Buggfix: historiken hoppade till toppen och fälldes ihop vid synk/radering
- Buggfix: svep på startsidan loggade ut användaren
- Buggfix: "Veckor i rad" visade 0 innan veckans första pass; snitt/vecka räknas från första passet

## 2026-05-13 (3)
- Footer-text och versionsnummer gjorda tydligare (större font, högre opacity)

## 2026-05-13 (2)
- Buggfix: auto-reload loopade sig själv vid lokal körning (kontrollerar nu bara version på GitHub Pages)
- Buggfix: modal-box använder nu direkt `position: fixed; bottom: 0` istället för flex-centrering, vilket fixar iOS touch-koordinatfel

## 2026-05-13
- Buggfix: egna övningar fungerar nu på mobil (touch-blockering i modal åtgärdad)
- Ny funktion: × på varje övningskort för att ta bort övning under pågående pass
- Ny funktion: egna övningar sparas nu i Firestore och synkas mellan alla enheter
- Modal för övningar döpt om till "Hantera övningar" med möjlighet att ta bort egna övningar

## 2026-04-03 (2)
- Buggfix: "Lägg till"-knappen och textfältet i modal fungerar nu korrekt på iPhone (touch-händelser blockeras från att bubbla upp till overlay)

## 2026-04-03
- Mid Cable Chest Fly tillagd som bröstövning med bild
- Inclined Hammercurls tillagd som bicepsövning i Rygg & Biceps
- Buggfix: edit-läget visade hela övningslistan istället för bara körda övningar
- Buggfix: modal för egen övning stängdes vid tryck på inputfältet på iPhone

## 2026-03-06 (3)
- Ny app-ikon (favicon + apple-touch-icon): Gemini_Generated_Image_ecnev6ecnev6ecne.png
- Borttagna oanvända filer: bg1.jpeg, bg2.jpeg, cover.jpg, favicon.jpeg, favicon.png, index_old.html, preview-filer

## 2026-03-06 (2)
- Helt ny design: bg3.jpeg som fast bakgrund, glassmorphism-stil på alla komponenter
- Inloggningssidan redesignad (Noir Glass) med Bebas Neue-typografi och teal-accenter
- Alla emojis borttagna från hela appen för ett proffsigare utseende
- Buggfix: "Senast"-datum för cardio visade fel datum

## 2026-03-06
- Cardiopass kan nu redigeras i efterhand via ✏️-knappen i historiken
- Nytt distansfält (km) på cardio-formuläret (valfritt), visas i historiken
- Kombinerade pass: lägg till cardio på styrkepass eller styrka på cardiopass
- Kombinerade pass visas som ett kort i historiken

## 2026-02-28
- Ny app-ikon och favicon baserade på cover.jpg (utan text): personen med skivstången visas som ikon

## 2026-02-27 (6)
- Kodoptimering: lyft ut TYPE_COLORS/TYPE_LABELS som globala konstanter (var duplicerade 3 gånger)
- Kodoptimering: slå ihop getExerciseType och getExerciseMuscleGroup till gemensam findExerciseInfo
- Buggfix: changeVariant kunde krascha på övningar utan viktkolumn (noWeight)
- Buggfix: XSS-risk i openLightbox – bild-URL sparas nu i data-attribut istället för inline onclick
- Buggfix: variabelshadowing i editWorkout (w skuggade sig själv)
- Prestandaförbättring: _getLastPerformed sorterar nu bara en gång + cachar resultat
- Prestandaförbättring: getPrevious cachar resultat per typ, invalideras vid dataändring

## 2026-02-27 (5)
- Swipe-to-back på iPhone: svep från vänster skärmkant för att navigera bakåt

## 2026-02-27 (4)
- Demo-användare tillagd i användarval med 72 fake-träningspass (14 veckors data)

## 2026-02-27 (3)
- Statistikfärger åtgärdade: varje muskelgrupp har nu unik kulör (Triceps=orange, Biceps=emerald, Mage=rosa etc.)
- Veckodagsstaplar uppdelade i färgsegment per muskelgrupp

## 2026-02-27 (2)
- Buggfix: statistiksidan fungerar igen – saknad funktion `getExerciseCategory` ersatt med `getExerciseType`

## 2026-02-27
- Auto-spara pågående pass: data återställs automatiskt om sidan laddas om under träning
- Lägg till övning från annan kategori: ny knapp i passvyn öppnar ett panel med alla övningar grupperade per kategori samt möjlighet att skriva eget övningsnamn
- Viktkolumnen borttagen för Plankan (sek), Sidoplanka (sek) och Hjulet

## 2026-02-25 (10)
- Buggfix: PB och förifyllda vikter fungerar nu korrekt även efter namnbyten på övningar

## 2026-02-25 (9)
- "Low cable flyes" omdöpt till "High to low cable flyes (drag curl)" (historik uppdaterad)
- "Low to high cable fly" tillagd i Bröst & Triceps med bild

## 2026-02-25 (8)
- "Good morning" omdöpt till "Hyperextensions" (historik uppdaterad, ny bild)

## 2026-02-25 (7)
- Ny bild på Good morning

## 2026-02-25 (6)
- "Made by: David Hefner" visas nu på alla sidor (fast position längst ner)

## 2026-02-25 (5)
- Ben & Rumpa tillagt som träningskategori med 9 övningar och bilder
- "Single arm cable extension" omdöpt till "Cable kickback triceps" (ny bild, historik uppdaterad)
- Papperskorgen i historiken flyttad in i expanderat pass (undviker felklick)
- Mobil-förbättringar: input-zoom fixad (16px), större kryssar, cardio 2 kolumner, statistiktext större

## 2026-02-25 (4)
- Lagt till "Made by: David Hefner" på startsidan och användarvalssidan

## 2026-02-25 (3)
- PB (personbästa) visas diskret under övningsnamnet vid träning: "PB: X kg × Y reps"

## 2026-02-25 (2)
- "Drag curl" omdöpt till "Low cable chest" (ny bild, visas med nytt namn även i historiken)
- App-ikon fixad för iPhone: PNG-fil genererad (SVG fungerar ej som hemskärmsikon på iOS)

## 2026-02-25
- Veckonummer (v.X) i stapeldiagrammet för statistiksidan
- Veckodagsfördelning (Mån–Sön) med mest aktiv dag markerad i rött
- Rolig statistik: rekordvecka, dagar i rad, favoritpass, snitt/vecka, träningstid på dygnet, längsta vila

## 2026-02-24
- App-ikon (SVG-hantel) och PWA-metadata (installerbar på mobil)
- Single arm cable extension tillagd i Triceps-gruppen

## 2026-02-23
- Low cable flyes tillagd i Bröst-gruppen
- Overhead tricep extension tillagd i Triceps-gruppen
- Övningar sorteras nu per muskelgrupp med rubriker (Bröst / Triceps, Rygg / Biceps etc.)
- Decimal-input fixad för iPhone (komma accepteras, konverteras till punkt)
- Övningar sorteras efter senast utförda (ej tränade länge sedan hamnar längst ner)
- Redigera gamla pass utan att ändra tidsstämpeln
- Historik grupperas per vecka med veckohuvuden
- Statistiksida med stapeldiagram (pass/vecka och pass/månad)

## 2026-02-20
- Klockslag visas i träningshistoriken

## 2026-02-15
- Firebase-synk i realtid mellan enheter
- Raderingsfunktion för pass i historiken
- Uppdaterade övningslistor

## 2026-02-10
- Övningsbilder för Axlar & Mage
- Övningsbilder för Rygg & Biceps

## 2026-02-05
- Användarval (David / Emma)
- Färdiga helkroppspass-program med slumpning
- Övningsbilder för Bröst & Triceps

## 2026-01-01
- Initial release: träningslogg med styrkepass och cardio
