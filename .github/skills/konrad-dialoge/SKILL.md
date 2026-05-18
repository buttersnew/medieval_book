---
name: konrad-dialoge
description: "Dialoge im Stil von Konrad von Steinare für das 13. Jahrhundert schreiben. Verwende diesen Skill, wenn Figurenrede für Szenen im mittelalterlichen Roman erzeugt, überarbeitet oder stilistisch vereinheitlicht werden soll, inklusive Chronisten-Ton, Standessprache, LaTeX-Regeln und Glossarverweisen."
argument-hint: "Worum geht der Dialog, wer spricht, wo und wann?"
---

# Konrad-Dialoge

## Ziel

Dieser Skill erzeugt oder überarbeitet Dialoge, die wie Teil der Chronik von Kuonrat von Steinare klingen.
Der Stil bleibt historisch plausibel, würdevoll und erzählerisch als Niederschrift eines Mönchs geführt.

## Wann verwenden

- Wenn neue Dialoge für Kapiteldateien in `content/book */chapter*.tex` benötigt werden.
- Wenn bestehende Figurenrede zu modern klingt und in mittelalterlichen Ton überführt werden soll.
- Wenn direkte Rede in eine Chronisten-Perspektive mit vorsichtiger Distanz gebracht werden soll.
- Wenn Dialoge LaTeX-konform mit `\enquote{...}` und passenden `\gls{...}`-Referenzen formuliert werden sollen.

## Stilkern

- Sprache ist durchgehend Deutsch in chronikalem Ton.
- Figuren sprechen standesgemäß: Ritter knapp und befehlend, Kleriker abwägend, Knechte erdig und direkt.
- Mittelhochdeutsche Färbung ist erwünscht, aber lesbar dosiert.
- Namen stehen in mittelhochdeutscher Form, zum Beispiel Kuonrat, Hadmar, Niclas.
- Moderne Redewendungen und anachronistische Begriffe sind ausgeschlossen.
- Für Unsicheres nutzt der Erzähler Formeln wie `wie mir berichtet ward`, `so heißt es`, `der Herr allein weiß es`.

## Dialog-Workflow

1. Kontext erfassen
- Ort, Zeit, Anlass, Beteiligte und Machtverhältnis der Szene bestimmen.
- Prüfen, was bereits in Kapitelzusammenfassungen und Charakterprofilen festgelegt ist.

2. Stimmen festlegen
- Für jede Figur Wortwahl, Satzlänge und Ton definieren.
- Stand und Beziehung zur Gegenseite in jeder Antwort hörbar machen.

3. Dialog entwerfen
- Redezüge kurz und prägnant halten, mit klarer Absicht pro Zeile.
- Direkte Rede ausschließlich mit `\enquote{...}` setzen.
- Bei namentlicher Nennung vorhandene Glossar- und Charakterschlüssel mit `\gls{...}` referenzieren.

4. Chronistenebene einziehen
- Zwischen Redebeiträgen knappe Beobachtungen des Mönchs einfügen, falls dies Klarheit oder Spannung schafft.
- Innere Gedanken nur vorsichtig und als Vermutung wiedergeben.

5. Schlussredaktion
- Prüfen, ob der Dialog Handlung voranbringt oder Beziehungen verändert.
- Prüfen, ob jede Zeile zeitlich und sozial plausibel klingt.

## Entscheidungslogik

- Wenn ein Herr einem Untergebenen spricht: Befehlsform, knappe Sätze, wenig Rechtfertigung.
- Wenn Untergebene mit Adel sprechen: ehrerbietige Anrede, indirektere Forderungen, vorsichtiger Widerspruch.
- Wenn kirchliche Figuren sprechen: moralische Rahmung, Verweise auf Pflicht, Maß und Sünde.
- Wenn Informationen unsicher sind: Erzähler markiert Unsicherheit explizit statt Details zu erfinden.
- Wenn ein Streit eskaliert: Satzlänge verkürzen, Wortwahl härten, Erzählkommentar knapp halten.

## Qualitätskriterien

- Dialog ist ohne moderne Idiome, Jargon oder Gegenwartslogik geschrieben.
- Jede Figur hat erkennbar eigene Stimme und sozialen Standort.
- Der Mönch bleibt als überliefernder Erzähler plausibel im Hintergrund.
- LaTeX-Regeln sind eingehalten: `\section{}` unverändert, `\enquote{...}` für Zitate, korrekte `\gls{...}`-Schlüssel.
- Keine Gedankenstriche im Fließtext.

## Ausgabeformat

Liefere standardmäßig einen direkt einfügbaren LaTeX-Block für eine Kapiteldatei mit:
- kurzer Szeneneinleitung im Chronistenstil,
- Dialogpassage,
- kurzem Ausklang, der den Übergang zur nächsten Handlung vorbereitet.

## Beispielprompts

- `/konrad-dialoge Verfasse einen Dialog zwischen Kuonrat und Hadmar vor der Abreise nach Raabs, angespannt aber höfisch.`
- `/konrad-dialoge Überarbeite diese Szene in mittelalterlichen Ton: [Text einfügen].`
- `/konrad-dialoge Schreibe eine kurze Verhörszene zwischen einem Mönch und einem Knecht, mit unsicherer Quellenlage.`
