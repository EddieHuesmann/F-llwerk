# Füllwerk

**Generative Fill für den Mac.** Bereich im Bild markieren, beschreiben, was dort entstehen soll, und aus mehreren Versionen wählen. Man kann auch skizzieren, Referenzbilder aufs Bild legen und einblenden, Farben ersetzen und Generiertes wieder wegradieren.

- Läuft auf jedem Mac ab **macOS 13 (Ventura)**, mit Apple Silicon und Intel.
- Download ca. **0,5 MB**.
- Bildmodell: **OpenAI** (eigener API-Schlüssel, ca. 0,02 $ pro Version) oder optional **lokal und kostenlos mit ComfyUI**.
- Projekte, Bilder und dein API-Schlüssel bleiben **nur auf deinem Mac**. Füllwerk hat keinen Server und sammelt keine Daten.

## Installieren – Schritt für Schritt

Das dauert etwa 3 Minuten. Du brauchst einen Mac mit **macOS 13 (Ventura) oder neuer**. Welche Version du hast, siehst du im **Apple-Menü** (oben links) → *Über diesen Mac*.

### 1. Herunterladen

1. Die Seite [**Releases → neueste Version**](../../releases/latest) öffnen.
2. Unten bei **Assets** auf **`Fuellwerk-1.2.zip`** klicken (ca. 0,5 MB). Die Datei landet in deinem Ordner **Downloads**.
   - In Safari entpackt sich die Zip-Datei oft von selbst. Dann liegt in *Downloads* schon **Füllwerk** mit dem Stuhl-Symbol. Weiter bei Schritt 3.

### 2. Entpacken

1. Den **Finder** öffnen und links auf **Downloads** klicken.
2. **`Fuellwerk-1.2.zip`** doppelklicken. Daneben erscheint **Füllwerk** mit dem Stuhl-Symbol.

### 3. In „Programme“ legen

1. Ein zweites Finder-Fenster öffnen (⌘N) und links auf **Programme** klicken.
2. **Füllwerk** aus *Downloads* in **Programme** ziehen.
   - Fragt der Mac nach einem Passwort, gib dein Mac-Passwort ein.
   - Gibt es Füllwerk dort schon (ältere Version): **Ersetzen** wählen. Deine Projekte und Einstellungen bleiben erhalten.
3. Die Zip-Datei in *Downloads* kannst du danach löschen.

### 4. Beim ersten Mal öffnen (einmalig)

Füllwerk ist kostenlos und nicht über ein kostenpflichtiges Apple-Entwicklerkonto signiert. macOS fragt deshalb beim ersten Start nach. Das ist nur **einmal** nötig.

**macOS 15 (Sequoia) und neuer:**

1. In *Programme* **Füllwerk** doppelklicken. Es erscheint „‚Füllwerk‘ nicht geöffnet – Apple konnte nicht überprüfen …“.
2. Auf **Fertig** klicken, **nicht** „In den Papierkorb legen“.
3. Im **Apple-Menü** (oben links) → **Systemeinstellungen** → links **Datenschutz & Sicherheit** öffnen.
4. Ganz nach **unten** scrollen bis zum Abschnitt *Sicherheit*. Dort steht: „‚Füllwerk‘ wurde blockiert, um deinen Mac zu schützen.“
5. Auf **Dennoch öffnen** klicken und mit Mac-Passwort oder Touch ID bestätigen.
6. Im nächsten Fenster noch einmal **Dennoch öffnen**. Füllwerk startet.

**macOS 13 (Ventura) und 14 (Sonoma):**

1. In *Programme* **mit der rechten Maustaste** (oder ctrl-Klick) auf **Füllwerk** klicken und **Öffnen** wählen.
2. In der Nachfrage auf **Öffnen** klicken. Füllwerk startet.

Ab jetzt startet Füllwerk ganz normal per Doppelklick, über das Launchpad oder über Spotlight (⌘ Leertaste, „Füllwerk“).

**Tipp:** Solange Füllwerk läuft, mit der rechten Maustaste auf das Symbol im **Dock** klicken und **Optionen → Im Dock behalten** wählen.

