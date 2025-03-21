# Home Lab and Server Ansible Playbooks

## Ansible Playbooks to help you set up your own server at home

These playbooks will configure and update Ubuntu, install Docker, and deploy the containers on two seperate machines.
It uses Traefik as it's reverse proxy manager and Authelia for Two Factor Authentication. See the services list [here](serviceslist.md). Most of the services will be accessible at https://\<service>.\<yourdomain>

**Important**: Make sure you set SSL/TLS encryption mode to **full** in Cloudflare.

## Acknowledgments

This project uses [Nick G's Ansible-Homeserver.](https://github.com/nickjg1/homeserver-ansible) as the template.

## Prerequisites

In order for you to use these playbooks, you'll need a couple things:

- Basic knowledge of internet protocols (SSH, TCP/UDP etc.), Ansible and Linux
- Router with ports 80 and 443 forwarded to your servers IP address
- Google Account
- Domain name
- Cloudflare account with your domain name [nameservers](https://www.youtube.com/watch?v=uqlo3lCqiy0) pointed to their DNS Servers
- A fresh install of Ubuntu Server LTS 22.04


## Notes and Disclaimers

This playbook opens one server up to the internet and potentially malicious attacks. Two factor authentication, Cloudflare and [Jeff Geerling's Security Role](https://github.com/geerlingguy/ansible-role-security) offer good layers of protection, but it's always good practice to be mindful of the risks. Further configuration in Cloudflare can strengthen your security.

This also changes the default listening port of SSH to 69. It can be changed in `group_vars/all/vars.yml`.

## Installation

Run this command, enter your sudo password and vault password when prompted:

```bash
ansible-playbook run.yml -K --ask-vault-pass
```

## Credit

- [Nick G](https://github.com/nickjg1)
- [Rishav Nandi](https://github.com/rishavnandi)
- [Jeff Geerling](https://github.com/geerlingguy)
