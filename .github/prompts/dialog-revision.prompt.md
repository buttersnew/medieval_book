---
name: Dialog-Revision
description: "Ueberarbeitet eine gegebene Dialogszene in mittelalterlichen Chronikstil fuer Konrad von Steinare, inkl. LaTeX- und Glossarregeln."
argument-hint: "Fuege den zu ueberarbeitenden Dialog oder eine Szenenbeschreibung ein"
agent: "agent"
---

Ueberarbeite den gegebenen Text als Dialog im Stil des Romans Konrad von Steinare.

Arbeite strikt nach diesen Kriterien:
- Chronikalischer Ton eines Moenchs, der spaeter berichtet.
- Historisch plausibles 13. Jahrhundert, ohne moderne Idiome.
- Standessprache deutlich machen (Adel, Klerus, Gefolge).
- Direkte Rede nur mit \enquote{...}.
- Bei namentlicher Nennung vorhandene Schluessel mit \gls{...} nutzen.
- Keine Gedankenstriche.

Ausgabeformat:
1. Revidierter LaTeX-Dialogblock
2. Kurze Liste Aenderungen (maximal 6 Punkte)
3. Offene Unsicherheiten mit Marker [fiktional zulaessig], falls noetig
