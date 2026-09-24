# Träningslogg

En mobilanpassad träningslogg-app byggd som en enda HTML-fil. Spårar styrkepass och cardio, synkroniserar data via Firebase och visar statistik.

**Live:** https://vg1414.github.io/traning/

## Funktioner

- **Styrkepass** – Bröst & Triceps, Rygg & Biceps, Axlar & Mage, Ben & Rumpa. Övningarna visas som hopfällda kort (senast gjorda överst) med förra resultatet – fäll ut och logga
- **Snabb loggning** – förra passets vikter/reps som gråa förslag, Enter hoppar till nästa ruta, "↺ Som förra" fyller i allt
- **PB och viktkurva** per övning
- **Egna övningar** – skapa med namn, muskelgrupp, typ (vikt eller bara reps/sek) och bildlänk. Redigera eller dölj även inbyggda övningar
- **Cardio** – Cykel, promenad, crosstrainer med tid, kcal och km (kan kombineras med styrka)
- **Helkroppspass** – slumpade färdiga program med svårighetsgrad
- **Välj datum** – logga pass i efterhand
- **Pågående pass sparas automatiskt** och kan återupptas från startsidan
- **Historik** – grupperad per vecka, redigera och ta bort pass
- **Statistik** – veckor i rad, rekordvecka, fördelning per muskelgrupp, diagram per vecka/månad/veckodag
- **Firande vid sparat pass** – konfetti, personbästa, roliga jämförelser, veckor i rad och jubileer
- **Firebase-synk** – realtidssynk mellan enheter, fungerar offline

## Teknik

- Vanilla HTML/CSS/JavaScript – inga ramverk
- Firebase Firestore (`users/david/workouts`, egna övningar i `global/custom_exercises`)
- PWA-metadata (installerbar på mobil)

## Återgå till tidigare version

Versionen före uppfräschningen 2026-09-24 finns som git-taggen `fore-uppfrasch-2026-09-24`.

## Träningskategorier

| Pass | Färg |
|---|---|
| Bröst & Triceps | Röd |
| Rygg & Biceps | Blå |
| Axlar & Mage | Lila |
| Cardio | Grön |
| Ben & Rumpa | Orange |
| Helkropp | Gul |
