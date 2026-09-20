---
title: "Die wahren Kosten von AI-first"
date: 2026-09-08
slug: "the-real-cost-of-ai-first"
tags: ["AI-first", "Kosten", "Strategie", "Betrieb"]
status: "published"
excerpt: "Inference ist der billigste Posten. Die Rechnung für AI-first besteht überwiegend aus Evaluation, Prüfung, Wartung und Compliance – und die meisten Budgets übersehen sie. Hier steht die Kalkulation, die entscheidet, ob sich ein AI-Feature lohnt."
---

Das erste AI-Feature, das ein Unternehmen ausliefert, ist meist günstig: ein API-Schlüssel, ein Prototyp, eine Demo, die in einer Führungsrunde gut ankommt. Im zweiten Jahr fließt das Geld – und es ist selten das Geld, das jemand eingeplant hatte.

## Die Rechnung besteht nicht aus Inference-Kosten

Modellaufrufe sind der sichtbarste Kostenposten und zunehmend der unwichtigste. Die Preise für ein gegebenes Fähigkeitsniveau sind in den letzten drei Jahren um etwa eine Größenordnung pro Jahr gefallen, und der Wettbewerbsdruck drückt sie weiter. Die Kosten rund um den Modellaufruf bleiben dagegen stabil oder steigen:

- **Evaluation und Dateninfrastruktur.** Jede Interaktion mit Ergebnis-Labels protokollieren, Golden Sets pflegen und Regressions-Gates aufbauen. Ohne das können Sie Verbesserung nicht von Rauschen unterscheiden – und zahlen stattdessen mit ausgelieferten Regressionen.
- **Menschliche Prüfung und Eskalation.** Wo eine falsche Antwort teuer ist, muss ein Mensch die Ausgabe prüfen. Diese Arbeit ist nicht kostenlos, und sie schrumpft nicht, nur weil das Modell besser geworden ist; sie verschiebt sich.
- **Wartung über den Modellwechsel hinweg.** Anbieter ziehen Modellversionen zurück, ändern Standardwerte und stufen Parameter als veraltet ein. Jedes dieser Ereignisse löst erneute Tests, Prompt-Anpassungen und manchmal eine Neubewertung des gesamten Features aus.
- **Compliance- und Sicherheitsprüfung.** Datenresidenz, Aufbewahrung, Listen von Unterauftragsverarbeitern, DPAs und inzwischen AI-spezifische Fragen von Kunden und App-Stores. Diese Arbeit fällt pro Feature einmalig an, wiederholt sich aber pro Anbieter und pro Jurisdiktion.
- **Support für probabilistische Software.** Nutzer melden Dinge, die schwer reproduzierbar sind, weil die Antwort jedes Mal anders ausfällt. Support-Werkzeuge und Playbooks müssen für diese Realität neu geschrieben werden.
- **Fehlerkosten.** Ein halluzinierter Preis, eine falsche Zusammenfassung in einer Vertragsprüfung, eine beleidigende Ausgabe, die einem Kunden angezeigt wird. In einem Kostenmodell tauchen sie vielleicht nie auf, aber sie sind der Grund, warum mehrere AI-Features stillschweigend zurückgezogen wurden.

Keiner dieser Posten taucht in einem Vergleich der „Kosten pro Million Tokens“ auf – genau deshalb werden sie leicht übersehen.

## Was die Belege über den Nutzen sagen

Die Verteilung des Nutzens ist ungleichmäßig. Zwei Arten von Belegen existieren im selben Markt nebeneinander.

Auf der einen Seite zeigen kontrollierte Messungen echte Gewinne bei eng umrissener Arbeit mit hohem Volumen: Ein randomisiertes GitHub-Experiment aus dem Jahr 2023 ergab, dass Entwickler mit einem AI-Assistenten eine Aufgabe 55,8 % schneller abschlossen (arXiv:2302.06590), und eine Studie zu Kundensupport-Werkzeugen fand im Durchschnitt etwa 14 % mehr pro Stunde gelöste Fälle, bei den unerfahrensten Mitarbeitenden rund 34 % (Brynjolfsson, Li & Raymond, NBER working paper 31161).

Auf der anderen Seite sind die Ergebnisse auf Portfolioebene schlecht. Eine MIT-Studie aus dem Jahr 2025 zu Generative-AI-Piloten in Unternehmen berichtete, dass die große Mehrheit keine messbaren Auswirkungen auf Gewinn und Verlust hatte, und eine S&P-Global-Umfrage aus dem Jahr 2024 ergab, dass ein großer Teil der Unternehmen die meisten ihrer AI-Initiativen aufgegeben hatte. Beide Befunde sind eher als Annäherungen an eine unübersichtliche Realität zu lesen denn als präzise Messungen – aber sie weisen in dieselbe Richtung.

