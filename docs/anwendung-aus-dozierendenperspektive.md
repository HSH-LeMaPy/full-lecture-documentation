# Anwendung aus Dozierendenperspektive

In diesem Abschnitt wird behandelt, wie das Projekt aus der Dozierendenperspektive genutzt wird. Das beinhaltet noch nicht das eigentliche Anpassen der Unterlagen. Sie können diesem Kapitel mit den Standardinhalten des Templates folgen. Auch wenn Ihnen das jetzt zu tun möglicherweise noch nicht sinnvoll erscheinen mag, stellt es eine wichtige Grundlage für zukünftige Anpassungen, beziehungsweise das eigentliche Kontrollieren dieser da.

## Website auf Moodle aufsetzen

Um die Website den Studierenden zur Verfügung zu stellen, müssen Sie den gesamten Inhalt des *_output* Ordners, bis auf den *_output/Folien* Ordners in Moodle hochladen. Über *index.html* wird die Website dann angesteuert.

## Folien nutzen

Um an die Folien zu kommen navigieren Sie in den Ordner *_output/Folien*. Hier können Sie die html Dateien nun als Folien nutzen.

## Inhalte zeitlich freischalten

Um Inhalte nicht sofort zur Verfügung zu stellen, öffnen Sie die Datei *solutions_release/solutions-release.html* in einem Texteditor (nicht im Browser!). Fügen Sie nun im bereits vorhandenem Format neue Dokumente zur Variable *releaseDates* hinzu. Ab diesem Datum werden diese Seiten dann auf der Website angezeigt.

Beispiel:
```js
// Das erste und zweite Lösungsblatt soll erst am 1. und 8. März angezeigt werden
  var releaseDates = {
    "1A_sol.html":  "2027-03-01",
    "2A_sol.html":  "2027-03-08"
  };
```

Beachten Sie aber, dass wenn man die url zum Dokument errät, man dieses trotzdem einsehen kann. *solutions-release.html* ist nur html code, welcher an das Profil *skript* rangehangen wird und damit bestimmte Seiten ausblendet, sie verschwinden nicht.

Falls Seiten wirklich unmöglich eingesehen werden sollen, können Sie nur jedes mal in *_quarto-skript.yml* und *_quarto-aufgaben.yml* die unerwünschten Dokumente auskommentieren, das Projekt dann neu rendern und schließlich neu auf Moodle hochladen. Mehr zu Renderingapassungen im übernächsten Kapitel.

## Navigation

[Vorseite](./anwendung-aus-studierendenperspektive.md) / [Nachseite](./ordnerstruktur.md)
