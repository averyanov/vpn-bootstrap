## About

[![Build Status](https://jenkins.gongled.me/buildStatus/icon?job=vpn-bootstrap)](https://jenkins.gongled.me/job/vpn-bootstrap)

Ansible roles which helps you setup IPSec/L2TP VPN on [Digital Ocean](https://digitalocean.com) droplet.

## Features

- [x] IPSec via OpenSwan
  - [x] PSK authentication
  - [ ] Certificate-based authentication
- [ ] StrongSwan
  - [ ] PSK authentication
  - [ ] Certificate-based authentication
- [x] PAM authentication (/etc/passwd)
- [x] L2TP via xl2tpd
- [x] sysctl
- [ ] IPTables

## Supported devices

* Windows 7+
* Ubuntu 14.04+
* Mac OS 10.9+
* iOS 8.0+
* Android 4.0+

## Requirements

* Ubuntu 12.04 x86_64 LTS
* Ubuntu 12.10 x86_64
* Ubuntu 13.04 x86_64
* Ubuntu 13.10 x86_64
* Ubuntu 14.04 x86_64 LTS

_It works in any region where you want to use._

## Quick install

Log in to your server as root via SSH and execute this command:

    curl -sL https://raw.githubusercontent.com/gongled/vpn-bootstrap/master/bin/vpn-bootstrap | bash -s -- username

Done. It works.

## Manual install

Log in to your server as root via SSH and execute this command:

    curl -sL https://raw.githubusercontent.com/gongled/vpn-bootstrap/master/bin/vpn-preconf | bash -s

Put custom settings in the JSON file:

    vim config.json

Run:

    ansible-playbook install.yml -c local -e @config.json

## License

MIT
