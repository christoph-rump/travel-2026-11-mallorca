# Mallorca-Tage, 5.–9. November 2026

Reiseplan für die Gruppe in der Villa in Costa de la Calma (DE/EN umschaltbar): Tagesplan, Karte, Restaurants & Bars, Einkauf & Services, Budget-Rechner, Wetter und Quellen.

Alles steckt in einer einzigen Datei, `index.html`. Keine Installation, kein Build.

## Lokal ansehen

`index.html` doppelklicken, sie öffnet sich im Browser.

## Auf GitHub Pages veröffentlichen

1. Auf github.com ein neues Repository anlegen, z. B. `mallorca-tage`.
2. **Add file → Upload files**: `index.html`, `README.md` und `.nojekyll` hochladen, **Commit changes**.
3. **Settings → Pages** → Source: **Deploy from a branch**, Branch **main**, Ordner **/ (root)**, **Save**.
4. Nach ein bis zwei Minuten ist die Seite unter `https://<dein-benutzername>.github.io/mallorca-tage/` erreichbar.

Hinweis: Mit einem kostenlosen GitHub-Konto ist eine Pages-Seite öffentlich, auch wenn das Repository privat ist. Der Plan enthält keine Adresse der Villa. In der Matrix im Reiter **Menü & Getränke** stehen Vornamen mit Ess- und Trinkvorlieben; wer das nicht öffentlich will, ersetzt sie in `PEOPLE` im Skript durch Kürzel. Die Allergie steht bewusst ohne Namen drin.

## Menü & Getränke

Pro Mahlzeit in der Villa gibt es zwei Vorschläge (A/B). Die Auswahl wird im Browser gespeichert und ändert automatisch die Einkaufsliste und die Texte im Tagesplan. Daten stehen im Skript unter `MENU`, `MX` (Matrix) und `SANGRIA`.

## Karte

Die Karte ist direkt in der Seite gezeichnet (SVG) und braucht keine externen Dienste. Pro Tag zeigt sie Routen, Uhrzeiten und Verkehrsmittel.

## Budget und Admin

Der Reiter **Budget** zeigt öffentlich nur Gesamtkosten, Rate pro Person, Kategorien und was inklusive ist. Die Einzelposten liegen verschlüsselt (AES-GCM, Schlüssel per PBKDF2 aus dem Passwort) im Reiter **Admin** und werden erst nach Eingabe des Passworts im Browser entschlüsselt. Das Passwort steht nirgends in den Dateien; bitte auch nicht in dieses Repository schreiben.

## Ändern

Texte stehen zweisprachig direkt im HTML (`data-l="de"` / `data-l="en"`). Kartenorte, Routen und Budget-Posten stehen im `<script>` am Ende der Datei.
