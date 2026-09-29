# Patchwork

**Generative Fill für den Mac.** Bereich im Bild markieren, beschreiben, was dort entstehen soll, und aus mehreren Versionen wählen. Man kann auch skizzieren, Referenzbilder aufs Bild legen und einblenden, das ganze Bild verändern (z. B. Tag → Nacht), das Bild über seine Ränder hinaus erweitern, Generiertes verschieben und verbiegen, Farben korrigieren und Versionen vergleichen.

- Läuft auf jedem Mac ab **macOS 13 (Ventura)**, mit Apple Silicon und Intel.
- Download ca. **0,7 MB**.
- Bildmodell: **OpenAI** (eigener API-Schlüssel, ca. 0,02 $ pro Version) oder optional **lokal und kostenlos mit ComfyUI**.
- Projekte, Bilder und dein API-Schlüssel bleiben **nur auf deinem Mac**. Patchwork hat keinen Server und sammelt keine Daten.
- **Früher hieß die App „Füllwerk“.** Wer sie schon hat, bekommt das Update wie gewohnt; Projekte, Presets und Schlüssel bleiben erhalten, und die App benennt sich beim nächsten Beenden selbst in „Patchwork“ um. Ältere Sicherungen (`.fuellwerk`) lassen sich weiter einspielen.

## Installieren – Schritt für Schritt

Das dauert etwa 3 Minuten. Du brauchst einen Mac mit **macOS 13 (Ventura) oder neuer**. Welche Version du hast, siehst du im **Apple-Menü** (oben links) → *Über diesen Mac*.

### 1. Herunterladen

1. Die Seite [**Releases → neueste Version**](../../releases/latest) öffnen.
2. Unten bei **Assets** auf **`Patchwork-1.4.3.zip`** klicken (ca. 0,7 MB). Die Datei landet in deinem Ordner **Downloads**.
   - In Safari entpackt sich die Zip-Datei oft von selbst. Dann liegt in *Downloads* schon **Patchwork** mit dem Stuhl-Symbol. Weiter bei Schritt 3.

### 2. Entpacken

1. Den **Finder** öffnen und links auf **Downloads** klicken.
2. **`Patchwork-1.4.3.zip`** doppelklicken. Daneben erscheint **Patchwork** mit dem Stuhl-Symbol.

### 3. In „Programme“ legen

1. Ein zweites Finder-Fenster öffnen (⌘N) und links auf **Programme** klicken.
2. **Patchwork** aus *Downloads* in **Programme** ziehen.
   - Fragt der Mac nach einem Passwort, gib dein Mac-Passwort ein.
   - Gibt es Patchwork dort schon (ältere Version): **Ersetzen** wählen. Deine Projekte und Einstellungen bleiben erhalten.
3. Die Zip-Datei in *Downloads* kannst du danach löschen.

### 4. Beim ersten Mal öffnen (einmalig)

Patchwork ist kostenlos und nicht über ein kostenpflichtiges Apple-Entwicklerkonto signiert. macOS fragt deshalb beim ersten Start nach. Das ist nur **einmal** nötig.

**macOS 15 (Sequoia) und neuer:**

1. In *Programme* **Patchwork** doppelklicken. Es erscheint „‚Patchwork‘ nicht geöffnet – Apple konnte nicht überprüfen …“.
2. Auf **Fertig** klicken, **nicht** „In den Papierkorb legen“.
3. Im **Apple-Menü** (oben links) → **Systemeinstellungen** → links **Datenschutz & Sicherheit** öffnen.
4. Ganz nach **unten** scrollen bis zum Abschnitt *Sicherheit*. Dort steht: „‚Patchwork‘ wurde blockiert, um deinen Mac zu schützen.“
5. Auf **Dennoch öffnen** klicken und mit Mac-Passwort oder Touch ID bestätigen.
6. Im nächsten Fenster noch einmal **Dennoch öffnen**. Patchwork startet.

**macOS 13 (Ventura) und 14 (Sonoma):**

1. In *Programme* **mit der rechten Maustaste** (oder ctrl-Klick) auf **Patchwork** klicken und **Öffnen** wählen.
2. In der Nachfrage auf **Öffnen** klicken. Patchwork startet.

Ab jetzt startet Patchwork ganz normal per Doppelklick, über das Launchpad oder über Spotlight (⌘ Leertaste, „Patchwork“).

**Tipp:** Solange Patchwork läuft, mit der rechten Maustaste auf das Symbol im **Dock** klicken und **Optionen → Im Dock behalten** wählen.

