# Geizkragen 04 🐷⚽

Handy-App mit den aktuellen Angeboten für Lebensmittel, Getränke und Drogerie in **Leverkusen** – mit Stadtteil-Auswahl, Favoriten, Einkaufszettel und Filialen mit Adresse.

## App installieren (Android)

1. Auf dem Handy die Seite **Releases** dieses Repositorys öffnen (rechts bzw. unter „Releases“).
2. Bei der neuesten Version `Geizkragen04.apk` herunterladen.
3. Die Datei öffnen. Android fragt einmalig, ob der Browser Apps installieren darf – erlauben.
4. Fertig. Bei einer neuen Version einfach die neue APK drüberinstallieren, Favoriten und Zettel bleiben erhalten.

## Wie es funktioniert

- `www/index.html` – die komplette App (eine Datei).
- `data/week.json` – die Angebote der Woche. Die App lädt diese Datei bei jedem Öffnen direkt von GitHub, neue Angebote brauchen also **keine** neue APK.
- `.github/workflows/android.yml` – baut bei jeder Änderung an der App automatisch eine neue APK und veröffentlicht sie als Release.
- Jeden Montag aktualisiert eine geplante Aufgabe `data/week.json`.

## Datenformat `data/week.json`

```json
{"from":"2026-10-19","to":"2026-10-24","updated":"2026-10-20",
 "offers":[{"id":"aldi-1","m":"aldi","n":"Storck Toffifee","br":"Storck Toffifee",
            "c":"Süßes & Snacks","p":0.99,"op":1.49,"q":125,"u":"g","b":"Toffifee",
            "from":"2026-10-19","to":"2026-10-24"}]}
```

Markt-IDs: `aldi, lidl, netto, penny, rewe, edeka, kaufland, trinkgut, hoffmann, dm, rossmann, philipps`.
