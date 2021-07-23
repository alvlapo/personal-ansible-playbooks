# Personal Ansible Playbooks
Ansible configuration that I use for workstations and servers

## Warning 
Please don't directly use this against your own machines, as it is something I developed for myself and may not translate to your use-case.

## Configuration
1. Create ```config/main.json``` as a copy of ```config/example.json```
2. Edit ```config/main.json```
    * `my_name` - my user name
    * `my_passwd` - a password for my user
    * `my_salt` - a salt for password hashing
    * `my_pubkey` - a public ssh key

## Run a playbook
```
ansible-playbook -u root -i inventory -e @config/main.json local.yml
```
