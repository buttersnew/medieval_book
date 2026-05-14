---
name: medieval-book-latex
description: "Struktur und Bearbeitung des LaTeX-Buchprojekts. Verwende diesen Skill wenn: ein neues Buch oder Kapitel hinzugefügt werden soll; ein neuer Charakter in das Charakterregister eingetragen werden soll; ein neuer Begriff, Ort oder historischer Kontext ins Glossar soll; Hintergrundbilder für Kapitelseiten zugewiesen werden sollen; Fragen zur Dateistruktur oder main.tex aufkommen."
---

# Medieval Book – LaTeX Projektstruktur

## Projektübersicht

Das Projekt ist ein LaTeX-Buch (`\documentclass[12pt,openany]{book}`) mit folgender Gliederung:

```
main.tex                        ← Master-Dokument (Einstiegspunkt)
misc/options.sty                ← Alle Pakete, Farben, Custom-Commands
content/
  book 1/                       ← Ordner für Buch 1
    chapter1.tex                ← Kapitel-Dateien
  book 2/                       ← Ordner für Buch 2 (gleiche Struktur)
  character_register.tex        ← Charakterdefinitionen (Glossar-Typ: characters)
  glossary.tex                  ← Begriffe, Orte, Konzepte (Glossar-Typ: terms)
  concept_art/                  ← Hintergrundbilder (chapter_decoration_*.png, page_decoration_*.png)
  appendix.tex
frontmatter/                    ← Titelseite, Copyright, Vorwort, Inhaltsverzeichnis, Rückseite
```

---

## Neues Buch hinzufügen

### Schritt 1 – Ordner anlegen
Erstelle einen neuen Ordner `content/book N/` (z. B. `content/book 2/`).

### Schritt 2 – Erste Kapiteldatei anlegen
Erstelle `content/book N/chapter1.tex` mit folgendem Grundgerüst:

```latex
% Kapitel 1
\section{Abschnitt eins}

\mylettrine{E}{rster} Absatz des Kapitels.
```

### Schritt 3 – Buch in `main.tex` eintragen
Füge den Block **vor** `\StopRandomBackgrounds` in `main.tex` ein:

```latex
% book N
\setchapterbackground{content/concept_art/chapter_decoration_X.png}{ManuscriptRed}
\chapter{Buchtitel}\label{buchtitel}
\input{content/book N/chapter1}
```

**Parameter von `\setchapterbackground`:**
- Argument 1: Pfad zum Hintergrundbild (relativ zum Projektstamm)
- Argument 2: Textfarbe des Kapiteltitels – entweder `ManuscriptRed` (RGB 192,0,0), `customgold` (RGB 203,161,53) oder `black`

---

## Neues Kapitel zu einem bestehenden Buch hinzufügen

### Schritt 1 – Kapiteldatei anlegen
Erstelle `content/book N/chapterX.tex`:

```latex
% Kapitel X
\section{Abschnittstitel}

\mylettrine{E}{rster} Absatz.
```

### Schritt 2 – Kapitel in `main.tex` einbinden
Füge nach dem letzten `\input` des betreffenden Buches ein:

```latex
\input{content/book N/chapterX}
```

> Kapitel teilen sich einen gemeinsamen `\chapter{}`-Eintrag des Buches. Für ein neues `\chapter{}` (eigener Inhaltsverzeichniseintrag) sieh den Abschnitt „Neues Buch hinzufügen".

---

## Charakter eintragen (`content/character_register.tex`)

Jeder Charakter mit eigenem Namen wird hier als Glossareintrag (Typ `characters`) definiert:

```latex
\newglossaryentry{Vorname von Nachname}{
  type=characters,
  name={Vorname von Nachname},
  description={Historischer oder fiktionaler Kontext: Herkunft, Rolle, Bedeutung im Werk.}
}
```

