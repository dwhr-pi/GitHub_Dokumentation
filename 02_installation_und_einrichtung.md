# 2. Installation und Einrichtung

- [Konto erstellen](#Konto_erstellen)
- [Profil einrichten](#Profil_einrichten)
- [Authentifizierung und Sicherheit](#Authentifizierung_und_Sicherheit)
- [GitHub Desktop installieren](#GitHub_Desktop_installieren)
- [Git-Kommandozeile einrichten](#Git-Kommandozeile_einrichten)
- [SSH-Schlüssel einrichten](#SSH-Schlüssel_einrichten)
- [Fazit](#Fazit)

<A name="Konto_erstellen"></A>
## Konto erstellen

Die Nutzung von GitHub beginnt mit der Erstellung eines persönlichen Kontos. Ein GitHub-Konto ist Ihre digitale Identität innerhalb der GitHub-Community und bildet die Grundlage für alle Ihre Aktivitäten auf der Plattform.

### Registrierung für ein neues persönliches Konto

Um ein neues GitHub-Konto zu erstellen, folgen Sie diesen Schritten:

1. Öffnen Sie Ihren Webbrowser und navigieren Sie zur GitHub-Startseite unter [https://github.com](https://github.com).

2. Auf der Startseite finden Sie ein Registrierungsformular. Geben Sie Ihre E-Mail-Adresse ein, erstellen Sie ein sicheres Passwort und wählen Sie einen eindeutigen Benutzernamen.

3. Ihr Benutzername ist ein wichtiger Teil Ihrer GitHub-Identität. Er wird in URLs, @mentions und in Ihrem Profil angezeigt. Wählen Sie daher einen Namen, der professionell und leicht zu merken ist.

4. Klicken Sie auf die Schaltfläche "Registrieren", um den Registrierungsprozess zu starten.

5. GitHub wird Ihnen eine E-Mail zur Verifizierung Ihrer E-Mail-Adresse senden. Öffnen Sie diese E-Mail und klicken Sie auf den Bestätigungslink, um Ihr Konto zu aktivieren.

6. Nach der Bestätigung Ihrer E-Mail-Adresse werden Sie aufgefordert, einige Fragen zu Ihrer Erfahrung und Ihren Plänen für die Nutzung von GitHub zu beantworten. Diese Informationen helfen GitHub, Ihr Erlebnis zu personalisieren.

7. Abschließend werden Sie zur Auswahl eines Abonnementplans aufgefordert. GitHub bietet verschiedene Pläne an, darunter einen kostenlosen Plan für persönliche Konten. Wählen Sie den Plan, der Ihren Bedürfnissen entspricht.

### Über Ihr persönliches Konto für GitHub

Ihr persönliches GitHub-Konto ist der Ausgangspunkt für alle Ihre Aktivitäten auf GitHub. Mit diesem Konto können Sie:

- Repositories erstellen und verwalten
- An Projekten anderer Benutzer mitarbeiten
- Issues und Pull Requests erstellen und kommentieren
- Ihr Profil anpassen, um Ihre Arbeit und Interessen zu präsentieren
- Mit anderen GitHub-Benutzern kommunizieren und zusammenarbeiten

Jedes GitHub-Konto hat ein Profil, das Informationen über Sie und Ihre Aktivitäten auf GitHub anzeigt. Ihr Profil ist Ihre öffentliche Präsenz auf GitHub und kann als eine Art Portfolio für Ihre Arbeit dienen.

### GitHub-Pläne und Kontotypen

GitHub bietet verschiedene Pläne für unterschiedliche Bedürfnisse:

- **GitHub Free**: Kostenlos für persönliche Konten und kleine Teams. Bietet unbegrenzte öffentliche und private Repositories, bis zu drei Mitarbeiter für private Repositories und grundlegende GitHub Actions-Minuten.

- **GitHub Pro**: Kostenpflichtig für Einzelpersonen. Bietet erweiterte Funktionen wie erweiterte GitHub Actions-Minuten, GitHub Codespaces und erweiterte Sicherheitsfunktionen.

- **GitHub Team**: Kostenpflichtig für Organisationen. Bietet Team-Funktionen wie Zugriffskontrollen und Teamverwaltung.

- **GitHub Enterprise**: Kostenpflichtig für große Unternehmen. Bietet erweiterte Sicherheits-, Compliance- und Verwaltungsfunktionen.

Neben persönlichen Konten gibt es auch Organisationskonten, die für Teams und Unternehmen gedacht sind. Organisationskonten ermöglichen eine feinere Kontrolle über den Zugriff auf Repositories und bieten zusätzliche Funktionen für die Teamzusammenarbeit.

<A name="Profil_einrichten"></A>
## Profil einrichten

Nach der Erstellung Ihres GitHub-Kontos ist es wichtig, Ihr Profil einzurichten, um sich der Community vorzustellen und Ihre Arbeit zu präsentieren.

### Profilbild hinzufügen

Ein Profilbild macht Ihr Konto persönlicher und hilft anderen, Sie zu erkennen. Um ein Profilbild hinzuzufügen:

1. Klicken Sie auf Ihr Profilsymbol in der oberen rechten Ecke der GitHub-Seite und wählen Sie "Einstellungen" aus dem Dropdown-Menü.

2. Scrollen Sie nach unten zum Abschnitt "Profilbild" und klicken Sie auf "Neues Bild hochladen".

3. Wählen Sie ein Bild von Ihrem Computer aus und passen Sie es bei Bedarf an.

4. Klicken Sie auf "Speichern", um Ihr neues Profilbild zu übernehmen.

### Profilinformationen bearbeiten

Ihr GitHub-Profil enthält verschiedene Informationen, die Sie anpassen können, um sich vorzustellen:

1. Navigieren Sie zu Ihrem Profil, indem Sie auf Ihr Profilsymbol klicken und "Ihr Profil" auswählen.

2. Klicken Sie auf "Profil bearbeiten", um Ihre Profilinformationen zu bearbeiten.

3. Fügen Sie einen Namen, eine Bio, einen Standort, eine Website und andere Informationen hinzu, die Sie teilen möchten.

4. Klicken Sie auf "Aktualisieren", um Ihre Änderungen zu speichern.

### README-Datei für Ihr Profil erstellen

GitHub bietet eine besondere Funktion, mit der Sie eine README-Datei direkt auf Ihrer Profilseite anzeigen können. Diese Datei kann verwendet werden, um sich ausführlicher vorzustellen, Ihre Fähigkeiten zu präsentieren oder andere Informationen zu teilen.

Um eine Profil-README zu erstellen:

1. Erstellen Sie ein neues Repository mit demselben Namen wie Ihr GitHub-Benutzername. Wenn Ihr Benutzername beispielsweise "octocat" ist, erstellen Sie ein Repository mit dem Namen "octocat".

2. Erstellen Sie in diesem Repository eine Datei mit dem Namen "README.md".

3. Bearbeiten Sie diese Datei mit Markdown-Formatierung, um Ihren Inhalt zu gestalten.

4. Committen und pushen Sie die Änderungen.

Die README-Datei wird nun automatisch auf Ihrer Profilseite angezeigt und kann verwendet werden, um sich auf kreative Weise vorzustellen.

<A name="Authentifizierung_und_Sicherheit"></A>
## Authentifizierung und Sicherheit

Die Sicherheit Ihres GitHub-Kontos ist von entscheidender Bedeutung, insbesondere wenn Sie an wichtigen Projekten arbeiten oder sensiblen Code verwalten.

### Zwei-Faktor-Authentifizierung (2FA) einrichten

Die Zwei-Faktor-Authentifizierung fügt eine zusätzliche Sicherheitsebene zu Ihrem Konto hinzu, indem sie neben Ihrem Passwort einen zweiten Authentifizierungsfaktor erfordert.

Um 2FA für Ihr GitHub-Konto einzurichten:

1. Gehen Sie zu Ihren Kontoeinstellungen, indem Sie auf Ihr Profilsymbol klicken und "Einstellungen" auswählen.

2. Klicken Sie im linken Seitenmenü auf "Passwort und Authentifizierung".

3. Scrollen Sie nach unten zum Abschnitt "Zwei-Faktor-Authentifizierung" und klicken Sie auf "Zwei-Faktor-Authentifizierung aktivieren".

4. Wählen Sie Ihre bevorzugte 2FA-Methode:
   - **SMS-Authentifizierung**: Erhalten Sie Codes per SMS auf Ihr Mobiltelefon.
   - **TOTP-Anwendung**: Verwenden Sie eine Authentifizierungs-App wie Google Authenticator oder Authy.
   - **Sicherheitsschlüssel**: Verwenden Sie einen physischen Sicherheitsschlüssel wie YubiKey.

5. Folgen Sie den Anweisungen, um die Einrichtung abzuschließen.

6. Speichern Sie Ihre Wiederherstellungscodes an einem sicheren Ort. Diese Codes ermöglichen den Zugriff auf Ihr Konto, falls Sie den Zugriff auf Ihr 2FA-Gerät verlieren.

### Persönliche Zugriffstoken (PATs)

Persönliche Zugriffstoken sind eine Alternative zu Passwörtern für die Authentifizierung bei GitHub, wenn Sie die API oder Befehlszeile verwenden. Sie bieten mehr Kontrolle und Sicherheit als Passwörter, da sie spezifische Berechtigungen haben und jederzeit widerrufen werden können.

Um ein persönliches Zugriffstoken zu erstellen:

1. Gehen Sie zu Ihren Kontoeinstellungen und klicken Sie im linken Seitenmenü auf "Entwicklereinstellungen".

2. Klicken Sie auf "Persönliche Zugriffstoken" und dann auf "Neues Token generieren".

3. Geben Sie eine Beschreibung für das Token ein und wählen Sie die Berechtigungen aus, die das Token haben soll.

4. Klicken Sie auf "Token generieren".

5. Kopieren Sie das Token und speichern Sie es an einem sicheren Ort. Aus Sicherheitsgründen wird GitHub das Token nicht erneut anzeigen.

<A name="GitHub_Desktop_installieren"></A>
## GitHub Desktop installieren

GitHub Desktop ist eine benutzerfreundliche Anwendung, die es Ihnen ermöglicht, mit GitHub zu interagieren, ohne Befehlszeilenbefehle verwenden zu müssen. Es ist ideal für Anfänger und für diejenigen, die eine visuelle Oberfläche bevorzugen.

### Installation unter Windows

1. Besuchen Sie die [GitHub Desktop-Website](https://desktop.github.com/) und klicken Sie auf "Download für Windows".

2. Öffnen Sie die heruntergeladene Installationsdatei (GitHubDesktopSetup.exe).

3. Folgen Sie den Anweisungen des Installationsassistenten, um die Installation abzuschließen.

4. Nach der Installation wird GitHub Desktop automatisch gestartet und fordert Sie zur Anmeldung mit Ihrem GitHub-Konto auf.

### Installation unter macOS

1. Besuchen Sie die [GitHub Desktop-Website](https://desktop.github.com/) und klicken Sie auf "Download für macOS".

2. Öffnen Sie die heruntergeladene DMG-Datei.

3. Ziehen Sie das GitHub Desktop-Symbol in den Anwendungsordner.

4. Öffnen Sie GitHub Desktop aus dem Anwendungsordner und melden Sie sich mit Ihrem GitHub-Konto an.

### Installation unter Linux

GitHub Desktop ist offiziell nicht für Linux verfügbar, aber es gibt Community-Forks, die Sie verwenden können:

1. Besuchen Sie das [shiftkey/desktop](https://github.com/shiftkey/desktop) Repository auf GitHub.

2. Folgen Sie den Anweisungen zur Installation der Linux-Version von GitHub Desktop.

3. Nach der Installation starten Sie die Anwendung und melden sich mit Ihrem GitHub-Konto an.

### Erste Schritte mit GitHub Desktop

Nach der Installation und Anmeldung können Sie GitHub Desktop verwenden, um:

1. Repositories zu klonen oder zu erstellen
2. Änderungen an Dateien zu committen
3. Branches zu erstellen und zwischen ihnen zu wechseln
4. Änderungen zu pushen und zu pullen
5. Pull Requests zu erstellen und zu überprüfen

GitHub Desktop bietet eine intuitive Oberfläche für diese Aufgaben und ist ein ausgezeichnetes Tool für Anfänger, die mit Git und GitHub beginnen.

<A name="Git-Kommandozeile_einrichten"></A>
## Git-Kommandozeile einrichten

Während GitHub Desktop eine benutzerfreundliche Oberfläche bietet, bevorzugen viele Entwickler die Flexibilität und Kontrolle der Git-Kommandozeile. Die Einrichtung von Git auf Ihrem System ist ein wichtiger Schritt, um mit GitHub über die Befehlszeile zu interagieren.

### Installation von Git

#### Windows

1. Besuchen Sie die [Git-Website](https://git-scm.com/download/win) und laden Sie den Installer herunter.

2. Führen Sie den Installer aus und folgen Sie den Anweisungen. Die Standardeinstellungen sind für die meisten Benutzer geeignet.

3. Während der Installation können Sie wählen, ob Git Bash (empfohlen) und Git GUI installiert werden sollen.

4. Nach Abschluss der Installation können Sie Git über die Eingabeaufforderung oder Git Bash verwenden.

#### macOS

Es gibt mehrere Möglichkeiten, Git auf macOS zu installieren:

1. **Über Homebrew**:
   ```
   brew install git
   ```

2. **Über den offiziellen Installer**:
   - Besuchen Sie die [Git-Website](https://git-scm.com/download/mac) und laden Sie den Installer herunter.
   - Führen Sie den Installer aus und folgen Sie den Anweisungen.

3. **Über Xcode Command Line Tools**:
   ```
   xcode-select --install
   ```

#### Linux

Auf den meisten Linux-Distributionen kann Git über den Paketmanager installiert werden:

- **Ubuntu/Debian**:
  ```
  sudo apt-get update
  sudo apt-get install git
  ```

- **Fedora**:
  ```
  sudo dnf install git
  ```

- **CentOS/RHEL**:
  ```
  sudo yum install git
  ```

### Git konfigurieren

Nach der Installation müssen Sie Git mit Ihren Benutzerinformationen konfigurieren:

1. Öffnen Sie ein Terminal oder eine Eingabeaufforderung.

2. Konfigurieren Sie Ihren Namen und Ihre E-Mail-Adresse:
   ```
   git config --global user.name "Ihr Name"
   git config --global user.email "ihre-email@beispiel.de"
   ```

3. Optional können Sie weitere Konfigurationen vornehmen:
   - Standard-Editor festlegen:
     ```
     git config --global core.editor "code --wait"  # Für Visual Studio Code
     ```
   - Zeilenumbrüche konfigurieren:
     ```
     git config --global core.autocrlf true  # Für Windows
     git config --global core.autocrlf input  # Für Mac/Linux
     ```

4. Überprüfen Sie Ihre Konfiguration:
   ```
   git config --list
   ```

### Authentifizierung einrichten

Um mit GitHub über die Befehlszeile zu interagieren, müssen Sie eine Authentifizierungsmethode einrichten. Die empfohlenen Methoden sind:

1. **SSH-Authentifizierung**: Wie im Abschnitt "[SSH-Schlüssel einrichten]#SSH-Schlüssel_einrichten)" beschrieben.

2. **HTTPS mit Credential Helper**:
   - Unter Windows:
     ```
     git config --global credential.helper wincred
     ```
   - Unter macOS:
     ```
     git config --global credential.helper osxkeychain
     ```
   - Unter Linux:
     ```
     git config --global credential.helper cache
     ```

3. **Persönliche Zugriffstoken**: Wie im Abschnitt "Persönliche Zugriffstoken (PATs)" beschrieben.

### Grundlegende Git-Befehle

Hier sind einige grundlegende Git-Befehle, die Sie kennen sollten:

- `git init`: Initialisiert ein neues Git-Repository
- `git clone`: Klont ein Repository von GitHub
- `git add`: Fügt Änderungen zum Staging-Bereich hinzu
- `git commit`: Committet Änderungen im Staging-Bereich
- `git push`: Überträgt lokale Commits an das Remote-Repository
- `git pull`: Holt und integriert Änderungen aus dem Remote-Repository
- `git branch`: Listet Branches auf oder erstellt einen neuen Branch
- `git checkout`: Wechselt zwischen Branches oder stellt Dateien wieder her
- `git merge`: Führt Branches zusammen
- `git status`: Zeigt den Status des Arbeitsverzeichnisses an

Diese Befehle bilden die Grundlage für die Arbeit mit Git und GitHub über die Befehlszeile.

<A name="SSH-Schlüssel_einrichten"></A>
### SSH-Schlüssel einrichten

SSH-Schlüssel bieten eine sichere Möglichkeit, sich bei GitHub zu authentifizieren, ohne jedes Mal Ihren Benutzernamen und Ihr Passwort eingeben zu müssen. Sie sind besonders nützlich für die Interaktion mit GitHub über die Befehlszeile.

Um einen SSH-Schlüssel einzurichten:

1. Öffnen Sie ein Terminal (Linux/Mac) oder Git Bash (Windows).

2. Generieren Sie ein neues SSH-Schlüsselpaar mit dem Befehl:
   ```
   ssh-keygen -t ed25519 -C "ihre-email@beispiel.de"
   ```

3. Wenn Sie zur Eingabe eines Dateinamens aufgefordert werden, drücken Sie Enter, um den Standarddateinamen zu akzeptieren.

4. Geben Sie eine sichere Passphrase ein, wenn Sie dazu aufgefordert werden.

5. Starten Sie den SSH-Agenten mit dem Befehl:
   ```
   eval "$(ssh-agent -s)"
   ```

6. Fügen Sie Ihren privaten SSH-Schlüssel zum SSH-Agenten hinzu:
   ```
   ssh-add ~/.ssh/id_ed25519
   ```

7. Kopieren Sie den Inhalt Ihrer öffentlichen SSH-Schlüsseldatei in die Zwischenablage:
   - Unter Linux/Mac: `cat ~/.ssh/id_ed25519.pub | xclip -selection clipboard`
   - Unter Windows: `cat ~/.ssh/id_ed25519.pub | clip`

8. Gehen Sie zu Ihren GitHub-Kontoeinstellungen und klicken Sie im linken Seitenmenü auf "SSH und GPG-Schlüssel".

9. Klicken Sie auf "Neuen SSH-Schlüssel hinzufügen", geben Sie einen Titel ein und fügen Sie den kopierten öffentlichen Schlüssel in das Feld "Schlüssel" ein.

10. Klicken Sie auf "SSH-Schlüssel hinzufügen", um den Vorgang abzuschließen.


<A name="Fazit"></A>
## Fazit

Die richtige Einrichtung Ihres GitHub-Kontos und Ihrer Entwicklungsumgebung ist ein wichtiger erster Schritt für eine erfolgreiche Nutzung von GitHub. Mit einem gut konfigurierten Konto, starken Sicherheitsmaßnahmen und den richtigen Tools können Sie die volle Leistungsfähigkeit von GitHub nutzen.

In den folgenden Kapiteln werden wir tiefer in die Funktionen und Workflows von GitHub eintauchen, beginnend mit grundlegenden Konzepten und fortschreitend zu fortgeschritteneren Themen wie Zusammenarbeit, CI/CD und mehr.

Denken Sie daran, dass die Einrichtung nur der Anfang ist. Die wahre Stärke von GitHub liegt in seiner Fähigkeit, Zusammenarbeit zu fördern, Code zu verwalten und Softwareentwicklungsprozesse zu verbessern. Mit einer soliden Grundlage sind Sie bereit, diese Vorteile voll auszuschöpfen.