### Falls etwas nicht klappt

| Meldung / Problem | Lösung |
|---|---|
| „Füllwerk ist beschädigt und kann nicht geöffnet werden“ | Die Datei hat beim Download ein Sperr-Merkmal bekommen. Das **Terminal** öffnen (Programme → Dienstprogramme), dies eingeben und Enter drücken: `xattr -dr com.apple.quarantine /Applications/Füllwerk.app`. Danach normal öffnen. |
| Kein „Dennoch öffnen“ in den Systemeinstellungen | Erst einmal versuchen, Füllwerk zu öffnen (Schritt 4.1). Der Knopf erscheint nur für etwa eine Stunde nach diesem Versuch. |
| „Füllwerk kann auf diesem Mac nicht verwendet werden“ | Der Mac hat eine ältere macOS-Version als 13. Im Apple-Menü → *Systemeinstellungen → Allgemein → Softwareupdate* aktualisieren. |
| Fenster bleibt leer oder weiß | Füllwerk beenden (⌘Q) und neu starten. Hilft das nicht: im Menü *Darstellung → Neu laden*. |
| Du findest Füllwerk nicht | Spotlight (⌘ Leertaste) → „Füllwerk“ eingeben. |

## Einrichten (OpenAI)

1. In Füllwerk rechts **Modell** aufklappen, dann **Erweiterte Einstellungen**.
2. Auf **API-Schlüssel erstellen ↗** klicken. Die OpenAI-Seite öffnet sich im Browser.
   - Anmelden oder registrieren, dann **Create new secret key**.
   - Unter **Billing** ein Guthaben aufladen, zum Beispiel 5 $.
   - **Tipp:** Unter *Limits* ein Monatsbudget setzen.
3. Den Schlüssel in Füllwerk einfügen, **merken** anhaken und auf **Schlüssel prüfen** klicken.

Unter der Qualitätsanzeige siehst du, was du diesen Monat über Füllwerk ausgegeben hast. **Guthaben ansehen ↗** öffnet deinen Kontostand bei OpenAI.

## Benutzen

1. Ein Bild ins Fenster ziehen, einfügen (⌘V) oder öffnen. Jedes Bild wird ein eigenes **Projekt** (Liste links).
2. Einen Bereich markieren: Rechteck (R), Lasso (L), Pinsel (B) oder Objekt (O, nur mit ComfyUI). Alternativ skizzieren (S).
3. Rechts beschreiben, was im Bereich passieren soll, **auf Englisch** (z. B. „a red bench“). Leer lassen heißt entfernen.
4. Auf **Versionen erzeugen** klicken.
5. Die Ergebnisse erscheinen unten in der **Galerie**. Das ausgewählte Bild ist das, woran du weiterarbeitest. Nochmal klicken führt zurück zum Original.
   - **Rechtsklick** auf ein Galeriebild: Farbe markieren, als final markieren, exportieren, löschen.
   - **⌘-Klick** wählt mehrere Bilder aus.
6. **Radierer (E):** Generiertes wegradieren, darunter kommt das Ausgangsbild zum Vorschein. Mit ⌥ holst du es zurück. Härte und Deckkraft sind einstellbar.
7. **Referenzbilder** (rechts hinzufügen, dann **Aufs Bild**): verschieben, skalieren, drehen, mit × wieder entfernen. **Einblenden** fügt sie passend ins Foto ein. Mit einer Skizze dazu entsteht zum Beispiel eine Hand, die das Objekt hält.
8. **Text (T):**
   - Ins Bild klicken und schreiben. Schrift, Farbe, fett, kursiv und Kontur lassen sich einstellen, dazu verschieben, skalieren und drehen.
   - Im Prompt beschreiben, wie der Text aussehen soll, z. B. „glass text“, „neon sign“, „painted on the wall“.
   - **Einblenden:** OpenAI macht ihn zum echten Teil des Bildes. Auf einer Wand oder einem Schild passt er sich perspektivisch an, am Himmel bleibt er flach.
   - Nennt der Prompt eine Szene (z. B. „… on a beach at sunset“), entsteht der Hintergrund mit.
   - **Direkt einsetzen** schreibt den Text ohne KI ins Bild.
