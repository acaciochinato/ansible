workstation_install
=========

I created this role to automate the process of configuring my workstations from a fresh RHEL/Debian/openSUSE installation. In my original (and personal) role I have more tasks personalized to my own use. So this repo only contains the tasks that (to me) makes sense for everyone who's after their Fresh OS Install and wants to:

- Add one or more users to the system
- Add more repositories to their system (Adjusting the variables in defaults/main.yml)
- Install some python modules
- Use Oh-My-ZSH as their default SHELL
- Have default folders installed on their $HOME path
- Use NFS for network sharing
- Have Logitech's MX Master 3 and wants it configured and ready to be used in their systems
- That's IT!!!!

Requirements
------------

- Root privileges on the target host
- RHEL Based distros
- Debian
- OpenSUSE Leap/Tumbleweed

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