### Falls etwas nicht klappt

| Meldung / Problem | Lösung |
|---|---|
| „Patchwork ist beschädigt und kann nicht geöffnet werden“ | Die Datei hat beim Download ein Sperr-Merkmal bekommen. Das **Terminal** öffnen (Programme → Dienstprogramme), dies eingeben und Enter drücken: `xattr -dr com.apple.quarantine /Applications/Patchwork.app`. Danach normal öffnen. |
| Kein „Dennoch öffnen“ in den Systemeinstellungen | Erst einmal versuchen, Patchwork zu öffnen (Schritt 4.1). Der Knopf erscheint nur für etwa eine Stunde nach diesem Versuch. |
| „Patchwork kann auf diesem Mac nicht verwendet werden“ | Der Mac hat eine ältere macOS-Version als 13. Im Apple-Menü → *Systemeinstellungen → Allgemein → Softwareupdate* aktualisieren. |
| Fenster bleibt leer oder weiß | Patchwork beenden (⌘Q) und neu starten. Hilft das nicht: im Menü *Darstellung → Neu laden*. |
| Du findest Patchwork nicht | Spotlight (⌘ Leertaste) → „Patchwork“ eingeben. |

## Einrichten (OpenAI)

1. In Patchwork rechts **Modell** aufklappen, dann **Erweiterte Einstellungen**.
2. Auf **API-Schlüssel erstellen ↗** klicken. Die OpenAI-Seite öffnet sich im Browser.
   - Anmelden oder registrieren, dann **Create new secret key**.
   - Unter **Billing** ein Guthaben aufladen, zum Beispiel 5 $.
   - **Tipp:** Unter *Limits* ein Monatsbudget setzen.
3. Den Schlüssel in Patchwork einfügen, **merken** anhaken und auf **Schlüssel prüfen** klicken.

Unter der Qualitätsanzeige siehst du, was du diesen Monat über Patchwork ausgegeben hast. **Guthaben ansehen ↗** öffnet deinen Kontostand bei OpenAI. Ein eigenes **Monatslimit** kannst du in den erweiterten Einstellungen setzen.

## Benutzen

### Die Grundidee

1. Ein Bild ins Fenster ziehen, einfügen (⌘V) oder öffnen. Jedes Bild wird ein eigenes **Projekt**.
2. Einen Bereich auswählen (siehe Werkzeuge unten) – oder nichts auswählen, dann gilt der Prompt für das **ganze Bild**.
3. Rechts beschreiben, was passieren soll, auf **Deutsch oder Englisch** (z. B. „eine rote Bank“, „bei Nacht“). Mit Auswahl und leerem Prompt wird der Inhalt entfernt.
4. Auf **Versionen erzeugen** klicken. Die Ergebnisse erscheinen unten in der **Galerie**. Das ausgewählte Bild ist das, woran du weiterarbeitest; nochmal klicken führt zurück zum Original.

Nichts geht verloren: Jede Änderung wird eine **neue Version**, die alte bleibt in der Galerie. Gefällt etwas nicht, löschst du die neue Version mit **×**.

Kurze Erklärungen zu allen Knöpfen erscheinen, wenn du mit der Maus über das kleine **ⓘ** oder über einen Knopf fährst. **?** zeigt alle Tastenkürzel.

### Werkzeuge (links)

| Werkzeug | Taste | Wofür |
|---|---|---|
| Rechteck, Lasso, Pinsel | R, L, B | Bereich auswählen. **⌘** gedrückt: hinzufügen, **⌥**: abziehen |
| Zauberstab | W | Fläche ähnlicher Farbe per Klick auswählen (Himmel, Wand). Toleranz einstellbar |
| Skizze | S | Grob malen, was entstehen soll. **⌘** + Ziehen: gerade Linie, **⌥**: radieren |
| Objekt | O | Objekt anklicken oder benennen (nur mit ComfyUI) |
| Retusche | E | Generiertes wegradieren – oder mit **Quelle** Teile aus einer anderen Version hineinmalen |
| Schützen | P | Grün übermalen, was sich **nie** ändern darf (Gesichter, Logos, Schrift) – gilt für alle Versionen |
| Frei transformieren | V oder ⌘T | Generiertes verschieben, skalieren, drehen, mit ⌘ + Ecke perspektivisch verzerren; **Verbiegen** legt ein Gitter darüber (Doppelklick setzt einen Punkt zurück) |
| Bild erweitern | X | Ränder nach außen ziehen, die neuen Flächen werden passend ergänzt |
| Text | T | Text ins Bild schreiben und von der KI einblenden lassen oder direkt einsetzen. **Auto** entscheidet selbst, **Frei im Raum** macht 3D-Buchstaben, die vor dem Hintergrund schweben (genau an deiner Stelle, die Umgebung bleibt unverändert), **Verschmelzen** passt den Text an eine Fläche an (Wand, Schild, Bildschirm). Die Schreibweise wird danach geprüft; weicht sie ab, ist die Version markiert |

