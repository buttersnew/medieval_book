---
description: "Use when creating or editing chapter files in content/book */chapter*.tex. Enforces medieval dialog style, chronicle perspective, LaTeX quote rules, and glossary key usage."
applyTo: "content/book */chapter*.tex"
---

# Dialogstil fuer Kapiteldateien

Diese Instruction gilt fuer Dialogstellen in Kapiteldateien.

## Ziel

Dialoge sollen in das 13. Jahrhundert passen und wie Teil einer moenchischen Chronik wirken.

## Pflichtregeln

- Sprache bleibt deutsch und historisch plausibel.
- Keine modernen Redewendungen, keine Gegenwartsbegriffe.
- Normale deutsche Umlaute im Fließtext direkt als `ä`, `ö`, `ü` schreiben, niemals als `ae`, `oe`, `ue`.
- Direkte Rede immer mit \enquote{...}, niemals mit rohen Anfuehrungszeichen.
- Benannte Charaktere und Glossarbegriffe bei namentlicher Nennung mit \gls{Schluessel} referenzieren.
- Jeder neu eingefuehrte mittelhochdeutsche Begriff muss in `content/glossary.tex` als Glossareintrag vom Typ `terms` angelegt werden und im Kapiteltext ueber `\gls{Schluessel}` erscheinen; rohe Begriffe wie `Frouwe` ohne Glossareintrag sind nicht erlaubt.
- Mittelhochdeutsche Namensformen verwenden, passend zum Register.
- Keine Gedankenstriche im Fliesstext.

## Rollenstimmen

- Adel: knapp, befehlend, standesbewusst.
- Klerus: abwaegend, moralisch gerahmt, mahnend.
- Gefolge und Knechte: direkter, erdiger, aber sozial untergeordnet.

## Chronistenperspektive

- Der Erzaehler ist ein spaeterer Berichterstatter, nicht Augenzeuge.
- Unsichere Details als unsicher markieren, zum Beispiel: so heisst es, wie mir berichtet ward.
- Innere Gedanken nur vorsichtig als Vermutung darstellen.

## Vor Abgabe pruefen

- Treibt der Dialog die Handlung voran oder klaert ein Verhaeltnis?
- Sind alle Stimmen klar unterscheidbar?
- Sind LaTeX-Form und gls-Schluessel korrekt?
