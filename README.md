# Git Einstieg

## Installation von Git


## Repository initialisieren

Der aktuelle Ordner soll Git Repository Funktionen erhalten

    git init

Ein Unterordner soll als Repository initialisiert werden

    git init ORDNER
    
Es kann notwendig sein, dass der Branch von 'master' auf 'main' geändert werden muss

    git branch -M main


## Grundkonfiguration von Git

### Globale Konfiguration
    git config --global user.name "User Name"
    git config --global user.email "user.name@mail.com"

### Konfiguration eines einzelnen Repositories
Wenn man für ein einzelnes Repository diese beiden Einstellungen anders haben möchte, dann muss man in dem Repository Ordner beide Befehle ohne "--global" ausführen

    git config user.name "User Name"
    git config user.email "user.name@mail.com"


## Git Status abfragen

    git status


## Die drei Bereiche von Git

### Workingdirectory

Das aktive genutze Arbeitsverzeichnis. Es entspricht der Ansicht im Dateiexplorer.

### Stage

Die Stage enthält alle 'gestageten' Dateien und Ordner. Eine Datei aus dem Workingdirectory kann mit dem Befehl *git add* in die Stage hinzugefügt werden.

    git add FILENAME

### Repository

Um Dateien, die sich in der Stage befinden, dauerhaft in das Repository hinzuzufügen, muss man diese *committen*.  

    git commit -m 'COMMIT MESSAGE'

Die Option *-m* steht für Message. Jeder Commit benötigt eine (kurze) Commitmessage. Diese sollte knapp und verständlich den Inhalt/ Grund des Commits wiedergeben.  
Beispiel für einen ersten Commit:  
    git commit -m "init commit"

## Git SSH

### Mehere SSH Keys verwenden
#### I. Clonen 

    `GIT_SSH_COMMAND="ssh -i ~/.ssh/SSHKEY" git clone URL`

#### II. Lokales Repository dauerhaft anpassen

    git config core.sshCommand 'ssh -i ~/.ssh/SSHKEY -F /dev/null'
