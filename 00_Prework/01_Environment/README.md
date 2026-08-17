# Environment setup

Install the toolchain the labs assume: Python 3.11+, git, and a code editor
with an AI assistant. Then create the course virtual environment.

Everything below is per-platform; find your operating system.

## Windows

Install with winget from an Administrator PowerShell:

```powershell
winget install Python.Python.3.12
winget install Git.Git
```

Then create and activate the course environment:

```powershell
py -m venv .venv
.venv\Scripts\Activate.ps1
pip install jupyter
```

If script activation is blocked, run
`Set-ExecutionPolicy -Scope CurrentUser RemoteSigned` once and reopen the
terminal.

## macOS

Install with Homebrew:

```bash
brew install python@3.12 git
```

Then create and activate the course environment:

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install jupyter
```

## Linux

Use your distribution's packages (Debian/Ubuntu shown):

```bash
sudo apt update && sudo apt install -y python3 python3-venv git
python3 -m venv .venv
source .venv/bin/activate
pip install jupyter
```

## Verify

On every platform, this must print a 3.11+ version and open Jupyter:

```bash
python --version
jupyter lab
```
