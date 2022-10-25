# git Kurs

## Was ist git und wozu ist es gut?

Git ist ein Versionskontrollsystem, also eine Software, die Dateiänderungen verfolgt. Ein git repository (eine "Lagerstätte") ist effektiv ein Ordner, in dem git "mitschreibt" was sich an Dateien geändert hat. Das passiert nur semi-automatisch, der git-Benutzer muss einen commit (eine "einreichung") machen, bei dem die spezifischen Dateien und der Grund der Änderung festgelegt werden.
Später kann das das repository auf einen Beliebigen vorherigen Zeitpunkt zurückgesetzt werden und vieles mehr.

Ein lokales Repository selbst ist ein komplettes, fertiges Versionskontrollsystem und ist an sich schon nützlich, git bietet aber außerdem den großen Vorteil, dass verschiedene Benutzer auf verschiedenen Computern unabhängig voneinander Änderungen an den Dateien vornehmen können, die man danach zusammenführen kann und später zB Zeilengenau herauszufinden, wann, was, von wem geändert wurde.

## Nutzung von git

git ist free und open source software, github ist in dem Umfang in dem wir es hier nutzen ebenfalls gratis
wenn ein github account angelegt und git installiert ist 
(https://git-scm.com/downloads, https://github.com/join)
kann man git bash oder git gui benutzen, dieser Kurs wird sich auf git bash beschränken, um die internen Funktionsweise besser zu vermitteln.
Außerhalb dieses Kurses spricht nichts dagegen eine Gui nach Wahl zu benutzen, siehe https://git-scm.com/download/gui/windows

## Hier Relevante Grundkonzepte

**Repository**: der "git-ordner" aber auch das Projekt, ein Repository ist effektiv nur eine liste von commits
**Commit**: die einzelnen Sätze an Änderungen, das kann auch mehrere Dateien beinhalten. Ein Commit enthält die komplette neue version, als "Snapshot" und somit kann man schnell vor und zurück springen ohne jedes mal mit unterschieden rechnen zu müssen. Dementsprechend ist ein Commit auch ein eindeutiger Zustand des gesamten Repositories, und zwei Leute, die zum selben commit "gehen" (siehe checkout) sollten den selben Zustand haben. 
(zumindest dinge die teil des repositories sind)

Ein commit beinhält außerdem noch
 
 - wer hat es geändert
 - wann wurde es geändert
 - was wurde geändert
 - von wo aus wurde es geändert ("parent", also welchen Zustand hatte das Repository vorher)
 
**Branch**: Ein Branch ist eine Fassung der Zeitlinie, die ab einem bestimmten punkt abzweigt. So kann man zum Beispiel einen Branch für das neue Loginsystem haben, während auf einem anderen Branch mit dem alten Loginsystem noch funktionierend an Datenbankanbindung gearbeitet wird. Branches kann man dann mergen.

**merge**: ein zusammenführen von unterschiedlichen versionen, meist branches, an sich nur commits, dazu nächstes mal mehr

**clone**: eine lokale kopie eines repositories anlegen

### nicht git zentrale terme
Diese sachen gelten für dinge wie github oder gitlab, sind aber kein teil von git selbst, aber im allgemeinen sehr wichtig.

**Fork**: eine Kopie eines Repositories das danach dem forkenden gehört und eigener Wege gehen kann. Jeder kann zB seinen eigenen Fork eines Open-Source Projektes machen um darin Änderungen vorzunehmen und diese Version stattdessen anzubieten.

**Pullrequest**: 
ist eine Anfrage an die jeweils berechtigten Leute einen "pull" zu machen, also änderungen reinziehen.
ein pullrequest geht von einem Branch in einen anderen, nicht nur innerhalb eines repositories, sondern auch zwischen verschiedenen Forks.



# next steps

dieses repository forken, einen lokalen clone erstellen, etwas ändern, einen commit anfertigen, pushen und einen PR stellen
