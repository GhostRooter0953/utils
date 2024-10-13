# utils

Simple role which just setups some handy packages plus some changes for MC configuration.

## Usage (example)

### Full (installs default packages and applies tweaks)

```yaml
    - role: utils
```

### Install default and custom packages

```yaml
    - role: utils
      utils_setup: install
      utils_custom_packages: [htop, apg]
```

### Install only custom packages

```yaml
    - role: utils
      utils_setup: install
      utils_packages: []
      utils_custom_packages: [htop, apg]
```

## Available parameters

| Param | Default | Description |
| -------- | -------- | -------- |
| `utils_setup` | `full` | Setup mode |
| `utils_apt.disable_install_recomends` | `true` | Disables install Recommends and Suggests by default |
| `utils_cloudinit.disable_users` | `true` | Disables default "ubuntu" or other user by cloudinit |
| `utils_dpkg.enable_manpages` | `false` | Removes dpkg filters, don't skip man pages on package installation |
| `utils_tweaks.motd_warning` | `true` | Adds colored warning in /etc/motd |
| `utils_packages` | See list below | Installs default utils packages |
| `utils_custom_packages` | `[]` | Installs custom utils packages |

### Default utils pacakges

- bash-completion
- cron
- curl
- dnsutils
- iproute2
- iputils-ping
- less
- logrotate
- lsof
- mc
- mtr-tiny
- nano
- ncurses-term
- netcat
- net-tools
- pbzip2
- rsync
- screen
- strace
- sysstat
- tcpdump
- telnet
- tmux
- unzip
- wget

## FAQ

...

## Useful links

- ...

## TODO

- Customize colors for motd
