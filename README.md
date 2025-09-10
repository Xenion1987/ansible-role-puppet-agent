# template-ansible-role

[![pre-commit](https://img.shields.io/badge/pre--commit-enabled-brightgreen?logo=pre-commit)](https://github.com/pre-commit/pre-commit) ![ansible-tests](https://github.com/Xenion1987/template-ansible-role/actions/workflows/ci.yml/badge.svg)

## Replace placeholder

### `.github/workflows/ci.yml`

Replace `template-ansible-role` with the new role name.

### `.vscode/settings.json`

Update and comment in Ansible and Python path values, if required

```sh
sed -i s,WORKSPACE_PATH,${PWD}, .vscode/settings.json
```

### OPTIONAL: Copy/move `.example.envrc` to `.envrc`

Requires [`direnv`](https://direnv.net/) to be installed and hooked into your shell.

### `meta/main.yml`

Update all `meta` informations to fit to your requirements.

### `meta/argument-specs.yml`

Explain all variables within this file. This also can be used to auto-generate a `README.md` file. Follow instructions on [docs.ansible.com](https://docs.ansible.com/ansible/latest/playbook_guide/playbooks_reuse_roles.html#role-argument-validation).

### `README.md`

Replace the template repo URL `github.com/Xenion1987/template-ansible-role` with the new repo URL.