Unter den Werkzeugen: **Auswahl umkehren**, **aufheben** (⌘D) und **Auswahl verfeinern** (vergrößern, verkleinern, weiche Kante, glätten). Die Auswahl bleibt im Projekt gespeichert.

### Rund um den Prompt

- **Presets ▾:** fertige Prompts für häufige Aufgaben – Entfernen, Himmel & Licht (z. B. **Tag → Nacht**, **Nacht → Tag**), Architektur & Stadt, Produkt/Studio.
- **＋** speichert deine aktuellen Einstellungen als **eigenes Preset** (Prompt, Stil, Art der Bearbeitung, Qualität, Anzahl). Eigene Presets lassen sich im Presets-Menü **exportieren und importieren**, z. B. für Kollegen.
- **Verlauf** (Uhr-Symbol): frühere Prompts, mit ☆ als Favorit merken.
- **Verbessern:** GPT schreibt deinen Prompt konkreter, passend zum Bild (kostet ca. 0,1 Cent).
- **Stil:** gilt für jeden Prompt im Projekt, z. B. „watercolor“ oder „35mm film“.
- **Art der Bearbeitung:** *Verändern* behält, was da ist (brennt, verschneit, bei Nacht …), *Einfügen* malt Neues. *Automatisch* erkennt es aus dem Prompt.
- **Qualität:** *Günstig* (ca. 2 Cent pro Version) oder *Besser* (ca. 7 Cent). Für Änderungen am ganzen Bild ist *Besser* deutlich treuer.

### Versionen in der Galerie

- **Rechtsklick** auf eine Version:
  - Farbe markieren, als final markieren, exportieren, löschen.
  - **Mehr davon erzeugen** – gleiche Einstellungen, neue Varianten.
  - **Prompt anzeigen …** – was du eingegeben hast, was an die KI ging, Modell, Qualität, Stil.
  - **Prompt und Einstellungen übernehmen**.
  - **Details nachrechnen** – bei großen Fotos wird der neue Bereich in voller Auflösung schärfer gerechnet (fragt vorher mit Preis).
  - **Als Pinselquelle** für die Retusche.
- **Vergleichen:** 2–4 Versionen mit ⌘-Klick markieren und auf **Vergleichen** klicken. Zwei: mit Schieberegler; drei oder vier: nebeneinander, gemeinsam zoomen.
- **Baum:** Der Umschalter *Raster / Baum* zeigt, welche Version aus welcher entstanden ist. Im Baum zoomt das Mausrad, ⇧ + Ziehen oder die mittlere Maustaste verschiebt, Doppelklick auf eine freie Stelle passt ein.
- **Warteschlange:** Während eine Runde läuft, heißt der Knopf **Einreihen** – die nächste Runde wartet mit dem Stand von jetzt, du kannst sofort weiterarbeiten.

### Farbe und Export (oben)

- **Farbe:** Farbkorrektur für das ganze Projekt (wie ein Filter über allen Versionen) – oder **Nur Auswahl**, dann wird sie als neue Version übernommen.
- **Export:** PNG, JPEG, WebP oder PDF, auch mehrere Versionen auf einmal.

### Projekte

- In der **Projektübersicht** (oben *Projekte*, ⌘1) lassen sich Projekte in Ordner sortieren, duplizieren, umbenennen.
- **Sichern:** *Alles sichern* oder per Rechtsklick einzelne Projekte/Ordner als **.fuellwerk**-Datei – mit allen Versionen. **Einspielen** (oder die Datei hineinziehen) holt sie zurück, z. B. auf einem anderen Mac. Nichts wird dabei überschrieben.
- **Aufräumen …** schlägt alte Versionen ohne Farbe und ohne „Final“ vor und zeigt, wie viel Platz frei wird. Gelöscht wird erst nach deiner Bestätigung.

### Wichtigste Tastenkürzel

