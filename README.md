# Familien-Adventskalender 2026

Ein Türchen pro Tag für die ganze Familie. Fragen, Fotos, Aufgaben und Schätzfragen werden in der WhatsApp-Gruppe beantwortet. Das Quiz und die Rangliste laufen in der App.

- **Kalender:** https://robbykev.github.io/Adventskalender/
- **Vorschau zum Testen (Countdown und Kalender umschaltbar):** https://robbykev.github.io/Adventskalender/?vorschau=1

## Punkte

- Quiz richtig beantwortet: 1 Punkt
- Foto, Frage oder Aufgabe als erledigt markiert: 1 Punkt (auch die Überraschungen vor dem 1.12.)
- Gedanken: keine Punkte
- Bei Gleichstand liegt vorne, wer öfter dabei war

Am 24.12. erscheint über der Rangliste die Siegerehrung.

## Als App speichern

Unten in der App gibt es den Knopf „Als App speichern“ mit der Anleitung für iPhone und Android.

## Firebase (für die gemeinsame Rangliste)

1. Firebase-Projekt anlegen und die **Realtime Database** aktivieren.
2. Eine Web-App registrieren und die Config in `index.html` bei `FIREBASE_CONFIG` eintragen.
3. Die Datenbank-Regeln so setzen:

```json
{
  "rules": {
    "advent2026": { ".read": true, ".write": true }
  }
}
```

Ohne Config läuft alles nur lokal auf dem jeweiligen Handy. Im Vorschau-Modus (`?vorschau=1`) wird nie in die Datenbank geschrieben.

## Inhalte ändern

Die Texte stehen in `index.html` in der Liste `TAGE`.
