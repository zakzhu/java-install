# Java-Install

[![build status][shield-build]][info-build]
[![gitter room][shield-gitter]][info-gitter]
[![license][shield-license]][info-license]
[![release][shield-release]][info-release]
[![prs welcome][shield-prs]][info-prs]

Ansible playbook for java installation.

[TOC]

## Features



## Requirements

- **Platforms:**
  - CentOS-7
  - Fedora
- **Dependencies:**
  - ansible

## Installation

```bash
yum -y install ansible
```

```bash
git clone https://github.com/zakzhu/java-install.git
```

## Usage

```bash
vim java-install/inventories/production/host_vars/localhost.yml
```

> EXAMPLE:
>
> ```yaml
> 
> ```

```bash
ansible-playbook -i inventories/production/inventory site.yml
```

```bash
source /etc/profile
```

## Contributing

See the [contribution guide][info-contribute].

## Frequently asked questions

Please see [FAQ.md][info-faq] for frequently asked questions.

## Thanks

The following excellent people helped massively:

- [Rowan Manning](https://rowanmanning.com)

## License

Java-Install is licensed under the [BSD-3-Clause][info-license] license.
Copyright &copy; 2020, Zak Zhu

[info-build]: https://travis-ci.org/github/zakzhu/java-install
[info-contribute]: CONTRIBUTING.md
[info-faq]: FAQ.md
[info-gitter]: https://gitter.im/zakzhu/java-install
[info-license]: LICENSE
[info-release]: https://github.com/zakzhu/java-install/releases
[info-prs]: https://github.com/zakzhu/java-install/pulls

[shield-build]: https://img.shields.io/travis/zakzhu/java-install
[shield-gitter]: https://img.shields.io/gitter/room/zakzhu/java-install
[shield-license]: https://img.shields.io/github/license/zakzhu/java-install
[shield-release]: https://img.shields.io/github/v/release/zakzhu/java-install
[shield-prs]: https://img.shields.io/badge/PRs-welcome-brightgreen
