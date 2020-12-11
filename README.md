# Java-Install

<!-- [![build status][shield-build]][info-build] -->

<!-- [![gitter room][shield-gitter]][info-gitter] -->

[![license][shield-license]][info-license]
[![release][shield-release]][info-release]
[![prs welcome][shield-prs]][info-prs]

Ansible playbook for java installation.

[TOC]

## Features

Support java distribution type:

- Adopt OpenJDK
- Alibaba Dragonwell
- Amazon Corretto
- Liberica OpenJDK
- Tencent Kona
- Oracle JDK

## Requirements

- **Platforms:**
  - CentOS-7
  - Fedora
- **Dependencies:**
  - ansible

## Installation

- ```bash
  yum -y install ansible
  ```

- ```bash
  git clone https://github.com/zakzhu/java-install.git
  ```

- Download the relevant openjdk tarball from the following website:

  > ```yaml
  > # JDK Pacakge Name:
  > #   - Adopt OpenJDK         https://github.com/AdoptOpenJDK/openjdk8-binaries/releases
  > #   - Alibaba Dragonwell    https://github.com/alibaba/dragonwell8/releases
  > #   - Amazon Corretto       https://docs.aws.amazon.com/corretto/latest/corretto-8-ug/downloads-list.html
  > #   - Liberica OpenJDK      https://bell-sw.com/pages/downloads/#/java-8-lts
  > #   - Tencent Kona          https://github.com/Tencent/TencentKona-8/releases
  > #   - Oracle JDK            https://www.oracle.com/java/technologies/javase/javase8-archive-downloads.html
  > ```

- ```bash
  cp OPENJDK-TARBALL java-install/roles/get_pkg/files/
  ```

## Usage

```bash
vim java-install/inventories/staging/host_vars/localhost.yml
```

> EXAMPLE:
>
> ```yaml
> ########################
> # Adopt OpenJDK
> ########################
> package:
>   name: adopt-openjdk
>   version: 8u275b01
>   checksum: 06fb04075ed503013beb12ab87963b2ca36abe9e397a0c298a57c1d822467c29
>
> package_tarball: "OpenJDK8U-jdk_x64_linux_hotspot_8u275b01.tar.gz"
> dgst_algo: sha256
> ```

```bash
ansible-playbook -i inventories/staging/inventory site.yml
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
