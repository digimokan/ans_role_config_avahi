# ans_role_config_avahi

Configure the Avahi service/host discovery service.

[![Release](https://img.shields.io/github/release/digimokan/ans_role_config_avahi.svg?label=release)](https://github.com/digimokan/ans_role_config_avahi/releases/latest "Latest Release Notes")
[![License](https://img.shields.io/badge/license-MIT-blue.svg?label=license)](LICENSE.md "Project License")

## Table Of Contents

* [Purpose](#purpose)
* [Supported Operating Systems](#supported-operating-systems)
* [Quick Start](#quick-start)
    * [Use From Parent Role As Dependency](#use-from-parent-role-as-dependency)
* [Role Options](#role-options)
* [Contributing](#contributing)

## Purpose

* Install the [avahi](https://avahi.org/) daemon.
* Configure the avahi daemon to start at boot.
* Ensure the avahi deamon is currently running.

## Supported Operating Systems

* Arch Linux.
* FreeBSD.

## Quick Start

### Use From Parent Role As Dependency

1. List in parent role's `meta/requirements.yml`:

   ```yaml
   - src: https://github.com/digimokan/ans_role_config_avahi
   ```

2. Invoke explicitly from a task in parent role:

   ```yaml
   - name: "Install and configure Avahi"
     ansible.builtin.include_role:
       name: ans_role_config_avahi
       public: yes
     vars:
       enable_host_discovery_service: true
   ```

## Role Options

See the role `defaults` file, for overridable vars:

* [defaults/main/](../defaults/main/)

## Contributing

* Feel free to report a bug or propose a feature by opening a new
  [Issue](https://github.com/digimokan/ans_role_config_avahi/issues).
* Follow the project's [Contributing](CONTRIBUTING.md) guidelines.
* Respect the project's [Code Of Conduct](CODE_OF_CONDUCT.md).

