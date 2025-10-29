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

3. **Fragen stellen, falls nötig**
   - Wenn wichtige Business-Informationen fehlen (Herausforderung, Ergebnis, etc.), nutze AskUserQuestion
   - Frage nach konkreten Details, nicht nach allgemeinen Vorgaben

4. **Plan präsentieren**
   - Zeige, welche Änderungen du vornehmen willst
   - Nutze ExitPlanMode um den Plan zur Freigabe vorzulegen

5. **Überarbeitung durchführen** (nach Freigabe)
   - Wende die CLAUDE.md-Richtlinien an:
     - **Struktur**: "Die Herausforderung / Die Lösung / Das Ergebnis" (falls Kundenprojekt)
     - **Ton**: Professional, für Business-Entscheider verständlich
     - **Positionierung**: Consulting-Kompetenz betonen, nicht nur Development
     - **Cross-Industry**: Neutrale Formulierung, keine Branchen-Einengung
     - **SEO**: Keywords natürlich integrieren
   - Aktualisiere das `contentQuality`-Feld auf den neuen Wert (3-5)
   - Aktualisiere die `description` im Frontmatter falls nötig

## Wichtige Hinweise

- **Immer in Plan Mode arbeiten**: Erst Analyse und Fragen, dann Plan, dann Umsetzung
- **Authentisch bleiben**: Keine Marketing-Phrasen, konkrete Aussagen
- **Business-Fokus**: Nutzen vor Technik
- **Consulting-Perspektive**: Architekturentscheidungen, Konzeption betonen

## Beispiel-Aufruf

```
/seite-ueberarbeiten Produktionssteuerung
/seite-ueberarbeiten content/projekt/datesapi.md
```
