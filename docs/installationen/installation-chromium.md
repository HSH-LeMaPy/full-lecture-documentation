# Chromium installieren

## Linux

### Debian

```bash
sudo apt update
sudo apt install chromium
```

Debian stellt Chromium direkt als Paket `chromium` bereit.

Installation prüfen:

```bash
chromium --version
```

### Ubuntu

Unter Ubuntu wird Chromium offiziell als Snap-Paket bereitgestellt:

```bash
sudo snap install chromium
```

Installation prüfen:

```bash
chromium --version
```

### Fedora

```bash
sudo dnf install chromium
```

Fedora stellt Chromium direkt über die Paketquellen bereit.

Installation prüfen:

```bash
chromium --version
```

### Arch Linux

```bash
sudo pacman -S chromium
```

Chromium befindet sich im offiziellen `Extra`-Repository von Arch Linux.

Installation prüfen:

```bash
chromium --version
```

---

## macOS

Falls Homebrew bereits installiert ist:

```bash
brew install --cask chromium
```

Installation prüfen:

```bash
"/Applications/Chromium.app/Contents/MacOS/Chromium" --version
```

> **Hinweis:** Der Chromium-Cask von Homebrew ist derzeit als deprecated markiert und soll ab dem **1. September 2026** deaktiviert werden.

Alternativ stellt das Chromium-Projekt offizielle Builds als Snapshots bereit. Diese müssen manuell heruntergeladen und entpackt werden.

---

## Windows

Das Chromium-Projekt stellt für Windows keine klassische Stable-Installation wie bei Google Chrome bereit. Offizielle Chromium-Builds können stattdessen als Snapshots heruntergeladen werden.

Auf der offiziellen Chromium-Download-Seite:

1. **Windows** als Plattform auswählen.
2. Den aktuellen Build auswählen.
3. Das ZIP-Archiv herunterladen.
4. Das Archiv beispielsweise nach

```text
C:\Program Files\Chromium
```

entpacken.

Chromium kann anschließend über

```text
C:\Program Files\Chromium\chrome.exe
```

gestartet werden.

In PowerShell kann die Version geprüft werden:

```powershell
& "C:\Program Files\Chromium\chrome.exe" --version
```

> Die offiziellen Chromium-Snapshots sind Entwicklungs-Builds und besitzen nicht denselben normalen Stable-Update-Prozess wie Google Chrome.

---

## Installation prüfen

Chromium starten:

### Linux

```bash
chromium
```

### macOS

```bash
open -a Chromium
```

### Windows

```powershell
& "C:\Program Files\Chromium\chrome.exe"
```

Für die Verwendung über die Kommandozeile kann zusätzlich geprüft werden:

```bash
chromium --version
```

## Navigation

[Zurück zum Installationsdokument](./../installation.md)
