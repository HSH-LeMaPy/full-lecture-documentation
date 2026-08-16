# Quarto installieren

Quarto wird als eigenständige Anwendung installiert. Die aktuell stabile Quarto-Version ist **1.10.x**; die offiziellen Installer stehen für Linux, macOS und Windows zur Verfügung.

## Linux

### Debian / Ubuntu

Auf der offiziellen Quarto-Download-Seite das `.deb`-Paket für die eigene Architektur herunterladen.

Anschließend beispielsweise:

```bash
cd ~/Downloads
sudo apt install ./quarto-*.deb
```

Installation prüfen:

```bash
quarto --version
```

### Fedora / RHEL

Das passende `.rpm`-Paket von der offiziellen Quarto-Download-Seite herunterladen. Quarto stellt RPM-Pakete für Linux bereit.

Anschließend:

```bash
cd ~/Downloads
sudo dnf install ./quarto-*.rpm
```

Installation prüfen:

```bash
quarto --version
```

---

## macOS

### Mit Homebrew

Falls Homebrew bereits installiert ist:

```bash
brew install --cask quarto
```

Quarto wird offiziell als Homebrew Cask bereitgestellt.

Installation prüfen:

```bash
quarto --version
```

### Alternativ

Auf der offiziellen Quarto-Download-Seite das macOS-`.pkg` herunterladen und den Installer ausführen.

---

## Windows

Unter Windows kann Quarto über `winget` installiert werden.

PowerShell oder Windows Terminal öffnen:

```powershell
winget install --id Posit.Quarto -e
```

Das Quarto-Paket wird unter der ID `Posit.Quarto` im Windows Package Manager geführt.

Danach das Terminal neu öffnen und die Installation prüfen:

```powershell
quarto --version
```

Alternativ kann der Windows-Installer über die offizielle Quarto-Download-Seite heruntergeladen werden.

---

## Installation prüfen

Neben der Versionsabfrage kann Quarto die installierte Umgebung überprüfen:

```bash
quarto check
```

Falls Quarto zusammen mit Python verwendet werden soll, kann außerdem die Jupyter-Unterstützung geprüft werden:

```bash
quarto check jupyter
```

Quarto verwendet unter Windows den Python Launcher und unter macOS und Linux standardmäßig Python aus dem `PATH`.

---

## Quarto-Dokument testen

Eine Datei namens `test.qmd` erstellen:

```markdown
---
title: "Quarto Test"
format: html
---

# Hallo Quarto

Quarto funktioniert.
```

Anschließend rendern:

```bash
quarto render test.qmd
```

Dadurch wird eine HTML-Datei erzeugt.

## Navigation

[Zurück zum Installationsdokument](./installation.md)

