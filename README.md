# ansible-discourse
Ansible tools for Discourse management

## discourse-updater
[discourse-updater.yml](https://github.com/pacharanero/ansible-discourse/blob/master/discourse-updater.yml) will update an Ubuntu Server and then update Discourse using the Pull from GitHub, `./launcher rebuild app` method, finishing by cleaning up stopped Docker containers and then rebooting the server.

### assumptions:
* assumes you have Ansible installed
* assumes you have set up an [Ansible Inventory](https://docs.ansible.com/ansible/latest/network/getting_started/basic_concepts.html?highlight=inventory#inventory) on your 'controller' machine, in `/etc/ansible/hosts`.
* assumes you have a list of `[discourses]` defined in this inventory.
* assumes you have already set up SSH credentials to log into the Discourse instances

### usage:
`$ git clone` this repo to `<somedir>`  
`$ cd <somedir>`  
`$ ansible-playbook discourse-updater.yml`  

------

### CONTRIBUTING
* Please create issues in https://github.com/pacharanero/ansible-discourse/issues
* I'm very happy to accept improvements via PR (you know what to do)
* Feature requests also considered.

### LICENSE
* MIT
