---
description: "Use when creating or editing character profile files in docs/characters/. Provides format rules for character documentation in the medieval book project."
applyTo: "docs/characters/*.md"
---

# Charakterprofil-Format

Dateien in `docs/characters/` dokumentieren Charaktere für den Konsistenz-Check des Novelist-Agenten. **Dateiname = vollständiger Charaktername** (z. B. `Konrad von Steiner.md`).

## Pflichtstruktur

```markdown
# <Charaktername>

## Basisdaten
- **Stand:** (z. B. Ritter, Kaufmann, Kleriker, Ordensbruder, Händler)
- **Herkunft:** (Ort, Region)
- **Erste Erwähnung:** Kapitel <Titel>

## Beschreibung
Kurze physische und charakterliche Beschreibung (3–5 Sätze).

## Bisheriger Verlauf
Chronologische Stichpunkte – ein Eintrag pro Kapitel in dem der Charakter vorkommt:
- **[Kapiteltitel]:** Was ist dem Charakter widerfahren?

## Beziehungen
- <Name>: <Verhältnis> (z. B. „Bruder", „Lehnsherr", „Feind")
```

## Regeln

- Jeder **benannte Charakter** der im Roman auftritt erhält eine eigene Datei.
- Der Charakter muss außerdem in `content/character_register.tex` als `\newglossaryentry` (Typ `characters`) eingetragen sein.
- **Bisheriger Verlauf** nach jedem Kapitel in dem der Charakter vorkommt ergänzen – niemals löschen, nur anfügen.
- Fiktionale Details mit `[fiktional zulässig]` markieren, historisch belegte mit `[gesichert]`.
