# Mysql 'shorcuts' Collection for Ansible

This repo hosts a 'shortcut' collection for msqyl plugins hosted in existing collections but with names too long to bother with.

## Included content

This is a 'meta' collection so it realy only includes references to other collections.

## Installation and Usage

### Installing the Collection from Ansible Galaxy

Before using the collection, you need to install it with the Ansible Galaxy CLI:

    ansible-galaxy collection install ./db.mysql.tgz

### Installing the mysql Python Library

	You can use your package manager of preferences or:

    pip3 install mysql

### Using modules in your playbooks

You can either call actions by their Fully Qualified Collection Namespace (FQCN), like `db.mysql.user`, or you can call modules by their short name if you list the `user` collection in the playbook's `collections`, like so:

```yaml
---
- hosts: localhost
  gather_facts: false
  connection: local

  collections:
    - db.mysql

  tasks:
    - name: Not to be confused with the ``user`` builtin action
      user:
		host: localhost
        password: imnottellingyou
        name: myappuser
        state: present
```

For documentation on how to use individual modules and other content included in this collection, please see the links in the 'Included content' section earlier in this README.

## Testing and Development

Some day?

## More Information

No

## License

GNU General Public License v3.0 or later

See LICENCE to see the full text.
