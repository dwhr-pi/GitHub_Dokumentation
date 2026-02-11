# 12. Sicherheit auf GitHub

- [Dependabot und Sicherheitsupdates](#)
- [Code-Scanning und SAST](#)
- [Secret-Scanning](#)
- [Sicherheitsrichtlinien](#)
- [Zwei-Faktor-Authentifizierung](#)
- [Zugriffsrechte verwalten](#)

## Grundlagen der Sicherheit auf GitHub

Die Sicherheit von Code und Daten ist ein zentraler Aspekt der modernen Softwareentwicklung. GitHub bietet eine Vielzahl von Funktionen und Best Practices, um die Sicherheit Ihrer Repositories und Projekte zu gewährleisten.

### Sicherheitsrisiken verstehen

Bevor wir uns mit den spezifischen Sicherheitsfunktionen von GitHub befassen, ist es wichtig, die häufigsten Sicherheitsrisiken zu verstehen, die bei der Softwareentwicklung und -zusammenarbeit auftreten können.

**Häufige Sicherheitsrisiken**:

1. **Offenlegung sensibler Daten**: Versehentliches Committen von Zugangsdaten, API-Schlüsseln, Passwörtern oder anderen vertraulichen Informationen in öffentliche oder private Repositories.

2. **Sicherheitslücken in Abhängigkeiten**: Die Verwendung von Drittanbieter-Bibliotheken und -Frameworks mit bekannten Sicherheitslücken kann Ihre Anwendung angreifbar machen.

3. **Unsicherer Code**: Fehler in der Implementierung, die zu Sicherheitslücken wie SQL-Injection, Cross-Site-Scripting (XSS) oder anderen Schwachstellen führen können.

4. **Unbefugter Zugriff**: Unzureichende Zugriffskontrollen, die es unbefugten Personen ermöglichen, auf Repositories, Branches oder sensible Daten zuzugreifen.

5. **Supply-Chain-Angriffe**: Kompromittierung von Abhängigkeiten oder Entwicklungstools, um bösartigen Code in Ihre Anwendung einzuschleusen.

6. **Social Engineering**: Angriffe, die auf die Manipulation von Entwicklern abzielen, um Zugang zu Systemen oder Daten zu erhalten.

**Sicherheitsverantwortung**:

Bei der Nutzung von GitHub teilen sich die Verantwortung für die Sicherheit zwischen GitHub und den Nutzern auf:

1. **GitHub ist verantwortlich für**:
   - Sicherheit der Plattforminfrastruktur
   - Verfügbarkeit und Zuverlässigkeit der Dienste
   - Bereitstellung von Sicherheitsfunktionen und -tools
   - Schutz vor externen Bedrohungen für die Plattform
   - Sicherheitspatches für die GitHub-Plattform

2. **Nutzer sind verantwortlich für**:
   - Sichere Konfiguration ihrer Repositories
   - Schutz ihrer Anmeldeinformationen
   - Überprüfung und Sicherung ihres Codes
   - Verwaltung von Zugriffsberechtigungen
   - Überwachung und Behebung von Sicherheitslücken in ihren Projekten

### Kontoabsicherung

Die Sicherheit Ihres GitHub-Kontos ist der erste und wichtigste Schritt zum Schutz Ihrer Projekte und Daten.

**Starke Passwörter und Passwort-Manager**:

- Verwenden Sie ein einzigartiges, komplexes Passwort für Ihr GitHub-Konto
- Nutzen Sie einen Passwort-Manager, um sichere Passwörter zu generieren und zu speichern
- Ändern Sie Ihr Passwort regelmäßig, besonders nach Sicherheitsvorfällen
- Teilen Sie Ihr Passwort niemals mit anderen Personen

**Zwei-Faktor-Authentifizierung (2FA)**:

Die Aktivierung der Zwei-Faktor-Authentifizierung ist eine der effektivsten Maßnahmen zum Schutz Ihres GitHub-Kontos:

1. **Aktivierung von 2FA**:
   - Navigieren Sie zu Ihren Kontoeinstellungen
   - Wählen Sie "Password and authentication"
   - Klicken Sie auf "Enable two-factor authentication"
   - Folgen Sie den Anweisungen zur Einrichtung

2. **2FA-Methoden**:
   - **TOTP-App** (Time-based One-Time Password): Verwenden Sie Apps wie Google Authenticator, Authy oder Microsoft Authenticator
   - **SMS**: Erhalten Sie Codes per SMS (weniger sicher als TOTP)
   - **Sicherheitsschlüssel**: Physische Sicherheitsschlüssel wie YubiKey oder Google Titan
   - **GitHub Mobile**: Bestätigen Sie Anmeldungen direkt in der GitHub Mobile App

3. **Recovery-Codes**:
   - Speichern Sie Ihre Recovery-Codes an einem sicheren Ort
   - Diese Codes ermöglichen den Zugriff auf Ihr Konto, wenn Sie keinen Zugriff auf Ihre 2FA-Methode haben
   - Generieren Sie neue Codes, wenn Sie einen verwendet haben

**Sitzungsverwaltung**:

- Überprüfen Sie regelmäßig Ihre aktiven Sitzungen unter "Settings" > "Security log"
- Melden Sie sich von nicht verwendeten Geräten ab
- Aktivieren Sie Benachrichtigungen für neue Anmeldungen
- Verwenden Sie "Sign out of all sessions", wenn Sie den Verdacht haben, dass Ihr Konto kompromittiert wurde

**Autorisierte Anwendungen überprüfen**:

- Überprüfen Sie regelmäßig die Anwendungen, die Zugriff auf Ihr GitHub-Konto haben
- Navigieren Sie zu "Settings" > "Applications" > "Authorized OAuth Apps"
- Widerrufen Sie den Zugriff für Anwendungen, die Sie nicht mehr verwenden oder nicht erkennen

### Repository-Sicherheit

Die Sicherheit Ihrer Repositories ist entscheidend für den Schutz Ihres Codes und Ihrer Daten.

**Öffentlich vs. Privat**:

- **Öffentliche Repositories**: Sichtbar für jeden im Internet, ideal für Open-Source-Projekte
- **Private Repositories**: Nur für Sie und ausdrücklich eingeladene Mitarbeiter sichtbar
- Wählen Sie den Repository-Typ basierend auf der Sensibilität des Codes und dem Zweck des Projekts

**Zugriffsberechtigungen**:

1. **Repository-Rollen**:
   - **Read**: Kann den Code anzeigen und klonen
   - **Triage**: Kann Issues und Pull Requests verwalten
   - **Write**: Kann Code pushen und Branches erstellen
   - **Maintain**: Kann die meisten Repository-Einstellungen verwalten
   - **Admin**: Hat vollständige Kontrolle über das Repository

2. **Mitarbeiter hinzufügen**:
   - Navigieren Sie zu "Settings" > "Manage access"
   - Klicken Sie auf "Invite a collaborator"
   - Suchen Sie nach dem Benutzernamen oder der E-Mail-Adresse
   - Wählen Sie die entsprechende Rolle aus

3. **Teams und Organisationen**:
   - Verwenden Sie Teams, um Berechtigungen für Gruppen von Benutzern zu verwalten
   - Weisen Sie Teams unterschiedliche Zugriffsebenen zu
   - Überprüfen Sie regelmäßig die Teammitgliedschaften und -berechtigungen

**Branch-Schutz**:

Branch-Schutzregeln sind ein wichtiges Werkzeug, um die Integrität Ihres Codes zu gewährleisten:

1. **Branch-Schutzregeln aktivieren**:
   - Navigieren Sie zu "Settings" > "Branches"
   - Klicken Sie auf "Add rule" neben "Branch protection rules"
   - Geben Sie den Branch-Namen ein (z.B. `main` oder `master`)

2. **Häufige Schutzoptionen**:
   - **Require pull request reviews before merging**: Erfordert eine bestimmte Anzahl von Genehmigungen
   - **Require status checks to pass before merging**: Stellt sicher, dass Tests bestanden werden
   - **Require signed commits**: Erfordert, dass alle Commits digital signiert sind
   - **Include administrators**: Wendet die Regeln auch auf Repository-Administratoren an
   - **Restrict who can push to matching branches**: Begrenzt, wer direkt in den Branch pushen kann

3. **Erweiterte Optionen**:
   - **Require linear history**: Verhindert Merge-Commits und erzwingt eine lineare Commit-Historie
   - **Allow force pushes**: Kann für bestimmte Benutzer oder Teams aktiviert werden
   - **Allow deletions**: Kontrolliert, ob der Branch gelöscht werden kann

**Sensible Daten schützen**:

1. **Vermeidung von Datenlecks**:
   - Verwenden Sie `.gitignore`, um sensible Dateien vom Tracking auszuschließen
   - Nutzen Sie Umgebungsvariablen für Konfigurationswerte
   - Speichern Sie Secrets in einem sicheren Secret-Management-System

2. **Umgang mit versehentlich committetem sensiblen Material**:
   - Ändern Sie sofort alle exponierten Passwörter oder Tokens
   - Verwenden Sie `git filter-branch` oder das BFG Repo-Cleaner-Tool, um sensible Daten aus der Git-Historie zu entfernen
   - Erzwingen Sie einen Push mit `git push --force`, nachdem Sie die Historie bereinigt haben
   - Beachten Sie, dass bereits geklonte Repositories möglicherweise noch die sensiblen Daten enthalten

3. **GitHub Secrets**:
   - Verwenden Sie GitHub Secrets für CI/CD-Workflows
   - Navigieren Sie zu "Settings" > "Secrets" > "Actions"
   - Klicken Sie auf "New repository secret"
   - Geben Sie einen Namen und Wert ein
   - Verwenden Sie diese Secrets in GitHub Actions-Workflows mit der Syntax `${{ secrets.SECRET_NAME }}`

## GitHub Security Features

GitHub bietet eine Reihe von Sicherheitsfunktionen, die Ihnen helfen, Sicherheitslücken zu identifizieren, zu beheben und zu verhindern.

### Dependabot

Dependabot ist ein leistungsstarkes Werkzeug, das Ihnen hilft, Ihre Abhängigkeiten sicher und aktuell zu halten.

**Dependabot Alerts**:

Dependabot Alerts benachrichtigen Sie über bekannte Sicherheitslücken in Ihren Abhängigkeiten:

1. **Aktivierung**:
   - Navigieren Sie zu "Settings" > "Security & analysis"
   - Aktivieren Sie "Dependabot alerts"

2. **Funktionsweise**:
   - GitHub scannt Ihre Abhängigkeitsdateien (z.B. package.json, requirements.txt, Gemfile)
   - Vergleicht Ihre Abhängigkeiten mit der GitHub Advisory Database
   - Erstellt Alerts für gefundene Sicherheitslücken
   - Benachrichtigt Repository-Administratoren

3. **Umgang mit Alerts**:
   - Überprüfen Sie Alerts unter der Registerkarte "Security" > "Dependabot alerts"
   - Priorisieren Sie Alerts basierend auf Schweregrad und Auswirkung
   - Schließen Sie Alerts mit einer Begründung, wenn sie nicht relevant sind

**Dependabot Security Updates**:

Dependabot Security Updates automatisieren die Behebung von Sicherheitslücken:

1. **Aktivierung**:
   - Navigieren Sie zu "Settings" > "Security & analysis"
   - Aktivieren Sie "Dependabot security updates"

2. **Funktionsweise**:
   - Dependabot erstellt automatisch Pull Requests, um anfällige Abhängigkeiten zu aktualisieren
   - Jeder PR aktualisiert eine Abhängigkeit auf die minimale Version, die die Sicherheitslücke behebt
   - Enthält Details zur Sicherheitslücke und Änderungsprotokoll-Informationen

3. **Best Practices**:
   - Überprüfen Sie Dependabot PRs zeitnah
   - Führen Sie Tests durch, um sicherzustellen, dass die Aktualisierung keine Probleme verursacht
   - Konfigurieren Sie CI/CD-Pipelines, um Dependabot PRs automatisch zu testen

**Dependabot Version Updates**:

Dependabot Version Updates helfen, Ihre Abhängigkeiten aktuell zu halten, auch wenn keine Sicherheitslücken vorliegen:

1. **Konfiguration**:
   - Erstellen Sie eine `.github/dependabot.yml`-Datei in Ihrem Repository
   - Definieren Sie die zu überwachenden Paket-Ökosysteme und Update-Häufigkeit

2. **Beispielkonfiguration**:
   ```yaml
   version: 2
   updates:
     - package-ecosystem: "npm"
       directory: "/"
       schedule:
         interval: "weekly"
       open-pull-requests-limit: 10
       
     - package-ecosystem: "pip"
       directory: "/"
       schedule:
         interval: "monthly"
   ```

3. **Anpassungsoptionen**:
   - **package-ecosystem**: Unterstützte Ökosysteme wie npm, pip, docker, github-actions
   - **directory**: Verzeichnis mit der Abhängigkeitsdatei
   - **schedule**: Häufigkeit der Updates (daily, weekly, monthly)
   - **target-branch**: Branch für Pull Requests
   - **labels**: Labels für Pull Requests
   - **assignees**: Zugewiesene Personen für Pull Requests
   - **reviewers**: Reviewer für Pull Requests
   - **ignore**: Abhängigkeiten oder Versionen, die ignoriert werden sollen

### Code Scanning mit CodeQL

Code Scanning ist eine Funktion, die automatisch Sicherheitslücken in Ihrem Code identifiziert.

**Grundlagen von Code Scanning**:

1. **Was ist Code Scanning?**
   - Automatisierte Codeanalyse zur Identifizierung von Sicherheitslücken
   - Basiert auf CodeQL, einer leistungsstarken Codeanalyse-Engine
   - Unterstützt mehrere Programmiersprachen (JavaScript, TypeScript, Python, Java, C/C++, C#, Go)
   - Integriert in den GitHub-Workflow

2. **Aktivierung**:
   - Navigieren Sie zu "Security" > "Code scanning alerts"
   - Klicken Sie auf "Set up code scanning"
   - Wählen Sie "CodeQL Analysis" oder einen anderen Anbieter
   - Konfigurieren Sie den Workflow nach Bedarf
   - Committen Sie die Workflow-Datei

3. **Funktionsweise**:
   - Der CodeQL-Workflow wird bei Push-Ereignissen oder nach einem Zeitplan ausgeführt
   - CodeQL kompiliert den Code und erstellt eine Datenbank
   - Führt Abfragen aus, um Sicherheitsprobleme zu identifizieren
   - Meldet Ergebnisse als Code Scanning Alerts

**CodeQL-Workflow konfigurieren**:

Ein typischer CodeQL-Workflow sieht wie folgt aus:

```yaml
name: "CodeQL"

on:
  push:
    branches: [ main ]
  pull_request:
    branches: [ main ]
  schedule:
    - cron: '0 0 * * 0'  # Jeden Sonntag um Mitternacht

jobs:
  analyze:
    name: Analyze
    runs-on: ubuntu-latest
    permissions:
      security-events: write

    steps:
    - name: Checkout repository
      uses: actions/checkout@v3

    - name: Initialize CodeQL
      uses: github/codeql-action/init@v2
      with:
        languages: javascript, python

    - name: Perform CodeQL Analysis
      uses: github/codeql-action/analyze@v2
```

Sie können diesen Workflow anpassen:
- Ändern Sie die Trigger-Ereignisse
- Fügen Sie oder entfernen Sie Sprachen
- Konfigurieren Sie zusätzliche Build-Schritte für kompilierte Sprachen
- Passen Sie die Abfragen an oder fügen Sie benutzerdefinierte Abfragen hinzu

**Umgang mit Code Scanning Alerts**:

1. **Alerts überprüfen**:
   - Navigieren Sie zu "Security" > "Code scanning alerts"
   - Sortieren Sie nach Schweregrad, Alter oder Status
   - Klicken Sie auf einen Alert, um Details anzuzeigen

2. **Alerts beheben**:
   - Verstehen Sie das Problem anhand der bereitgestellten Informationen
   - Folgen Sie den Empfehlungen zur Behebung
   - Committen Sie die Änderung
   - Der Alert wird automatisch geschlossen, wenn das Problem behoben ist

3. **Alerts verwalten**:
   - Markieren Sie falsch positive Ergebnisse als "Dismissed"
   - Fügen Sie eine Begründung hinzu, warum der Alert ignoriert werden kann
   - Erstellen Sie benutzerdefinierte Abfragen, um die Genauigkeit zu verbessern
   - Konfigurieren Sie Benachrichtigungen für neue Alerts

**Erweiterte CodeQL-Funktionen**:

1. **Benutzerdefinierte Abfragen**:
   - Erstellen Sie eigene CodeQL-Abfragen für projektspezifische Probleme
   - Speichern Sie Abfragen in einem `.github/codeql`-Verzeichnis
   - Verweisen Sie auf benutzerdefinierte Abfragen in Ihrem Workflow

2. **CodeQL-Datenbanken**:
   - Exportieren Sie CodeQL-Datenbanken für lokale Analyse
   - Teilen Sie Datenbanken mit Sicherheitsexperten
   - Führen Sie komplexe Analysen außerhalb von GitHub durch

3. **Integration mit SARIF**:
   - Importieren Sie Ergebnisse von anderen Codeanalyse-Tools im SARIF-Format
   - Verwenden Sie die `github/codeql-action/upload-sarif`-Aktion
   - Konsolidieren Sie Sicherheitsergebnisse von verschiedenen Tools

### Secret Scanning

Secret Scanning schützt vor versehentlich committetem sensiblen Material wie API-Schlüsseln, Zugangsdaten und Tokens.

**Grundlagen von Secret Scanning**:

1. **Was ist Secret Scanning?**
   - Automatische Erkennung von Secrets in Repositories
   - Unterstützung für über 100 Secret-Typen von verschiedenen Diensten
   - Benachrichtigung von Repository-Administratoren und Secret-Ausstellern
   - Verfügbar für öffentliche Repositories und private Repositories mit GitHub Advanced Security

2. **Aktivierung**:
   - Für öffentliche Repositories: Automatisch aktiviert
   - Für private Repositories:
     - Navigieren Sie zu "Settings" > "Security & analysis"
     - Aktivieren Sie "Secret scanning"

3. **Unterstützte Secret-Typen**:
   - API-Schlüssel (AWS, Google Cloud, Azure, etc.)
   - Authentifizierungstoken (GitHub, NPM, PyPI, etc.)
   - Datenbank-Anmeldeinformationen
   - Zertifikate und private Schlüssel
   - Andere sensible Informationen

**Umgang mit Secret Scanning Alerts**:

1. **Alerts überprüfen**:
   - Navigieren Sie zu "Security" > "Secret scanning alerts"
   - Überprüfen Sie neue Alerts zeitnah
   - Klicken Sie auf einen Alert, um Details anzuzeigen

2. **Maßnahmen bei erkannten Secrets**:
   - Widerrufen Sie das exponierte Secret sofort
   - Erstellen Sie ein neues Secret
   - Aktualisieren Sie alle Systeme, die das alte Secret verwendet haben
   - Überprüfen Sie Logs auf unbefugte Nutzung

3. **Alerts verwalten**:
   - Markieren Sie Alerts als "Resolved" nach der Behebung
   - Markieren Sie falsch positive Ergebnisse als "Dismissed"
   - Fügen Sie eine Begründung hinzu, warum der Alert ignoriert werden kann

**Secret Scanning konfigurieren**:

1. **Benutzerdefinierte Muster**:
   - Erstellen Sie benutzerdefinierte Muster für organisationsspezifische Secrets
   - Navigieren Sie zu den Organisationseinstellungen > "Security & analysis" > "Secret scanning"
   - Klicken Sie auf "New pattern"
   - Definieren Sie einen Namen, ein Muster (Regex) und eine Beispiel-Übereinstimmung

2. **Push Protection**:
   - Verhindert das Pushen von erkannten Secrets
   - Blockiert den Push und benachrichtigt den Entwickler
   - Ermöglicht das Überschreiben in Ausnahmefällen
   - Aktivieren Sie unter "Settings" > "Security & analysis" > "Secret scanning" > "Push protection"

3. **Benachrichtigungen**:
   - Konfigurieren Sie Benachrichtigungen für Secret Scanning Alerts
   - Integrieren Sie mit Slack, Microsoft Teams oder anderen Diensten
   - Erstellen Sie benutzerdefinierte Workflows für die Reaktion auf Alerts

### Security Advisories

Security Advisories ermöglichen es Ihnen, Sicherheitslücken in Ihren Projekten verantwortungsvoll zu verwalten und zu veröffentlichen.

**Grundlagen von Security Advisories**:

1. **Was sind Security Advisories?**
   - Ein Mechanismus zur verantwortungsvollen Offenlegung von Sicherheitslücken
   - Bietet einen privaten Raum zur Diskussion und Behebung von Sicherheitsproblemen
   - Ermöglicht die Veröffentlichung strukturierter Informationen über Sicherheitslücken
   - Integriert mit der GitHub Advisory Database

2. **Erstellung eines Advisories**:
   - Navigieren Sie zu "Security" > "Advisories"
   - Klicken Sie auf "New draft advisory"
   - Füllen Sie die erforderlichen Informationen aus:
     - Titel und Beschreibung
     - Schweregrad und Auswirkungen
     - Betroffene Versionen
     - Behebungsinformationen

3. **Zusammenarbeit an einem Advisory**:
   - Fügen Sie Mitarbeiter zum Advisory hinzu
   - Diskutieren Sie das Problem privat
   - Arbeiten Sie an einem Fix in einem temporären privaten Fork
   - Testen Sie die Lösung, bevor Sie sie veröffentlichen

**Veröffentlichung eines Advisories**:

1. **Vorbereitung zur Veröffentlichung**:
   - Stellen Sie sicher, dass ein Fix verfügbar ist
   - Aktualisieren Sie alle Informationen im Advisory
   - Überprüfen Sie die Genauigkeit der CVE-Details (falls zugewiesen)
   - Koordinieren Sie die Veröffentlichung mit anderen betroffenen Parteien

2. **Veröffentlichungsprozess**:
   - Klicken Sie auf "Publish advisory"
   - Das Advisory wird öffentlich sichtbar
   - Es wird in die GitHub Advisory Database aufgenommen
   - Dependabot beginnt, Alerts für betroffene Repositories zu erstellen

3. **Nach der Veröffentlichung**:
   - Kommunizieren Sie das Advisory an Ihre Community
   - Aktualisieren Sie das Advisory bei Bedarf mit zusätzlichen Informationen
   - Überwachen Sie Feedback und Fragen von Nutzern

**CVE-Zuweisung**:

1. **Was ist ein CVE?**
   - Common Vulnerabilities and Exposures (CVE) ist ein Standard für die Identifizierung von Sicherheitslücken
   - Jede CVE hat eine eindeutige Kennung (z.B. CVE-2023-12345)
   - CVEs werden in verschiedenen Sicherheitsdatenbanken referenziert

2. **CVE-Anforderung über GitHub**:
   - GitHub ist eine CVE Numbering Authority (CNA)
   - Sie können eine CVE direkt über das Advisory-Formular anfordern
   - Wählen Sie "Request CVE ID" im Advisory
   - GitHub weist eine CVE-ID zu und fügt sie dem Advisory hinzu

3. **Manuelle CVE-Zuweisung**:
   - Wenn Sie bereits eine CVE-ID haben, können Sie sie manuell hinzufügen
   - Geben Sie die CVE-ID im entsprechenden Feld ein
   - Stellen Sie sicher, dass alle CVE-Details korrekt sind

### Security Overview und Security Insights

GitHub bietet Tools, um einen Überblick über die Sicherheitslage Ihrer Repositories und Organisationen zu erhalten.

**Security Overview**:

1. **Was ist Security Overview?**
   - Eine zentrale Ansicht für Sicherheitsrisiken in Ihren Repositories
   - Verfügbar für Organisationen mit GitHub Advanced Security
   - Zeigt Alerts von Dependabot, Code Scanning und Secret Scanning

2. **Zugriff auf Security Overview**:
   - Navigieren Sie zur Registerkarte "Security" in Ihrer Organisation
   - Sehen Sie eine Zusammenfassung aller Sicherheitsrisiken
   - Filtern Sie nach Repository, Alert-Typ, Schweregrad oder Status

3. **Verwendung von Security Overview**:
   - Identifizieren Sie Repositories mit den meisten Sicherheitsrisiken
   - Priorisieren Sie die Behebung basierend auf Schweregrad
   - Überwachen Sie den Fortschritt bei der Risikominderung
   - Identifizieren Sie Muster oder häufige Probleme

**Security Insights**:

1. **Repository-Insights**:
   - Jedes Repository hat eine eigene Sicherheitsübersicht
   - Navigieren Sie zu "Security" > "Insights"
   - Sehen Sie Trends und Statistiken zu Sicherheitsrisiken
   - Überwachen Sie die Behebungsrate und durchschnittliche Zeit bis zur Behebung

2. **Dependabot-Insights**:
   - Zeigt Statistiken zu Abhängigkeiten und Sicherheitslücken
   - Identifiziert die am häufigsten betroffenen Abhängigkeiten
   - Verfolgt die Behebungsrate von Dependabot Alerts

3. **Code Scanning-Insights**:
   - Zeigt Trends bei Code Scanning Alerts
   - Identifiziert häufige Sicherheitsprobleme im Code
   - Verfolgt die Behebungsrate von Code Scanning Alerts

**Sicherheitsberichte**:

1. **Exportieren von Daten**:
   - Exportieren Sie Sicherheitsdaten für Compliance-Berichte
   - Verwenden Sie die GitHub API, um benutzerdefinierte Berichte zu erstellen
   - Integrieren Sie mit Sicherheits-Dashboards oder SIEM-Systemen

2. **Benutzerdefinierte Dashboards**:
   - Erstellen Sie benutzerdefinierte Dashboards mit GitHub Actions
   - Generieren Sie regelmäßige Sicherheitsberichte
   - Visualisieren Sie Sicherheitstrends über Zeit

3. **Compliance-Nachweise**:
   - Verwenden Sie Sicherheitsberichte für Audits
   - Dokumentieren Sie Sicherheitsmaßnahmen und -prozesse
   - Zeigen Sie kontinuierliche Verbesserung der Sicherheitslage

## Sichere Entwicklungspraktiken

Neben den GitHub-spezifischen Sicherheitsfunktionen gibt es allgemeine Praktiken für sichere Softwareentwicklung, die Sie in Ihren GitHub-Workflow integrieren können.

### Sichere Codierungspraktiken

Die Implementierung sicherer Codierungspraktiken ist ein wesentlicher Bestandteil der Entwicklung sicherer Software.

**Grundprinzipien**:

1. **Validierung von Eingaben**:
   - Validieren Sie alle Benutzereingaben
   - Verwenden Sie Whitelisting statt Blacklisting
   - Behandeln Sie alle externen Daten als potenziell bösartig
   - Implementieren Sie angemessene Datentyp-Konvertierungen

2. **Ausgabekodierung**:
   - Kodieren Sie Ausgaben entsprechend dem Kontext
   - Verwenden Sie HTML-Escaping für Webinhalte
   - Verwenden Sie parametrisierte Abfragen für Datenbankoperationen
   - Vermeiden Sie die direkte Einbettung von Benutzereingaben in Ausgaben

3. **Authentifizierung und Autorisierung**:
   - Implementieren Sie starke Authentifizierungsmechanismen
   - Verwenden Sie das Prinzip der geringsten Berechtigung
   - Überprüfen Sie Berechtigungen bei jeder sensiblen Operation
   - Verwenden Sie sichere Session-Management-Techniken

4. **Sichere Kommunikation**:
   - Verwenden Sie HTTPS für alle Netzwerkkommunikation
   - Implementieren Sie angemessene TLS-Konfigurationen
   - Validieren Sie Zertifikate bei Client-Server-Kommunikation
   - Schützen Sie sensible Daten während der Übertragung

**Sprachspezifische Best Practices**:

1. **JavaScript/TypeScript**:
   - Verwenden Sie `===` statt `==` für Vergleiche
   - Nutzen Sie Content Security Policy (CSP)
   - Vermeiden Sie `eval()` und andere dynamische Code-Ausführung
   - Verwenden Sie moderne Frameworks mit eingebauten Sicherheitsfunktionen

2. **Python**:
   - Verwenden Sie `subprocess.run()` mit `shell=False`
   - Nutzen Sie ORM-Frameworks statt direkter SQL-Abfragen
   - Vermeiden Sie `pickle` für nicht vertrauenswürdige Daten
   - Verwenden Sie virtuelle Umgebungen und pinnen Sie Abhängigkeitsversionen

3. **Java**:
   - Verwenden Sie PreparedStatements für SQL-Abfragen
   - Validieren Sie XML-Eingaben gegen XXE-Angriffe
   - Implementieren Sie angemessene Serialisierungssicherheit
   - Nutzen Sie Security Manager für Sandbox-Umgebungen

4. **Go**:
   - Verwenden Sie `html/template` für HTML-Ausgaben
   - Nutzen Sie `crypto/rand` für kryptografische Zufallszahlen
   - Implementieren Sie Context-Timeouts für alle I/O-Operationen
   - Vermeiden Sie unsichere Typkonvertierungen

**Code-Review für Sicherheit**:

1. **Sicherheits-Checklisten**:
   - Erstellen Sie sprachspezifische Sicherheits-Checklisten
   - Integrieren Sie diese in Ihren Pull-Request-Template
   - Aktualisieren Sie Checklisten basierend auf neuen Bedrohungen

2. **Manuelle Reviews**:
   - Schulen Sie Entwickler in sicherheitsbewusstem Code-Review
   - Führen Sie dedizierte Sicherheits-Reviews für kritische Komponenten durch
   - Verwenden Sie Pair Programming für sicherheitskritischen Code

3. **Automatisierte Sicherheitsprüfungen**:
   - Integrieren Sie SAST-Tools (Static Application Security Testing) in CI/CD
   - Führen Sie regelmäßige Abhängigkeitsüberprüfungen durch
   - Implementieren Sie Pre-Commit-Hooks für grundlegende Sicherheitsprüfungen

### Sichere CI/CD-Praktiken

Continuous Integration und Continuous Deployment (CI/CD) sind wesentliche Bestandteile moderner Softwareentwicklung, müssen aber sicher implementiert werden.

**Sichere GitHub Actions-Workflows**:

1. **Workflow-Sicherheit**:
   - Verwenden Sie spezifische Versionen von Actions (`@v2` statt `@master`)
   - Überprüfen Sie Third-Party-Actions vor der Verwendung
   - Begrenzen Sie Workflow-Berechtigungen auf das Notwendige
   - Verwenden Sie `permissions`-Schlüssel, um Berechtigungen einzuschränken

2. **Secrets-Management**:
   - Speichern Sie Secrets in GitHub Secrets, nicht im Workflow-Code
   - Verwenden Sie Umgebungs-Secrets für umgebungsspezifische Werte
   - Rotieren Sie Secrets regelmäßig
   - Vermeiden Sie die Ausgabe von Secrets in Logs

3. **Beispiel für einen sicheren Workflow**:
   ```yaml
   name: Secure CI

   on:
     push:
       branches: [ main ]
     pull_request:
       branches: [ main ]

   permissions:
     contents: read
     security-events: write

   jobs:
     build:
       runs-on: ubuntu-latest
       steps:
         - uses: actions/checkout@v3
         - name: Set up environment
           uses: actions/setup-node@v3
           with:
             node-version: '16'
         - name: Install dependencies
           run: npm ci
         - name: Run security checks
           run: npm audit
         - name: Run tests
           run: npm test
   ```

**Sichere Deployment-Praktiken**:

1. **Umgebungssicherheit**:
   - Verwenden Sie GitHub Environments für verschiedene Deployment-Stufen
   - Konfigurieren Sie Schutzregeln für Produktionsumgebungen
   - Implementieren Sie Genehmigungsworkflows für kritische Deployments
   - Nutzen Sie Umgebungs-Secrets für umgebungsspezifische Anmeldeinformationen

2. **Artefakt-Integrität**:
   - Signieren Sie Build-Artefakte
   - Überprüfen Sie Signaturen vor dem Deployment
   - Implementieren Sie Immutable Artifacts
   - Speichern Sie Artefakte sicher

3. **Deployment-Sicherheit**:
   - Implementieren Sie Blue/Green- oder Canary-Deployments
   - Führen Sie automatisierte Sicherheitstests nach dem Deployment durch
   - Überwachen Sie Deployments auf ungewöhnliche Aktivitäten
   - Halten Sie Rollback-Pläne bereit

**Supply Chain Security**:

1. **Abhängigkeitsmanagement**:
   - Verwenden Sie Dependabot für automatische Updates
   - Pinnen Sie Abhängigkeitsversionen
   - Verwenden Sie Lockfiles (package-lock.json, Pipfile.lock)
   - Führen Sie regelmäßige Audits von Abhängigkeiten durch

2. **Vertrauenswürdige Quellen**:
   - Beziehen Sie Abhängigkeiten nur aus vertrauenswürdigen Quellen
   - Überprüfen Sie die Reputation von Paketautoren
   - Seien Sie vorsichtig bei neuen oder selten verwendeten Paketen
   - Implementieren Sie interne Paket-Proxies oder -Repositories

3. **Software Bill of Materials (SBOM)**:
   - Generieren Sie SBOMs für Ihre Projekte
   - Dokumentieren Sie alle verwendeten Komponenten
   - Aktualisieren Sie SBOMs bei Änderungen
   - Teilen Sie SBOMs mit Stakeholdern

### Sicherheitskultur und -prozesse

Eine starke Sicherheitskultur und gut definierte Prozesse sind ebenso wichtig wie technische Maßnahmen.

**Sicherheitsbewusstsein**:

1. **Schulung und Sensibilisierung**:
   - Führen Sie regelmäßige Sicherheitsschulungen durch
   - Teilen Sie Informationen über neue Bedrohungen und Schwachstellen
   - Fördern Sie eine Kultur, in der Sicherheit Priorität hat
   - Belohnen Sie das Melden von Sicherheitsproblemen

2. **Dokumentation**:
   - Dokumentieren Sie Sicherheitsrichtlinien und -verfahren
   - Erstellen Sie Leitfäden für sichere Entwicklung
   - Halten Sie Incident-Response-Pläne bereit
   - Aktualisieren Sie Dokumentation regelmäßig

3. **Kommunikation**:
   - Etablieren Sie klare Kommunikationskanäle für Sicherheitsprobleme
   - Definieren Sie Eskalationspfade
   - Fördern Sie offene Diskussionen über Sicherheitsthemen
   - Teilen Sie Lessons Learned aus Sicherheitsvorfällen

**Sicherheitsprozesse**:

1. **Threat Modeling**:
   - Führen Sie Threat Modeling in frühen Entwicklungsphasen durch
   - Identifizieren Sie potenzielle Bedrohungen und Angriffsvektoren
   - Priorisieren Sie Risiken basierend auf Auswirkung und Wahrscheinlichkeit
   - Implementieren Sie angemessene Gegenmaßnahmen

2. **Sicherheitstests**:
   - Integrieren Sie Sicherheitstests in den Entwicklungszyklus
   - Führen Sie regelmäßige Penetrationstests durch
   - Implementieren Sie automatisierte Sicherheitstests
   - Validieren Sie die Wirksamkeit von Sicherheitsmaßnahmen

3. **Incident Response**:
   - Entwickeln Sie einen Incident-Response-Plan
   - Definieren Sie Rollen und Verantwortlichkeiten
   - Üben Sie die Reaktion auf Sicherheitsvorfälle
   - Dokumentieren Sie Vorfälle und Maßnahmen

**Kontinuierliche Verbesserung**:

1. **Metriken und Messungen**:
   - Definieren Sie Sicherheitsmetriken (z.B. Zeit bis zur Behebung, Anzahl offener Vulnerabilities)
   - Verfolgen Sie Fortschritte über Zeit
   - Setzen Sie realistische Ziele für Verbesserungen
   - Berichten Sie regelmäßig über den Sicherheitsstatus

2. **Feedback-Schleifen**:
   - Sammeln Sie Feedback zu Sicherheitsprozessen
   - Führen Sie Post-Incident-Reviews durch
   - Passen Sie Prozesse basierend auf Erfahrungen an
   - Lernen Sie aus Fehlern und Erfolgen

3. **Externe Validierung**:
   - Beteiligen Sie sich an Bug-Bounty-Programmen
   - Führen Sie externe Sicherheitsaudits durch
   - Holen Sie Feedback von Sicherheitsexperten ein
   - Vergleichen Sie Ihre Praktiken mit Industriestandards

## Sicherheit für Open-Source-Projekte

Open-Source-Projekte haben spezifische Sicherheitsanforderungen und -herausforderungen, die besondere Aufmerksamkeit erfordern.

### Verantwortungsvolle Offenlegung

Die verantwortungsvolle Offenlegung von Sicherheitslücken ist ein wichtiger Aspekt der Open-Source-Sicherheit.

**Sicherheitsrichtlinien**:

1. **SECURITY.md-Datei**:
   - Erstellen Sie eine SECURITY.md-Datei im Repository
   - Beschreiben Sie, wie Sicherheitslücken gemeldet werden können
   - Definieren Sie den Prozess für die Bearbeitung von Sicherheitsmeldungen
   - Geben Sie an, welche Versionen unterstützt werden

2. **Beispiel für eine SECURITY.md**:
   ```markdown
   # Sicherheitsrichtlinien

   ## Unterstützte Versionen

   | Version | Unterstützt |
   | ------- | ----------- |
   | 5.1.x   | ✅          |
   | 5.0.x   | ✅          |
   | 4.0.x   | ❌          |
   | < 4.0   | ❌          |

   ## Melden einer Sicherheitslücke

   Bitte melden Sie Sicherheitslücken nicht über öffentliche GitHub Issues.

   Stattdessen senden Sie eine E-Mail an security@example.com oder nutzen Sie die
   private Vulnerability Reporting-Funktion von GitHub.

   Wir werden so schnell wie möglich antworten und Sie über den Fortschritt bei
   der Behebung des Problems informieren.
   ```

3. **Private Vulnerability Reporting**:
   - Aktivieren Sie Private Vulnerability Reporting in den Repository-Einstellungen
   - Dies ermöglicht es Benutzern, Sicherheitslücken privat zu melden
   - Bearbeiten Sie gemeldete Probleme in einem privaten Kontext
   - Veröffentlichen Sie Fixes, bevor Sie das Problem öffentlich machen

**Kommunikation mit Sicherheitsforschern**:

1. **Respektvoller Umgang**:
   - Behandeln Sie Sicherheitsforscher mit Respekt
   - Danken Sie ihnen für ihre Bemühungen
   - Kommunizieren Sie transparent über den Fortschritt
   - Halten Sie vereinbarte Zeitpläne ein

2. **Koordinierte Offenlegung**:
   - Arbeiten Sie mit dem Melder zusammen, um einen angemessenen Zeitplan festzulegen
   - Geben Sie dem Melder die Möglichkeit, den Fix zu überprüfen
   - Erwähnen Sie den Melder in der Offenlegung (mit deren Zustimmung)
   - Koordinieren Sie die Veröffentlichung von Fixes und Advisories

3. **Anerkennung**:
   - Führen Sie eine CONTRIBUTORS.md- oder ACKNOWLEDGMENTS.md-Datei
   - Erwähnen Sie Sicherheitsforscher in Release Notes
   - Erwägen Sie Bug-Bounty-Programme oder andere Formen der Anerkennung
   - Fördern Sie eine positive Beziehung zur Sicherheitsgemeinschaft

### Community-Sicherheit

Die Einbindung der Community in Sicherheitsaspekte kann die Sicherheit von Open-Source-Projekten erheblich verbessern.

**Beitragende einbinden**:

1. **Sicherheitsrichtlinien für Beitragende**:
   - Fügen Sie Sicherheitsrichtlinien in CONTRIBUTING.md ein
   - Definieren Sie Erwartungen für sicherheitsrelevante Pull Requests
   - Stellen Sie Ressourcen für sichere Entwicklung bereit
   - Ermutigen Sie zu sicherheitsbewussten Beiträgen

2. **Sicherheits-Champions**:
   - Identifizieren Sie Beitragende mit Sicherheitsexpertise
   - Weisen Sie ihnen spezielle Rollen oder Verantwortlichkeiten zu
   - Fördern Sie ihre Beteiligung an sicherheitsrelevanten Diskussionen
   - Nutzen Sie ihr Wissen für Sicherheitsreviews

3. **Transparenz**:
   - Kommunizieren Sie offen über Sicherheitspraktiken
   - Teilen Sie Informationen über behobene Sicherheitslücken
   - Diskutieren Sie Sicherheitsverbesserungen öffentlich
   - Seien Sie transparent über Sicherheitsrisiken

**Sicherheitsaudits und -reviews**:

1. **Community-Audits**:
   - Organisieren Sie Community-Sicherheitsaudits
   - Laden Sie Beitragende ein, sich auf bestimmte Sicherheitsaspekte zu konzentrieren
   - Dokumentieren Sie Ergebnisse und Maßnahmen
   - Wiederholen Sie Audits regelmäßig

2. **Externe Audits**:
   - Suchen Sie nach Möglichkeiten für professionelle Sicherheitsaudits
   - Nutzen Sie Programme wie die Open Source Security Foundation (OpenSSF)
   - Veröffentlichen Sie Audit-Ergebnisse (nach Behebung von Problemen)
   - Implementieren Sie Empfehlungen aus Audits

3. **Kontinuierliche Reviews**:
   - Implementieren Sie kontinuierliche Sicherheitsreviews
   - Überprüfen Sie regelmäßig kritische Komponenten
   - Aktualisieren Sie Sicherheitspraktiken basierend auf neuen Erkenntnissen
   - Fördern Sie eine Kultur des kontinuierlichen Lernens

**Sicherheitsressourcen**:

1. **Dokumentation**:
   - Erstellen Sie Sicherheitsdokumentation für Benutzer
   - Bieten Sie Anleitungen zur sicheren Konfiguration
   - Dokumentieren Sie bekannte Sicherheitsrisiken und Gegenmaßnahmen
   - Halten Sie Dokumentation aktuell

2. **Schulungsmaterialien**:
   - Entwickeln Sie Schulungsmaterialien für Beitragende
   - Teilen Sie Ressourcen zu sicheren Entwicklungspraktiken
   - Erstellen Sie Beispiele für sichere Implementierungen
   - Bieten Sie Mentoring für neue Beitragende an

3. **Werkzeuge und Integrationen**:
   - Stellen Sie Werkzeuge für Sicherheitstests bereit
   - Dokumentieren Sie CI/CD-Integrationen für Sicherheitsprüfungen
   - Teilen Sie Konfigurationen für Sicherheitstools
   - Entwickeln Sie projektspezifische Sicherheitswerkzeuge

### Langfristige Sicherheitsplanung

Langfristige Sicherheitsplanung ist entscheidend für die nachhaltige Sicherheit von Open-Source-Projekten.

**Versionierung und Support**:

1. **Versionsrichtlinien**:
   - Definieren Sie klare Versionsrichtlinien
   - Legen Sie Support-Zeiträume für verschiedene Versionen fest
   - Kommunizieren Sie End-of-Life-Daten im Voraus
   - Bieten Sie Migrationspfade für veraltete Versionen

2. **Backporting von Sicherheitsfixes**:
   - Definieren Sie Richtlinien für das Backporting von Sicherheitsfixes
   - Priorisieren Sie kritische Sicherheitsfixes für unterstützte Versionen
   - Dokumentieren Sie, welche Fixes in welche Versionen übernommen wurden
   - Testen Sie Backports gründlich

3. **LTS-Versionen (Long-Term Support)**:
   - Erwägen Sie LTS-Versionen für stabile Projekte
   - Definieren Sie längere Support-Zeiträume für LTS-Versionen
   - Fokussieren Sie sich auf Stabilität und Sicherheit für LTS
   - Planen Sie Ressourcen für langfristigen Support

**Nachhaltige Sicherheit**:

1. **Ressourcenplanung**:
   - Planen Sie Ressourcen für Sicherheitsarbeit ein
   - Berücksichtigen Sie Sicherheit bei der Priorisierung von Arbeit
   - Suchen Sie nach Finanzierungsmöglichkeiten für Sicherheitsarbeit
   - Verteilen Sie Sicherheitsverantwortlichkeiten auf mehrere Personen

2. **Wissenstransfer**:
   - Dokumentieren Sie Sicherheitswissen und -entscheidungen
   - Fördern Sie den Wissensaustausch zwischen Beitragenden
   - Vermeiden Sie Single Points of Failure bei Sicherheitsexpertise
   - Mentoren Sie neue Beitragende in Sicherheitsaspekten

3. **Kontinuierliche Verbesserung**:
   - Überprüfen Sie regelmäßig Sicherheitspraktiken
   - Passen Sie Prozesse basierend auf Erfahrungen an
   - Bleiben Sie über neue Bedrohungen und Best Practices informiert
   - Implementieren Sie proaktiv Sicherheitsverbesserungen

**Sicherheits-Roadmap**:

1. **Langfristige Ziele**:
   - Definieren Sie langfristige Sicherheitsziele
   - Erstellen Sie eine Roadmap für Sicherheitsverbesserungen
   - Priorisieren Sie Maßnahmen basierend auf Risiko und Aufwand
   - Überprüfen und aktualisieren Sie die Roadmap regelmäßig

2. **Technische Schulden**:
   - Identifizieren Sie sicherheitsrelevante technische Schulden
   - Planen Sie die schrittweise Behebung
   - Berücksichtigen Sie Sicherheitsaspekte bei Refactoring
   - Dokumentieren Sie bekannte Probleme und geplante Lösungen

3. **Zukunftssicherheit**:
   - Antizipieren Sie zukünftige Sicherheitsanforderungen
   - Planen Sie für neue Technologien und Standards
   - Berücksichtigen Sie Änderungen in der Bedrohungslandschaft
   - Investieren Sie in flexible und erweiterbare Sicherheitsarchitekturen

## Fazit

Die Sicherheit auf GitHub ist ein vielschichtiges Thema, das technische Maßnahmen, Prozesse und kulturelle Aspekte umfasst. Durch die Implementierung der in diesem Kapitel beschriebenen Best Practices und die Nutzung der von GitHub bereitgestellten Sicherheitsfunktionen können Sie die Sicherheit Ihrer Projekte erheblich verbessern.

Denken Sie daran, dass Sicherheit ein kontinuierlicher Prozess ist, der ständige Aufmerksamkeit und Anpassung erfordert. Neue Bedrohungen entstehen ständig, und Sicherheitspraktiken müssen entsprechend weiterentwickelt werden.

Investitionen in Sicherheit zahlen sich langfristig aus, indem sie das Vertrauen der Benutzer stärken, Datenschutzverletzungen verhindern und die Integrität Ihrer Software gewährleisten. Durch die Integration von Sicherheit in jeden Aspekt Ihres Entwicklungsprozesses auf GitHub können Sie robustere, vertrauenswürdigere und nachhaltigere Softwareprojekte erstellen.

In den folgenden Kapiteln werden wir uns mit weiteren fortgeschrittenen Funktionen von GitHub befassen und einen umfassenden Überblick über die Plattform abschließen.
