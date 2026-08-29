# Use Fedora Linux as a persistent environment

Install the package once:

```bash
cpak install github.com/containerpak/fedora
```

Create an environment and open Bash:

```bash
cpak environment create --name Fedora --origin github.com/containerpak/fedora
cpak environment shell --environment Fedora --command /bin/bash
```

The shell runs as root inside the environment, so Fedora packages can be installed normally:

```bash
dnf install git gcc make
```

## Persistent storage

Installed packages, system configuration and the private home directory remain available after the shell closes or the environment stops. Host files, desktop services and devices stay unavailable unless you grant them through the environment settings.

## Manage the environment

```bash
cpak environment list
cpak environment inspect --environment Fedora
cpak environment processes --environment Fedora
cpak environment stop --environment Fedora
```

Deleting the environment also deletes its installed packages, system changes and private home:

```bash
cpak environment delete --environment Fedora
```