9. **Exportieren** (oben rechts): PNG, JPEG, WebP oder PDF, auch mehrere Versionen auf einmal.

Weitere Tastenkürzel: **Leertaste** halten vergleicht mit dem Ausgangsbild, **Esc** bricht das Erzeugen ab, **⌘Z** nimmt Skizzen- und Radierstriche zurück.

## Optional: lokal und kostenlos mit ComfyUI

Ohne Internet und ohne Kosten, aber mit viel Speicherplatz und langsamer als OpenAI. Nur auf Macs mit Apple Silicon (M1 und neuer). Das Objekt-Werkzeug und die Bildanalyse brauchen ComfyUI.

1. In Füllwerk unter **Modell** den Anbieter **ComfyUI** wählen. Alternativ auf **Einrichtung prüfen …** klicken.
2. Das **Einrichtungs-Fenster** zeigt, was fehlt, jeweils mit Dateigröße, und was schon vorhanden ist:

   | Datei | Größe | |
   |---|---|---|
   | Comfy Desktop (Programm) | 0,2 GB + ca. 3–5 GB beim ersten Start | nötig |
   | Bildmodell Realistic Vision V6 Inpainting | 2,1 GB | nötig |
   | ControlNet Scribble und Canny | je 0,7 GB | empfohlen |
   | Hyper-SD Schnell-LoRAs | 2 × 0,3 GB | empfohlen |
   | Erweiterungen Florence-2 und SAM 2 | klein, + 1,2 GB beim ersten Gebrauch | für das Objekt-Werkzeug |

3. Auf **Ausgewählte herunterladen** klicken:
   - Füllwerk lädt alles von den Originalquellen (Hugging Face, GitHub, Hersteller).
   - Jedes Modell wird per Prüfsumme kontrolliert und in die richtigen ComfyUI-Ordner gelegt.
   - Die Erweiterungen werden installiert.
   - Abbrechen ist jederzeit möglich.
4. Comfy Desktop öffnet sich nach dem Download als Installationsfenster:
   - Comfy Desktop in **Programme** ziehen.
   - Einmal starten und eine Installation anlegen.
   - Zurück in Füllwerk auf **Erneut prüfen** klicken und den Rest herunterladen.

Insgesamt belegt das etwa **8–12 GB**. Füllwerk startet ComfyUI danach selbst im Hintergrund.

## Gut zu wissen

- **Updates (ab Version 1.1 automatisch):**
  - Füllwerk sieht beim Start höchstens einmal am Tag auf GitHub nach, ob es eine neue Version gibt.
  - Wenn ja, erscheint unten rechts ein Hinweis mit den Neuerungen: **Jetzt aktualisieren** oder **Später**. Ohne deinen Klick wird nichts installiert.
  - Beim Aktualisieren lädt Füllwerk die neue Version, prüft ihre Prüfsumme und Echtheit, ersetzt sich selbst und startet neu. Deine Projekte, Einstellungen und dein API-Schlüssel bleiben erhalten.
  - Füllwerk muss dafür im Ordner **Programme** liegen.
  - Abschalten oder von Hand suchen: **Modell → Erweiterte Einstellungen → Beim Start nach Updates suchen** bzw. **Jetzt nach Updates suchen**. Dabei sieht GitHub deine IP-Adresse.
  - **Wer noch Version 1.0 hat,** installiert 1.1 einmal von Hand wie oben beschrieben (Schritte 1–3, beim Verschieben „Ersetzen“ wählen). Danach geht es automatisch.
- **Deinstallieren:** Füllwerk in den Papierkorb legen. Wer auch die Projekte löschen will: `~/Library/WebKit/local.fuellwerk.app` löschen.
- **Kosten:** Mit OpenAI zahlst du direkt bei OpenAI, Füllwerk verdient nichts daran.
- Kostenlos, **ohne Gewähr**.
- Schrift: *Instrument Sans*, SIL Open Font License 1.1 (liegt der App bei).
