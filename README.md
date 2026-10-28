# Revisionsunterlagen-Prüfung (LPH 8, Kaufland)

Einzeldatei-Web-App (`index.html`) auf GitHub Pages, Daten in Supabase (Projekt „Protokoll“).

- **Checkliste IP → FM**: alle 19 Gewerke der Vorlage `20261016_Vorlage_Objektuebergabe_IP_FM.xlsx` (349 Prüfpunkte). Standardmäßig geprüft: Blitzschutz, Elektro, Heizung, Lüftung, Entrauchung, Sanitär, Sprinkler/Feuerlöscher, Fördertechnik, Betriebshandbuch. Weitere Gewerke je Markt zuschaltbar.
- **Protokoll BPM → TFM**: Kopfdaten und Kommentar je Punkt.
- **Ordnerstruktur**: Prüfung des Firmen-Projektordners (00–16 mit 01_Abnahme / 02_Dokumente / 03_Pläne) per Ordnerauswahl im Browser (nur Namen, kein Upload); leere Struktur als ZIP.
- **Export**: Excel im Layout der Vorlage (Vorlage ist eingebettet), Druck/PDF.
- Anhänge je Prüfpunkt im öffentlichen Bucket `revision-anlagen` (bis 25 MB).

Tabellen: `revision_pruefungen`, `revision_punkte` (bereits angelegt). Zugriff offen per Link wie bei Bemusterung/Wandfreigabe.

Bau: `python3 build.py` setzt `src/*` mit `template.json` und `vorlage.xlsx` zu `index.html` zusammen. Test: `tests/pw_test_rev.js` (Playwright, Supabase gemockt).
