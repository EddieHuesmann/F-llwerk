# Füllwerk

**Generative Fill für den Mac.** Bereich im Bild markieren, beschreiben, was dort entstehen soll, und aus mehreren Versionen wählen. Man kann auch skizzieren, Referenzbilder aufs Bild legen und einblenden, Farben ersetzen und Generiertes wieder wegradieren.

- Läuft auf jedem Mac ab **macOS 13 (Ventura)**, mit Apple Silicon und Intel.
- Download ca. **0,5 MB**.
- Bildmodell: **OpenAI** (eigener API-Schlüssel, ca. 0,02 $ pro Version) oder optional **lokal und kostenlos mit ComfyUI**.
- Projekte, Bilder und dein API-Schlüssel bleiben **nur auf deinem Mac**. Füllwerk hat keinen Server und sammelt keine Daten.

## Installieren

1. Unter [**Releases**](../../releases/latest) die Datei **`Fuellwerk-1.0.zip`** herunterladen.
2. Die Zip-Datei doppelklicken. Im Download-Ordner liegt jetzt **Füllwerk**.
3. **Füllwerk** in den Ordner **Programme** ziehen.
4. Füllwerk doppelklicken. Beim **ersten Start** meldet macOS „Apple konnte nicht überprüfen, ob ‚Füllwerk‘ frei von Schadsoftware ist“. Das liegt daran, dass die App nicht über ein kostenpflichtiges Apple-Entwicklerkonto signiert ist.
   - Auf **Fertig** klicken (nicht „In den Papierkorb“).
   - **Systemeinstellungen → Datenschutz & Sicherheit** öffnen und ganz nach unten scrollen.
   - Bei „Füllwerk wurde blockiert …“ auf **Dennoch öffnen** klicken und mit dem Mac-Passwort bestätigen.
   - Das ist nur einmal nötig. Danach startet Füllwerk normal.

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
6. **Radierer (E):** Generiertes wegradieren, darunter kommt das Ausgangsbild zum Vorschein. Mit ⌥ holst du es zurück.
7. **Exportieren** (oben rechts): PNG, JPEG, WebP oder PDF, auch mehrere Versionen auf einmal.

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

- **Updates:** Neue Versionen erscheinen unter *Releases*. Die alte App durch die neue ersetzen, deine Projekte und Einstellungen bleiben erhalten.
- **Deinstallieren:** Füllwerk in den Papierkorb legen. Wer auch die Projekte löschen will: `~/Library/WebKit/local.fuellwerk.app` löschen.
- **Kosten:** Mit OpenAI zahlst du direkt bei OpenAI, Füllwerk verdient nichts daran.
- Kostenlos, **ohne Gewähr**.
- Schrift: *Instrument Sans*, SIL Open Font License 1.1 (liegt der App bei).
