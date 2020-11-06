# Ansible Role : VM creation

Ansible Role for Canaima Project's VM creation.

This role is used to automate VMs creation in order to deploy services on them.

Requirements
------------

- Linux (Debian or RedHat/CentOS)
- Virtualbox 6.x installed
- VBoxManage installed

Example Playbook
----------------

```
- name: Create VM 'test' (CentOS)
  hosts: "{{ hosts }}"
  remote_user: "{{ user }}"
  tasks:
  - include_role:
      name: vm_creation
      tasks_from: install_centos
    vars:
      vm_ip: "{{ vm_ip }}"
      vm_name: test
      vm_memory: "{{ vm_ram }}"
```

Authors Information
------------------

* **Toréa TESSIER** - <torea.tessier2@gmail.com> - [Canaima Project](https://github.com/canaima-project)
* **Marco FRANCOIS** - <marco.francois@reseau.eseo.fr>
