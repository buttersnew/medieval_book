---
description: "Use when creating or editing chapter summary files in docs/chapters/. Provides format rules for chapter documentation in the medieval book project."
applyTo: "docs/chapters/*.md"
---

# Kapitelzusammenfassung-Format

Dateien in `docs/chapters/` dokumentieren Kapitel für den Konsistenz-Check des Novelist-Agenten. **Dateiname = Kapiteltitel** (z. B. `Die Ankunft in Wien.md`).

## Pflichtstruktur

```markdown
# <Kapiteltitel>

## Zusammenfassung
3–5 Sätze: Was passiert, wo, mit wem, welche Konsequenzen ergeben sich.

## Wichtige Ereignisse
- <Ereignis 1>
- <Ereignis 2>

## Beteiligte Charaktere
- <Name 1>
- <Name 2>

## Schauplätze
- <Ort 1> (Region, z. B. Wien / Herzogtum Österreich)

## Offene Handlungsfäden
- Was bleibt ungeklärt oder wird im nächsten Kapitel relevant?
```

## Regeln

- Eine Datei pro `\section{}` in `main.tex` / pro Kapitel-Datei (`chapterN.tex`).
- Zusammenfassung nach dem Schreiben des Kapitels anlegen, nie vorher.
- Offene Handlungsfäden müssen im Folgekapitel aufgelöst oder explizit weitergeführt werden.
- Neue Glossareinträge (mhd. Begriffe, Orte) die im Kapitel eingeführt wurden hier kurz vermerken, damit sie auffindbar bleiben.
