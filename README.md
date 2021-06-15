# ansible-roles
Various roles I've written for basic automation of tasks.  I will randomly add to this as I find things I get tired of repeatedly doing.

## Setting up
- Create a parent folder for your inventory and playbooks.
- Clone this into that folder.
- Playbooks can call various roles.

Directory structure will be similar to:

Ansible (Parent Folder)
  \- Roles (this repo)
  \- inventory.ini
  \- RunCentosUpdates.yaml
  \- SomeOtherPlaybook.yaml

### Example
For a playbook called RunCentosUpdates.yaml:
```
---
- name: Update centos hosts
  hosts: centos
  roles:
    - updateCentos
```