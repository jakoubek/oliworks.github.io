# Seite überarbeiten

Du sollst eine Content-Seite sprachlich und inhaltlich überarbeiten, um die Qualität gemäß den CLAUDE.md-Richtlinien zu verbessern.

## Aufgabe

Der Nutzer gibt dir einen Seitennamen, Titel oder Dateipfad. Du sollst:

1. **Die Seite finden und lesen**
   - Suche nach dem angegebenen Namen/Titel in `content/projekt/` oder `content/`
   - Lese die aktuelle Version der Seite

2. **Aktuelle Qualität analysieren**
   - Prüfe gegen die CLAUDE.md Content-Standards
   - Identifiziere konkrete Schwächen (z.B. zu technisch, fehlende Struktur, kein Consulting-Fokus)
   - **Checkliste - prüfe alle Elemente**:
     - [ ] **Titel**: Aussagekräftig, beschreibt die Lösung/das Ergebnis, nicht nur Thema
     - [ ] **Slug/Filename**: SEO-optimiert (3-5 Wörter, Keywords, kebab-case, keine Umlaute)
     - [ ] **Description**: Vollständig, SEO-Keywords, Nutzen klar
     - [ ] **Body/Content**: Struktur, Ton, Business-Fokus, Cross-Industry

3. **Fragen stellen, falls nötig**
   - Wenn wichtige Business-Informationen fehlen (Herausforderung, Ergebnis, etc.), nutze AskUserQuestion
   - Frage nach konkreten Details, nicht nach allgemeinen Vorgaben

4. **Plan präsentieren**
   - Zeige, welche Änderungen du vornehmen willst
   - Nutze ExitPlanMode um den Plan zur Freigabe vorzulegen

5. **Überarbeitung durchführen** (nach Freigabe)
   - **WICHTIG: Überarbeite ALLE Elemente systematisch** - nutze die Checkliste:

   **A) Frontmatter-Elemente**:
   - [ ] **`title`**: Aussagekräftig überarbeiten (Lösung/Ergebnis, nicht nur Thema)
   - [ ] **`description`**: Vollständig, SEO-Keywords, Kundennutzen klar
   - [ ] **`contentQuality`**: Auf neuen Wert (3-5) aktualisieren

   **B) Filename/Slug**:
   - [ ] **Filename**: SEO-optimiert umbenennen falls nötig (mit `git mv`)
     - 3-5 Wörter, Keywords, kebab-case, keine Umlaute, keine Füllwörter

   **C) Body/Content**:
   - Wende die CLAUDE.md-Richtlinien an:
     - **Struktur**: "Die Herausforderung / Die Lösung / Das Ergebnis" (falls Kundenprojekt)
     - **Ton**: Professional, für Business-Entscheider verständlich
     - **Positionierung**: Consulting-Kompetenz betonen, nicht nur Development
     - **Cross-Industry**: Neutrale Formulierung, keine Branchen-Einengung
     - **SEO**: Keywords natürlich integrieren

## Wichtige Hinweise

- **Immer in Plan Mode arbeiten**: Erst Analyse und Fragen, dann Plan, dann Umsetzung
- **Alle Elemente prüfen**: Titel, Slug, Description UND Body - vergiss keines!
- **Authentisch bleiben**: Keine Marketing-Phrasen, konkrete Aussagen
- **Business-Fokus**: Nutzen vor Technik
- **Consulting-Perspektive**: Architekturentscheidungen, Konzeption betonen
- **Systematisch vorgehen**: Arbeite die Checkliste (Titel → Slug → Description → Body) ab

## Beispiel-Aufruf

```
/seite-ueberarbeiten Produktionssteuerung
/seite-ueberarbeiten content/projekt/datesapi.md
```
