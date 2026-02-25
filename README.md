# Träningslogg

En mobilanpassad träningslogg-app byggd som en enda HTML-fil. Spårar styrkepass och cardio, synkroniserar data via Firebase och visar statistik.

**Live:** https://vg1414.github.io/traning/

## Funktioner

- **Styrkepass** – Bröst & Triceps, Rygg & Biceps, Axlar & Mage med övningar sorterade per muskelgrupp
- **Cardio** – Cykel, promenad, crosstrainer med tid och kcal
- **Helkroppspass** – Slumpmässiga färdiga program med svårighetsgrad
- **Förra passets vikter** visas som referens när du loggar
- **Redigera gamla pass** – Lägg till glömda övningar utan att ändra tidsstämpeln
- **Historik** – Alla pass i omvänd ordning, grupperade per vecka
- **Statistik** – Stapeldiagram per vecka/månad, veckodagsfördelning, rekordvecka, dagar i rad m.m.
- **Firebase-synk** – Realtidssynk mellan enheter, två profiler (David / Emma)
- **Offline-stöd** – Fungerar utan internet via Firebase persistence

## Teknik

- Vanilla HTML/CSS/JavaScript – inga ramverk
- Firebase Firestore för molnsynk
- localStorage som fallback
- PWA-metadata (installerbar på mobil)

## Träningskategorier

| Pass | Färg |
|---|---|
| Bröst & Triceps | Röd |
| Rygg & Biceps | Blå |
| Axlar & Mage | Lila |
| Cardio | Grön |
| Ben & Rumpa | Orange |
| Helkropp | Gul |
