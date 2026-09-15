# Installation

In diesem Abschnitt wird das Aufsetzen der Umgebung zum Nutzen der Template behandelt.

## Vorwort zur Installation

Um ein Projekt, welches auf der *HsH Full Lecture Template* basiert aufzusetzen und betriebsbereit zu machen, bedarf es verschiedener Programme. Wie genau diese auf welchem Betriebssystem installiert werden ändert sich häufig. Daher wurde sich beim verfassen dieser Dokumentation dazu entschieden, nur auf die Installations-Dokumentationen der zugrundeliegenden Technologien zu verweisen. Es wird hierfür empfohlen KI zur Hilfe zu nehmen.

## Repository lokal ziehen

[Installieren Sie sich git](./installation-git.md) und ziehen Sie sich das Repository mit

```bash
git clone https://github.com/HSH-LeMaPy/hsh-full-lecture-template
```

lokal auf Ihren Rechner. Navigieren Sie dann in den Ordner und betrachten Sie die vor sich liegenden Dateien.

## Aufsetzen über Nix (Linux und MacOS)

Wenn Sie Linux oder einen Mac nutzen (oder [WSL](https://learn.microsoft.com/en-us/windows/wsl/about) auf Windows nutzen möchten), wird empfohlen das Projekt über [Nix](https://nixos.org/) aufzusetzen. Nix ist vereinfacht gesagt ein Werkzeug für reproduzierbare Entwicklungsumgebungen und daher praktisch, dass damit alle die an einem Projekt arbeiten, die selben Versionen und Abhängigkeiten nutzen.

Dabei reicht es, dass eine Person bei Bedarf auch mit hilfe einer KI, eine sogenannte *Nix Flake* definiert bzw die bereits definierte pflegt und alle anderen diese nur ausführen.

Zunächst sollten Sie sich [Nix installieren](./installation-nix.md).

Jetzt müssen Sie über das Terminal in den Ordner in dem Sie das git Projekt haben navigieren und dann in den Unterordner *Routinen* gehen. Führen Sie dann folgenden Befehl aus:

```bash
nix develop
```

Damit ist die Installation abgeschlossen.

## Aufsetzen über Einzelinstallationen (Windows, Linux und MacOS)

Diese Methode ist deutlich mehr Arbeit und fehleranfälliger, weswegen empfohlen wird auf Linux und Mac erstere anzuwenden.

Installieren Sie sich zunächst folgende Programme:

- [Quarto hinstallieren](./installation-quarto.md)
- [Python installieren](./installation-python.md)

Außerdem benötigen Sie einen Chromium basierten Browser auf Ihrem System. Die meisten haben das mit Google Chrome bereits, wenn nicht, sollten Sie sich noch Chromium installieren:

- [Chromium installieren](./installation-chromium.md)

Als nächstes benötigen Sie alle Python-Packages die Sie in dem Projekt verwenden möchten. Um zukünftig auch die .ipynb-Dateien als ganzes ausführen zu können, sind dabei besonders die folgenden beiden Empfohlen:

```bash
pip install ipykernel jupyter
```

## Installation prüfen

Um die Installation nun zu prüfen, führen Sie die Befehle aus dem Dokument *render_website.ipynb* aus. 

## Navigation

[Vorseite](./README.md) / [Nachseite]()
