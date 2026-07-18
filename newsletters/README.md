# Newsletter-Anleitung

Alles was du brauchst, um eine Ausgabe zu schreiben — mit Bild, mit mehreren
Bildern oder ganz ohne.

---

## 1. Neue Ausgabe anlegen

Auf GitHub im Browser, kein Programm nötig:

1. Ordner **`newsletters`** öffnen
2. Oben rechts **„Add file" → „Create new file"**
3. Dateinamen eintragen: `2026-08-01-sommerfest.md`
   - Datum vorne im Format `JAHR-MONAT-TAG`
   - danach ein Kurzname deiner Wahl
   - Endung immer `.md`
4. Text schreiben (siehe unten)
5. Unten auf **„Commit changes"** klicken

Nach ein bis zwei Minuten steht die Ausgabe auf der Webseite. Die neueste steht
ganz oben ausgeschrieben, ältere rutschen ins aufklappbare Archiv.

Ändern oder löschen geht genauso: Datei anklicken, Stift-Symbol, bearbeiten,
committen.

---

## 2. Eine Ausgabe ohne Bild

Das ist die einfachste Form:

    # Ein Sommerfest in der Kapelle

    Liebe Freunde,

    am Sonntag feiern wir im Garten hinter der Kapelle. Für Kaffee und Kuchen
    ist gesorgt.

    ## Diese Woche

    - Sonntag 9:30 Uhr Gottesdienst
    - Mittwoch 19:00 Uhr Abendgebet
    - Donnerstag Chorprobe

    Herzlich,
    **Reverend Marius**

Die Regeln kurz:

| Was du schreibst | Was rauskommt |
|---|---|
| `# Titel` | Der Titel der Ausgabe (die **erste** Zeile mit einem `#`) |
| `## Zwischenüberschrift` | Grüne Zwischenüberschrift |
| Leerzeile | Trennt Absätze |
| `- Punkt` | Aufzählung |
| `**fett**` | **fett** |
| `*kursiv*` | *kursiv* |
| `[Text](https://...)` | Ein Link |

---

## 3. Ein Bild einfügen

Das Bild muss zuerst im Ordner **`images`** liegen.

**Bild hochladen:** Ordner `images` öffnen → „Add file" → „Upload files" →
Datei hineinziehen → „Commit changes". Am besten JPG, und vorher auf etwa
1000 Pixel Breite verkleinern, sonst lädt die Seite langsam.

**Bild in den Text setzen** — in einer eigenen Zeile, mit Leerzeilen drumherum:

    Liebe Freunde,

    ![Unsere Kapelle im Sommer](../images/kapelle-sommer.jpg)

    so schön war es am vergangenen Sonntag.

Der Aufbau ist immer:

    ![Bildunterschrift](../images/dateiname.jpg)

- Das `!` am Anfang ist wichtig — ohne wird ein Link daraus statt eines Bildes.
- Der Text in den eckigen Klammern erscheint als **Bildunterschrift** unter dem
  Bild.
- In den runden Klammern steht der Pfad: **`../images/`** und der Dateiname.
  Auf **Groß- und Kleinschreibung achten**, `Foto.JPG` und `foto.jpg` sind
  verschieden.

### Warum `../images/` und nicht `images/`?

