# Quarto Dateien

Das Projekt selbst und wie es gerendet wird, lebt in den *quarto*.yml* Dateien. Diese Dokumentation wird nur auf das wichtigste was in diesen Dateien steht eingehen, nutzen Sie für alles andere die offizielle Quarto-Dokumentation.

## quarto.yml

Die Grundlegenste Datei ist *quarto.yml*. Wenn man *quarto render* ohne Profilspezifikation ausführt, wird diese Datei angesprochen.

Öffnen Sie die Datei und ändern Sie zunächst den Projekttitel zum Namen Ihres Kurses um, und den Autor zu Ihnen selbst.

*profile:group:* enthält eine Liste aller beim rendering vorhandenen Profile. Das erste in dieser Liste wird genutzt, wenn kein Profil angegeben wurde, also bei einem leerem *quarto render*. Wenn Sie ein neues Profil anlegen möchten, muss es mit in diese Liste überführt werden.

## quarto-skript.yml

Das hier ist die wichtigste Datei. In ihr wird die Website selbst definiert und alle .html-Seiten die gerendert werden sollen.

### project:render:

Hier steht der Pfad zu allen Dokumenten die grundsätzlich gerendert werden, unabhängig davon ob diese am Ende auf der Website angezeigt werden sollen oder nicht. Wenn Sie beispielsweise "Material/Inhalte/1I_Einfuehrung.qmd" hier auskommentieren, wird dieses Kapitel nicht mehr mit gerendert.

### website:sidebar:

Hier werden alle Verlinkungen auf der Website angegeben. Beispielsweise wird bestimmt, welche Links angezeigt werden, wenn man in der Navigationsleiste oben auf Inhalte drückt. Es wird auch bestimmt, welche Elemente überhaupt in der Navigationsleiste vorliegen.

### Unterschied der beiden

Wenn ein Dokument nur in *project:render:* steht wird es gerendert und man kann mit der richtigen Pfad-URL auf dieses zugreifen, aber auf der Website gibt es keinen Link zu diesem.

Wenn ein Dokument nur in *website:sidebar:* steht, gibt es einen Link auf der Seite der zu nichts führt.

Neue Dokumente sollten daher in beiden stehen. Wie man Dokumente hinzufügt wird in einem zukünftigen Kapitel geklärt.

### format: und author:

Allgemeines was Sie besser in der offiziellen Quarto-Dokumentation nachlesen. Wenn es Sie interessiert, probieren Sie es die Werte zu ändern und prüfen dann den dazugehörigen Effekt auf die Seite.

## _quarto-pdfs.yml

In diesem Profil werden die pdfs der Begleitdokumente und der Inhalte gerendert. Standardmäßig werden alle gerendert. Unter *format:* wird die Extension angesprochen, mit welcher die pdf am Ende so aussieht wie sie soll (mit dem HsH-Logo usw).

## quarto-cheatsheet.yml

Hiermit wird das Cheatsheet als pdf gerendert. Auch hier bestimmt *format:* die Extension die das Aussehen des Cheatsheets bestimmt. Weil das Aussehen der pdf etwas anders ist als bei den anderen Dokumenten, nutzt es seine eigene Extension und braucht entsprechend auch ein eigenes Profil, weswegen es nicht mit in _quarto-pdfs.yml gerendert wird. 

## quarto-notebooks.yml

Hier werden die .ipynb Notebooks der Begleitdokumente gerendert.

## quarto-aufgaben.yml

Hier werden die Aufgabenblätter als pdfs und ipynbs gerendert. Unter *format:* wird die selbe Extension genutzt wie im Profil pdfs.

## quarto-folien.yml

Hier kann man optional die nicht für die Website notwendigen Vorlesungsfolien rendern. Unter *format:revealjs:footer:* sollten Sie den footer der Folien zu etwas für Ihre Lehrveranstaltung angemessenem ändern.

## Navigation

[Vorseite](./ordnerstruktur.md) / [Nachseite](./inhaltliche-anpassungen.md)
