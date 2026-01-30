# 5. Git-Grundlagen für GitHub

## Einführung in Git

### Video-Tutorial: Git-Grundlagen
[Git Tutorial Deutsch #1 Was ist Git?](https://www.youtube.com/watch?v=MgnRFZJ7M2s)
[Git Tutorial - In 40 Minuten Git lernen für Anfänger](https://www.youtube.com/watch?v=uGLQF2kUwOA)

Git ist ein verteiltes Versionskontrollsystem, das die Grundlage für GitHub bildet. Es wurde 2005 von Linus Torvalds, dem Schöpfer des Linux-Kernels, entwickelt, um die Zusammenarbeit an großen Softwareprojekten zu verbessern. Um GitHub effektiv nutzen zu können, ist ein grundlegendes Verständnis von Git unerlässlich.

### Was ist Versionskontrolle?

Versionskontrolle ist ein System, das Änderungen an Dateien über die Zeit aufzeichnet, sodass Sie bestimmte Versionen später abrufen können. Sie ermöglicht es Entwicklern, frühere Versionen von Code wiederherzustellen, Änderungen zu vergleichen, zu sehen, wer eine Änderung vorgenommen hat, und vieles mehr.

Versionskontrollsysteme bieten folgende Vorteile:

- Vollständiger Änderungsverlauf jeder Datei
- Nachvollziehbarkeit, wer wann welche Änderungen vorgenommen hat
- Möglichkeit, zu früheren Versionen zurückzukehren
- Parallele Entwicklung durch Branching und Merging
- Backup und Wiederherstellung

### Verteilte vs. zentralisierte Versionskontrolle

Es gibt zwei Haupttypen von Versionskontrollsystemen:

**Zentralisierte Versionskontrollsysteme (CVCS)** wie SVN (Subversion) haben einen zentralen Server, der alle Dateiversionen enthält. Entwickler checken Dateien aus diesem zentralen Repository aus und wieder ein. Der Nachteil ist, dass bei einem Serverausfall niemand zusammenarbeiten oder Änderungen speichern kann.

**Verteilte Versionskontrollsysteme (DVCS)** wie Git hingegen ermöglichen es jedem Entwickler, eine vollständige Kopie des Repositories einschließlich seiner gesamten Historie lokal zu haben. Dies bietet mehrere Vorteile:

- Arbeiten ohne Internetverbindung
- Schnellere Operationen, da die meisten Aktionen lokal stattfinden
- Jeder Klon ist ein vollständiges Backup des Repositories
- Flexiblere Workflows und Zusammenarbeit

Git ist ein DVCS und bietet daher all diese Vorteile. GitHub erweitert Git um eine webbasierte Oberfläche und kollaborative Funktionen, die die Zusammenarbeit noch weiter vereinfachen.

### Git-Architektur

Um Git effektiv zu nutzen, ist es wichtig, seine grundlegende Architektur zu verstehen:

1. **Arbeitsverzeichnis**: Dies ist der Ordner auf Ihrem Computer, der die aktuellen Dateien enthält, an denen Sie arbeiten.

2. **Staging-Bereich (Index)**: Ein Zwischenbereich, in dem Sie Änderungen für den nächsten Commit vorbereiten. Hier können Sie auswählen, welche Änderungen Sie committen möchten.

3. **Lokales Repository**: Eine Datenbank auf Ihrem Computer, die alle Versionen Ihrer Dateien und die vollständige Projekthistorie enthält.

4. **Remote-Repository**: Eine Version Ihres Repositories, die auf einem Server (wie GitHub) gehostet wird und mit anderen geteilt werden kann.

Der typische Git-Workflow umfasst:
- Änderungen im Arbeitsverzeichnis vornehmen
- Ausgewählte Änderungen zum Staging-Bereich hinzufügen
- Änderungen aus dem Staging-Bereich in das lokale Repository committen
- Commits mit dem Remote-Repository synchronisieren (push/pull)

## Grundlegende Git-Befehle

Um effektiv mit Git und GitHub zu arbeiten, sollten Sie die folgenden grundlegenden Befehle verstehen und beherrschen.

### Repository initialisieren und klonen

**Repository initialisieren**:
```
git init
```
Dieser Befehl erstellt ein neues, leeres Git-Repository im aktuellen Verzeichnis. Er initialisiert ein `.git`-Unterverzeichnis, das alle notwendigen Metadaten für das Repository enthält.

**Repository klonen**:
```
git clone https://github.com/benutzername/repository-name.git
```
Dieser Befehl erstellt eine lokale Kopie eines Remote-Repositories. Er lädt alle Dateien, Branches und die gesamte Commit-Historie herunter.

### Änderungen verfolgen

**Status überprüfen**:
```
git status
```
Zeigt den Status des Arbeitsverzeichnisses und des Staging-Bereichs an. Es informiert über geänderte Dateien, die noch nicht zum Staging-Bereich hinzugefügt wurden, und über Änderungen im Staging-Bereich, die noch nicht committet wurden.

**Änderungen zum Staging-Bereich hinzufügen**:
```
git add dateiname.txt    # Eine bestimmte Datei hinzufügen
git add verzeichnis/     # Ein Verzeichnis hinzufügen
git add .                # Alle Änderungen hinzufügen
```
Diese Befehle fügen Änderungen zum Staging-Bereich hinzu, wodurch sie für den nächsten Commit vorbereitet werden.

**Änderungen committen**:
```
git commit -m "Beschreibende Commit-Nachricht"
```
Dieser Befehl speichert die Änderungen aus dem Staging-Bereich dauerhaft im Repository. Jeder Commit erstellt einen Snapshot des Projekts zu diesem Zeitpunkt.

**Änderungen ohne Staging committen**:
```
git commit -a -m "Commit-Nachricht"
```
Dieser Befehl fügt automatisch alle bereits verfolgten Dateien zum Staging-Bereich hinzu und committet sie. Neue Dateien werden jedoch nicht einbezogen.

### Mit Remote-Repositories arbeiten

**Remote-Repository hinzufügen**:
```
git remote add origin https://github.com/benutzername/repository-name.git
```
Dieser Befehl verknüpft Ihr lokales Repository mit einem Remote-Repository auf GitHub.

**Remote-Repositories anzeigen**:
```
git remote -v
```
Zeigt alle konfigurierten Remote-Repositories mit ihren URLs an.

**Änderungen pushen**:
```
git push origin main
```
Dieser Befehl überträgt Ihre lokalen Commits zum Remote-Repository. `origin` ist der Standardname für das Remote-Repository, und `main` ist der Branch, zu dem Sie pushen.

**Änderungen pullen**:
```
git pull origin main
```
Dieser Befehl holt Änderungen vom Remote-Repository und führt sie mit Ihrem lokalen Branch zusammen. Es ist eine Kombination aus `git fetch` und `git merge`.

**Änderungen fetchen**:
```
git fetch origin
```
Dieser Befehl lädt Änderungen vom Remote-Repository herunter, ohne sie automatisch mit Ihrem lokalen Branch zusammenzuführen. Dies ist nützlich, um zu sehen, was sich geändert hat, bevor Sie die Änderungen integrieren.

### Mit Branches arbeiten

**Neuen Branch erstellen**:
```
git branch neuer-branch-name
```
Dieser Befehl erstellt einen neuen Branch, wechselt aber nicht automatisch zu diesem.

**Neuen Branch erstellen und zu diesem wechseln**:
```
git checkout -b neuer-branch-name
```
Dieser Befehl erstellt einen neuen Branch und wechselt sofort zu diesem.

**Zu einem Branch wechseln**:
```
git checkout branch-name
```
Dieser Befehl wechselt zu einem bestehenden Branch.

**Alle Branches anzeigen**:
```
git branch          # Lokale Branches anzeigen
git branch -a       # Alle Branches (lokal und remote) anzeigen
```
Diese Befehle zeigen eine Liste aller verfügbaren Branches an.

**Branch löschen**:
```
git branch -d branch-name       # Lokalen Branch löschen
git push origin --delete branch-name  # Remote-Branch löschen
```
Diese Befehle löschen einen Branch lokal oder remote.

### Änderungen zusammenführen

**Branches zusammenführen**:
```
git checkout zielbranch
git merge quellbranch
```
Diese Befehle führen Änderungen aus einem Branch (quellbranch) in einen anderen (zielbranch) zusammen.

**Merge-Konflikte lösen**:
Wenn Git nicht automatisch entscheiden kann, wie Änderungen zusammengeführt werden sollen, entsteht ein Merge-Konflikt. Die Konfliktdateien werden mit speziellen Markierungen versehen:
```
<<<<<<< HEAD
Änderungen im aktuellen Branch
=======
Änderungen im zu mergenden Branch
>>>>>>> branch-name
```
Sie müssen diese Konflikte manuell lösen, indem Sie die Dateien bearbeiten, die Markierungen entfernen und die gewünschte endgültige Version erstellen. Anschließend fügen Sie die gelösten Dateien zum Staging-Bereich hinzu und committen sie.

### Änderungen überprüfen

**Commit-Historie anzeigen**:
```
git log                 # Vollständige Historie anzeigen
git log --oneline       # Kompakte Historie anzeigen
git log --graph --oneline  # Grafische Darstellung der Historie
```
Diese Befehle zeigen die Commit-Historie des Repositories an.

**Änderungen zwischen Commits anzeigen**:
```
git diff                # Änderungen im Arbeitsverzeichnis anzeigen
git diff --staged       # Änderungen im Staging-Bereich anzeigen
git diff commit1 commit2  # Unterschiede zwischen zwei Commits anzeigen
```
Diese Befehle zeigen detaillierte Unterschiede zwischen verschiedenen Versionen an.

**Informationen zu einem Commit anzeigen**:
```
git show commit-hash
```
Dieser Befehl zeigt detaillierte Informationen zu einem bestimmten Commit an, einschließlich der Änderungen.

### Änderungen rückgängig machen

**Änderungen im Arbeitsverzeichnis verwerfen**:
```
git checkout -- dateiname.txt
```
Dieser Befehl verwirft Änderungen an einer Datei im Arbeitsverzeichnis und stellt die Version aus dem letzten Commit wieder her.

**Änderungen aus dem Staging-Bereich entfernen**:
```
git reset HEAD dateiname.txt
```
Dieser Befehl entfernt eine Datei aus dem Staging-Bereich, behält aber die Änderungen im Arbeitsverzeichnis bei.

**Letzten Commit ändern**:
```
git commit --amend -m "Neue Commit-Nachricht"
```
Dieser Befehl ändert den letzten Commit, indem er neue Änderungen hinzufügt oder die Commit-Nachricht aktualisiert.

**Zu einem früheren Commit zurückkehren**:
```
git reset --soft commit-hash   # Behält Änderungen im Staging-Bereich
git reset --mixed commit-hash  # Behält Änderungen im Arbeitsverzeichnis (Standard)
git reset --hard commit-hash   # Verwirft alle Änderungen
```
Diese Befehle setzen den aktuellen Branch auf einen früheren Commit zurück, mit unterschiedlichen Auswirkungen auf Ihre Änderungen.

## Git-Workflows für GitHub

Ein Git-Workflow ist ein Rezept oder eine Empfehlung für die Verwendung von Git in Ihrem Projekt. Es gibt verschiedene Workflows, die je nach Projektgröße, Teamstruktur und Entwicklungsprozess geeignet sein können.

### GitHub Flow

GitHub Flow ist ein einfacher, leichtgewichtiger Workflow, der sich gut für kontinuierliche Bereitstellung und kleinere Teams eignet:

1. **Erstellen eines Branches**: Erstellen Sie einen neuen Branch von `main` für jede neue Funktion oder Fehlerbehebung.
2. **Änderungen vornehmen**: Nehmen Sie Ihre Änderungen im Branch vor und committen Sie regelmäßig.
3. **Pull Request erstellen**: Öffnen Sie einen Pull Request, um Feedback zu Ihren Änderungen zu erhalten.
4. **Diskussion und Review**: Diskutieren Sie Ihre Änderungen und nehmen Sie bei Bedarf weitere Commits vor.
5. **Deployment und Tests**: Testen Sie Ihre Änderungen in einer Produktionsumgebung.
6. **Zusammenführen**: Führen Sie den Branch in `main` zusammen, wenn alles in Ordnung ist.

Dieser Workflow ist einfach zu verstehen und zu implementieren, eignet sich aber möglicherweise nicht für Projekte mit formellen Releases oder mehreren Versionen.

### Git Flow

Git Flow ist ein robusterer Workflow, der sich gut für Projekte mit geplanten Releases eignet:

1. **Hauptbranches**: `main` (Produktionscode) und `develop` (Entwicklungscode)
2. **Feature-Branches**: Zweige von `develop` für neue Funktionen
3. **Release-Branches**: Zweige von `develop` zur Vorbereitung eines Releases
4. **Hotfix-Branches**: Zweige von `main` für dringende Fehlerbehebungen
5. **Zusammenführen**: Feature-Branches werden in `develop` zusammengeführt, Release-Branches in `main` und `develop`, Hotfix-Branches in `main` und `develop`

Git Flow bietet eine klare Struktur für die Verwaltung von Releases, ist aber komplexer und kann für kleinere Projekte oder kontinuierliche Bereitstellung zu schwerfällig sein.

### Trunk-Based Development

Trunk-Based Development konzentriert sich auf die regelmäßige Integration von Code in einen einzelnen Hauptbranch (den "Trunk", normalerweise `main`):

1. **Kurze Branches**: Entwickler erstellen kurzlebige Feature-Branches, die schnell wieder in `main` integriert werden.
2. **Häufige Integration**: Code wird mehrmals täglich in `main` integriert.
3. **Feature Flags**: Unvollständige Funktionen werden hinter Feature Flags versteckt.
4. **Automatisierte Tests**: Umfangreiche automatisierte Tests stellen sicher, dass der Hauptbranch stabil bleibt.

Dieser Workflow fördert kontinuierliche Integration und reduziert Merge-Konflikte, erfordert jedoch eine starke Testautomatisierung und Disziplin im Team.

### Forking Workflow

Der Forking Workflow ist besonders in Open-Source-Projekten beliebt:

1. **Fork erstellen**: Jeder Entwickler erstellt einen persönlichen Fork des offiziellen Repositories.
2. **Lokales Klonen**: Der Entwickler klont seinen Fork lokal.
3. **Upstream hinzufügen**: Der Entwickler fügt das offizielle Repository als "upstream" Remote hinzu.
4. **Feature-Branch erstellen**: Der Entwickler erstellt einen Branch für seine Änderungen.
5. **Änderungen pushen**: Der Entwickler pusht seine Änderungen zu seinem Fork.
6. **Pull Request erstellen**: Der Entwickler erstellt einen Pull Request vom Branch in seinem Fork zum offiziellen Repository.

Dieser Workflow bietet eine klare Trennung zwischen offiziellen und Beitragsrepositorys und ist ideal für Projekte mit vielen externen Beitragenden.

## Fortgeschrittene Git-Techniken

Nachdem Sie die Grundlagen beherrschen, können Sie Ihre Git-Fähigkeiten mit fortgeschrittenen Techniken erweitern.

### Stashing

Stashing ermöglicht es Ihnen, Änderungen vorübergehend zu speichern, ohne sie zu committen:

```
git stash                  # Änderungen stashen
git stash list             # Liste aller Stashes anzeigen
git stash apply            # Letzten Stash anwenden, ohne ihn zu entfernen
git stash pop              # Letzten Stash anwenden und entfernen
git stash drop             # Letzten Stash entfernen
git stash clear            # Alle Stashes entfernen
```

Stashing ist nützlich, wenn Sie schnell den Branch wechseln müssen, aber Ihre aktuellen Änderungen noch nicht committen möchten.

### Rebasing

Rebasing ist eine Alternative zum Merging, die eine lineare Projekthistorie erzeugt:

```
git checkout feature-branch
git rebase main
```

Diese Befehle nehmen die Änderungen aus dem Feature-Branch und wenden sie auf den neuesten Stand des Hauptbranches an. Dies erzeugt eine sauberere Historie, kann aber problematisch sein, wenn der Branch bereits gepusht wurde.

**Interaktives Rebasing**:
```
git rebase -i HEAD~3
```

Dieser Befehl startet ein interaktives Rebase für die letzten drei Commits. Sie können Commits zusammenfassen, bearbeiten, umsortieren oder entfernen.

### Cherry-Picking

Cherry-Picking ermöglicht es Ihnen, bestimmte Commits aus einem Branch in einen anderen zu übernehmen:

```
git cherry-pick commit-hash
```

Dieser Befehl wendet die Änderungen eines bestimmten Commits auf den aktuellen Branch an. Dies ist nützlich, wenn Sie nur bestimmte Änderungen übernehmen möchten, nicht aber den gesamten Branch.

### Submodule und Subtrees

Submodule und Subtrees ermöglichen es, externe Repositories in Ihr Projekt einzubinden:

**Submodule**:
```
git submodule add https://github.com/benutzername/repository-name.git pfad/zum/submodule
git submodule update --init --recursive
```

Submodule sind nützlich, wenn Sie externe Projekte einbinden möchten, ohne deren Code direkt in Ihr Repository zu kopieren.

**Subtrees**:
```
git subtree add --prefix=pfad/zum/subtree https://github.com/benutzername/repository-name.git main --squash
```

Subtrees bieten eine Alternative zu Submodulen, bei der der externe Code direkt in Ihr Repository integriert wird.

### Git Hooks

Git Hooks sind Skripte, die automatisch ausgeführt werden, wenn bestimmte Git-Ereignisse eintreten:

1. **Pre-commit**: Wird vor einem Commit ausgeführt, kann verwendet werden, um Code zu linting oder Tests durchzuführen.
2. **Post-commit**: Wird nach einem Commit ausgeführt, kann für Benachrichtigungen verwendet werden.
3. **Pre-push**: Wird vor einem Push ausgeführt, kann verwendet werden, um sicherzustellen, dass alle Tests bestanden werden.
4. **Post-receive**: Wird auf dem Server nach dem Empfang eines Pushes ausgeführt, kann für Deployment verwendet werden.

Git Hooks werden im Verzeichnis `.git/hooks` gespeichert und müssen ausführbar sein.

### Git Aliases

Git Aliases ermöglichen es Ihnen, eigene Abkürzungen für häufig verwendete Git-Befehle zu erstellen:

```
git config --global alias.co checkout
git config --global alias.br branch
git config --global alias.ci commit
git config --global alias.st status
```

Nach dieser Konfiguration können Sie `git co` anstelle von `git checkout` verwenden, was Zeit spart und die Effizienz erhöht.

## Git und GitHub integrieren

Git und GitHub arbeiten nahtlos zusammen, aber es gibt einige spezifische Aspekte, die Sie beachten sollten.

### SSH vs. HTTPS für GitHub

Es gibt zwei Hauptmethoden, um mit GitHub-Repositories zu interagieren:

**HTTPS**:
- Einfacher einzurichten
- Funktioniert auch in restriktiven Netzwerken
- Erfordert regelmäßige Passworteingabe (es sei denn, Sie verwenden einen Credential Helper)

**SSH**:
- Sicherer
- Keine Passworteingabe erforderlich nach der Einrichtung
- Kann in einigen Netzwerken blockiert sein

Um SSH für GitHub einzurichten:
1. Generieren Sie ein SSH-Schlüsselpaar
2. Fügen Sie den öffentlichen Schlüssel zu Ihrem GitHub-Konto hinzu
3. Testen Sie die Verbindung mit `ssh -T git@github.com`

### GitHub CLI

GitHub CLI ist ein Kommandozeilentool, das die Interaktion mit GitHub direkt vom Terminal aus ermöglicht:

```
gh repo create       # Repository erstellen
gh pr create         # Pull Request erstellen
gh issue create      # Issue erstellen
gh repo clone        # Repository klonen
```

GitHub CLI vereinfacht viele GitHub-spezifische Aufgaben und integriert sich gut mit Git.

### Git Credential Manager

Git Credential Manager speichert Ihre Anmeldeinformationen sicher, sodass Sie sie nicht bei jedem Push eingeben müssen:

**Windows**:
Git Credential Manager wird automatisch mit Git for Windows installiert.

**macOS**:
```
git config --global credential.helper osxkeychain
```

**Linux**:
```
git config --global credential.helper cache
```

Dies verbessert den Workflow, insbesondere wenn Sie HTTPS für die Verbindung zu GitHub verwenden.

### .gitignore und GitHub-spezifische Dateien

**.gitignore** ist eine spezielle Datei, die Git mitteilt, welche Dateien und Verzeichnisse ignoriert werden sollen. GitHub bietet vorgefertigte .gitignore-Vorlagen für verschiedene Programmiersprachen und Frameworks.

Andere wichtige GitHub-spezifische Dateien sind:

- **README.md**: Die Hauptdokumentationsdatei, die auf der Repository-Hauptseite angezeigt wird.
- **LICENSE**: Definiert die Lizenzbedingungen für Ihr Projekt.
- **CONTRIBUTING.md**: Richtlinien für Beitragende.
- **CODE_OF_CONDUCT.md**: Verhaltensregeln für die Projektgemeinschaft.
- **.github/workflows/**: Verzeichnis für GitHub Actions-Workflows.
- **.github/ISSUE_TEMPLATE/**: Vorlagen für Issues.
- **.github/PULL_REQUEST_TEMPLATE.md**: Vorlage für Pull Requests.

Diese Dateien helfen, Ihr Repository zu strukturieren und die Zusammenarbeit zu erleichtern.

## Git-Best-Practices

Die Einhaltung von Best Practices kann Ihnen helfen, Git effektiver zu nutzen und häufige Probleme zu vermeiden.

### Commit-Nachrichten

Gute Commit-Nachrichten sind entscheidend für die Nachvollziehbarkeit und Zusammenarbeit:

1. **Kurze, beschreibende Betreffzeile** (max. 50 Zeichen)
2. **Leerzeile** zwischen Betreff und Hauptteil
3. **Detaillierter Hauptteil** (bei Bedarf), der erklärt, WAS und WARUM (nicht WIE)
4. **Verwendung der Befehlsform** ("Füge Feature hinzu" statt "Feature hinzugefügt")
5. **Referenzierung von Issues** (z.B. "Fixes #123")

Beispiel für eine gute Commit-Nachricht:
```
Füge Benutzerauthentifizierung hinzu

- Implementiere Login-Formular mit E-Mail und Passwort
- Füge Passwort-Hashing mit bcrypt hinzu
- Erstelle JWT-basierte Sitzungsverwaltung

Löst Issue #42
```

### Atomic Commits

Atomic Commits sind Commits, die eine einzelne, zusammenhängende Änderung enthalten:

1. **Eine logische Änderung pro Commit**
2. **Vollständige Änderungen** (keine halbfertigen Funktionen)
3. **Tests und Dokumentation** zusammen mit dem Code

Atomic Commits machen es einfacher, Änderungen zu verstehen, zu überprüfen und bei Bedarf rückgängig zu machen.

### Branching-Strategien

Effektive Branching-Strategien verbessern die Zusammenarbeit und Code-Qualität:

1. **Kurze Lebensdauer von Branches**: Halten Sie Feature-Branches kurz und führen Sie sie regelmäßig zusammen.
2. **Beschreibende Branch-Namen**: Verwenden Sie beschreibende Namen wie `feature/user-authentication` oder `bugfix/login-error`.
3. **Regelmäßiges Rebasing oder Merging**: Halten Sie Ihre Branches aktuell mit dem Hauptbranch.
4. **Branch-Hygiene**: Löschen Sie Branches nach dem Zusammenführen.

### Häufige Fehler vermeiden

Einige häufige Git-Fehler und wie man sie vermeidet:

1. **Große Binärdateien committen**: Verwenden Sie `.gitignore` und erwägen Sie Git LFS für große Dateien.
2. **Sensible Daten committen**: Verwenden Sie `.gitignore` für Konfigurationsdateien mit Passwörtern und API-Schlüsseln.
3. **Direkt in den Hauptbranch committen**: Verwenden Sie immer Feature-Branches für Änderungen.
4. **Unzureichende Commit-Nachrichten**: Schreiben Sie aussagekräftige Commit-Nachrichten.
5. **Force-Push ohne Vorsicht**: Vermeiden Sie `git push --force`, es sei denn, Sie wissen genau, was Sie tun.
6. **Merge-Konflikte ignorieren**: Lösen Sie Konflikte sorgfältig und testen Sie nach dem Zusammenführen.

## Git-Troubleshooting

Selbst erfahrene Entwickler stoßen gelegentlich auf Probleme mit Git. Hier sind einige häufige Probleme und ihre Lösungen.

### Merge-Konflikte lösen

Merge-Konflikte treten auf, wenn Git nicht automatisch entscheiden kann, wie Änderungen zusammengeführt werden sollen:

1. **Identifizieren Sie die Konfliktdateien** mit `git status`
2. **Öffnen Sie die Dateien** und suchen Sie nach Konfliktmarkierungen (`<<<<<<<`, `=======`, `>>>>>>>`)
3. **Bearbeiten Sie die Dateien**, um die gewünschte endgültige Version zu erstellen
4. **Entfernen Sie die Konfliktmarkierungen**
5. **Fügen Sie die gelösten Dateien hinzu** mit `git add`
6. **Schließen Sie den Merge ab** mit `git commit`

### Verlorene Commits wiederherstellen

Wenn Sie versehentlich Commits verloren haben, können Sie sie oft wiederherstellen:

1. **Reflog überprüfen**: `git reflog` zeigt eine Historie aller Aktionen in Ihrem Repository
2. **Commit identifizieren**: Finden Sie den Hash des verlorenen Commits
3. **Branch erstellen**: `git branch wiederherstellung commit-hash`
4. **Oder Cherry-Pick verwenden**: `git cherry-pick commit-hash`

### Fehlgeschlagene Pushes beheben

Wenn ein Push fehlschlägt, liegt das oft daran, dass Ihr lokaler Branch nicht aktuell ist:

1. **Änderungen pullen**: `git pull origin main`
2. **Merge-Konflikte lösen** (falls vorhanden)
3. **Erneut pushen**: `git push origin main`

Alternativ können Sie auch rebasen:
1. **Änderungen fetchen**: `git fetch origin`
2. **Rebase durchführen**: `git rebase origin/main`
3. **Erneut pushen**: `git push origin main`

### Große Dateien aus der Historie entfernen

Wenn Sie versehentlich große Dateien committet haben, können Sie sie mit `git filter-branch` oder dem BFG Repo-Cleaner entfernen:

**Mit BFG** (einfacher):
1. Installieren Sie BFG: `java -jar bfg.jar`
2. Führen Sie aus: `java -jar bfg.jar --delete-files grosse-datei.zip mein-repository`
3. Bereinigen Sie: `git reflog expire --expire=now --all && git gc --prune=now --aggressive`
4. Force-Push: `git push --force`

**Mit filter-branch** (komplexer, aber ohne zusätzliche Tools):
```
git filter-branch --force --index-filter 'git rm --cached --ignore-unmatch pfad/zur/grossen/datei' --prune-empty --tag-name-filter cat -- --all
```

### Repository reparieren

Wenn Ihr Repository beschädigt ist, können Sie versuchen, es zu reparieren:

1. **Konsistenz prüfen**: `git fsck`
2. **Garbage Collection**: `git gc`
3. **Repository packen**: `git repack -a -d`
4. **Referenzen prüfen**: `git fsck --full`

Wenn diese Schritte nicht helfen, ist es oft einfacher, ein frisches Klon zu erstellen.

## Fazit

Git ist ein leistungsstarkes Werkzeug, das die Grundlage für GitHub bildet. Mit einem soliden Verständnis der Git-Grundlagen können Sie GitHub effektiver nutzen und produktiver mit anderen zusammenarbeiten. Die in diesem Kapitel behandelten Konzepte und Befehle bilden das Fundament für die erfolgreiche Arbeit mit Git und GitHub.

In den folgenden Kapiteln werden wir uns mit fortgeschritteneren GitHub-Funktionen befassen, die auf diesen Git-Grundlagen aufbauen, wie Zusammenarbeit mit anderen Entwicklern, GitHub Actions für CI/CD und GitHub Pages für Webhosting.
