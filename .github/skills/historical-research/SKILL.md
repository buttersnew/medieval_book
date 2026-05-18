---
name: historical-research
description: "Recherche von historischem Kontext für das Buchprojekt (1200–1300, Österreich, Böhmen, Baltikum, Ägypten). Verwende diesen Skill wenn: historische Fakten zu einer Person, einem Ort oder einem Ereignis benötigt werden; ein Glossareintrag, Charaktereintrag oder Eintrag im Literaturverzeichnis mit Kontext gefüllt werden soll; geprüft werden soll ob Details/Szenen historisch plausibel sind; politische, religiöse oder kulturelle Verhältnisse der Epoche entsprechen."
---

# Historische Recherche – 13. Jahrhundert

## Zeitfenster und Schauplätze

**Immer als Filter anwenden:** Alle Informationen müssen im Zeitraum **1200–1300 n. Chr.** verortet sein.

| Region | Relevante Zeitspanne im Buch | Politischer Rahmen |
|---|---|---|
| Österreich / Herzogtum Österreich | durchgehend | Babenberger (bis 1246), dann Interregnum, dann Habsburger (ab 1273) |
| Böhmen / Königreich Böhmen | durchgehend | Přemysliden-Dynastie |
| Baltikum (Livland, Preußen, Litauen) | durchgehend | Livländischer Orden, Deutscher Orden, heidnische Stämme |
| Ägypten / Sultanat der Ayyubiden und Mamluken | Endphase | Ayyubiden (bis 1250), Mamluken (ab 1250) |

---

## Recherche-Workflow

### 1. Rechercheobjekt klassifizieren

Bestimme zuerst die Kategorie:

| Kategorie | Ziel der Recherche |
|---|---|
| **Person** | Historische Biografie, Rolle, Lebensdaten, Zugehörigkeit |
| **Ort** | Geografie, politische Zugehörigkeit, Bedeutung im 13. Jh. |
| **Ereignis** | Datum, Beteiligte, Ursache, Folgen, regionale Auswirkung |
| **Konzept / Objekt** | Kulturelle Praxis, Recht, Religion, Technologie, Alltagsleben |

### 2. Zeitfenster-Check (Pflicht)

Vor jeder Aussage prüfen:
- Existierte Person/Ort/Begriff **nachweislich zwischen 1200 und 1300**?
- Wenn die Quelle ein anderes Jahrhundert nennt: explizit kennzeichnen und Relevanz begründen.
- Anachronismen aktiv markieren: **[ANACHRONISMUS: erst ab Jahr X]**

### 3. Regionale Einordnung

Prüfe, ob die Information zur **Zielregion** des Buches passt:
- Österreich/Böhmen: Feudalstruktur, Ministeriale, Stadtrechte, Bischöfe
- Baltikum: Christianisierungsfeldzüge, Ordensritter, heidnische Gegner, Handelswege (Hanse)
- Ägypten: Kreuzzüge (5.–7. Kreuzzug), islamische Verwaltung, Kairo, Nilhandel

### 4. Quellen und Verlässlichkeit

Recherchiere bevorzugt mit Websuche. Bewerte Quellen nach:
- **Primärquellen** (Chroniken, Urkunden): höchste Glaubwürdigkeit
- **Fachliteratur / Wikipedia mit Belegen**: gut, aber auf Zeitraum prüfen
- **Allgemeine Enzyklopädien ohne Belege**: nur als Einstieg, nicht zitieren

Gib bei jeder Aussage an, wie gesichert sie ist:
- `[gesichert]` – belegbar durch Primärquellen oder Fachliteratur
- `[wahrscheinlich]` – zeitgenössisch plausibel, aber nicht direkt belegt
- `[fiktional zulässig]` – keine historischen Belege, widerspricht aber auch nichts

### 5. Ergebnis aufbereiten

Je nach Verwendungszweck das Ergebnis in einem der folgenden Formate ausgeben:

#### A) Glossareintrag (Ort oder Begriff) → `content/glossary.tex`

```latex
\newglossaryentry{Begriffname}{
    type=terms,
    name={Begriffname},
    description={Historischer Kontext (13. Jh.): Kurzbeschreibung. [gesichert/wahrscheinlich]}
}
```

#### B) Charaktereintrag → `content/character_register.tex`

```latex
\newglossaryentry{Vorname von Nachname}{
  type=characters,
  name={Vorname von Nachname},
  description={Lebensdaten (soweit bekannt). Herkunft, Stand, Rolle. Historischer oder fiktionaler Kontext. [gesichert/wahrscheinlich/fiktional zulässig]}
}
```

#### C) Hintergrundinformation (für Kapitelplanung, kein LaTeX-Output)

Freitext mit:
- Zeitliche Einordnung
- Politische/religiöse Lage
- Alltagsleben, Reisewege, Sprache
- Hinweise auf mögliche Anachronismen

---

## Wichtige historische Ankerpunkte (1200–1300)

### Österreich / Böhmen
- 1246: Tod Friedrichs II. (letzter Babenberger), Österreich wird Streitobjekt
- 1251: Přemysl Ottokar II. wird Herzog von Österreich
- 1273: Rudolf I. von Habsburg wird König, beginnt habsburgische Herrschaft
- 1278: Schlacht auf dem Marchfeld – Ende der böhmischen Vorherrschaft

### Baltikum
- 1202: Gründung des Schwertbrüderordens (Livland)
- 1226: Deutscher Orden erhält Kulmerland (Beginn der Preußenfeldzüge)
- 1236: Niederlage des Schwertbrüderordens bei Saule, Fusion mit Deutschem Orden
- 1260: Litauischer Sieg bei Durbe, großer Aufstand der Prußen

### Ägypten / Kreuzzüge
- 1218–1221: 5. Kreuzzug (Damiette)
- 1228–1229: 6. Kreuzzug (Friedrich II., diplomatischer Vertrag)
- 1248–1254: 7. Kreuzzug (Ludwig IX., Niederlage bei Al-Mansura 1250)
- 1250: Mamluken übernehmen die Macht in Ägypten

---

## Checkliste Rechercheergebnis

- [ ] Zeitraum 1200–1300 explizit bestätigt
- [ ] Region korrekt zugeordnet
- [ ] Verlässlichkeitsgrad angegeben (`[gesichert]` / `[wahrscheinlich]` / `[fiktional zulässig]`)
- [ ] Anachronismen markiert oder ausgeschlossen
- [ ] Quellenangabe (Primärquelle oder Fachliteratur) bereitgestellt und in Literaturverzeichnis aufgenommen
- [ ] Ergebnis in passendem Format (Glossar, Charakterregister oder Freitext) aufbereitet und Quelle korrekt zitiert
