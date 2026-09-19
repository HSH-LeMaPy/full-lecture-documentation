# Nix installieren – nur zum Ausführen von Flakes

Diese Anleitung richtet Nix so ein, dass es ausschließlich als Laufzeit für Nix Flakes verwendet werden kann. Nix ersetzt dabei **nicht** den normalen Paketmanager des Systems.

Die empfohlenen offiziellen Installationen verwenden unter Linux und macOS den Multi-User-Modus.

## Linux

### 1. Nix installieren

```bash
sh <(curl -L https://nixos.org/nix/install) --daemon
```

Danach das Terminal neu öffnen oder die Shell-Konfiguration neu laden.

Prüfen, ob Nix verfügbar ist:

```bash
nix --version
```

### 2. Flakes verwenden

Flakes und die moderne `nix`-CLI können direkt pro Befehl aktiviert werden:

```bash
nix --experimental-features 'nix-command flakes' run .
```

Dadurch ist keine permanente Änderung an der Nix-Konfiguration notwendig. Die Nix-Dokumentation unterstützt das Aktivieren von `nix-command` und `flakes` direkt über diesen Parameter.

Falls die Flake eine bestimmte App exportiert:

```bash
nix --experimental-features 'nix-command flakes' run .#app
```

---

## macOS

### 1. Nix installieren

Im Terminal:

```bash
sh <(curl -L https://nixos.org/nix/install) --daemon
```

Die Multi-User-Installation ist auch unter macOS die empfohlene Variante.

Danach das Terminal neu öffnen und prüfen:

```bash
nix --version
```

### 2. Flakes verwenden

Eine lokale Flake ausführen:

```bash
nix --experimental-features 'nix-command flakes' run .
```

Eine bestimmte App aus einer Flake ausführen:

```bash
nix --experimental-features 'nix-command flakes' run .#app
```

`nix run` baut die von der Flake bereitgestellte Anwendung und führt sie anschließend aus.

---

## Windows mit WSL

Nix wird unter Windows **innerhalb von WSL** installiert. Die folgenden Befehle werden daher nicht in PowerShell oder `cmd.exe`, sondern im Linux-Terminal von WSL ausgeführt.

### 1. WSL installieren

PowerShell als Administrator öffnen:

```powershell
wsl --install
```

Anschließend Windows gegebenenfalls neu starten und die eingerichtete Linux-Distribution öffnen.

### 2. Nix innerhalb von WSL installieren

Im WSL-Terminal:

```bash
sh <(curl -L https://nixos.org/nix/install) --daemon
```

Danach WSL neu starten:

```powershell
wsl --shutdown
```

Anschließend die Linux-Distribution erneut öffnen und prüfen:

```bash
nix --version
```

### 3. Flakes verwenden

Im WSL-Terminal:

```bash
nix --experimental-features 'nix-command flakes' run .
```

Oder für eine bestimmte App:

```bash
nix --experimental-features 'nix-command flakes' run .#app
```

---

## Optional: Flakes dauerhaft aktivieren

Wenn nicht bei jedem Aufruf

```text
--experimental-features 'nix-command flakes'
```

angegeben werden soll, können die Features dauerhaft aktiviert werden.

Bei einer Multi-User-Installation:

```bash
sudo mkdir -p /etc/nix
sudo nano /etc/nix/nix.conf
```

Folgende Zeile hinzufügen:

```ini
experimental-features = nix-command flakes
```

Danach den Nix-Daemon beziehungsweise die Sitzung neu starten.

Anschließend reicht:

```bash
nix run .
```

oder:

```bash
nix run .#app
```

## Verwendung

In ein Repository mit einer `flake.nix` wechseln:

```bash
cd mein-projekt
```

Die Standard-App der Flake starten:

```bash
nix run .
```

Alternativ kann eine Flake auch direkt über eine Flake-Referenz ausgeführt werden, beispielsweise aus einem Git-Repository. Flakes können sowohl lokale Pfade als auch Referenzen wie GitHub-Repositories verwenden.

## Wichtig

Nix muss für diesen Anwendungsfall **nicht als allgemeiner Paketmanager verwendet werden**.

Insbesondere ist es nicht notwendig, Pakete dauerhaft mit Nix zu installieren. Für Projekte, die eine ausführbare Flake bereitstellen, genügt normalerweise:

```bash
nix run .
```

Nix lädt die benötigten Abhängigkeiten in den Nix Store, baut beziehungsweise lädt das entsprechende Flake-Output und führt anschließend die Anwendung aus.

## Navigation

[Zurück zum Installationsdokument](./../installation.md)
