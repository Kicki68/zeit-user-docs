# Auto-Ausgangsrechnungen 

ZEIT.IO kann genehmigte Projektzeiten und Ausgaben automatisch abrechnen und die Rechnungen auch automatisch versenden.
Das spart Ihnen viel Zeit und reduziert Fehler.

## Wie funktioniert das Auto-Ausgangsrechnungsverfahren?

Das Auto-Ausgangsrechnungsverfahren hängt immer an einem Projekt und muss im Projekt explizit aktiviert werden.
Bei dem Verfahren werden genehmigte Zeiten und Ausgaben, aus einem bestimmten Zeitraum, automatisch in eine 
Rechnung umgewandelt und versendet. 

Mit dem Verfahren kann man z.B. ein genehmigtes Timesheet, direkt nach der Genehmigung, automatisch in eine Rechnung 
umwandeln und an den Kunden versenden. Oder man kann damit zeitgesteuert am Xten Tag des Monats alle genehmigten 
Zeiten und Ausgaben des Vormonats in eine Rechnung umwandeln und versenden.

Das Auto-Ausgangsrechnungsverfahren besteht aus den folgenden Komponenten:

- **Auslöser**: Der Auslöser bestimmt, wann die Rechnung erstellt und versendet wird. 
  Es gibt sowohl eventbasierte als auch zeitgesteuerte Auslöser. Der Ausslöser kann z.B.
  eine Genehmigung oder ein bestimmter Tag im Monat sein.
- **Rechnungsart**: Die Rechnungsart bestimmt, wie diese aussehen soll. 
- **Zielzustand**: Der Zielzustand bestimmt, ob die Rechnung in den Entwurf- oder in den Versandzustand übergehen soll.

## Wie konfiguriere ich das Auto-Ausgangsrechnungsverfahren?

Das Auto-Ausgangsrechnungsverfahren können Sie immer im Projekt konfigurieren. Das bedeutet auch, dass Sie in jedem
Projekt eine andere Konfiguration für das Auto-Ausgangsrechnungsverfahren wählen können. Dafür navigieren Sie einfach
zu dem Projekt, für das Sie das Auto-Ausgangsrechnungsverfahren konfigurieren wollen. Links unten im Seitenmenü finden
Sie den Punkt "Auto.-Ausgangsrechnungen", wo Sie dann die entsprecehnden Einstellungen vornehmen können.

## Auslöser konfigurieren

Der Auslöser bestimmt, wann die Rechnung erstellt und versendet werden soll. 
Es gibt eventbasierte und zeitgesteuerte Auslöser. 

### Eventbasierte Auslöser

- **Timesheet-Genehmigung**: Das Verfahren wird ausgelöst, wenn ein Timesheet zum aktuellen Projekt genehmigt wird.
  Die so erstellte Rechnung enthält alle genehmigten Zeiten, unabhängig davon,
  über welchen Zeitraum sich das Timesheet erstreckt. 
  Genehmigte Ausgaben aus dem gleichen Zeitraum und Projekt werden **nicht** in die Rechnung übernommen. 
  Die so erstellt Rechnung enthält ausschließlich die Positionen des genehmigten Timesheets.
- **Ausgaben-Genehmigung**: Das Verfahren wird ausgelöst, wenn eine Ausgabe zum aktuellen Projekt genehmigt wird.
  Die so erstellte Rechnung enthält alle genehmigten Ausgaben des Ausgabenbelegs, unabhängig davon,
  über welchen Zeitraum sie sich erstrecken. 
  Genehmigte Zeiten aus dem gleichen Zeitraum und Projekt werden **nicht** in die Rechnung übernommen. 
  Die so erstellt Rechnung enthält ausschließlich die Positionen der genehmigten Ausgaben.
- **Timesheet- ODER Ausgaben-Genehmigung**: Das Verfahren wird ausgelöst, wenn ein Timesheet **oder** eine Ausgabe zum aktuellen Projekt genehmigt wird. 
  Die so erstellte Rechnung enthält ausschließlich die Positionen des genehmigten Objektes, unabhängig davon,
  über welchen Zeitraum sich die Zeiten und Ausgaben erstrecken. 
  Dieser Auslöser generiert entweder eine Rechnung zu einem Timesheet oder zu einer Ausgabeneinreichung.

### Zeitgesteuerte Auslöser

- **Der Xte Tag des Monats**: Das Verfahren wird am Xten Tag des Monats ausgelöst. 
  Die so erstellte Rechnung enthält alle Zeiten und Ausgaben des Vormonats, die am Xten
  Tag genehmigt wurden. Der Tag des Monats kann zwischen 1 und 15 liegen. Genehmigungen,
  die nach dem Xten Tag erfolgen, müssen manuell abgerechnet werden. 
- **Tag X bis Tag Y des Monats**: Hierbei wird zwischen dem Xten und Yten Tag des Monats, jede Stunde geprüft, ob es genehmigte Zeiten oder Ausgaben aus dem Vormonat gibt, die noch nicht abgerechnet wurden. 
  Wenn das der Fall ist dann werden die Positionen abgerechnet. 

## Rechnungsart konfigurieren

Die Rechnungsart bestimmt, wie die Rechnung aussehen soll und welche Informationen sie enthalten soll. Aktuell gibt 
es die folgenden Rechnungsarten:

- **Projekt**: Alle gebuchten Zeiten und Spesen aus dem Projekt werden automatisch auf die Rechnung gesetzt. 
  Expertennamen und Projektaktivitäten tauchen auf dieser Rechnung nicht auf.
- **Experte**: Es wird je eine Rechnung pro Experte generiert. Auf der Rechnung erscheint das Projekt, der Name des Experten und der Abrechnungszeitraum.
- **Experten**: Es wird eine Rechnung generiert, bei der die Stunden nach Experten gruppiert sind.
- **Aktivitäten**: Es wird eine Rechnung generiert, bei der die Stunden nach Aktivitäten gruppiert sind.
- **Wartungsvertrag-Monatlich:** Es wird jeden Monat eine fixe Wartungspauschale abgerechnet, welche X Service-Stunden inkludiert. 
  Zusätzlich geleistete Stunden aus dem Projekt, die mit der Wartungspauschale nicht abgegolten sind, werden ebenfalls mit abgerechnet, wenn vorhanden.
- **Wartungsvertrag-Dacuro**: Es wird jeden Monat eine fixe Wartungspauschale abgerechnet, welche X Service-Stunden inkludiert. 
  Am Ende eines Quartals werden zusätzlich geleistete Stunden aus dem Projekt, die mit der Wartungspauschale nicht abgegolten sind, ebenfalls mit abgerechnet.

## Zielzustand konfigurieren

Bei dem Zielzustand handelt es sich um den Zustand, in den die Rechnung nach der Erstellung übergehen soll. 
Folgende Zustände sind möglich:

- **Entwurf**: Die Rechnung wird erstellt und in den Entwurf-Zustand überführt. Sie können die Rechnung dann noch einmal prüfen und ggf. anpassen, bevor Sie sie versenden.
- **Abgeschlossen**: Die Rechnung wird erstellt und in den Abgeschlossen-Zustand überführt. 
  Sie können sie dann nicht mehr bearbeiten, sondern nur noch versenden.
- **Abgeschlossen und versendet**: Die Rechnung wird erstellt, abgeschlossen und and den Kunden versendet. 
  Sie können sie dann nicht mehr bearbeiten.

Außerdem können hier noch Sprache, Datums-Format und E-Mail-Empfänger konfiguriert werden, sowie wie mögliche Leistungsnachweise an die Rechnung angehängt werden sollen.