| | |
|---|---|
| **⌘↩** | Versionen erzeugen (während einer Runde: einreihen) |
| **Mausrad** / **⇧ + Ziehen** | Bild zoomen / verschieben (auch Leertaste + Ziehen oder mittlere Maustaste) |
| **Leertaste** halten | mit dem Ausgangsbild vergleichen |
| **⌘Z** | Auswahl, Skizze, Retusche oder Schutz rückgängig |
| **Esc** | laufende Runde abbrechen |
| **?** | alle Tastenkürzel |

### Kosten im Blick

Unter der Qualität siehst du, was du diesen Monat über Patchwork ausgegeben hast. Unter **Modell → Erweiterte Einstellungen → Monatslimit** kannst du eine Grenze setzen: Ab 80 % erscheint ein Hinweis, ab dem Limit fragt Patchwork vor jeder Runde nach.

## Optional: lokal und kostenlos mit ComfyUI

Ohne Internet und ohne Kosten, aber mit viel Speicherplatz und langsamer als OpenAI. Nur auf Macs mit Apple Silicon (M1 und neuer). Das Objekt-Werkzeug und die Bildanalyse brauchen ComfyUI.

1. In Patchwork unter **Modell** den Anbieter **ComfyUI** wählen. Alternativ auf **Einrichtung prüfen …** klicken.
2. Das **Einrichtungs-Fenster** zeigt, was fehlt, jeweils mit Dateigröße, und was schon vorhanden ist:

   | Datei | Größe | |
   |---|---|---|
   | Comfy Desktop (Programm) | 0,2 GB + ca. 3–5 GB beim ersten Start | nötig |
   | Bildmodell Realistic Vision V6 Inpainting | 2,1 GB | nötig |
   | ControlNet Scribble und Canny | je 0,7 GB | empfohlen |
   | Hyper-SD Schnell-LoRAs | 2 × 0,3 GB | empfohlen |
   | Erweiterungen Florence-2 und SAM 2 | klein, + 1,2 GB beim ersten Gebrauch | für das Objekt-Werkzeug |

3. Auf **Ausgewählte herunterladen** klicken:
   - Patchwork lädt alles von den Originalquellen (Hugging Face, GitHub, Hersteller).
   - Jedes Modell wird per Prüfsumme kontrolliert und in die richtigen ComfyUI-Ordner gelegt.
   - Die Erweiterungen werden installiert.
   - Abbrechen ist jederzeit möglich.
4. Comfy Desktop öffnet sich nach dem Download als Installationsfenster:
   - Comfy Desktop in **Programme** ziehen.
   - Einmal starten und eine Installation anlegen.
   - Zurück in Patchwork auf **Erneut prüfen** klicken und den Rest herunterladen.

Insgesamt belegt das etwa **8–12 GB**. Patchwork startet ComfyUI danach selbst im Hintergrund.

Mit ComfyUI den Prompt bitte **auf Englisch** schreiben – die lokalen Bildmodelle verstehen kein Deutsch.

## Gut zu wissen

- **Updates (ab Version 1.1 automatisch):**
  - Patchwork sieht beim Start höchstens einmal am Tag auf GitHub nach, ob es eine neue Version gibt.
  - Wenn ja, erscheint unten rechts ein Hinweis mit den Neuerungen: **Jetzt aktualisieren** oder **Später**. Ohne deinen Klick wird nichts installiert.
  - Beim Aktualisieren lädt Patchwork die neue Version, prüft ihre Prüfsumme und Echtheit, ersetzt sich selbst und startet neu. Deine Projekte, Einstellungen und dein API-Schlüssel bleiben erhalten.
  - Patchwork muss dafür im Ordner **Programme** liegen.
  - Abschalten oder von Hand suchen: **Modell → Erweiterte Einstellungen → Beim Start nach Updates suchen** bzw. **Jetzt nach Updates suchen**. Dabei sieht GitHub deine IP-Adresse.
  - **Wer noch Version 1.0 hat,** installiert die neueste Version einmal von Hand wie oben beschrieben (Schritte 1–3, beim Verschieben „Ersetzen“ wählen). Danach geht es automatisch.
- **Deinstallieren:** Patchwork in den Papierkorb legen. Wer auch die Projekte löschen will: `~/Library/WebKit/local.fuellwerk.app` löschen.
- **Kosten:** Mit OpenAI zahlst du direkt bei OpenAI, Patchwork verdient nichts daran.
- Kostenlos, **ohne Gewähr**.
- Schriften: *Roboto*, *Bebas Neue* und *Instrument Sans*, SIL Open Font License 1.1 (liegen der App bei).