Der Widerspruch ist nicht kompliziert aufzulösen. Gewinne entstehen dort, wo ein Workflow eine messbare Kennzahl, genug Volumen, um ins Gewicht zu fallen, und eine Ausgabe hat, die ein Mensch schnell prüfen kann. Verluste häufen sich dort, wo die Kennzahl nie definiert wurde, das Volumen gering war oder das Feature gebaut wurde, weil es möglich war, statt weil jemand für das Ergebnis verantwortlich war.

## Die Kalkulation, die den Ausschlag gibt

Schreiben Sie vor dem Bauen drei Zahlen auf:

1. **Kosten pro Aufgabe** mit dem Modell, einschließlich Wiederholungen, Prüfaufwand und anteiliger Wartung.
2. **Kosten pro Aufgabe heute**, alles eingerechnet – Gehalt, Werkzeuge, Fehlerkorrektur.
3. **Kosten eines Fehlers** und ob eine menschliche Prüfstufe sie begrenzt.

Ein AI-Feature ist vertretbar, wenn die erste Zahl nach Einrechnung der Prüfkosten deutlich unter der zweiten liegt, die dritte durch einen Prozess begrenzt wird, den Sie tatsächlich betreiben, und das Volumen hoch genug ist, dass sich der Unterschied kumuliert. Ist die dritte Zahl unbegrenzt – eine Entscheidung, die jemanden schädigen, gegen eine Vorschrift verstoßen oder eine Beziehung zerstören kann –, dann ist die Prüfstufe nicht optional und muss von Anfang an eingepreist werden.

Daraus folgen zwei Konsequenzen. Erstens sind einige der besten AI-Projekte klein: Sie ersetzen eine eng umrissene, repetitive Aufgabe mit hohem Volumen. Zweitens sollten manche Features abgelehnt werden. Das ist keine AI-feindliche Haltung; das ist es, was ein Budget tut.

## Wo AI schlicht das falsche Werkzeug ist

- **Deterministische Logik.** Steuerberechnung, Berechtigungsregeln, Bestandsrechnung. Regeln sind billiger, schneller, prüfbar und stabil. Ein Modell hinzuzufügen macht sie schlechter, nicht moderner.
- **Geringes Volumen.** Wenn eine Aufgabe fünfzig Mal im Monat läuft, werden die Fixkosten für ein Eval-Set, einen Prüfprozess und einen Wartungsverantwortlichen nie zurückverdient.
- **Schlechte Eingaben.** Wenn die zugrunde liegenden Daten unvollständig sind oder der Prozess undefiniert ist, produziert ein Modell selbstsicheren Unsinn in großem Maßstab. Reparieren Sie zuerst die Daten; das Modell hat sonst nichts, womit es arbeiten kann.
- **Unbegrenzte Fehlerkosten ohne Prüfung.** Wo ein Mensch ohnehin jede Ausgabe freigeben muss, fragen Sie ehrlich, ob das Modell überhaupt etwas gespart hat oder die Arbeit nur verschoben wurde.

## Ehrliche Budgetierung

Drei Gewohnheiten unterscheiden Teams, die Nutzen erzielen, von Teams, die Rechnungen erhalten.

**Setzen Sie eine Obergrenze, bevor Sie bauen.** Maximale Kosten pro erfolgreich erledigter Aufgabe und eine Volumenannahme. Wenn das Feature diese Obergrenze bei diesem Volumen nicht unterbietet, wird es nicht ausgeliefert – egal, wie gut die Demo war.

**Verfolgen Sie die Kosten pro erfolgreichem Ergebnis, nicht pro Aufruf.** Ein billiges Modell, das ein Drittel der Fälle nicht löst, ist teuer. Ein leistungsfähiges Modell nur für die schwierigen 20 % der Fälle einzusetzen und den Rest von einem kleinen Modell erledigen zu lassen, ist meist die günstigste verfügbare Architektur.

**Schreiben Sie das Abbruchkriterium vorab auf.** „Wenn die Qualität auf unserem Eval-Set bis Datum Y nicht X erreicht, hören wir auf.“ Fast jede AI-Initiative, die zu einem dauerhaften Kostenträger wird, begann als Pilot, den niemand beenden durfte.

Die Preise werden weiter fallen, und das hilft – aber günstigere Inference senkt weder den Prüfaufwand noch die Wartung oder die Kosten einer falschen Antwort. AI-first ist nicht die Entscheidung, AI überall einzusetzen. Es ist die Disziplin, die Stellen zu finden, an denen die Zahlen wirklich aufgehen, und den Mut zu haben, das zu sagen, wenn sie es nicht tun.

*Zum Weiterlesen: [AI-first ist eine Disziplin, kein Slogan](/blog/de/ai-first-is-a-discipline).*
