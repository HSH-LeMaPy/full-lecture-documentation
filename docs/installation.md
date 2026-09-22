# Installation

In diesem Abschnitt wird das Aufsetzen der Umgebung zum Nutzen der Template behandelt.

## Vorwort zur Installation

Um ein Projekt, welches auf der *Full Lecture Template* basiert aufzusetzen und betriebsbereit zu machen, bedarf es verschiedener Programme. Wie genau diese auf welchem Betriebssystem installiert werden ändert sich häufig. Daher wurde sich beim verfassen dieser Dokumentation dazu entschieden, nur auf die Installations-Dokumentationen der zugrundeliegenden Technologien zu verweisen. Es wird hierfür empfohlen KI zur Hilfe zu nehmen.

## Repository lokal ziehen

[Installieren Sie sich git](./installationen/installation-git.md) und initialisieren Sie ein neues Repository.

Ziehen Sie sich jetzt das Template lokal in diesen Ordner. Wenn Sie Quarto bereits installiert haben, können Sie das hiermit machen:

```bash
quarto use template HSH-LeMaPy/full-lecture-template
```

Alternativ können Sie auch auf GitHub navigieren und es als Zip im Ordner entpacken oder mit git clone in den Ordner ziehen. Dabei müssen Sie dann aber beachten, dass Sie für ein neues repo .git einmal löschen und neu aufsetzen müssten, sonst pushen Sie auf die Template.

```bash
git clone https://github.com/HSH-LeMaPy/full-lecture-template.git full-lecture-template
cd full-lecture-template
rm -rf .git
git init
```

lokal auf Ihren Rechner. Navigieren Sie dann in den Ordner und betrachten Sie die vor sich liegenden Dateien.

## Aufsetzen über Nix (Linux und MacOS)

Wenn Sie Linux oder einen Mac nutzen (oder [WSL](https://learn.microsoft.com/en-us/windows/wsl/about) auf Windows nutzen möchten), wird empfohlen das Projekt über [Nix](https://nixos.org/) aufzusetzen. Nix ist vereinfacht gesagt ein Werkzeug für reproduzierbare Entwicklungsumgebungen und daher praktisch, dass damit alle die an einem Projekt arbeiten, die selben Versionen und Abhängigkeiten nutzen.

Dabei reicht es, dass eine Person bei Bedarf auch mit hilfe einer KI, eine sogenannte *Nix Flake* definiert bzw die bereits definierte pflegt und alle anderen diese nur ausführen.

Zunächst sollten Sie sich [Nix installieren](./installationen/installation-nix.md).

Jetzt müssen Sie über das Terminal in den Ordner in dem Sie das git Projekt haben navigieren und dann in den Unterordner *Routinen* gehen. Führen Sie dann folgenden Befehl aus:

```bash
nix develop
```

Damit ist die Installation abgeschlossen.

## Aufsetzen über Einzelinstallationen (Windows, Linux und MacOS)

Diese Methode ist deutlich mehr Arbeit und fehleranfälliger, weswegen empfohlen wird auf Linux und Mac erstere anzuwenden.

Installieren Sie sich zunächst folgende Programme:

- [Quarto hinstallieren](./installationen/installation-quarto.md)
- [Python installieren](./installationen/installation-python.md)

Außerdem benötigen Sie einen Chromium basierten Browser auf Ihrem System. Die meisten haben das mit Google Chrome bereits, wenn nicht, sollten Sie sich noch Chromium installieren:

- [Chromium installieren](./installationen/installation-chromium.md)

Als nächstes benötigen Sie alle Python-Packages die Sie in dem Projekt verwenden möchten. Um zukünftig auch die .ipynb-Dateien als ganzes ausführen zu können, sind dabei besonders die folgenden beiden Empfohlen:

```bash
pip install ipykernel jupyter
```

## Installation prüfen

Um die Installation nun zu prüfen, führen Sie die Befehle aus dem Dokument *render_website.ipynb* aus. 

## Extensions ggf aktualisieren

Falls sich beispielsweise etwas an den Extensions ändert, führen Sie folgenden Befehl zum aktualisieren Ihrer lokalen Extensions aus:

```bash
quarto update HSH-LeMaPy/full-lecture-template
```

Das dürfte nur sehr selten notwendig sein, da sich die Extensions nur selten ändern.

## Navigation

[Vorseite](./README.md) / [Nachseite](./anwendung-aus-studierendenperspektive.md)
