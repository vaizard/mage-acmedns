# mage-acmedns
Ansible role to deploy ACME-DNS. This role uses the containers/podman collection. See 
https://github.com/containers/ansible-podman-collections#installing-the-collection-from-ansible-galaxy
on how to install it.

## Usage

```
- hosts: acmedns
  strategy: free
  roles:
     - { role: mage-update }
     - { role: mage-base-common }
     - { role: mage-podman }
     - { role: mage-acmedns }
```
