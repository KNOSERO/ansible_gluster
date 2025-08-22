# Ansible Gluster
Script for installing and configuring gluster in Ansible

## Example

```yaml
---
- name: Install gluster
  hosts: all
  become: yes
  vars:
    glusterfs_servers:
      - 192.168.0.2
      - 192.168.0.3
    glusterfs_mounts:
      - { volume: gluster, mountpoint: /mnt/gluster }

  tasks:
    - name: Run install_gluster.yml
      include_tasks: ./task/ansible_gluster/playbook.yml
```