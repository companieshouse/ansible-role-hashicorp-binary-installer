Ansible Role: HashiCorp Binary Installer
========================================

An [Ansible Galaxy](https://galaxy.ansible.com/) role for installing one or more [HashiCorp](https://www.hashicorp.com/) tools from binary distribution packages. Signature verification is used to ensure files have not been tampered with. 

Requirements
------------

- [GnuPG](https://gnupg.org/) installed on the host(s) that the role will run against
- HashiCorp's [public key](https://www.hashicorp.com/security) imported into the GnuPG keyring

Role Variables
--------------

Variable           | Default        | Description
-------------------|----------------|-------------
`hashicorp_tools`  | *None*         | A list of dictionaries defining one or more tools to be installed. Each dictionary should include a `name` and `version` key. Refer to the `supported_tools` variable in this role for a full list of the supported tool names.

For example:

```
hashicorp_tools:
  - name: vault, version: 1.0.0
  - name: consul, version: 1.0.0
```

Example Requirements File
-------------------------

```
- src: https://github.com/companieshouse/ansible-role-hashicorp-binary-installer
  name: hashicorp
```

License
-------

MIT

