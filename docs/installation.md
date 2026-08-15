# Installation

## Vorwort zur Installation

Um ein Projekt, welches auf der *HsH Full Lecture Template* basiert aufzusetzen, bedarf es verschiedener Programme. Wie genau diese auf welchem Betriebssystem installiert werden ändert sich häufig. Daher wurde sich beim verfassen dieser Dokumentation dazu entschieden, nur auf die Installations-Dokumentationen der zugrundeliegenden Technologien zu verweisen. Es wird hierfür empfohlen KI zur Hilfe zu nehmen.

## Repository lokal ziehen
Installieren Sie sich [git](https://git-scm.com/install/) und ziehen Sie sich das Repository mit

```bash
git clone https://github.com/HSH-LeMaPy/hsh-full-lecture-template
```

lokal auf Ihren Rechner. Navigieren Sie dann in den Ordner und betrachten Sie die vor sich liegenden Dateien.

## Aufsetzen über Nix (Linux und MacOS)

Wenn Sie Linux oder einen Mac nutzen (oder [WSL](https://learn.microsoft.com/en-us/windows/wsl/about) auf Windows nutzen möchten), wird empfohlen das Projekt über [Nix](https://nixos.org/) aufzusetzen. Nix ist vereinfacht gesagt ein Werkzeug für reproduzierbare Entwicklungsumgebungen und daher praktisch, dass damit alle die an einem Projekt arbeiten, die selben Versionen und Abhängigkeiten nutzen.

Dabei reicht es, dass eine Person bei Bedarf auch mit hilfe einer KI, eine sogenannte *Nix Flake* definiert bzw die bereits definierte pflegt und alle anderen diese nur ausführen.

Zunächst sollten Sie sich [Nix](https://nixos.org/download/) installieren.

Jetzt müssen Sie über das Terminal in den Ordner in dem Sie das git Projekt haben navigieren und dann in den Unterordner *Routinen* gehen. Führen Sie dann folgenden Befehl aus:

```bash
nix develop
```

Damit ist die Installation abgeschlossen.

## Installation prüfen


