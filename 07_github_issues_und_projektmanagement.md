# 7. GitHub Issues und Projektmanagement

## Einführung in GitHub Issues

### Video-Tutorial: GitHub Issues
[Github Tutorial - Issues (Deutsch/German)](https://www.youtube.com/watch?v=wSHNvdRjB9Q)
[Wie du ein GitHub Issue erstellest | GitHub Tutorial Deutsch](https://www.youtube.com/watch?v=oWuFYthqIGA)

GitHub Issues ist ein leistungsstarkes Werkzeug zur Verfolgung von Aufgaben, Fehlern und Funktionsanfragen in Softwareprojekten. Es bildet das Rückgrat des Projektmanagements auf GitHub und ermöglicht es Teams, ihre Arbeit effektiv zu organisieren, zu priorisieren und zu verfolgen.

### Was sind GitHub Issues?

GitHub Issues sind digitale Einträge, die verschiedene Aspekte eines Projekts dokumentieren und verfolgen. Sie können für verschiedene Zwecke verwendet werden:

- **Fehlerverfolgung**: Dokumentation und Nachverfolgung von Softwarefehlern
- **Funktionsanfragen**: Vorschläge für neue Funktionen oder Verbesserungen
- **Aufgabenverwaltung**: Planung und Zuweisung von Arbeitsaufgaben
- **Diskussionen**: Plattform für projektbezogene Diskussionen und Entscheidungsfindung
- **Dokumentation**: Aufzeichnung wichtiger Informationen und Entscheidungen

Issues bieten eine zentrale Stelle, an der alle Projektbeteiligten zusammenarbeiten können, unabhängig von ihrer Rolle oder ihrem Standort. Sie fördern Transparenz, erleichtern die Kommunikation und verbessern die Nachvollziehbarkeit von Entscheidungen und Fortschritten.

### Anatomie eines Issues

Ein GitHub Issue besteht aus mehreren Komponenten, die zusammen einen umfassenden Überblick über eine bestimmte Aufgabe oder ein Problem bieten:

**Titel**: Eine kurze, beschreibende Überschrift, die das Hauptanliegen des Issues zusammenfasst. Ein guter Titel ist präzise und informativ, sodass andere Teammitglieder schnell verstehen können, worum es geht.

**Beschreibung**: Der Hauptteil des Issues, der detaillierte Informationen enthält. Eine gute Beschreibung umfasst:
- Kontext und Hintergrundinformationen
- Detaillierte Erklärung des Problems oder der Aufgabe
- Bei Fehlern: Schritte zur Reproduktion, erwartetes vs. tatsächliches Verhalten
- Relevante Screenshots oder Videos
- Umgebungsinformationen (Betriebssystem, Browser, Versionen etc.)

**Labels**: Farbige Tags, die helfen, Issues zu kategorisieren und zu filtern. GitHub bietet standardmäßig einige Labels wie "bug", "enhancement" oder "documentation", aber Teams können auch eigene Labels erstellen, die ihren spezifischen Bedürfnissen entsprechen.

**Assignees**: Personen, die für die Bearbeitung des Issues verantwortlich sind. Die Zuweisung von Issues hilft, Verantwortlichkeiten klar zu definieren und sicherzustellen, dass jede Aufgabe einen Eigentümer hat.

**Meilensteine**: Gruppierungen von Issues, die zu einem bestimmten Ziel oder Zeitrahmen gehören, wie ein Release oder ein Sprint. Meilensteine helfen, den Fortschritt in Richtung größerer Ziele zu verfolgen.

**Kommentare**: Diskussionen und Updates zum Issue. Kommentare ermöglichen es Teammitgliedern, Informationen auszutauschen, Fragen zu stellen, Fortschritte zu melden und Entscheidungen zu dokumentieren.

**Verknüpfungen**: Verbindungen zu anderen Issues, Pull Requests oder externen Ressourcen. Verknüpfungen helfen, Beziehungen zwischen verschiedenen Aspekten des Projekts zu verstehen und zu navigieren.

**Status**: Ein Issue kann offen oder geschlossen sein. Offene Issues repräsentieren Aufgaben oder Probleme, die noch bearbeitet werden müssen, während geschlossene Issues abgeschlossene oder nicht mehr relevante Einträge darstellen.

### Issues erstellen und verwalten

Die Erstellung und Verwaltung von Issues ist ein grundlegender Aspekt der Arbeit mit GitHub. Hier ist ein Überblick über den Prozess:

**Issues erstellen**:

1. Navigieren Sie zum Repository, in dem Sie ein Issue erstellen möchten.
2. Klicken Sie auf die Registerkarte "Issues".
3. Klicken Sie auf die grüne Schaltfläche "New issue".
4. Wenn das Repository Issue-Templates verwendet, wählen Sie die passende Vorlage aus oder klicken Sie auf "Open a blank issue".
5. Geben Sie einen aussagekräftigen Titel ein.
6. Verfassen Sie eine detaillierte Beschreibung, idealerweise mit Markdown-Formatierung für bessere Lesbarkeit.
7. Fügen Sie bei Bedarf Labels, Assignees, Projekte und Meilensteine hinzu.
8. Klicken Sie auf "Submit new issue".

**Issues verwalten**:

Die effektive Verwaltung von Issues ist entscheidend für ein erfolgreiches Projektmanagement. Hier sind einige wichtige Aspekte:

*Priorisierung*: Nicht alle Issues sind gleich wichtig. Teams sollten klare Kriterien für die Priorisierung von Issues haben, basierend auf Faktoren wie Geschäftsauswirkung, Kundenbedarf, technische Dringlichkeit und Abhängigkeiten. Labels wie "priority: high", "priority: medium" und "priority: low" können helfen, die Priorität visuell darzustellen.

*Kategorisierung*: Die Verwendung von Labels zur Kategorisierung von Issues nach Typ (bug, feature, documentation), Komponente (frontend, backend, database) oder Status (ready for development, in progress, needs review) erleichtert die Organisation und Filterung.

*Zuweisung*: Die Zuweisung von Issues an bestimmte Teammitglieder stellt sicher, dass jede Aufgabe einen klaren Eigentümer hat. Es ist wichtig, die Arbeitslast gleichmäßig zu verteilen und die Fähigkeiten und Interessen der Teammitglieder zu berücksichtigen.

*Verfolgung*: Regelmäßige Überprüfungen des Issue-Status helfen, den Fortschritt zu verfolgen und sicherzustellen, dass nichts übersehen wird. Teams können wöchentliche Issue-Triage-Meetings abhalten, um neue Issues zu bewerten und bestehende zu aktualisieren.

*Schließen*: Ein Issue sollte geschlossen werden, wenn die zugehörige Aufgabe abgeschlossen ist oder das Problem nicht mehr relevant ist. Es ist wichtig, beim Schließen eines Issues eine klare Erklärung zu geben, insbesondere wenn es nicht gelöst wurde.

### Issue-Templates

Issue-Templates sind vordefinierte Strukturen, die als Leitfaden für die Erstellung neuer Issues dienen. Sie helfen, konsistente und vollständige Informationen zu gewährleisten und den Prozess der Issue-Erstellung zu standardisieren.

**Vorteile von Issue-Templates**:

- Förderung von Konsistenz und Vollständigkeit in Issue-Beschreibungen
- Vereinfachung des Issue-Erstellungsprozesses für Beitragende
- Reduzierung der Zeit, die für Nachfragen nach fehlenden Informationen benötigt wird
- Verbesserung der Qualität und Nützlichkeit von Issues

**Erstellen von Issue-Templates**:

1. Erstellen Sie ein Verzeichnis `.github/ISSUE_TEMPLATE/` in Ihrem Repository.
2. Erstellen Sie Markdown-Dateien für verschiedene Issue-Typen, z.B. `bug_report.md`, `feature_request.md`, `documentation.md`.
3. Jede Template-Datei sollte mit YAML-Frontmatter beginnen, das Metadaten wie Name, Beschreibung und Labels definiert:

```yaml
---
name: Bug Report
about: Erstellen Sie einen Bericht, um uns bei der Verbesserung zu helfen
title: '[BUG] '
labels: bug
assignees: ''
---
```

4. Fügen Sie nach dem Frontmatter den Inhalt des Templates hinzu, der als Leitfaden für den Issue-Ersteller dient:

```markdown
## Beschreibung des Fehlers
Eine klare und präzise Beschreibung des Fehlers.

## Reproduktionsschritte
Schritte, um das Verhalten zu reproduzieren:
1. Gehen Sie zu '...'
2. Klicken Sie auf '....'
3. Scrollen Sie nach unten zu '....'
4. Sehen Sie den Fehler

## Erwartetes Verhalten
Eine klare und präzise Beschreibung dessen, was Sie erwartet haben.

## Screenshots
Falls zutreffend, fügen Sie Screenshots hinzu, um Ihr Problem zu erklären.

## Umgebung
- Betriebssystem: [z.B. Windows 10]
- Browser: [z.B. Chrome 91.0]
- Version: [z.B. 1.2.3]

## Zusätzlicher Kontext
Fügen Sie hier weiteren Kontext zum Problem hinzu.
```

5. Committen und pushen Sie die Template-Dateien zu Ihrem Repository.

Sobald die Templates eingerichtet sind, werden sie automatisch angezeigt, wenn jemand ein neues Issue erstellt. Der Benutzer kann dann das passende Template auswählen und die vorgegebenen Felder ausfüllen.

**Konfiguration von Issue-Templates**:

Für eine erweiterte Konfiguration können Sie eine `config.yml`-Datei im `.github/ISSUE_TEMPLATE/`-Verzeichnis erstellen:

```yaml
blank_issues_enabled: false
contact_links:
  - name: GitHub Community Support
    url: https://github.community/
    about: Bitte stellen Sie Fragen zur GitHub-Nutzung hier.
  - name: Sicherheitslücke melden
    url: https://example.com/security
    about: Bitte melden Sie Sicherheitslücken hier.
```

Diese Konfiguration kann verwendet werden, um leere Issues zu deaktivieren und alternative Kontaktmöglichkeiten für bestimmte Anliegen anzubieten.

## GitHub Projektmanagement-Tools

GitHub bietet eine Reihe von Werkzeugen, die speziell für das Projektmanagement entwickelt wurden. Diese Tools helfen Teams, ihre Arbeit zu organisieren, zu visualisieren und zu verfolgen.

### Projektboards

GitHub Projektboards sind flexible Tools zur Organisation und Priorisierung von Arbeit. Sie verwenden Karten, Spalten und Automatisierung, um Issues, Pull Requests und Notizen zu verwalten.

**Arten von Projektboards**:

- **Repository-Projektboards**: Spezifisch für ein einzelnes Repository. Diese sind ideal für die Verwaltung von Arbeit innerhalb eines bestimmten Projekts.
- **Organisations-Projektboards**: Können Issues und Pull Requests aus mehreren Repositories innerhalb einer Organisation enthalten. Diese sind nützlich für die Koordination von Arbeit über verschiedene Projekte hinweg.
- **Benutzer-Projektboards**: Persönliche Projektboards, die von einzelnen Benutzern erstellt werden können, um ihre eigene Arbeit zu organisieren.

**Erstellen eines Projektboards**:

1. Navigieren Sie zum Repository, zur Organisation oder zu Ihrem persönlichen Dashboard.
2. Klicken Sie auf die Registerkarte "Projects".
3. Klicken Sie auf "New project".
4. Geben Sie einen Namen und eine Beschreibung ein.
5. Wählen Sie ein Projektvorlage (Kanban, Basic, Automated Kanban, etc.).
6. Klicken Sie auf "Create project".

**Projektboard-Spalten**:

Projektboards bestehen aus Spalten, die den Workflow repräsentieren. Typische Spalten könnten sein:

- **To Do**: Aufgaben, die noch nicht begonnen wurden
- **In Progress**: Aufgaben, an denen aktuell gearbeitet wird
- **Review**: Aufgaben, die überprüft werden müssen
- **Done**: Abgeschlossene Aufgaben

Sie können Spalten hinzufügen, umbenennen, neu anordnen oder löschen, um Ihren spezifischen Workflow abzubilden.

**Karten zu Projektboards hinzufügen**:

Karten repräsentieren einzelne Arbeitseinheiten auf einem Projektboard. Es gibt drei Arten von Karten:

1. **Issues**: Bestehende Issues aus dem Repository oder der Organisation
2. **Pull Requests**: Bestehende Pull Requests aus dem Repository oder der Organisation
3. **Notizen**: Kurze Textnotizen, die direkt auf dem Projektboard erstellt werden können

Um Karten hinzuzufügen:
- Klicken Sie auf das "+" Symbol in einer Spalte
- Wählen Sie "Add cards" und ziehen Sie Issues oder Pull Requests auf das Board
- Oder wählen Sie "Add note" und geben Sie Text ein

**Automatisierung in Projektboards**:

GitHub bietet Automatisierungsfunktionen, die den Projektmanagement-Workflow vereinfachen:

- **Automatisches Hinzufügen**: Neue Issues oder Pull Requests können automatisch zu einer bestimmten Spalte hinzugefügt werden.
- **Automatisches Verschieben**: Karten können automatisch zwischen Spalten verschoben werden, basierend auf bestimmten Ereignissen:
  - Wenn ein Issue oder Pull Request zugewiesen wird
  - Wenn ein Pull Request geöffnet wird
  - Wenn ein Pull Request genehmigt wird
  - Wenn ein Issue oder Pull Request geschlossen wird

Um Automatisierung zu konfigurieren:
1. Klicken Sie auf das Menü einer Spalte (drei Punkte)
2. Wählen Sie "Manage automation"
3. Aktivieren oder deaktivieren Sie die gewünschten Automatisierungsregeln

**Best Practices für Projektboards**:

- **Halten Sie es einfach**: Beginnen Sie mit einem einfachen Workflow und erweitern Sie ihn bei Bedarf.
- **Regelmäßige Überprüfungen**: Führen Sie regelmäßige Team-Meetings durch, um das Projektboard zu überprüfen und zu aktualisieren.
- **Klare Verantwortlichkeiten**: Stellen Sie sicher, dass jede Karte einen klaren Eigentümer hat.
- **Konsistente Labels**: Verwenden Sie konsistente Labels, um Karten zu kategorisieren und zu priorisieren.
- **Archivieren Sie abgeschlossene Karten**: Halten Sie Ihr Board aufgeräumt, indem Sie abgeschlossene Karten regelmäßig archivieren.

### Meilensteine

Meilensteine sind ein Werkzeug zur Gruppierung von Issues und Pull Requests für ein bestimmtes Ziel oder einen Zeitrahmen. Sie sind besonders nützlich für die Planung von Releases, Sprints oder anderen zeitlich begrenzten Projekten.

**Erstellen eines Meilensteins**:

1. Navigieren Sie zum Repository.
2. Klicken Sie auf die Registerkarte "Issues".
3. Klicken Sie auf "Milestones".
4. Klicken Sie auf "New milestone".
5. Geben Sie einen Titel, ein optionales Fälligkeitsdatum und eine Beschreibung ein.
6. Klicken Sie auf "Create milestone".

**Meilensteine verwalten**:

- **Issues und Pull Requests zuweisen**: Beim Erstellen oder Bearbeiten eines Issues oder Pull Requests können Sie einen Meilenstein auswählen.
- **Fortschritt verfolgen**: Meilensteine zeigen eine Fortschrittsanzeige, die den Prozentsatz abgeschlossener Issues anzeigt.
- **Filtern nach Meilensteinen**: Sie können Issues und Pull Requests nach Meilensteinen filtern, um alle Elemente zu sehen, die zu einem bestimmten Ziel gehören.
- **Meilensteine schließen**: Wenn alle Issues und Pull Requests eines Meilensteins abgeschlossen sind, können Sie den Meilenstein schließen, um ihn als erledigt zu markieren.

**Best Practices für Meilensteine**:

- **Klare Ziele**: Jeder Meilenstein sollte ein klares, messbares Ziel haben.
- **Realistische Zeitrahmen**: Setzen Sie realistische Fälligkeitsdaten, die den Umfang der Arbeit und die verfügbaren Ressourcen berücksichtigen.
- **Regelmäßige Überprüfungen**: Überprüfen Sie regelmäßig den Fortschritt der Meilensteine und passen Sie bei Bedarf den Umfang oder das Fälligkeitsdatum an.
- **Dokumentation**: Verwenden Sie die Meilenstein-Beschreibung, um wichtige Informationen wie Ziele, Kriterien für den Abschluss und Abhängigkeiten zu dokumentieren.

### Labels

Labels sind farbige Tags, die helfen, Issues und Pull Requests zu kategorisieren und zu organisieren. Sie sind ein einfaches, aber leistungsstarkes Werkzeug für das Projektmanagement.

**Standardlabels**:

GitHub bietet standardmäßig einige Labels:
- `bug`: Etwas funktioniert nicht wie erwartet
- `documentation`: Verbesserungen oder Ergänzungen der Dokumentation
- `duplicate`: Dieses Issue oder dieser Pull Request existiert bereits
- `enhancement`: Neue Funktion oder Anfrage
- `good first issue`: Gut für Erstbeitragende
- `help wanted`: Zusätzliche Aufmerksamkeit wird benötigt
- `invalid`: Dies scheint nicht richtig zu sein
- `question`: Weitere Informationen werden angefordert
- `wontfix`: Daran wird nicht gearbeitet

**Benutzerdefinierte Labels erstellen**:

1. Navigieren Sie zum Repository.
2. Klicken Sie auf die Registerkarte "Issues".
3. Klicken Sie auf "Labels".
4. Klicken Sie auf "New label".
5. Geben Sie einen Namen, eine Beschreibung und eine Farbe ein.
6. Klicken Sie auf "Create label".

**Effektive Verwendung von Labels**:

Labels können für verschiedene Zwecke verwendet werden:

*Kategorisierung*: Verwenden Sie Labels, um Issues nach Typ zu kategorisieren (bug, feature, documentation).

*Priorisierung*: Erstellen Sie Labels wie "priority: high", "priority: medium" und "priority: low", um die Dringlichkeit anzuzeigen.

*Status*: Verwenden Sie Labels wie "status: ready for development", "status: in progress", "status: needs review", um den aktuellen Status anzuzeigen.

*Komponenten*: Kennzeichnen Sie Issues nach den betroffenen Komponenten (frontend, backend, database).

*Komplexität*: Verwenden Sie Labels wie "complexity: easy", "complexity: medium", "complexity: hard", um den Schwierigkeitsgrad anzuzeigen.

*Release-Planung*: Erstellen Sie Labels für bestimmte Releases oder Versionen (v1.0, v1.1, v2.0).

**Best Practices für Labels**:

- **Konsistentes Namensschema**: Verwenden Sie ein konsistentes Namensschema für verwandte Labels, z.B. "priority: high", "priority: medium", "priority: low".
- **Farbkodierung**: Verwenden Sie Farben sinnvoll, z.B. Rot für Bugs, Grün für Funktionen, Blau für Dokumentation.
- **Dokumentation**: Fügen Sie Beschreibungen zu Ihren Labels hinzu, damit andere verstehen, wofür sie verwendet werden.
- **Regelmäßige Überprüfung**: Überprüfen Sie regelmäßig Ihre Labels und entfernen Sie nicht verwendete oder redundante Labels.
- **Begrenzte Anzahl**: Vermeiden Sie zu viele Labels, da dies die Übersichtlichkeit beeinträchtigen kann. Konzentrieren Sie sich auf die wichtigsten Kategorisierungen.

### GitHub Projects (neue Version)

GitHub hat eine neue Version von Projects eingeführt, die leistungsfähiger und flexibler ist als die klassischen Projektboards. Diese neue Version, oft als "GitHub Projects (Beta)" oder einfach "Projects" bezeichnet, bietet tabellarische und Kanban-Ansichten, benutzerdefinierte Felder und erweiterte Filtermöglichkeiten.

**Hauptmerkmale von GitHub Projects**:

*Flexible Ansichten*: Wechseln Sie zwischen Tabellen-, Board- und Roadmap-Ansichten, je nach Ihren Bedürfnissen.

*Benutzerdefinierte Felder*: Erstellen Sie benutzerdefinierte Felder wie Dropdown-Menüs, Datumsfelder, Zahlenfelder und mehr, um zusätzliche Informationen zu erfassen.

*Gruppierung und Sortierung*: Gruppieren und sortieren Sie Elemente nach beliebigen Feldern, um verschiedene Perspektiven auf Ihre Arbeit zu erhalten.

*Filterung*: Erstellen Sie komplexe Filter, um genau die Elemente zu finden, die Sie benötigen.

*Automatisierung*: Konfigurieren Sie Workflows, die automatisch Feldwerte aktualisieren, basierend auf bestimmten Ereignissen.

*Integrationen*: Verbinden Sie Projects mit GitHub Issues, Pull Requests und Discussions für eine nahtlose Erfahrung.

**Erstellen eines neuen Projects**:

1. Navigieren Sie zum Repository oder zur Organisation.
2. Klicken Sie auf die Registerkarte "Projects".
3. Klicken Sie auf "New project".
4. Wählen Sie eine Vorlage oder beginnen Sie mit einem leeren Projekt.
5. Geben Sie einen Namen und eine Beschreibung ein.
6. Klicken Sie auf "Create".

**Anpassen von Projects**:

*Felder hinzufügen*:
1. Klicken Sie auf das "+" Symbol in der Kopfzeile.
2. Wählen Sie einen Feldtyp (Text, Zahl, Datum, Single select, etc.).
3. Geben Sie einen Namen und Standardwerte ein.
4. Klicken Sie auf "Save".

*Ansichten erstellen*:
1. Klicken Sie auf das Dropdown-Menü "Views" in der oberen linken Ecke.
2. Wählen Sie "New view".
3. Wählen Sie einen Ansichtstyp (Table, Board, Roadmap).
4. Geben Sie einen Namen ein und konfigurieren Sie die Ansicht.
5. Klicken Sie auf "Save".

*Filter und Gruppierungen*:
1. Klicken Sie auf "Filter" oder "Group by" in der Kopfzeile.
2. Wählen Sie ein Feld und einen Wert zum Filtern oder Gruppieren.
3. Fügen Sie bei Bedarf weitere Filter hinzu.

**Workflows und Automatisierung**:

GitHub Projects ermöglicht die Konfiguration von Workflows, die automatisch Feldwerte aktualisieren:

1. Klicken Sie auf das Menü (drei Punkte) in der oberen rechten Ecke.
2. Wählen Sie "Workflows".
3. Wählen Sie einen vordefinierten Workflow oder erstellen Sie einen benutzerdefinierten.
4. Konfigurieren Sie die Bedingungen und Aktionen.
5. Klicken Sie auf "Save".

Beispiele für Workflows:
- Automatisches Setzen des Status auf "In Progress", wenn ein Issue einem Benutzer zugewiesen wird
- Automatisches Setzen des Status auf "Done", wenn ein Issue geschlossen wird
- Automatisches Aktualisieren des Fälligkeitsdatums, wenn ein Meilenstein aktualisiert wird

**Best Practices für GitHub Projects**:

- **Beginnen Sie einfach**: Starten Sie mit einer einfachen Struktur und erweitern Sie sie nach Bedarf.
- **Dokumentieren Sie Ihre Prozesse**: Erstellen Sie eine Dokumentation, die erklärt, wie Ihr Team Projects verwendet.
- **Regelmäßige Überprüfungen**: Führen Sie regelmäßige Team-Meetings durch, um Projects zu überprüfen und zu aktualisieren.
- **Nutzen Sie Automatisierung**: Automatisieren Sie so viel wie möglich, um manuelle Aktualisierungen zu reduzieren.
- **Experimentieren Sie mit Ansichten**: Nutzen Sie verschiedene Ansichten, um verschiedene Perspektiven auf Ihre Arbeit zu erhalten.

## Agile Projektmanagement mit GitHub

GitHub bietet alle notwendigen Werkzeuge, um agile Projektmanagement-Methoden wie Scrum oder Kanban zu implementieren. Mit einigen Anpassungen und Best Practices können Teams GitHub effektiv für agile Entwicklung nutzen.

### Scrum mit GitHub

Scrum ist ein agiles Framework, das auf iterativer und inkrementeller Entwicklung basiert. Es umfasst feste Zeiträume (Sprints), regelmäßige Meetings und spezifische Rollen.

**Einrichten von Scrum mit GitHub**:

*Backlog verwalten*:
- Verwenden Sie Issues, um User Stories, Tasks und Bugs zu repräsentieren.
- Nutzen Sie Labels wie "user story", "task", "bug" zur Kategorisierung.
- Verwenden Sie Meilensteine für Sprints.
- Nutzen Sie ein Projektboard mit einer Spalte für den Product Backlog.

*Sprints planen*:
1. Erstellen Sie einen Meilenstein für jeden Sprint mit einem klaren Fälligkeitsdatum.
2. Weisen Sie Issues dem Sprint-Meilenstein zu.
3. Verwenden Sie ein Projektboard mit Spalten wie "Sprint Backlog", "In Progress", "Review" und "Done".
4. Schätzen Sie den Aufwand mit benutzerdefinierten Feldern oder Labels (z.B. "effort: 1", "effort: 2", etc.).

*Daily Scrums*:
- Verwenden Sie GitHub Discussions oder externe Tools für tägliche Updates.
- Jedes Teammitglied kann kommentieren, was es gestern getan hat, was es heute tun wird und ob es Hindernisse gibt.

*Sprint Review und Retrospektive*:
- Erstellen Sie ein Issue für jede Retrospektive, um Diskussionen und Aktionspunkte zu dokumentieren.
- Verwenden Sie GitHub Releases, um abgeschlossene Arbeit am Ende eines Sprints zu markieren.
- Nutzen Sie GitHub Pages, um Sprint-Demos zu hosten.

**Best Practices für Scrum mit GitHub**:

- **Klare Definitionen**: Definieren Sie klar, was "Ready" und "Done" bedeutet.
- **Konsistente Labels**: Verwenden Sie konsistente Labels für User Stories, Tasks, Bugs und Prioritäten.
- **Automatisierung**: Nutzen Sie GitHub Actions, um repetitive Aufgaben zu automatisieren.
- **Burndown-Charts**: Verwenden Sie GitHub API und externe Tools, um Burndown-Charts zu erstellen.
- **Regelmäßige Überprüfungen**: Führen Sie regelmäßige Backlog-Grooming-Sessions durch, um Issues zu priorisieren und zu verfeinern.

### Kanban mit GitHub

Kanban ist ein agiles Framework, das sich auf kontinuierlichen Fluss und visuelle Darstellung der Arbeit konzentriert. Es hat keine festen Zeiträume und betont die Begrenzung der Arbeit in Bearbeitung (WIP).

**Einrichten von Kanban mit GitHub**:

*Kanban-Board erstellen*:
1. Erstellen Sie ein Projektboard mit Spalten wie "Backlog", "Ready", "In Progress", "Review" und "Done".
2. Konfigurieren Sie WIP-Limits für jede Spalte (z.B. mit einer Notiz am Anfang der Spalte: "WIP Limit: 3").
3. Aktivieren Sie die Automatisierung, um Karten basierend auf Issue- und PR-Status zu verschieben.

*Arbeit visualisieren*:
- Verwenden Sie Issues für alle Arbeitseinheiten.
- Nutzen Sie Labels zur Kategorisierung und Priorisierung.
- Fügen Sie Assignees hinzu, um Verantwortlichkeiten klar zu machen.
- Verwenden Sie benutzerdefinierte Felder für zusätzliche Informationen wie Schätzungen oder Klassen von Service.

*Fluss messen*:
- Verfolgen Sie die Durchlaufzeit (Zeit, die ein Issue benötigt, um von "Ready" bis "Done" zu gelangen).
- Überwachen Sie die Anzahl der Issues in jeder Spalte, um Engpässe zu identifizieren.
- Verwenden Sie GitHub API und externe Tools, um Metriken wie Durchlaufzeit und Durchsatz zu berechnen.

**Best Practices für Kanban mit GitHub**:

- **WIP-Limits einhalten**: Respektieren Sie die WIP-Limits, um Überlastung zu vermeiden und den Fluss zu verbessern.
- **Regelmäßige Überprüfungen**: Führen Sie regelmäßige Kanban-Meetings durch, um das Board zu überprüfen und Prozesse zu verbessern.
- **Kontinuierliche Verbesserung**: Nutzen Sie Metriken, um Ihren Prozess kontinuierlich zu verbessern.
- **Klare Richtlinien**: Definieren Sie klare Richtlinien für den Übergang von Issues zwischen Spalten.
- **Visualisierung von Blockaden**: Verwenden Sie Labels oder Notizen, um blockierte Issues hervorzuheben.

### Metriken und Berichte

Die Messung und Visualisierung von Projektmetriken ist ein wichtiger Aspekt des agilen Projektmanagements. GitHub bietet Grundfunktionen für Metriken, aber für fortgeschrittenere Berichte können externe Tools oder benutzerdefinierte Skripte erforderlich sein.

**Grundlegende Metriken in GitHub**:

*Issue-Statistiken*:
- Anzahl der offenen vs. geschlossenen Issues
- Issues nach Labels, Assignees oder Meilensteinen
- Durchschnittliche Zeit bis zum Schließen von Issues

*Pull-Request-Statistiken*:
- Anzahl der offenen vs. geschlossenen Pull Requests
- Durchschnittliche Zeit bis zum Zusammenführen
- Anzahl der Kommentare und Reviews

*Meilenstein-Fortschritt*:
- Prozentsatz abgeschlossener Issues pro Meilenstein
- Verbleibende Zeit bis zum Fälligkeitsdatum

**Erweiterte Metriken und Berichte**:

Für fortgeschrittenere Metriken und Berichte können Sie die GitHub API verwenden, um Daten zu extrahieren und zu analysieren:

*Burndown-Charts*:
- Zeigen den Fortschritt während eines Sprints
- Vergleichen die tatsächliche Arbeit mit der geplanten Arbeit

*Durchlaufzeit*:
- Misst die Zeit, die ein Issue benötigt, um von der Erstellung bis zum Abschluss zu gelangen
- Hilft, die Effizienz des Entwicklungsprozesses zu verstehen

*Durchsatz*:
- Misst die Anzahl der abgeschlossenen Issues pro Zeiteinheit
- Hilft, die Kapazität des Teams zu verstehen

*Kumulatives Flussdiagramm*:
- Zeigt die Anzahl der Issues in verschiedenen Stadien im Laufe der Zeit
- Hilft, Engpässe und Trends zu identifizieren

**Tools für Metriken und Berichte**:

*GitHub-eigene Tools*:
- GitHub Insights: Bietet grundlegende Metriken für Repositories
- GitHub Projects: Ermöglicht die Visualisierung und Filterung von Daten

*Externe Tools*:
- ZenHub: Erweitert GitHub um agile Funktionen wie Burndown-Charts und Velocity-Tracking
- Jira: Kann mit GitHub integriert werden für umfassenderes Projektmanagement
- Grafana: Kann mit der GitHub API verbunden werden, um benutzerdefinierte Dashboards zu erstellen

*Benutzerdefinierte Lösungen*:
- Verwenden Sie die GitHub API mit Skriptsprachen wie Python oder JavaScript
- Speichern Sie Daten in einer Datenbank für historische Analysen
- Erstellen Sie benutzerdefinierte Dashboards mit Tools wie Tableau oder Power BI

**Best Practices für Metriken und Berichte**:

- **Fokus auf Wert**: Konzentrieren Sie sich auf Metriken, die tatsächlichen Wert für Ihr Team und Projekt liefern.
- **Kontext beachten**: Interpretieren Sie Metriken immer im Kontext des Projekts und des Teams.
- **Transparenz**: Teilen Sie Metriken und Berichte mit dem gesamten Team, um Transparenz zu fördern.
- **Kontinuierliche Verbesserung**: Verwenden Sie Metriken, um Bereiche für Verbesserungen zu identifizieren.
- **Nicht nur Zahlen**: Ergänzen Sie quantitative Metriken mit qualitativen Feedback und Diskussionen.

## Integration mit externen Tools

GitHub bietet eine Vielzahl von Integrationen mit externen Tools, die das Projektmanagement erweitern und verbessern können. Diese Integrationen ermöglichen es Teams, GitHub mit ihren bestehenden Workflows und Tools zu verbinden.

### GitHub Apps und Marketplace

Der GitHub Marketplace ist ein zentraler Ort, an dem Sie Apps und Aktionen finden können, die mit GitHub integriert werden können. Diese Apps erweitern die Funktionalität von GitHub und können für verschiedene Zwecke verwendet werden, von der Codequalität bis zum Projektmanagement.

**Beliebte Projektmanagement-Apps**:

*ZenHub*:
- Fügt agile Funktionen direkt in die GitHub-Oberfläche ein
- Bietet Funktionen wie Epics, Velocity-Tracking und Burndown-Charts
- Ermöglicht mehrere Projektboards und Repository-übergreifende Planung

*Jira Software*:
- Verbindet Jira-Issues mit GitHub-Repositories
- Synchronisiert Commits, Branches und Pull Requests mit Jira-Issues
- Ermöglicht die Nutzung von Jiras umfangreichen Projektmanagement-Funktionen

*Trello*:
- Verbindet Trello-Karten mit GitHub-Issues und Pull Requests
- Automatisiert die Aktualisierung von Trello-Karten basierend auf GitHub-Aktivitäten
- Bietet eine visuelle Kanban-Oberfläche für die Arbeitsverwaltung

*Monday.com*:
- Integriert GitHub-Issues und Pull Requests in Monday.com-Boards
- Ermöglicht die Verwaltung von Entwicklungsarbeit im Kontext anderer Projektaktivitäten
- Bietet umfangreiche Visualisierungs- und Berichtsoptionen

**Installation und Konfiguration von Apps**:

1. Navigieren Sie zum [GitHub Marketplace](https://github.com/marketplace).
2. Suchen Sie nach der gewünschten App oder filtern Sie nach Kategorie.
3. Klicken Sie auf die App und wählen Sie einen Plan (viele Apps bieten kostenlose Pläne oder Testversionen).
4. Klicken Sie auf "Install it for free" oder den entsprechenden Button für kostenpflichtige Pläne.
5. Wählen Sie, ob Sie die App für alle Repositories oder nur für ausgewählte installieren möchten.
6. Folgen Sie den spezifischen Konfigurationsschritten für die jeweilige App.

**Erstellen eigener GitHub Apps**:

Wenn keine bestehende App Ihren Anforderungen entspricht, können Sie Ihre eigene GitHub App erstellen:

1. Navigieren Sie zu Ihren GitHub-Einstellungen.
2. Klicken Sie auf "Developer settings" > "GitHub Apps" > "New GitHub App".
3. Geben Sie die erforderlichen Informationen ein und konfigurieren Sie die Berechtigungen.
4. Implementieren Sie die Logik für Ihre App mit einer Programmiersprache Ihrer Wahl.
5. Hosten Sie Ihre App auf einem Server oder einer Plattform wie Heroku oder AWS.

### Webhooks und API-Integration

Webhooks und die GitHub API bieten leistungsstarke Möglichkeiten zur Integration von GitHub mit externen Systemen und zur Automatisierung von Workflows.

**Webhooks**:

Webhooks sind HTTP-Callbacks, die ausgelöst werden, wenn bestimmte Ereignisse in einem Repository auftreten. Sie können verwendet werden, um externe Systeme über GitHub-Aktivitäten zu informieren.

*Einrichten von Webhooks*:
1. Navigieren Sie zu den Repository-Einstellungen.
2. Klicken Sie auf "Webhooks" > "Add webhook".
3. Geben Sie die Payload-URL ein (die URL, an die GitHub Ereignisse senden soll).
4. Wählen Sie den Content-Typ (application/json oder application/x-www-form-urlencoded).
5. Konfigurieren Sie ein optionales Secret für die Sicherheit.
6. Wählen Sie die Ereignisse aus, die den Webhook auslösen sollen.
7. Klicken Sie auf "Add webhook".

*Anwendungsfälle für Webhooks*:
- Auslösen von CI/CD-Pipelines
- Aktualisieren externer Projektmanagement-Tools
- Benachrichtigung von Team-Chat-Plattformen wie Slack oder Discord
- Aktualisierung von Dokumentation oder Websites
- Ausführung von benutzerdefinierten Skripten oder Workflows

**GitHub API**:

Die GitHub API ermöglicht programmatischen Zugriff auf fast alle Funktionen von GitHub. Sie kann verwendet werden, um benutzerdefinierte Integrationen und Automatisierungen zu erstellen.

*Verwendung der GitHub API*:
1. Erstellen Sie ein persönliches Zugriffstoken oder eine GitHub App für die Authentifizierung.
2. Verwenden Sie HTTP-Anfragen, um mit der API zu interagieren.
3. Verarbeiten Sie die JSON-Antworten, um Daten zu extrahieren oder Aktionen auszuführen.

*Beispiel für eine API-Anfrage in Python*:
```python
import requests

# Authentifizierung mit persönlichem Zugriffstoken
headers = {
    'Authorization': 'token YOUR_PERSONAL_ACCESS_TOKEN',
    'Accept': 'application/vnd.github.v3+json'
}

# Issues in einem Repository abrufen
response = requests.get(
    'https://api.github.com/repos/OWNER/REPO/issues',
    headers=headers
)

issues = response.json()
for issue in issues:
    print(f"#{issue['number']}: {issue['title']}")
```

*Anwendungsfälle für die GitHub API*:
- Erstellung benutzerdefinierter Dashboards und Berichte
- Automatisierung von Repository-Verwaltungsaufgaben
- Implementierung benutzerdefinierter Workflows
- Integration mit internen Systemen und Datenbanken
- Erstellung von Bots für Repository-Wartung und Code-Reviews

**Best Practices für Integrationen**:

- **Sicherheit**: Verwenden Sie Secrets für Webhooks und sichere Authentifizierung für API-Anfragen.
- **Fehlerbehandlung**: Implementieren Sie robuste Fehlerbehandlung und Wiederholungslogik.
- **Rate Limits**: Beachten Sie die API-Rate-Limits und implementieren Sie Caching, wo möglich.
- **Minimale Berechtigungen**: Fordern Sie nur die Berechtigungen an, die Ihre Integration tatsächlich benötigt.
- **Dokumentation**: Dokumentieren Sie Ihre Integrationen gründlich, damit andere sie verstehen und warten können.
- **Überwachung**: Überwachen Sie Ihre Integrationen auf Fehler und Leistungsprobleme.

### Kontinuierliche Integration und Bereitstellung

Kontinuierliche Integration (CI) und Kontinuierliche Bereitstellung (CD) sind Praktiken, die die Automatisierung von Tests und Deployments betonen. GitHub bietet mit GitHub Actions eine integrierte Lösung für CI/CD, die nahtlos mit dem Projektmanagement-Workflow verbunden werden kann.

**GitHub Actions für CI/CD**:

GitHub Actions ermöglicht die Automatisierung von Workflows direkt in GitHub-Repositories. Diese Workflows können durch verschiedene Ereignisse ausgelöst werden, wie Push-Operationen, Pull Requests oder Issue-Kommentare.

*Einrichten eines CI/CD-Workflows*:
1. Erstellen Sie ein Verzeichnis `.github/workflows` in Ihrem Repository.
2. Erstellen Sie eine YAML-Datei für Ihren Workflow, z.B. `ci.yml`.
3. Definieren Sie die Auslöser, Jobs und Schritte für Ihren Workflow.

*Beispiel für einen einfachen CI-Workflow*:
```yaml
name: CI

on:
  push:
    branches: [ main ]
  pull_request:
    branches: [ main ]

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
    - uses: actions/checkout@v2
    - name: Set up Node.js
      uses: actions/setup-node@v2
      with:
        node-version: '14'
    - name: Install dependencies
      run: npm ci
    - name: Run tests
      run: npm test
```

*Integration mit Projektmanagement*:
- Verwenden Sie Status-Checks, um sicherzustellen, dass nur Code, der Tests besteht, zusammengeführt werden kann.
- Aktualisieren Sie automatisch Issues und Projektboards basierend auf CI/CD-Ergebnissen.
- Verwenden Sie Labels oder Kommentare, um den Status von Builds und Deployments anzuzeigen.
- Erstellen Sie automatisierte Release-Notes basierend auf zusammengeführten Pull Requests.

**Externe CI/CD-Tools**:

Neben GitHub Actions können auch externe CI/CD-Tools mit GitHub integriert werden:

*Jenkins*:
- Verbindet Jenkins-Pipelines mit GitHub-Repositories
- Bietet umfangreiche Anpassungsoptionen und Plugins
- Unterstützt komplexe Build- und Deployment-Szenarien

*CircleCI*:
- Bietet parallele Builds und schnelle Feedback-Schleifen
- Integriert sich nahtlos mit GitHub für Status-Checks und Benachrichtigungen
- Unterstützt Docker und verschiedene Programmiersprachen

*Travis CI*:
- Einfach einzurichten und zu verwenden
- Gute Unterstützung für Open-Source-Projekte
- Integriert sich gut mit GitHub für Status-Checks

*GitLab CI/CD*:
- Kann mit GitHub-Repositories verbunden werden
- Bietet umfassende CI/CD-Funktionen
- Unterstützt Multi-Stage-Pipelines und Auto-DevOps

**Best Practices für CI/CD**:

- **Frühe und häufige Integration**: Integrieren Sie Code so früh und so oft wie möglich.
- **Automatisierte Tests**: Implementieren Sie umfassende automatisierte Tests auf verschiedenen Ebenen (Unit, Integration, End-to-End).
- **Schnelles Feedback**: Optimieren Sie Pipelines für schnelles Feedback an Entwickler.
- **Konsistente Umgebungen**: Verwenden Sie Container oder virtuelle Maschinen für konsistente Build- und Test-Umgebungen.
- **Infrastruktur als Code**: Definieren Sie Ihre CI/CD-Konfiguration als Code und speichern Sie sie im Repository.
- **Monitoring und Logging**: Überwachen Sie Ihre Pipelines und sammeln Sie Logs für Fehlerbehebung und Optimierung.

## Fazit

GitHub bietet eine umfassende Suite von Projektmanagement-Tools, die es Teams ermöglichen, ihre Arbeit effektiv zu organisieren, zu verfolgen und zu liefern. Von einfachen Issues und Projektboards bis hin zu komplexen Integrationen und Automatisierungen – GitHub kann an die Bedürfnisse verschiedener Teams und Projekte angepasst werden.

Die in diesem Kapitel behandelten Konzepte und Best Practices bilden eine solide Grundlage für effektives Projektmanagement mit GitHub. Durch die Kombination dieser Werkzeuge mit klaren Prozessen und einer Kultur der Zusammenarbeit können Teams ihre Produktivität steigern, die Codequalität verbessern und erfolgreiche Projekte liefern.

In den folgenden Kapiteln werden wir uns mit weiteren fortgeschrittenen Funktionen von GitHub befassen, wie GitHub Actions für Workflow-Automatisierung, GitHub Pages für Webhosting und GitHub Security für die Absicherung Ihrer Projekte.
