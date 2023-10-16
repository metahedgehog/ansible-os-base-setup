# Ansible Playbook for System Setup on Debian/RHEL-based Systems

This Ansible playbook automates the setup of Debian or RHEL-based systems with the following tasks:

User Creation: Generates a random username and sets up a user account with a secure password.
Sudo Configuration: Configures sudo access for the newly created user.
Adding User to Sudo Group: Ensures the user is part of the sudo group.
Package Updates: Updates system packages to the latest versions.
Firewall Installation: Installs and configures a firewall (e.g., UFW or firewalld) for enhanced security.

Example usage:

```bash
ansible-playbook -i inventory.ini setup-system.yml -e "ansible_become_pass=<your_root_password" -e "ansible_user=root" -e "upassword=<your_password"
```
