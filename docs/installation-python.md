# Python installieren

## Linux

### Debian / Ubuntu

```bash
sudo apt update
sudo apt install python3 python3-pip python3-venv
```

`python3-venv` stellt die Unterstützung für virtuelle Python-Umgebungen bereit.

Installation prüfen:

```bash
python3 --version
python3 -m pip --version
```

### Fedora

```bash
sudo dnf install python3 python3-pip
```

Fedora stellt `pip` über das Paket `python3-pip` bereit.

Installation prüfen:

```bash
python3 --version
python3 -m pip --version
```

### Arch Linux

```bash
sudo pacman -S python python-pip
```

Arch Linux stellt Python über `python` und pip über `python-pip` bereit.

Installation prüfen:

```bash
python --version
python -m pip --version
```

---

## macOS

Auf macOS kann Python über den offiziellen Installer von Python.org installiert werden. Die offiziellen Installer unterstützen sowohl Apple-Silicon- als auch Intel-Macs.

Nach der Installation:

```bash
python3 --version
python3 -m pip --version
```

### Alternativ mit Homebrew

Falls Homebrew bereits installiert ist:

```bash
brew install python
```

Danach:

```bash
python3 --version
python3 -m pip --version
```

Das von macOS beziehungsweise den Apple-Entwicklertools bereitgestellte System-Python sollte nicht verändert oder entfernt werden.

---

## Windows

Unter Windows kann Python direkt über `winget` installiert werden. Microsoft empfiehlt aktuell Python 3.14 als stabile Version.

PowerShell oder Windows Terminal öffnen:

```powershell
winget install Python.Python.3.14
```

Danach das Terminal schließen und erneut öffnen.

Installation prüfen:

```powershell
python --version
python -m pip --version
```

Alternativ kann der offizielle **Python Install Manager** von Python.org verwendet werden. Nach dessen Installation stehen unter anderem die Befehle `python` und `py` zur Verfügung.

---

## Virtuelle Umgebung erstellen

Für einzelne Projekte sollte eine virtuelle Umgebung verwendet werden, damit Abhängigkeiten voneinander getrennt bleiben. Python empfiehlt dieses Vorgehen insbesondere für projektbezogene Installationen.

### Linux / macOS

```bash
python3 -m venv .venv
source .venv/bin/activate
```

Bei Arch Linux gegebenenfalls:

```bash
python -m venv .venv
source .venv/bin/activate
```

### Windows

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

Anschließend können Pakete innerhalb der Umgebung installiert werden:

```bash
python -m pip install <paket>
```

Virtuelle Umgebung verlassen:

```bash
deactivate
```

## Navigation

[Zurück zum Installationsdokument](./installation.md)