Beides funktioniert auf der Webseite. Aber mit den zwei Punkten davor zeigt
GitHub das Bild auch in der **Vorschau** an, wenn du die Datei bearbeitest
(Reiter „Preview"). Ohne die Punkte siehst du dort nur ein kaputtes Bildsymbol,
obwohl auf der Webseite alles stimmt — GitHub sucht das Bild dann nämlich im
Ordner `newsletters/`, wo es nicht liegt.

Kurz: **`../images/` benutzen**, dann kannst du vorab kontrollieren, ob alles
richtig sitzt.

### Bild ohne Unterschrift

Eckige Klammern einfach leer lassen:

    ![](../images/kapelle-sommer.jpg)

---

## 4. Mehrere Bilder

**Nebeneinander:** mehrere Bildzeilen **direkt untereinander**, ohne Leerzeile
dazwischen:

    ![Der Chor](../images/chor.jpg)
    ![Das Buffet](../images/buffet.jpg)

Die beiden stehen dann nebeneinander. Auf dem Handy rutschen sie automatisch
untereinander.

**Untereinander:** eine Leerzeile zwischen die Bildzeilen setzen:

    ![Der Chor](../images/chor.jpg)

    ![Das Buffet](../images/buffet.jpg)

Merksatz: **keine Leerzeile = nebeneinander, Leerzeile = untereinander.**

Mehr als zwei bis drei nebeneinander wird schnell klein — dann lieber
untereinander.

---

## 5. Ausgabe im Voraus schreiben und terminieren

Eine `publish:`-Zeile ganz oben in die Datei:

    publish: 2026-08-01 09:00

    # Ein Sommerfest in der Kapelle

    Liebe Freunde, ...

Die Ausgabe erscheint dann erst am 1. August um 9:00 Uhr. Format `HH:MM` in
24-Stunden-Schreibweise. Uhrzeit weglassen (`publish: 2026-08-01`) heißt
Mitternacht. Ohne `publish:`-Zeile gilt das Datum aus dem Dateinamen.

Die `publish:`-Zeile wird beim Anzeigen entfernt, sie steht nicht im Newsletter.

Du kannst mehrere Wochen im Voraus schreiben und alle auf einmal hochladen —
jede Ausgabe geht zu ihrem eigenen Termin raus.

### Zeitzone

Welche Uhrzeit gemeint ist, steht in **`newsletters/timezone.txt`**. Dort steht:

    America/Detroit

Das ist Michigan-Zeit (Eastern Time), Sommer- und Winterzeit automatisch. Du
schreibst die Zeiten also so, wie die Uhr bei dir an der Wand steht.

Zum Umstellen die Datei bearbeiten, zum Beispiel `Europe/Berlin`,
`America/New_York`, `America/Chicago` oder `America/Los_Angeles`. Nur ein Name
pro Datei. Bei einem Tippfehler wird wieder Michigan-Zeit benutzt und eine
Warnung ins Protokoll geschrieben.

### Zwei Einschränkungen

- **Nicht minutengenau.** GitHub startet die Zeitsteuerung mit Verzögerung.
  Rechne mit etwa 15–30 Minuten nach der angegebenen Zeit. Für „Sonntagfrüh"
  reicht das, für „Punkt 12:00" nicht.
- **Nicht geheim.** Das Repo ist öffentlich, eine vorbereitete Ausgabe kann
  jeder in diesem Ordner lesen, bevor sie auf der Webseite erscheint. Soll eine
  Ausgabe vorher wirklich niemand sehen, lade sie erst am Tag selbst hoch.

---

## 6. Per E-Mail verschicken

Die Webseite verschickt **nichts** von selbst. Du schickst den Newsletter selbst
aus deinem E-Mail-Programm.

**Wichtig:** die Adressen der Abonnenten immer ins **Bcc**-Feld setzen, niemals
in „An" oder „Cc". Sonst sieht jeder Empfänger die Adressen aller anderen.

Anmeldungen kommen als einzelne E-Mail bei dir an (Betreff `NEWSLETTER SIGNUP`).
Trage sie in deine Google-Kontaktgruppe „Newsletter" ein, dann kannst du beim
Schreiben einfach den Gruppennamen ins Bcc-Feld tippen.

---

## 7. Wenn etwas nicht klappt

Im Repo unter **Actions → Build Newsletter Index** steht beim letzten Lauf,
was passiert ist:

- `Published 3 issue(s)` — so viele Ausgaben sind sichtbar
- `waiting: ... (due ...)` — diese Ausgabe wartet noch auf ihren Termin
- `Skipping ...: filename must be YYYY-MM-DD-name.md` — der Dateiname stimmt
  nicht
- `Skipping image with unsupported path` — der Bildpfad ist nicht erlaubt

**Ausgabe erscheint nicht?** Meist stimmt der Dateiname nicht (Datum fehlt oder
Endung ist nicht `.md`), oder der `publish:`-Termin liegt noch in der Zukunft.

**Bild wird nicht angezeigt?** Prüfe, ob die Datei wirklich im Ordner `images`
liegt und ob der Name im Text **exakt** gleich geschrieben ist, inklusive
Groß- und Kleinschreibung und Endung (`.jpg`, `.jpeg` oder `.png`).

**Bild fehlt nur in der GitHub-Vorschau?** Dann steht wahrscheinlich `images/`
statt `../images/` im Text. Auf der Webseite erscheint es trotzdem richtig —
aber mit `../` davor siehst du es auch in der Vorschau.

**Statt des Bildes steht Text da?** Dann fehlt das `!` am Zeilenanfang.
