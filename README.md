# Ansible Role: TightVNC and Xubuntu Desktop

This Ansible role installs the TightVNC server and the Xubuntu desktop environment. It configures the VNC server with a password and a specific port.

## Requirements

- Ansible installed
- A Debian-based system (like Ubuntu)

## Role Variables

- `vnc_user`: The user to run the VNC server 
- `vnc_password`: The password for VNC access (default "password").
- `vnc_display`: The display number for the VNC server (default: ":1").
- `vnc_port`: The port number for the VNC server (default: 5900).

## Example Playbook

```yaml
- hosts: your_target_host
  become: yes
  vars:
    vnc_user: "your_username"
    vnc_password: "your_secure_password"
    vnc_display: ":1"
    vnc_port: 5901
  roles:
    - atb-ansible-tightvnc