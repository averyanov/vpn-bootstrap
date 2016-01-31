## About

![vpn-bootstrap](https://raw.githubusercontent.com/gongled/vpn-bootstrap/master/vpn-bootstrap.png)

vpn-bootstrap helps you setup IPSec/L2TP server.

## Quick install

Log in to your server as superuser (root) via SSH and execute this command:

    curl -sL https://raw.githubusercontent.com/gongled/vpn-bootstrap/master/bin/vpn-bootstrap | bash -s -- username

Done. It works.

## Manual install

Log in to your server as superuser (root) via SSH and execute this command:

    curl -sL https://raw.githubusercontent.com/gongled/vpn-bootstrap/master/bin/vpn-preconf | bash -s

Put custom settings in the JSON file:

    vim config.json

Run:

    ansible-playbook install.yml -c local -e @config.json

## Supported platforms

* Ubuntu 12.04 x86_64 LTS
* Ubuntu 12.10 x86_64
* Ubuntu 13.04 x86_64
* Ubuntu 13.10 x86_64
* Ubuntu 14.04 x86_64 LTS

## License

MIT License
