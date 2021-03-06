# Logrotate Ansible role
![Logo](https://raw.githubusercontent.com/idealista/cookiecutter-ansible-role/master/logo.gif)

[![Build Status](https://travis-ci.com/idealista/logrotate_role.png)](https://travis-ci.com/idealista/logrotate_role)

This Ansible role installs logrotate in a Debian environment.

- [Getting Started](#getting-started)
  - [Prerequisities](#prerequisities)
  - [Installing](#installing)
- [Usage](#usage)
- [Testing](#testing)
- [Built With](#built-with)
- [Versioning](#versioning)
- [Authors](#authors)
- [License](#license)
- [Contributing](#contributing)

## Getting Started

These instructions will get you a copy of the role for your Ansible playbook. Once launched, it will install a [logrotate](https://github.com/logrotate/logrotate) server in a Debian system.

### Prerequisities

Ansible 2.9.x.x version installed.
Inventory destination should be a Debian environment.

For testing purposes, [Molecule](https://molecule.readthedocs.io/) with [Docker](https://www.docker.com/) as driver.

### Installing

Create or add to your roles dependency file (e.g requirements.yml):

```
- src: idealista.logrotate_role
  version: 2.0.0
  name: logrotate
```

Install the role with ansible-galaxy command:

```
ansible-galaxy install -p roles -r requirements.yml -f
```

Use in a playbook:

```
---
- hosts: someserver
  roles:
    - { role: logrotate }
```

## Usage

Look to the [defaults vars](defaults/main.yml) and [specific OS related](vars/) files to see the possible configuration vars.
*Important note about logrotate configuration*
currently, only Debian 9 (Stretch) and Debian 10 (Buster) are supported:
* In Debian 9, logrotate is triggered by the cron utility
* In Debian 10, it works as a systemd service triggered with a timer by default.

## Testing

```
$ pipenv sync
$ pipenv run molecule test
```

Note: Debian10 (Debian Buster) will be used as default linux distro if none is provided.

See [molecule.yml](https://github.com/idealista/logrotate_role/blob/master/molecule/default/molecule.yml) to check possible testing platforms.

## Built With

![Ansible](https://img.shields.io/badge/ansible-2.9.9-green.svg)
![Molecule](https://img.shields.io/badge/molecule-3.0.4-green.svg)

## Versioning

For the versions available, see the [tags on this repository](https://github.com/idealista/logrotate_role/tags).

Additionaly you can see what change in each version in the [CHANGELOG.md](https://github.com/idealista/logrotate_role/blob/master/CHANGELOG.md) file.

## Authors

* **Idealista** - *Work with* - [idealista](https://github.com/idealista)

See also the list of [contributors](https://github.com/idealista/logrotate_role/contributors) who participated in this project.

## License

![Apache 2.0 License](https://img.shields.io/hexpm/l/plug.svg)

This project is licensed under the [Apache 2.0](https://www.apache.org/licenses/LICENSE-2.0) license - see the [LICENSE](LICENSE) file for details.

## Contributing

Please read [CONTRIBUTING.md](https://github.com/idealista/logrotate_role/blob/master/.github/CONTRIBUTING.md) for details on our code of conduct, and the process for submitting pull requests to us.
