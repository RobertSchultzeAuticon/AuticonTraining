# git praxis

## grundlagen und begriffe

### Stage
die staging area ist kurz zusammenzufassen als "alles was grad ausgewählt ist"
die Dateien sind markiert demnächst committed zu werden

### Editor
git nutzt standartmäßig vim als editor, wem das nicht gefällt kann unter windows zum beispiel notepad++ mit dem befehl 
`git config --global core.editor "'C:/Program Files/Notepad++/notepad++.exe' -multiInst -notabbar -nosession -noPlugin"`
einstellen oder sich etwas anderes ergooglen :)


## grundlegender workflow

### ein git erstellen oder clonen
 - `git init` macht einen Ordner zum lokalen repository
 - `git clone [url]` macht eine Kopie eines repositories von der URL
 
### eine datei bearbeiten

... wie auch immer ihr dateien erstellen und editieren wollt, zum beispiel Notepad
 
### eine datei hinzufügen
 - `git add [datei]` "staged" eine Datei
 - `git add *` fügt alles zum Staging hinzu
 
### commit
 - `git commit -m "[message]"` macht einen commit mit der spezifischen nachricht
 - `git commit` öffnet den vordefinierten editor für die commit nachricht
 
### push
 - `git push origin main` pusht die aktuellen commits ins als "origin" registrierte repository auf den branch namens "main"
 
origin ist der voreingestellte name für das **upstream** repository von dem gecloned wurde
`git remote add origin git@github.com:User/UserRepo.git` fügt ein origin in ein repository ohne origin hinzu 
set-url anstatt add, würde die url von origin editieren


## Branches/checkout
ein branch ist eine getrennte version des repositories in der ein anderer Satz Änderungen existieren kann
das ist vor allem für Kooperation und Organisation nützlich, um zum Beispiel einen Satz Änderungen Stück für Stück gemeinsam zu bearbeiten 
wenn ein branch aktiviert ist, wird der stand aller dateien auf den stand im branch gesetzt und commits werden dann auf diesem branch gemacht. solange alles committed ist, kann der branch gewechselt werden ohne zu pushen

 - `git checkout -b [branchname]` erstellt einen neuen branch und aktiviert ihn gleich
 - `git checkout [branchname]` aktiviert den branch, wenn er existiert
 - `git branch -d [branchname]` löscht einen branch
 - `git push origin [branchname]` ist nötig, damit andere ihn sehen können, wie oben
 
## Kooperation

### pull
 - `git pull` "zieht" die aktuelle Version des aktiven branches vom eingestellten origin 
 - `git merge [branchname]` "verschmilzt" die änderungen eines lokal existierenden (also schonmal gepullt) branches in den aktuellen branch
 - `git diff [quellbranch] [zielbranch]` zeigt die änderungen bevor sie passieren
 
### merge 
 - wenn mergekonflike auftreten können sie manuell oder mit einem merge-tool behoben werden (beliebiger editor, kdiff3, meld, visual studio, alle jetbrains IDEs, usw)
 - danach einfach git add und commit
 

