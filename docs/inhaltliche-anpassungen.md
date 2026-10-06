# Inhaltliche Anpassungen

Sie haben nun verschiedene Dokumente, welche Sie über die Website erreichen können. Bevor wir dazu kommen wie Sie weitere Dokumente hinzufügen, behandeln wir wie Sie vorliegende inhaltlich anpassen können. Alles hier behandelte findet nun vollständig im *Material*-Ordner statt.

## Beispiele

In den Dateien *Material/Inhalte/1I_Einfuehrung.qmd*, *Material/Begleitdokumente/1B_Einfuehrung.qmd*, *Material/Uebungen/Aufgabenblaetter/1A_content.qmd* und *Material/Cheatsheet/Cheatsheet.qmd* finden Sie bereits alle grundlegenden Beispielstrukturen dazu wie Sie Ihre .qmd-Dateien inhaltlich füllen können.

## Auslagern

Bestimmte Inhalte sollten dabei nicht in die .qmd-Dateien selbst geschrieben, sondern ausgelagert werden.

Bilder sollen in den Bilderordner *Material/Bilder* und auf sie soll mit folgender Syntax gezeigt werden:

```markdown
![](Pfad/Bilder/bild.png){width=300}
```

Code soll in den Code-Ordner *Material/Code* und auf diesen soll mit folgender Syntax gezeigt werden, am Beispiel von Pythoncode:

Wenn der Code ausgeführt angezeigt werden soll:

``````markdown
```{python}
#| echo: false
{{< include "Pfad/Code/code.py" >}}
```
``````

Wenn der Code selbst angezeigt werden soll:

``````markdown
```{.python}
{{< include "Pfad/Code/code.py" >}}
```
``````

Am besten werden für eine bessere Übersichtlichkeit sowohl im Bilder- als auch ganz besonders im Code-Order thematisch geordnete Unterordner verwendet. Standardmäßig ist das beispielsweise der *Beispiel*-Ordner *Material/Code/Beispielcode*.

## Navigation

[Vorseite](./quarto-dateien.md) / [Nachseite]()
