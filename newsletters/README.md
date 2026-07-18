# Newsletter-Ausgaben

## Neue Ausgabe schreiben

Neue Datei in diesem Ordner anlegen, Dateiname immer so:

    JAHR-MONAT-TAG-kurzer-name.md

Zum Beispiel `2026-08-01-sommerfest.md`. Das Datum im Dateinamen bestimmt die
Reihenfolge auf der Webseite (neueste oben).

Aufbau der Datei:

    # Titel der Ausgabe

    Der erste Absatz.

    Der zweite Absatz. Eine Leerzeile trennt Absätze.

    ## Eine Zwischenüberschrift

    - Ein Aufzählungspunkt
    - Noch einer

    Man kann **fett** und *kursiv* schreiben und [Links setzen](https://example.com).

Die erste Zeile mit `#` ist der Titel. Alles danach ist der Text.

Sobald die Datei auf GitHub liegt, baut ein Workflow die Übersicht automatisch
neu und die Ausgabe erscheint auf der Newsletter-Seite. Das dauert etwa eine
Minute.

## Ausgabe im Voraus schreiben und zu einem Termin veröffentlichen

Schreibe eine `publish:`-Zeile an den Anfang der Datei:

    publish: 2026-08-01 09:00

    # Titel der Ausgabe

    Der Text ...

Die Ausgabe erscheint dann erst am 1. August um 9:00 Uhr auf der Webseite.
Uhrzeit ist immer **deutsche Zeit** (Europe/Berlin), im Format `HH:MM` in
24-Stunden-Schreibweise. Die Uhrzeit kann man weglassen (`publish: 2026-08-01`),
dann erscheint sie um Mitternacht.

Ohne `publish:`-Zeile gilt das Datum aus dem Dateinamen, also sofort sobald
dieses Datum erreicht ist.

Die `publish:`-Zeile wird beim Anzeigen automatisch entfernt, sie steht also
nicht im Newsletter.

**Zwei Dinge dazu:**

- GitHub führt die Zeitsteuerung **nicht auf die Minute genau** aus. Rechne
  damit, dass die Ausgabe etwa 15–30 Minuten nach der angegebenen Zeit
  erscheint. Für „Sonntag früh" reicht das, für „Punkt 12:00" nicht.
- Das Repo ist öffentlich. Eine vorbereitete Ausgabe kann also jeder im Ordner
  `newsletters/` lesen, **bevor** sie auf der Webseite erscheint. Die
  Zeitsteuerung regelt die Anzeige, nicht die Geheimhaltung. Wenn eine Ausgabe
  wirklich vorher niemand sehen darf, lade sie erst am Tag selbst hoch.

Prüfen kann man das jederzeit: im Repo unter **Actions → Build Newsletter
Index** zeigt der letzte Lauf an, welche Ausgaben veröffentlicht sind und
welche noch warten (`waiting: ... (due ...)`).

## Per E-Mail verschicken

Die Webseite verschickt **nichts** von selbst. Du schickst den Newsletter selbst
aus deinem E-Mail-Programm.

**Wichtig:** die Adressen der Abonnenten immer ins **Bcc**-Feld setzen, niemals
in "An" oder "Cc". Sonst sieht jeder Empfänger die Adressen aller anderen.

Anmeldungen kommen als einzelne E-Mail bei dir an. Trage sie in deine
Google-Kontaktgruppe "Newsletter" ein, dann kannst du beim Schreiben einfach
den Gruppennamen ins Bcc-Feld tippen.
