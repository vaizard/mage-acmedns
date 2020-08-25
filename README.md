# mage-acmedns
Ansible role to deploy ACME-DNS. This role uses the 

- mage-podman role (https://github.com/vaizard/mage-podman/) and the
- containers/podman collection (see install instructions here https://github.com/containers/ansible-podman-collections#installing-the-collection-from-ansible-galaxy)

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

If you run up into issues, look at mage-podman documentation.
This role intentionally uses podman just for the fun of it. Supporting acme-dns without podman is dead simple, PRs to implement it as well as a side-by-side options are welcome.