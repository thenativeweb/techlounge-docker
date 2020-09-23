# Folge 2: Installation

- [Video der Folge 2: Installation auf Windows](https://www.youtube.com/watch?v=ne_akDsPrHg)
- [Video der Folge 2: Installation auf macOS](https://www.youtube.com/watch?v=WxO9cnQ0BQI)
- [Video der Folge 2: Installation auf Linux](https://www.youtube.com/watch?v=-UNAvc9jOsw)

In der zweiten Folge wird Docker installiert.

## Installation auf Windows

Auf Windows 10 kann Docker Desktop [heruntergeladen](https://www.docker.com/products/docker-desktop) und installiert werden.

### Automatisierte Installation

#### Windows-Features aktivieren

Folgende PowerShell-Befehle können verwendet werden, um die benötigten Windows-Features per Script zu aktivieren. Anschließend ist ein Reboot notwendig.

- WSL 2 Features

  ```shell
  PS C:\> Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux -NoRestart
  PS C:\> Enable-WindowsOptionalFeature -Online -FeatureName VirtualMachinePlatform -NoRestart
  ```

- Hyper-V und Windows-Container Features

  ```shell
  PS C:\> Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Hyper-V -All -NoRestart
  PS C:\> Enable-WindowsOptionalFeature -Online -FeatureName Containers -All -NoRestart
  ```

#### Paket-Manager

Mit dem Paket-Manager [Chocolatey](https://chocolatey.org) kann Docker Desktop per Kommando oder in einem Script installiert werden.

```shell
PS C:\> choco install -y docker-desktop
```

## Installation auf macOS

Auf macOS kann Docker Desktop [heruntergeladen](https://www.docker.com/products/docker-desktop) und installiert werden.

### Automatisierte Installation

Mit dem Paket-Manager [Homebrew](https://brew.sh/index_de) kann Docker Desktop per Kommando oder in einem Script installiert werden.

```shell
$ brew cask install docker
```

## Installation auf Linux

Auf Linux kann die Docker Engine als Linux-Paket für verschiedene Linux-Distributionen [heruntergeladen](https://download.docker.com/linux/) werden, oder anhand der [Anleitung](https://docs.docker.com/engine/install/) installiert werden.

### Convenience-Script

Mit folgendem Aufruf kann ein Script heruntergeladen werden, dass die Schritte der Anleitung automatisch durchführt.

```shell
$ curl https://get.docker.com | sh
```

## Weitere Schritte

Wiederhole die Schritte von Folge 1, um das Image, das wir auf den Docker Hub gestellt haben, lokal auf deinen Rechner herunterzuladen (`docker login` und `docker pull`). Starte einen Container (`docker run`) oder baue das Image noch einmal lokal (`docker build`).

## Wichtige Links der Folge

- [Docker](https://docker.com)
- [Docker Hub](https://hub.docker.com)
- [Docker Desktop](https://www.docker.com/products/docker-desktop)
- [Dokumentation zu Docker Desktop](https://docs.docker.com/desktop)
- [WSL 2](https://aka.ms/wsl2)
- [Visual Studio Code](https://code.visualstudio.com)
