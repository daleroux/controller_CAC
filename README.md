# Ⓐ Ansible Project: controller_CAC 

For Demo purposes Configuration as Code for Controller


## Tested with Ansible

Ansible core 2.15.3.
<!-- List the versions of Ansible the collection has been tested with. Must match what is in galaxy.yml. -->
Collection: infra.controller_configuration
version:    2.5.1

## Requirements & setting up your environment: 

  - Access to an ansible controller, define the fqdn of your controller in vars/my_site.yml

  - System Administrator privileges on the controller 
         controller_username and controller_password are defined in vars/vault.yml

  - Define controller_user_default_password as well as the password for the service account 'ansible' (ansible_password) in vars/vault.yml

  - Two linux VMs with service account 'ansible'
         password for the ansible service account is defined in  vars/vault.yml.  This service account doesn't require privilege escalation. Setup the name/IP of your linux VMs in vars/controller_inventories.yml



## Running the playbook

ansible-playbook configure_controller_as_code.yml --ask-vault-pass


## End result

Organizations, Teams, Users, Roles, Inventories, Hosts, Credentials, Projects and Templates will be configured

