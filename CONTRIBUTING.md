# Mitarbeit in Repositories von ki|partner

Alle Factory-Repositories folgen dem Factory-Standard. Diese Seite fasst zusammen, was für jeden Beitrag gilt, ob von Menschen oder Agenten.

## Die fünf Grundregeln

1. Keine Zeile Code ohne Anforderung mit Akzeptanzkriterium.
2. Kein Merge ohne grüne Checks, Review und Nachweis.
3. Kein Release ohne Kundentest und unterschriebenes Abnahmeprotokoll.
4. Kein Fehler zweimal: Jeder Fehler wird ein Test, eine Regel oder eine Skill-Anpassung.
5. Kein Wissen nur im Kopf: Entscheide als ADR, Begriffe im Glossar, wiederkehrende Abläufe als Skill.

## Ablauf eines Beitrags

1. Jede Arbeit beginnt bei einem Issue mit Anforderungs-ID (Vorlage «Anforderung»).
2. Branch vom Default-Branch, Name `<id>-<kurzbeschreibung>`, z. B. `us-07-teileinloesung`.
3. Kleine PRs: unter 400 geänderten Zeilen. Ab 1000 Zeilen blockiert der Pflicht-Workflow.
4. Die PR-Beschreibung folgt der Vorlage: Zusammenfassung, Nachweise, Merge-Risiko, Risikoklasse, Anforderungen.
5. Merge nur per Squash, nachdem alle Checks grün sind und das Review erfolgt ist.

## Review nach Risikoklasse

| Klasse | Betrifft | Review |
| --- | --- | --- |
| A | Geld, Salden, Buchungen, Anmeldung und Rechte, Personendaten, Netzwerk, Datenbank-Migrationen | Zwei automatische Reviews, Gegenprüfung durch ein zweites Modell, immer ein Mensch; Einweg-Entscheid |
| B | Fachlogik ohne Geld oder Personendaten, Abläufe in der Oberfläche | Automatisches Review; im Pilot liest ein Mensch jeden PR |
| C | Texte, Dokumentation, Gestaltung | Automatisches Review; Mensch nach Bedarf |

## Daten und Geheimnisse

- Nie echte Kundendaten in Tests, Issues, Screenshots oder Prompts. Nur synthetische Testdaten.
- Keine Geheimnisse im Code. Secret-Scan läuft bei jedem PR.
- Agenten arbeiten ohne Zugang zu Produktionsumgebungen.

## Sprache

Deutsch (Schweiz, «ss» statt «ß») für Dokumentation, PRs, Issues und Oberflächen. Bezeichner im Code auf Englisch, Fachbegriffe wie im Glossar des Projekts.
