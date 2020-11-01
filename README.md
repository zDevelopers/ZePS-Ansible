# ZéPS – Ansible

This repository contains an Ansible playbook used to build and deploy the ZePS Core & GUI into a FreeBSD production server.

To deploy (or update) a ZePS instance, first install Ansible dependencies, then run the playbook. Python and rsync must be installed on the host; Maven and NodeJS 12+ must be available on the controller.

```console
ansible-galaxy install -r requirements.yml
ansible-playbook playbook.yml
```

This playbook will install or update the ZePS on every host from your inventory in the `zcraft` group. To deploy to Zcraft's server, add this to your inventory (e.g. `/etc/ansible/hosts`):

```ini
[zcraft]
zcraft.fr
```
