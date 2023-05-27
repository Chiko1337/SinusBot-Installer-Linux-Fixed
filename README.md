# SinusBot Installer for Linux

## Officially supported Linux distributions

- Debian 11+
- Ubuntu 20.04+

## Installation

```bash
bash <(wget --no-check-certificate -O - 'https://raw.githubusercontent.com/Chiko1337/SinusBot-Installer-for-Ubuntu-22.04-Debian-11-YT-DLP-/main/sinusbot_installer.sh')
```

This command basically downloads the latest version of the installer-script and executes it via the bash.

## Features

- Install the SinusBot to a selected folder
  - Automatic = /opt/sinusbot
  - or own dir
- Update the SinusBot and youtube-dl
- Reset the password
- Uninstall the bot

The following tasks will be done:

- Checks if the linux distribution is supported
- Installs the latest supported version of the teamspeak client
- Installs all the necessary dependencies
- Creates a separated user
- Installs the latest SinusBot version
- Installs youtube-dl
- Adds a cronjob for daily youtube-dl update
- Sets all the file permissions correctly
- Generates startup files:
  - systemd file => `service sinusbot {start|stop|restart|status}`
  - init.d => `/etc/init.d/sinusbot {start|stop|restart}`
- Removes all temporary files
- Starts the SinusBot after installation

The duration of the installation process depends on your system (how many packages need to be updated, internet connection, processing power) but typically takes about one to five minutes.

## Contribution

If you want to contribute, the sourcecode is formatted with the [shell-format](https://marketplace.visualstudio.com/items?itemName=foxundermoon.shell-format) extension from VS Code.
