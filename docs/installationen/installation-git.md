# Git installieren

## Linux

### Debian / Ubuntu

```bash
sudo apt update
sudo apt install git
```

### Fedora

```bash
sudo dnf install git
```

### Arch Linux

```bash
sudo pacman -S git
```

Installation prüfen:

```bash
git --version
```

---

## macOS

Git kann über die Xcode Command Line Tools installiert werden:

```bash
xcode-select --install
```

Anschließend prüfen:

```bash
git --version
```

Alternativ kann Git mit Homebrew installiert werden:

```bash
brew install git
```

---

## Windows

Git kann über `winget` installiert werden.

PowerShell oder Windows Terminal öffnen und ausführen:

```powershell
winget install --id Git.Git -e
```

Anschließend das Terminal neu öffnen und die Installation prüfen:

```powershell
git --version
```

Alternativ kann **Git for Windows** über den offiziellen Installer installiert werden.

---

## Grundkonfiguration

Nach der Installation sollten einmal der Name und die E-Mail-Adresse für Commits gesetzt werden:

```bash
git config --global user.name "Max Mustermann"
git config --global user.email "max@example.com"
```

Konfiguration prüfen:

```bash
git config --global --list
```

---

## Repository klonen

Ein Git-Repository kann anschließend mit folgendem Befehl geklont werden:

```bash
git clone <repository-url>
```

Danach in das Repository wechseln:

```bash
cd <repository>
```

## Navigation

[Zurück zum Installationsdokument](./../installation.md)
