workstation_install
=========

I created this role to automate the process of configuring my workstations from a fresh RHEL/Debian/openSUSE installation. In my original (and personal) role I have more tasks personalized to my own use. So, what this role do:

- Add one or more users to the system
- Add more repositories to their system (Adjusting the variables in defaults/main.yml)
- Install some python modules
- Use Oh-My-ZSH as their default SHELL
- Have default folders created on their $HOME path
- Use NFS for network sharing
- Configure Logitech MX Master 3 mouse

Requirements
------------

- Root privileges on the target host
- RHEL Based distros, Debian or OpenSUSE Leap/Tumbleweed

Role Variables
------------
- Adjust the variables to your own needs. Default variables are located in defaults/main.yml and Distro-Based variables in vars/[distro].yml

Example Playbook
------------

- The role can be called with `~$ ansible <target_host> -m include_role --args name=ansible-role-workstation-install -u [privileged_user] -K`

*Remember to put the role in your role's path*

Author Information
------------
Created by Acácio Chinato - acacio.chinato@tutanota.de
03/24/2023
