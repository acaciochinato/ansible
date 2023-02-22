rootless_podman
=========

This role ensures podman is properly configured on the target host to run in rootless mode with an unprivileged user called podman. These are the steps that's followed:

- Make sure the user podman is present
- Make sure the necessary packages are installed
- Make sure the user dependencies are met to fully function in rootless mode and with systemd

Requirements
------------

- RHEL Based distros
- The only requirement is to have root privileges on the target host

Role Variables
------------
- `podman_passwd` need's to be set hashed.
 - The correct way to store sensitive information is using Ansible Vault. To use it check this link: https://docs.ansible.com/ansible/2.8/user_guide/vault.html

Example Playbook
------------

- The role can be called with `~$ ansible <target_host> -m include_role --args name=ansible-role-rootless_podman -k`

*Remember to put the role in your role's path*

Author Information
------------
Created by Acácio Chinato - acacio.chinato@tutanota.de
02/02/2023