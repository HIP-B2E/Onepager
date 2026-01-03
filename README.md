# Onepager B2E

Ein schlanker Onepager für **Business to Environment (B2E)** basierend auf der bereitgestellten Broschüre. Die Seite übernimmt Farben und Stimmung der Vorlage, enthält ein Kontaktformular und lässt sich lokal ohne Build-Toolchain starten.

## Inhalte
- Hero mit Claim und Call-to-Action
- Sektionen für Vision, Werte, solidarisches Finanzierungsmodell, Vorteile, FAQ und Prozess
- Kontaktbereich mit Mail-Link und Formular (mailto: kontakt@hip.swiss)

## Lokale Nutzung
1. Repository klonen:
   ```bash
   git clone <repo-url>
   cd Onepager
   ```
2. Eine lokale Vorschau starten (optional):
   ```bash
   python -m http.server 8000
   ```
3. Im Browser `http://localhost:8000` öffnen und `index.html` ansehen. Alternativ kann die Datei auch direkt im Browser geöffnet werden.

### Warum gibt es keine automatische Vorschau?
In dieser Umgebung wird kein permanenter Webserver oder GitHub Pages automatisch bereitgestellt. Daher können keine direkten Vorschaulinks generiert werden. Die schnelle Variante ist der oben genannte lokale Aufruf via `python -m http.server`. Möchtest du eine dauerhaft verfügbare Vorschau, kannst du GitHub Pages aktivieren:

1. Änderungen committen und in ein GitHub-Repository pushen.
2. In den Repository-Einstellungen unter **Pages** den Branch (z. B. `main`) und den Ordner `/` auswählen.
3. Nach wenigen Minuten ist die Seite unter der von GitHub Pages angezeigten URL erreichbar.

## Anpassungen
- Farben und Typografie werden in `styles.css` definiert.
- Inhalte können in `index.html` bearbeitet werden. Bilder/Logos können bei Bedarf unter `assets/` ergänzt und im HTML referenziert werden.

## GitHub: Schritt für Schritt
1. **GitHub-Konto & neues Repository erstellen**
   - Auf <https://github.com> registrieren/anmelden.
   - Rechts oben auf **+** → **New repository** klicken.
   - Einen Namen vergeben (z. B. `onepager`), Sichtbarkeit wählen (Public/Private) und **Create repository** wählen.

2. **Code hochladen**
   - Falls Git installiert ist:
     ```bash
     git clone <deine-repo-url>
     cd <repo-name>
     # Projektdateien (index.html, styles.css, README.md, ggf. assets/) hineinkopieren
     git add .
     git commit -m "Add onepager"
     git push origin main
     ```
   - Alternativ im Browser: Im Repository auf **Add file** → **Upload files** klicken, `index.html`, `styles.css` und `README.md` hochladen und committen.

3. **GitHub Pages aktivieren (für eine öffentliche Vorschau)**
   - Im Repository auf **Settings** → **Pages** gehen.
   - **Source**: Branch `main` (oder der verwendete Branch) und **Root** auswählen, speichern.
   - Nach wenigen Minuten zeigt GitHub die öffentliche URL an (z. B. `https://<user>.github.io/<repo>`). Diese kann geteilt werden.

4. **Lokale Vorschau und Tests**
   - Optional vor dem Push: Im Projektverzeichnis `python -m http.server 8000` starten und unter `http://localhost:8000` prüfen.

5. **Änderungen pflegen**
   - Inhalte/Farben in `index.html` und `styles.css` anpassen.
   - Änderungen committen (`git add`, `git commit`) und per `git push` hochladen.
   - GitHub Pages aktualisiert sich automatisch nach jedem Push.
