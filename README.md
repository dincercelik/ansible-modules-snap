# Installation
This module is **NOT** included with Ansible v2.5 and below. Install with `git clone https://github.com/dincercelik/ansible-modules-snap.git`. Valid installation paths are [the playbook's library directory](http://docs.ansible.com/ansible/playbooks_best_practices.html#bundling-ansible-modules-with-playbooks), or [Ansible's modules path](http://docs.ansible.com/ansible/developing_modules.html#module-paths).

# Examples

```
- name: Install the package "hello-world"
  snap:
    name: hello-world
    state: present

- name: Install the package "hello-world" with classic confinement policy
  snap:
    name: hello-world
    state: present
    classic: yes

- name: Install the package "hello-world" from beta channel
  snap:
    name: hello-world
    state: present
    beta: yes

- name: Remove the package "hello-world"
  snap:
    name: hello-world
    state: absent

- name: Update the package "hello-world"
  snap:
    name: hello-world
    state: refresh

- name: Disable the package "hello-world"
  snap:
    name: hello-world
    state: disabled

- name: Enable the package "hello-world"
  snap:
    name: hello-world
    state: enabled
```

# Author Information

This module was created by [Dincer Celik](mailto:hello@dincercelik.com).