**Regeln:**
- Schlüssel (erster Parameter) und `name` sind identisch und entsprechen dem vollen Namen.
- Im Fließtext wird ein Charakter mit `\gls{Vorname von Nachname}` referenziert.
- Historischer Kontext, Quellen und fiktionale Abweichungen gehören in `description`.
- `description` darf **nicht** mit einem Punkt (`.`) enden – LaTeX fügt diesen automatisch an.

---

## Glossareintrag anlegen (`content/glossary.tex`)

Orte, historische Begriffe, Konzepte und sonstige Fachbegriffe werden hier als Typ `terms` definiert:

```latex
\newglossaryentry{Begriffname}{
    type=terms,
    name={Begriffname},
    description={Historischer oder geographischer Kontext.}
}
```

**Regeln:**
- Für Orte: geografische Lage, historische Epoche, Bedeutung für die Handlung.
- Im Fließtext: `\gls{Begriffname}`.
- `description` darf **nicht** mit einem Punkt (`.`) enden – LaTeX fügt diesen automatisch an.

---

## Verfügbare Hintergrundbilder (`content/concept_art/`)

| Kategorie | Dateien | Verwendung |
|---|---|---|
| Kapitel-Titelseiten | `chapter_decoration_1.png` … `chapter_decoration_10.png` | `\setchapterbackground{...}{Farbe}` |
| Zufällige Seitenhintergründe | `page_decoration_1.png` … `page_decoration_13.png` | Automatisch via `\StartRandomBackgrounds` |
| Titelseite | `title_page_2.png` | In `frontmatter/titlepage.tex` |

Zufällige Seitenhintergründe sind **per Block** aktivierbar:

```latex
\StartRandomBackgrounds
% ... Kapitelinhalte ...
\StopRandomBackgrounds
```

---

## Wichtige Custom-Commands (aus `misc/options.sty`)

| Command | Beschreibung |
|---|---|
| `\setchapterbackground{bild}{farbe}` | Hintergrundbild + Textfarbe für das nächste `\chapter{}` |
| `\StartRandomBackgrounds` | Aktiviert zufällige Seitenhintergründe |
| `\StopRandomBackgrounds` | Deaktiviert zufällige Seitenhintergründe |
| `\mylettrine{B}{eginnt} Text...` | Initialbuchstabe (Drop Cap): 1. Arg = Großbuchstabe, 2. Arg = Rest des ersten Wortes, danach normaler Text |
| `\carolingian` | Mittelalterliche Schriftart (PfefferMediaeval) für Titel |
| `\hsp` | Kleines Kerning (1pt) für verschachtelte Anführungszeichen |
| `\enquote{Text}` | Korrekte typografische Anführungszeichen – **immer** verwenden statt `„..."` oder `"..."` |

> **Pflicht:** Für alle Anführungszeichen im Fließtext (Dialoge, hervorgehobene Begriffe, Zitate) ausschließlich `\enquote{...}` verwenden. Rohe Anführungszeichen (`„"`, `""`, `''`) sehen im kompilierten PDF hässlich aus und sind verboten.

---

## Dokumentausgabe steuern (`main.tex`)

Am Anfang von `main.tex` können zwei Schalter gesetzt werden:

```latex
% \printversiontrue   % Druckversion: mit Bleed und Beschnittzugabe
% \boundversiontrue   % Gebundene Vorschau: asymmetrische Ränder
% (beide auskommentiert = symmetrischer Bildschirm-PDF)
```

---

## Checkliste: Buch/Kapitel fertigstellen

- [ ] Ordner `content/book N/` existiert
- [ ] Mindestens eine `chapterX.tex` im Ordner angelegt
- [ ] Eintrag in `main.tex` mit `\setchapterbackground`, `\chapter{}`, `\label{}`, `\input{}` vorhanden
- [ ] Alle namentlich genannten Charaktere in `character_register.tex` definiert
- [ ] Alle Orte und Fachbegriffe in `glossary.tex` definiert
- [ ] Hintergrundbild aus `content/concept_art/` ausgewählt
