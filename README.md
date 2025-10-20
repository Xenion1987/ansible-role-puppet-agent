# Ansible role: puppet_agent

[![Ansible Galaxy downloads](https://img.shields.io/ansible/role/d/Xenion1987/puppet_agent?label=Galaxy%20downloads&logo=ansible&color=%23096598)](https://galaxy.ansible.com/ui/standalone/roles/Xenion1987/puppet_agent)
[![Ansible Galaxy](https://img.shields.io/badge/role-puppet_agent-000000.svg?logo=ansible)](https://galaxy.ansible.com/xenion1987/puppet_agent)
[![CI](https://github.com/xenion1987/ansible-role-puppet-agent/actions/workflows/ci.yml/badge.svg)](https://github.com/xenion1987/ansible-role-puppet-agent/actions/workflows/ci.yml)
[![License](https://img.shields.io/github/license/Xenion1987/ansible-role-puppet-agent)](https://github.com/Xenion1987/ansible-role-puppet-agent/blob/main/LICENSE)
[![Maintained](https://img.shields.io/badge/Maintained-yes-success.svg)](https://github.com/Xenion1987/ansible-role-puppet-agent)
[![Molecule](https://img.shields.io/badge/tested%20with-Molecule-blue.svg)](https://github.com/ansible-community/molecule)

This role installs and configures the Puppet agent on Debian- or RedHat-like systems.

## Table of content

- [Requirements](#requirements)
- [Default Variables](#default-variables)
  - [puppet_all_auto_sign_certificate](#puppet_all_auto_sign_certificate)
  - [puppet_all_config_main](#puppet_all_config_main)
  - [puppet_all_major_version](#puppet_all_major_version)
  - [puppet_all_package_dependencies](#puppet_all_package_dependencies)
  - [puppet_all_repo_type](#puppet_all_repo_type)
  - [puppet_all_runinterval](#puppet_all_runinterval)
  - [puppet_all_server](#puppet_all_server)
  - [puppet_debian_binary_path](#puppet_debian_binary_path)
  - [puppet_debian_config_path](#puppet_debian_config_path)
  - [puppet_debian_gpg_key_url](#puppet_debian_gpg_key_url)
  - [puppet_debian_package_dependencies](#puppet_debian_package_dependencies)
  - [puppet_debian_repo_name](#puppet_debian_repo_name)
  - [puppet_redhat_binary_path](#puppet_redhat_binary_path)
  - [puppet_redhat_config_path](#puppet_redhat_config_path)
  - [puppet_redhat_gpg_key_url](#puppet_redhat_gpg_key_url)
  - [puppet_redhat_package_dependencies](#puppet_redhat_package_dependencies)
  - [puppet_redhat_repo_name](#puppet_redhat_repo_name)
- [Dependencies](#dependencies)
- [License](#license)
- [Author](#author)

---

## Requirements

- Minimum Ansible version: `2.11`

## Default Variables

### puppet_all_auto_sign_certificate

Allow to sign certs by delegated puppet server.


**_Type:_** bool<br />

#### Default value

```YAML
puppet_all_auto_sign_certificate: false
```

### puppet_all_config_main

Puppet's config file values for the `[main]` section.


**_Type:_** dict<br />

#### Default value

```YAML
puppet_all_config_main:
  runinterval: '{{ puppet_all_runinterval }}'
  server: '{{ puppet_all_server }}'
```

### puppet_all_major_version

Which Puppet major version to use. May be formatted like `"X"`, `"X.X"` or `"X.X.X"`.


**_Type:_** str<br />

#### Default value

```YAML
puppet_all_major_version: '8'
```

### puppet_all_package_dependencies

Puppet's dependencies.

**_Type:_** list<br />

#### Default value

```YAML
puppet_all_package_dependencies:
  - ca-certificates
  - gnupg2
```

### puppet_all_repo_type

Which puppet repository to use. May be either `enterprise` or `community`.


**_Type:_** str<br />

#### Default value

```YAML
puppet_all_repo_type: community
```

### puppet_all_runinterval

How long to start another Puppet run.

**_Type:_** str<br />

#### Default value

```YAML
puppet_all_runinterval: 60m
```

### puppet_all_server

Puppet Server's FQDN.

**_Type:_** str<br />

#### Default value

```YAML
puppet_all_server: puppet.domain.tld
```

### puppet_debian_binary_path

#### Default value

```YAML
puppet_debian_binary_path: /opt/puppetlabs/bin/puppet
```

### puppet_debian_config_path

#### Default value

```YAML
puppet_debian_config_path: /etc/puppetlabs/puppet/puppet.conf
```

### puppet_debian_gpg_key_url

#### Default value

```YAML
puppet_debian_gpg_key_url: https://apt.puppet.com/DEB-GPG-KEY-future
```

### puppet_debian_package_dependencies

#### Default value

```YAML
puppet_debian_package_dependencies:
  - apt-transport-https
```

### puppet_debian_repo_name

#### Default value

```YAML
puppet_debian_repo_name: https://apt.puppet.com
```

### puppet_redhat_binary_path

#### Default value

```YAML
puppet_redhat_binary_path: /opt/puppetlabs/puppet/bin/puppet
```

### puppet_redhat_config_path

#### Default value

```YAML
puppet_redhat_config_path: /etc/puppetlabs/puppet/puppet.conf
```

### puppet_redhat_gpg_key_url

#### Default value

```YAML
puppet_redhat_gpg_key_url: https://yum.puppet.com/RPM-GPG-KEY-puppet
```

### puppet_redhat_package_dependencies

#### Default value

```YAML
puppet_redhat_package_dependencies: []
```

### puppet_redhat_repo_name

#### Default value

```YAML
puppet_redhat_repo_name: https://yum.puppet.com
```

## Dependencies

None.

## License

BSD, MIT

## Author

Xenion1987
