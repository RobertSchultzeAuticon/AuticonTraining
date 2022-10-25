# git Kurs

## Was ist git und wozu ist es gut?

Git ist ein Versionskontrollsystem, also eine Software, die Dateiänderungen verfolgt. Ein git-Repository (eine "Lagerstätte") ist effektiv ein Ordner, in dem git "mitschreibt" was sich an Dateien geändert hat. Das passiert nur semi-automatisch, git-Benutzer**innen müssen einen Commit (eine "Einreichung") machen, bei dem die spezifischen Dateien und der Grund der Änderung festgelegt werden.
Später kann das Repository auf einen beliebigen vorherigen Zeitpunkt zurückgesetzt werden und vieles mehr.

Ein lokales Repository selbst ist ein komplettes, fertiges Versionskontrollsystem und ist an sich schon nützlich, git bietet aber außerdem den großen Vorteil, dass verschiedene Benutzer auf verschiedenen Computern unabhängig voneinander Änderungen an den Dateien vornehmen können, die man danach zusammenführen kann und später z.B. zeilengenau herauszufinden, wann, was, von wem geändert wurde.

## Nutzung von git

git ist free und Open-Source-Software, github ist in dem Umfang, in dem wir es hier nutzen, ebenfalls gratis.
Wenn ein GitHub-Account angelegt und git installiert ist (https://git-scm.com/downloads, https://github.com/join), kann man git bash oder git gui benutzen, dieser Kurs wird sich auf git bash beschränken, um die internen Funktionsweise besser zu vermitteln.
Außerhalb dieses Kurses spricht nichts dagegen, eine GUI nach Wahl zu benutzen, siehe https://git-scm.com/download/gui/windows

## Hier relevante Grundkonzepte

**Repository**: der "git-Ordner" aber auch das Projekt, ein Repository ist effektiv nur eine Liste von Commits
**Commit**: die einzelnen Sätze an Änderungen, der kann auch mehrere Dateien beinhalten. Ein Commit enthält die komplette neue Version, als "Snapshot" und somit kann man schnell vor und zurück springen ohne jedes Mal mit Unterschieden rechnen zu müssen. Dementsprechend ist ein Commit auch ein eindeutiger Zustand des gesamten Repositories, und zwei Leute, die zum selben commit "gehen" (siehe checkout), sollten den selben Zustand haben. 
(zumindest dinge die teil des repositories sind)

Ein Commit beinhält außerdem noch
 
 - wer hat es geändert
 - wann wurde es geändert
 - was wurde geändert
 - von wo aus wurde es geändert ("parent", also welchen Zustand hatte das Repository vorher)
 
**Branch**: Ein Branch ist eine Fassung der Zeitlinie, die ab einem bestimmten Punkt abzweigt. So kann man zum Beispiel einen Branch für das neue Loginsystem haben, während auf einem anderen Branch mit dem alten Loginsystem noch funktionierend an Datenbankanbindung gearbeitet wird. Branches kann man dann mergen.

**merge**: ein Zusammenführen von unterschiedlichen Versionen, meist Branches, an sich nur Commits, dazu nächstes Mal mehr

**clone**: eine lokale Kopie eines Repositories anlegen

### nicht git zentrale terme
Diese Sachen gelten für Dinge wie github oder gitlab, sind aber kein Teil von git selbst, aber im allgemeinen sehr wichtig.

**Fork**: eine Kopie eines Repositories das danach dem forkenden gehört und eigener Wege gehen kann. Jeder kann z.B. seinen eigenen Fork eines Open-Source-Projektes machen um darin Änderungen vorzunehmen und diese Version stattdessen anzubieten.

**Pullrequest**: ist eine Anfrage an die jeweils berechtigten Leute, einen "pull" zu machen, also Änderungen reinziehen.
Ein pullrequest geht von einem Branch in einen anderen, nicht nur innerhalb eines Repositories, sondern auch zwischen verschiedenen Forks.

# Next Steps

Dieses Repository forken, einen lokalen Clone erstellen, etwas ändern, einen Commit anfertigen, pushen und einen PR stellen
