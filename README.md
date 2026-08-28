# Fedora Linux (cpak)

## Installation

```bash
cpak install github.com/containerpak/fedora
```

Create a persistent environment and open Bash:

```bash
cpak environment create --name Fedora --origin github.com/containerpak/fedora
cpak environment shell --environment Fedora --command /bin/bash
```

The environment keeps its root filesystem and private home between sessions. It has network access for `dnf`; host files, desktop services and devices are not exposed by default.
